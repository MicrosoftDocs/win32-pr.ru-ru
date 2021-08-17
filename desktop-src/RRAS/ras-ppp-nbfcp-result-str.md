---
title: Структура RAS_PPP_NBFCP_RESULT (Рассапи. h)
description: '\_ \_ Структура результатов RAS PPP нбфкп \_ используется для передачи результатов операции проекции PPP-протокола NetBEUI (NBF) для порта.'
ms.assetid: 670bf125-cad5-481f-89e4-858e636316bd
keywords:
- RAS структуры RAS_PPP_NBFCP_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_NBFCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e415e6aea75dcf78d19d776e4df0a6edf704db473eacf0c8ddbb366ffbf65947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789598"
---
# <a name="ras_ppp_nbfcp_result-structure"></a>\_ \_ Структура результата нбфкп PPP для RAS \_

\[структура **\_ \_ \_ результатов RAS PPP нбфкп** не поддерживается в Windows Vista.\]

Структура **\_ \_ \_ результатов RAS PPP нбфкп** используется для передачи результатов операции проекции PPP-протокола NetBEUI (NBF) для порта.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _RAS_PPP_NBFCP_RESULT {
  DWORD dwError;
  DWORD dwNetBiosError;
  CHAR  szName[NETBIOS_NAME_LEN + 1];
  WCHAR wszWksta[NETBIOS_NAME_LEN + 1];
} RAS_PPP_NBFCP_RESULT;
```



## <a name="members"></a>Члены

<dl> <dt>

**дверрор**
</dt> <dd>

Указывает результаты операции NBF "Проекция". Значение NO \_ Error указывает на успешное выполнение. в этом случае член **всзвкста** содержит имя удаленного компьютера. Если операция проекции не выполнена, **дверрор** является кодом ошибки из Winerror. h или расеррор. h.

</dd> <dt>

**двнетбиосеррор**
</dt> <dd>

Пропускать этот элемент на сервере; Он относится только к клиенту.

</dd> <dt>

**szName**
</dt> <dd>

Пропускать этот элемент на сервере; Он относится только к клиенту.

</dd> <dt>

**всзвкста**
</dt> <dd>

Строка в Юникоде, заканчивающаяся нулем и указывающая NetBIOS-имя клиентской рабочей станции RAS.

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

[**\_Порт RAS \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**\_ \_ результат проекции PPP для RAS \_**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**расадминпортжетинфо**](rasadminportgetinfo.md)
</dt> </dl>

 

 





