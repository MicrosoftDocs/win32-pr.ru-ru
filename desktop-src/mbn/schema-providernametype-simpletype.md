---
description: Определяет строковый тип для элемента ProviderName в профиле мобильного широкополосного подключения.
ms.assetid: 1644ded2-f931-4920-848d-e0405d8723e3
title: Простой тип Провидернаметипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerNameType
api_type:
- Schema
ms.openlocfilehash: e0a1a0c999eebe8d4ac9922564a28f3b8abce90397fbbda3556bf7726c7355cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118744397"
---
# <a name="providernametype-simple-type"></a>Простой тип Провидернаметипе

Простой тип **провидернаметипе** определяет строковый тип для элемента [**providerName**](schema-providername-providertype-element.md) в профиле мобильного широкополосного подключения. Эта строка состоит по меньшей мере из одного символа и не длиннее 20 символов.

``` syntax
<xs:simpleType name="providerNameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="20"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



 

 




