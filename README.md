# proje-odevim
Mehmet Ali Emiroğlu 223010710022 Kayseri Üniversitesi Bilgisayar Programcılığı

PROJE KURULUM ADIMLARI

1. Projeyi indirdikten sonra komut dizininde proje dosyasına geliniz
2.  python -m venv venv komutu ile virtual env oluşturun
3.  MacOS için source venv/bin/activate | Windows için venv\scripts\activate komutunu çalıştırarak virtual env'i aktif edin
4.  pip install -r requirements.txt komutu ile gereken modülleri yükleyin
5.  Daha sonra yeni bir komut satırında dropdb --if-exists auctions komutunu çalıştırarak auctions adına bir PostgreSQL veritabanı olup olmadığını kontrol edin. Not: isterseni auctions veya başka bir veritabanı adı kullanabilirsiniz
6.  psql postgres komutuyla postgresql server'ını başlatın
7.  CREATE DATABASE auctions; komutuyla veritabanınızı oluşturun
8.  CREATE USER veritabani_kullanici_adi WITH SUPERUSER PASSWORD 'sifre'; komutuyla veritabanı kullanıcı adı ve şifreyi oluşturun
9.  \q komutuyla postgresql'den çıkış yapabilirsiniz
10.  proje dizininde touch .env komutunu çalıştırın
11.  içerisine
SECRET_KEY=yoursecretkey
DEBUG=True
DATABASE_NAME=auctions
DATABASE_USER=veritabani_kullanici_adi
DATABASE_PASS=sifre
DATABASE_HOST=localhost
burayı yapıştırın
12. Proje dizininde python manage.py makemigrations komutunu çalıştırın
13. Daha sonra python manage.py migrate komutunu çalıştırın
14. python manage.py createsuperuser komutuyla yetkili kullanıcıyı oluşturun
15. python manage.py runserver komutuyla projeyi başlatın ve 127.0.0.1:8000 adresine gidin
16. Admin paneli için 127.0.0.1:8000/admin dizinine gidin ve belirttiğiniz admin kullanıcı adı ve şifresiyle giriş yapın
