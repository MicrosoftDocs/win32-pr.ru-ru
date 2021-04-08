---
title: Свойство Девицестринг Ивмусбдевице (Впккоминтерфацес. h)
description: Возвращает имя USB-устройства.
ms.assetid: 2ae82e2a-b33a-4039-acdb-958b094b1045
keywords:
- Девицестринг свойство Virtual PC
- Девицестринг свойство Virtual PC, интерфейс Ивмусбдевице
- Ивмусбдевице интерфейс Virtual PC, свойство Девицестринг
topic_type:
- apiref
api_name:
- IVMUSBDevice.DeviceString
- IVMUSBDevice.get_DeviceString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ed76f55f5b1218db70991f5917edf6d5b7b655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892041"
---
# <a name="ivmusbdevicedevicestring-property"></a>Ивмусбдевице: свойство Евицестринг:D

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Возвращает имя USB-устройства.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_DeviceString(
  [out, retval] BSTR *deviceName
);
```



## <a name="property-value"></a>Значение свойства

Имя USB-устройства.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                            | Значение                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>               | Метод завершился успешно.<br/> |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl> | Параметр имеет **значение NULL**.<br/>         |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмусбдевице определяется как 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмусбдевице**](ivmusbdevice.md)
</dt> </dl>

 

