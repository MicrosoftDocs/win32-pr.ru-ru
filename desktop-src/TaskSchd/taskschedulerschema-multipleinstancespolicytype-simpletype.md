---
title: Простой тип Мултиплеинстанцесполицитипе
description: Определяет константы политики экземпляра для элемента Мултиплеинстанцесполици (Сеттингстипе).
ms.assetid: 6e3f83b0-b71e-49c9-9c27-5a37f996746b
keywords:
- планировщик задач простого типа Мултиплеинстанцесполицитипе
topic_type:
- apiref
api_name:
- multipleInstancesPolicyType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 29a3523ef16224836ada474fb32265084453479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988870"
---
# <a name="multipleinstancespolicytype-simple-type"></a>Простой тип Мултиплеинстанцесполицитипе

Определяет константы политики экземпляра для элемента [**мултиплеинстанцесполици (сеттингстипе)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) .

``` syntax
<xs:simpleType name="multipleInstancesPolicyType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="Parallel"
         />
        <xs:enumeration
            value="Queue"
         />
        <xs:enumeration
            value="IgnoreNew"
         />
        <xs:enumeration
            value="StopExisting"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Значения перечисления

Простой тип **мултиплеинстанцесполицитипе** определяет следующие значения.



| Значение        | Описание                                                                                     |
|--------------|-------------------------------------------------------------------------------------------------|
| Параллельные     | Запускает новый экземпляр во время работы существующего экземпляра.<br/>                           |
| Очередь        | Запускает новый экземпляр Task после завершения всех остальных экземпляров задачи.<br/>      |
| игноренев    | По умолчанию. Не запускает новый экземпляр, если запущен существующий экземпляр задачи.<br/> |
| стопексистинг | Останавливает существующий экземпляр задачи перед запуском нового экземпляра.<br/>                |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Простые типы схемы планировщик задач](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





