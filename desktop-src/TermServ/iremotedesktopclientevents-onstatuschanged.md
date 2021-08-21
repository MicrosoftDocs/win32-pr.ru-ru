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
ms.openlocfilehash: d08b15eb2b8112afcef6c98a841a249672df2ae3fbb7f36ceea513d53a5b0478
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351626"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                           |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Локатионапи. h</dt> </dl>       |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | ДИИД \_ иремотедесктопклиентевентс определяется как 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иремотедесктопклиентевентс**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





