---
description: '\_Класс контейнера CIM представляет связь между содержащимся и содержащимся физическим элементом. Содержащий объект должен быть физическим пакетом.'
ms.assetid: 9b119163-3c56-44e2-ba66-d8add3c375fa
ms.tgt_platform: multiple
title: Класс CIM_Container
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Container
- CIM_Container.PartComponent
- CIM_Container.GroupComponent
- CIM_Container.LocationWithinContainer
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 70aca54c80a954deed88d1ec740f0057753bf5e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990634"
---
# <a name="cim_container-class"></a><span data-ttu-id="cbe4e-104">\_Класс контейнера CIM</span><span class="sxs-lookup"><span data-stu-id="cbe4e-104">CIM\_Container class</span></span>

<span data-ttu-id="cbe4e-105">Класс **\_ контейнера CIM** представляет связь между содержащимся и содержащимся физическим элементом.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-105">The **CIM\_Container** class represents an association between a contained and a containing physical element.</span></span> <span data-ttu-id="cbe4e-106">Содержащий объект должен быть физическим пакетом.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-106">A containing object must be a physical package.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cbe4e-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cbe4e-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cbe4e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cbe4e-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cbe4e-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbe4e-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbe4e-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Container : CIM_Component
{
  CIM_PhysicalElement REF PartComponent;
  CIM_PhysicalPackage REF GroupComponent;
  string                  LocationWithinContainer;
};
```

## <a name="members"></a><span data-ttu-id="cbe4e-112">Члены</span><span class="sxs-lookup"><span data-stu-id="cbe4e-112">Members</span></span>

<span data-ttu-id="cbe4e-113">Класс **\_ контейнера CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cbe4e-113">The **CIM\_Container** class has these types of members:</span></span>

-   [<span data-ttu-id="cbe4e-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="cbe4e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cbe4e-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="cbe4e-115">Properties</span></span>

<span data-ttu-id="cbe4e-116">Класс **\_ контейнера CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-116">The **CIM\_Container** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cbe4e-117">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbe4e-118">Тип данных: **CIM \_ фисикалпаккаже**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-118">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="cbe4e-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cbe4e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbe4e-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="cbe4e-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="cbe4e-121">[**\_ Фисикалпаккаже CIM**](cim-physicalpackage.md) , представляющий физический пакет, содержащий другие физические элементы, включая другие пакеты.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-121">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that represents the physical package that contains other physical elements, including other packages.</span></span>

</dd> <dt>

<span data-ttu-id="cbe4e-122">**локатионвисинконтаинер**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbe4e-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbe4e-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cbe4e-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cbe4e-125">Произвольная строка, представляющая расположение физического элемента в физическом пакете.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="cbe4e-126">Сведения относительно стационарных элементов в контейнере (например, "второй отсек для дисков сверху"), углы, высота и другие данные могут быть записаны в это свойство.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="cbe4e-127">Эта строка может дополнять или использоваться вместо создания экземпляра объекта [**\_ расположения CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="cbe4e-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="cbe4e-128">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-128">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbe4e-129">Тип данных: **CIM \_ фисикалелемент**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-129">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="cbe4e-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cbe4e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbe4e-131">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="cbe4e-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="cbe4e-132">[**\_ Фисикалелемент CIM**](cim-physicalelement.md) , описывающий физический элемент, содержащийся в пакете.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-132">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical element which is contained in the package.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cbe4e-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cbe4e-133">Remarks</span></span>

<span data-ttu-id="cbe4e-134">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-134">WMI does not implement this class.</span></span> <span data-ttu-id="cbe4e-135">Дополнительные сведения о классах, производных от **CIM \_ Container**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="cbe4e-135">For more information about classes derived from **CIM\_Container**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="cbe4e-136">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cbe4e-137">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbe4e-138">Требования</span><span class="sxs-lookup"><span data-stu-id="cbe4e-138">Requirements</span></span>



| <span data-ttu-id="cbe4e-139">Требование</span><span class="sxs-lookup"><span data-stu-id="cbe4e-139">Requirement</span></span> | <span data-ttu-id="cbe4e-140">Значение</span><span class="sxs-lookup"><span data-stu-id="cbe4e-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbe4e-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cbe4e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="cbe4e-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cbe4e-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cbe4e-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cbe4e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="cbe4e-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cbe4e-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cbe4e-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cbe4e-145">Namespace</span></span><br/>                | <span data-ttu-id="cbe4e-146">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cbe4e-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cbe4e-147">MOF</span><span class="sxs-lookup"><span data-stu-id="cbe4e-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cbe4e-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cbe4e-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cbe4e-149">DLL</span><span class="sxs-lookup"><span data-stu-id="cbe4e-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbe4e-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbe4e-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbe4e-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbe4e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbe4e-152">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="cbe4e-152">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

