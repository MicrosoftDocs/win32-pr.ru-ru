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
ms.openlocfilehash: 53ad1bde74f2d2a1649fa5fdee23ef70ab53b09d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662391"
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
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**UserLogonCred**](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Усерлогонкред (contextType)**](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




