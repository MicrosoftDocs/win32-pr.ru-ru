---
title: Интерфейс Ивмвиртуалнетворкколлектион (Впккоминтерфацес. h)
description: Определяет коллекцию объектов Ивмвиртуалнетворк. Чтобы получить объект Ивмвиртуалнетворкколлектион, используйте свойство VirtualNetworks Ивмвиртуалпк.
ms.assetid: 3d595bc3-1a8d-4e09-a809-944d4dcdc675
keywords:
- Виртуальный ПК с интерфейсом Ивмвиртуалнетворкколлектион
- Ивмвиртуалнетворкколлектион интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32694b311482e58635ca28dc005fe68ab08495c15d251e176fb78266e7624e29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592275"
---
# <a name="ivmvirtualnetworkcollection-interface"></a>Интерфейс Ивмвиртуалнетворкколлектион

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Определяет коллекцию объектов [**ивмвиртуалнетворк**](ivmvirtualnetwork.md) . Чтобы получить объект **ивмвиртуалнетворкколлектион** , используйте свойство [**Ивмвиртуалпк:: VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) .

## <a name="members"></a>Элементы

Интерфейс **ивмвиртуалнетворкколлектион** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **Ивмвиртуалнетворкколлектион** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Интерфейс **ивмвиртуалнетворкколлектион** имеет следующие свойства.



| Свойство                                                             | Тип доступа          | Описание                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmvirtualnetworkcollection--newenum.md)<br/> | Только для чтения<br/> | Перечислитель для коллекции.<br/>                                                                  |
| [**Count**](ivmvirtualnetworkcollection-count.md)<br/>        | Только для чтения<br/> | Число виртуальных сетей в этой коллекции.<br/>                                                 |
| [**Item**](ivmvirtualnetworkcollection-item.md)<br/>          | Только для чтения<br/> | Объект [**ивмвиртуалнетворк**](ivmvirtualnetwork.md) , соответствующий указанному индексу.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                     |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                           |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                  |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl>  |
| IID<br/>                      | IID \_ ивмвиртуалнетворкколлектион определен как 8ed680be-4242-4b2a-a21c-1982d8b0f675<br/> |



 

