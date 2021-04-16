---
title: IMsRdpDeviceV2 Искомпоситедевице, свойство
description: Указывает, является ли устройство составным.
ms.assetid: cc54f3f0-de0b-4f75-b5a1-4f061ac95ab5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Искомпоситедевице
- Службы удаленных рабочих столов свойства Искомпоситедевице, интерфейс IMsRdpDeviceV2
- Службы удаленных рабочих столов интерфейса IMsRdpDeviceV2, свойство Искомпоситедевице
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsCompositeDevice
- IMsRdpDeviceV2.get_IsCompositeDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2341544543f436272486a839ffdd3ee68a4a4478
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489111"
---
# <a name="imsrdpdevicev2iscompositedevice-property"></a>Свойство IMsRdpDeviceV2:: Искомпоситедевице

Указывает, является ли устройство составным.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_IsCompositeDevice(
  [out, retval] VARIANT_BOOL *pvboolCompositeDevice
);
```



## <a name="property-value"></a>Значение свойства

**значение true** , если устройство является составным устройством; в противном случае — **значение false**.

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

 

 





