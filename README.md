> Một ngày đẹp trời, bạn thấy trên google play có 1 app quá đỉnh, quá khét. Bạn muốn clone lại app từ UI đến feature? Cách nhanh nhất là có thể bóc chộm app nhà họ. Ở đây tôi sẽ hướng dẫn bạn tìm cách bẻ khoá và tìm kiếm những thứ cần thiết để có thể clone lại app đó. 😎

# Cách ăn chộm resources ඞ

# Apkpure
* Để chộm resources, bạn có thể dùng những phần mềm như `jadx`, nhưng làm sao để `jadx` decompile cho bạn? Việc cần làm là file apk của app mà bạn muốn chộm. Nhưng google play không cho phép tải file apk. Còn `apkpure` thì có.
* Link: [Apkpure](https://apkpure.com/)
* Tìm kiếm bằng tên app

    <img width="959" alt="image" src="https://user-images.githubusercontent.com/84316258/234759076-58dc42ef-a669-4927-b073-64145670f5fc.png">

* Tìm kiếm bằng link google play

    ![Ctrl C](https://user-images.githubusercontent.com/84316258/234759847-a3d094c2-f044-43fe-b2a4-fae315cee95c.png)

## Cách dùng `jadx`?
* Link download: [jadx](https://github.com/Lazygarde/tai-lieu-cac-thu/new/main)

* Open file apk

    <img width="960" alt="image" src="https://user-images.githubusercontent.com/84316258/234756581-2a39747a-e9bb-4ecf-8442-75f87e1e4321.png">
* Resources

    <img width="960" alt="image" src="https://user-images.githubusercontent.com/84316258/234757279-53662503-3d93-4799-81cc-e6d15f9ee41c.png">
* Save decompiled resources

    <img width="960" alt="image" src="https://user-images.githubusercontent.com/84316258/234757867-ab6c9fc7-2df3-4fae-8c49-784ad4b3c387.png">
* Resources

    <img width="856" alt="image" src="https://user-images.githubusercontent.com/84316258/234758188-19e1d9f9-2db8-47a4-a20d-f09e0f663e40.png">

> Vậy là xong. Bạn đã bẻ được khoá để vào được nhà họ rồi. Vậy làm sao để tìm kiếm những thứ mình cần 🤔. Sau đây là những thư mục quan trọng mà bạn cần tìm kiếm.
* `AndroidManifest.xml`:

    <img width="960" alt="image" src="https://user-images.githubusercontent.com/84316258/234762651-4d114f42-9d57-4ff2-802e-30fbe7784d61.png">
    
    Đường dẫn là `resources\AndroidManifest.xml`. Mainifest chứa rất nhiều thông tin quan trọng. Khi tìm hiểu về các công nghệ để có thể làm 1 sản phẩm như app mình đang decompile, bạn không thể bỏ qua Manifest. Vì ở đây sẽ có các thông tin về các Activity, Service, Receiver, Permission, ...

    - Activity: Là màn hình của app. Ví dụ như Splash Screen, Login Screen, Home Screen, ... Có thể giúp ích cho việc hiểu thêm về luồng của app.
    - Service: Là các dịch vụ của app. Ví dụ như dịch vụ nhắn tin, dịch vụ gọi điện, ... Cũng hữu ích trong việc hiểu thêm về luồng của app.
    - Permission: Là các quyền của app. Ví dụ như SET_WALLPAPER, INTERNET, VIBRATE, ... Có thể giúp ích cho việc hiểu thêm về tính năng của app.
    - Receiver: Là các bộ thu của app. Ví dụ như bộ thu tin nhắn, bộ thu cuộc gọi, ... Cũng hữu ích trong việc hiểu thêm về tính năng của app.
* `res`:

    Đối với `res`, bạn có thể tìm thấy hầu hết hình ảnh, âm thanh, font chữ, ... của app. Rất hữu ích trong việc clone giao diện app.

    Một số những thư mục quan trọng như:

    * bộ thư mục `drawable` (drawable, drawable-hdpi, drawable-xhdpi, ...): Chứa tất cả hình ảnh của app. VD như các file png, jpg, webp, xml, ...
    * `layout`: Chứa tất cả các design xml các màn hình của app.
    * `values`: Chứa tất cả các file xml chứa các giá trị của app. VD như các file string, color, dimen, style, ...
    * `raw`: Chứa tất cả các file ở dạng thô. VD như các file json, mp3, wav, ...
    
        Sau 1 buổi tìm kiếm âm thanh trên mạng sao cho giống với app đối thủ, mà quên mất là mình có jadx. 🤦‍♂️

        <img width="960" alt="image" src="https://user-images.githubusercontent.com/84316258/234782640-a0083431-1d4a-4fc9-840f-a2671177c552.png">

        Trong thư mục `raw` có đầy đủ, uy tín luôn. 😂 (Thực ra còn có cả lottie nữa 😂)
    * `font`: Chứa tất cả các font chữ của app.

# Cách bóc chộm API ඞ
