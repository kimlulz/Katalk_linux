# Katalk_linux

![1](https://user-images.githubusercontent.com/42508318/117267739-8f252800-ae91-11eb-8b8a-8a8cb1121f4f.png)
![2](https://user-images.githubusercontent.com/42508318/117267750-91878200-ae91-11eb-9e74-82c8fec96d42.png)

## Prepare
```
sudo dpkg --add-architecture i386 
wget -nc https://dl.winehq.org/wine-builds/winehq.key
sudo apt-key add winehq.key
```
Add repository for your OS environment below..
|Distro|Repository|
|:----:|:----:|
| Ubuntu 21.04 | sudo add-apt-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ hirsute main' |
| Ubuntu 20.10 | sudo add-apt-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ groovy main' |
| Ubuntu 20.04 | sudo add-apt-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ focal main' |
| Ubuntu 18.04 | sudo add-apt-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ bionic main' |
| Debian 10 (Buster) | deb https://dl.winehq.org/wine-builds/debian/ buster main |
```
sudo apt update
sudo apt install --install-recommends winehq-stable
sudo apt install playonlinux
```
## Configure
![스크린샷, 2021-05-06 17-40-37](https://user-images.githubusercontent.com/42508318/117268393-32763d00-ae92-11eb-8ed2-e00611e424ca.png)   
PlayOnLinux -> 상단바 [도구] -> Wine 버전 관리     
Wine 최신버전 설치
    
![스크린샷, 2021-05-06 17-43-17](https://user-images.githubusercontent.com/42508318/117268930-c7793600-ae92-11eb-9557-c0b75b856bfd.png)
PlayOnLinux 메인 -> 설치 -> Install a non-listed program    
![스크린샷, 2021-05-06 17-45-46](https://user-images.githubusercontent.com/42508318/117269356-2ccd2700-ae93-11eb-84bf-2bfec5df8cec.png)
![스크린샷, 2021-05-06 17-45-49](https://user-images.githubusercontent.com/42508318/117269367-2dfe5400-ae93-11eb-86b5-adf8481c93d3.png)
![스크린샷, 2021-05-06 17-46-12](https://user-images.githubusercontent.com/42508318/117269370-2dfe5400-ae93-11eb-9e7b-e675fca36e37.png)
![스크린샷, 2021-05-06 17-46-22](https://user-images.githubusercontent.com/42508318/117269373-2e96ea80-ae93-11eb-8cc7-d1a039921423.png)
![스크린샷, 2021-05-06 17-46-26](https://user-images.githubusercontent.com/42508318/117269377-2f2f8100-ae93-11eb-9d11-a6018bbb2c30.png)
![스크린샷, 2021-05-06 17-46-30](https://user-images.githubusercontent.com/42508318/117269381-2f2f8100-ae93-11eb-9f8e-e219235cffdc.png)
![스크린샷, 2021-05-06 17-47-05](https://user-images.githubusercontent.com/42508318/117269388-2fc81780-ae93-11eb-9dd8-55ae84b280c5.png)    
install wine gecko/mono if winecfg popup it..    

  ![스크린샷, 2021-05-06 18-52-35](https://user-images.githubusercontent.com/42508318/117279013-3dce6600-ae9c-11eb-8c88-b1807265d0b5.png)
![스크린샷, 2021-05-06 18-53-39](https://user-images.githubusercontent.com/42508318/117279168-67878d00-ae9c-11eb-8272-88e7dfb23098.png)    
Select Windows 10 and add library "d3dx11_43" and click Apply.

 ![스크린샷, 2021-05-06 18-54-59](https://user-images.githubusercontent.com/42508318/117279335-969dfe80-ae9c-11eb-83bb-7768de0d40c4.png)   
Select d3dx11, gdiplus, gecko, mono28    

![스크린샷, 2021-05-06 18-57-30](https://user-images.githubusercontent.com/42508318/117279746-f98f9580-ae9c-11eb-903b-d9580aeb9ad9.png)    
Download Kakaotalk installer and select installer file    
process of installation same with windows

![스크린샷, 2021-05-06 18-58-58](https://user-images.githubusercontent.com/42508318/117279993-1f1c9f00-ae9d-11eb-8be6-9a5d5e3738e8.png)    
Do not check "카카오톡 실행" for make shortcut.    

![스크린샷, 2021-05-06 18-59-48](https://user-images.githubusercontent.com/42508318/117280146-44111200-ae9d-11eb-917f-48f4059f9b80.png)    
Kakaotalk -> Next -> Next    

## Run
![스크린샷, 2021-05-06 19-00-33](https://user-images.githubusercontent.com/42508318/117280242-5c812c80-ae9d-11eb-967b-11d3f5c9ae38.png)    
Run Kakaotalk    

It will show "RECV_SOCKET_ERROR(err_code=336130329) (Error Code: 50114) FriendList. or LOCO protocol".  just retry.

![1](https://user-images.githubusercontent.com/42508318/117267739-8f252800-ae91-11eb-8b8a-8a8cb1121f4f.png)    
Finished

## Optional
![스크린샷, 2021-05-07 12-49-02](https://user-images.githubusercontent.com/42508318/117395648-4b82fa80-af33-11eb-93d2-91133d26b090.png)
![스크린샷, 2021-05-07 12-49-59](https://user-images.githubusercontent.com/42508318/117395657-50e04500-af33-11eb-9c9d-82ade39fa9c2.png)    
Using [Topicons plus gnome shell extention](https://extensions.gnome.org/extension/1031/topicons/, "Gnome Shell Extention") to combine the Wine system tray into the top bar

