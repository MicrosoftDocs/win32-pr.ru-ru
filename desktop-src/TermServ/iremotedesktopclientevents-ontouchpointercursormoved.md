---
title: Иремотедесктопклиентевентс Онтаучпоинтеркурсормовед, метод
description: Вызывается, когда курсор сенсорного указателя переместился и свойство Евентсенаблед имеет значение true.
ms.assetid: 55A6AC99-0723-4215-9428-D2DAAC77A74A
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онтаучпоинтеркурсормовед
- Службы удаленных рабочих столов метода Онтаучпоинтеркурсормовед, интерфейс Иремотедесктопклиентевентс
- Службы удаленных рабочих столов интерфейса Иремотедесктопклиентевентс, метод Онтаучпоинтеркурсормовед
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnTouchPointerCursorMoved
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae347e19942bf0c82112e5cec6a3fb4fe131349f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672663"
---
# <a name="iremotedesktopclienteventsontouchpointercursormoved-method"></a>Метод Иремотедесктопклиентевентс:: Онтаучпоинтеркурсормовед

Вызывается, когда курсор сенсорного указателя переместился и свойство [**евентсенаблед**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) имеет значение true.

## <a name="syntax"></a>Синтаксис


```C++
void OnTouchPointerCursorMoved(
  [in] long x,
  [in] long y
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*x* \[ в\]
</dt> <dd></dd> <dt>

*y* \[ в\]
</dt> <dd></dd> </dl>

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

 

