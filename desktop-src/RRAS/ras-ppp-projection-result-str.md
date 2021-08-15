---
title: Структура RAS_PPP_PROJECTION_RESULT (Рассапи. h)
description: '\_ \_ Структура результата проекции PPP для RAS \_ используется для передачи результатов различных операций проекции PPP для порта.'
ms.assetid: 061b1b51-4b6f-4127-8ee5-8a1913a2aa99
keywords:
- RAS структуры RAS_PPP_PROJECTION_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_PROJECTION_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce1bb82b34490f8a1f3734225cbde1e761c575a2019a30db7790bfc7fa3c169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789588"
---
# <a name="ras_ppp_projection_result-structure"></a>\_ \_ Структура результата проекции PPP для RAS \_

\[структура **\_ \_ \_ результата проекции PPP для RAS** не поддерживается Windows Vista.\]

Структура **\_ \_ \_ результата проекции PPP для RAS** используется для передачи результатов различных операций проекции PPP для порта.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _RAS_PPP_PROJECTION_RESULT {
  RAS_PPP_NBFCP_RESULT nbf;
  RAS_PPP_IPCP_RESULT  ip;
  RAS_PPP_IPXCP_RESULT ipx;
  RAS_PPP_ATCP_RESULT  at;
} RAS_PPP_PROJECTION_RESULT;
```



## <a name="members"></a>Члены

<dl> <dt>

**nbf**
</dt> <dd>

Структура [**\_ \_ \_ результата нбфкп для RAS PPP**](ras-ppp-nbfcp-result-str.md) , которая сообщает результат операции проекции PPP NetBEUI (NBF).

</dd> <dt>

**см**
</dt> <dd>

[**\_ \_ \_ Результирующая структура RAS PPP РРР**](ras-ppp-ipcp-result-str.md) , которая сообщает результат операции проекции протокола IP PPP.

</dd> <dt>

**пользу**
</dt> <dd>

структура [**\_ \_ \_ результата ppp ррр**](ras-ppp-ipxcp-result-str.md) , которая сообщает о результате операции проекции IPX-Exchange пакетов ppp.

</dd> <dt>

**at**
</dt> <dd>

[**\_ \_ \_ Результирующая структура RAS PPP**](ras-ppp-atcp-result-str.md) .

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура сообщает результаты проекции для протоколов NetBEUI, TCP/IP и IPX. Каждая структура PPP имеет элемент **дверрор** , который указывает, является ли действительная информация в структуре допустимой. Если **дверрор** не является \_ ошибкой, другие сведения являются допустимыми. Если **дверрор** является одним из кодов ошибок в файле Winerror. h или расеррор. h, другие сведения являются недопустимыми.

## <a name="requirements"></a>Requirements (Требования)



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

[**\_результат RAS \_ PPP \_**](ras-ppp-atcp-result-str.md)
</dt> <dt>

[**\_результат RAS \_ PPP \_**](ras-ppp-ipcp-result-str.md)
</dt> <dt>

[**\_результат PPP \_ для удаленного доступа \_**](ras-ppp-ipxcp-result-str.md)
</dt> <dt>

[**\_ \_ результат нбфкп PPP для RAS \_**](ras-ppp-nbfcp-result-str.md)
</dt> <dt>

[**расадминпортжетинфо**](rasadminportgetinfo.md)
</dt> </dl>

 

 





