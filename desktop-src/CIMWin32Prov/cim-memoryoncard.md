---
description: Класс CIM \_ меморйонкард связывает физическую память, размещенную на досках размещения, платах адаптеров и т. д. Эта ассоциация явно определяет связь памяти с картами.
ms.assetid: 0d094cad-c542-4794-b6e1-87cdc8067668
ms.tgt_platform: multiple
title: Класс CIM_MemoryOnCard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryOnCard
- CIM_MemoryOnCard.LocationWithinContainer
- CIM_MemoryOnCard.PartComponent
- CIM_MemoryOnCard.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2094101ab0cbbbc769194793273bf080cfe52818
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655932"
---
# <a name="cim_memoryoncard-class"></a><span data-ttu-id="72a3d-104">\_Класс CIM меморйонкард</span><span class="sxs-lookup"><span data-stu-id="72a3d-104">CIM\_MemoryOnCard class</span></span>

<span data-ttu-id="72a3d-105">Класс **CIM \_ меморйонкард** связывает физическую память, размещенную на досках размещения, платах адаптеров и т. д.</span><span class="sxs-lookup"><span data-stu-id="72a3d-105">The **CIM\_MemoryOnCard** class associates physical memory located on hosting boards, adapter cards, and so on.</span></span> <span data-ttu-id="72a3d-106">Эта ассоциация явно определяет связь памяти с картами.</span><span class="sxs-lookup"><span data-stu-id="72a3d-106">This association explicitly defines the relationship of memory to cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="72a3d-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="72a3d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="72a3d-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="72a3d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="72a3d-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="72a3d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="72a3d-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="72a3d-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="72a3d-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72a3d-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryOnCard : CIM_PackagedComponent
{
  string                 LocationWithinContainer;
  CIM_PhysicalMemory REF PartComponent;
  CIM_Card           REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="72a3d-112">Члены</span><span class="sxs-lookup"><span data-stu-id="72a3d-112">Members</span></span>

<span data-ttu-id="72a3d-113">Класс **CIM \_ меморйонкард** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="72a3d-113">The **CIM\_MemoryOnCard** class has these types of members:</span></span>

-   [<span data-ttu-id="72a3d-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="72a3d-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72a3d-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="72a3d-115">Properties</span></span>

<span data-ttu-id="72a3d-116">Класс **CIM \_ меморйонкард** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="72a3d-116">The **CIM\_MemoryOnCard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72a3d-117">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="72a3d-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a3d-118">Тип данных: **\_ карта CIM**</span><span class="sxs-lookup"><span data-stu-id="72a3d-118">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="72a3d-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="72a3d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72a3d-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="72a3d-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="72a3d-121">[**\_ Карта CIM**](cim-card.md) , описывающая карточку, которая включает в себя или "содержит" память.</span><span class="sxs-lookup"><span data-stu-id="72a3d-121">A [**CIM\_Card**](cim-card.md) describing the card that includes or 'contains' memory.</span></span>

</dd> <dt>

<span data-ttu-id="72a3d-122">**локатионвисинконтаинер**</span><span class="sxs-lookup"><span data-stu-id="72a3d-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a3d-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="72a3d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72a3d-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="72a3d-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72a3d-125">Произвольная строка, представляющая расположение физического элемента в физическом пакете.</span><span class="sxs-lookup"><span data-stu-id="72a3d-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="72a3d-126">Сведения относительно стационарных элементов в контейнере (например, "второй отсек для дисков сверху"), углы, высота и другие данные могут быть записаны в это свойство.</span><span class="sxs-lookup"><span data-stu-id="72a3d-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="72a3d-127">Эта строка может дополнять или использоваться вместо создания экземпляра объекта [**\_ расположения CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="72a3d-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="72a3d-128">Это свойство наследуется от [**CIM- \_ контейнера**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="72a3d-128">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="72a3d-129">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="72a3d-129">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a3d-130">Тип данных: **CIM \_ фисикалмемори**</span><span class="sxs-lookup"><span data-stu-id="72a3d-130">Data type: **CIM\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="72a3d-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="72a3d-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72a3d-132">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="72a3d-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="72a3d-133">[**\_ Фисикалмемори CIM**](cim-physicalmemory.md) , описывающий физическую память, расположенную на карте.</span><span class="sxs-lookup"><span data-stu-id="72a3d-133">A [**CIM\_PhysicalMemory**](cim-physicalmemory.md) describing the physical memory which is located on the card.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72a3d-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="72a3d-134">Remarks</span></span>

<span data-ttu-id="72a3d-135">Класс **CIM \_ меморйонкард** является производным от [**CIM \_ паккажедкомпонент**](cim-packagedcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="72a3d-135">The **CIM\_MemoryOnCard** class is derived from [**CIM\_PackagedComponent**](cim-packagedcomponent.md).</span></span>

<span data-ttu-id="72a3d-136">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="72a3d-136">WMI does not implement this class.</span></span>

<span data-ttu-id="72a3d-137">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="72a3d-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="72a3d-138">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="72a3d-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="72a3d-139">Требования</span><span class="sxs-lookup"><span data-stu-id="72a3d-139">Requirements</span></span>



| <span data-ttu-id="72a3d-140">Требование</span><span class="sxs-lookup"><span data-stu-id="72a3d-140">Requirement</span></span> | <span data-ttu-id="72a3d-141">Значение</span><span class="sxs-lookup"><span data-stu-id="72a3d-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72a3d-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="72a3d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="72a3d-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72a3d-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="72a3d-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="72a3d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="72a3d-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72a3d-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="72a3d-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="72a3d-146">Namespace</span></span><br/>                | <span data-ttu-id="72a3d-147">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="72a3d-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="72a3d-148">MOF</span><span class="sxs-lookup"><span data-stu-id="72a3d-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72a3d-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72a3d-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="72a3d-150">DLL</span><span class="sxs-lookup"><span data-stu-id="72a3d-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72a3d-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72a3d-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72a3d-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72a3d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72a3d-153">**\_ПАККАЖЕДКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="72a3d-153">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> </dl>

 

