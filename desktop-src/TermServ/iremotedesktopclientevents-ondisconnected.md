---
title: Метод Иремотедесктопклиентевентс с отключением
description: Вызывается, когда клиентский элемент управления был отключен от удаленного сеанса.
ms.assetid: EA26B530-0AA8-49D6-8E3C-E53179FC5104
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода OnDisconnection
- Службы удаленных рабочих столов метода ondisconnectо, интерфейс Иремотедесктопклиентевентс
- Интерфейс Иремотедесктопклиентевентс службы удаленных рабочих столов, отключенный метод
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd59b03fe9cb23309d53773289291c8a791935a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802938"
---
# <a name="iremotedesktopclienteventsondisconnected-method"></a>Иремотедесктопклиентевентс:: ondisconnectный метод

Вызывается, когда клиентский элемент управления был отключен от удаленного сеанса.

## <a name="syntax"></a>Синтаксис


```C++
void OnDisconnected(
  [in] long disconnectReason,
  [in] long ExtendedDisconnectReason,
  [in] BSTR disconnectErrorMessage
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

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                           |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                 |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | ДИИД \_ иремотедесктопклиентевентс определяется как 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иремотедесктопклиентевентс**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





