---
description: '\_Ассоциация РЕАЛИЗЕСАГГРЕГАТЕПЕКСТЕНТ CIM представляет связь, в которой \_ класс CIM аггрегатепекстент реализован на физическом носителе.'
ms.assetid: 420dde1d-daa8-4cd3-b3fd-c2aefdc1e217
ms.tgt_platform: multiple
title: Класс CIM_RealizesAggregatePExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesAggregatePExtent
- CIM_RealizesAggregatePExtent.Dependent
- CIM_RealizesAggregatePExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb80414134534d09a4030e2e87003a660e69fd9f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655833"
---
# <a name="cim_realizesaggregatepextent-class"></a><span data-ttu-id="28c3c-103">\_Класс CIM реализесаггрегатепекстент</span><span class="sxs-lookup"><span data-stu-id="28c3c-103">CIM\_RealizesAggregatePExtent class</span></span>

<span data-ttu-id="28c3c-104">Ассоциация **\_ реализесаггрегатепекстент CIM** представляет связь, в которой класс [**CIM \_ аггрегатепекстент**](cim-aggregatepextent.md) реализован на физическом носителе.</span><span class="sxs-lookup"><span data-stu-id="28c3c-104">The **CIM\_RealizesAggregatePExtent** association represents the relationship in which the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class is realized on a physical media.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28c3c-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="28c3c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="28c3c-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="28c3c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="28c3c-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="28c3c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="28c3c-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="28c3c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="28c3c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28c3c-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B81-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesAggregatePExtent : CIM_Realizes
{
  CIM_AggregatePExtent REF Dependent;
  CIM_PhysicalMedia    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="28c3c-110">Члены</span><span class="sxs-lookup"><span data-stu-id="28c3c-110">Members</span></span>

<span data-ttu-id="28c3c-111">Класс **CIM \_ реализесаггрегатепекстент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="28c3c-111">The **CIM\_RealizesAggregatePExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="28c3c-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="28c3c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="28c3c-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="28c3c-113">Properties</span></span>

<span data-ttu-id="28c3c-114">Класс **CIM \_ реализесаггрегатепекстент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="28c3c-114">The **CIM\_RealizesAggregatePExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="28c3c-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="28c3c-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28c3c-116">Тип данных: **CIM \_ фисикалмедиа**</span><span class="sxs-lookup"><span data-stu-id="28c3c-116">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="28c3c-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="28c3c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28c3c-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="28c3c-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="28c3c-119">[**\_ Фисикалмедиа CIM**](cim-physicalmedia.md) , описывающий физический носитель, на котором реализован экстент.</span><span class="sxs-lookup"><span data-stu-id="28c3c-119">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="28c3c-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="28c3c-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28c3c-121">Тип данных: **CIM \_ аггрегатепекстент**</span><span class="sxs-lookup"><span data-stu-id="28c3c-121">Data type: **CIM\_AggregatePExtent**</span></span>
</dt> <dt>

<span data-ttu-id="28c3c-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="28c3c-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28c3c-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="28c3c-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="28c3c-124">[**\_ Аггрегатепекстент CIM**](cim-aggregatepextent.md) , расположенный на носителе.</span><span class="sxs-lookup"><span data-stu-id="28c3c-124">The [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) that is located on the media.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28c3c-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28c3c-125">Remarks</span></span>

<span data-ttu-id="28c3c-126">Класс **CIM \_ реализесаггрегатепекстент** является производным от [**CIM \_**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="28c3c-126">The **CIM\_RealizesAggregatePExtent** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="28c3c-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="28c3c-127">WMI does not implement this class.</span></span>

<span data-ttu-id="28c3c-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="28c3c-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="28c3c-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="28c3c-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="28c3c-130">Требования</span><span class="sxs-lookup"><span data-stu-id="28c3c-130">Requirements</span></span>



| <span data-ttu-id="28c3c-131">Требование</span><span class="sxs-lookup"><span data-stu-id="28c3c-131">Requirement</span></span> | <span data-ttu-id="28c3c-132">Значение</span><span class="sxs-lookup"><span data-stu-id="28c3c-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28c3c-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28c3c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="28c3c-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28c3c-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="28c3c-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28c3c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="28c3c-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28c3c-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="28c3c-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="28c3c-137">Namespace</span></span><br/>                | <span data-ttu-id="28c3c-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="28c3c-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="28c3c-139">MOF</span><span class="sxs-lookup"><span data-stu-id="28c3c-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28c3c-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="28c3c-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="28c3c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="28c3c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28c3c-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28c3c-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28c3c-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28c3c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28c3c-144">**\_Реализации CIM**</span><span class="sxs-lookup"><span data-stu-id="28c3c-144">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

