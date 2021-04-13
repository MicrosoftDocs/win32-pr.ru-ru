---
description: Связывает виртуальную машину и ее устройства с экземплярами \_ SETTINGDATA CIM, представляющими текущие параметры, которые применяются к этим объектам.
ms.assetid: 991FE773-1F87-4D5E-89E6-CB1A33989B1A
title: Класс Msvm_SettingsDefineState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineState
- Msvm_SettingsDefineState.ManagedElement
- Msvm_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f104943be80df696b58c9d5d6eaad4c430362338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265243"
---
# <a name="msvm_settingsdefinestate-class"></a>\_Класс мсвм сеттингсдефинестате

Связывает виртуальную машину и ее устройства с экземплярами [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)) , представляющими текущие параметры, которые применяются к этим объектам. В частности, он связывает [**мсвм \_ ComputerSystem**](msvm-computersystem.md) с экземплярами [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md)и связывает **\_ \* мсвм* _, производную от [_ *CIM \_* *](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , с **мсвм \_ \** _, производными от [_ *CIM \_ ресаурцеаллокатионсеттингдата*. *](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_SettingsDefineState : CIM_SettingsDefineState
{
  Msvm_ComputerSystem           REF ManagedElement;
  Msvm_VirtualSystemSettingData REF SettingData;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ сеттингсдефинестате** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ сеттингсдефинестате** имеет следующие свойства.

<dl> <dt>

**манажеделемент**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на виртуальную машину.

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на текущие активные параметры виртуальной машины.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Доступ к классу **\_ сеттингсдефинестате мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                                            |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                                 |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_СЕТТИНГСДЕФИНЕСТАТЕ CIM**](cim-settingsdefinestate.md)
</dt> <dt>

[**\_СЕТТИНГСДЕФИНЕСТАТЕ CIM**](/previous-versions/windows/desktop/clushyperv/cim-settingsdefinestate)
</dt> <dt>

[Классы управления виртуальной системой](virtual-system-management-classes.md)
</dt> </dl>

 

