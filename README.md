# p.client-server-lat-2
Langkah 1 :
Buat proyek web menggunakan link berikut start.spring.io kemudian pilih Spring web dan kemudian bahasa java dan sesuaikan versinya dengan device (disini saya menggunakan jdk 17 kemudian isi artifactnya(saya menggunakan latihan2-service) kemudian spring bootversinya pakai yang versi 2.6.11(yang saya pakai) dan untuk grubnya isi dengan com.fauzan kemudian download dan extrack dari zip menjadi file kemudian import ke dalam apache netbean


Langkah 2 :
Kemudian cari proyek yang bernama LatihanServiceApplication dibawah package com.fauzan.latihan.service kemudian pada proyek itu masukkan code berikut :
```
package com.fauzan.microservices.latihan2.service;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.RestController;

@SpringBootApplication
@RestController
public class Latihan2ServiceApplication {

	public static void main(String[] args) {
		SpringApplication.run(Latihan2ServiceApplication.class, args);
	}
        @GetMapping("/hello")
            public String hello(@RequestParam(value = "name", defaultValue = "Latihan 2") String name) {
            return String.format("Hello %s!", name);
        }

}
```
Langkah 3 :
Kemudian cari proyek aplication.properties yang berada di Other Source >> src/main/resources >> >> aplication.properties kemudian masukkan code berikut :
server.port=8010


Langkah 4 :
Terakhir untuk output buka chrome/browser lalu ketik local host sesuai port yang dibuat
Link : latihan2
![Screenshot 2022-09-26 220335](https://user-images.githubusercontent.com/113502282/192313005-fdde1e49-039b-410b-9e34-c97372a3d493.png)
