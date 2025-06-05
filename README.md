# Install-aaPanel

0. Remote Server menggunakan ssh dan masuk ke root : sudo su

1. Update Repositori : 
   ```bash
   sudo apt update -y
   ```

3. Install aaPanel :
   ```bash
   URL=https://www.aapanel.com/script/install_7.0_en.sh && if [ -f /usr/bin/curl ];then curl -ksSO "$URL" ;else wget --no-check-certificate -O install_7.0_en.sh "$URL";fi;bash install_7.0_en.sh aapanel
   ```
4. Do you want to install aaPanel to the /www directory now?(y/n): ( y  )

5. Ganti dan matikan service di Bawah ini : bt
	- mengganti username	: arthasa ( 6 )
	- mengganti password	: 081212 ( 5 )
	- mengganti port	: 8090 ( 8 )
	- mengganti security entrance ( 28 )
	- mematikan panel SSL	: Off ( 27 )
	- Restart aaPanel	: ( 1 )

6. kunjungi Websitenya http://<IP-SERVER>:8090/aapanel | lalu login

7. Pili packages LAMP ( apache 2.4, PHP 7.4, Pure-Ftpd 1.0.49 ) | Quick Install atau tambahkan NGINX 1.27

8. Pilih Menu Website -> Add Site

9. Isi bagian
	- Domain name	isi dengan custome+port = mikhmon.01:8001
	- lalu masuk ke folder Document Root di website /www/wwwroot/...

10. Centang pilih semua file -> More -> Delete

11. Remote download -> paste url address -> confirm

12. Klik kanan file mk.zip -> pilih unzip -> confirm

13. Install cloudflare tunnel

14. Buka one.dash.cloudflare.com (KHUSUS YANG UDAH ADA AKUN CLOUDFLARE)

15. Networks -> Tunnels -> Create a tunnel -> Select Cloudflared

16. Name your tunnel : Tunnel name <ISI BEBAS> lalu save tunnel

17. Pilih Debian -> 64-bit

18. Copy If you don’t have cloudflared installed on your machine -> paste di terminal

19. Lalu copy juga After you have installed cloudflared on your machine -> paste di terminal

20. Isi Subdomain panel/aapanel -> pilih domain -> Type service HTTP -> URL 127.0.0.1:8090

21. Tambahkan juga untuk mikhmon mikhmon/sesuaikan -> pilih domain -> Type service HTTP -> URL <IP-SERVER>:8001

22. Akses panelnya menggunakan https://panel.DOMAIN/aapanel

23. Akses mikhmon juga
