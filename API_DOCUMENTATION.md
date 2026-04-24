# API Құқықтары және Ендпоинттері

## Ойыншылар Өндіктіліктері

### GET /api/v1/players
Барлық ойыншыларды беру

```json
{
  "players": [
    {
      "id": 1,
      "name": "Аблай Нурманов",
      "position": "Форвард",
      "number": 10,
      "birth_date": "1995-05-15",
      "nationality": "Қазақстан",
      "contract_end": "2027-06-30",
      "status": "active"
    }
  ],
  "total": 25,
  "page": 1,
  "limit": 10
}
```

### POST /api/v1/players
Жаңа ойыншы құру

### PUT /api/v1/players/{id}
Ойыншы деректерін өңдеу

### DELETE /api/v1/players/{id}
Ойыншыны өшіру (архив)

## Матчтар Өндіктіліктері

### GET /api/v1/matches
Барлық матчтарды беру

### POST /api/v1/matches
Жаңа матш құру

### PUT /api/v1/matches/{id}
Матч ақпаратын өңдеу

### GET /api/v1/matches/{id}/statistics
Матштың статистикасын беру

## Тренірілеу Өндіктіліктері

### GET /api/v1/training/schedule
Тренірілеу кестесін беру

### POST /api/v1/training/exercises
Жаңа жаттығу құру

### GET /api/v1/training/exercises
Барлық жаттығуларды беру

## Қаржы Өндіктіліктері

### GET /api/v1/finance/salaries
Жалақы деректерін беру

### POST /api/v1/finance/payments
Төлемді құру

### GET /api/v1/finance/reports
Қаржылық есептемелерді беру

---
**Қосылған**: 2026-04-24
**Версия**: v1.2
