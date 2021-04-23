---
description: Ассоциация CIM \_ коллектионофсенсорс представляет двоичные датчики, составляющие датчик с многорежимным состоянием.
ms.assetid: d9494716-bb4e-4aa2-9e3b-e865360c740f
ms.tgt_platform: multiple
title: Класс CIM_CollectionOfSensors
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfSensors
- CIM_CollectionOfSensors.PartComponent
- CIM_CollectionOfSensors.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06f33d3b55c2c35526495d492b0f063fee9c1a0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990639"
---
# <a name="cim_collectionofsensors-class"></a><span data-ttu-id="1b957-103">\_Класс CIM коллектионофсенсорс</span><span class="sxs-lookup"><span data-stu-id="1b957-103">CIM\_CollectionOfSensors class</span></span>

<span data-ttu-id="1b957-104">Ассоциация **CIM \_ коллектионофсенсорс** представляет двоичные датчики, составляющие датчик с многорежимным состоянием.</span><span class="sxs-lookup"><span data-stu-id="1b957-104">The **CIM\_CollectionOfSensors** association represents the binary sensors that make up the multistate sensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1b957-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="1b957-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1b957-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1b957-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1b957-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="1b957-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1b957-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="1b957-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b957-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b957-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2ABF536-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_CollectionOfSensors : CIM_Component
{
  CIM_BinarySensor     REF PartComponent;
  CIM_MultiStateSensor REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="1b957-110">Члены</span><span class="sxs-lookup"><span data-stu-id="1b957-110">Members</span></span>

<span data-ttu-id="1b957-111">Класс **CIM \_ коллектионофсенсорс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1b957-111">The **CIM\_CollectionOfSensors** class has these types of members:</span></span>

-   [<span data-ttu-id="1b957-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="1b957-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1b957-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="1b957-113">Properties</span></span>

<span data-ttu-id="1b957-114">Класс **CIM \_ коллектионофсенсорс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1b957-114">The **CIM\_CollectionOfSensors** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1b957-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="1b957-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b957-116">Тип данных: **CIM \_ мултистатесенсор**</span><span class="sxs-lookup"><span data-stu-id="1b957-116">Data type: **CIM\_MultiStateSensor**</span></span>
</dt> <dt>

<span data-ttu-id="1b957-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1b957-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b957-118">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="1b957-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="1b957-119">[**\_ Мултистатесенсор CIM**](cim-multistatesensor.md) , описывающий датчик с несколькими состояниями.</span><span class="sxs-lookup"><span data-stu-id="1b957-119">A [**CIM\_MultiStateSensor**](cim-multistatesensor.md) that describes the multi-state sensor.</span></span>

</dd> <dt>

<span data-ttu-id="1b957-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="1b957-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b957-121">Тип данных: **CIM \_ бинарисенсор**</span><span class="sxs-lookup"><span data-stu-id="1b957-121">Data type: **CIM\_BinarySensor**</span></span>
</dt> <dt>

<span data-ttu-id="1b957-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1b957-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b957-123">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (2), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="1b957-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (2), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="1b957-124">[**\_ Бинарисенсор CIM**](cim-binarysensor.md) , описывающий двоичный датчик, который является частью датчика с несколькими состояниями.</span><span class="sxs-lookup"><span data-stu-id="1b957-124">A [**CIM\_BinarySensor**](cim-binarysensor.md) that describes a binary sensor that is part of the multi-state sensor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b957-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b957-125">Remarks</span></span>

<span data-ttu-id="1b957-126">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="1b957-126">WMI does not implement this class.</span></span>

<span data-ttu-id="1b957-127">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="1b957-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1b957-128">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="1b957-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b957-129">Требования</span><span class="sxs-lookup"><span data-stu-id="1b957-129">Requirements</span></span>



| <span data-ttu-id="1b957-130">Требование</span><span class="sxs-lookup"><span data-stu-id="1b957-130">Requirement</span></span> | <span data-ttu-id="1b957-131">Значение</span><span class="sxs-lookup"><span data-stu-id="1b957-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b957-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b957-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1b957-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b957-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1b957-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b957-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1b957-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b957-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1b957-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1b957-136">Namespace</span></span><br/>                | <span data-ttu-id="1b957-137">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1b957-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1b957-138">MOF</span><span class="sxs-lookup"><span data-stu-id="1b957-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b957-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b957-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b957-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1b957-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b957-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b957-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b957-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b957-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b957-143">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="1b957-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

