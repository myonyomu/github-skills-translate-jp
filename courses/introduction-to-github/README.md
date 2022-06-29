<!-- 
  <<< Author notes: Header of the course >>> 
  Include a 1280×640 image, course title in sentence case, and a concise description in emphasis.
  In your repository settings: enable template repository, add your 1280×640 social image, auto delete head branches.
  Add your open source license, GitHub uses Creative Commons Attribution 4.0 International.
-->

# Introduction to GitHub

_1時間でGitHubを始めてみよう。_

<!-- 
  <<< Author notes: Start of the course >>> 
  Include start button, a note about Actions minutes,
  and tell the learner why they should take the course.
  Each step should be wrapped in <details>/<summary>, with an `id` set.
  The start <details> should have `open` as well.
  Do not use quotes on the <details> tag attributes.
-->

<!-- step0 -->

人々はGitHubを使用して、世界でも最先端なテクノロジーをいくつも構築しています。GitHubには、データ視覚化や新しいゲームの作成などに関する様々なコミュニティと一連のツールがあり、改善の役に立ちます。GitHub Skillsの「Introduction to GitHub」コースでは、1時間以内にコントリビューションを始めるために必要なすべてのことをガイドします。

- **対象者** ：新規開発者、新たなGitHubユーザー、学生。
- **学習内容**：リポジトリ、ブランチ、コミット、プルリクエストを紹介します。
- **作成するもの**：[Profile README](https://docs.github.com/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/managing-your-profile-readme)として使用できる短いMarkdownファイルを作成します。
- **前提条件**：なし。このコースは、GitHubを開始する際の素晴らしい入門ドキュメントです。
- **所要時間**：このコースの長さは4ステップで、完了までに1時間もかかりません。

**※訳者注** コントリビューション(Contribution): 日本語直訳で「貢献」。GitHub上では、コードのコミットやマージ、ドキュメントやイシューの追加や編纂など、GitHub上で行われる活動全般を指す。

## このコースの開始方法

1. このイントロダクションの上部にある、**Use this template**ボタンを右クリックし、新しいタブでリンクを開きます。
   ![Use this template](https://user-images.githubusercontent.com/1221423/169618716-fb17528d-f332-4fc5-a11a-eaa23562665e.png)
2. 新しく開いたタブで、手順に従って新しいリポジトリを作成します。
   - あなたがOrganizationアカウントのOwnerの場合、リポジトリをホストする個人アカウントまたは組織を選択します。
   - パブリックリポジトリを作成することをお勧めします。――プライベートリポジトリの場合、[アクションにかかった時間分だけ請求が発生します](https://docs.github.com/en/billing/managing-billing-for-github-actions/about-billing-for-github-actions)。
3. 新しいリポジトリが作成されたら、約20秒待ってから、ページを更新します。新しいリポジトリのREADMEにある手順に従って操作を行ってください。

<!-- end step0 -->

<!-- 
  <<< Author notes: Step 1 >>> 
  Choose 3-5 steps for your course.
  The first step is always the hardest, so pick something easy!
  Link to docs.github.com for further explanations.
  Encourage users to open new tabs for steps!
-->

<details id=1>
<summary><h2>Step 1: ブランチを作成する</h2></summary>

_「Introduction to GitHub」へようこそ! 👋_

**GitHubとは？**: GitHubは、バージョン管理に[Git](https://docs.github.com/get-started/quickstart/github-glossary#git)を使用するコラボレーションプラットフォームです。GitHubは、[オープンソース](https://docs.github.com/get-started/quickstart/github-glossary#open-source)ソフトウェアを共有して貢献するための人気のある場所です。
<br>📺 ビデオ：[GitHubとは？(What is GitHub?)](https://www.youtube.com/watch?v=w3jLJU7DT5E)

**リポジトリ(repository)とは？**: [リポジトリ](https://docs.github.com/get-started/quickstart/github-glossary#repository)は、ファイルとフォルダを含むプロジェクトです。リポジトリは、ファイルとフォルダのバージョンを追跡します。
<br>📺 ビデオ：[リポジトリの探索](https://www.youtube.com/watch?v=R8OAwrcMlRw)

**ブランチ(branch)とは?**: [ブランチ](https://docs.github.com/en/get-started/quickstart/github-glossary#branch)は、リポジトリの並列バージョンです。デフォルトでは、リポジトリには`main`という名前が付けられたブランチが1つあり、それが最も信頼のおけるブランチと見なされます。リポジトリ内では、`main`のブランチから追加のブランチを作成できます。ブランチを使用して、プロジェクトのさまざまなバージョンを一度に作成できます。

追加されたブランチでは、`main`バージョンに影響を与えることなく編集を行うことができます。ブランチを使用すると、作業を`main`ブランチから分離できます。言い換えれば、あなたが貢献している間も、他の皆は安全に仕事をすることが可能です。
<br>📺 ビデオ：[ブランチ](https://www.youtube.com/watch?v=xgQmu81G1yY)

**プロファイルREADME(profile README)とは?**: [プロファイルREADME](https://docs.github.com/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/managing-your-profile-readme)は、基本的にGitHubプロファイルの「自己紹介」セクションであり、GitHub.comのコミュニティと自分に関する情報を共有できます。GitHubは、プロファイルページの上部にプロファイルREADMEを表示します。

### ⌨️ Activity: はじめてのブランチ
1. 新しいブラウザタブを開き、今開かれているこのリポジトリのページに移動します。次に、手順を読みながら、新しく開いたブラウザタブで、2番以降の手順に取り組みます。
2. **Code**タブに移動します。
3. `main`ブランチのドロップダウンをクリックします。
   ![image showing my-first-branch entry](/images/my-first-branch.png)
4. 入力欄にブランチの名前を入力します。ブランチ名は`my-first-branch`としてください。
5. **Create branch: my-first-branch**をクリックして、ブランチを作成します。
6. Step 2に進んでください！<br>
   **注**：パブリックリポジトリを作成し、最初のブランチが正しく設定されていることを確認したい場合は、約20秒待ってから、このページ（新しく開いたブラウザのタブ）を更新してください。[GitHub Actions](https://docs.github.com/en/actions)によって、このステップは自動的に閉じられ、次のステップが開かれます。
</details>

<!-- 
  <<< Author notes: Step 2 >>>
  Start this step by acknowledging the previous step.
  Define terms and link to docs.github.com.
-->

<details id=2>
<summary><h2>Step 2: ファイルをコミットする</h2></summary>

_おみごと！ブランチを作成することができました! 🎉_

ブランチを作成すると、`main`ブランチを変更せずにプロジェクトを編集できます。ブランチができたので、ファイルを作成して最初のコミットを行います。

**コミット(commit)とは？**：[コミット](https://docs.github.com/pull-requests/committing-changes-to-your-project/creating-and-editing-commits/about-commits)は、プロジェクト内のファイルとフォルダーに対する一連の変更です。コミットはブランチ内に存在します。

### ⌨️ Activity: はじめてのコミット

次の手順では、GitHubで変更をコミットする手順を案内します。変更をコミットするには、まず新しいブランチに新しいファイルを追加する必要があります。

1. **Code**タブで、新しく作成したブランチである`my-first-branch`にいることを確認します。
2. **Add file**ドロップダウンを選択し、**Create new file**をクリックします。<br>
  ![create new file option](/images/create-new-file.png)
3. **Name your file...** と書いてある入力欄にと`PROFILE.md`入力します。
4. **Edit new file**と書いてあるタブのテキストエリアに、以下の内容をコピーします。
   ```
   Welcome to my GitHub profile!
   ```
   ![profile.md file screenshot](/images/my-profile-file.png)
5. コミットを行う際には、行った変更を説明する短いコミットメッセージを入力できます。これは、他の人があなたのコミットに何が含まれているかを知るのに役立ちます。GitHubは単純なデフォルトのメッセージを提供しますが、練習のために少し変更してみましょう。**Commit new file**のすぐ下のテキスト入力フィールドに、`Add PROFILE.md`と入力します。どこに何を入力すべきかを確認する場合は、下のドロップダウンを展開してください。
   <details>
   <summary> スクリーンショットを確認するには、このドロップダウンを展開してください。</summary>

     ![screenshot of adding a new file with a commit message](/images/commit-full-screen.png)

   </details>
6. このレッスンでは、他のフィールドを無視して、**Commit new file**をクリックします。
7. Step 3へ進んでください!<br>
   **注**： 以前と同様に、約20秒待ってから、このページ（新しく開いたブラウザのタブ）を更新すると、[GitHub Actions](https://docs.github.com/en/actions)によってこのステップが自動的に閉じられ、次のステップが開きます。
</details>

<!-- 
  <<< Author notes: Step 3 >>> 
  Just a historic note: the previous version of this step forced the learner
  to write a pull request description,
  checked that `main` was the receiving branch,
  and that the file was named correctly.
-->

<details id=3>
<summary><h2>Step 3: プルリクエストをする</h2></summary>

_コミットを作成するという偉業を成し遂げました！✨_

コミットを作成したら、次はプルリクエストを介して変更案を共有してみましょう！

**プルリクエスト(pull request)とは?**: コラボレーションはプルリクエストで発生します。プルリクエストは、ブランチ内の変更を他の人に表示します。このプルリクエストは、ブランチで行った変更を保持したまま、それらを`main`ブランチに適用することを提案します。<br>
📺 [ビデオ: プルリクエストの概要](https://youtu.be/kJr-PIfLDl4)

### ⌨️ Activity: プルリクエストを作ろう
コミットを行った後に、新しくブランチへのプッシュがあったメッセージとともに、**Compare & pull request**ボタンが表示されていることに気付いたかもしれません。

![screenshot of message and button](/images/compare-and-pull-request.png)

必要に応じて、**Compare & pull request**をクリックしてから、以下の手順6に進んでください。ボタンをクリックしない場合は、以下の手順でプルリクエストを手動で設定する手順を説明します。

1. リポジトリの**Pull requests**タブをクリックします。 
2. **New pull request**をクリックします。
3. **base**ドロップダウンで、`main`が選択されていることを確認します。
4. **compare**ドロップダウンを選択し、`my-first-branch`をクリックします。<br>
5. [プルリクエストの作成]をクリックします。
6. プルリクエストにタイトルを入力してください： `Add my first file`.
7. 次のフィールドは、行った変更の説明を提供するのに役立ちます。これまでに達成したことの説明を自由に追加してください。念のためお伝えしておくと、これまでにブランチを作成し、ファイルを作成し、コミットを行いました。<br>
   ![screenshot showing pull request](/images/Pull-request-description.png)
8. **Create pull request**をクリックします。
9. Step 4へ進んでください! <br>
   **注**: 以前と同様に、約20秒待ってから、このページ（指示に従っているページ）を更新すると、[GitHub Actions](https://docs.github.com/en/actions)によってこのステップが自動的に閉じられ、次のステップが開きます。結果として、プルリクエストを作成したタブでGitHub Actionsが実行されている様子を確認することができるかもしれません。以下の画像は、アクションの実行が終了した後にプルリクエストに表示される可能性のある行を示しています。<br>
   ![screenshot of an example of an actions line](/images/Actions-to-step-4.png)
</details>

<!-- 
  <<< Author notes: Step 4 >>> 
  Just a historic note: The previous version of this step required responding
  to a pull request review before merging. The previous version also handled
  if users accidentally closed without merging.
-->

<details id=4>
<summary><h2>Step 4: プルリクエストをマージする</h2></summary>

_素晴らしい出来栄えです! 😎_

プルリクエストが正常に作成されました。これで、プルリクエストをマージすることができます。

**マージ(merge)とは?**：[マージ](https://docs.github.com/en/get-started/quickstart/github-glossary#merge)は、プルリクエストとブランチの変更を`main`ブランチに追加します。
📺 [ビデオ：GitHub flowを理解する](https://www.youtube.com/watch?v=PBI2Rz-ZOxU)

前のステップで述べたような、進行状況が自動的に次のステップに進むアクションが実行されているメッセージは確認できているでしょうか？プルリクエストをマージする前に、それが完了するのを待つ必要があります。**Merge pull request**ボタンが緑色になっていれば、準備が完了している常態です。

![screenshot of green merge pull request button](/images/Green-merge-pull-request.png)
### ⌨️ Activity: プルリクエストをマージしてみよう

1. **Merge pull request**をクリックします。
2. **Confirm merge**をクリックします。
3. ブランチがマージされたら、もうこのブランチは必要ありません。ブランチを削除するには、**Delete branch**をクリックします。<br>
   ![screenshot showing delete branch button](/images/delete-branch.png)
4. **Finish**ステップをチェックして、次に何を学ぶことができるかを確認してください。<br>
   **注**：以前と同様に、約20秒待ってから、このページ（指示に従っているページ）を更新すると、[GitHub Actions](https://docs.github.com/en/actions)によってこのステップが自動的に閉じられ、次のステップが開きます。
</details>

<!-- 
  <<< Author notes: Finish >>> 
  Review what we learned, ask for feedback, provide next steps.
-->

<details id=X>
<summary><h2>Finish</h2></summary>

_おめでとうございます。このコースを修了し、開発者の世界に入門しました!_

<img src=https://octodex.github.com/images/collabocats.jpg alt=celebrate width=300 align=right>

以下があなたの業績です。
- GitHub、リポジトリ、ブランチ、コミット、プルリクエストについて学びました。
- ブランチ、コミット、およびプルリクエストを作成しました。
- プルリクエストをマージしました。
- はじめてのコントリビューションを行いました！🎉

### 次は何をする?
プロファイルのREADMEを作成する場合は、以下の簡単な手順を使用するか、[プロファイルのREADMEの管理](https://docs.github.com/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/managing-your-profile-readme)に関する記事の手順に従ってください。

1. GitHubユーザー名と一致する名前で新しいパブリックリポジトリを作成します。
2. 1で作成したリポジトリのルートで、`README.md`と名付けられたファイルを作成します。「ルート」とは、リポジトリ内のどんなフォルダ内にもないことを意味します。
3. `README.md`ファイルの内容を編集します。
4. ファイル用に新しいブランチを作成した場合は、ブランチでプルリクエストを作成してマージします。
5. 私たちはあなたの新しいプロフィールを見てみたいです！ソーシャルメディアであなたのプロフィールとタグをつけて私たちに共有してください！
6. 最後に、[ディスカッションボード](https://github.com/skills/.github/discussions)でこのコースについてのご意見をお聞かせください。

詳細を確認したり、参加したりするには、次のリソースを確認してください:
- あなたは学生ですか？もしそうなら、[Student Developer Pack](https://education.github.com/pack)をチェックしてください。
- [別のGitHubスキルコースを受講してください。](https://github.com/skills)
- [GitHub入門ドキュメントをお読みください。](https://docs.github.com/en/get-started)
- コントリビュートを行うプロジェクトを見つけるには、[GitHub Explore](https://github.com/explore)をチェックしてください。

</details>

<!--
  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---

ヘルプが欲しいときには: [ディスカッションボード](https://github.com/skills/.github/discussions)に投稿する。 &bull; [GitHub status pageを確認する](https://www.githubstatus.com/)

&copy; 2022 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [CC-BY-4.0 License](https://creativecommons.org/licenses/by/4.0/legalcode)
