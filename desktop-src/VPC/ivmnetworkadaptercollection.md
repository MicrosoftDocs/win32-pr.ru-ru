---
title: Интерфейс Ивмнетворкадаптерколлектион (Впккоминтерфацес. h)
description: Определяет коллекцию адаптеров виртуальных сетевых интерфейсов. Чтобы получить объект Ивмнетворкадаптерколлектион, используйте свойства Ивмвиртуалмачине адаптера, Ивмвиртуалнетворк адаптера и Ивмвиртуалпк Унконнектеднетворкадаптерс.
ms.assetid: cfb03a7c-a568-488c-9284-798b7e21027a
keywords:
- Виртуальный ПК с интерфейсом Ивмнетворкадаптерколлектион
- Ивмнетворкадаптерколлектион интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8005b88cb873f00708829672cdeb6563b606d42b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071722"
---
# <a name="ivmnetworkadaptercollection-interface"></a>Интерфейс Ивмнетворкадаптерколлектион

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Определяет коллекцию адаптеров виртуальных сетевых интерфейсов. Чтобы получить объект Ивмнетворкадаптерколлектион, используйте свойства [**ивмвиртуалмачине:: адаптера**](ivmvirtualmachine-networkadapters.md), [**Ивмвиртуалнетворк:: адаптера**](ivmvirtualnetwork-networkadapters.md)и [**ивмвиртуалпк:: унконнектеднетворкадаптерс**](ivmvirtualpc-unconnectednetworkadapters.md) .

## <a name="members"></a>Элементы

Интерфейс **ивмнетворкадаптерколлектион** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **Ивмнетворкадаптерколлектион** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Интерфейс **ивмнетворкадаптерколлектион** имеет следующие свойства.



| Свойство                                                             | Тип доступа          | Описание                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmnetworkadaptercollection--newenum.md)<br/> | Только для чтения<br/> | Перечислитель для коллекции.<br/>                                                                  |
| [**Расчета**](ivmnetworkadaptercollection-count.md)<br/>        | Только для чтения<br/> | Число сетевых интерфейсов в этой коллекции.<br/>                                               |
| [**Элемент**](ivmnetworkadaptercollection-item.md)<br/>          | Только для чтения<br/> | Объект [**ивмнетворкадаптер**](ivmnetworkadapter.md) , соответствующий указанному индексу.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                     |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                           |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl>  |
| IID<br/>                      | IID \_ ивмнетворкадаптерколлектион определен как ebaeafe9-EBCD-47cf-866e-ad87d735e479<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмнетворкадаптер**](ivmnetworkadapter.md)
</dt> <dt>

[**Ивмвиртуалмачине:: адаптера**](ivmvirtualmachine-networkadapters.md)
</dt> <dt>

[**Ивмвиртуалнетворк:: адаптера**](ivmvirtualnetwork-networkadapters.md)
</dt> <dt>

[**Ивмвиртуалпк:: Унконнектеднетворкадаптерс**](ivmvirtualpc-unconnectednetworkadapters.md)
</dt> </dl>

 

