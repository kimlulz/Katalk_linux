# Katalk_linux
> *20251103* Remove `playonlinux` method cuz of it's deprecation and has many exploits.

> 사진 추가 예정..

✅  Most of dsitros will works

    sure it works well on rocky(el10), Arch Linux

---

## Prepare
### Install flatpak and bottles
1. `flatpak` 설치

| 배포판 | 명령어 | 비고 |
| :- | :- | :- |
| **Arch Linux**  | `sudo pacman -S flatpak` | |
| **Fedora/RHEL-Based**  | `sudo dnf install flatpak` | Fedora already has `flatpak` |
| **Debian/Ubuntu-Based**  | `sudo apt install flatpak` | |
| **Alpine**  | `sudo apk add flatpak` | |

2. flatpak 저장소 추가

`flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo`

3. bottles 설치 및 재부팅

`flatpak install flathub com.usebottles.bottles && sudo reboot`

--- 

### Configure bottles

1. bottles 실행

2. 매뉴 버튼(≡) -> Preferences -> 실행기(runner) 탭 에서 원하는 runner 설치 

3. 추가 버튼(+) -> 이름(KakaoTalk) 입력, `커스텀`, 실행기 선택 후 생성

4. bottles -> `KakaoTalk` 클릭

---

### Install

1. 한글 폰트 부재로 인해 실행 시 한글이 깨지므로 의존성(Dependencies) -> `cjkfonts` 설치

> 💡 수동으로 폰트 넣고 싶으면 `~/.var/app/com.usebottles.bottles/data/bottles/bottles/KakaoTalk/drive_c/windows/Fonts` 디렉터리에 넣으면 됨.

2. 카카오톡 설치

실행파일 실행 (Run Executable) -> 카카오톡 설치파일 선택 -> 카카오톡 설치(윈도우와 동일한 방법으로..)

3. 아이콘 만들기
-1. 아이콘 받아오기
```
# (1) Binwalk 이용하여 아이콘 추출 (`binwalk` 패키지 설치 필요)
mkdir -P ~/.local/share/icons/wine
binwalk -e KakaoTalk_Setup.exe
mv ./extractions/KakaoTalk_Setup.exe.extracted/1A380/image.png ~/.local/share/icons/wine/KakaoTalk.png
```

-2. 바로가기 만들기

```
cat << 'EOF' > ~/.local/share/applications/KakaoTalk.desktop
[Desktop Entry]
Encoding=UTF-8
Name=KakaoTalk
Comment=KakaoTalk
Exec=xdg-open bottles:run/KakaoTalk/KakaoTalk
Terminal=false
Type=Application
Icon=~/.local/share/icons/wine/KakaoTalk.png
EOF
```


---

## Optional
![스크린샷, 2021-05-07 12-49-02](https://user-images.githubusercontent.com/42508318/117395648-4b82fa80-af33-11eb-93d2-91133d26b090.png)
![스크린샷, 2021-05-07 12-49-59](https://user-images.githubusercontent.com/42508318/117395657-50e04500-af33-11eb-9c9d-82ade39fa9c2.png)    
Using [Topicons plus gnome shell extention](https://extensions.gnome.org/extension/1031/topicons/, "Gnome Shell Extention") to combine the Wine system tray into the top bar

