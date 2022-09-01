# RoK_OCR_TOTALPOWER

## 概要

ゲーム【Rise of Kingdom】の同盟戦力を計算するプログラムです．  
各王国幹部のKvK前の戦力調整の手間が減ることを祈って．  

## 準備
  * google colaboratory (Jupytor Notebook)
  * 王国戦力ランキングのスクリーンショット
  * やる気

## 使用方法

### 1. スクリーンショットをアップロードする  
スクリーンショットの保存場所は`/content/original`をデフォルトに設定しています．  
必要に応じて作成/変更してください.  
トリミング後の画像を保存するディレクトリも必要に応じて変更してください．  
アップロードは画面左のファイルマークから行えます．

### 2. スプレッドシートの作成場所を指定する  
新規で作成するようにしていますが，必要に応じて既存のスプレッドシートに追加することも可能です．  
詳しくはgoogle.colabライブラリをググってください．

### 3. トリミング後の画像の確認をする  
トリミングに関しては各自の使用する画像によって異なります．  
コード内ではiPadで撮ったスクリーンショットを基準にしています．  
必要に応じて2つ目のコードセル内の下記の値を変更してください．　　
      
   ```
     # トリミングする左上の座標
     left, top = 1650, 550
     # トリミングする右上の座標
     right, bottom = 1850, 1400
   ```
      
### 4. 実行
Tesseractのlayoutの値は6になっています．  
langについては，
"eng"を使用すると1と7の誤認識が発生したため"jpn"を使用しています．

### 5. OCRによる誤認識を訂正する   
デフォルトでは間違えやすい1を7にする処理と，誤認識があったときに前後の戦力の平均を代入する処理がされます．  
お好みで処理を変えてください．  

### 6. スプレッドシートの確認
各自の責任で確認してください．

## 注意事項

  * OCRは完璧ではありません．
  
  * 誤認識が起こる前提で使用ください．
  
  * 誤認識を修正する際に前後の戦力の平均を使っているように，計算された総合戦力は概算になります．
