# 論文メモ
 
 - [x] **GraphBERT: Bridging Graph and Text for Malicious Behavior Detection on Social Media(2022ICDM)**  
   [[link]](https://ieeexplore.ieee.org/document/10027673)
   ツイートの情報(ハッシュタグやエンティティなど)を，ツイートノードと情報ノードでエッジを形成し異種グラフで表現．これでグラフベースの関係情報を得る．この情報とBERTを組み合わせて悪質ツイート，ユーザの分類を行う．BERT単体，またはBERT+CNN や BERT+LSTMの手法よりも良い結果に．つまり，GNNから有用な構造情報を取得できているということに
 ***

- [x] **COVID-19 patients classification using Graph neural network on a Heterogeneous graph(2020ICCC)**  
   [[link]](https://www.dbpia.co.kr/journal/articleDetail?nodeId=NODE10506109)
   [[github link]](https://github.com/KienMN/COVID-19-in-Korea-graph)
   コロナ患者と，患者の住む市，市のある県などをノードとして異種グラフを作成．GNNより患者の感染症例を分類．複雑なアプローチを施したが結果は改善されず．つまり，今回作成した異種グラフではニューラルネットワークの学習が困難だった．原因としてはクラスの不均衡さ，不十分な特徴量が考えられる．感染者の居住地情報が感染症例の分類に役立つと考えていたが，その情報のみでは不十分だった模様．データセットの改善や強力なGNNが解決策となると考えられる．
***

- [x] **An Analysis of French-Language Tweets About COVID-19 Vaccines: Supervised Learning Approach(2022JMIR)**  
   [[link]](https://medinform.jmir.org/2022/5/e37831)
   BERTを用いてワクチンツイートの分類ができるか検証．ワクチン関連のツイートの特徴として，賛成反対いがいにも，曖昧，皮肉，無関係といったツイートが多くありこれらもうまく分類できるかどうかを検証．CamemBERT というフランス語BERTモデルを微調整して使用．ツイートは，(1) 賛成 反対 中立， (2) コンテンツの種類 (科学的，政治的，社会的，またはワクチン接種の状況) に分類．(1)の分類は困難，(2)の分類は(1)よりかは高いがまずまずの結果に．そこで，ツイート本文が170文字以上のものに限定して再度実験を行うと，結果が改善された．コメント：ツイートのラベル参考になりそう．ちなみにラベル付けは手動で行っていた．
***

- [x] **Understanding Political Polarization via Jointly Modeling Users, Connections and Multimodal Contents on Heterogeneous Graphs(2022ACM)**  
   [[link]](https://dl.acm.org/doi/abs/10.1145/3503161.3547898)
   異種グラフからユーザ埋め込みを学習し，政治的な意見を検出．最終的にはその結果から政治的偏向の理解を深めることが目的.コンテンツ(ツイート)のみでなく，ユーザとツイートがエッジで結ばれた異種グラフを作成．ユーザノードの初期特徴量はフォローフォロワー数やプロフィール文，ツイートノードはテキスト情報と投稿したユーザ情報から算出．この異種グラフにGNNを適用し政治的偏向の理解に有効なembeddingを得る．同種のGNNフレームワークを凌駕する精度でユーザー埋め込みを学習．
***
