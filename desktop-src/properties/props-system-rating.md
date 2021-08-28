---
description: Система оценок, использующая целочисленные значения от 1 до 99. это система оценки, используемая оболочкой Windows Vista.
ms.assetid: a6288d29-1ef3-4da1-bd30-577336ab6817
title: System. Оценка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adc62e69ced0f82426f19badb1aebef0453084a9b951b749aed256aa64820a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119598134"
---
# <a name="systemrating"></a>System. Оценка

Система оценок, использующая целочисленные значения от 1 до 99. это система оценки, используемая оболочкой Windows Vista.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Rating
   shellPKey = PKEY_Rating
   formatID = 64440492-4C8B-11D1-8B70-080036B11A03
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = OneStar
            minValue = 1
            setValue = 1
            defineMaxValue = 12
            text = 1 Star
            defineToken = RATING_ONE_STAR
         enumRange
            name = TwoStars
            minValue = 13
            setValue = 25
            defineMaxValue = 37
            text = 2 Stars
            defineToken = RATING_TWO_STARS
         enumRange
            name = ThreeStars
            minValue = 38
            setValue = 50
            defineMaxValue = 62
            text = 3 Stars
            defineToken = RATING_THREE_STARS
         enumRange
            name = FourStars
            minValue = 63
            setValue = 75
            defineMaxValue = 87
            text = 4 Stars
            defineToken = RATING_FOUR_STARS
         enumRange
            name = FiveStars
            minValue = 88
            setValue = 99
            defineMaxValue = 99
            text = 5 Stars
            defineToken = RATING_FIVE_STARS
         enumRange
            name
            minValue = 100
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Rating
   shellPKey = PKEY_Rating
   formatID = 64440492-4C8B-11D1-8B70-080036B11A03
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            defineMinName = RATING_UNRATED_MIN
            setValue = 0
            defineSetName = RATING_UNRATED_SET
            defineMaxValue = 0
            defineMaxName = RATING_UNRATED_MAX
            text = Unrated
         enumRange
            minValue = 1
            defineMinName = RATING_ONE_STAR_MIN
            setValue = 1
            defineSetName = RATING_ONE_STAR_SET
            defineMaxValue = 12
            defineMaxName = RATING_ONE_STAR_MAX
            text = 1 Star
         enumRange
            minValue = 13
            defineMinName = RATING_TWO_STARS_MIN
            setValue = 25
            defineSetName = RATING_TWO_STARS_SET
            defineMaxValue = 37
            defineMaxName = RATING_TWO_STARS_MAX
            text = 2 Stars
         enumRange
            minValue = 38
            defineMinName = RATING_THREE_STARS_MIN
            setValue = 50
            defineSetName = RATING_THREE_STARS_SET
            defineMaxValue = 62
            defineMaxName = RATING_THREE_STARS_MAX
            text = 3 Stars
         enumRange
            minValue = 63
            defineMinName = RATING_FOUR_STARS_MIN
            setValue = 75
            defineSetName = RATING_FOUR_STARS_SET
            defineMaxValue = 87
            defineMaxName = RATING_FOUR_STARS_MAX
            text = 4 Stars
         enumRange
            minValue = 88
            defineMinName = RATING_FIVE_STARS_MIN
            setValue = 99
            defineSetName = RATING_FIVE_STARS_SET
            defineMaxValue = 99
            defineMaxName = RATING_FIVE_STARS_MAX
            text = 5 Stars
         enumRange
            minValue = 100
```

## <a name="remarks"></a>Remarks

Значения PKEY определены в списке PKEY. h.

Сведения о совместимости с системами оценок, которые используют значения от 1 до 5, см. в свойстве [System. симплератинг](./props-system-simplerating.md). однако обратите внимание, что System. симплератинг не используется в оболочке Windows Vista.

В следующей таблице описывается, что означает система оценки, используемая в пользовательском интерфейсе оболочки, в терминах значения [System. рейтингов]() .



| System. Оценка | Оценка |
|---------------|-------------|
| 1–12          | 1 звезда      |
| 13-37         | 2 звезды     |
| 38-62         | 3 звезды     |
| 63-87         | 4 звезды     |
| 88-99         | 5 звезд     |



 

Когда пользователь рассчитывает элемент, выбрав значение рейтинга "звезда" в пользовательском интерфейсе, фактические значения [System. рейтинга]() присваиваются, как показано в следующей таблице:



| Оценка | Значение, назначенное через пользовательский интерфейс |
|-------------|---------------------------|
| 1 звезда      | 1                         |
| 2 звезды     | 25                        |
| 3 звезды     | 50                        |
| 4 звезды     | 75                        |
| 5 звезд     | 99                        |



 

Если файл имеет значение [System. симплератинг](./props-system-simplerating.md) , а не значение [System. рейтингов]() , используйте приведенную ниже таблицу для преобразования и указания значений для System. рейтингов.



| System. Симплератинг | System. Оценка |
|---------------------|---------------|
| 1                   | 1             |
| 2                   | 25            |
| 3                   | 50            |
| 4                   | 75            |
| 5                   | 99            |



 

Если в файле имеются сохраненные значения [System. Оценка]() и [System. симплератинг](./props-system-simplerating.md) , всегда используйте значение System. рейтингов при запросе непосредственно, без ссылки на System. симплератинг.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[пропертидескриптион](./propdesc-schema-propertydescription.md)
</dt> <dt>

[сеарчинфо](./propdesc-schema-searchinfo.md)
</dt> <dt>

[лабелинфо](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[булеанформат](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[енумератедлист](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[дравконтрол](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[едитконтрол](./propdesc-schema-editcontrol.md)
</dt> <dt>

[филтерконтрол](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[куериконтрол](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
