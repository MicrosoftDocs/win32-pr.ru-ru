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
ms.openlocfilehash: 7697bc7ff1aa42569cf954b3f0b037f66ec67ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544239"
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

## <a name="remarks"></a>Комментарии

Приложение может вызвать эту функцию для завершения сеанса Miracast по любой причине. Приложению не требуется вызывать его при получении типа **дисконнектеднотификатион** в своем обратном вызове.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                    |
| Окончание поддержки клиента<br/>    | Windows 10<br/>                                                                      |
| Поддержка конца сервера<br/>    | Windows Server 2016<br/>                                                             |
| Header<br/>                   | <dl> <dt>Вфдсинк. h</dt> </dl>       |
| Библиотека<br/>                  | <dl> <dt>Вифидисплай. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ \_ обратный вызов уведомления приемника для дисплея WFD \_**](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




