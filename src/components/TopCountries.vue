<template>
    <div id="countries">
    </div>
</template>

<script>
    import * as hc from 'highcharts';

    export default {
        mounted() {

            hc.chart(this.$el, {
                chart: {
                    type: "bar",
                    backgroundColor: 'transparent'
                },
                credits: {
                    enabled: false
                },
                legend: {
                    enabled: false
                },
                plotOptions: {
                    bar: {
                        color: "#5f21f2",
                        pointWidth: 20,

                        dataLabels: {
                            enabled: true,
                            inside: false,
                            color: "#5f21f2",
                            style: {
                                fontWeight: 'bold'
                            },
                            align: "left",
                            allowOverlap: false,
                            overflow: false,
                            crop: false,
                            formatter() {
                                return `~${this.y / 1000000}M`
                            }
                        },

                    },
                    series: {
                        groupPadding: 0.2
                    }
                },
                xAxis: {
                    type: "category",
                    visible: true,
                    allowTicks: false,
                    lineWidth: 0,
                    labels: {
                        useHTML: true,
                        style: {
                            width: "160%",
                            color: "#000000",
                            fontWeight: "bolder",
                            fontSize: "1.1rem",
                            padding: "0"
                        },
                        align: 'left',
                        enabled: true,
                        overflow: false,
                        crop: true,
                        x: 0,
                        y: -20,
                        distance: 0,
                        padding: 0
                    }

                },
                yAxis: {
                    visible: false,
                    labels: {
                        enabled: true
                    },
                },

                title: {
                    text: null
                },
                series: [{
                    name: "Number of subscribers",
                    data: [
                        ["U. Arab Emirates", 5500000],
                        ["United States", 3600000],
                        ["India", 3400000]
                    ]
                }]
            });
        }
    };
</script>

<style lang="scss" scoped>
    #countries {
        height: 200px;
        width: 100%;
    }
</style>


