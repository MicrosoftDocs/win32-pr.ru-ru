---
description: Ассоциация CIM \_ паккажедкомпонент представляет собой явную связь, в которой компонент обычно содержится в физическом пакете, таком как шасси или плата.
ms.assetid: ef0cdbc4-41ee-4517-92ca-61cfcbe64c36
ms.tgt_platform: multiple
title: Класс CIM_PackagedComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackagedComponent
- CIM_PackagedComponent.LocationWithinContainer
- CIM_PackagedComponent.PartComponent
- CIM_PackagedComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b95cbbea60bfbd6bb352e53cfecb8819d99ec24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895517"
---
# <a name="cim_packagedcomponent-class"></a><span data-ttu-id="279e6-103">\_Класс CIM паккажедкомпонент</span><span class="sxs-lookup"><span data-stu-id="279e6-103">CIM\_PackagedComponent class</span></span>

<span data-ttu-id="279e6-104">Ассоциация **CIM \_ паккажедкомпонент** представляет собой явную связь, в которой компонент обычно содержится в физическом пакете, таком как шасси или плата.</span><span class="sxs-lookup"><span data-stu-id="279e6-104">The **CIM\_PackagedComponent** association represents an explicit relationship in which a component is typically contained by a physical package, such as a chassis or card.</span></span>

<span data-ttu-id="279e6-105">**Примечание**  .  Компонент может быть удален из или еще не вставлен в, содержащий его пакет (то есть **съемное** логическое свойство имеет **значение true**).</span><span class="sxs-lookup"><span data-stu-id="279e6-105">**Note**  A component may be removed from, or not yet inserted into, its containing package (that is, the **Removable** Boolean property is **TRUE**).</span></span> <span data-ttu-id="279e6-106">Таким образом, компонент не всегда связан с контейнером.</span><span class="sxs-lookup"><span data-stu-id="279e6-106">Therefore, a component may not always be associated with a container.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="279e6-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="279e6-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="279e6-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="279e6-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="279e6-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="279e6-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="279e6-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="279e6-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="279e6-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="279e6-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B79-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackagedComponent : CIM_Container
{
  string                    LocationWithinContainer;
  CIM_PhysicalComponent REF PartComponent;
  CIM_PhysicalPackage   REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="279e6-112">Члены</span><span class="sxs-lookup"><span data-stu-id="279e6-112">Members</span></span>

<span data-ttu-id="279e6-113">Класс **CIM \_ паккажедкомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="279e6-113">The **CIM\_PackagedComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="279e6-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="279e6-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="279e6-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="279e6-115">Properties</span></span>

<span data-ttu-id="279e6-116">Класс **CIM \_ паккажедкомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="279e6-116">The **CIM\_PackagedComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="279e6-117">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="279e6-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="279e6-118">Тип данных: **CIM \_ фисикалпаккаже**</span><span class="sxs-lookup"><span data-stu-id="279e6-118">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="279e6-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="279e6-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="279e6-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="279e6-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="279e6-121">[**\_ Фисикалпаккаже CIM**](cim-physicalpackage.md) , описывающий физический пакет, содержащий компоненты.</span><span class="sxs-lookup"><span data-stu-id="279e6-121">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package that contains component(s).</span></span>

</dd> <dt>

<span data-ttu-id="279e6-122">**локатионвисинконтаинер**</span><span class="sxs-lookup"><span data-stu-id="279e6-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="279e6-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="279e6-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="279e6-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="279e6-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="279e6-125">Произвольная строка, представляющая расположение физического элемента в физическом пакете.</span><span class="sxs-lookup"><span data-stu-id="279e6-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="279e6-126">Сведения относительно стационарных элементов в контейнере (например, "второй отсек для дисков сверху"), углы, высота и другие данные могут быть записаны в это свойство.</span><span class="sxs-lookup"><span data-stu-id="279e6-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="279e6-127">Эта строка может дополнять или использоваться вместо создания экземпляра объекта [**\_ расположения CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="279e6-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="279e6-128">Это свойство наследуется от [**CIM- \_ контейнера**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="279e6-128">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="279e6-129">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="279e6-129">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="279e6-130">Тип данных: **CIM \_ фисикалкомпонент**</span><span class="sxs-lookup"><span data-stu-id="279e6-130">Data type: **CIM\_PhysicalComponent**</span></span>
</dt> <dt>

<span data-ttu-id="279e6-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="279e6-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="279e6-132">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="279e6-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="279e6-133">[**\_ Фисикалкомпонент CIM**](cim-physicalcomponent.md) , описывающий физический компонент, содержащийся в пакете.</span><span class="sxs-lookup"><span data-stu-id="279e6-133">A [**CIM\_PhysicalComponent**](cim-physicalcomponent.md) describing the physical component which is contained in the package.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="279e6-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="279e6-134">Remarks</span></span>

<span data-ttu-id="279e6-135">Класс **CIM \_ паккажедкомпонент** является производным от [**\_ контейнера CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="279e6-135">The **CIM\_PackagedComponent** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="279e6-136">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="279e6-136">WMI does not implement this class.</span></span>

<span data-ttu-id="279e6-137">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="279e6-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="279e6-138">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="279e6-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="279e6-139">Требования</span><span class="sxs-lookup"><span data-stu-id="279e6-139">Requirements</span></span>



| <span data-ttu-id="279e6-140">Требование</span><span class="sxs-lookup"><span data-stu-id="279e6-140">Requirement</span></span> | <span data-ttu-id="279e6-141">Значение</span><span class="sxs-lookup"><span data-stu-id="279e6-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="279e6-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="279e6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="279e6-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="279e6-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="279e6-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="279e6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="279e6-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="279e6-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="279e6-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="279e6-146">Namespace</span></span><br/>                | <span data-ttu-id="279e6-147">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="279e6-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="279e6-148">MOF</span><span class="sxs-lookup"><span data-stu-id="279e6-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="279e6-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="279e6-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="279e6-150">DLL</span><span class="sxs-lookup"><span data-stu-id="279e6-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="279e6-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="279e6-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="279e6-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="279e6-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="279e6-153">**\_Контейнер CIM**</span><span class="sxs-lookup"><span data-stu-id="279e6-153">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

