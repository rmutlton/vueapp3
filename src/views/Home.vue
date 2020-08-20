<template>
  <v-container>
    <v-row>
      <v-col cols="4">
        <v-card color="#385F73" dark>
          <v-card-title><div class="font-big">จำนวนลูกค้า</div></v-card-title>

          <v-card-text><div class="font-big">50 คน</div></v-card-text>

          <v-card-actions>
            <v-btn text>ข้อมูลลูกค้า</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col cols="4">
        <v-card color="#385F73" dark>
          <v-card-title><div class="font-big">จำนวนสินค้า</div></v-card-title>

          <v-card-text><div class="font-big">20 ชิ้น</div></v-card-text>

          <v-card-actions>
            <v-btn text>ข้อมูลสินค้า</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col cols="4">
        <v-card color="#385F73" dark>
          <v-card-title><div class="font-big">จำนวนรายงาน</div></v-card-title>

          <v-card-text><div class="font-big">16 รายการ</div></v-card-text>

          <v-card-actions>
            <v-btn text>ข้อมูลรายงาน</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
        <v-card class="mx-auto text-center" color="green" dark>
          <v-card-text>
            <v-sheet color="rgba(0, 0, 0, .12)">
              <v-sparkline
                :value="value"
                color="rgba(255, 255, 255, .8)"
                height="70"
                padding="14"
                stroke-linecap="round"
                smooth
                line-width="2"
                type="trend"
              >
                <template v-slot:label="item"> {{ item.value }} บ.</template>
              </v-sparkline>
            </v-sheet>
          </v-card-text>

          <v-card-text>
            <div class="font-big">รายงานการขาย</div>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      value: [700, 200, 300, 700, 500, 600, 700],
    };
  },
};
</script>

<style scope>
.font-big {
  font-size: 30px;
}
</style>
