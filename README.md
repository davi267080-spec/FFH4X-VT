# FFH4X VT — projeto Android

Este projeto empacota a interface HTML do FFH4X VT em um aplicativo Android usando WebView.

## Requisitos
- Android Studio atualizado
- JDK 17 (normalmente incluído no Android Studio)
- Android SDK Platform 35 instalado pelo SDK Manager

## Como gerar o APK
1. Extraia `FFH4X_VT_Android.zip`.
2. Abra o Android Studio e escolha **Open**.
3. Selecione a pasta `FFH4X_VT_Android` extraída (a pasta que contém `settings.gradle`).
4. Aguarde a sincronização do Gradle. Se solicitado, instale o Android SDK Platform 35 pelo SDK Manager.
5. Para criar um APK de teste, escolha **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
6. Quando terminar, clique em **locate** na notificação do Android Studio. O APK normalmente fica em `app/build/outputs/apk/debug/app-debug.apk`.
7. Transfira o APK para o celular e abra-o para instalar. Talvez seja necessário permitir a instalação para o app usado para abrir o arquivo.

## Observações
- O projeto não inclui um APK já compilado; ele inclui o código-fonte para compilar no Android Studio.
- A interface e o botão de injeção são demonstrativos. O app não se conecta ao Free Fire e não injeta códigos no jogo.
- Para publicar na Play Store, será necessário preparar uma versão de lançamento assinada e atender às políticas atuais da loja.

## Gerar APK usando apenas o celular (GitHub Actions)
1. Crie uma conta em https://github.com/ e um repositório novo chamado `FFH4X-VT`.
2. Envie todos os arquivos e pastas deste projeto para o repositório, mantendo os caminhos. Inclua também a pasta oculta `.github/workflows` e o arquivo `build-apk.yml`.
3. Abra a aba **Actions** do repositório e selecione **Build FFH4X VT APK**. Se aparecer, toque em **Run workflow**.
4. Aguarde o workflow terminar com sucesso. Abra a execução concluída, vá até **Artifacts** e baixe `FFH4X-VT-debug-APK`.
5. Extraia o ZIP baixado para encontrar `app-debug.apk` e instale no Android.
Observação: a interface do GitHub no celular pode dificultar o envio de muitas pastas; se isso acontecer, use o navegador em modo “site para computador”. O workflow compila o APK de teste na nuvem.
