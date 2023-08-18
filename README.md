<h1 align="center">Response Table 響應式表格</h1>

<p align="center">
可以依照裝置螢幕切換表格模式
</p>


## Init
```
npm install
```

## Build
```
npm run build
```



```

<ResponseTable :data="tableData" style="width: 100%" >
    <ResponseTableColumn prop="date" label="Date" width="180" />
    <ResponseTableColumn prop="name" label="Name" width="180" />
    <ResponseTableColumn prop="address" label="Address" />
</ResponseTable>


<templete v-if="isDesTop">
//桌機
<ResponseTableDesTop >
    <ResponseTableColumnDesTop>
</ResponseTableDesTop>
<templete v-if="isMobile">
</templete>
//行動
<ResponseTableMobile>
    <ResponseTableColumnMobile>
</ResponseTableMobile>

</templete>
```