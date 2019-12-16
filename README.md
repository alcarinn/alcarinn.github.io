

<script src="https://code.jquery.com/jquery-3.1.1.min.js"></script>

<script src="https://code.highcharts.com/highcharts.js"></script>
<script src="https://code.highcharts.com/modules/item-series.js"></script>
<script src="https://code.highcharts.com/modules/exporting.js"></script>
<script src="https://code.highcharts.com/modules/export-data.js"></script>
<script src="https://code.highcharts.com/modules/accessibility.js"></script>

<script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js" integrity="sha384-Q6E9RHvbIyZFJoft+2mJbHaEWldlvI9IOYy5n3zV9zzTtmI3UksdQRVvoxMfooAo" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js" integrity="sha384-wfSDF2E50Y2D1uUdj0O3uMBJnjuUD4Ih7YwaYd1iqfktj0Uod8GCExl3Og8ifwB6" crossorigin="anonymous"></script>
# Abstract:
In October 2019, the <b>Swiss federal elections</b> took place and led to a huge paradigm shift. Almost all the parties started talking about climate change and the two Swiss green parties increased considerably their numbers of representatives into the parliament. This phenomenon has been called the <b><i>Green Wave</i></b>, and has been designated <a href="https://www.rts.ch/info/culture/10916700-en-suisse-romande-vague-verte-choisie-comme-expression-de-l-annee.html">expression of the year</a> in Romandy. Through this data story, we aim to better understand how the different <b>Swiss political parties</b> communicate their ideas to the public, e.g., what are the keywords and topics they address the most. We concentrate on the six largest parties of the last elections and observe if there is any <b>change in their communication</b> over the years and if so, if it has a relationship with the results of the federal elections.

<div id="container" style="min-width: 310px; height: 400px; margin: auto"></div>


# Introduction:

Twitter is became a central medium of communication and is used by most of the politicians to transmit their ideas. The restriction of 280 characters by tweet forces the politicians to be succinct and to compress their ideas to keep only the essential, using often the same recurrent keywords. It provides for us a good way to grasp what topics are mainly addressed by each party and politician. Therefore, we analyze <b>163,186 tweets</b> posted by the sixth largest parties (listed below) and some of their members (selected by their <a href="https://www.tagesanzeiger.ch/sonntagszeitung/wer-hat-in-bern-am-meisten-einfluss/story/11893481">influence</a> in the parliament). We also use the archives of the Radio Television of Switzerland (<b>RTS</b>) to understand what are the principal topics discussed by the politicians over the years. Finally, we compare the changes in communications of the parties with the <b>results of the federal</b> elections using the associated datasets.

# Swiss parties you said ?

To familiarize with political parties of Switzerland, we propose first a small introduction about them, with the most used words in their tweets (members and parties tweets aggregated):

<div class="container">
    <div class="row" style="background-color: #66be29;">
        <div class="col-lg-6 col-md-6 nopadding">
            <img src="static/images/WordCloud_2_UDC_logo.png" onmouseover="this.src='static/images/UDC_logo.jpg';" onmouseout="this.src='static/images/WordCloud_2_UDC_logo.png';">
        </div>
        <div class="col-lg-6 col-md-6 nopadding" style="color: #FFFFFF;">
            <div class="boxtext">
                <h2> UDC </h2>
                The Swiss People’s party (Union Démocratique du Centre in French) is a national-conservative, <b>right-wing</b> populist party. It’s the party with the more members in the Swiss parliament. They fight
                for the preservation of Switzerland's political sovereignty (they are Eurosceptic) and are against mass immigration by making the asylum laws stricter. The party opposes governmental measures for environmental protection.
            </div>
        </div>
    </div>
</div>
<br>
<div class="container">
    <div class="row"  style="background-color: #e52935;">
        <div class="col-lg-6 col-md-6 nopadding" style="background-color: #e52935; color: #FFFFFF;">
            <div class="boxtext">
                <h2> PS </h2>
                The Social Democratic Party of Switzerland or Socialist party (Parti Socialiste Suisse in French) is a socialist, progressive and <b>Centre-left</b> party. It’s the second strongest party in Switzerland. They are in favor of strong
                public services, environmental policy with climate change mitigation and social equity in an open society. The party is against policies of economic liberalization such as deregulation and capitalism.
            </div>
        </div>

        <div class="col-lg-6 col-md-6 nopadding">
            <img src="static/images/WordCloud_2_PS_logo.png" onmouseover="this.src='static/images/PS_logo.png';" onmouseout="this.src='static/images/WordCloud_2_PS_logo.png';">
        </div>
    </div>
