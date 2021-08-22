---
title: Иремотедесктопклиентевентс Онаутореконнектинг, метод
description: Вызывается, когда клиентский элемент управления пытается автоматически восстановить соединение с удаленным сеансом.
ms.assetid: 299408A9-ED14-42F4-B324-AF4C86FEDABE
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онаутореконнектинг
- Службы удаленных рабочих столов метода Онаутореконнектинг, интерфейс Иремотедесктопклиентевентс
- Службы удаленных рабочих столов интерфейса Иремотедесктопклиентевентс, метод Онаутореконнектинг
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7246b8822b3d3abed5d483f52c64eee88d67f99694bda44c5d8f72318cb2c04a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511734"
---
# <a name="iremotedesktopclienteventsonautoreconnecting-method"></a>Метод Иремотедесктопклиентевентс:: Онаутореконнектинг

Вызывается, когда клиентский элемент управления пытается автоматически восстановить соединение с удаленным сеансом.

## <a name="syntax"></a>Синтаксис


```C++
void OnAutoReconnecting(
  [in] long         disconnectReason,
  [in] long         ExtendedDisconnectReason,
  [in] BSTR         disconnectErrorMessage,
  [in] VARIANT_BOOL networkAvailable,
  [in] long         attemptCount,
  [in] long         maxAttemptCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*дисконнектреасон* \[ окне\]
</dt> <dd>

Причина события Disconnect.

</dd> <dt>

*Екстендеддисконнектреасон* \[ окне\]
</dt> <dd>

Расширенные сведения о событии Disconnect.

</dd> <dt>

*дисконнектеррормессаже* \[ окне\]
</dt> <dd>

Сообщение об ошибке для события Disconnect.

</dd> <dt>

*нетворкаваилабле* \[ окне\]
</dt> <dd>

Доступна ли сеть.

</dd> <dt>

*аттемпткаунт* \[ окне\]
</dt> <dd>

В этом случае это.

</dd> <dt>

*максаттемпткаунт* \[ окне\]
</dt> <dd>

Будет выполнено максимальное число попыток повторного подключения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                           |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                 |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | ДИИД \_ иремотедесктопклиентевентс определяется как 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иремотедесктопклиентевентс**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





