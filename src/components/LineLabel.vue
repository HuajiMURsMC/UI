<!--
  Copyright (C) 2022 Suwings <Suwings@outlook.com>

  This program is free software: you can redistribute it and/or modify
  it under the terms of the GNU Affero General Public License as published by
  the Free Software Foundation, either version 3 of the License, or
  (at your option) any later version.
  
  According to the AGPL, it is forbidden to delete all copyright notices, 
  and if you modify the source code, you must open source the
  modified source code.

  版权所有 (C) 2022 Suwings <Suwings@outlook.com>

  该程序是免费软件，您可以重新分发和/或修改据 GNU Affero 通用公共许可证的条款，
  由自由软件基金会，许可证的第 3 版，或（由您选择）任何更高版本。

  根据 AGPL 与用户协议，您必须保留所有版权声明，如果修改源代码则必须开源修改后的源代码。
  可以前往 https://mcsmanager.com/ 阅读用户协议，申请闭源开发授权等。
-->

<template>
  <div
    class="line-label-wrapper"
    v-bind:class="{
      'line-label-margin-24': !size,
      'line-label-margin-12': size == 'small',
      'line-label-margin-4': size == 'mini'
    }"
  >
    <div
      class="line-label-title"
      v-bind:class="{
        'line-label-title-120px': !space,
        'line-label-title-80px': space == 'small',
        'line-label-title-40px': space == 'mini'
      }"
    >
      <slot name="title"></slot>
    </div>
    <div class="line-label-text">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    size: String,
    space: String
  }
};
</script>

<style scoped>
.line-label-wrapper {
  line-height: 14px;
  font-size: 14px;
}

.line-label-margin-24 {
  margin: 24px 0px;
}

.line-label-margin-12 {
  margin: 12px 0px;
}

.line-label-margin-4 {
  margin: 4px 0px;
}

.line-label-title-120px {
  width: 120px;
}

.line-label-title-80px {
  width: 80px;
}

.line-label-title-40px {
  width: 40px;
}

.line-label-title {
  display: inline-block;

  color: rgb(117, 117, 117);
}

.line-label-text {
  display: inline-block;
  vertical-align: top;
}

.line-label-link {
  font-size: 14px;
  color: #348de6;
}
</style>
