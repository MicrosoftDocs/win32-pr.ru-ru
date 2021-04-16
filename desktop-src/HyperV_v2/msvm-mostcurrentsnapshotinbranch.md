---
description: Связывает экземпляр \_ класса мсвм ComputerSystem или мсвм \_ планнедкомпутерсистем, представляющий виртуальную систему, с экземпляром \_ класса мсвм виртуалсистемсеттингдата, представляющего моментальный снимок виртуальной системы, который является самым актуальным моментальным снимком в ветви зависимых моментальных снимков.
ms.assetid: EEB9D2C1-C463-4EFE-862F-95E8AD8E1753
title: Класс Msvm_MostCurrentSnapshotInBranch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MostCurrentSnapshotInBranch
- Msvm_MostCurrentSnapshotInBranch.Antecedent
- Msvm_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3ed0824fd68670245e2c8d09b73733ff23be16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664508"
---
# <a name="msvm_mostcurrentsnapshotinbranch-class"></a>\_Класс мсвм мосткуррентснапшотинбранч

Связывает экземпляр класса [**мсвм \_ ComputerSystem**](msvm-computersystem.md) или [**мсвм \_ планнедкомпутерсистем**](msvm-plannedcomputersystem.md) , представляющий виртуальную систему, с экземпляром класса [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , представляющего моментальный снимок виртуальной системы, который является самым актуальным моментальным снимком в ветви зависимых моментальных снимков.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Experimental, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MostCurrentSnapshotInBranch : CIM_MostCurrentSnapshotInBranch
{
  CIM_ComputerSystem            REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ мосткуррентснапшотинбранч** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ мосткуррентснапшотинбранч** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ ComputerSystem**](msvm-computersystem.md) или [**мсвм \_ планнедкомпутерсистем**](msvm-plannedcomputersystem.md) , представляющий виртуальную систему. Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , представляющий моментальный снимок виртуальной системы, который является самым актуальным моментальным снимком в ветви зависимых моментальных снимков. Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

