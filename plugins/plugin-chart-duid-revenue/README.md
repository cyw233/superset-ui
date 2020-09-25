## @superset-ui/plugin-chart-duid-revenue

[![Version](https://img.shields.io/npm/v/@superset-ui/plugin-chart-duid-revenue.svg?style=flat-square)](https://img.shields.io/npm/v/@superset-ui/plugin-chart-duid-revenue.svg?style=flat-square)
[![David (path)](https://img.shields.io/david/apache-superset/superset-ui.svg?path=packages%2Fsuperset-ui-plugin-chart-duid-revenue&style=flat-square)](https://david-dm.org/apache-superset/superset-ui?path=packages/superset-ui-plugin-chart-duid-revenue)

This plugin provides DUID Revenue for Superset.

### Usage

Configure `key`, which can be any `string`, and register the plugin. This `key` will be used to lookup this chart throughout the app.

```js
import DuidRevenueChartPlugin from '@superset-ui/plugin-chart-duid-revenue';

new DuidRevenueChartPlugin()
  .configure({ key: 'duid-revenue' })
  .register();
```

Then use it via `SuperChart`. See [storybook](https://apache-superset.github.io/superset-ui/?selectedKind=plugin-chart-duid-revenue) for more details.

```js
<SuperChart
  chartType="duid-revenue"
  width={600}
  height={600}
  formData={...}
  queryData={{
    data: {...},
  }}
/>
```

### File structure generated

```
├── README.md
├── package.json
├── src
│   ├── DuidRevenue.tsx
│   ├── images
│   │   └── thumbnail.png
│   ├── index.ts
│   ├── plugin
│   │   ├── buildQuery.ts
│   │   ├── controlPanel.ts
│   │   ├── index.ts
│   │   └── transformProps.ts
│   └── types.ts
├── test
│   └── index.test.ts
└── types
    └── external.d.ts
```