</div>
<br>
<div class="container">
    <div class="row" style="background-color: #375191; ">
        <div class="col-lg-6 col-md-6 nopadding">
            <img src="static/images/WordCloud_2_PLR_logo.png" onmouseover="this.src='static/images/PLR_logo.png';" onmouseout="this.src='static/images/WordCloud_2_PLR_logo.png';">
        </div>
        <div class="col-lg-6 col-md-6 nopadding" style="background-color: #375191; color: #FFFFFF;">
            <div class="boxtext">
                <h2> PLR </h2>
                The Liberals (Parti Libéral-radical in French) is a liberal and <b>right-wing</b> party. It’s the third largest party in the Swiss parliament. They call themselves the party of the economy and promote individual responsibility. The
                party believes that an open society and economic freedom are more conducive to prosperity, rather than a redistributive and regulative state.
            </div>

        </div>
    </div>
</div>
<br>
<div class="container">
    <div class="row" style="background-color: #84b414;">
        <div class="col-lg-6 col-md-6 nopadding" style="background-color: #84b414; color: #FFFFFF;">
            <div class="boxtext">

                <h2> Les VERTS </h2>
                The green Party of Switzerland (Les Verts in French) is a environmentalist, progressive and <b>left-wing</b> party. It’s the fourth-largest party in Switzerland. Their main concerns are the protection of the environment and the fight
                against climate change. The party is often allied with the Socialist Party, sharing common values such as social equity and strong public services.
            </div>
        </div>

        <div class="col-lg-6 col-md-6 nopadding">
            <img src="static/images/WordCloud_2_VERTS_logo.png" onmouseover="this.src='static/images/VERTS_logo.png';" onmouseout="this.src='static/images/WordCloud_2_VERTS_logo.png';">
        </div>
    </div>
</div>
<br>
<div class="container">
    <div class="row" style="background-color: #f6a12b;">
        <div class="col-lg-6 col-md-6 nopadding">
            <img src="static/images/WordCloud_2_PDC_logo.png" onmouseover="this.src='static/images/PDC_logo.png';" onmouseout="this.src='static/images/WordCloud_2_PDC_logo.png';">
        </div>
        <div class="col-lg-6 col-md-6 nopadding" style="background-color: #f6a12b; color: #FFFFFF;">
            <div class="boxtext">

                <h2> PDC </h2>
                The Christian Democratic People’s party of Switzerland (Parti Démocrate-Chrétien in French) is a Christian-democratic and <b>centre-right</b> party. It’s the fifth strongest party in Switzerland. They advocate moderate social
                conservatism and social market economy, balance between economic liberalism and social justice. They consider themselves as the link between the left and the right wing.
            </div>
        </div>

    </div>
</div>
<br>
<div class="container">
    <div class="row"  style="background-color: #1a1915;">
        <div class="col-lg-6 col-md-6 nopadding" style="background-color: #1a1915; color: #a5c840;">
            <div class="boxtext">
                <h2> PVL </h2>
                The Green Liberal Party of Switzerland (Parti Vert’Libéral in French) is a <b>centre-right</b>, green-liberal party in Switzerland. It’s the youngest and the sixth strongest party in Switzerland. They seek to combine moderate economic
                liberalism with environmental sustainability. The party promotes economic growth, but with the preservation of the environment. They encourage sustainable energy.
            </div>
        </div>
        <div class="col-lg-6 col-md-6 nopadding">
            <img src="static/images/WordCloud_2_VERTS_LIB_logo.png" onmouseover="this.src='static/images/VERTS_LIB_logo.jpg';" onmouseout="this.src='static/images/WordCloud_2_VERTS_LIB_logo.png';">
        </div>
    </div>
</div>


# Topics to pick

# What ? The party is evolving !

We are interested in how the communication has evolved over the last legislature (2015-2019). Specifically, what are the main topics of each year for the different parties. The following chart represents the evolution of these different topics <b>over the years</b>.


