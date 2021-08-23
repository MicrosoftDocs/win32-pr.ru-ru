---
title: Простой тип UInt8Type
description: Определяет тип Byte без знака.
ms.assetid: bda12d06-683f-4183-a84b-2bc3159c4eff
keywords:
- Журнал событий простого типа UInt8Type
topic_type:
- apiref
api_name:
- UInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81a48c21e34edecbf4dfb4f9c2e87c85a77e3f500ec42b8607f1de004e7679ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511314"
---
# <a name="uint8type-simple-type"></a>Простой тип UInt8Type

Определяет тип Byte без знака. Значение может быть указано в виде 1-байтового целого или шестнадцатеричного значения в диапазоне от 0 до 255.

``` syntax
<xs:simpleType name="UInt8Type">
    <xs:union
        memberValues="unsignedByte HexInt8Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





