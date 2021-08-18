---
title: Интерфейс Ивмусбдевицеколлектион (Впккоминтерфацес. h)
description: Определяет коллекцию USB-устройств, подключенных к системе узла. Чтобы получить объект Ивмусбдевицеколлектион, используйте свойство Усбдевицеколлектион Ивмвиртуалпк.
ms.assetid: a5cca485-29d3-47fa-9cda-fedcdc379155
keywords:
- Виртуальный ПК с интерфейсом Ивмусбдевицеколлектион
- Ивмусбдевицеколлектион интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1daf5df827bd9d890ede26242957adb2da8a025e8b1d272254e145b12f5aee91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752543"
---
# <a name="ivmusbdevicecollection-interface"></a>Интерфейс Ивмусбдевицеколлектион

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Определяет коллекцию USB-устройств, подключенных к системе узла. Чтобы получить объект **ивмусбдевицеколлектион** , используйте свойство [**Ивмвиртуалпк:: усбдевицеколлектион**](ivmvirtualpc-usbdevicecollection.md) .

## <a name="members"></a>Элементы

Интерфейс **ивмусбдевицеколлектион** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **Ивмусбдевицеколлектион** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Интерфейс **ивмусбдевицеколлектион** имеет следующие свойства.



| Свойство                                                        | Тип доступа          | Описание                                                                         |
|:----------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmusbdevicecollection--newenum.md)<br/> | Только для чтения<br/> | Перечислитель для коллекции.<br/>                                        |
| [**Count**](ivmusbdevicecollection-count.md)<br/>        | Только для чтения<br/> | Число USB-устройств в этой коллекции.<br/>                            |
| [**Компонент**](ivmusbdevicecollection-item.md)<br/>          | Только для чтения<br/> | Объект USB-устройства, соответствующий заданному индексу (от 1).<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмусбдевицеколлектион определен как 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749<br/>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивмусбдевице**](ivmusbdevice.md)
</dt> <dt>

[**Ивмвиртуалпк:: Усбдевицеколлектион**](ivmvirtualpc-usbdevicecollection.md)
</dt> </dl>

 