You can select the party that you wish:
<button id="All">All</button>
<button id="UDC">UDC</button>
<button id="PS">PS</button>
<button id="PLR">PLR</button>
<button id="VERTS">VERTS</button>
<button id="PDC">PDC</button>
<button id="PVL">PVL</button>

<div id="topicsByYear" style="min-width: 310px; height: 650px; margin: auto"></div>

Globally, we observe a lot of changes over the years and three are really significant:
<ol>
  <li>The topic of the <b>climate</b> has largely <b>gained</b> in importance during the two past years.</li>
  <li>The theme of the <b>immigration</b> has <b>lost</b> in importance over the last legislature.</li>
  <li>Between 2015 and 2017, the question of the <b>AVS</b> (Assurance-Vieillesse et Survivants) has also considerably <b>grown</b> in importance.</li>
</ol>

These changes could be explained by the actualities e.g., votations, crisis, bombing, etc... We will focus on the first and main change, the climate change. During the past years, all the parties have started talking often about the global warming and the protection of the environment. The PLR and the PS have respectively <b>increased of approximately 25 and 40 times their communication about the climate</b> (in proportion). About 50% of the communication of the green party in 2019 is also about the climate, more than the other green (liberal) party, 36%. Thus the <i>Green Wave</i> has submerged until the twittersphere.

<script type="text/javascript">

var chart = Highcharts.chart('topicsByYear', {
  chart: {
    type: 'area'
},
title: {
    text: 'Evolution of the topics over the years for all the parties in their tweets'
},
xAxis: {
    categories: ['2015', '2016', '2017', '2018', '2019'],
    tickmarkPlacement: 'on',
    text: 'Years',
},
yAxis: {
    labels: {
        format: '{value}%'
    },
    title: {
        enabled: false
    }
},
tooltip: {
    pointFormat: '<span style="color:{series.color}">{series.name}</span>: <b>{point.percentage:.1f}%</b> ({point.y:,.0f} occurences)<br/>',
    split: true
},
plotOptions: {
    area: {
        stacking: 'percent',
        lineColor: '#ffffff',
        lineWidth: 1,
        marker: {
            lineWidth: 1,
            lineColor: '#ffffff'
        },
        accessibility: {
            pointDescriptionFormatter: function (point) {
                function round(x) {
                    return Math.round(x * 100) / 100;
                }
                return (point.index + 1) + ', ' + point.category + ', ' +
                    point.y + ' millions, ' + round(point.percentage) + '%, ' +
                    point.series.name;
            }
        }
    }
},
series: [{
    name: 'Climate',
    data: [100, 25, 118, 333, 2121]
}, {
    name: 'Immigration',
    data: [257, 223, 134, 275, 176]
}, {
    name: 'Safety',
    data: [104, 105, 114, 143, 222]
}, {
    name: 'Liberty',
    data: [138, 99, 109, 142, 236]
}, {
    name: 'Egality',
    data: [94, 98, 96, 292, 386]
}, {
    name: 'Economy',
    data: [159, 157, 164, 274, 513]
}, {
    name: 'Work',
    data: [232, 257, 331, 614, 677]
}, {
    name: 'Women',
    data: [72, 80, 205, 241, 497]
}, {
    name: 'Digital',
    data: [28, 37, 87, 132, 105]
}, {
    name: 'Family',
    data: [215, 165, 110, 170, 276]
}, {
    name: 'AVS',
    data: [45, 137, 263, 86, 179]
}, {
    name: 'Health',
    data: [51, 43, 104, 246, 382]
}, {
    name: 'Europe',
    data: [157, 141, 143, 322, 499]
}, {
    name: 'Army',
    data: [57, 37, 68, 40, 40]
}]

});

$('#All').click(function () {
    chart.update({
      title: {
          text: 'Evolution of the topics over the years for all the parties in their tweets'
      },
      series: [{
          name: 'Climate',
          data: [100, 25, 118, 333, 2121]
      }, {
          name: 'Immigration',
          data: [257, 223, 134, 275, 176]
      }, {
          name: 'Safety',
          data: [104, 105, 114, 143, 222]
      }, {
          name: 'Liberty',
          data: [138, 99, 109, 142, 236]
      }, {
          name: 'Egality',
          data: [94, 98, 96, 292, 386]
      }, {
          name: 'Economy',
          data: [159, 157, 164, 274, 513]
      }, {
          name: 'Work',
          data: [232, 257, 331, 614, 677]
      }, {
          name: 'Women',
          data: [72, 80, 205, 241, 497]
      }, {
          name: 'Digital',
          data: [28, 37, 87, 132, 105]
      }, {
          name: 'Family',
          data: [215, 165, 110, 170, 276]
      }, {
          name: 'AVS',
          data: [45, 137, 263, 86, 179]
      }, {
          name: 'Health',
          data: [51, 43, 104, 246, 382]
      }, {
          name: 'Europe',
          data: [157, 141, 143, 322, 499]
      }, {
          name: 'Army',
          data: [57, 37, 68, 40, 40]
      }]
    });
});

