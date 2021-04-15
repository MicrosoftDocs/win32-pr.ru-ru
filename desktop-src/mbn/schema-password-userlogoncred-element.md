---
description: Указывает пароль, используемый для проверки подлинности пользователя.
ms.assetid: 9c02413b-a4c7-4c1f-a150-e27cc125faf6
title: Password (Усерлогонкред), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Password
api_type:
- Schema
ms.openlocfilehash: b05e34bcbaa91aba5cbfbd14f2bc8534aa91dd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662397"
---
# <a name="password-userlogoncred-element"></a>Password (Усерлогонкред), элемент

Элемент [**Password (усерлогонкред)**](schema-ignorepassword-userlogoncred-element.md) указывает пароль, используемый для проверки подлинности пользователя.

Элемент представляет собой строку длиной до 255 символов.

Этот элемент является необязательным.

``` syntax
<xs:element name="Password"
    type="string"
 />
```

Элемент **Password** определяется элементом [**усерлогонкред**](schema-userlogoncred-contexttype-element.md) .

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

 

 




