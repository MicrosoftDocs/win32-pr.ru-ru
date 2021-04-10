---
description: Определяет строковый тип для элемента Иконфилепас в профиле мобильного широкополосного подключения.
ms.assetid: 053bc5b8-fab2-4abe-97f8-ed98aea880b1
title: Простой тип Иконфилетипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- iconFileType
api_type:
- Schema
ms.openlocfilehash: 168c2709f8b3049270711e286a35fbbd11e1ffef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144797"
---
# <a name="iconfiletype-simple-type"></a>Простой тип Иконфилетипе

Простой тип **иконфилетипе** определяет строковый тип для элемента [**иконфилепас**](schema-iconfilepath-mbnprofile-element.md) в профиле мобильного широкополосного подключения. Эта строка состоит по меньшей мере из одного символа и не длиннее 1024 символов.

``` syntax
<xs:simpleType name="iconFileType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="1024"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



 

 




