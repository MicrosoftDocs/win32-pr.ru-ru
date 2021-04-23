---
description: Класс CIM \_ елементкапаЦити связывает \_ объект CIM фисикалкапаЦити с одним или несколькими физическими элементами. Он связывает описание минимальных и максимальных требований к оборудованию (или возможностей) с описываемыми физическими элементами.
ms.assetid: 368c31e8-d56b-4b90-ba3f-20d9b0de8730
ms.tgt_platform: multiple
title: Класс CIM_ElementCapacity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapacity
- CIM_ElementCapacity.Capacity
- CIM_ElementCapacity.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c6ecac913f6d4affcd9784a30d85fa08dfe0486
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496284"
---
# <a name="cim_elementcapacity-class"></a><span data-ttu-id="6cf88-104">\_Класс CIM елементкапаЦити</span><span class="sxs-lookup"><span data-stu-id="6cf88-104">CIM\_ElementCapacity class</span></span>

<span data-ttu-id="6cf88-105">Класс **CIM \_ елементкапаЦити** связывает объект [**CIM \_ фисикалкапаЦити**](cim-physicalcapacity.md) с одним или несколькими физическими элементами.</span><span class="sxs-lookup"><span data-stu-id="6cf88-105">The **CIM\_ElementCapacity** class associates a [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) object with one or more physical elements.</span></span> <span data-ttu-id="6cf88-106">Он связывает описание минимальных и максимальных требований к оборудованию (или возможностей) с описываемыми физическими элементами.</span><span class="sxs-lookup"><span data-stu-id="6cf88-106">It associates a description of the minimum and maximum hardware requirements (or capabilities) to the physical elements being described.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6cf88-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="6cf88-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6cf88-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6cf88-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6cf88-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="6cf88-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6cf88-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="6cf88-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cf88-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6cf88-111">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B6A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementCapacity
{
  CIM_PhysicalCapacity REF Capacity;
  CIM_PhysicalElement  REF Element;
};
```

## <a name="members"></a><span data-ttu-id="6cf88-112">Члены</span><span class="sxs-lookup"><span data-stu-id="6cf88-112">Members</span></span>

<span data-ttu-id="6cf88-113">Класс **CIM \_ елементкапаЦити** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6cf88-113">The **CIM\_ElementCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="6cf88-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="6cf88-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6cf88-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="6cf88-115">Properties</span></span>

<span data-ttu-id="6cf88-116">Класс **CIM \_ елементкапаЦити** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6cf88-116">The **CIM\_ElementCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6cf88-117">**Производительность**</span><span class="sxs-lookup"><span data-stu-id="6cf88-117">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cf88-118">Тип данных: **CIM \_ фисикалкапаЦити**</span><span class="sxs-lookup"><span data-stu-id="6cf88-118">Data type: **CIM\_PhysicalCapacity**</span></span>
</dt> <dt>

<span data-ttu-id="6cf88-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cf88-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6cf88-120">Ссылка на класс [**CIM \_ фисикалкапаЦити**](cim-physicalcapacity.md) , который описывает минимальные и максимальные требования и возможность поддержки различных типов оборудования для физического элемента.</span><span class="sxs-lookup"><span data-stu-id="6cf88-120">Reference to the [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) class that describes the minimum and maximum requirements and the ability to support different types of hardware for a physical element.</span></span>

</dd> <dt>

<span data-ttu-id="6cf88-121">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6cf88-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cf88-122">Тип данных: **CIM \_ фисикалелемент**</span><span class="sxs-lookup"><span data-stu-id="6cf88-122">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="6cf88-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cf88-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cf88-124">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="6cf88-124">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="6cf88-125">Ссылка на описываемый физический элемент.</span><span class="sxs-lookup"><span data-stu-id="6cf88-125">Reference to the physical element being described.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6cf88-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6cf88-126">Remarks</span></span>

<span data-ttu-id="6cf88-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="6cf88-127">WMI does not implement this class.</span></span>

<span data-ttu-id="6cf88-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="6cf88-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6cf88-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="6cf88-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cf88-130">Требования</span><span class="sxs-lookup"><span data-stu-id="6cf88-130">Requirements</span></span>



| <span data-ttu-id="6cf88-131">Требование</span><span class="sxs-lookup"><span data-stu-id="6cf88-131">Requirement</span></span> | <span data-ttu-id="6cf88-132">Значение</span><span class="sxs-lookup"><span data-stu-id="6cf88-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf88-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6cf88-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6cf88-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6cf88-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6cf88-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6cf88-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6cf88-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6cf88-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6cf88-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6cf88-137">Namespace</span></span><br/>                | <span data-ttu-id="6cf88-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6cf88-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6cf88-139">MOF</span><span class="sxs-lookup"><span data-stu-id="6cf88-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6cf88-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6cf88-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6cf88-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6cf88-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cf88-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cf88-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

