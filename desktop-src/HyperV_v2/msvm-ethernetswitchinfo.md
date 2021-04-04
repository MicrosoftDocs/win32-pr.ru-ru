---
description: Определяет связь между коммутатором Ethernet и ресурсом коммутатора.
ms.assetid: fb29f4cb-50c4-4865-b267-21ff99bb4a8b
title: Класс Msvm_EthernetSwitchInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchInfo
- Msvm_EthernetSwitchInfo.Antecedent
- Msvm_EthernetSwitchInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1106e0930716572b10a95846865d8f90aa991cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999773"
---
# <a name="msvm_ethernetswitchinfo-class"></a>\_Класс мсвм есернетсвитчинфо

Определяет связь между коммутатором Ethernet и ресурсом коммутатора.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchInfo : CIM_Dependency
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  Msvm_EthernetSwitchData    REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ есернетсвитчинфо** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ есернетсвитчинфо** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ виртуалесернетсвитч**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Ссылка на класс [**мсвм \_ виртуалесернетсвитч**](msvm-virtualethernetswitch.md) , представляющий систему размещения. Это свойство является производным [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ есернетсвитчдата**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Ссылка на класс [**мсвм \_ есернетсвитчдата**](msvm-ethernetswitchdata.md) , представляющий ресурс коммутатора. Это свойство является производным [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

