# 🌠 Android Servisleri

## 👀 Servislere Genel Bakış

* 🚧 Android'de arkaplanda çalışmak için [Background Tasks](https://developer.android.com/guide/background) dokümanına bakılmalıdır
* 👮‍♂️ Android arka plan işlemlerini, [resmi dokümanında](https://developer.android.com/guide/background) da bataryayı korumak adına [buradaki](https://developer.android.com/about/versions/oreo/background.html) kısıtları uyguladığını belirtmektedir
  * Kullanıcıya arayüz \(UI\) sağlamayan her arkaplan işlemi \(Background Service\) kısıtlı sürede çalışır
  * Kısıtlanmayı engellemek adına [Foreground Service](https://developer.android.com/guide/components/services#Foreground) yapısı kullanılır
    * Kullanıcıya [kaldırılamayan bir bildirim](https://developer.android.com/guide/topics/ui/notifiers/notifications.html#foreground-service) gösterilir
    * Kullanıcı arkaplan işlemlerinden haberdar olur
  * Servisin birden fazla istekle baş etmesi gerekirse [IntentService](https://developer.android.com/guide/components/services#ExtendingIntentService) yerine [Service](https://developer.android.com/guide/components/services#ExtendingService) kullanılır
  * Servis tek bir işle baş edecek ise [IntentService](https://developer.android.com/guide/components/services#ExtendingIntentService) yapısı kullanılabilir
    * Çok fazla kısıtlamaya tabi tutulan
    * Tek bir istek için kullanılan
    * İşi bittiğinde kapanan bir sistemdir
* 🌑 Cihaz uyku moduna girdiğinde arka plan işlemleri aksamaya başlar, bundan dolayı [WakeLock](https://developer.android.com/training/scheduling/wakelock#java) özelliğinin aktif olması gerekir
* ⏳ Uzun süreli işlemler için hızı ve verimliliği artırma adına [multi-threading](https://developer.android.com/training/multiple-threads/) yapısı tercih edilmelidir

## 🌞 Foreground Services

Kullanıcının bildirim veya arayüz ile haberi olan arkaplan görevleridir

* Önceli servislerdir ve öncelik seviyesi bildirilmelidir
* Kullanıcıya [kaldırılamayan bir bildirim](https://developer.android.com/guide/topics/ui/notifiers/notifications.html#foreground-service) gösterilmesi zorunludur
* Kullanıcının arkaplan işlemlerinden haberdar olması amaçlanır
* Servisin çalıştırılması için [`FOREGROUND_SERVICE`](https://developer.android.com/reference/android/Manifest.permission.html#FOREGROUND_SERVICE) iznine ihtiyaç duyulur
  * Android'in [izin isteme hiyerarşisine](https://developer.android.com/guide/topics/permissions/overview) uygun ilerler
  * İzin alınmadığı taktirde [`SecurityException`](https://developer.android.com/reference/java/lang/SecurityException.html) hatası verir

{% hint style="info" %}
🧙‍♂️ Android dokümanında [Running a service in the foreground](https://developer.android.com/guide/components/services#Foreground) alanında işlenmektedir
{% endhint %}

