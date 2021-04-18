---
title: Простой тип Ленгстипе
description: Определяет тип длины, используемый для указания числа байтов или символов в элементе данных переменной длины, например двоичных данных или строки ANSI или Юникод.
ms.assetid: a15e4241-cce3-4f62-bc1c-f70fb1ea5d38
keywords:
- Журнал событий простого типа Ленгстипе
topic_type:
- apiref
api_name:
- LengthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dbb0720c2e26fa73056ccffdd17392e93e491c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341205"
---
# <a name="lengthtype-simple-type"></a>Простой тип Ленгстипе

Определяет тип длины, используемый для указания числа байтов или символов в элементе данных переменной длины, например двоичных данных или строки ANSI или Юникод. Значение может быть указано в виде значения xs: Унсигнедшорт или в виде строки, ссылающейся на имя узла элемента данных, который содержит короткое значение без знака.

``` syntax
<xs:simpleType name="LengthType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





