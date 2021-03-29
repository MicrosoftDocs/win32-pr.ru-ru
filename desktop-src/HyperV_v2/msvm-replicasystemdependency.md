---
description: Представляет связь между экземпляром \_ класса COMPUTERSYSTEM CIM, представляющего реплику виртуальной машины, и экземпляром класса платформы CIM \_ , представляющего тестовую реплику виртуальной машины.
ms.assetid: c3216ddd-7f70-4287-9f7e-1fd7a60b1a0a
title: Класс Msvm_ReplicaSystemDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicaSystemDependency
- Msvm_ReplicaSystemDependency.Antecedent
- Msvm_ReplicaSystemDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8c0db6e476cb883ee1179fcfcc9ac4b212f0b09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264721"
---
# <a name="msvm_replicasystemdependency-class"></a>\_Класс мсвм репликасистемдепенденци

Представляет связь между экземпляром класса [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющего реплику виртуальной машины, и экземпляром класса платформы **CIM, \_** представляющего тестовую реплику виртуальной машины.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicaSystemDependency : CIM_Dependency
{
  CIM_ComputerSystem REF Antecedent;
  CIM_ComputerSystem REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ репликасистемдепенденци** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ репликасистемдепенденци** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ ComputerSystem**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")
</dt> </dl>

Ссылка на экземпляр класса [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий реплику виртуальной машины. Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ ComputerSystem**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ зависимость CIM. Dependent")
</dt> </dl>

Ссылка на экземпляр класса [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий тестовую реплику виртуальной машины, созданную методом [**мсвм \_ репликатионсервице. тестрепликасистем**](testreplicasystem-msvm-replicationservice.md) . Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

