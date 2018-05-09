<template>
  <div id="app">
    <EditTable :defaultData="data" :tableIndex="tableIndex">
    </EditTable>
  </div>
</template>

<script>
import EditTable from "./components/editTable/EditTable";

export default {
  name: "App",
  components: {
    EditTable
  },
  data() {
    return {
      data: [
        {
          id: "6B62FD5322ED7884E0538D09400ADBC6",
          isDeleted: 0,
          code: "SC6472A5.null.RE9",
          name: "SC6472A5.null.RE9",
          areaCode: "CQ_LM_GC",
          materielCode: "materiel_type_1",
          sectionCodes: " ",
          status: 1,
          entBrand: "长安1",
          bisBrand: "长安汽车",
          proBrand: "凌轩",
          proName: "凌轩",
          proModel: "SC6472A5",
          proStateCode: "V3-L",
          proColor: "RE9",
          proColorName: "霓红",
          proModelName: "JL478QEA 1.6L 国五 国五 7.4",
          areaName: "重庆-长安铃木一工厂",
          materielName: "物料类型1"
        },
        {
          id: "6B62FD5322EF7884E0538D09400ADBC6",
          isDeleted: 0,
          code: "SC7169C.C43A.YC3",
          name: "SC7169C.C43A.YC3",
          areaCode: "CQ_LM_GC",
          materielCode: "materiel_type_1",
          sectionCodes: " ",
          status: 1,
          entBrand: "长安",
          bisBrand: "长安汽车",
          proBrand: "星光小卡",
          proName: "逸动",
          proModel: "SC7169C",
          proStateCode: "C43A",
          proColor: "YC3",
          proColorName: "华彩金",
          proModelName: "1.6L 4AT 国四",
          areaName: "重庆-长安铃木一工厂",
          materielName: "物料类型1"
        },
        {
          id: "6B62FD5322F07884E0538D09400ADBC6",
          isDeleted: 0,
          code: "SC7169C.C6.YB6",
          name: "SC7169C.C6.YB6",
          areaCode: "CQ_LM_GC",
          materielCode: "materiel_type_1",
          sectionCodes: " ",
          status: 1,
          entBrand: "长安",
          bisBrand: "长安汽车",
          proBrand: "逸动",
          proName: "逸动",
          proModel: "SC7169C",
          proStateCode: "C6",
          proColor: "YB6",
          proColorName: "闪光动力金黄",
          proModelName: "1.6L 4AT 国四",
          areaName: "重庆-长安铃木一工厂",
          materielName: "物料类型1"
        },
        {
          id: "6B62FD5322F17884E0538D09400ADBC6",
          isDeleted: 0,
          code: "SC7169C.C6.YC3",
          name: "SC7169C.C6.YC3",
          areaCode: "CQ_LM_GC",
          materielCode: "materiel_type_1",
          sectionCodes: " ",
          status: 1,
          entBrand: "长安",
          bisBrand: "长安汽车",
          proBrand: "逸动",
          proName: "逸动",
          proModel: "SC7169C",
          proStateCode: "C6",
          proColor: "YC3",
          proColorName: "华彩金",
          proModelName: "1.6L 4AT 国四",
          areaName: "重庆-长安铃木一工厂",
          materielName: "物料类型1"
        },
        {
          id: "6B62FD5322F27884E0538D09400ADBC6",
          isDeleted: 0,
          code: "SC7141A5.A31A.YB8",
          name: "SC7141A5.A31A.YB8",
          areaCode: "CQ_LM_GC",
          materielCode: "materiel_type_1",
          sectionCodes: " ",
          status: 1,
          entBrand: "长安",
          bisBrand: "长安汽车",
          proBrand: "奔奔",
          proName: "新奔奔",
          proModel: "SC7141A5",
          proStateCode: "A31A",
          proColor: "YB8",
          proColorName: "闪光香摈黄",
          proModelName: "1.4L MT 国五二",
          areaName: "重庆-长安铃木一工厂",
          materielName: "物料类型1"
        },
        {
          id: "6B62FD5322F37884E0538D09400ADBC6",
          isDeleted: 0,
          code: "SC7141A5.A31A.YC5",
          name: "SC7141A5.A31A.YC5",
          areaCode: "CQ_LM_GC",
          materielCode: "materiel_type_1",
          sectionCodes: " ",
          status: 1,
          entBrand: "长安",
          bisBrand: "长安汽车",
          proBrand: "奔奔",
          proName: "新奔奔",
          proModel: "SC7141A5",
          proStateCode: "A31A",
          proColor: "YC5",
          proColorName: "香槟",
          proModelName: "1.4L MT 国五二",
          areaName: "重庆-长安铃木一工厂",
          materielName: "物料类型1"
        },
        {
          id: "6B62FD5322F47884E0538D09400ADBC6",
          isDeleted: 0,
          code: "SC7141A5.A31A.YC6",
          name: "SC7141A5.A31A.YC6",
          areaCode: "CQ_LM_GC",
          materielCode: "materiel_type_1",
          sectionCodes: " ",
          status: 1,
          entBrand: "长安",
          bisBrand: "长安汽车",
          proBrand: "奔奔",
          proName: "新奔奔",
          proModel: "SC7141A5",
          proStateCode: "A31A",
          proColor: "YC6",
          proColorName: "炫目橙",
          proModelName: "1.4L MT 国五二",
          areaName: "重庆-长安铃木一工厂",
          materielName: "物料类型1"
        },
        {
          id: "6B62FD5322F57884E0538D09400ADBC6",
          isDeleted: 0,
          code: "SC5020XXYAB5.H6D1.NA4",
          name: "SC5020XXYAB5.H6D1.NA4",
          areaCode: "CQ_LM_GC",
          materielCode: "materiel_type_1",
          sectionCodes: " ",
          status: 1,
          entBrand: "长安",
          bisBrand: "长安轻型车",
          proBrand: "睿行",
          proName: "睿行M90",
          proModel: "SC5020XXYAB5",
          proStateCode: "H6D1",
          proColor: "NA4",
          proColorName: "闪光琥珀棕",
          proModelName: "SC5020XXYAB5",
          areaName: "重庆-长安铃木一工厂",
          materielName: "物料类型1"
        },
        {
          id: "6B62FD5322F67884E0538D09400ADBC6",
          isDeleted: 0,
          code: "SC7155AA5.S1-L.BJ8",
          name: "SC7155AA5.S1-L.BJ8",
          areaCode: "CQ_LM_GC",
          materielCode: "materiel_type_1",
          sectionCodes: " ",
          status: 1,
          entBrand: "长安",
          bisBrand: "长安汽车",
          proBrand: "CS",
          proName: "CS55",
          proModel: "SC7155AA5",
          proStateCode: "S1-L",
          proColor: "BJ8",
          proColorName: "深海蓝",
          proModelName: "JL476ZQCD 1.5T 国Ⅴ 6MT 不带STT",
          areaName: "重庆-长安铃木一工厂",
          materielName: "物料类型1"
        },
        {
          id: "6B62FD5322F77884E0538D09400ADBC6",
          isDeleted: 0,
          code: "SC7155AA5.S1-L.YF1",
          name: "SC7155AA5.S1-L.YF1",
          areaCode: "CQ_LM_GC",
          materielCode: "materiel_type_1",
          sectionCodes: " ",
          status: 1,
          entBrand: "长安",
          bisBrand: "长安汽车",
          proBrand: "CS",
          proName: "CS55",
          proModel: "SC7155AA5",
          proStateCode: "S1-L",
          proColor: "YF1",
          proColorName: "活力橙黄",
          proModelName: "JL476ZQCD 1.5T 国Ⅴ 6MT 不带STT",
          areaName: "重庆-长安铃木一工厂",
          materielName: "物料类型1"
        }
      ],
      tableIndex: [
        {
          name: "企业品牌",
          dataKey: "entBrand",
          width: 120,
          required: true
        },
        {
          name: "业务品牌",
          dataKey: "bisBrand",
          type: "selectRemote",
          url: "config/data/child/product_bis_brand",
          width: 120,
          required: true
        },
        {
          name: "产品品牌",
          dataKey: "proBrand",
          type: "selectRemote",
          url: "config/data/child/product_pro_brand",
          width: 100,
          required: true
        },
        {
          name: "产品名称",
          dataKey: "proName",
          width: 100,
          required: true
        },
        {
          name: "车型号",
          dataKey: "proModel",
          width: 140,
          required: true
        },
        {
          name: "车型名称",
          dataKey: "proModelName",
          width: 200
        },
        {
          name: "状态号",
          dataKey: "proStateCode",
          width: 200,
          required: true
        },
        {
          name: "车身颜色",
          dataKey: "proColor",
          width: 100,
          required: true
        },
        {
          name: "车身颜色名称",
          dataKey: "proColorName",
          width: 160
        },
        {
          name: "产品段",
          dataKey: "sectionCodes",
          width: 100
        },
        {
          name: "整车编码",
          dataKey: "code",
          width: 230,
          required: true
        },
        {
          name: "制造基地",
          dataKey: "areaCode",
          type: "selectRemote",
          selectKey: "areaName",
          url: "zclr-analyze/basic-product/makeArea",
          width: 180,
          required: true
        },
        {
          name: "物料类型",
          dataKey: "materielCode",
          type: "selectRemote",
          selectKey: "materielName",
          url: "config/data/child/materiel_type",
          width: 110
        },
        {
          dataKey: "status",
          name: "状态",
          width: 100,
          type: "select",
          required: true
        }
      ]
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
