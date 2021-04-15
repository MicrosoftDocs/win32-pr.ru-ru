---
description: Поле типа в записи управления доступом (ACE), которое определяет, является ли ACE записью ACE, которая разрешает доступ или запрещает доступ.
ms.assetid: a78c72f7-0bc0-4bda-9012-4abe45342d8d
ms.tgt_platform: multiple
title: Константы типа ACE пространства имен (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Allow
- Deny
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 0c9f1f7e05f663782c0d748ddb296ca36ecbe29c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648999"
---
# <a name="namespace-ace-type-constants"></a>Константы типа ACE пространства имен

Поле **типа** в записи управления доступом (ACE), которое определяет, является ли ACE записью ACE, которая разрешает доступ или запрещает доступ.

<dl> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Возможность**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



ACE разрешает доступ к пространству имен.


</dt> </dl> </dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>**Deny**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



ACE запрещает доступ к пространству имен.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Файл Winnt. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы безопасности WMI](wmi-security-constants.md)
</dt> <dt>

[Настройка дескрипторов безопасности Намепаце](setting-namespace-security-descriptors.md)
</dt> <dt>

[Установка наследования безопасности пространства имен](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[**\_\_системсекурити**](--systemsecurity.md)
</dt> </dl>

 

 




