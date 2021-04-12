---
title: Свойство Item Ивмусбдевицеколлектион (Впккоминтерфацес. h)
description: Извлекает объект USB-устройства, соответствующий указанному индексу.
ms.assetid: 664a038e-7c86-43a9-a376-c913d431dc93
keywords:
- Свойство элемента Virtual PC
- Свойство элемента Virtual PC, интерфейс Ивмусбдевицеколлектион
- Интерфейс Ивмусбдевицеколлектион Virtual PC, свойство Item
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection.Item
- IVMUSBDeviceCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b50b96de6b19dab15852f58d78480b46da1e9ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490938"
---
# <a name="ivmusbdevicecollectionitem-property"></a>Свойство Ивмусбдевицеколлектион:: Item

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Извлекает объект USB-устройства, соответствующий указанному индексу.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Item(
  [in]          long         index,
  [out, retval] IVMUSBDevice **usbDevice
);
```



## <a name="property-value"></a>Значение свойства

Объект [**ивмусбдевице**](ivmusbdevice.md) .

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно. <br/>                                                      |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр *усбдевице* имеет **значение NULL**. <br/>                                             |
| <dl> <dt> \_ E \_ бадиндекс</dt> <dt>0x8002000B</dt> </dl>  | Индекс запрошенного элемента не соответствует элементу в этой коллекции. <br/> |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/>                                                   |



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

[**ивмусбдевице**](ivmusbdevice.md)
</dt> <dt>

[**ивмусбдевицеколлектион**](ivmusbdevicecollection.md)
</dt> </dl>

 

