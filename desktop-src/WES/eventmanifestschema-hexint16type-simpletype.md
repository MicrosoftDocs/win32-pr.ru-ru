---
title: Простой тип UInt16Type
description: Определяет короткий тип без знака.
ms.assetid: 2200bb14-8f38-43fd-aed3-2a6b3ac33ed5
keywords:
- Журнал событий простого типа UInt16Type
topic_type:
- apiref
api_name:
- UInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3398b0ad92724c8b7f415bd85e8101d7c74cc6a9391e1f95349f6ef629dff0c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343733"
---
# <a name="uint16type-simple-type"></a>Простой тип UInt16Type

Определяет короткий тип без знака. Значение может быть задано в виде 2-байтового целого или шестнадцатеричного значения в диапазоне от 0 до 65 535.

``` syntax
<xs:simpleType name="UInt16Type">
    <xs:union
        memberValues="unsignedShort HexInt16Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





