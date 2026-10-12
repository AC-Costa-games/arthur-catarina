# Arthur Lorenzo Fly — app Android

O app abre o jogo (`app/src/main/assets/index.html`) em tela cheia, deitado.

## Gerar o APK

- **Pelo GitHub:** acontece sozinho a cada mudança no `index.html` da raiz (veja `.github/workflows/gerar-apk.yml`). O APK aparece em **Releases**.
- **Pelo Android Studio:** copie o `index.html` da raiz para `app/src/main/assets/`, abra esta pasta e use **Build > Build APK(s)**. O arquivo sai em `app/build/outputs/apk/debug/app-debug.apk`.
