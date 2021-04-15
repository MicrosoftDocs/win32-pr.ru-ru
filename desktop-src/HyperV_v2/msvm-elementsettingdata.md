---
description: Связывает управляемый элемент с его данными конфигурации.
ms.assetid: 4DB78E43-E387-478E-999C-770B35925721
title: Класс Msvm_ElementSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementSettingData
- Msvm_ElementSettingData.ManagedElement
- Msvm_ElementSettingData.SettingData
- Msvm_ElementSettingData.IsDefault
- Msvm_ElementSettingData.IsCurrent
- Msvm_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f4d2af614e3b161f49a0d37d1e4d1ee48ce0aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682870"
---
# <a name="msvm_elementsettingdata-class"></a>\_Класс мсвм елементсеттингдата

Связывает управляемый элемент с его данными конфигурации. Некоторые из наиболее важных приложений этой ассоциации используются при связывании виртуальной машины и логических устройств, назначенных этой системе, со сведениями о конфигурации моментальных снимков. Текущие сведения о конфигурации связаны с виртуальной машиной и ее устройствами через ассоциацию [**мсвм \_ сеттингсдефинестате**](msvm-settingsdefinestate.md) .

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementSettingData : CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault = 0;
  uint16                 IsCurrent = 0;
  uint16                 IsNext = 0;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ елементсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ елементсеттингдата** имеет следующие свойства.

<dl> <dt>

**IsCurrent**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, что параметр, на который указывает ссылка, в данный момент используется в операции элемента или что эти сведения неизвестны. Это свойство наследуется от [**CIM \_ елементсеттингдата**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata). Значение по умолчанию — 0 (неизвестно).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>**Является текущим** (1)
</dt> <dt>

<span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>**Не является текущим** (2)
</dt> </dl>

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, что параметр, на который указывает ссылка, является значением по умолчанию для элемента или что эта информация неизвестна. Это свойство наследуется от [**CIM \_ елементсеттингдата**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata). Значение по умолчанию — 0 (неизвестно).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>Значение **по умолчанию** (1)
</dt> <dt>

<span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>**Не является значением по умолчанию** (2)
</dt> </dl>

</dd> <dt>

**По подследу**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, является ли параметр, на который указывает ссылка, следующим параметром, который должен быть применен. Это свойство наследуется от [**CIM \_ елементсеттингдата**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata). Значение по умолчанию — 0 (неизвестно).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>**Следующий** (1)
</dt> <dt>

<span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>**Не далее** (2)
</dt> <dt>

<span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>**Следующее для отдельного использования** (3)
</dt> </dl>

</dd> <dt>

**манажеделемент**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на виртуальную машину или виртуальное устройство. Это свойство наследуется от [**CIM \_ елементсеттингдата**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Тип данных: **[ **\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85))**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на параметры снапшоттед для виртуальной машины или виртуального устройства. Это свойство наследуется от [**CIM \_ елементсеттингдата**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Доступ к классу **\_ елементсеттингдата мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Примеры

См. раздел [запросы к сетевым объектам](querying-networking-objects.md).

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

[**\_ЕЛЕМЕНТСЕТТИНГДАТА CIM**](cim-elementsettingdata.md)
</dt> <dt>

[**\_ЕЛЕМЕНТСЕТТИНГДАТА CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)
</dt> <dt>

[Классы управления виртуальной системой](virtual-system-management-classes.md)
</dt> </dl>

 

