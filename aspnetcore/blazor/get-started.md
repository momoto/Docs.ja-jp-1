---
title: ASP.NET Core Blazor を使ってみる
author: guardrex
description: 好みのツールで Blazor アプリを構築して、Blazor の使用を開始しましょう。
monikerRange: '>= aspnetcore-3.0'
ms.author: riande
ms.custom: mvc
ms.date: 07/23/2019
uid: blazor/get-started
ms.openlocfilehash: b4609858be43acf9d1b2d8be5eff4879fd56f49f
ms.sourcegitcommit: 051f068c78931432e030b60094c38376d64d013e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/24/2019
ms.locfileid: "68948332"
---
# <a name="get-started-with-aspnet-core-blazor"></a>ASP.NET Core Blazor を使ってみる

作成者: [Daniel Roth](https://github.com/danroth27)、[Luke Latham](https://github.com/guardrex)

Blazor を使ってみる:

1. 最新の[.Net Core 3.0 PREVIEW SDK](https://dotnet.microsoft.com/download/dotnet-core/3.0)リリースをインストールします。

1. コマンドシェルで次のコマンドを実行して、Blazor テンプレートをインストールします。

   ```console
   dotnet new -i Microsoft.AspNetCore.Blazor.Templates::3.0.0-preview7.19365.7
   ```

1. ツールの選択に関するガイダンスに従ってください。

   # <a name="visual-studiotabvisual-studio"></a>[Visual Studio](#tab/visual-studio)

   1 \。 **ASP.NET と web 開発**ワークロードを使用して、最新の[Visual Studio preview](https://visualstudio.com/vs/preview)をインストールします。

   2 \。 新しいプロジェクトを作成します。

   3 \。 **[Blazor App]** を選択します。           **[次へ]** を選択します。

   4 \。 **[プロジェクト名]** フィールドにプロジェクト名を入力するか、既定のプロジェクト名をそのまま使用します。 **場所**エントリが正しいことを確認するか、プロジェクトの場所を指定します。 **[作成]** を選択します。

   5 \。 Blazor クライアント側のエクスペリエンスについては、 **Blazor (クライアント側)** テンプレートを選択してください。 Blazor サーバー側のエクスペリエンスについては、 **Blazor Server アプリ**テンプレートを選択してください。 **[作成]** を選択します。 サーバー側とクライアント側の2つの Blazor ホスティングモデルの詳細については<xref:blazor/hosting-models>、「」を参照してください。

   6 \。 **F5 キー**を押してアプリを実行します。

   > [!NOTE]
   > 以前のプレビューリリースの ASP.NET Core Blazor (Preview 6 以前) 用に Blazor Visual Studio 拡張機能をインストールした場合は、プレビュー7で拡張機能をアンインストールできます。 Visual Studio でテンプレートを表示するには、コマンドシェルに Blazor テンプレートをインストールするだけで十分です。

   # <a name="visual-studio-codetabvisual-studio-code"></a>[Visual Studio Code](#tab/visual-studio-code)

   1 \。 [Visual Studio Code](https://code.visualstudio.com/) のインストール。

   2 \。 [ C# Visual Studio Code 拡張機能の](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp)最新版をインストールします。

   3 \。 Blazor のクライアント側のエクスペリエンスについては、コマンドシェルで次のコマンドを実行します。

      ```console
      dotnet new blazor -o WebApplication1
      ```

      Blazor のサーバー側のエクスペリエンスについては、コマンドシェルで次のコマンドを実行します。

      ```console
      dotnet new blazorserverside -o WebApplication1
      ```

      サーバー側とクライアント側の2つの Blazor ホスティングモデルの詳細については<xref:blazor/hosting-models>、「」を参照してください。

   4 \。 Visual Studio Code で*WebApplication1*フォルダーを開きます。

   5 \。 Blazor のサーバー側プロジェクトの場合、IDE は、プロジェクトをビルドおよびデバッグするためにアセットを追加するように要求します。 **[はい]** を選択します。

   6 \。 Blazor サーバー側アプリを使用している場合は、Visual Studio Code デバッガーを使用してアプリを実行します。 Blazor クライアント側アプリを使用している場合`dotnet run`は、アプリのプロジェクトフォルダーからを実行します。

   7 \。 ブラウザーで、`https://localhost:5001` に移動します。

   <!--

   # [Visual Studio for Mac](#tab/visual-studio-mac)

   1\. Install [Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/). Switch the [Update channel to Preview](/visualstudio/mac/install-preview).

   2\. Select **File** > **New Solution** or **New Project**.

   3\. In the sidebar, select **.NET Core** > **App**.

   4\. For a Blazor server-side experience, select the **ASP.NET Core Blazor Server App** template. For a Blazor client-side experience, select the **ASP.NET Core Blazor WebAssembly App** template. Select **Next**. For information on the two Blazor hosting models, server-side and client-side, see <xref:blazor/hosting-models>.

   5\. The **Target Framework** defaults to **.NET Core 3.0**. Select **Next**.

   6\. In the **Project Name** field, enter `WebApplication1`. Select **Create**.

   7\. Select **Run** > **Run Without Debugging** to run the app *without the debugger*. Running with the debugger isn't supported at this time.

   -->

   # <a name="net-core-clitabnetcore-cli"></a>[.NET Core CLI](#tab/netcore-cli/)

   Blazor のクライアント側のエクスペリエンスについては、コマンドシェルで次のコマンドを実行します。

   ```console
   dotnet new blazor -o WebApplication1
   cd WebApplication1
   dotnet run
   ```

   Blazor のサーバー側のエクスペリエンスについては、コマンドシェルで次のコマンドを実行します。

   ```console
   dotnet new blazorserverside -o WebApplication1
   cd WebApplication1
   dotnet run
   ```

   サーバー側とクライアント側の2つの Blazor ホスティングモデルの詳細については<xref:blazor/hosting-models>、「」を参照してください。

   ブラウザーで、`https://localhost:5001` に移動します。

   ---

サイドバーのタブからは、複数のページを使用できます。

* ホーム (Home)
* カウンター
* データのフェッチ

Counter ページ上で **[クリックしてください]** ボタンを選択し、ページを更新することなくカウンターをインクリメントします。 通常、web ページでカウンターを増やすには JavaScript を記述する必要がありますがC#、を使用して Razor コンポーネントの方が優れています。

*Pages/Counter.razor*:

[!code-cshtml[](get-started/samples_snapshot/3.x/Counter1.razor?highlight=7,12-15)]

ブラウザーでの`/counter`要求が、上部の`@page`ディレクティブで指定されている場合、コンポーネント`Counter`はそのコンテンツをレンダリングします。 コンポーネントは、レンダリングツリーのメモリ内表現にレンダリングされ、柔軟で効率的な方法で UI を更新するために使用できます。

**[クリックし**てください] ボタンが選択されるたびに、次のようになります。

* `onclick`イベントが発生します。
* `IncrementCount` メソッドが呼び出された場合。
* `currentCount`がインクリメントされます。
* コンポーネントが再び表示されます。

ランタイムは、新しいコンテンツを前のコンテンツと比較し、変更されたコンテンツのみをドキュメントオブジェクトモデル (DOM) に適用します。

HTML 構文を使用してコンポーネントを別のコンポーネントに追加します。 たとえば、コンポーネントに`Counter` `<Counter />` `Index`要素を追加して、コンポーネントをアプリのホームページに追加します。

*Pages/Index.razor*:

[!code-cshtml[](get-started/samples_snapshot/3.x/Index1.razor?highlight=7)]

アプリを実行します。 ホームページには、 `Counter`コンポーネントによって提供される独自のカウンターがあります。

コンポーネントのパラメーターは、属性または[子コンテンツ](xref:blazor/components#child-content)を使用して指定されます。これにより、子コンポーネントのプロパティを設定できます。 `Counter`コンポーネントにパラメーターを追加するには、コンポーネントの`@code`ブロックを更新します。

* 属性`[Parameter]`を使用し`IncrementAmount`て、のプロパティを追加します。
* `currentCount` の値を増やすときに `IncrementAmount` を使うように `IncrementCount` メソッドを変更します。

*Pages/Counter.razor*:

[!code-cshtml[](get-started/samples_snapshot/3.x/Counter2.razor?highlight=12-13,17)]

属性を`IncrementAmount`使用し`Index`て、 `<Counter>`コンポーネントの要素でを指定します。

*Pages/Index.razor*:

[!code-cshtml[](get-started/samples_snapshot/3.x/Index2.razor?highlight=7)]

アプリを実行します。 コンポーネントには、 **[クリックし**てください] ボタンが選択されるたびに10ずつ増加する独自のカウンターがあります。 `Index` の`Counter`コンポーネント (*Counter*) `/counter`は、1つずつ増加し続けています。

## <a name="next-steps"></a>次の手順

<xref:tutorials/first-blazor-app>

## <a name="additional-resources"></a>その他の資料

* <xref:signalr/introduction>