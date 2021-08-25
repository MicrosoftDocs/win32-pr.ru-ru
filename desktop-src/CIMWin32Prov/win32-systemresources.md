---
description: '\_Класс WMI взаимосвязей Win32 системресаурцес связывает системный ресурс и компьютерную систему, на которой он находится.'
ms.assetid: 90bff0b0-7c1d-44bf-b67e-aefeaa4b4a83
ms.tgt_platform: multiple
title: Класс Win32_SystemResources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemResources
- Win32_SystemResources.GroupComponent
- Win32_SystemResources.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 160be61ab1dc850cc84938be68f79c02ead0597727d330c5d2ea7d3494a923dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827964"
---
# <a name="win32_systemresources-class"></a>\_Класс Win32 системресаурцес

[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ системресаурцес** связывает системный ресурс и компьютерную систему, на которой он находится.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemResources : CIM_ComputerSystemResource
{
  Win32_ComputerSystem REF GroupComponent;
  CIM_SystemResource   REF PartComponent;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ системресаурцес** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ системресаурцес** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ ComputerSystem**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Ссылка на экземпляр, представляющий компьютерную систему, в которой находится ресурс.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ системресаурце**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ системресаурце")
</dt> </dl>

Ссылка на экземпляр, представляющий ресурс (например, службы ввода-вывода и ресурсы памяти), доступный в компьютерной системе.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ системресаурцес** является производным от [**CIM \_ компутерсистемресаурце**](cim-computersystemresource.md).

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

[**\_КОМПУТЕРСИСТЕМРЕСАУРЦЕ CIM**](cim-computersystemresource.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> </dl>

 

 
