# Kotlin Gradle Repositories for Iran 🇮🇷

> Ready-to-use Gradle repository configurations for Kotlin Multiplatform, Android, JVM, and Java projects.

اگر هنگام Sync یا دانلود Dependencyها با سرعت پایین، Timeout یا محدودیت در دسترسی به Repositoryهای Maven مواجه هستید، این پروژه مجموعه‌ای از Repositoryهای جایگزین (Mirror) را در اختیار شما قرار می‌دهد که تنها با چند خط تنظیمات قابل استفاده هستند.

این تنظیمات برای پروژه‌های **Kotlin Multiplatform، Android، JVM و Java** مناسب بوده و از Gradle 7 به بعد قابل استفاده هستند.

---

## ✨ ویژگی‌ها

- ✅ مناسب برای Kotlin Multiplatform
- ✅ مناسب برای Android
- ✅ مناسب برای Java
- ✅ مناسب برای Kotlin/JVM
- ✅ سازگار با Gradle 7+
- ✅ سازگار با Gradle 8+
- ✅ سازگار با Gradle 9+
- ✅ دارای چندین Mirror داخلی و خارجی
- ✅ دارای Fallback به Repositoryهای رسمی
- ✅ آماده برای Copy & Paste

---

# 🚀 Usage

## settings.gradle.kts

```kotlin
pluginManagement {
    repositories {

        // Community Mirrors
        maven("https://en-mirror.ir")
        maven("https://maven.devneeds.ir")
        maven("https://gradle.iranrepo.ir")
        maven("https://gradle.jamko.ir")
        maven("https://archive.ito.gov.ir/gradle/maven-plugin/")

        // Myket Mirror
        maven("https://maven.myket.ir")

        // Aliyun Mirrors
        maven("https://maven.aliyun.com/repository/gradle-plugin")
        maven("https://maven.aliyun.com/repository/google")

        // Official repositories
        google()
        gradlePluginPortal()
        mavenCentral()
    }
}

dependencyResolutionManagement {

    repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)

    repositories {

        // Community Mirrors
        maven("https://en-mirror.ir")
        maven("https://maven.devneeds.ir")
        maven("https://gradle.iranrepo.ir")
        maven("https://gradle.jamko.ir")
        maven("https://archive.ito.gov.ir/gradle/maven-plugin/")

        // Myket Mirror
        maven("https://maven.myket.ir")

        // Aliyun Mirrors
        maven("https://maven.aliyun.com/repository/public")
        maven("https://maven.aliyun.com/repository/central")
        maven("https://maven.aliyun.com/repository/google")

        //Jitpack Mirror
        maven("https://jitpack.io")

        // Official repositories
        google()
        mavenCentral()
    }
}
```

---

# 💡 چرا از این Repository استفاده کنیم؟

- کاهش احتمال Timeout هنگام دریافت Dependencyها
- استفاده از چندین Mirror به جای یک Repository
- حفظ Repositoryهای رسمی به عنوان Fallback
- مناسب برای پروژه‌های Kotlin Multiplatform
- مناسب برای Android Studio
- مناسب برای IntelliJ IDEA
- بدون نیاز به Plugin اضافی
- راه‌اندازی تنها با Copy & Paste

---

<div dir="rtl">

## 📌 ترتیب قرارگیری Repositoryها

Gradle وابستگی‌ها را به ترتیب Repositoryهای تعریف‌شده بررسی می‌کند. بنابراین توصیه می‌شود **Repository Mirrorها را قبل از Repositoryهای رسمی** مانند <code>Google Maven</code>، <code>Maven Central</code> و <code>Gradle Plugin Portal</code> قرار دهید.

به این ترتیب، Gradle ابتدا از Mirrorها استفاده کرده و در صورت نیاز به‌صورت خودکار به Repositoryهای رسمی مراجعه می‌کند.

</div> Sync و Build می‌شود.

---
# 🤝 مشارکت

اگر Mirror جدیدی می‌شناسید یا یکی از Repositoryها دچار مشکل شده است، خوشحال می‌شوم Issue یا Pull Request ثبت کنید.

پیشنهادها، گزارش خطا و بهبود مستندات نیز استقبال می‌شوند.

---

# 📄 License

MIT License
