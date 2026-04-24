# Ішінара Деректер Модельі

## Ойыншы (Player)
```
Player {
  id: UUID
  name: String (қажетті)
  position: Enum [Қорғаушы, Орта, Форвард]
  shirt_number: Integer (1-99)
  birth_date: Date
  nationality: String
  height: Float (см)
  weight: Float (кг)
  contract_start: Date
  contract_end: Date
  salary: Decimal
  status: Enum [active, injured, suspended, transferred]
  created_at: Timestamp
  updated_at: Timestamp
}
```

## Матш (Match)
```
Match {
  id: UUID
  home_team: String
  away_team: String
  date: DateTime (қажетті)
  location: String
  referee: String
  home_score: Integer
  away_score: Integer
  status: Enum [scheduled, in_progress, completed, cancelled]
  attendance: Integer
  created_at: Timestamp
  updated_at: Timestamp
}
```

## Матш Статистикасы (Match Statistics)
```
MatchStatistics {
  id: UUID
  match_id: UUID (FK)
  player_id: UUID (FK)
  goals: Integer
  assists: Integer
  yellow_cards: Integer
  red_cards: Integer
  passes: Integer
  pass_accuracy: Float
  shots_on_target: Integer
  tackles: Integer
  interceptions: Integer
  created_at: Timestamp
}
```

## Тренірілеу Сәтсебісі (Training Session)
```
TrainingSession {
  id: UUID
  date: DateTime (қажетті)
  duration: Integer (минут)
  location: String
  coach_id: UUID (FK)
  participants: Array[UUID]
  exercises: Array[Exercise]
  intensity: Enum [low, medium, high]
  notes: Text
  created_at: Timestamp
  updated_at: Timestamp
}
```

## Жаттығу (Exercise)
```
Exercise {
  id: UUID
  name: String (қажетті)
  description: Text
  duration: Integer (минут)
  difficulty: Enum [beginner, intermediate, advanced]
  category: String
  video_url: String (optional)
  created_at: Timestamp
  updated_at: Timestamp
}
```

## Төлем (Payment)
```
Payment {
  id: UUID
  player_id: UUID (FK)
  amount: Decimal (қажетті)
  payment_date: Date (қажетті)
  payment_type: Enum [salary, bonus, transfer_fee, other]
  status: Enum [pending, completed, failed, cancelled]
  description: Text
  created_at: Timestamp
  updated_at: Timestamp
}
```

## Пайдаланушы (User)
```
User {
  id: UUID
  email: String (уникалды, қажетті)
  password: String (хешталған)
  first_name: String
  last_name: String
  role: Enum [admin, coach, medical_staff, accountant, player, viewer]
  phone: String
  is_active: Boolean
  created_at: Timestamp
  updated_at: Timestamp
  last_login: DateTime
}
```

---
**Құрылған**: 2026-04-24
**Версия**: v1.2
