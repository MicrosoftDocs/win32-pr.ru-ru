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
ms.openlocfilehash: 289e91b3d7139001bfab22c81bfb0f9e9871033f6296286373c5bde18fdc366d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758383"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





