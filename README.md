# vue插件(适用油站弹框)

## 下载
`npm i apply-stations -S`

## 使用
```
// main.js
import applyStations from 'apply-stations'
import 'apply-stations/lib/apply-stations.css'
Vue.use(applyStations)

// XXX.vue
<applyStations :applyStations="applyStations" v-if="applyStations.length" @hiddenStations = "hiddenStations"></applyStations>

export default {
  data () {
    return {
      applyStations: []
    }
  },
  methods: {
    hiddenStations () {
      // 这里关闭弹框...
      this.applyStations = []
    },
    showStations () {
      // 加载油站列表,数据格式要求如下
      this.applyStations = [
        { city: '太原市', address: ['太原市杏花岭区建设北路76号', '太原市杏花岭区建设北路76号'] },
        { city: '太原市', address: ['太原市杏花岭区建设北路76号', '太原市杏花岭区建设北路76号'] },
        { city: '太原市', address: ['太原市杏花岭区建设北路76号', '太原市杏花岭区建设北路76号'] },
        { city: '太原市', address: ['太原市杏花岭区建设北路76号', '太原市杏花岭区建设北路76号', '太原市杏花岭区建设北路76号', '太原市杏花岭区建设北路76号'] },
        { city: '北京市', address: ['北京市杏花岭区建设北路76号', '北京市杏花岭区建设北路76号'] }
      ]
    }
  }
}
```
