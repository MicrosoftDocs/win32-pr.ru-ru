---
title: Имсрдпдевицеколлектион Девицебиндекс, свойство
description: Извлекает устройство по указанному индексу.
ms.assetid: fcfc459b-46e1-4f26-a331-745fcf06638b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Девицебиндекс
- Службы удаленных рабочих столов свойства Девицебиндекс, интерфейс Имсрдпдевицеколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпдевицеколлектион, свойство Девицебиндекс
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceByIndex
- IMsRdpDeviceCollection.get_DeviceByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12d763d4c147efa26e904a1903149504ee557ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493173"
---
# <a name="imsrdpdevicecollectiondevicebyindex-property"></a>Имсрдпдевицеколлектион: свойство Евицебиндекс:D

Извлекает устройство по указанному индексу.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_DeviceByIndex(
  [in]          ULONG index,
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

 

 





