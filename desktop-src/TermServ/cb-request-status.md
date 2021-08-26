---
title: Перечисление CB_REQUEST_STATUS (Кбклиент. h)
description: Указывает состояние асинхронного запроса.
ms.assetid: 35FAC8EA-BA17-405F-AE10-33A816029F62
ms.tgt_platform: multiple
keywords:
- Перечисление CB_REQUEST_STATUS службы удаленных рабочих столов
topic_type:
- apiref
api_name:
- CB_REQUEST_STATUS
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6647f10ab91fd5cb1919d49c4c00d22b8b1722de9b20d9b83fdee8fcceaef95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871974"
---
# <a name="cb_request_status-enumeration"></a>\_ \_ Перечисление состояния запросов CB

Указывает состояние асинхронного запроса. Это перечисление используется с методом [**иконнектионброкеррекуест:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _CB_REQUEST_STATUS { 
  CB_STATUS_INVALID                     = 1,
  CB_STATUS_INITIATING_REQUEST          = 0,
  CB_STATUS_REQUEST_COMPLETED,
  CB_STATUS_REQUEST_FAILED,
  CB_STATUS_REQUEST_ABORTED,
  CB_STATUS_FINDING_DESTINATION,
  CB_STATUS_LOADING_DESTINATION,
  CB_STATUS_BRINGING_SESSION_ONLINE,
  CB_STATUS_REDIRECTING_TO_DESTINATION
} CB_REQUEST_STATUS;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**\_состояние CB \_ недопустимо**
</dt> <dd>

Объект запроса не инициализирован.

</dd> <dt>

<span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**\_запрос на \_ инициирование состояния CB \_**
</dt> <dd>

Не используется.

</dd> <dt>

<span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**\_запрос состояния \_ CB \_ выполнен**
</dt> <dd>

Запрос завершен.

</dd> <dt>

<span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**\_ \_ сбой запроса состояния \_ CB**
</dt> <dd>

Ошибка запроса.

</dd> <dt>

<span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**\_запрос состояния \_ CB \_ прерван**
</dt> <dd>

Запрос был прерван.

</dd> <dt>

<span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**\_состояние CB \_ Поиск \_ места назначения**
</dt> <dd>

Не используется.

</dd> <dt>

<span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**\_назначение " \_ Загрузка \_ состояния CB"**
</dt> <dd>

Не используется.

</dd> <dt>

<span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**\_состояние CB \_ перевод \_ сеанса в \_ режим «в сети»**
</dt> <dd>

Не используется.

</dd> <dt>

<span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**\_состояние CB \_ Перенаправление \_ на \_ место назначения**
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                        |
| Заголовок<br/>                   | <dl> <dt>Кбклиент. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Иконнектионброкеррекуест:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md)
</dt> </dl>

 

 





