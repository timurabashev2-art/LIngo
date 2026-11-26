# LINGO — Android starter project

Это стартовый нативный Android-проект с иконкой LINGO и базовыми рабочими экранами:
- гостевой вход;
- выбор языка и поиск по каталогу;
- короткий входной тест;
- простые упражнения;
- локальное сохранение выбранного языка, уровня и XP;
- экран прогресса.

## Важно
Это ранний MVP, а не завершённый продукт. В каталоге есть большой набор языков, но полноценные курсы для каждого языка ещё не подготовлены. Голосовые звонки, распознавание речи, синхронизация между устройствами, настоящие награды A1–C2, Android-виджеты и полноценная светлая тема требуют следующих этапов разработки. Разделы, которые ещё не готовы, явно обозначены в приложении.

## Сборка APK на Windows
1. Установи Android Studio с официального сайта Android Developers.
2. Распакуй ZIP.
3. В Android Studio выбери **Open** и открой папку `LINGO_Android_Project`.
4. Дождись Gradle Sync. При запросе установи Android SDK Platform 35 и Build Tools.
5. Выбери **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
6. APK появится в `app/build/outputs/apk/debug/app-debug.apk`.

Для установки на телефон передай APK на Android и открой его. Android может попросить разрешить установку из этого источника.

Package: `com.lingo.app`
Version: `0.1.0`


## Build an APK without installing Android Studio

This project includes a GitHub Actions workflow at `.github/workflows/android.yml`.

1. Create a GitHub account and a new **public or private** repository.
2. Extract this ZIP on your computer.
3. Upload the *contents* of the extracted folder to the repository (the files `build.gradle`, `settings.gradle`, and the `app` folder should be at the repository root).
4. Open the repository's **Actions** tab. The workflow named **Build LINGO APK** starts automatically after a push to `main`. You can also select it and press **Run workflow**.
5. When the run finishes successfully, open that run, find **Artifacts**, and download **LINGO-debug-APK**. The APK is inside the downloaded artifact ZIP.

This creates a debug APK for testing. It is not a signed Google Play release. The workflow builds the existing starter app; it does not add unfinished features such as voice calls or speech recognition.
