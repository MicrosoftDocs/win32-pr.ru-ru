---
description: '\_Класс WMI взаимосвязей Win32 системсистемдривер связывает компьютерную систему и системный драйвер, работающий на этой компьютерной системе.'
ms.assetid: 82638c29-6769-4410-90bc-b408b27adad4
ms.tgt_platform: multiple
title: Класс Win32_SystemSystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSystemDriver
- Win32_SystemSystemDriver.GroupComponent
- Win32_SystemSystemDriver.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b193d173fa0592a44ba437543659dec456e432ea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539326"
---
# <a name="win32_systemsystemdriver-class"></a>\_Класс Win32 системсистемдривер

[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ системсистемдривер** связывает компьютерную систему и системный драйвер, работающий на этой компьютерной системе.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSystemDriver : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_SystemDriver   REF PartComponent;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ системсистемдривер** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ системсистемдривер** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ ComputerSystem**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Ссылка на экземпляр, представляющий свойства компьютерной системы, на которой выполняется драйвер.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ SystemDriver**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")
</dt> </dl>

Ссылка на экземпляр, представляющий системный драйвер, работающий в компьютерной системе.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **Win32 \_ системсистемдривер** является производным от [**CIM \_ системкомпонент**](cim-systemcomponent.md).

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

[**\_СИСТЕМКОМПОНЕНТ CIM**](cim-systemcomponent.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> </dl>

 

 
