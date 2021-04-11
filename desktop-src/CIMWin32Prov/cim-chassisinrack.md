---
description: Ассоциация CIM \_ чассисинракк представляет собой &\# 0034, содержащий&\# 0034; отношение между стойкой и содержащимся в ней шасси.
ms.assetid: 1c8a5058-58fe-42e0-b337-7e1a05120789
ms.tgt_platform: multiple
title: Класс CIM_ChassisInRack
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ChassisInRack
- CIM_ChassisInRack.LocationWithinContainer
- CIM_ChassisInRack.PartComponent
- CIM_ChassisInRack.GroupComponent
- CIM_ChassisInRack.BottomU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fd582991df30bc36cd71c4c3fa08d9a5a5153819
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141947"
---
# <a name="cim_chassisinrack-class"></a><span data-ttu-id="5d390-103">\_Класс CIM чассисинракк</span><span class="sxs-lookup"><span data-stu-id="5d390-103">CIM\_ChassisInRack class</span></span>

<span data-ttu-id="5d390-104">Ассоциация **CIM \_ чассисинракк** представляет собой отношение "содержит" между стойкой и содержащимся в ней шасси.</span><span class="sxs-lookup"><span data-stu-id="5d390-104">The **CIM\_ChassisInRack** association represents the "containing" relationship between a rack and a chassis that it contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5d390-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="5d390-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5d390-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5d390-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5d390-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="5d390-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5d390-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="5d390-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d390-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d390-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B73-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ChassisInRack : CIM_Container
{
  string          LocationWithinContainer;
  CIM_Chassis REF PartComponent;
  CIM_Rack    REF GroupComponent;
  uint16          BottomU;
};
```

## <a name="members"></a><span data-ttu-id="5d390-110">Члены</span><span class="sxs-lookup"><span data-stu-id="5d390-110">Members</span></span>

<span data-ttu-id="5d390-111">Класс **CIM \_ чассисинракк** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5d390-111">The **CIM\_ChassisInRack** class has these types of members:</span></span>

-   [<span data-ttu-id="5d390-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="5d390-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d390-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="5d390-113">Properties</span></span>

<span data-ttu-id="5d390-114">Класс **CIM \_ чассисинракк** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5d390-114">The **CIM\_ChassisInRack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d390-115">**боттому**</span><span class="sxs-lookup"><span data-stu-id="5d390-115">**BottomU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d390-116">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d390-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d390-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d390-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d390-118">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("US")</span><span class="sxs-lookup"><span data-stu-id="5d390-118">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Us")</span></span>
</dt> </dl>

<span data-ttu-id="5d390-119">Целое число, указывающее наименьший или нижний уровень "U", в который подключен корпус.</span><span class="sxs-lookup"><span data-stu-id="5d390-119">Integer that indicates the lowest or bottom "U" in which the chassis is mounted.</span></span> <span data-ttu-id="5d390-120">"U" — это стандартная единица измерения для высоты стойки или компонента, монтируемого в стойку, которая равна 1,75 дюйма или 4,445 сантиметров.</span><span class="sxs-lookup"><span data-stu-id="5d390-120">A "U" is a standard unit of measure for the height of a rack, or rack-mountable component, and is equal to 1.75 inches or 4.445 centimeters.</span></span>

</dd> <dt>

<span data-ttu-id="5d390-121">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="5d390-121">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d390-122">Тип данных: **\_ стойка CIM**</span><span class="sxs-lookup"><span data-stu-id="5d390-122">Data type: **CIM\_Rack**</span></span>
</dt> <dt>

<span data-ttu-id="5d390-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d390-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d390-124">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="5d390-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="5d390-125">[**\_ Стойка CIM**](cim-rack.md) , описывающая стойку, которая содержит шасси.</span><span class="sxs-lookup"><span data-stu-id="5d390-125">A [**CIM\_Rack**](cim-rack.md) that describes the rack that contains the chassis.</span></span>

</dd> <dt>

<span data-ttu-id="5d390-126">**локатионвисинконтаинер**</span><span class="sxs-lookup"><span data-stu-id="5d390-126">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d390-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5d390-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d390-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d390-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d390-129">Произвольная строка, представляющая расположение физического элемента в физическом пакете.</span><span class="sxs-lookup"><span data-stu-id="5d390-129">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="5d390-130">Сведения относительно стационарных элементов в контейнере (например, "второй отсек для дисков сверху"), углы, высота и другие данные могут быть записаны в это свойство.</span><span class="sxs-lookup"><span data-stu-id="5d390-130">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="5d390-131">Эта строка может дополнять или использоваться вместо создания экземпляра объекта [**\_ расположения CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="5d390-131">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="5d390-132">Это свойство наследуется от [**CIM- \_ контейнера**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="5d390-132">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d390-133">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="5d390-133">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d390-134">Тип данных: **CIM \_ Chassis**</span><span class="sxs-lookup"><span data-stu-id="5d390-134">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="5d390-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d390-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d390-136">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="5d390-136">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="5d390-137">[**\_ Корпус CIM**](cim-chassis.md) , описывающий корпус, который монтируется в стойку.</span><span class="sxs-lookup"><span data-stu-id="5d390-137">A [**CIM\_Chassis**](cim-chassis.md) that describes the chassis which is mounted in the rack.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d390-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d390-138">Remarks</span></span>

<span data-ttu-id="5d390-139">Класс **CIM \_ чассисинракк** является производным от [**\_ контейнера CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="5d390-139">The **CIM\_ChassisInRack** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="5d390-140">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="5d390-140">WMI does not implement this class.</span></span>

<span data-ttu-id="5d390-141">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="5d390-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5d390-142">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="5d390-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d390-143">Требования</span><span class="sxs-lookup"><span data-stu-id="5d390-143">Requirements</span></span>



| <span data-ttu-id="5d390-144">Требование</span><span class="sxs-lookup"><span data-stu-id="5d390-144">Requirement</span></span> | <span data-ttu-id="5d390-145">Значение</span><span class="sxs-lookup"><span data-stu-id="5d390-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d390-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5d390-146">Minimum supported client</span></span><br/> | <span data-ttu-id="5d390-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d390-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5d390-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5d390-148">Minimum supported server</span></span><br/> | <span data-ttu-id="5d390-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d390-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5d390-150">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5d390-150">Namespace</span></span><br/>                | <span data-ttu-id="5d390-151">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5d390-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5d390-152">MOF</span><span class="sxs-lookup"><span data-stu-id="5d390-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d390-153"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d390-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d390-154">DLL</span><span class="sxs-lookup"><span data-stu-id="5d390-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d390-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d390-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d390-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d390-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d390-157">**\_Контейнер CIM**</span><span class="sxs-lookup"><span data-stu-id="5d390-157">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

