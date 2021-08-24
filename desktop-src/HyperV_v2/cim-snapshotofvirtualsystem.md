---
description: Связывает виртуальную систему с моментальным снимком виртуальной системы.
ms.assetid: f85f6914-dbb8-42c9-a732-11d48613c15c
title: Класс CIM_SnapshotOfVirtualSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SnapshotOfVirtualSystem
- CIM_SnapshotOfVirtualSystem.Antecedent
- CIM_SnapshotOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 598ee11064872653ec216cef5751312e02809fb1cc45e4831fa50e01b1af46a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899640"
---
# <a name="cim_snapshotofvirtualsystem-class"></a>\_Класс CIM снапшотофвиртуалсистем

Связывает виртуальную систему с моментальным снимком виртуальной системы.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Abstract, Version("2.22.0"), AMENDMENT]
class CIM_SnapshotOfVirtualSystem : CIM_Dependency
{
  CIM_ComputerSystem           REF Antecedent;
  CIM_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ снапшотофвиртуалсистем** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ снапшотофвиртуалсистем** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ ComputerSystem**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ссылка на компьютерную систему, представляющую виртуальную систему.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ виртуалсистемсеттингдата**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Ссылка на объект данных параметров, представляющий моментальный снимок виртуальной системы.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Зависимость CIM**](cim-dependency.md)
</dt> </dl>

 

