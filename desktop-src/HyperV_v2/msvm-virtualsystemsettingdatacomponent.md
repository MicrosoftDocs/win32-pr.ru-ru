---
description: Универсальная ассоциация, используемая для установления части отношений между одним экземпляром CIM \_ виртуалсистемсеттингдата и одним или несколькими экземплярами CIM \_ ресаурцеаллокатионсеттингдата.
ms.assetid: 936B41E7-1B3B-4A7B-86F0-E2F4497CE610
title: Класс Msvm_VirtualSystemSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingDataComponent
- Msvm_VirtualSystemSettingDataComponent.GroupComponent
- Msvm_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bfff3981d6fdb9fdb0368fa887c559026fc10af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662227"
---
# <a name="msvm_virtualsystemsettingdatacomponent-class"></a>\_Класс мсвм виртуалсистемсеттингдатакомпонент

Универсальная ассоциация, используемая для установления отношений "часть" между одним экземпляром [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)) и одним или несколькими экземплярами [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingDataComponent : CIM_VirtualSystemSettingDataComponent
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалсистемсеттингдатакомпонент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ виртуалсистемсеттингдатакомпонент** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **override**, **min** (1), **Max** (1)
</dt> </dl>

Родительский элемент в ассоциации. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдатакомпонент**](/previous-versions//cc150674(v=vs.85)).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дочерний элемент в ассоциации. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдатакомпонент**](/previous-versions//cc150674(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Доступ к классу **\_ виртуалсистемсеттингдатакомпонент мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ВИРТУАЛСИСТЕМСЕТТИНГДАТАКОМПОНЕНТ CIM**](cim-virtualsystemsettingdatacomponent.md)
</dt> <dt>

[**\_ВИРТУАЛСИСТЕМСЕТТИНГДАТАКОМПОНЕНТ CIM**](/previous-versions//cc150674(v=vs.85))
</dt> <dt>

[Классы виртуальных систем](virtual-system-classes.md)
</dt> </dl>

 

