# Install-aaPanel

0. Remote Server menggunakan ssh dan masuk ke root : sudo su

1. Update Repositori : sudo apt update -y

2. Install aaPanel : 

URL=https://www.aapanel.com/script/install_7.0_en.sh && if [ -f /usr/bin/curl ];then curl -ksSO "$URL" ;else wget --no-check-certificate -O install_7.0_en.sh "$URL";fi;bash install_7.0_en.sh aapanel

3. Do you want to install aaPanel to the /www directory now?(y/n): ( y  )

4. Ganti dan matikan service di Bawah ini : bt
	- mengganti username	: arthasa ( 6 )
	- mengganti password	: 081212 ( 5 )
	- mengganti port	: 8090 ( 8 )
	- mengganti security entrance ( 28 )
	- mematikan panel SSL	: Off ( 27 )
	- Restart aaPanel	: ( 1 )

5. kunjungi Websitenya http://<IP-SERVER>:8090/aapanel | lalu login

6. Pili packages LAMP ( apache 2.4, PHP 7.4, Pure-Ftpd 1.0.49 ) | Quick Install atau tambahkan NGINX 1.27

7. Pilih Menu Website -> Add Site

8. Isi bagian
	- Domain name	isi dengan custome+port = mikhmon.01:8001
	- lalu masuk ke folder Document Root di website /www/wwwroot/...

9. Centang pilih semua file -> More -> Delete

10. Remote download -> paste url address -> confirm

11. Klik kanan file mk.zip -> pilih unzip -> confirm

12. Install cloudflare tunnel

13. Buka one.dash.cloudflare.com (KHUSUS YANG UDAH ADA AKUN CLOUDFLARE)

14. Networks -> Tunnels -> Create a tunnel -> Select Cloudflared

15. Name your tunnel : Tunnel name <ISI BEBAS> lalu save tunnel

16. Pilih Debian -> 64-bit

17. Copy If you don’t have cloudflared installed on your machine -> paste di terminal

18. Lalu copy juga After you have installed cloudflared on your machine -> paste di terminal

19. Isi Subdomain panel/aapanel -> pilih domain -> Type service HTTP -> URL 127.0.0.1:8090

20. Tambahkan juga untuk mikhmon mikhmon/sesuaikan -> pilih domain -> Type service HTTP -> URL <IP-SERVER>:8001

21. Akses panelnya menggunakan https://panel.<DOMAIN>/aapanel

22. Akses mikhmon juga
