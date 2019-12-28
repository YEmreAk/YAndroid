---
description: Android üzerinde verileri kaydetme
---

# 🔸 Veri Saklama Yöntemleri

## 🆚 Shared Preference vs Saved Instance State

| 👐 Shared Preference | 💾 Saved Instance State |
| :--- | :--- |
| Uygulama hatta cihaz kapatılsa dahi veriler korunur | Sadece Activity üzerinde verileri saklar |
| Temel veriler için kullanılır | Anlık veriler için tercih edilir |
| Az sayıda anahtar / değer çifti ile saklanır | Az sayıda anahtar / değer çifti ile saklanır |
| Veriler uygulamaya özgüdür \(gizli\) | Veriler uygulamaya özgüdür \(gizli\) |
| Genellikle kullanıcı tercihleri için kullanılır | Cihazın yapılandırma ayarlarında veri kaybını engellemek için kullanılır |

{% hint style="info" %}
‍🧙‍♂ Detaylar için  [Shared preferences vs. saved instance state](https://google-developer-training.github.io/android-developer-fundamentals-course-concepts-v2/unit-4-saving-user-data/lesson-9-preferences-and-settings/9-1-c-shared-preferences/9-1-c-shared-preferences.html#whentouse) alanına bakabilirsin.
{% endhint %}

## 🆚 Shared Preference vs Database

{% embed url="https://stackoverflow.com/a/6276936/9770490" %}

## 📜 JSON Verilerini İşleme

{% embed url="https://stackoverflow.com/a/9606629/9770490" %}