$('#UDC').click(function () {
    chart.update({
      title: {
          text: 'Evolution of the topics over the years for the UDC in their tweets'
      },
      series: [{
          name: 'Climate',
          data: [2, 0, 1, 12, 16]
      }, {
          name: 'Immigration',
          data: [41, 33, 8, 36, 48]
      }, {
          name: 'Safety',
          data: [10, 7, 2, 1, 30]
      }, {
          name: 'Liberty',
          data: [5, 6, 6, 14, 78]
      }, {
          name: 'Egality',
          data: [0, 0, 1, 0, 4]
      }, {
          name: 'Economy',
          data: [5, 5, 1, 12, 31]
      }, {
          name: 'Work',
          data: [4, 8, 4, 8, 35]
      }, {
          name: 'Women',
          data: [3, 0, 0, 2, 17]
      }, {
          name: 'Digital',
          data: [0, 0, 0, 0, 0]
      }, {
          name: 'Family',
          data: [4, 3, 0, 6, 6]
      }, {
          name: 'AVS',
          data: [2, 1, 5, 1, 14]
      }, {
          name: 'Health',
          data: [0, 0, 0, 0, 10]
      }, {
          name: 'Europe',
          data: [6, 2, 4, 22, 95]
      }, {
          name: 'Army',
          data: [3, 2, 0, 0, 2]
      }]
    });
});

$('#PS').click(function () {
    chart.update({
      title: {
          text: 'Evolution of the topics over the years for the PS in their tweets'
      },
      series: [{
          name: 'Climate',
          data: [3, 8, 39, 96, 353]
      }, {
          name: 'Immigration',
          data: [73, 88, 71, 174, 44]
      }, {
          name: 'Safety',
          data: [30, 27, 59, 86, 87]
      }, {
          name: 'Liberty',
          data: [31, 30, 45, 57, 36]
      }, {
          name: 'Egality',
          data: [55, 70, 77, 198, 180]
      }, {
          name: 'Economy',
          data: [29, 35, 64, 113, 81]
      }, {
          name: 'Work',
          data: [120, 164, 218, 373, 316]
      }, {
          name: 'Women',
          data: [36, 63, 147, 184, 216]
      }, {
          name: 'Digital',
          data: [6, 2, 22, 37, 41]
      }, {
          name: 'Family',
          data: [85, 62, 69, 92, 112]
      }, {
          name: 'AVS',
          data: [22, 62, 180, 56, 71]
      }, {
          name: 'Health',
          data: [29, 26, 63, 68, 146]
      }, {
          name: 'Europe',
          data: [92, 94, 99, 182, 107]
      }, {
          name: 'Army',
          data: [7, 18, 24, 27, 16]
      }]

    });
});

$('#PLR').click(function () {
    chart.update({
      title: {
          text: 'Evolution of the topics over the years for the PLR in their tweets'
      },
      series: [{
          name: 'Climate',
          data: [4, 1, 10, 30, 176]
      }, {
          name: 'Immigration',
          data: [55, 55, 23, 33, 26]
      }, {
          name: 'Safety',
          data: [23, 37, 21, 24, 20]
      }, {
          name: 'Liberty',
          data: [66, 53, 44, 37, 38]
      }, {
          name: 'Egality',
          data: [6, 10, 9, 31, 13]
      }, {
          name: 'Economy',
          data: [33, 47, 49, 71, 89]
      }, {
          name: 'Work',
          data: [52, 50, 58, 124, 96]
      }, {
          name: 'Women',
          data: [25, 8, 27, 11, 35]
      }, {
          name: 'Digital',
          data: [16, 33, 41, 73, 18]
      }, {
          name: 'Family',
          data: [27, 45, 9, 10, 32]
      }, {
          name: 'AVS',
          data: [10, 46, 34, 6, 15]
      }, {
          name: 'Health',
          data: [0, 7, 6, 55, 43]
      }, {
          name: 'Europe',
          data: [31, 24, 14, 43, 67]
      }, {
          name: 'Army',
          data: [9, 1, 6, 4, 4]
      }]
    });
});

