# Point-and-shoot-Camera
Linux系統管理實務　期末報告　第二組  <br/>
指導教授：練喆明、俞旭昇  <br/>
組員：103213516　吳宗翰  <br/>
　　　103213525　高玟瑜
# 壹、題目發想緣起
現今相機的功能越來越多，不僅有拍照的功能，甚至連上wifi上傳至網路空間的相機也漸漸地攻占消費者市場。由於我們兩位皆熱愛拍照，所以非常嚮往能夠上傳至網路空間的相機，現在市面上已經有許多可以與網路空間串流的相機了，但礙於還是學生，經濟有限的情況下，未能一償照片即時更新的心願，於是透過這堂課實作Raspberry Pi打造一台符合我們要求與願想的輕便相機，並用自己的能力來將此相機實作出來，再以相機記錄映於眼簾的美景。
# 貳、實作所需材料
<table>
  <tr>
		<td>材料</td>
		<td>數量</td>
		<td>價格</td>
		<td>來源</td>
	</tr>
	<tr>
		<td>Raspberry Pi</td>
		<td>1</td>
		<td>課堂提供</td>
		<td>   </td>
	</tr>
	<tr>
		<td>觸控螢幕3.2吋</td>
		<td>1</td>
		<td>露天拍賣</td>
		<td>800</td>
	</tr>
	<tr>
		<td>相機</td>
		<td>1</td>
		<td>露天拍賣</td>
		<td>740</td>
	</tr>
	<tr>
		<td>按鈕</td>
		<td>5</td>
		<td>組員提供</td>
		<td>   </td>
	</tr>
	<tr>
		<td>LED燈</td>
		<td>3</td>
		<td>露天拍賣</td>
		<td>5</td>
	</tr>
	<tr>
		<td>麵包板</td>
		<td>1</td>
		<td>組員提供</td>
		<td>   </td>
	</tr>
	<tr>
		<td>銲接板</td>
		<td>3</td>
		<td>組員提供</td>
		<td>   </td>
	</tr>
	<tr>
		<td>杜邦線</td>
		<td>數條</td>
		<td>露天拍賣</td>
		<td>100</td>
	</tr>
	<tr>
		<td>排針</td>
		<td>數排</td>
		<td>露天拍賣</td>
		<td>8</td>
	</tr>
	<tr>
		<td>瓦楞紙板</td>
		<td>數片</td>
		<td>組員提供</td>
		<td>   </td>
	</tr>
</table>
# 參、使用的現有軟體與來源
1. Postfix
2. Vim
3. Camera modules
4. TFT Module  <br/>
以上來源參考/取自RPI官方

# 肆、實作過程
<table>
  <tr>
		<td>碰到哪些問題</td>
		<td>如何解決</td>
	</tr>
	<tr>
		<td>想要利用指撥開關縮減硬體的配置，讓操作方式單純簡單。</td>
		<td>先藉由麵包板上的元件測試來看看，所設計的電路與程式是否正確無誤，再將指撥按鈕移至電路板上進行銲接。</td>
	</tr>
	<tr>
		<td>按鈕開關供電部分。由於麵包板空間有限，無法將全部元件插上麵包板上完整呈現。</td>
		<td>選擇將部分元件挪至銲接板上，使用銲接的方法，把各個相同功能屬性的元件銲在同個電路板上，如此就可以避免過於雍塞的情況。</td>
	</tr>
	<tr>
		<td>Raspberry Pi所提供的GPIO數量過少，若裝置TFT就會將所有的訊號、供電與接地腳佔滿，造成麵包板上元件無法接收訊號、供電與接地。</td>
		<td>先利用公對母杜邦線將Pi的GPIO都導到麵包板上，並找到TFT的製作商或是供應商，尋找網站上公告的TFT腳位配置，找到TFT會使用到的相對應腳位，採用公對公杜邦線導向TFT，即可擁有與直接插上Pi相同的功能。接著找出TFT上NC的腳位來當作按鈕或是LED的訊號腳。</td>
	</tr>
	<tr>
		<td>上傳至Facebook</td>
		<td>上網找了許多資料，我們也有找到網友分享的步驟，但因Facebook不斷的更新，以至於和分享的資料有落差。</td>
	</tr>
	<tr>
		<td>觸控面板安裝、觸控</td>
		<td>在網路上找到一家網站的實作可以成功顯示樹莓的桌面，但卻一直無法觸控，經過不斷的重灌、除錯後，觸控功能總算是完成了。</td>
	</tr>
