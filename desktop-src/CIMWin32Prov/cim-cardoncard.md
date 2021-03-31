---
description: Ассоциация CIM \_ кардонкард описывает связи с картами, которые могут быть подключены к материнским платам, платам адаптера или картам, поддерживающим специальные модули, подобные картам.
ms.assetid: a500b29d-d836-4755-b5df-b296e3cbd2ab
ms.tgt_platform: multiple
title: Класс CIM_CardOnCard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CardOnCard
- CIM_CardOnCard.LocationWithinContainer
- CIM_CardOnCard.PartComponent
- CIM_CardOnCard.GroupComponent
- CIM_CardOnCard.MountOrSlotDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15f94bb8d0f159e71cac44f069f9d8e7d9453509
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423386"
---
# <a name="cim_cardoncard-class"></a><span data-ttu-id="791e9-103">\_Класс CIM кардонкард</span><span class="sxs-lookup"><span data-stu-id="791e9-103">CIM\_CardOnCard class</span></span>

<span data-ttu-id="791e9-104">Ассоциация **CIM \_ кардонкард** описывает связи с картами, которые могут быть подключены к материнским платам, платам адаптера или картам, поддерживающим специальные модули, подобные картам.</span><span class="sxs-lookup"><span data-stu-id="791e9-104">The **CIM\_CardOnCard** association describes relationships about cards that can be plugged into motherboards/baseboards, daughtercards of an adapter, or cards that support special card-like modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="791e9-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="791e9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="791e9-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="791e9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="791e9-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="791e9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="791e9-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="791e9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="791e9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="791e9-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B77-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CardOnCard : CIM_Container
{
  string       LocationWithinContainer;
  CIM_Card REF PartComponent;
  CIM_Card REF GroupComponent;
  string       MountOrSlotDescription;
};
```

## <a name="members"></a><span data-ttu-id="791e9-110">Члены</span><span class="sxs-lookup"><span data-stu-id="791e9-110">Members</span></span>

<span data-ttu-id="791e9-111">Класс **CIM \_ кардонкард** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="791e9-111">The **CIM\_CardOnCard** class has these types of members:</span></span>

-   [<span data-ttu-id="791e9-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="791e9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="791e9-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="791e9-113">Properties</span></span>

<span data-ttu-id="791e9-114">Класс **CIM \_ кардонкард** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="791e9-114">The **CIM\_CardOnCard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="791e9-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="791e9-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="791e9-116">Тип данных: **\_ карта CIM**</span><span class="sxs-lookup"><span data-stu-id="791e9-116">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="791e9-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="791e9-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="791e9-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="791e9-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="791e9-119">[**\_ Карта CIM**](cim-card.md) , которая описывает карточку, в которой размещена другая карта.</span><span class="sxs-lookup"><span data-stu-id="791e9-119">A [**CIM\_Card**](cim-card.md) that describes the card that hosts another card.</span></span>

</dd> <dt>

<span data-ttu-id="791e9-120">**локатионвисинконтаинер**</span><span class="sxs-lookup"><span data-stu-id="791e9-120">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="791e9-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="791e9-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="791e9-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="791e9-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="791e9-123">Произвольная строка, представляющая расположение физического элемента в физическом пакете.</span><span class="sxs-lookup"><span data-stu-id="791e9-123">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="791e9-124">Сведения относительно стационарных элементов в контейнере (например, "второй отсек для дисков сверху"), углы, высота и другие данные могут быть записаны в это свойство.</span><span class="sxs-lookup"><span data-stu-id="791e9-124">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="791e9-125">Эта строка может дополнять или использоваться вместо создания экземпляра объекта [**\_ расположения CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="791e9-125">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="791e9-126">Это свойство наследуется от [**CIM- \_ контейнера**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="791e9-126">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="791e9-127">**маунторслотдескриптион**</span><span class="sxs-lookup"><span data-stu-id="791e9-127">**MountOrSlotDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="791e9-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="791e9-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="791e9-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="791e9-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="791e9-130">Описание и определение того, как карта подключена или подключена к другой плате.</span><span class="sxs-lookup"><span data-stu-id="791e9-130">Describes and identifies how the card is mounted on or plugged into the "other" card.</span></span> <span data-ttu-id="791e9-131">Сведения о слоте могут быть добавлены в это поле и могут быть достаточными для определенных целей управления, что позволяет избежать создания экземпляров объектов соединителей и слотов только для моделирования связей карт с досками размещения или другими адаптерами.</span><span class="sxs-lookup"><span data-stu-id="791e9-131">Slot information can be included in this field and may be sufficient for certain management purposes, which avoids creating instantiations of connector/slot objects just to model the relationship of cards to hosting boards or other adapters.</span></span> <span data-ttu-id="791e9-132">С другой стороны, если сведения о слоте и соединителе доступны, это поле можно использовать для предоставления подробных данных о подключении или вставке слота.</span><span class="sxs-lookup"><span data-stu-id="791e9-132">On the other hand, if slot and connector information is available, this field can be used to provide detailed mounting or slot insertion data.</span></span>

</dd> <dt>

<span data-ttu-id="791e9-133">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="791e9-133">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="791e9-134">Тип данных: **\_ карта CIM**</span><span class="sxs-lookup"><span data-stu-id="791e9-134">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="791e9-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="791e9-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="791e9-136">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="791e9-136">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="791e9-137">[**\_ Карта CIM**](cim-card.md) , которая описывает карточку, подключенную к другой плате или подключенную иным образом.</span><span class="sxs-lookup"><span data-stu-id="791e9-137">A [**CIM\_Card**](cim-card.md) that describes the card that is plugged into or otherwise mounted on another card.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="791e9-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="791e9-138">Remarks</span></span>

<span data-ttu-id="791e9-139">Класс **CIM \_ кардонкард** является производным от [**\_ контейнера CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="791e9-139">The **CIM\_CardOnCard** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="791e9-140">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="791e9-140">WMI does not implement this class.</span></span>

<span data-ttu-id="791e9-141">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="791e9-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="791e9-142">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="791e9-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="791e9-143">Требования</span><span class="sxs-lookup"><span data-stu-id="791e9-143">Requirements</span></span>



| <span data-ttu-id="791e9-144">Требование</span><span class="sxs-lookup"><span data-stu-id="791e9-144">Requirement</span></span> | <span data-ttu-id="791e9-145">Значение</span><span class="sxs-lookup"><span data-stu-id="791e9-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="791e9-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="791e9-146">Minimum supported client</span></span><br/> | <span data-ttu-id="791e9-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="791e9-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="791e9-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="791e9-148">Minimum supported server</span></span><br/> | <span data-ttu-id="791e9-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="791e9-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="791e9-150">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="791e9-150">Namespace</span></span><br/>                | <span data-ttu-id="791e9-151">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="791e9-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="791e9-152">MOF</span><span class="sxs-lookup"><span data-stu-id="791e9-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="791e9-153"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="791e9-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="791e9-154">DLL</span><span class="sxs-lookup"><span data-stu-id="791e9-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="791e9-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="791e9-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="791e9-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="791e9-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="791e9-157">**\_Контейнер CIM**</span><span class="sxs-lookup"><span data-stu-id="791e9-157">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

