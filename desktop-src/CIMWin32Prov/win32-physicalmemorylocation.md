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
ms.openlocfilehash: daa6d47b13cb5caa74a10f28ab5fcd6e66e1524f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990794"
---
# <a name="win32_physicalmemorylocation-class"></a><span data-ttu-id="a4ed3-103">\_Класс Win32 фисикалмеморилокатион</span><span class="sxs-lookup"><span data-stu-id="a4ed3-103">Win32\_PhysicalMemoryLocation class</span></span>

<span data-ttu-id="a4ed3-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ фисикалмеморилокатион** связывает массив физической памяти с физической памятью.</span><span class="sxs-lookup"><span data-stu-id="a4ed3-104">The **Win32\_PhysicalMemoryLocation** association [WMI class](../wmisdk/retrieving-a-class.md) relates an array of physical memory and its physical memory.</span></span>

<span data-ttu-id="a4ed3-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a4ed3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a4ed3-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="a4ed3-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4ed3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4ed3-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF562-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_PhysicalMemoryLocation : CIM_PackagedComponent
{
  string                        LocationWithinContainer;
  Win32_PhysicalMemory      REF PartComponent;
  Win32_PhysicalMemoryArray REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="a4ed3-108">Члены</span><span class="sxs-lookup"><span data-stu-id="a4ed3-108">Members</span></span>

<span data-ttu-id="a4ed3-109">Класс **Win32 \_ фисикалмеморилокатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a4ed3-109">The **Win32\_PhysicalMemoryLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="a4ed3-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a4ed3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a4ed3-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a4ed3-111">Properties</span></span>

<span data-ttu-id="a4ed3-112">Класс **Win32 \_ фисикалмеморилокатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a4ed3-112">The **Win32\_PhysicalMemoryLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a4ed3-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="a4ed3-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4ed3-114">Тип данных: **Win32 \_ фисикалмеморяррай**</span><span class="sxs-lookup"><span data-stu-id="a4ed3-114">Data type: **Win32\_PhysicalMemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="a4ed3-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a4ed3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4ed3-116">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ фисикалмеморяррай")</span><span class="sxs-lookup"><span data-stu-id="a4ed3-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PhysicalMemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="a4ed3-117">[**\_ Фисикалмеморяррай Win32**](win32-physicalmemoryarray.md) , представляющий массив физической памяти, который содержит физическую память.</span><span class="sxs-lookup"><span data-stu-id="a4ed3-117">A [**Win32\_PhysicalMemoryArray**](win32-physicalmemoryarray.md) that represents the physical memory array that contains the physical memory.</span></span>

</dd> <dt>

<span data-ttu-id="a4ed3-118">**локатионвисинконтаинер**</span><span class="sxs-lookup"><span data-stu-id="a4ed3-118">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4ed3-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a4ed3-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4ed3-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a4ed3-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4ed3-121">Произвольная строка, представляющая расположение физического элемента в физическом пакете.</span><span class="sxs-lookup"><span data-stu-id="a4ed3-121">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="a4ed3-122">Сведения относительно стационарных элементов в контейнере (например, "второй отсек для дисков сверху"), углы, высота и другие данные могут быть записаны в это свойство.</span><span class="sxs-lookup"><span data-stu-id="a4ed3-122">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="a4ed3-123">Эта строка может дополнять или использоваться вместо создания экземпляра объекта [**\_ расположения CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="a4ed3-123">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="a4ed3-124">Это свойство наследуется от [**CIM- \_ контейнера**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="a4ed3-124">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4ed3-125">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a4ed3-125">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4ed3-126">Тип данных: **Win32 \_ фисикалмемори**</span><span class="sxs-lookup"><span data-stu-id="a4ed3-126">Data type: **Win32\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="a4ed3-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a4ed3-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4ed3-128">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ фисикалмемори")</span><span class="sxs-lookup"><span data-stu-id="a4ed3-128">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PhysicalMemory")</span></span>
</dt> </dl>

<span data-ttu-id="a4ed3-129">[**\_ Фисикалмемори Win32**](win32-physicalmemory.md) , представляющий физическую память, содержащуюся в массиве физической памяти.</span><span class="sxs-lookup"><span data-stu-id="a4ed3-129">A [**Win32\_PhysicalMemory**](win32-physicalmemory.md) that represents the physical memory contained in the physical memory array.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4ed3-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4ed3-130">Remarks</span></span>

<span data-ttu-id="a4ed3-131">Класс **Win32 \_ фисикалмеморилокатион** является производным от [**CIM \_ паккажедкомпонент**](cim-packagedcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="a4ed3-131">The **Win32\_PhysicalMemoryLocation** class is derived from [**CIM\_PackagedComponent**](cim-packagedcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4ed3-132">Требования</span><span class="sxs-lookup"><span data-stu-id="a4ed3-132">Requirements</span></span>



| <span data-ttu-id="a4ed3-133">Требование</span><span class="sxs-lookup"><span data-stu-id="a4ed3-133">Requirement</span></span> | <span data-ttu-id="a4ed3-134">Значение</span><span class="sxs-lookup"><span data-stu-id="a4ed3-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4ed3-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4ed3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a4ed3-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4ed3-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a4ed3-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4ed3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a4ed3-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4ed3-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a4ed3-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a4ed3-139">Namespace</span></span><br/>                | <span data-ttu-id="a4ed3-140">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a4ed3-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a4ed3-141">MOF</span><span class="sxs-lookup"><span data-stu-id="a4ed3-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4ed3-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4ed3-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4ed3-143">DLL</span><span class="sxs-lookup"><span data-stu-id="a4ed3-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4ed3-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4ed3-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4ed3-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4ed3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4ed3-146">**\_ПАККАЖЕДКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="a4ed3-146">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> <dt>

[<span data-ttu-id="a4ed3-147">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="a4ed3-147">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
