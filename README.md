#### 示例代码参考 energy-plan-page下的 plan-year-product
##### 更新ucf-common的公共代码
```js
components-->Button
components-->FormItemCom
components-->Grid
components-->SearchPanel
components-->Section
styles-->app.less
```
##### detail页面修改 IndexView

1. 去掉AcHandTable 组件的tableClassName // tableClassName='hand-table-custom'
2.分页和按钮位置调整
```js
<div className="btn-page-group">
    <div className='table-header'>
        <Button shape="border" onClick={this.delRecordDetail}>删除</Button>
        <Button className="ml8" shape="border" onClick={this.expDetail}>导出</Button>
    </div>
    {/*分页信息*/}
    <PaginationTable
        onChange={this.onTableChange}
        total={detailObj.total} // 总共多少条
        pageNum={detailObj.pageNum} // 每页多少条
        activePage={detailObj.activePage} // 第几页
    />
</div>
```
3.Tabs 添加 tabBarStyle
```js
  <Tabs tabBarStyle="upborder">
      <TabPane tab='计划明细' key="1"/>
  </Tabs>
```
4.将创建信息整合到基础信息中，放到最后


