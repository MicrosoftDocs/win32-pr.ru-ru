---
description: Определяет функцию обратного вызова&\# 8212;, которая реализуется в приложении&\# 8212;, которое было указано в функции вфдстартдисплайсинк.
ms.assetid: 0D4C00FD-4ED6-4F0F-BB72-0A1FCC05DB37
title: Функция обратного вызова WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK (Вфдсинк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK
api_type:
- UserDefined
api_location:
- wfdsink.h
ms.openlocfilehash: c576f88a5b7f97484647c4c06f44522a5c3c379f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663037"
---
# <a name="wfd_display_sink_notification_callback-callback-function"></a>\_ \_ \_ Функция обратного вызова для уведомлений о приемнике для дисплея WFD \_

Функция **\_ \_ \_ \_ обратного вызова уведомления о приемнике WFD дисплея** определяет функцию обратного вызова, которая реализуется в приложении, которая была указана для функции [**вфдстартдисплайсинк**](wfdstartdisplaysink.md) .

## <a name="syntax"></a>Синтаксис


```C++
DWORD CALLBACK WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK(
  _In_opt_          PVOID                                 pvContext,
  _In_        const PWFD_DISPLAY_SINK_NOTIFICATION        pNotification,
  _Inout_opt_       PWFD_DISPLAY_SINK_NOTIFICATION_RESULT pNotificationResult
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвконтекст* \[ в необязательное\]
</dt> <dd>

Необязательный указатель контекста, передаваемый функции обратного вызова.

</dd> <dt>

*пнотификатион* \[ окне\]
</dt> <dd>

Указатель на структуру, содержащую данные уведомления о приемнике экрана.

</dd> <dt>

*пнотификатионресулт* \[ в, out, необязательно\]
</dt> <dd>

Указатель на структуру, содержащую данные, которые могут быть заданы приложением для указания результата обработки уведомления о приемнике отображения.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                         |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                              |
| Header<br/>                   | <dl> <dt>Вфдсинк. h</dt> </dl> |



 

 




