# flutter
Flutterは、Googleが開発したクロスプラットフォームのUIツールキットで、一つのコードベースでiOS、Android、Web、デスクトップアプリを開発できます。

## WindowsへのFlutterのインストール方法
Flutterは、WindowsでもMacでもLinuxでもスマホでもWebでも利用できます。しかしWindowsの利用者は多いわりに、多くのプログラミング言語などはWindowsは他のOSと違い特殊で、リリースが遅れる事もあるので、説明も少なく不便なこともあります。ただし開発ニーズが多いです。  

**WindowsへのFlutterのインストール手順**を、できるだけわかりやすく解説します。

### 1\. Flutter SDKのダウンロード

  * **Flutter公式サイト** ([https://flutter.dev/](https://www.google.com/url?sa=E&source=gmail&q=https://flutter.dev/)) にアクセスします。
  * **Get started** ボタンをクリックし、**Flutter SDK** をダウンロードします。
  * ダウンロードした ZIP ファイルを解凍し、任意の場所に保存します。（例：Z:\\usr\\flutter）

### 2\. 環境変数の設定

  * **Windowsキー+Pause/Breakキー** を押して、システムのプロパティを開きます。
  * **詳細設定** タブの **環境変数** ボタンをクリックします。
  * **システム環境変数** の **Path** を選択し、**編集** ボタンをクリックします。
  * **新規** ボタンをクリックし、Flutter SDKを解凍したフォルダ内の **bin** フォルダのパスを追加します。（例：Z:\\usr\\flutter\\bin）
  * **OK** ボタンを連打して設定を保存します。

### 3\. Android Studioのセットアップ

  * **Android Studio** を起動し、**Plugins** から **Flutter** と **Dart** プラグインをインストールします。
  * **Flutter SDKのパス** を設定します。Android StudioがFlutter SDKの場所を自動検出できない場合は、手動で設定する必要があります。

### 4\. Flutterコマンドの確認

コマンドプロンプトを開き、以下のコマンドを実行して、Flutterが正しくインストールされているか確認します。

```bash
flutter doctor
```
このコマンドを実行すると、Flutterの環境が診断され、不足しているツールや設定などが表示されます。   

実際にスマホのアプリを作成するにはAndroid Studioのエミュレーターが必要です。しかしWebサーバーを作るには、Visual Studioなどは必要が無いですが、Windowsアプリを作るには必要です。

### 5\. エミュレーターまたは実機の準備

  * **Androidエミュレーター:** Android Studioで仮想デバイスを作成できます。
  * **実機:** USBケーブルでAndroid端末を接続します。
  * スマホのアプリ以外のWindows・Mac・Linuxアプリや、Webサーバーを作成では必要ありません。

### 6\. 開発キットの準備やアップデート

  * **Android SDK:** FlutterでAndroidアプリを開発するには、Android SDKが必要です。Android Studioのインストール時に一緒にインストールされます。
  * **Java:** Java Development Kit (JDK) が必要です。Oracleの公式サイトからダウンロードできます。
  * **最新版の利用:** Flutterは頻繁にアップデートされます。最新版を利用することで、新しい機能やバグ修正を利用できます。

### 7\. 新規プロジェクトの作成する
Flutterプロジェクトの作成方法は、Android StudioやVisual Studio CodeといったIDE（統合開発環境）を利用するのが一般的です。しかし開発PCなどがメモリーなどが少ない場合は、コマンドで操作するとリソース負担が減り開発可能になります。

### コマンドでFlutterプロジェクト作成する
以下のコマンドで新規Flutterプロジェクトを作成できます。
```bash
flutter create new_flutter_project
```

### Android StudioでFlutterプロジェクト作成する
1. **Android Studioの起動:** Android Studioを起動し、「Start a new Flutter project」を選択します。
2. **プロジェクトテンプレートの選択:** Flutter Applicationを選択し、Nextをクリックします。
3. **プロジェクトの設定:**
   * **Flutter SDK path:** Flutter SDKのパスを指定します。
   * **Project name:** プロジェクト名を入力します。
   * **Project location:** プロジェクトを保存する場所を指定します。
   * **Description:** プロジェクトの説明を入力します。
   * **Organization:** 組織名を入力します。
   * **Project ID:** プロジェクトのIDを入力します。
4. **プラットフォームの選択:** Android、iOS、または両方を選択できます。
5. **言語の選択:** Dart言語を選択します。
6. **Finish:** 設定を確認し、Finishをクリックしてプロジェクトを作成します。

#### プロジェクト構造

作成されたプロジェクトの主なフォルダとファイルは以下の通りです。

* **lib:** Dartソースコードを記述するフォルダです。
* **android:** Android用のネイティブコードが格納されるフォルダです。
* **ios:** iOS用のネイティブコードが格納されるフォルダです。
* **pubspec.yaml:** プロジェクトで使用するパッケージを管理するファイルです。

### Flutterプロジェクトの構造と基本的な使い方

* **main.dart:** アプリケーションのエントリーポイントとなるファイルです。
* **Widget:** FlutterのUIを構成する基本的な要素です。
* **StatelessWidget:** 状態を持たないWidgetです。
* **StatefulWidget:** 状態を持つWidgetです。
* **ホットリロード:** コードを変更すると、シミュレーターや実機上のアプリが自動的に更新される機能です。
* **状態管理:** Provider、Riverpod、BLoCなど、Flutterの状態管理ライブラリを利用して、アプリの状態を管理することができます。
* **パッケージ:** pub.devで公開されているパッケージを利用することで、機能を拡張することができます。

### スマホのアプリを作る（ビルドする）
ビルドとはGoogle Play（Android）やApp Store（iOS）で公開できるファイル（いわゆるスマホのアプリ）を作成することです。
* `flutter build apk`コマンドでAndroid用のAPKファイルを作成できます。
* `flutter build ios`コマンドでiOS用のIPAファイルを作成できます。

コマンドを入力したら以下の場所にビルドしたファイルが作成されます。
```
コマンドを打ったルート\build\app\outputs\flutter-apk\app-release.apk
```
  
コマンドを入力し以下のエラーが出る場合は、パスは日本語やUnicodeなどではなく、ANSI文字のみにしてください。
```bash
flutter build apk
Your project path contains non-ASCII characters
```
たぶん他のプログラミング言語なども、ANSI文字のみにしないとエラーが多く出ると思います。また環境変数のパスなどは_と-を混じらせると認識しない場合もあります。昔のUnixでは頭文字が大文字（HTML書類名がIndex.html）と小文字（HTML書類内でindex.html）だと認識せずに、これに類似したルータで広域接続障害もありました。

### 8\.プロジェクトを実行する
プロジェクトを実行するには複数の方法があります。多くはAndroid Studioで実行ですが、他にメモリーが軽量なコマンド入力や、特殊な例としてAPKファイルなどを、Windowsなどのスマホの仮想アプリにインストールして起動も出来ます。

#### デスクトップアプリやWebサーバーとして起動する
作成したプロジェクトをデスクトップアプリやWebサーバーとして起動するには、Android Studioのツールバーにある実行ボタンをクリックするか、ターミナルで以下のコマンドを実行します。
```bash
flutter run
```
このコマンドを入力後に、起動したOSのデスクトップアプリかWebブラウザーのどれで起動するのか聞いてきますので、選ぶと選んだOSのアプリやWebブラウザーで起動します。しかし例えばWindowsを選んでも、デスクトップアプリの開発ソフトであるVisualStadioがインストールされていないと起動しませんので、インストールしてください。

#### スマホのアプリとして起動する
ビルドしたAPK（Andorid）ファイルかIPA（iOS）ファイルを、Windowsなどのスマホの仮想アプリか、スマホの実機にファイル転送しアイコンを押すと、インストールなどされて起動できます。ただし証明書をつけるなどをしないと、セキュリティ機能で拒否するかもしれません。  

これが野良アプリという状態で悪意のあるプログラムもあり、Google PlayやApp Storeでは証明書をつけたり審査をしているので、不明なWebサイトで配布されているAPLやIPAファイルはインストールしない方が良いです。方やDART（テキスト）ファイルはコンパイル（ビルド）済みファイルと違い、ソースコード（中身の文章）が見れるので研究用に、身元不明なものも利用しても良いかもしれません。

### その他
  * **Visual Studio Code:** Visual Studio CodeなどもIDEでもFlutter開発を行うことが出来て、人気があるので開発参加者が多く、多言語対応で、多機能です。
  * コマンド入力やメモ帳などで編集よりも、IDEで作成した方がコパイロットなどのAIによる補助機能などで、簡単に多様な開発が出来ます。
  * **Flutterのドキュメント:** Flutterの公式ドキュメントには、より詳細な情報やチュートリアルが掲載され、最新情報を得た方が良いです。

**より詳しい情報やトラブルシューティングについては、Flutterの公式ドキュメントを参照することをおすすめします。**

### 参考情報

  * **Flutter公式サイト:** [https://flutter.dev/](https://www.google.com/url?sa=E&source=gmail&q=https://flutter.dev/)
  * **Android Studio:** [https://developer.android.com/studio/](https://www.google.com/url?sa=E&source=gmail&q=https://developer.android.com/studio/)

**この回答は、Flutterのインストール手順を簡潔にまとめたものです。より詳細な情報や、特定の環境でのトラブルシューティングについては、上記の公式サイトを参照してください。**
