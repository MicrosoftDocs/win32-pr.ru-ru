---
title: Интерфейс Ивмфлоппидривеколлектион (Впккоминтерфацес. h)
description: Определяет коллекцию дисководов гибких дисков в виртуальной машине.
ms.assetid: ba05fa84-81c3-4e70-98f5-404a9bc517ad
keywords:
- Виртуальный ПК с интерфейсом Ивмфлоппидривеколлектион
- Ивмфлоппидривеколлектион интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6637c0c4a8c8b87f4458081b0893b0939c8eaf04c97738c02d39da5e0fd8eebb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653594"
---
# <a name="ivmfloppydrivecollection-interface"></a>Интерфейс Ивмфлоппидривеколлектион

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Определяет коллекцию дисководов гибких дисков в виртуальной машине. Чтобы получить объект **ивмфлоппидривеколлектион** , используйте свойство [**Ивмвиртуалмачине:: флоппидривес**](ivmvirtualmachine-floppydrives.md) .

## <a name="members"></a>Элементы

Интерфейс **ивмфлоппидривеколлектион** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **Ивмфлоппидривеколлектион** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Интерфейс **ивмфлоппидривеколлектион** имеет следующие свойства.



| Свойство.                                                          | Тип доступа          | Описание                                                                 |
|:------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**\_NewEnum**](ivmfloppydrivecollection--newenum.md)<br/> | Только для чтения<br/> | Перечислитель для коллекции.<br/>                                |
| [**Count**](ivmfloppydrivecollection-count.md)<br/>        | Только для чтения<br/> | Число дисководов гибких дисков в этой коллекции.<br/>                  |
| [**Элемент**](ivmfloppydrivecollection-item.md)<br/>          | Только для чтения<br/> | Объект дисковода гибких дисков, соответствующий указанному индексу.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмфлоппидривеколлектион определен как 8ba70a25-F698-4ee5-85CE-3cc93a925516<br/>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмфлоппидриве**](ivmfloppydrive.md)
</dt> <dt>

[**Ивмвиртуалмачине:: Флоппидривес**](ivmvirtualmachine-floppydrives.md)
</dt> </dl>

 

