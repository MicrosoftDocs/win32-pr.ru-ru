---
title: IMsRdpClient9 attachEvent, метод
description: Присоединяет событие.
ms.assetid: 3a887aeb-a74f-4477-8cf3-8ac43a31fa26
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода attachEvent
- службы удаленных рабочих столов метода attachEvent, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод attachEvent
- службы удаленных рабочих столов метода attachEvent, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, метод attachEvent
topic_type:
- apiref
api_name:
- IMsRdpClient9.attachEvent
- IMsRdpClient10.attachEvent
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1bd3fd518fba825c209a4170e6b314a7b774a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489135"
---
# <a name="imsrdpclient9attachevent-method"></a>Метод IMsRdpClient9:: attachEvent

Присоединяет событие.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT attachEvent(
  [in] BSTR      eventName,
  [in] IDispatch *callback
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*EventName* \[ окне\]
</dt> <dd>

Событие для присоединения.

</dd> <dt>

*обратный вызов* \[ окне\]
</dt> <dd>

Обратный вызов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                                                                                                                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                                                                                                                                                                                       |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                  |
| IID<br/>                      | \_MSRDPCLIENT9 CLSID определен как 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> \_MSRDPCLIENT9NOTSAFEFORSCRIPTING CLSID определен как 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> IID \_ IMsRdpClient9 определен как 28904001-04B6-436C-A55B-0AF1A0883DC9<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> </dl>

 

 





