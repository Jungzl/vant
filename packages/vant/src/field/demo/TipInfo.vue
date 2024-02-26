<script setup lang="ts">
import VanField from '..';
import VanCellGroup from '../../cell-group';
import { ref } from 'vue';
import { useTranslate } from '../../../docs/site';

const t = useTranslate({
  'zh-CN': {
    phone: '手机号',
    tipInfo: '帮助提示',
    phoneTip: '手机号格式为11位数字',
    phonePlaceholder: '请输入手机号',
  },
  'en-US': {
    phone: 'Phone',
    tipInfo: 'Tip Info',
    phoneTip: 'Phone number should be 11 digits',
    phonePlaceholder: 'Phone',
  },
});

const phone = ref('123');
</script>

<template>
  <demo-block :title="t('tipInfo')">
    <van-cell-group inset>
      <van-field
        v-model="phone"
        :label="t('phone')"
        :placeholder="t('phonePlaceholder')"
        :tip-message="t('phoneTip')"
      />
    </van-cell-group>
  </demo-block>
</template>
