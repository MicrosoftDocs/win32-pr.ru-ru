---
description: Определяет тип, используемый для указания допустимых значений цвета определенных элементов в XML-файле журнала.
ms.assetid: 10a19f28-d0aa-4126-b3f5-fde35fc5fdb0
title: Простой тип Колортипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ColorType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 883c34f42f8d31f3581599445b398b93676d416b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701352"
---
# <a name="colortype-simple-type"></a>Простой тип Колортипе

Определяет тип, используемый для указания допустимых значений цвета определенных элементов в XML-файле журнала.

``` syntax
<xs:simpleType name="ColorType">
    <xs:restriction
        base="string"
     />
</xs:simpleType>
```

## <a name="remarks"></a>Комментарии

Цвет может быть шестнадцатеричным значением RGB в формате \# RRGGBB. Оно должно соответствовать следующему регулярному выражению: \# \[ 0-9a-fA-F \] {6} . Например: " \# 4a79B5".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                     |



 

 




