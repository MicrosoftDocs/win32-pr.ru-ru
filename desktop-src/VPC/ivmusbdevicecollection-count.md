---
title: Свойство Ивмусбдевицеколлектион Count (Впккоминтерфацес. h)
description: Возвращает число USB-устройств в этой коллекции.
ms.assetid: 8d17397b-4f4a-475d-99fe-4df0d74fe5a5
keywords:
- Число свойств Virtual PC
- Число свойств Virtual PC, интерфейс Ивмусбдевицеколлектион
- Ивмусбдевицеколлектион интерфейс Virtual PC, свойство Count
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection.Count
- IVMUSBDeviceCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a0c2146df70f0432a19d65daad44ba6f1ec372
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490941"
---
# <a name="ivmusbdevicecollectioncount-property"></a>Свойство Ивмусбдевицеколлектион:: count

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Возвращает число USB-устройств в этой коллекции.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Значение свойства

Число USB-устройств.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>     |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>        |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмусбдевицеколлектион определен как 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749<br/>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмусбдевицеколлектион**](ivmusbdevicecollection.md)
</dt> </dl>

 

