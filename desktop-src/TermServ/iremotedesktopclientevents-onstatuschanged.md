---
title: Метод Иремотедесктопклиентевентс Онстатусчанжед (Локатионапи. h)
description: Вызывается, когда клиентский элемент управления обновил свое состояние.
ms.assetid: AAFBDC9E-C8B5-4924-AA69-82EF09996AF7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онстатусчанжед
- Службы удаленных рабочих столов метода Онстатусчанжед, интерфейс Иремотедесктопклиентевентс
- Службы удаленных рабочих столов интерфейса Иремотедесктопклиентевентс, метод Онстатусчанжед
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b17e42e75072033f952c7ef790365d6a363a5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492771"
---
# <a name="iremotedesktopclienteventsonstatuschanged-method"></a>Метод Иремотедесктопклиентевентс:: Онстатусчанжед

Вызывается, когда клиентский элемент управления обновил свое состояние.

## <a name="syntax"></a>Синтаксис


```C++
void OnStatusChanged(
   long statusCode,
   BSTR statusMessage
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*statusCode* 
</dt> <dd>

Новый код состояния.

</dd> <dt>

*statusMessage* 
</dt> <dd>

Текст сообщения о состоянии.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                           |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Локатионапи. h</dt> </dl>       |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | ДИИД \_ иремотедесктопклиентевентс определяется как 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иремотедесктопклиентевентс**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





