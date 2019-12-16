
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.min.js"></script>
<script src="https://code.highcharts.com/highcharts.js"></script>
<script src="https://code.highcharts.com/modules/item-series.js"></script>
<script src="https://code.highcharts.com/modules/exporting.js"></script>
<script src="https://code.highcharts.com/modules/export-data.js"></script>
<script src="https://code.highcharts.com/modules/accessibility.js"></script>

# Abstract:
In October 2019, the <b>Swiss federal elections</b> took place and led to a huge paradigm shift. Almost all the parties started talking about climate change and the two Swiss green parties increased considerably their numbers of representatives into the parliament. This phenomenon has been called the <b><i>Green Wave</i></b>, and has been designated <a target="_BLANK" href="https://www.rts.ch/info/culture/10916700-en-suisse-romande-vague-verte-choisie-comme-expression-de-l-annee.html">expression of the year</a> in Romandy. Through this data story, we aim to better understand how the different <b>Swiss political parties</b> communicate their ideas to the public, e.g., what are the keywords and topics they address the most. We concentrate on the six largest parties of the last elections and observe if there is any <b>change in their communication</b> over the years and if so, if it has a relationship with the results of the federal elections.

<div id="container" style="min-width: 310px; height: 400px; margin: auto"></div>


# Introduction:

Twitter is became a central medium of communication and is used by most of the politicians to transmit their ideas. The restriction of 280 characters by tweet forces the politicians to be succinct and to compress their ideas to keep only the essential, using often the same recurrent keywords. It provides for us a good way to grasp what topics are mainly addressed by each party and politician. Therefore, we analyze <b>163,186 tweets</b> posted by the sixth largest parties (listed below) and some of their members (selected by their <a target="_BLANK" href="https://www.tagesanzeiger.ch/sonntagszeitung/wer-hat-in-bern-am-meisten-einfluss/story/11893481">influence</a> in the parliament). We also use the archives of the Radio Television of Switzerland (<b>RTS</b>) to understand what are the principal topics discussed by the politicians over the years. Finally, we compare the changes in communications of the parties with the <b>results of the federal</b> elections using the associated datasets.

# Swiss parties you said ?

To familiarize with political parties of Switzerland, we propose first a small introduction about them, with the most used words in their tweets (members and parties tweets aggregated):

<h2 style = "color: #FFFFFF;background-color:#006400;display: table; "> UDC</h2> The Swiss People’s party or Democratic Union of the Centre (Union Démocratique du Centre in french) is a national-conservative, right wing populist party. It’s the party with the more members in the Swiss parliament. They fight for the preservation of Switzerland's political sovereignty (they are eurosceptic) and are against mass immigration by making the asylum laws stricter. The party opposes governmental measures for environmental protection.

<h2 style = "color: #FFFFFF;background-color:#EB001F;display: table; "> PSS </h2> The Social Democratic Party of Switzerland or Socialist party (Parti Socialiste suisse in French) is a socialist, progressive and Centre-left party. It’s the second strongest party in Switzerland. They are in favor of strong public services, environmental policy with climate change mitigation and social equity in an open society. The party is against policies of economic liberalization such as deregulation and capitalism.

<h2 style = "color: #FFFFFF;background-color:#009EE0;display: table; "> PLR </h2> The Liberals (Parti Libéral-radical in French) is a liberal and right-wing party. It’s the third largest party in the Swiss parliament. They call themselves the party of the economy and promote individual responsibility. The party believes that an open society and economic freedom are more conducive to prosperity, rather than a redistributive and regulative state.

<h2 style = "color: #FFFFFF;background-color:#33cc33;display: table; "> Les VERTS</h2> The green Party of Switzerland (Les Verts in French) is a environmentalist, progressive and left-wing party. It’s the fourth-largest party in Switzerland. Their main concerns are the protection of the environment and the fight against climate change. The party is often allied with the Socialist Party, sharing common values such as social equity and strong public services.

<h2 style = "color: #FFFFFF;background-color:#FFA500;display: table; "> PDC </h2> The Christian Democratic People’s party of Switzerland (Parti Démocrate-Chrétien in French) is a Christian-democratic and centre-right party. It’s the fifth strongest party in Switzerland. They advocate moderate social conservatism and social market economy, balance between economic liberalism and social justice. They consider themselves as the link between the left and the right wing.

<h2 style = "color: #000000;background-color:#ccff66;display: table; "> PVL </h2> The Green Liberal Party of Switzerland (Parti vert’libéral in French) is a centre-right,  green-liberal party in Switzerland. It’s the youngest and the sixth strongest party in Switzerland. They seek to combine moderate economic liberalism with environmental sustainability. The party promotes economic growth, but with the preservation of the environment. They encourage sustainable energy.



<script type="text/javascript">

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
