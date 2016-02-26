#Windows PowerShell の必要な状態の構成の概要

> Windows PowerShell 4.0 では、Windows PowerShell 5.0 の適用対象:

このトピックでは、Windows PowerShell で Windows PowerShell 必要な状態 Configuration (DSC) の機能について説明します。 DSC の概要を説明し、理解し、DSC を使用する必要がありますドキュメント リソースを見つけるには、このトピックを使用することができます。

##機能の説明

DSC は、展開しソフトウェア サービスの構成データを管理、およびこれらのサービスが実行される環境を管理することができる Windows PowerShell での新しい管理プラットフォームです。

DSC は、Windows PowerShell 言語の拡張機能、新しい Windows PowerShell コマンドレット、およびソフトウェア環境を構成する方法を宣言によって指定に使用できるリソースのセットを提供します。 また、維持し、既存の構成を管理するための手段も提供します。

##実際の適用

次に、いくつかのシナリオ例を構成および自動化された方法で一連のコンピューター (対象のノードとも呼ばれます) を管理する組み込みの DSC リソースを使用することができます。

* 有効にするか、サーバーの役割と機能を無効にします。
* レジストリ設定を管理します。
* ファイルとディレクトリを管理します。
* 開始、停止、およびプロセスやサービスを管理します。
* グループとユーザー アカウントを管理します。
* 新しいソフトウェアを展開します。
* 環境変数を管理します。
* Windows PowerShell スクリプトの実行
* 目的の状態から離れたがある構成を修正する方法
* 特定のノードで、実際の構成の状態を検出します。

##主要な概念

DSC は、構成、展開、およびシステムの管理に使用される宣言型のプラットフォームです。 次の 3 つの主要なコンポーネントで構成されます。

* [構成](configurations.md) 定義およびリソースのインスタンスを構成する宣言型の PowerShell スクリプトを示します。 構成、DSC (および、リソースの構成によって呼び出される) を実行しているは単に「をできるように、」は、システムが、構成によってレイアウトの状態が存在することすることです。 DSC 構成はべき等でも。 ローカル構成マネージャー (LCM) は、構成がどのステート マシンが構成されていることを確認引き続きを宣言します。
* リソースとは、命令型のビルド ブロック DSC サブ システムのさまざまなコンポーネントをモデル化し、変更の状態の制御フローの実装に書き込まれます。 PowerShell モジュール内に存在し、何か、ファイルまたは Windows プロセスとしてジェネリックまたは具体的には、IIS サーバーまたは Azure で実行されている仮想マシンとしてモデル化するように記述できます。
* ローカル構成マネージャー (LCM) とは、DSC をするには、リソースの構成の間の相互作用を容易にするエンジンです。 LCM は、リソースによって実装される制御フローを使用して、構成によってレイアウトの状態が維持されていることを確認する、システムに定期的にポーリングを行います。 状態から、システムがある場合、LCM を「行うよう」構成宣言に従ってリソース内の複数のロジックを使用します。

DSC には、さまざまな新しい言語キーワード、コマンドレット、および DSC リソースの構成では、ヘルプのビルドの作成を許可する、構成を呼び出す、および、LCM を管理するツールも含まれています。 PsDesiredStateConfig モジュールの一部として、Windows 8.1 でのこれらのコマンドレットの多く見つかんだことができます (など `開始 DscConfiguration`, 、`セット DscLocalConfigurationManager`, 、および `Get DscResource`)。 XDscResourceDesigner (で見つかった、 [PowerShell ギャラリー](https://www.powershellgallery.com/packages/xDSCResourceDesigner/)) を DSC リソースの開発を簡略化するためのコマンドレットのコレクションです。

##関連項目

* [DSC の構成](configurations.md)
* [DSC リソース](resources.md)
* [ローカルの Configuration Manager の構成](metaconfig.md)




