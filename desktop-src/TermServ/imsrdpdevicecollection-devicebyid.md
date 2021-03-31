---
title: Имсрдпдевицеколлектион Девицебид, свойство
description: Извлекает устройство с указанным идентификатором.
ms.assetid: b64e83fa-5a94-4080-8efa-45cbfe5ceb88
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Девицебид
- Службы удаленных рабочих столов свойства Девицебид, интерфейс Имсрдпдевицеколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпдевицеколлектион, свойство Девицебид
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceById
- IMsRdpDeviceCollection.get_DeviceById
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 228e3c7cf03457ca740d4a415257008988215077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490341"
---
# <a name="imsrdpdevicecollectiondevicebyid-property"></a>Имсрдпдевицеколлектион: свойство Евицебид:D

Извлекает устройство с указанным идентификатором.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_DeviceById(
  [in]          BSTR devInstanceId,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a>Значение свойства

Указатель интерфейса [**имсрдпдевице**](imsrdpdevice.md) .

## <a name="error-codes"></a>Коды ошибок

Если метод выполнен успешно, возвращается значение **S \_ OK** . Любое другое значение **HRESULT** указывает на сбой вызова.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                            |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ имсрдпдевицеколлектион определен как 56540617-d281-488c-8738-6a8fdf64a118<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпдевицеколлектион**](imsrdpdevicecollection.md)
</dt> </dl>

 

 





