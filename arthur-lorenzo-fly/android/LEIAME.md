# Arthur Lorenzo Fly — app Android

O app abre o jogo (`app/src/main/assets/index.html`) em tela cheia, deitado.

## Gerar o APK

- **Pelo GitHub:** acontece sozinho a cada mudança no `index.html` do jogo (veja `.github/workflows/arthur-lorenzo-fly-apk.yml` na raiz do repositório). O APK aparece em **Releases**.
- **Pelo Android Studio:** copie o `../index.html` (pasta do jogo) para `app/src/main/assets/`, abra esta pasta e use **Build > Build APK(s)**. O arquivo sai em `app/build/outputs/apk/debug/app-debug.apk`.
