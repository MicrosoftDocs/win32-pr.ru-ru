---
title: Сложный тип Идлетригжертипе
description: Определяет базовый тип для элемента Идлетригжер.
ms.assetid: 05beabb7-2e6f-4df1-809a-9f64a578d80a
keywords:
- планировщик задач сложного типа Идлетригжертипе
topic_type:
- apiref
api_name:
- idleTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a5c1ae0c6a88576eb7996a8151e96bb92c4a47c0d732a3558deede3b835356f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100024"
---
# <a name="idletriggertype-complex-type"></a>Сложный тип Идлетригжертипе

Определяет базовый тип для элемента [**идлетригжер**](taskschedulerschema-idletrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="idleTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
         />
    </xs:complexContent>
</xs:complexType>
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[планировщик задач сложные типы схемы](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





