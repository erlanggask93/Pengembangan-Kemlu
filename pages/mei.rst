Mei
=========================

Instalasi dan konfigurasi untuk menjalankan PP Financial Dashboard API Services dibagi menjadi dua jenis, yakni **Local** dan **Production**.
Ikuti instalasi **Local** jika Anda ingin menjalankan PP Financial Dashboard API Services di lokal komputer Anda. Ikuti instalasi **Production** jika Anda ingin menjalankan PP Financial Dashboard API Services di server production.

Local
-----

Untuk menjalankan PP Financial Dashboard API Services di lokal komputer, pastikan Anda sudah menginstall Golang (Go) dan MySQL sesuai persyaratan yang dibutuhkan.

1. Buka terminal, lalu jalankan perintah:

.. code-block:: bash

    $ git clone https://pt-pp@dev.azure.com/pt-pp/ppit-mantapp/_git/ppit-mantap-api

2. Buka folder ppit-mantap-api, lalu buat file ``.env`` dengan cara copy paste melalui file ``env.example``.
3. Isi ``DB_READ_HOST, DB_READ_DATABASE, DB_READ_USERNAME, DB_READ_PASSWORD`` di dalam file ``.env`` sesuai dengan konfigurasi database Anda. Contoh:

.. code-block:: bash

    DB_READ_HOST="localhost"
    DB_READ_PORT="3306"
    DB_READ_DATABASE="finance-pp"
    DB_READ_USERNAME="root"
    DB_READ_PASSWORD=""
    DB_READ_CHARSET="utf8mb4"
    DB_READ_PARSE_TIME="True"
    DB_READ_LOC="Local"

4. Isi ``DB_WRITE_HOST, DB_WRITE_DATABASE, DB_WRITE_USERNAME, DB_WRITE_PASSWORD`` di dalam file ``.env`` sesuai dengan konfigurasi database Anda. Contoh:

.. code-block:: bash

    DB_WRITE_HOST="localhost"
    DB_WRITE_PORT="3306"
    DB_WRITE_DATABASE="finance-pp"
    DB_WRITE_USERNAME="root"
    DB_WRITE_PASSWORD=""
    DB_WRITE_CHARSET="utf8mb4"
    DB_WRITE_PARSE_TIME="True"
    DB_WRITE_LOC="Local"

5. Isi ``KEY_JWT, KEY_API_KEY`` di dalam fil ``.env`` dengan random string sesuai kebutuhan. Pastikan mengisi ``KEY_API_KEY`` dengan random string yang sudah dienkripsi, contoh:

.. code-block:: bash

    KEY_JWT="1234"
    KEY_API_KEY="apVPXKasdhvWjHV3y5FAyOv6c5WXbZw2ThqlZhjjp8dHtMEV8s2h0AW"

.. warning::
    KEY_JWT dan KEY_API_KEY bersifat rahasia. Jangan membagikannya kepada orang yang tidak memiliki otorisasi.

6. Buka terminal, arahkan ke folder ppit-mantap-api, lalu jalankan perintah:

.. code-block:: bash

    $ go run main.go

7. Buka browser, lalu arahkan ke alamat ``http://localhost:9000``.

Production
----------

**ON PROGRESS**