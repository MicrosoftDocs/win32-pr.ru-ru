---
description: '\_Класс WMI взаимосвязей Win32 системоператингсистем связывает компьютерную систему и ее операционную систему.'
ms.assetid: dc71f80b-6fbd-4bc8-8783-3922d8050518
ms.tgt_platform: multiple
title: Класс Win32_SystemOperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemOperatingSystem
- Win32_SystemOperatingSystem.PrimaryOS
- Win32_SystemOperatingSystem.GroupComponent
- Win32_SystemOperatingSystem.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba3f8ac94ec882ee1df96da51d93d2c24fde9b3f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142691"
---
# <a name="win32_systemoperatingsystem-class"></a>\_Класс Win32 системоператингсистем

[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ системоператингсистем** связывает компьютерную систему и ее операционную систему.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemOperatingSystem : CIM_InstalledOS
{
  boolean                   PrimaryOS;
  Win32_ComputerSystem  REF GroupComponent;
  Win32_OperatingSystem REF PartComponent;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ системоператингсистем** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ системоператингсистем** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ ComputerSystem**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

[**Платформа Win32 \_ ComputerSystem**](win32-computersystemprocessor.md) , описывающая свойства компьютерной системы, на которой установлена операционная система.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 с \_ операционной** системы
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Инструментарий WMI \| Win32 \_ ")
</dt> </dl>

Операционная [**система \_ Win32**](win32-operatingsystem.md) с описанием свойств операционной системы, работающей на данной компьютерной системе.

</dd> <dt>

**примарйос**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Операционная система DMTF \| 001,4 ")
</dt> </dl>

Если **значение равно true**, то установленная операционная система является операционной системой по умолчанию для компьютерной системы.

Это свойство наследуется от [**CIM \_ инсталледос**](cim-installedos.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **Win32 \_ системоператингсистем** является производным от [**CIM \_ инсталледос**](cim-installedos.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ИНСТАЛЛЕДОС CIM**](cim-installedos.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> </dl>

 

 
