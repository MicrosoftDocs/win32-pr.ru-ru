---
title: Структура RAS_PPP_ATCP_RESULT (Рассапи. h)
description: '\_Результирующая структура RAS PPP для сервера \_ \_ сообщает результат операции проецирования протокола AppleTalk для порта.'
ms.assetid: ac9df618-f79c-4066-a37e-f92e64e951dd
keywords:
- RAS структуры RAS_PPP_ATCP_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_ATCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa3122026613ba5012f950a98a615dbb8c9ef34133a2a24249fca545eaa2060
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789638"
---
# <a name="ras_ppp_atcp_result-structure"></a>\_ \_ \_ Результирующая структура RAS PPP

\[**\_ \_ \_ результирующая структура RAS PPP** не поддерживается для Windows Vista.\]

**\_ \_ \_ Результирующая структура RAS PPP для сервера** сообщает результат операции проецирования протокола AppleTalk для порта.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _RAS_PPP_ATCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_ATADDRESSLEN + 1];
} RAS_PPP_ATCP_RESULT;
```



## <a name="members"></a>Члены

<dl> <dt>

**дверрор**
</dt> <dd>

Задает значение, указывающее результаты операции с проекцией AppleTalk. Значение NO \_ Error указывает на успешное выполнение, в этом случае член **всзаддресс** является допустимым. Если операция проекции не выполнена, **дверрор** является кодом ошибки из Winerror. h или расеррор. h.

</dd> <dt>

**всзаддресс**
</dt> <dd>

Указывает строку в Юникоде, завершающуюся нулем, которая указывает IP-адрес, назначенный удаленному клиенту.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                       |
| Заголовок<br/>                   | <dl> <dt>Рассапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Обзор службы удаленного доступа (RAS)](about-remote-access-service.md)
</dt> <dt>

[Структуры администрирования сервера RAS](ras-server-administration-structures.md)
</dt> <dt>

[**\_ \_ результат проекции PPP для RAS \_**](ras-ppp-projection-result-str.md)
</dt> </dl>

 

 





