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
ms.openlocfilehash: 13cf70534510e1aed8def9005d0c2d1eafab2a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415229"
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
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



 

 