$('#VERTS').click(function () {
    chart.update({
      title: {
          text: 'Evolution of the topics over the years for the VERTS in their tweets'
      },
      series: [{
          name: 'Climate',
          data: [75, 11, 57, 153, 1365]
      }, {
          name: 'Immigration',
          data: [44, 16, 9, 9, 28]
      }, {
          name: 'Safety',
          data: [11, 6, 19, 9, 30]
      }, {
          name: 'Liberty',
          data: [4, 3, 4, 8, 47]
      }, {
          name: 'Egality',
          data: [22, 5, 3, 38, 148]
      }, {
          name: 'Economy',
          data: [47, 49, 16, 18, 203]
      }, {
          name: 'Work',
          data: [24, 7, 23, 31, 134]
      }, {
          name: 'Women',
          data: [4, 1, 5, 20, 156]
      }, {
          name: 'Digital',
          data: [4, 1, 19, 2, 24]
      }, {
          name: 'Family',
          data: [22, 7, 6, 13, 56]
      }, {
          name: 'AVS',
          data: [8, 5, 6, 4, 2]
      }, {
          name: 'Health',
          data: [15, 2, 5, 6, 58]
      }, {
          name: 'Europe',
          data: [12, 8, 7, 9, 115]
      }, {
          name: 'Army',
          data: [10, 3, 7, 6, 11]
      }]
    });
});

$('#PDC').click(function () {
    chart.update({
      title: {
          text: 'Evolution of the topics over the years for the PDC in their tweets'
      },
      series: [{
          name: 'Climate',
          data: [8, 4, 6, 7, 47]
      }, {
          name: 'Immigration',
          data: [36, 27, 23, 17, 24]
      }, {
          name: 'Safety',
          data: [13, 24, 11, 18, 41]
      }, {
          name: 'Liberty',
          data: [19, 6, 9, 24, 12]
      }, {
          name: 'Egality',
          data: [10, 12, 4, 19, 19]
      }, {
          name: 'Economy',
          data: [16, 12, 28, 48, 64]
      }, {
          name: 'Work',
          data: [23, 23, 23, 63, 61]
      }, {
          name: 'Women',
          data: [2, 4, 25, 14, 37]
      }, {
          name: 'Digital',
          data: [2, 1, 4, 17, 19]
      }, {
          name: 'Family',
          data: [60, 40, 23, 45, 41]
      }, {
          name: 'AVS',
          data: [3, 20, 37, 14, 73]
      }, {
          name: 'Health',
          data: [6, 7, 30, 116, 114]
      }, {
          name: 'Europe',
          data: [13, 11, 15, 42, 51]
      }, {
          name: 'Army',
          data: [26, 10, 31, 2, 7]
      }]
    });
});

$('#PVL').click(function () {
    chart.update({
      title: {
          text: 'Evolution of the topics over the years for the PVL in their tweets'
      },
      series: [{
          name: 'Climate',
          data: [8, 1, 5, 35, 164]
      }, {
          name: 'Immigration',
          data: [8, 4, 0, 6, 6]
      }, {
          name: 'Safety',
          data: [17, 4, 2, 5, 14]
      }, {
          name: 'Liberty',
          data: [13, 1, 1, 2, 25]
      }, {
          name: 'Egality',
          data: [1, 1, 2, 6, 22]
      }, {
          name: 'Economy',
          data: [29, 9, 6, 12, 45]
      }, {
          name: 'Work',
          data: [9, 5, 5, 15, 35]
      }, {
          name: 'Women',
          data: [2, 4, 1, 10, 36]
      }, {
          name: 'Digital',
          data: [0, 0, 1, 3, 3]
      }, {
          name: 'Family',
          data: [17, 8, 3, 4, 29]
      }, {
          name: 'AVS',
          data: [0, 3, 1, 5, 4]
      }, {
          name: 'Health',
          data: [2, 1, 0, 1, 11]
      }, {
          name: 'Europe',
          data: [3, 2, 4, 24, 64]
      }, {
          name: 'Army',
          data: [2, 3, 0, 1, 0]
      }]
    });
});

