# Git ve GitHub Rehberi

## Git ve GitHub Aşamaları

1. **Çalışma Alanı**: Kodun yazıldığı ve düzenlendiği yerel alandır.
2. **Geçici Alan**: Commit'e hazırlanmış dosyaların bulunduğu geçici alan.
3. **Yerel Depo**: Commit'lerin kaydedildiği yerel depo.
4. **GitHub (Uzak Depo)**: Kodların çevrimiçi olarak depolandığı platform.

## Terminal Komutları

- **`pwd`**: Bulunduğun dosya yolunu gösterir.
- **`git init`**: Bulunduğun klasörü Git'e ekler.
- **`git status`**: Hangi dosyaların takip edilip edilmediğini gösterir.
- **`git add .`**: “.` sayesinde klasördeki tüm dosyaların takip edilmesini sağlar. Eğer nokta yerine dosya ismi yazsaydı, sadece o dosya takip edilirdi.
- **`git config --global (user.name || user.email)`**: Commit'leri kimin yaptığını bilmesi için isim ve email girilmesi gerekmektedir.
- **`git commit -m "mesaj"`**: Tüm yapılan değişiklikleri yerel depoya kaydeder.
- **`git log`**: Commit geçmişini gösterir. (`--oneline` komutunu eklersek, sadece commit'lerin başlıklarını ve mesajlarını görürüz.)
- **`git diff`**: Yapılan tüm değişiklikleri gösterir. (Bu değişiklikler, geçici alanda tutulanlar için geçerlidir.)
- **`git diff dosyaadı.uzantı`**: Sadece belirtilen dosyadaki yapılan değişiklikleri gösterir.
- **`git diff --staged`**: Geçici alandaki değişiklikleri görmeye yarar.
- **`git restore text.txt`**: Bir dosyada yapılan değişikliği geri alır. Bu komut, dosyayı son commit edilmiş haline geri döndürür.
- **`git restore .`**: Çalışma alanındaki tüm değişiklikleri geri alır.
- **`git reset`**: Geçici alana gönderilmiş dosyaları geri getirir.
- **`git remote add origin repo-link`**: Uzak bir depo bağlantısını ekler.
- **`git push -u origin master`**: Yerel depodaki değişiklikleri uzaktaki depoya gönderir.
- **`git clone projelinki`**: GitHub'daki projeyi bilgisayarınıza indirir.
- **`git remote -v`**: Uzak bağlantıları gösterir.
- **`git fetch`**: Projedeki değişiklikleri getirir ancak çalışma alanına eklemez.
- **`git diff master..origin/master`**: Yapılan değişiklikleri gösterir.
- **`git merge`**: Güncellenen dosyaları çalışma alanına dahil etmek için kullanılır.
- **`git pull origin master`**: Fetch ve merge işlemlerini birleştirir.

## Ekip Çalışması

- **`git branch`**: Anlık olarak hangi branch'te olduğunuzu ve diğer branch'leri gösterir.
- **`git switch -c branchName`**: Yeni bir branch açar ve o branch'e geçer. Örn: `git switch -c feature/login-system`
- **`git push -u origin feature/login-system`**: Ana branch yerine farklı bir branch'i uzaktaki repoya gönderir.
- **`git merge feature/login-system`**: Ana branch'te (master) iken, merge komutunu çalıştırdığınızda `feature/login-system` branch'i ile birleşir.  
  **Not**: Merge işlemi yapılmadan önce, ana kodun güncel olduğundan emin olunmalıdır.

## Git Commit Yönetimi

- **`git commit --amend`**: Commit mesajının düzenlenmesini sağlar. (Komut satırında `wq` yazarak kaydedip çıkabilirsiniz.)
- **`git checkout hash`**: Eski commit'ler arasında dolaşmanıza olanak tanır.
- **`git reset --soft HEAD~1`**: Son commit'i siler, ancak değişiklikler geçici alanda kalır.
- **`git reset --mixed HEAD~1`**: Son commit'i siler ve değişiklikleri çalışma alanına aktarır.
- **`git reset --hard HEAD~1`**: Son commit'i tamamen siler. (Sonrasında `git push --force` kullanmak gerekir.)
- **`git revert hash`**: Commit'i kaldırmak için yeni bir commit oluşturur. (Bu yöntem `git reset --hard`'ın aksine daha güvenlidir.)
- **`git reflog`**: Silinmiş veya silinmemiş tüm commit geçmişini gösterir. (Bu kayıtlar sadece 90 gün boyunca tutulur. Yani commit'in silinmesinden itibaren 90 gün sonra reflog'dan da silinir.)
- **`git reset --hard hash`**: Buraya silinmiş commit'in reflog'dan alınmış hash'ini girerseniz, commit'i geri getirebilirsiniz.

## README İçeriği

1. **Logo**: Projeye ait logo.
2. **Proje Adı ve Açıklaması**: Projenin adı ve kısa açıklaması.
3. **İçindekiler**: Proje içeriğini sıralayan liste.
4. **Kurulum**: Projeyi kurmak için gerekli adımlar.
5. **Kullanım**: Projeyi nasıl kullanabileceğinize dair bilgiler.
6. **Özellikler**: Projede bulunan özellikler.
7. **Katkıda Bulunma**: Başkalarının projeye nasıl katkıda bulunabileceği.
8. **Destek ve İletişim**: Proje ile ilgili destek ve iletişim bilgileri.
9. **Lisans**: Projeye ait lisans bilgisi.
10. **Teşekkür**: (Varsa Sponsorluklar ve Destekçiler)

---

Bu rehber, Git ve GitHub kullanımınızı kolaylaştırmak ve süreci daha anlaşılır kılmak için hazırlanmıştır.
