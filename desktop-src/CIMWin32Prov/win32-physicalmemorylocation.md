---
description: '\_Класс WMI взаимосвязей Win32 фисикалмеморилокатион связывает массив физической памяти с физической памятью.'
ms.assetid: 40252428-77ca-4dfb-8048-c05096a114d8
ms.tgt_platform: multiple
title: Класс Win32_PhysicalMemoryLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemoryLocation
- Win32_PhysicalMemoryLocation.LocationWithinContainer
- Win32_PhysicalMemoryLocation.PartComponent
- Win32_PhysicalMemoryLocation.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10f4822312619b5b7fb811a998d82527b6e8bd0bd604e0d2095dae5103935e41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972064"
---
# <a name="win32_physicalmemorylocation-class"></a>\_Класс Win32 фисикалмеморилокатион

[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ фисикалмеморилокатион** связывает массив физической памяти с физической памятью.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF562-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_PhysicalMemoryLocation : CIM_PackagedComponent
{
  string                        LocationWithinContainer;
  Win32_PhysicalMemory      REF PartComponent;
  Win32_PhysicalMemoryArray REF GroupComponent;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ фисикалмеморилокатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ фисикалмеморилокатион** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ фисикалмеморяррай**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ фисикалмеморяррай")
</dt> </dl>

[**\_ Фисикалмеморяррай Win32**](win32-physicalmemoryarray.md) , представляющий массив физической памяти, который содержит физическую память.

</dd> <dt>

**локатионвисинконтаинер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Произвольная строка, представляющая расположение физического элемента в физическом пакете. Сведения относительно стационарных элементов в контейнере (например, "второй отсек для дисков сверху"), углы, высота и другие данные могут быть записаны в это свойство. Эта строка может дополнять или использоваться вместо создания экземпляра объекта [**\_ расположения CIM**](cim-location.md) .

Это свойство наследуется от [**CIM- \_ контейнера**](cim-container.md).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ фисикалмемори**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ фисикалмемори")
</dt> </dl>

[**\_ Фисикалмемори Win32**](win32-physicalmemory.md) , представляющий физическую память, содержащуюся в массиве физической памяти.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ фисикалмеморилокатион** является производным от [**CIM \_ паккажедкомпонент**](cim-packagedcomponent.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_ПАККАЖЕДКОМПОНЕНТ CIM**](cim-packagedcomponent.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

 
