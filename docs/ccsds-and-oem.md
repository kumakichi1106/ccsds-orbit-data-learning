## CCSDSとは何か

CCSDS（Consultative Committee for Space Data Systems）は、宇宙データシステムに関する国際標準化や推奨規格を検討・策定する委員会。

CCSDSが作成する推奨規格には、拘束力があるわけではない。

---

## CCSDSは何を目的としているのか

主な目的は、宇宙活動における組織間の相互運用性を高めること。

複数の宇宙機関などが共通に利用できる規格を整備することで、異なる組織間でもデータやシステムを連携しやすくすることを目指している。

---

## OEMとは何か

OEM（Orbit Ephemeris Message）は、宇宙機の軌道情報をやり取りするためのメッセージ形式。

CCSDSのODM（Orbit Data Messages）という推奨規格の中で定義されている。

---

## CCSDSとOEMの関係

- **CCSDS**：宇宙データシステムの国際標準化・推奨規格を検討する組織
- **ODM**：CCSDSが定める軌道情報交換の推奨規格
- **OEM**：ODMで定義されているメッセージ形式の一つ

---

## OEMにはどのような情報が含まれているのか

- 宇宙機名・Object ID
- 時刻（Epoch / Time System）
- 座標系（Reference Frame）
- 位置（X / Y / Z）
- 速度（Vx / Vy / Vz）
- 加速度（任意）
- 共分散情報（任意）
- 補間方法

時刻ごとの位置・速度などの状態ベクトルを並べ、宇宙機の軌道暦を表現できる。

---

## TLEとOEMにはどのような違いがあるのか

| TLE | OEM |
|---|---|
| ある時点の平均軌道要素を表す | 時刻付きの位置・速度などの状態ベクトルを扱う |
| 軌道要素からSGP4などの対応するモデルで軌道を伝播する | 複数時刻の状態ベクトルを扱える |
| 固定幅の2行形式 | KVN / XML |
| 傾斜角、離心率、平均近点角、平均運動などを持つ | 位置、速度、時刻、座標系などを持つ |

※間違っている可能性があるので要精査

---

## 疑問
- TLEとOEMの精度は何によって決まるのか。
- TLEを高頻度で取得した場合、OEMとの差は縮まるのか。
- 実際の衛星運用では、TLEとOEMをどのように使い分けるのか。
- ODMにはOEM以外にOPM・OMM・OCMがある。それぞれ何を表していて、どのような用途で使うのか。

---

## 参考にした情報

1. **JAXA CCSDSサイト**
   https://stage.tksc.jaxa.jp/ccsds/index.html

2. **JAXA「CCSDSの概要」**
   https://stage.tksc.jaxa.jp/ccsds/ccsds/ccsds.html

3. **CCSDS公式**
   https://ccsds.org/about/faqs/
  
4. **JAXA「CCSDS Blue Books（CCSDS 502.0-B-3）」**
   https://stage.tksc.jaxa.jp/ccsds/docs/doc_blue.html

5. **CCSDS公式「Orbit Data Messages（CCSDS 502.0-B-3）」**
   https://ccsds.org/publications/bluebooks/

6. **Space-Track.org**
   https://www.space-track.org/documentation
