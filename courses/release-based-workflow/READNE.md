
<!--
    The step and endstep markers will cause this 
    introduction content to be hidden once the 
    repository is created off the template
-->

# Create a release based workflow

<!--step0-->
[GitHub flow](https://guides.github.com/introduction/flow/)を基盤にしてリリースベースのワークフローを作成します。GitHubでリリースベースのワークフローを使用すると、プロジェクトでデプロイ可能なイテレーションをパッケージ化し、より多くのユーザーがダウンロードして使用できるようなコラボレーションを簡単に実現できます。

GitHub Releases機能を使用すると、チームはプロジェクトの履歴の特定の時点に基づいて、ソフトウェアをパッケージ化してユーザーに提供できます。

- **対象者** ：開発者、DevOps エンジニア、IT運用者、マネージャー、およびチーム。
- **学習内容**：リリースベースのワークフローのやりかた。
- **作成するもの**：タグ、リリース、およびリリースノートを作成します。
- **前提条件**：ブランチ、コミット、およびプル リクエストについて学習する必要がある場合は、まず[Introduction to GitHub](https://github.com/skills/introduction-to-github)を受講してください。（※[翻訳済み](../introduction-to-github/README.md)）
- **所要時間**：このコースの長さは7ステップで、完了までに1時間もかかりません。

## このコースの開始方法

1. このイントロダクションの上部にある、**Use this template**ボタンを右クリックし、新しいタブでリンクを開きます。
   ![Use this template](https://user-images.githubusercontent.com/1221423/169618716-fb17528d-f332-4fc5-a11a-eaa23562665e.png)
2. 新しく開いたタブで、手順に従って新しいリポジトリを作成します。(※元の文では明記されていませんが、このチュートリアルでは`Include all branches`のチェックが必須です。)
   - パブリックリポジトリを作成することをお勧めします。――プライベートリポジトリの場合、[アクションにかかった時間分だけ請求が発生します](https://docs.github.com/en/billing/managing-billing-for-github-actions/about-billing-for-github-actions)。
   ![Create a new repository](https://user-images.githubusercontent.com/1221423/169618722-406dc508-add4-4074-83f0-c7a7ad87f6f3.png)
3. 新しいリポジトリが作成されたら、約20秒待ってから、ページを更新します。新しいリポジトリのREADMEにある手順に従って操作を行ってください。
<!--endstep0-->

<!--Step 1-->
<details id=1 >
<summary><h2>Step 1: ベータ版リリースを作成してみよう</h2></summary>

### GitHub flowについて

[GitHub flow](https://guides.github.com/introduction/flow/)は、規則的なデプロイを伴うプロジェクト向けの、軽量のブランチベースのワークフローです。

![github-flow](https://user-images.githubusercontent.com/6351798/48032310-63842400-e114-11e8-8db0-06dc0504dcb5.png)

一部のプロジェクトは、継続的なデプロイにより、より頻繁にデプロイされることもあります。このようなプロジェクトでは、メインブランチに新しいコミットがあるたびに「リリース」とみなされるかもしれません。

しかし、プロジェクトによっては、このようなバージョンとリリースの取り扱いをせず、異なる構造に依存しているということもあります。

### バージョンについて

バージョンは、OS、アプリ、依存関係など、更新されるソフトウェアのさまざまな繰り返しの開発サイクルです。一般的な例は、Windowsなら「Windows 8.1」「Windows 10」、MacOSならば「macOS High Sierra」「macOS Mojave」といったものです。

開発者はコードを更新し、プロジェクトでバグのテストを実行します。その間、開発者は新しいコードやバグから保護するために特定のセキュリティを設定する場合があります。その後、テスト済みのコードを本番環境で使用できるようになります。チームはコードをバージョン管理し、エンドユーザーがインストールできるようにリリースします。

### ⌨️ Activity: 現在のコードベースのリリース作ってみよう
このステップでは、GitHubでこのリポジトリのリリースを作成します。

GitHubのリリースは、特定のコミットのことを指します。リリースには、Markdownファイルのリリースノートと、バイナリを添付して含めることができます。

大規模なリリースにリリースベースのワークフローを使用する前に、タグとリリースを作成しましょう。

1. 新しいブラウザー タブを開き、このタブの指示を読みながら、2番目のタブの手順に取り組みます。
2. このリポジトリの**Releases**ページに移動します。
  - リポジトリの上部にある**Code**タブをクリックできます。次に、リポジトリの説明の下にあるナビゲーション バーを見つけて、**0 releases**をクリックします。(※GitHubのUI変更で場所や表示が変わっている。リリースが存在しないときはリリース数が表示されなくなったため、2022/08現在では、Codeページ=>画面右側のペインからReleasesをクリックしてリリースページを開くことができる)
3. **Create a new release**ボタンをクリックします
4. _Tag Version_ のフィールドで、番号を指定します。この場合、**v0.9**を使用します。ターゲットは**main**のままにしておいてください。(※GitHubのUI変更で変わっている。2022/08現在では、Tag Versionフィールドではなく、Chose a Tagのトグルダウンをクリックし、v0.9を入力欄に入力して、Create new tagで新しくタグを作成する)
5. 「最初のベータ版リリース(First beta release)」のように、リリースにタイトルを付けます。必要に応じて、リリースに簡単な説明を付けることもできます
6. ベータ版のリリースであるため、**This is a pre-release** の横にあるチェックボックスを選択します。
7. **Publish release**ボタンをクリックします
8. 約20秒待つと、次のステップのためにこのページが更新されます

</details>

<!--Step 2-->
<details id=2>
<summary><h2>Step 2: リリースブランチに新しい機能を追加してみよう</h2></summary>

### リリースマネジメント

将来のリリースの準備をするときは、タスクや機能以上のものを整理する必要があります。チームの明確なワークフローを作成し、作業が整理されていることを確認することが重要です。

リリースを管理する方法はいくつかあります。`production`, `dev`, `main`といった、存続期間の長いブランチを使用する場合もあれば、一部のチームは、シンプルな機能ブランチを利用し、メインブランチからリリースする場合もあります。

1つの戦略が別の戦略よりも優れているということはありません。ですが、GitHubでは、可能な限り、ブランチについて意識的に考え、存続期間の長いブランチを減らすことを推奨しています。

この演習では、リリースバージョンごとに1つの長期ブランチを利用する戦略を採用し、`release-v1.0`ブランチをリリースブランチとして使用します。

### 保護されたブランチ(Protected branches)
`main`ブランチと同様に、リリースブランチも保護することができます。これは、強制プッシュや誤った削除からブランチを保護できることを意味します。このリポジトリでは既に構成済です。

### 機能の追加
リリースは通常、数多くの小さな変更で構成されます。バグを把握していないため、バージョン アップデートの前にゲームで更新するいくつかの機能に焦点を当てます。

- ページの背景色を黒に更新する必要があります。
- テキストの色を緑に変えるお手伝いをします。

### ⌨️ Activity: `base.css`のアップデート

1. `main`ブランチから新しいブランチを作成し、以下のように`base.css`内の`body`のCSS定義を変更します。これにより、ページの背景が黒に設定されます

```css
body {
    background-color: black;
}
```

2. プルリクエストのページを開き、`release-v1.0`を`base`の欄に、新たに追加した機能ブランチを`compare`の欄に入力して、新しくプルリクエストとしてオープンしてください。
3. プルリクエストのテンプレート変更内容の説明をに入力します。

### 新機能をリリースブランチにマージする
GitHubのリリース機能があったとしても、GitHub flowはチームと連携するために未だ重要な戦略です。迅速な機能の追加とバグ修正のために、生存期間の短いブランチを使用することをお勧めします。

できるだけ早くリリースのプルリクエストをオープンすることができるように、この機能プルリクエストをマージしてみましょう。

### ⌨️ Activity: プルリクエストをマージする

1.  **Merge pull request**をクリックし、ブランチを消去します。
2. 約20秒待ってから、次のステップのためにこのページを更新します。

</details>

<!--Step 3-->
<details id=3>
<summary><h2>Step 3: リリースプルリクエストをオープンする</h2></summary>

### リリースブランチと`main`ブランチ

リリースブランチと`main`ブランチ間は、できるだけ早くプルリクエストをオープンすべきです。長い期間オープンのままになるかもしれませんが、問題はありません。

一般的に、プルリクエストの説明には以下を含めることができます。
- プルリクエストに関連する[Issueへの参照](https://docs.github.com/en/articles/basic-writing-and-formatting-syntax/#mentioning-people-and-teams)
- プルリクエストで提案された変更の説明
- 提案された変更のレビューを担当する、個人やチームへの[@メンション](https://docs.github.com/en/articles/basic-writing-and-formatting-syntax/#mentioning-people-and-teams)

このプル リクエストの作成を迅速に行うために、プルリクエストのテンプレートをリポジトリに追加しました。プルリクエストを作成すると、デフォルトのテキストが自動的に表示されます。これは、必要なすべての情報を特定して入力するのに役立つでしょう。テンプレートコンテンツを使用したくない場合は、プルリクエストからテキストを削除し、望む形にプルリクエストメッセージを置き換えてください。

### :keyboard: Activity: Open a release pull request
`release-v1.0`ブランチと`main`ブランチを比較する、新しいプルリクエストを作成してみましょう。

1. 新しいブラウザタブを開き、このタブの指示を読みながら、新しく開いたタブで以下の手順を実行します。
2. `base: main` `compare: release-v1.0`として**新しいプルリクエスト**をオープンします。
3. プルリクエストのタイトルが**Release v1.0**であることを確認してください。
4. プルリクエストの詳細を本文に含めます。例を以下に示します。
    ```
    ## Description: 
    - Changed page background color to black.
    - Changed game text color to green.
    ```
5. 約20秒待ってから、次のステップのためにこのページを更新します。

</details>

<!--Step 4-->
<details id=4>
<summary><h2>Step 4: Generate release notes and merge</h2></summary>

### Automatically generated release notes
[Automatically generated release notes](https://docs.github.com/en/repositories/releasing-projects-on-github/automatically-generated-release-notes) provide an automated alternative to manually writing release notes for your GitHub releases. With automatically generated release notes, you can quickly generate an overview of the contents of a release. Automatically generated release notes include a list of merged pull requests, a list of contributors to the release, and a link to a full changelog. You can also customize your release notes once they are generated.

### :keyboard: Activity: Generate release notes

1. In a separate tab, go to the **Releases** page for this repository.
    - _Tip: To reach this page, click the **Code** tab at the top of your repository. Then, find the navigation bar below the repository description, and click the **Releases** heading link_
1. Click the **Draft a new release** button
1. In the field for _Tag version_, specify `v1.0.0`
1. To the right of the tag dropdown, click the _Target_ dropddown and select the `release-v1.0` branch
    - _Tip: This is temporary in order to generate release notes based on the changes in this branch_
1. To the top right of the description text box, click **Generate release notes**
1. Review the release notes in the text box and customize the content if desired
1. Set the _Target_ branch back to the `main`, as this is the branch you want to create your tag on once the release branch is merged
1. Click **Save draft**

You can now [merge](https://docs.github.com/en/get-started/quickstart/github-glossary#merge) your pull request!

### :keyboard: Activity: Merge into main

1. In a separate tab, go to the **Pull requests** page for this repository.
1. Open your **Release v1.0** pull request
1. Click **Merge pull request**.
1. Wait about 20 seconds then refresh this page for the next step.

</details>

<!--Step 5-->
<details id=5>
<summary><h2>Step 5: Finalize the release</h2></summary>

### Finalizing releases

It's important to be aware of the information what will be visible in that release. In the pre-release, the version and commit messages are visible.

![image](https://user-images.githubusercontent.com/13326548/47883578-bdba7780-ddea-11e8-84b8-563e12f02ca6.png)

### Semantic versioning

Semantic versioning is a formal convention for specifying compatibility. It uses a three-part version number: **major version**; **minor version**; and **patch**.  Version numbers convey meaning about the underlying code and what has been modified. For example, versioning could be handled as follows:

| Code status  | Stage  | Rule  | Example version  |
|---|---|---|---|
| First release  | New product  | Start with 1.0.0  | 1.0.0  |
| Backward compatible fix  | Patch release  | Increment the third digit  | 1.0.1  |
| Backward compatible new feature  | Minor release  | Increment the middle digit and reset the last digit to zero  | 1.1.0  |
| Breaking updates | Major release | Increment the first digit and reset the middle and last digits to zero | 2.0.0 |

Check out this article on [Semantic versioning](https://semver.org/) to learn more.

### Finalize the release

Now let's change our recently automated release from _draft_ to _latest release_.

### :keyboard: Activity: Finalize release

1. In a separate tab, go to the **Releases** page for this repository
    - To reach this page, click the **Code** tab at the top of your repository. Then, find the navigation bar below the repository description, and click the **Releases** heading link
1. Click the **Edit** button next to your draft release
1. Click the **Draft a new release** button
1. Ensure the _Target_ branch is set to `main`
1. Click **Publish release**
1. Wait about 20 seconds then refresh this page for the next step

</details>

<!--Step 6-->
<details id=6>
<summary><h2>Step 6: Commit a hotfix to the release</h2></summary>

Notice that I didn't delete the branch? That's intentional.

Sometimes mistakes can happen with releases, and we'll want to be able to correct them on the same branch.

Now that your release is finalized, we have a confession to make. Somewhere in our recent update, I made a mistake and introduced a bug. Instead of changing the text colors to green, we changed the whole game background.

_Tip: Sometimes GitHub Pages takes a few minutes to update. Your page might not immediately show the recent updates you've made._

![image](https://user-images.githubusercontent.com/13326548/48045461-487dd800-e145-11e8-843c-b91a82213eb8.png)

"Hotfixes", or a quick fix to address a bug in software, are a normal part of development. Oftentimes you'll see application updates whose only description is "bug fixes".

When bugs come up after you release a version, you'll need to address them.

We've already created this branch and pull request. The suggested change will be merged into the main branch. Later we will `cherry-pick` the hotfix commits into the release branch.

Submit a hotfix by approving and merging the pull request.

### :keyboard: Activity: Merge the hotfix
1. In a separate tab, go to the **Pull requests** page and view the open pull request
1. Review the changes and approve the pull request
1. Click **Merge pull request**
1. Wait about 20 seconds then refresh this page for the next step

</details>

<!--Step 7-->
<details id=7>
<summary><h2>Step 7: Create release v1.0.1</h2></summary>

### A final release

You updated the source code, but users can't readily access your most recent changes. Prepare a new release, and distribute that release to the necessary channels.

### Create release v1.0.1

With descriptive pull requests and auto generated release notes, you don't have to spend a lot of time working on your release draft. Follow the steps below to create your new release, generate the release notes, and publish.

### :keyboard: Activity: Complete release

1. In a separate tab, go to to the **Releases** page for this repository
    - _Tip: To reach this page, click the **Code** tab at the top of your repository. Then, find the navigation bar below the repository description, and click the **Releases** heading link_
1. Click the **Draft a new release** button
1. Set the _Target_ branch to `main`
    - _Tip: Practice your semantic version syntax. What should the tag and title for this release be?_
1. To the top right of the description text box, click **Generate release notes**
1. Review the release notes in the text box and customize the content if desired
1. Click **Publish release**
1. Wait about 20 seconds then refresh this page for the next step

</details>

<details id=x>
<summary><h2>Finish</h2></summary>

### Congratulations friend, you've completed this course!

Here's a recap of all the tasks you've accomplished in your repository:

- Create a beta release.
- Add a new feature to the release branche.
- Open a release pull request
- Automate release notes.
- Merge and finalize the release branch.
- Commit a hotfix to the release.
- Create release v1.0.1.

### What's next?

- [We'd love to hear what you thought of this course](TBD-feedback-link).
- [Take another GitHub Skills course](https://github.com/skills).
- [Read the GitHub Getting Started docs](https://docs.github.com/en/get-started).
- To find projects to contribute to, check out [GitHub Explore](https://github.com/explore).

</details>

---

Get help: [Post in our discussion board](https://github.com/skills/.github/discussions) • [Review the GitHub status page](https://www.githubstatus.com/)

© 2022 GitHub • [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) • [CC-BY-4.0 License](https://creativecommons.org/licenses/by/4.0/legalcode)
