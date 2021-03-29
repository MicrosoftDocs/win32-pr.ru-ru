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
ms.openlocfilehash: 3741972fdd81887713e75ed5b596e0ba1a10fd3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414752"
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

 

 





