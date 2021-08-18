---
title: Свойство Мануфактурерстринг Ивмусбдевице (Впккоминтерфацес. h)
description: Получает имя изготовителя USB-устройства.
ms.assetid: 0d815887-96bf-4795-a4eb-32fb2f35c57e
keywords:
- Мануфактурерстринг свойство Virtual PC
- Мануфактурерстринг свойство Virtual PC, интерфейс Ивмусбдевице
- Ивмусбдевице интерфейс Virtual PC, свойство Мануфактурерстринг
topic_type:
- apiref
api_name:
- IVMUSBDevice.ManufacturerString
- IVMUSBDevice.get_ManufacturerString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb0ec725779e4ffd18d46752f4083ad53c5b77c8392b45dc414d927b1038988
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973714"
---
# <a name="ivmusbdevicemanufacturerstring-property"></a>Свойство Ивмусбдевице:: Мануфактурерстринг

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Получает имя изготовителя USB-устройства.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_ManufacturerString(
  [out, retval] BSTR *manufacturerName
);
```



## <a name="property-value"></a>Значение свойства

Имя изготовителя USB-устройства.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                            | Значение                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>               | Метод завершился успешно.<br/> |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl> | Параметр имеет **значение NULL**.<br/>         |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмусбдевице определяется как 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмусбдевице**](ivmusbdevice.md)
</dt> </dl>

 

