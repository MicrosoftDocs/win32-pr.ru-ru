---
description: Указывает имя пользователя для входа.
ms.assetid: a312de24-2a81-4fac-9c23-4e67e171e692
title: Элемент UserName (Усерлогонкред)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UserName
api_type:
- Schema
ms.openlocfilehash: 836a2d26c5de63da754b562ce418026db44a9603a303b63bec80b2959ff9cdc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065780"
---
# <a name="username-userlogoncred-element"></a>Элемент UserName (Усерлогонкред)

Элемент **username (усерлогонкред)** указывает имя пользователя для входа.

Элемент представляет собой строку, которая не может быть длиннее 255 символов.

Этот элемент является необязательным.

``` syntax
<xs:element name="UserName"
    type="nameType"
 />
```

Элемент **username** определяется элементом [**усерлогонкред**](schema-userlogoncred-contexttype-element.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**UserLogonCred**](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Усерлогонкред (contextType)**](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




