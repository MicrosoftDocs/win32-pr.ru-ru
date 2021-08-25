---
title: Свойство Девицекласс Ивмусбдевице (Впккоминтерфацес. h)
description: Возвращает класс устройства USB-устройства.
ms.assetid: 46c258b9-6064-4e8c-aa5d-71b26c07351c
keywords:
- Девицекласс свойство Virtual PC
- Девицекласс свойство Virtual PC, интерфейс Ивмусбдевице
- Ивмусбдевице интерфейс Virtual PC, свойство Девицекласс
topic_type:
- apiref
api_name:
- IVMUSBDevice.DeviceClass
- IVMUSBDevice.get_DeviceClass
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f192c81e8dff1d0b1f124393c9eceb9f6268ac43043337399dedb9cdcbebb3be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006914"
---
# <a name="ivmusbdevicedeviceclass-property"></a>Ивмусбдевице: свойство Евицекласс:D

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Возвращает класс устройства USB-устройства.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_DeviceClass(
  [out, retval] VMUSBDeviceClassEnum *deviceClass
);
```



## <a name="property-value"></a>Значение свойства

Класс устройства. Список значений см. в разделе [**вмусбдевицеклассенум**](vmusbdeviceclassenum.md).

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                            | Значение                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>               | Метод завершился успешно.<br/> |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl> | Параметр имеет **значение NULL**.<br/>         |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмусбдевице определяется как 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивмусбдевице**](ivmusbdevice.md)
</dt> </dl>

 

