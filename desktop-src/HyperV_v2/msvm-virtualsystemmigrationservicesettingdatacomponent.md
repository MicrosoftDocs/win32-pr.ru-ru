---
description: Ассоциация, используемая для представления параметров сети миграции виртуальной системы для службы миграции виртуальной системы.
ms.assetid: 5704dce7-1db3-4049-8c61-58bfa9596766
title: Класс Msvm_VirtualSystemMigrationServiceSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingDataComponent
- Msvm_VirtualSystemMigrationServiceSettingDataComponent.GroupComponent
- Msvm_VirtualSystemMigrationServiceSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1ba69ebd6cfd50b30923db2ecc87e7e5aeebcaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662232"
---
# <a name="msvm_virtualsystemmigrationservicesettingdatacomponent-class"></a>\_Класс мсвм виртуалсистеммигратионсервицесеттингдатакомпонент

Ассоциация, используемая для представления параметров сети миграции виртуальной системы для службы миграции виртуальной системы.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingDataComponent : CIM_Component
{
  Msvm_VirtualSystemMigrationServiceSettingData REF GroupComponent;
  Msvm_VirtualSystemMigrationNetworkSettingData REF PartComponent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалсистеммигратионсервицесеттингдатакомпонент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ виртуалсистеммигратионсервицесеттингдатакомпонент** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ виртуалсистеммигратионсервицесеттингдата**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**агрегатная функция**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ виртуалсистеммигратионсервицесеттингдата**](msvm-virtualsystemmigrationservicesettingdata.md) , представляющий параметры службы миграции.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ виртуалсистеммигратионнетворксеттингдата**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ виртуалсистеммигратионнетворксеттингдата**](msvm-virtualsystemmigrationnetworksettingdata.md) , представляющий параметры сети миграции.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

