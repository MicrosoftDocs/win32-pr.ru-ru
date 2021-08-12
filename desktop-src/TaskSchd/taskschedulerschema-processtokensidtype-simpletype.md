---
title: Простой тип Процесстокенсидтипе
description: Определяет возможные значения для элемента Процесстокенсидтипе (ПринЦипалтипе).
ms.assetid: 9db3e113-c525-4cbf-88c2-be256d641e92
keywords:
- планировщик задач простого типа Процесстокенсидтипе
topic_type:
- apiref
api_name:
- processTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 505f8abe340af36c25792ec97a5a465a166eedb74921c800d2a568d10a5cce0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611906"
---
# <a name="processtokensidtype-simple-type"></a>Простой тип Процесстокенсидтипе

Определяет возможные значения для элемента [**процесстокенсидтипе (принЦипалтипе)**](taskschedulerschema-processtokensidtype-principaltype-element.md) .

``` syntax
<xs:simpleType name="processTokenSidType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="None"
         />
        <xs:enumeration
            value="Unrestricted"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Значения перечисления

Простой тип **процесстокенсидтипе** определяет следующие значения.



| Значение        | Описание                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Нет         | Задачи выполняются в процессе, который не содержит идентификатор безопасности токена процесса (изменения в списке групп токенов процессов не вносятся).<br/> |
| С неограниченным доступом | Идентификатор безопасности задачи будет производным от полного пути задачи и будет добавлен в список групп токенов процесса.<br/>                           |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



 

 