$(function () {
        $('#container').highcharts({
            chart: {
                type: 'item'
            },

            title: {
                text: 'Results of the 2019 Swiss federal elections in Romandy'
            },


            legend: {
                labelFormat: '{name} <span style="opacity: 0.4">{y}</span>'
            },

            series: [{
                name: 'Representatives',
                keys: ['name', 'y', 'color', 'label'],
                data: [
                    ['Parti Socialiste', 16, '#EB001F', 'PS'],
                    ['Les Verts', 14, '#33cc33', 'VERTS'],
                    ['Parti démocrate-chrétien', 7, 'orange', 'PDC'],
                    ['Parti vert-libéraux', 6, '#ccff66', 'PVL'],
                    ['Parti libéral-radical', 12, '#009EE0', 'PLR'],
                    ['Union démocratique du centre', 15, 'darkgreen', 'UDC'],
                    ['Others', 6, '#000000', 'Others']
                ],
                dataLabels: {
                    enabled: true,
                    format: '{point.label}'
                },

                // Circular options
                center: ['50%', '88%'],
                size: '170%',
                startAngle: -100,
                endAngle: 100
            }]

        });
    });

</script>

## Get Started


## Next Steps

See: [Customize Duo](https://chibicode.github.io/duo/posts/customize).

## Like or Retweet Appreciated :)

<blockquote class="twitter-tweet" data-cards="hidden" data-lang="en"><p lang="en" dir="ltr">Just published: Duo, A Simple Jekyll Theme.  <a href="https://t.co/G2kffR9e4U">https://t.co/G2kffR9e4U</a> <a href="https://twitter.com/jekyllrb?ref_src=twsrc%5Etfw">@jekyllrb</a></p>&mdash; Shu Uesugi (@chibicode) <a href="https://twitter.com/chibicode/status/923156795824128000?ref_src=twsrc%5Etfw">October 25, 2017</a></blockquote>

<!-- <a href="https://github.com/chibicode/duo" class="github-corner"><svg width="80" height="80" viewBox="0 0 250 250" style="fill:#151513; color:#fff; position: absolute; top: 0; border: 0; right: 0;"><path d="M0,0 L115,115 L130,115 L142,142 L250,250 L250,0 Z"></path><path d="M128.3,109.0 C113.8,99.7 119.0,89.6 119.0,89.6 C122.0,82.7 120.5,78.6 120.5,78.6 C119.2,72.0 123.4,76.3 123.4,76.3 C127.3,80.9 125.5,87.3 125.5,87.3 C122.9,97.6 130.6,101.9 134.4,103.2" fill="currentColor" style="transform-origin: 130px 106px;" class="octo-arm"></path><path d="M115.0,115.0 C114.9,115.1 118.7,116.5 119.8,115.4 L133.7,101.6 C136.9,99.2 139.9,98.4 142.2,98.6 C133.8,88.0 127.5,74.4 143.8,58.0 C148.5,53.4 154.0,51.2 159.7,51.0 C160.3,49.4 163.2,43.6 171.4,40.1 C171.4,40.1 176.1,42.5 178.8,56.2 C183.1,58.6 187.2,61.8 190.9,65.4 C194.5,69.0 197.7,73.2 200.1,77.6 C213.8,80.2 216.3,84.9 216.3,84.9 C212.7,93.1 206.9,96.0 205.4,96.6 C205.1,102.4 203.0,107.8 198.3,112.5 C181.9,128.9 168.3,122.5 157.7,114.1 C157.9,116.9 156.7,120.9 152.7,124.9 L141.0,136.5 C139.8,137.7 141.6,141.9 141.8,141.8 Z" fill="currentColor" class="octo-body"></path></svg></a><style>.github-corner:hover .octo-arm{animation:octocat-wave 560ms ease-in-out}@keyframes octocat-wave{0%,100%{transform:rotate(0)}20%,60%{transform:rotate(-25deg)}40%,80%{transform:rotate(10deg)}}@media (max-width:500px){.github-corner:hover .octo-arm{animation:none}.github-corner .octo-arm{animation:octocat-wave 560ms ease-in-out}}</style><script async defer src="https://buttons.github.io/buttons.js"></script> -->
