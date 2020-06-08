�ychart.js�ɂ��āz
https://www.webprofessional.jp/introduction-chart-js-2-0-six-examples/
�������Y��ł킩��₷���B

��{�I��chart�̍\���͈ȉ�

�@type
  �\��������}�̌`���A

�Alabel
  �e�l�̃��x��

�Bdata
  �e�l

�CbackgroundColor
  �w�i
  borderColor
  �g�F

�Doption
 �^�C�g���A�h�[�i�c�O���t�̌��AonClick�̗l�ȃC�x���g�@�\��ǉ��ł���B

�f�[�^�̌`���͓�ʂ肠��A
�y�v�f���ɃR���N�V�����`���œ��͂�����@�z�A�y�e�l���ɓ��͂�����@�z������B
�l�I�ɂ͑O�҂̕������₷�����A�v�f������������Ɖǐ��������Ȃ�B
�f�[�^�����ږ����A�f�[�^��ʖ��ǂ���̂ق����g���₷�������f���Ďg���Ɨǂ��Ǝv����B

���ǋL
�@�f�[�^�̌`���������̂ł͂Ȃ��A1�n��2�n�Ńf�[�^�̓��͕������ς�����݂����B
�@2���O��
�@
�y�v�f���ɃR���N�V�����`���œ��͂�����@�z
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.1.4/Chart.min.js"></script>
<canvas id="myChart" width="400" height="400"></canvas>
<script>
var ctx = document.getElementById("myChart").getContext('2d');
var myChart = new Chart(ctx, {
    type: 'bar',
    data: {
        labels: ["��", "��", "���F", "��", "��", "��"],
        datasets: [{
            label: '���[��',
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