</table>
# 伍、 運用哪些與課程內容中相關的技巧
1. 開機時，將IP寄到信箱
2. 將照片上傳Google Drive

# 陸、 實際產出
#### 一、 解決了哪些問題
<table>
  <tr>
  		<td>是否解決</td>
		<td>碰到哪些問題</td>
		<td>如何解決</td>
	</tr>
	<tr>
	  	<td></td>
		<td>想要利用指撥開關縮減硬體的配置，讓操作方式單純簡單。</td>
		<td>先藉由麵包板上的元件測試來看看，所設計的電路與程式是否正確無誤，再將指撥按鈕移至電路板上進行銲接。</td>
	</tr>
	<tr>
		<td>  ✔  </td>
		<td>按鈕開關供電部分。由於麵包板空間有限，無法將全部元件插上麵包板上完整呈現。</td>
		<td>選擇將部分元件挪至銲接板上，使用銲接的方法，把各個相同功能屬性的元件銲在同個電路板上，如此就可以避免過於雍塞的情況。</td>
	</tr>
	<tr>
		<td>  ✔  </td>
		<td>Raspberry Pi所提供的GPIO數量過少，若裝置TFT就會將所有的訊號、供電與接地腳佔滿，造成麵包板上元件無法接收訊號、供電與接地。</td>
		<td>先利用公對母杜邦線將Pi的GPIO都導到麵包板上，並找到TFT的製作商或是供應商，尋找網站上公告的TFT腳位配置，找到TFT會使用到的相對應腳位，採用公對公杜邦線導向TFT，即可擁有與直接插上Pi相同的功能。接著找出TFT上NC的腳位來當作按鈕或是LED的訊號腳。</td>
	</tr>
	<tr>
		<td></td>
		<td>上傳至Facebook</td>
		<td>上網找了許多資料，我們也有找到網友分享的步驟，但因Facebook不斷的更新，以至於和分享的資料有落差。</td>
	</tr>
	<tr>
		<td>  ✔  </td>
		<td>觸控面板安裝、觸控</td>
		<td>在網路上找到一家網站的實作可以成功顯示樹莓的桌面，但卻一直無法觸控，經過不斷的重灌、除錯後，觸控功能總算是完成了。</td>
	</tr>
</table>
#### 二、 寫了什麼軟體或修改哪些設定
<table>
  <tr>
		<td>作用</td>
		<td>動作</td>
	</tr>
	<tr>
		<td>開機時將IP寄到信箱</td>
		<td>1. 撰寫寄IP到信箱程式。<br/>
		2. 修改該檔案的權限。<br/> 
		sudo chmod 755 sendip.sh<br/> 
		3. 設定該shell檔可以一開機就執行。<br/>
		sudo update-rc.d sendip.sh defaults</td>
	</tr>
	<tr>
		<td>相機</td>
		<td>1. 輸入raspi-config指令，設定相機的驅動程式。<br/>
		raspi-config>Enable Camera>Enable</td>
	</tr>
	<tr>
		<td>觸控面板(顯示)</td>
		<td>1. Raspberry Pi 的顯示輸出從 HDMI bus 換成 SPI bus<br/>
		sudo nano /usr/share/X11/xorg.conf.d/99-fbturbo.conf<br/>
		“fbdev /dev/fb0”> fbdev /dev/fb1”<br/>
		2. TFT會使用到SPI，所以進入到raspi-config中設定SPI，因為預設的SPI是關閉的。<br/>
		raspi-config>Advanced Options>SPI>Yes<br/>
		3. SPI功能加入blacklist file<br/>
		sudo vim /etc/modprobe.d/raspi-blacklist<br/>
		加入相關設定<br/>
		4. 將TFT顯示與觸控的模組加入kernel<br/>
		sudo vim /etc/modules<br/>
		加入相關設定<br/>
		5. 修改/boot/cmdline.txt<br/>
		加入相關設定<br/>
		6. 設定成開機就會執行<br/>
		sudo nano /etc/rc.local <br/>
		加入 su -l pi -o startx<br/>
		7. 校準命令<br/>
		sudo TSLIB_FBDEVICE=/dev/fb1<br/>
		sudo TSLIB_TSDEVICE=/dev/input/touchscreen <br/>
		ts_calibrate</td>
	</tr>
