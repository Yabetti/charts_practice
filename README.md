【chart.jsについて】
https://www.webprofessional.jp/introduction-chart-js-2-0-six-examples/
ここが綺麗でわかりやすい。

基本的なchartの構成は以下

①type
  表示させる図の形式、

②label
  各値のラベル

③data
  各値

④backgroundColor
  背景
  borderColor
  枠色

⑤option
 タイトル、ドーナツグラフの穴、onClickの様なイベント機能を追加できる。

データの形式は二通りあり、
【要素毎にコレクション形式で入力する方法】、【各値毎に入力する方法】がある。
個人的には前者の方が見やすいが、要素数が多すぎると可読性が悪くなる。
データが項目毎か、データ種別毎どちらのほうが使いやすいか判断して使うと良いと思われる。

※追記
　データの形式が二つあるのではなく、1系と2系でデータの入力方式が変わったみたい。
　2が前者
　
【要素毎にコレクション形式で入力する方法】
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.1.4/Chart.min.js"></script>
<canvas id="myChart" width="400" height="400"></canvas>
<script>
var ctx = document.getElementById("myChart").getContext('2d');
var myChart = new Chart(ctx, {
    type: 'bar',
    data: {
        labels: ["赤", "青", "黄色", "緑", "紫", "橙"],
        datasets: [{
            label: '得票数',
            data: [12, 19, 3, 5, 2, 3],
            backgroundColor: [
                'rgba(255, 99, 132, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
                'rgba(153, 102, 255, 0.2)',
                'rgba(255, 159, 64, 0.2)'
            ],
            borderColor: [
                'rgba(255,99,132,1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
            ],
            borderWidth: 1
        }]
    },
    options: {
        scales: {
            yAxes: [{
                ticks: {
                    beginAtZero:true
                }
            }]
        }
    }
});
</script>