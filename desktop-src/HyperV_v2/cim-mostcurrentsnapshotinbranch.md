---
description: Представляет связь между виртуальной системой и самым актуальным моментальным снимком системы. Эта ассоциация может существовать только в том случае, если виртуальная система была создана с помощью моментального снимка или если моментальный снимок был создан из виртуальной системы.
ms.assetid: e6040818-84cf-4cec-ab7b-a733fe5d01d2
title: Класс CIM_MostCurrentSnapshotInBranch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MostCurrentSnapshotInBranch
- CIM_MostCurrentSnapshotInBranch.Antecedent
- CIM_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 078a7c9f1669a2aa0449dce01022eba0eadcb2c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683260"
---
# <a name="cim_mostcurrentsnapshotinbranch-class"></a>\_Класс CIM мосткуррентснапшотинбранч

Представляет связь между виртуальной системой и самым актуальным моментальным снимком системы. Эта ассоциация может существовать только в том случае, если виртуальная система была создана с помощью моментального снимка или если моментальный снимок был создан из виртуальной системы.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Experimental, Version("2.16.0"), AMENDMENT]
class CIM_MostCurrentSnapshotInBranch : CIM_Dependency
{
  CIM_ComputerSystem           REF Antecedent;
  CIM_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ мосткуррентснапшотинбранч** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ мосткуррентснапшотинбранч** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ ComputerSystem**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ссылка на экземпляр [**CIM \_ ComputerSystem**](cim-computersystem.md) , представляющий виртуальную систему.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ виртуалсистемсеттингдата**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ссылка на экземпляр [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) , представляющий моментальный снимок виртуальной системы.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Зависимость CIM**](cim-dependency.md)
</dt> </dl>

 

