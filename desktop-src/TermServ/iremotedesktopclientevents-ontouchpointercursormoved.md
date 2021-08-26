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
ms.openlocfilehash: 4a7c6d542031ab375d7e960b82bb36ba52ea6c9ecab58764c13595871687a731
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072304"
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

 

