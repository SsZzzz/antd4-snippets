# antd4-snippets README

提供大部分的 antd 组件以及 dva 的代码片段,以下是一些例子.

### antdButton

```html
<Button type="primary">按钮</Button>
```

### antdRow

```html
<Row gutter={16}>
  <Col span={6}></Col>
  <Col span={6}></Col>
  <Col span={6}></Col>
  <Col span={6}></Col>
</Row>
```

### antdTable

```jsx
const columns = [
  {
    title: '',
    dataIndex: '',
  },
];

function handleTableChange(pagination, filters, sorter) {}

<Table
  rowKey="id"
  dataSource={[]}
  columns={columns}
  loading={loading}
  onChange={handleTableChange}
  pagination={{
    current: current,
    pageSize: pageSize,
    total: total,
    showSizeChanger: true,
    showQuickJumper: true,
    showTotal: (total) => `共 ${total} 条`,
  }}
/>
```

### !dva

```javascript
import { cloneDeep } from 'lodash-es';

const state = {};

export default {
  namespace: 'name',
  subscriptions: {
    setup({ dispatch, history }) {
      history.listen(({ pathname }) => {
        if (pathname === '/pathname') {
          dispatch({ type: 'reset' });
        }
      });
    },
  },
  state: cloneDeep(state),
  effects: {},
  reducers: {
    save(state, { payload }) {
      return {
        ...state,
        ...payload,
      };
    },
    reset() {
      return cloneDeep(state);
    },
  },
};
```

### antdSpace
### antdAffix
### antdBreadcrumb
### antdDropdown
### antdMenu
### antdPageHeader
### antdPagination
### antdSteps
### antdAutoComplete
### antdCascader
### antdCheckbox
### antdCheckboxAll
### antdCheckboxGroup
### antdCheckboxGroupCustom
### antdDatePicker
### antdRangePicker
### antdForm
### antdInput
### antdInputNumber
### antdRadioGroup
### antdRate
### antdSelect
### antdSlider
### antdSwitch
### antdTimePicker
### antdTreeSelect
### antdUpload
### antdAvatar
### antdBadge
### antdCalendar
### antdCard
### antdCarousel
### antdCollapse
### antdDescriptions
### antdEmpty
### antdPopover
### antdStatistic
### antdTabs
### antdTag
### antdTooltip
### antdTree
### antdAlert
### antdDrawer
### antdModal
### antdNotification
### antdPopconfirm
### antdProgress
### antdResult
### antdSkeleton
### antdSpin
### antdAnchor
### antdBackTop
### !dva
### dvaEffect
### dvaEffectQuery
### useDispatch
### useSelector
### useSelectorLoading
### dispatch

**Enjoy!**
