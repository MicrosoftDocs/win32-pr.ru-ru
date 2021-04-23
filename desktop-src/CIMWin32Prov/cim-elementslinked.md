---
description: Ассоциация CIM \_ елементслинкед представляет физические элементы, которые соединяются физической связью.
ms.assetid: b9e1d11e-6f89-4d7a-9b5c-01161e7c1bdf
ms.tgt_platform: multiple
title: Класс CIM_ElementsLinked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementsLinked
- CIM_ElementsLinked.Dependent
- CIM_ElementsLinked.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 353809056d1ca3bae710272b02c2636a3f02eef1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655918"
---
# <a name="cim_elementslinked-class"></a><span data-ttu-id="5b99e-103">\_Класс CIM елементслинкед</span><span class="sxs-lookup"><span data-stu-id="5b99e-103">CIM\_ElementsLinked class</span></span>

<span data-ttu-id="5b99e-104">Ассоциация **CIM \_ елементслинкед** представляет физические элементы, которые соединяются физической связью.</span><span class="sxs-lookup"><span data-stu-id="5b99e-104">The **CIM\_ElementsLinked** association represents physical elements that are cabled together by a physical link.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b99e-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="5b99e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5b99e-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5b99e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5b99e-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="5b99e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5b99e-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="5b99e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b99e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b99e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B83-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementsLinked : CIM_Dependency
{
  CIM_PhysicalElement REF Dependent;
  CIM_PhysicalLink    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="5b99e-110">Члены</span><span class="sxs-lookup"><span data-stu-id="5b99e-110">Members</span></span>

<span data-ttu-id="5b99e-111">Класс **CIM \_ елементслинкед** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5b99e-111">The **CIM\_ElementsLinked** class has these types of members:</span></span>

-   [<span data-ttu-id="5b99e-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="5b99e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b99e-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="5b99e-113">Properties</span></span>

<span data-ttu-id="5b99e-114">Класс **CIM \_ елементслинкед** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5b99e-114">The **CIM\_ElementsLinked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5b99e-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="5b99e-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b99e-116">Тип данных: **CIM \_ фисикаллинк**</span><span class="sxs-lookup"><span data-stu-id="5b99e-116">Data type: **CIM\_PhysicalLink**</span></span>
</dt> <dt>

<span data-ttu-id="5b99e-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b99e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b99e-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="5b99e-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="5b99e-119">[**\_ Фисикаллинк CIM**](cim-physicallink.md) , описывающий физическую связь.</span><span class="sxs-lookup"><span data-stu-id="5b99e-119">A [**CIM\_PhysicalLink**](cim-physicallink.md) that describes the physical link.</span></span>

</dd> <dt>

<span data-ttu-id="5b99e-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="5b99e-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b99e-121">Тип данных: **CIM \_ фисикалелемент**</span><span class="sxs-lookup"><span data-stu-id="5b99e-121">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="5b99e-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b99e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b99e-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="5b99e-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5b99e-124">[**\_ Фисикалелемент CIM**](cim-physicalelement.md) , описывающий связанный физический элемент.</span><span class="sxs-lookup"><span data-stu-id="5b99e-124">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical element that is linked.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b99e-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5b99e-125">Remarks</span></span>

<span data-ttu-id="5b99e-126">Класс **CIM \_ елементслинкед** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="5b99e-126">The **CIM\_ElementsLinked** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="5b99e-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="5b99e-127">WMI does not implement this class.</span></span>

<span data-ttu-id="5b99e-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="5b99e-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5b99e-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="5b99e-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b99e-130">Требования</span><span class="sxs-lookup"><span data-stu-id="5b99e-130">Requirements</span></span>



| <span data-ttu-id="5b99e-131">Требование</span><span class="sxs-lookup"><span data-stu-id="5b99e-131">Requirement</span></span> | <span data-ttu-id="5b99e-132">Значение</span><span class="sxs-lookup"><span data-stu-id="5b99e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b99e-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b99e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5b99e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b99e-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5b99e-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b99e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5b99e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b99e-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5b99e-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5b99e-137">Namespace</span></span><br/>                | <span data-ttu-id="5b99e-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5b99e-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5b99e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="5b99e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b99e-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b99e-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b99e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5b99e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b99e-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b99e-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b99e-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b99e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b99e-144">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="5b99e-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