</table>

# 柒、 組裝過程及製作教學
####一、 組裝過程
內部圖 <br/>
![step](https://github.com/s103213516/Point-and-shoot-Camera/blob/master/DSC_7061.JPG) <br/><br/>
組裝完成圖 <br/>
![step](https://github.com/s103213516/Point-and-shoot-Camera/blob/master/DSC_7064.JPG) <br/><br/>
####二、 製作教學
GPIO-拍照按鈕與關機按鈕 <br/>
![step](https://github.com/s103213516/Point-and-shoot-Camera/blob/master/Btn.png) <br/><br/>
元件銲接圖-拍照按鈕與關機按鈕(正面)<br/>
![step](https://github.com/s103213516/Point-and-shoot-Camera/blob/master/Snap1.jpg) <br/>
利用銲接電路進行拍照按鈕與關機按鈕的製作，此圖為電路正面情況，三個按鈕之間個別串入三電阻(電阻值：220+5%Ω、1K+5%Ω)，防止電流量過大燒毀元件，而在電阻之後是Raspberry Pi GPIO的訊號接腳。<br/><br/>
元件銲接圖-拍照按鈕與關機按鈕(背面)<br/>
![step](https://github.com/s103213516/Point-and-shoot-Camera/blob/master/Snap2.jpg) <br/>
圖中三個藍色箭頭即為訊號接腳銲接處。紅框則是電路實際走線。<br/><br/>
GPIO-LED燈 <br/>
![step](https://github.com/s103213516/Point-and-shoot-Camera/blob/master/LED.png) <br/><br/>
元件銲接圖-LED燈(正面)<br/>
![step](https://github.com/s103213516/Point-and-shoot-Camera/blob/master/Snap5.jpg) <br/>
圖為三個發光二極體的布線方法，與正電之間有先串入一個電阻(電阻值：220+5%Ω)，防止電流量過大燒毀元件。<br/><br/>
元件銲接圖-LED燈(背面)<br/>
![step](https://github.com/s103213516/Point-and-shoot-Camera/blob/master/Snap6.jpg) <br/>
這個部分不需要正電的加入，因為直接以GPIO.7的訊號電路為輸出腳位，並用程式來控制正電的輸出。<br/><br/>
GPIO-上傳至Google Drive、Dropbox按鈕 <br/>
![step](https://github.com/s103213516/Point-and-shoot-Camera/blob/master/UpDate.png) <br/><br/>
元件銲接圖-上傳至Google Drive、Dropbox按鈕(正面)<br/>
![step](https://github.com/s103213516/Point-and-shoot-Camera/blob/master/Snap3.jpg) <br/>
圖為上傳至Google Drive、Dropbox的按鈕製作，一樣各有一個電阻(皆為1K+5%Ω)來防止電流量過大燒毀元件，而在電阻之後是Raspberry Pi GPIO的訊號接腳。<br/><br/>
元件銲接圖-上傳至Google Drive、Dropbox按鈕(背面)<br/>
![step](https://github.com/s103213516/Point-and-shoot-Camera/blob/master/Snap4.jpg) <br/>
上下兩方是正負電，兩個藍色箭頭是按鈕的訊號線，紅框則是電路實際走線。<br/><br/><br/>
Camera<br/>
(1) 安裝驅動，下指令確認是否可以拍照<br/>
sudo raspi-config  選擇Enable Camera即可<br/><br/>
(2) 快門拍照<br/>
raspistill -o image.jpg -t 1000<br/><br/><br/>
按鈕<br/>
(1) 能夠控制快門<br/>
raspistill -o image.jpg -t 2000<br/><br/>
(2) 能夠控制4秒自拍快門

	x=0<br/>
	while x<4:<br/>
  	GPIO.output(7,True)  讓LED燈會亮<br/>
  	time.sleep(1)  間隔一秒鐘<br/>
  	GPIO.output(7,False)  讓LED燈熄滅<br/>
  	time.sleep(1)  間隔一秒鐘<br/>
  	x+=1<br/>
	raspistill -o image.jpg -t 2000<br/>

(3) 拍好的照片上傳至Google Drive<br/>
https://github.com/prasmussen/gdrive  找到drive-linux-rpi<br/> v1.8.0，右鍵，複製連結，利用wget下載檔案，完成後把檔名改成drive<br/>
sudo chmod 775 drive  修改drive權限<br/>
./drive  將出現那串網址貼到firefox，執行後會出現一個hash code，將其複製到terminal<br/>
./drive list  列出所有清單<br/>
./drive folder -t LSA  建立一個資料夾，複製其ID<br/>
./drive upload -f image.jpg -p 把剛剛複製的ID貼上  上傳照片<br/><br/>
(4) 拍好的照片上傳至Dropbox<br/>
sudo apt-get update  更新最新的軟體資料<br/>
sudo apt-get upgrade  更新軟體<br/>
mkdir ~/Dropbox  建立一個Dropbox資料夾<br/>
cd ~/Dropbox  進入Dropbox資料夾<br/>
git clone https://github.com/andreafabrizi/Dropbox-Uploader  下載Dropbox Uploader軟體<br/>
cd Dropbox-Uploader  進入軟體路徑<br/>
./dropbox_uploader.sh list  設定Dropbox Uploader軟體，取得App key、App secret，和設定token<br/>
./dropbox_uploader.sh upload image.jpg /home/pi/Dropbox/  上傳照片<br/><br/>
(5) 關機<br/>
sh shutdn.sh  shutdn.sh檔案其內容是echo "raspberry" | sudo -S shutdown -h now<br/><br/><br/>
觸控面板<br/>
(1) 設定觸控面板輸出畫面<br/>
sudo nano /usr/share/X11/xorg.conf.d/99-fbturbo.conf  先將 Raspberry Pi 的顯示輸出從 HDMI bus 換成 SPI bus<br/>
	找到這一行 Option "fbdev" "/dev/fb0"，將 fb0 換成 fb1<br/>
	fb0 選項是告訴顯示驅動程式將輸出定在 HDMI<br/>
	fb1 選項則是將輸出改定到 LCD 螢幕<br/>
sudo raspi-config  選擇Advanced Options，A6 SPI即可<br/>
vim /etc/modprobe.d/raspi-blacklist.conf<br/>

	#blacklist spi-bcm2708<br/>
	blacklist i2c-bcm2708<br/>
	blacklist snd-soc-pcm512x<br/>
	blacklist snd-soc-wm8804<br/>

sudo REPO_URI=https://github.com/notro/rpi-firmware rpi-update<br/>
vim /etc/modules<br/>

	spi-bcm2708<br/>
	fbtft_device name=waveshare32b gpios=dc:22,reset:27 speed=48000000<br/>
	waveshare32b width=320 height=240 buswidth=8 init=-	1,0xCB,0x39,0x2C,0x00,0x34,0x02,-1,0xCF,0x00,0XC1,0X30,-	1,0xE8,0x85,0x00,0x78,-1,0xEA,0x00,0x00,-1,0xED,0x64,0x03,0X12,0X81,-	1,0xF7,0x20,-1,0xC0,0x23,-1,0xC1,0x10,-1,0xC5,0x3e,0x28,-1,0xC7,0x86,-	1,0x36,0x28,-1,0x3A,0x55,-1,0xB1,0x00,0x18,-1,0xB6,0x08,0x82,0x27,-1,0xF2,0x00,-1,0x26,0x01,-1,0xE0,0x0F,0x31,0x2B,0x0C,0x0E,0x08,0x4E,0xF1,0x37,0x07,0x10,0x03,0x0E,0x09,0x00,-1,0XE1,0x00,0x0E,0x14,0x03,0x11,0x07,0x31,0xC1,0x48,0x08,0x0F,0x0C,0x31,0x36,0x0F,-1,0x11,-2,120,-1,0x29,-1,0x2c,-3<br/>
	ads7846_device model=7846 cs=1 gpio_pendown=17 speed=1000000<br/>
	keep_vref_on=1 swap_xy=0 pressure_max=255 x_plate_ohms=60<br/>
	x_min=200 x_max=3900 y_min=200 y_max=3900<br/>

vim /boot/cmdline.txt<br/>

	dwc_otg.lpm_enable=0 console=ttyAMA0,115200 console=tty1<br/>
	root=/dev/mmcblk0p2 rootfstype=ext4 elevator=deadline rootwait<br/> 
	fbtft_device.custom fbtft_device.name=waveshare32b <br/>
	fbtft_device.gpios=dc:22,reset:27 fbtft_device.bgr=1 <br/>
	fbtft_device.speed=48000000 <br/>
	fbcon=map:10 fbcon=font:ProFont6x11 logo.nologo dma.dmachans=0x7f35 <br/>
	console=tty1 consoleblank=0 fbtft_device.fps=50 fbtft_device.rotate=0<br/>

vim /etc/rc.local<br/>

	su -l pi -c startx<br/>

sudo raspi-config  選擇Enable Boot to Desktop/Scratch，Desktop Log in as user ‘pi’ at the graphical desktop即可<br/><br/>
(2) 旋轉觸控面板畫面
vim /boot/cmdline.txt

	fbtft_device.rotate=90
	
<br/>(3) 校準觸控面板游標位置
vim /etc/modules<br/>

	swap_xy=1<br/>

sudo apt-get install xinput evtest<br/>
vim /etc/X11/xinit/xinitrc<br/>

	DISPLAY=:0 xinput --set-prop 'ADS7846 Touchscreen' <br/>
	'Evdev Axis Inversion' 1 0<br/>

aptitude install libts-bin<br/>
export TSLIB_TSDEVICE=/dev/input/event0<br/>
export TSLIB_FBDEVICE=/dev/fb1<br/>
ts_calibrate<br/>
ts_test<br/><br/>
<br/><br/>(4) 安裝相機與觸控面板同步模組
sudo apt-get install python-pip<br/>
sudo pip install picamera==0.8<br/>
wget https://github.com/adafruit/adafruit-pi-cam/archive/master.zip<br/>
unzip master.zip<br/>
cd adafruit-pi-cam-master<br/>
sudo python cam.py<br/>

# 捌、 操作教學
正面圖
![step](https://github.com/s103213516/Point-and-shoot-Camera/blob/master/DSC_7069.JPG)
背面圖
![step](https://github.com/s103213516/Point-and-shoot-Camera/blob/master/DSC_7065.JPG)
上面圖
![step](https://github.com/s103213516/Point-and-shoot-Camera/blob/master/DSC_7067.JPG)



# 玖、 工作分配表
<table>
  <tr>
		<td>   </td>
		<td>吳宗翰</td>
		<td>高玟瑜</td>
	</tr>
	<tr>
		<td>電路銲接</td>
		<td>✔</td>
		<td></td>
	</tr>
	<tr>
		<td>麵包板電路設計</td>
		<td>✔</td>
		<td></td>
	</tr>
	<tr>
		<td>相關資料搜尋、彙整</td>
		<td></td>
		<td>✔</td>
	</tr>
	<tr>
		<td>程式撰寫</td>
		<td>✔</td>
		<td>✔</td>
	</tr>
	<tr>
		<td>外觀製作</td>
		<td></td>
		<td>✔</td>
	</tr>
	<tr>
		<td>文件處理</td>
		<td></td>
		<td>✔</td>
	</tr>
</table>





# 拾、 參考來源
1. 封面照片：
http://iguang.tw/gohappy/product/24955.html
2. Raspberry Pi最佳入門與實戰應用，碁峰資訊股份有限公司，2015年02月
3. 電路參考：
https://sites.google.com/site/raspberrypidiy/home
4. TFT畫面顯示：
http://mcuapps.com/blog/build-lcd-touchscreen-drivers-for-raspberry-pi
5. TFT面板觸控功能： <br/>
(1) http://mcuapps.com/blog/build-lcd-touchscreen-drivers-for-raspberry-pi <br/>
(2) http://www.geekfan.net/5618/
6. TFT面板與相機同步顯示：
https://learn.adafruit.com/diy-wifi-raspberry-pi-touch-cam/pi-setup
