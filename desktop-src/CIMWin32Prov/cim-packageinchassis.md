---
description: Ассоциация CIM \_ паккажеинчассис представляет собой связь, в которой шасси может содержать другие пакеты, такие как другие шасси и платы.
ms.assetid: 3243bc0f-ce20-4108-b6e3-838bcb8f2fec
ms.tgt_platform: multiple
title: Класс CIM_PackageInChassis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageInChassis
- CIM_PackageInChassis.LocationWithinContainer
- CIM_PackageInChassis.PartComponent
- CIM_PackageInChassis.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 26b65f983970c91d36e8d0a301277c67a2cc5639
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496272"
---
# <a name="cim_packageinchassis-class"></a><span data-ttu-id="50727-103">\_Класс CIM паккажеинчассис</span><span class="sxs-lookup"><span data-stu-id="50727-103">CIM\_PackageInChassis class</span></span>

<span data-ttu-id="50727-104">Ассоциация **CIM \_ паккажеинчассис** представляет собой связь, в которой шасси может содержать другие пакеты, такие как другие шасси и платы.</span><span class="sxs-lookup"><span data-stu-id="50727-104">The **CIM\_PackageInChassis** association represents the relationship in which a chassis can contain other packages, such as other chassis and cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="50727-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="50727-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="50727-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="50727-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="50727-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="50727-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="50727-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="50727-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="50727-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50727-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B74-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageInChassis : CIM_Container
{
  string                  LocationWithinContainer;
  CIM_PhysicalPackage REF PartComponent;
  CIM_Chassis         REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="50727-110">Члены</span><span class="sxs-lookup"><span data-stu-id="50727-110">Members</span></span>

<span data-ttu-id="50727-111">Класс **CIM \_ паккажеинчассис** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="50727-111">The **CIM\_PackageInChassis** class has these types of members:</span></span>

-   [<span data-ttu-id="50727-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="50727-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="50727-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="50727-113">Properties</span></span>

<span data-ttu-id="50727-114">Класс **CIM \_ паккажеинчассис** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="50727-114">The **CIM\_PackageInChassis** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="50727-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="50727-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50727-116">Тип данных: **CIM \_ Chassis**</span><span class="sxs-lookup"><span data-stu-id="50727-116">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="50727-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="50727-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50727-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="50727-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="50727-119">[**\_ Корпус CIM**](cim-chassis.md) , описывающий корпус, который содержит другие физические пакеты.</span><span class="sxs-lookup"><span data-stu-id="50727-119">A [**CIM\_Chassis**](cim-chassis.md) describing the chassis that contains other physical packages.</span></span>

</dd> <dt>

<span data-ttu-id="50727-120">**локатионвисинконтаинер**</span><span class="sxs-lookup"><span data-stu-id="50727-120">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50727-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="50727-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50727-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="50727-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50727-123">Произвольная строка, представляющая расположение физического элемента в физическом пакете.</span><span class="sxs-lookup"><span data-stu-id="50727-123">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="50727-124">Сведения относительно стационарных элементов в контейнере (например, "второй отсек для дисков сверху"), углы, высота и другие данные могут быть записаны в это свойство.</span><span class="sxs-lookup"><span data-stu-id="50727-124">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="50727-125">Эта строка может дополнять или использоваться вместо создания экземпляра объекта [**\_ расположения CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="50727-125">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="50727-126">Это свойство наследуется от [**CIM- \_ контейнера**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="50727-126">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="50727-127">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="50727-127">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50727-128">Тип данных: **CIM \_ фисикалпаккаже**</span><span class="sxs-lookup"><span data-stu-id="50727-128">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="50727-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="50727-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50727-130">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="50727-130">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="50727-131">[**\_ Фисикалпаккаже CIM**](cim-physicalpackage.md) , описывающий физический пакет, содержащийся в корпусе.</span><span class="sxs-lookup"><span data-stu-id="50727-131">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package which is contained in the chassis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50727-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50727-132">Remarks</span></span>

<span data-ttu-id="50727-133">Класс **CIM \_ паккажеинчассис** является производным от [**\_ контейнера CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="50727-133">The **CIM\_PackageInChassis** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="50727-134">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="50727-134">WMI does not implement this class.</span></span>

<span data-ttu-id="50727-135">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="50727-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="50727-136">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="50727-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="50727-137">Требования</span><span class="sxs-lookup"><span data-stu-id="50727-137">Requirements</span></span>



| <span data-ttu-id="50727-138">Требование</span><span class="sxs-lookup"><span data-stu-id="50727-138">Requirement</span></span> | <span data-ttu-id="50727-139">Значение</span><span class="sxs-lookup"><span data-stu-id="50727-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50727-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50727-140">Minimum supported client</span></span><br/> | <span data-ttu-id="50727-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50727-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="50727-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50727-142">Minimum supported server</span></span><br/> | <span data-ttu-id="50727-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50727-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="50727-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="50727-144">Namespace</span></span><br/>                | <span data-ttu-id="50727-145">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="50727-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="50727-146">MOF</span><span class="sxs-lookup"><span data-stu-id="50727-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50727-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50727-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="50727-148">DLL</span><span class="sxs-lookup"><span data-stu-id="50727-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50727-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50727-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50727-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50727-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50727-151">**\_Контейнер CIM**</span><span class="sxs-lookup"><span data-stu-id="50727-151">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

