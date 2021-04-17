---
title: Простой тип Пастипе
description: Определяет минимальное и максимальное число символов для строки, определяющей путь к файлу.
ms.assetid: 09908f75-ba7b-4e31-877e-80fabea6bd27
keywords:
- планировщик задач простого типа Пастипе
topic_type:
- apiref
api_name:
- pathType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a75ef7d85eba2aa39e0c3c768fec0908c7ea16b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682131"
---
# <a name="pathtype-simple-type"></a>Простой тип Пастипе

Определяет минимальное и максимальное число символов для строки, определяющей путь к файлу. Путь не может быть пустой строкой и должен содержать менее 260 символов.

``` syntax
<xs:simpleType name="pathType">
    <xs:restriction
        base="nonEmptyString"
    >
        <xs:maxLength
            value="260"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





