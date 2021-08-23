---
description: Очищает состояние открываемого сеанса или текущего открытого сеанса.
ms.assetid: 8247AFA9-F471-4CCD-972D-D0C827E86880
title: Функция Вфддисплайсинкклосесессион (Вфдсинк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDCloseDisplaySinkSession
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 7e8169c541535eb2c5adfd0959da47cee4951750687f7d926798534ddc7cbf88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064904"
---
# <a name="wfddisplaysinkclosesession-function"></a>Функция Вфддисплайсинкклосесессион

Очищает состояние открываемого сеанса или текущего открытого сеанса.

## <a name="syntax"></a>Синтаксис


```C++
DWORD WINAPI WFDCloseDisplaySinkSession(
  _In_ HANDLE hSessionHandle
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хсессионхандле* \[ окне\]
</dt> <dd>

Маркер, полученный по последнему вызову [**\_ \_ \_ \_ обратного вызова уведомления приемника WFD**](wfd-display-sink-notification-callback.md) , который включал в себя один.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, возвращается значение ошибки \_ Success.

## <a name="remarks"></a>Remarks

приложение может вызвать эту функцию, чтобы завершить сеанс Miracast по любой причине. Приложению не требуется вызывать его при получении типа **дисконнектеднотификатион** в своем обратном вызове.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                    |
| Окончание поддержки клиента<br/>    | Windows 10,<br/>                                                                      |
| Поддержка конца сервера<br/>    | Windows Server 2016<br/>                                                             |
| Header<br/>                   | <dl> <dt>Вфдсинк. h</dt> </dl>       |
| Библиотека<br/>                  | <dl> <dt>Вифидисплай. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ \_ обратный вызов уведомления приемника для дисплея WFD \_**](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




