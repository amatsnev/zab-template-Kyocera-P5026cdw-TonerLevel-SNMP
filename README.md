# Zabbix Template: Kyocera ECOSYS P5026cdw Toner Level (SNMP)

Шаблон Zabbix для мониторинга уровней тонеров принтера **Kyocera ECOSYS P5026cdw** по SNMP.

## Возможности

- Мониторинг уровня тонера:
  - Black
  - Cyan
  - Magenta
  - Yellow
- Триггеры по порогам:
  - Предупреждение (`{$TONER_LEVEL_WARNING}` – по умолчанию 15%)
  - Ошибка (`{$TONER_LEVEL_ERROR}` – по умолчанию 5%)
- Элемент для контроля уровня контейнера с отработанным тонером

## Требования

- Zabbix 6.0+
- Включённый и настроенный SNMP на принтере
- SNMP community/credentials, настроенные в хосте Zabbix

## Установка

1. Импортируйте файл шаблона в Zabbix (`Configuration → Templates → Import`).
2. Привяжите шаблон к хосту с принтером.
3. При необходимости откорректируйте макросы:
   - `{$TONER_LEVEL_WARNING}`
   - `{$TONER_LEVEL_ERROR}`

## Примечания

- Интервал опроса по умолчанию: 30 минут для тонеров.
- Значения приводятся к процентам через препроцессинг (MULTIPLIER).
