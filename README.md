# 📅 almanac-holidays

中国法定节假日数据，供 [岁记 (Almanac)](https://github.com/huangshouqing/almanac) App 远程热更新使用。

## 数据格式

每年一个 JSON 文件（如 `2026.json`），格式：

```json
{
  "year": 2026,
  "holidays": [
    {
      "name": "春节",
      "nameEn": "Spring Festival",
      "startDate": "2026-02-17",
      "endDate": "2026-02-23",
      "days": 7,
      "workdays": ["2026-02-14", "2026-02-28"]
    }
  ]
}
```

## 字段说明

| 字段 | 说明 |
|------|------|
| `name` | 节假日中文名 |
| `nameEn` | 节假日英文名 |
| `startDate` | 放假开始日期 |
| `endDate` | 放假结束日期 |
| `days` | 放假天数 |
| `workdays` | 调休上班日期列表 |

## 更新方式

每年 11-12 月国务院发布下一年放假通知后，新增对应年份 JSON 文件即可，App 会自动拉取。

## 使用

App 远程地址配置：
```
https://raw.githubusercontent.com/huangshouqing/almanac-holidays/main/{year}.json
```
