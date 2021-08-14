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
ms.openlocfilehash: 0e8e847e268486e58bc36bd1bcf9f454b2d8af7b7664d0372613c40c818f932f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758513"
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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Простые типы схемы планировщик задач](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





