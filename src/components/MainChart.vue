<template>
    <div class="chart">
        <div id="container" class="chart__container"></div>
    </div>
</template>

<script>
    import * as hc from 'highcharts';

    export default {

        mounted: () => {
            hc.chart("container", {
                chart: {
                    type: "column"
                },
                credits: {
                    enabled: false
                },
                title: {
                    text: "Number of subscribers",
                    align: "left",
                    style: {
                        fontWeight: "bold"
                    }
                },
                legend: {
                    enabled: false
                },
                plotOptions: {
                    column: {
                        color: "#5f21f2"
                    }
                },
                xAxis: {
                    type: "category",
                    labels: {
                        style: {
                            fontSize: "0.7rem"
                        }
                    }
                },
                yAxis: {
                    title: {
                        enabled: false
                    }
                },
                series: [{
                    name: "Number of subscribers",
                    data: [
                        ["Oct 2017", 550000],
                        ["Nov 2017", 500000],
                        ["Dec 2017", 600000],
                        ["Jan 2018", 700000],
                        ["Feb 2018", 650000],
                        ["Mar 2018", 690000],
                        ["Apr 2018", 800000],
                        ["May 2018", 500000],
                        ["Jun 2018", 520000],
                        ["Jul 2018", 730000],
                        ["Aug 2018", 710000],
                        ["Sep 2018", 900000]
                    ]
                }]
            });
        }
    };
</script>

<style lang="scss" scoped>
    .chart {
        margin-top: 2rem;
        margin-bottom: 2rem;
    }

    .chart__container {
        height: 300px;
    }
</style>


