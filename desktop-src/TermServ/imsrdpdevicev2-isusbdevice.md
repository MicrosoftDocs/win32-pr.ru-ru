---
title: IMsRdpDeviceV2 Исусбдевице, свойство
description: Указывает, что устройство предназначено для перенаправления USB.
ms.assetid: df4c9764-ad96-4f35-9537-3890293a944c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Исусбдевице
- Службы удаленных рабочих столов свойства Исусбдевице, интерфейс IMsRdpDeviceV2
- Службы удаленных рабочих столов интерфейса IMsRdpDeviceV2, свойство Исусбдевице
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsUSBDevice
- IMsRdpDeviceV2.get_IsUSBDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e03e2572912487cb924f65350dbdd7818d07d2a7b172d18cb28fab87335a00dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138567"
---
# <a name="imsrdpdevicev2isusbdevice-property"></a>Свойство IMsRdpDeviceV2:: Исусбдевице

Указывает, что устройство предназначено для перенаправления USB.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_IsUSBDevice(
  [out, retval] VARIANT_BOOL *pvboolUSBDevice
);
```



## <a name="property-value"></a>Значение свойства

**значение true** , если устройство предназначено для перенаправления USB; в противном случае — **значение false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7 с пакетом обновления 1 (SP1)<br/>                                                          |
| Минимальная версия сервера<br/> | Windows Server 2008 R2 с пакетом обновления 1 (SP1)<br/>                                             |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 определен как 5fb94466-7661-42a8-98b7-01904c11668f<br/>      |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpDeviceV2**](imsrdpdevicev2.md)
</dt> </dl>

 

 





