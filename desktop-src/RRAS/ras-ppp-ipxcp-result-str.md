---
title: Структура RAS_PPP_IPXCP_RESULT (Рассапи. h)
description: '\_Структура результатов «RAS PPP \_ IPXCP» \_ используется для передачи результатов операции проецирования объединенной сети PPP (IPX) для порта.'
ms.assetid: e1236e1b-f0ef-46cf-a12f-35529215752c
keywords:
- RAS структуры RAS_PPP_IPXCP_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_IPXCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb7ca4d006bd1a1df5a645799998b463c0b14f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071700"
---
# <a name="ras_ppp_ipxcp_result-structure"></a>\_ \_ Структура результатов PPP для RAS РРР \_

\[**\_ \_ \_ Результирующая структура RAS PPP IPXCP** не поддерживается в Windows Vista.\]

Структура **результатов «RAS \_ PPP \_ IPXCP \_** » используется для передачи результатов операции проецирования объединенной сети PPP (IPX) для порта.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _RAS_PPP_IPXCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPXADDRESSLEN + 1];
} RAS_PPP_IPXCP_RESULT;
```



## <a name="members"></a>Члены

<dl> <dt>

**дверрор**
</dt> <dd>

Указывает результаты операции IPX-проекции. Значение NO \_ Error указывает на успешное выполнение, в этом случае член **всзаддресс** является допустимым. Если операция проекции не выполнена, **дверрор** является кодом ошибки из Winerror. h или расеррор. h.

</dd> <dt>

**всзаддресс**
</dt> <dd>

Строка в Юникоде, заканчивающаяся нулем и указывающая IPX-адрес, назначенный удаленному клиенту. Эта строка содержит * NET ***.** Форма _узла_ .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Рассапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Обзор службы удаленного доступа (RAS)](about-remote-access-service.md)
</dt> <dt>

[Структуры администрирования сервера RAS](ras-server-administration-structures.md)
</dt> <dt>

[**\_Порт RAS \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**\_ \_ результат проекции PPP для RAS \_**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**расадминпортжетинфо**](rasadminportgetinfo.md)
</dt> </dl>

 

 





