# BERT関連
 - [x] **GraphBERT: Bridging Graph and Text for Malicious Behavior Detection on Social Media(2022ICDM)**  
   [[link]](https://ieeexplore.ieee.org/document/10027673)
GNNとBERTを組み合わせて，悪質ツイートの検出
   <details><summary>概要</summary><div>
   ツイートの情報(ハッシュタグやエンティティなど)を，ツイートノードと情報ノードでエッジを形成し異種グラフで表現．これでグラフベースの関係情報を得る．この情報とBERTを組み合わせて悪質ツイート，ユーザの分類を行う．BERT単体，またはBERT+CNN や BERT+LSTMの手法よりも良い結果に．つまり，GNNから有用な構造情報を取得できているということに
---
- [x] **COVID-19 patients classification using Graph neural network on a Heterogeneous graph(2020ICCC)**  
   [[link]](https://www.dbpia.co.kr/journal/articleDetail?nodeId=NODE10506109)
   [[github link]](https://github.com/KienMN/COVID-19-in-Korea-graph)
   異種グラフを用いてコロナ患者の分類を行う．
   <details><summary>概要</summary><div>
   コロナ患者と，患者の住む市，市のある県などをノードとして異種グラフを作成．GNNより患者の感染症例を分類．複雑なアプローチを施したが結果は改善されず．つまり，今回作成した異種グラフではニューラルネットワークの学習が困難だった．原因としてはクラスの不均衡さ，不十分な特徴量が考えられる．感染者の居住地情報が感染症例の分類に役立つと考えていたが，その情報のみでは不十分だった模様．データセットの改善や強力なGNNが解決策となると考えられる．
---
- [x] **Understanding Political Polarization via Jointly Modeling Users, Connections and Multimodal Contents on Heterogeneous Graphs(2022ACM)**  
   [[link]](https://dl.acm.org/doi/abs/10.1145/3503161.3547898)
   異種グラフからユーザ埋め込みを学習し，政治的な意見を検出．
   <details><summary>概要</summary><div>
    最終的にはその結果から政治的偏向の理解を深めることが目的.コンテンツ(ツイート)のみでなく，ユーザとツイートがエッジで結ばれた異種グラフを作成．ユーザノードの初期特徴量はフォローフォロワー数やプロフィール文，ツイートノードはテキスト情報と投稿したユーザ情報から算出．この異種グラフにGNNを適用し政治的偏向の理解に有効なembeddingを得る．同種のGNNフレームワークを凌駕する精度でユーザー埋め込みを学習．
---
- [x] **CSI: A Hybrid Deep Model for Fake News Detection(2017ACM)**  
   [[link]](https://arxiv.org/abs/1703.06959)
   フェイクニュース検出
   <details><summary>概要</summary><div>
    フェイクニュースの自動検出の際に，Capture，Score，Integrateという3つのモジュールからモデルを提案する．Captureは，RNNを用いてニュース記事に対するユーザの時間的表現を取得，Scoreはユーザの行動に基づいてスコアを学習し，Integrateはこの2つのモジュールの統合を行い，出力で記事がFakeかどうかを判断．ユーザの特徴量は，ユーザについては，どの記事に関与したかに着目していた
---
# GNN関連
- [x] **An Analysis of French-Language Tweets About COVID-19 Vaccines: Supervised Learning Approach(2022JMIR)**  
   [[link]](https://medinform.jmir.org/2022/5/e37831)
   BERTを用いてワクチンツイートの分類ができるか検証．
   <details><summary>概要</summary><div>
    ワクチン関連のツイートの特徴として，賛成反対いがいにも，曖昧，皮肉，無関係といったツイートが多くありこれらもうまく分類できるかどうかを検証．CamemBERT というフランス語BERTモデルを微調整して使用．ツイートは，(1) 賛成 反対 中立， (2) コンテンツの種類 (科学的，政治的，社会的，またはワクチン接種の状況) に分類．(1)の分類は困難，(2)の分類は(1)よりかは高いがまずまずの結果に．そこで，ツイート本文が170文字以上のものに限定して再度実験を行うと，結果が改善された．コメント：ツイートのラベル参考になりそう．ちなみにラベル付けは手動で行っていた．
---
- [x] **Prediction of COVID-19 tweeting: classification based on graph neural networks(2022MIPRO)**  
   [[link]](https://ieeexplore.ieee.org/abstract/document/9803426)
   GNNに基づく新型コロナウイルス感染症ツイート予測
   <details><summary>概要</summary><div>
    あるユーザが，今後コロナ関連のツイートをするかどうかを予測するモデルを構築．特に，node2vecを使用し，ユーザのフォロワーネットワークから抽出された特性のベクトルとしてユーザをモデル化している．
---
- [x] **Graph Contrastive Learning with Augmentations(2020NeurIPS)**  
   [[link]](https://arxiv.org/abs/2010.13902)
   GNNの対照学習
   <details><summary>概要</summary><div>
    対照学習の概念をGNNに適用．Graph Contrastive Learning（GCL）としている．グラフにおける不変表現の学習を促進させることが目的であり，実験により汎化性と頑健性が示された．拡張に関してはノードやエッジの削除，追加などが挙げられており，もう少し検討が必要な模様
---
- [x] **Local discriminative graph convolutional networks for text classification(2023   )**  
   [[link]](https://link.springer.com/article/10.1007/s00530-023-01112-y)
   GNN 局所的大域的の両方から学習を行う
   <details><summary>概要</summary><div>
    従来のテキスト分類GNNの問題点として，正解ラベルと予測ラベルの適合度にのみ着目している点が挙げられる．つまり，グラフが暗黙的に符号化する局所的なクラス内多様性と局所的なクラス間類似性を無視しているといえる．テキスト分類の精度をより向上させるためには，クラス内とクラス間の両方の多様体構造を考慮することが重要となっている．そこで本論文では局所識別グラフ畳み込みネットワーク(LDGCN)を提案する．テキストデータの局所クラス間散布行列と局所クラス内散布行列を構築し，新しいLDGCNの特徴空間では，同じクラスのテキストは互いに密接にマッピングされ，異なるクラスのテキストはできるだけ離れてマッピングされるよう学習を行う．
---
- [x] **Detecting Political Opinions in Tweets through Bipartite Graph Analysis: A Skip Aggregation Graph Convolution Approach(2023   )**  
   [[link]](https://arxiv.org/abs/2304.11367)
   ツイートとユーザをノードとすグラフにGNNを適用する際，スキップ集約メカニズムを用いてユーザ特徴量問題を解消する
   <details><summary>概要</summary><div>
    ツイート中の政治的意見を検出するために，ユーザーの投稿とリツイートの行動に基づいてユーザーとツイートの二部グラフを構築し，GNNベースのノード分類問題に変換する．GNNを適用する際，ツイート表現を学習するために，新しいスキップ集約メカニズムを提案する．グラフを構築する際，ツイートノードはBERTを用いて初期特徴量を設定することができるが，ユーザノードはテキストではないため初期特徴量を設定することができない．そこで，ツイート表現を学習する際に2近傍先のノード，つまりユーザノードをスキップしたツイートノードの特徴量から学習を行うことで，先ほどの問題を解決する．
---
- [x] **A Heterogeneous Information Network based Cross Domain Insurance Recommendation System for Cold Start Users(2020SIGIR)**  
   [[link]](https://arxiv.org/abs/2007.15293)
   異種ネットワークの情報集約
   <details><summary>概要</summary><div>
    ユーザへの保険推薦のための，異種情報ネットワークに基づくクロスドメイン推薦．
    推薦のために，3つのレベル（関係，ノード，意味）の注意集約(attention aggregation)を採用し，ユーザーと保険商品の表現を得る．具体的には，まず1ホップ異種隣接を集約するための関係的注意を提案する．これは，異なる1ホップ近傍間で同じ集計関数を使用するのではなく，関係の種類ごとに特定の集計関数を学習する．次にメタパスに基づく隣接を集約するためのノード注意，メタパスに基づく隣接集合を集約するための意味的注意を提案する．(メタパスが異なれば，意味も異なるという考えに基づき，メタパスにに基づく隣接の定義を与えている)最後に，関係的注意の集約と意味的注意の集約の結果を元のノード埋め込みに集約し，ノード表現を更新する．
---
# その他手法
- [x] **Heterogeneous Graph Attention Network(2019WWW)**  
   [[link]](https://arxiv.org/abs/1903.07293)
   異種グラフにおけるAttentionを用いた学習
   <details><summary>概要</summary><div>
   ノードとそのメタパスに基づく隣接ノードとの間の重要度を学習する「ノードレベルAttention」と，異なるメタパスの重要度を学習する「セマンティックレベルAttention」が存在する．ノードレベルAttentionでは，各メタパスごと(どのノードを基準に近傍を考えるか)の近傍ノードから，重要なノードを決定，つまり，(1)Aベースにおける近傍ノードのうち重要なもの(2)Dベースにおける近傍ノードのうち重要なものを決定する．そしてそれらの重要性を考慮して，ソースノードに情報を集約させる．「セマンティックレベルAttention」では，「ノードレベルAttention」で得られた各メタパスごとの重要ノードを考慮したソースノードのうち，それぞれのメタパスの重要性を決定する．以上のプロセスで，異種グラフの学習を行う．
---
- [x] **Heterogeneous Graph Transformer(2022WWW)**  
   [[link]](https://arxiv.org/abs/2003.01332)
   異種グラフにおけるTransformerのアーキテクチャを参考にした学習
   <details><summary>概要</summary><div>
   異種グラフにおける学習において，Attentionを計算する際にTransformerのアーキテクチャを用いて異種グラフの各メタパス情報を考慮した学習を行う．具体的には，同種GNNであるGATにおけるAttentionを計算する際，Transformerのアーキテクチャを参考に各ソースノード，ターゲットノードの種類ごとに固有の表現空間に，Query,Keyとしてマッピングする．そして，GATにおけるMessageを計算する際，ターゲットノードの種類ごとに固有の表現空間に，Vakueとしてマッピングする．そうすることで，異種グラフにおける各メタパスごとに固有の表現空間を保持する．
---
- [x] **Heterogeneous Graph Transformer(2022WWW)**  
   [[link]](https://arxiv.org/abs/2003.01332)
   異種グラフにおけるTransformerのアーキテクチャを参考にした学習
   <details><summary>概要</summary><div>
   異種グラフにおける学習において，Attentionを計算する際にTransformerのアーキテクチャを用いて異種グラフの各メタパス情報を考慮した学習を行う．具体的には，同種GNNであるGATにおけるAttentionを計算する際，Transformerのアーキテクチャを参考に各ソースノード，ターゲットノードの種類ごとに固有の表現空間に，Query,Keyとしてマッピングする．そして，GATにおけるMessageを計算する際，ターゲットノードの種類ごとに固有の表現空間に，Vakueとしてマッピングする．そうすることで，異種グラフにおける各メタパスごとに固有の表現空間を保持する．


