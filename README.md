# Send Email with PHPMailer

Trong dự án này tôi sử dụng package PHPMailer và sử dụng SMTP của Gmail để gửi email.

### Khởi động một tool như XAMPP để khởi động môi trường Apache để gói thư viện hoạt động!

## Sử dụng Composer quản lý gói thư viện
Link hướng dẫn cài đặt: https://nentang.vn/app/edu/khoa-hoc/thiet-ke-lap-trinh-web-backend/khoa-hoc-backend-thiet-ke-web-voi-laravel/lessons/cai-dat-composer-de-quan-ly-cac-goi-thu-vien-trong-php

Một số lệnh:

*Lệnh để trỏ tới thư mục chứa code:*
```bash
cd c:\xampp\htdocs\signinwithGoogle
```
*Lệnh để kiểm tra version*
```bash
php composer.phar --version
```
*Cài đặt gói thư viện với composer*

Lưu ý hãy trỏ tới thư mục chứa code rồi nhập lệnh
```bash
composer require phpmailer/phpmailer
```
hoặc download ở bài viết Github gốc: https://github.com/PHPMailer/PHPMailer


Lưu ý: Khi composer được cài đặt cũng sẽ bao gồm 2 gói là composer.json và composer.lock nằm ở folder gốc.
## Document &  Video
Tham khảo: www.youtube.com/watch?v=h2bLhhAli0o

## Giải thích source:
- sendEmail.php: Khi chạy code này sử xử lý để gửi email tới email bạn chỉ định
- a.hmtl: File HTML chứa source HTML để file sendmail đọc và gửi email dưới định dạng HTML

## Command

Hãy sửa các tham số trên cho phía sender:
```bash
    $mail->isSMTP();                                            //Send using SMTP
    $mail->Host       = 'smtp.gmail.com';                     //Set the SMTP server to send through
    $mail->SMTPAuth   = true;                                   //Enable SMTP authentication
    $mail->Username   = 'email người gửi';                     //SMTP username
    $mail->Password   = 'pass';                               //SMTP password
    $mail->SMTPSecure = PHPMailer::ENCRYPTION_STARTTLS;            //Enable implicit TLS encryption
    $mail->Port       = 587;  //Port Gmail là 587, các port phù thuộc vào SMTP của hãng cung cấp       
```

Các tham số người nhận:
```bash
    //Recipients
    $mail->setFrom('emaol người gửi', 'tên hiển thị');
    $mail->addAddress('email người nhận', 'tên');     //Add a recipient
    // $mail->addReplyTo('info@example.com', 'Information');
    // $mail->addCC('cc@example.com');
    $mail->addBCC('email người nhận BCC');
```

Tham số thư:
```bash
    //Attachments
    // $mail->addAttachment('/var/tmp/file.tar.gz');         //Add attachments
    // $mail->addAttachment('/tmp/image.jpg', 'new.jpg');    //Optional name

    //Content
    $mail->CharSet = 'UTF-8';  // Đặt mã hóa UTF-8 cho email để gửi tiếng việt ko lỗi

    $mail->isHTML(true);                                  //Set email format to HTML
    $mail->Subject = 'Đã tiếp nhận đơn hàng Microsoft 365 của bạn!';
    // $mail->Body    = '';
    $mail->Body = file_get_contents('a.html');
    $mail->AltBody = 'This is the body in plain text for non-HTML mail clients';

```


## 🚀 About Me
Hello 👋I am Vinh. I'm studying HCMC University of Technology and Education

**Major:** Electronics and Telecommunication

**Skill:** 

*- Microcontroller:* ESP32/8266 - ARDUINO - PIC - Raspberry Pi

*- Programming languages:* C/C++/HTML/CSS/PHP/SQL and
related Frameworks (Bootstrap)

*- Communication Protocols:* SPI, I2C, UART, CAN

*- Data Trasmissions:* HTTP, TCP/IP, MQTT
## Authors

- [@my_fb](https://www.facebook.com/vcao.vn)
- [@my_email](contact@vinhcaodatabase.com)

## Demo

![Logo](https://codingninja.asia/images/codeninjalogo.png)

## Hướng dẫn

https://www.youtube.com/watch?v=yi2b9U1kQyc&t=1s

