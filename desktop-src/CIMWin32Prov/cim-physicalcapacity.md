---
description: Класс CIM \_ фисикалкапаЦити является абстрактным классом, который представляет минимальные и максимальные требования физического элемента и его способность поддерживать различные типы оборудования.
ms.assetid: e422aec0-1830-464e-ac52-2911652165a2
ms.tgt_platform: multiple
title: Класс CIM_PhysicalCapacity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalCapacity
- CIM_PhysicalCapacity.Caption
- CIM_PhysicalCapacity.Description
- CIM_PhysicalCapacity.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50f928f69d34600c0f90865a4df44a5d7697fc89
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990633"
---
# <a name="cim_physicalcapacity-class"></a><span data-ttu-id="7781f-103">\_Класс CIM фисикалкапаЦити</span><span class="sxs-lookup"><span data-stu-id="7781f-103">CIM\_PhysicalCapacity class</span></span>

<span data-ttu-id="7781f-104">Класс **CIM \_ фисикалкапаЦити** является абстрактным классом, который представляет минимальные и максимальные требования физического элемента и его способность поддерживать различные типы оборудования.</span><span class="sxs-lookup"><span data-stu-id="7781f-104">The **CIM\_PhysicalCapacity** class is an abstract class that represents a physical element's minimum and maximum requirements and its ability to support different types of hardware.</span></span> <span data-ttu-id="7781f-105">Например, минимальные и максимальные требования к памяти можно моделировать как подкласс **CIM \_ фисикалкапаЦити**.</span><span class="sxs-lookup"><span data-stu-id="7781f-105">For example, minimum and maximum memory requirements can be modeled as a subclass of **CIM\_PhysicalCapacity**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7781f-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="7781f-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7781f-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7781f-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7781f-108">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="7781f-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="7781f-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="7781f-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7781f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7781f-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B69-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalCapacity
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="7781f-111">Члены</span><span class="sxs-lookup"><span data-stu-id="7781f-111">Members</span></span>

<span data-ttu-id="7781f-112">Класс **CIM \_ фисикалкапаЦити** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7781f-112">The **CIM\_PhysicalCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="7781f-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="7781f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7781f-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="7781f-114">Properties</span></span>

<span data-ttu-id="7781f-115">Класс **CIM \_ фисикалкапаЦити** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7781f-115">The **CIM\_PhysicalCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7781f-116">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="7781f-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7781f-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7781f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7781f-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7781f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7781f-119">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7781f-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7781f-120">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="7781f-120">Short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="7781f-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7781f-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7781f-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7781f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7781f-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7781f-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7781f-124">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="7781f-124">Textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="7781f-125">**Name**</span><span class="sxs-lookup"><span data-stu-id="7781f-125">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7781f-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7781f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7781f-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7781f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7781f-128">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7781f-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7781f-129">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="7781f-129">Label by which the object is known.</span></span> <span data-ttu-id="7781f-130">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="7781f-130">When subclassed, this property can be overridden to be a key property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7781f-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7781f-131">Remarks</span></span>

<span data-ttu-id="7781f-132">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="7781f-132">WMI does not implement this class.</span></span>

<span data-ttu-id="7781f-133">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="7781f-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7781f-134">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="7781f-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7781f-135">Требования</span><span class="sxs-lookup"><span data-stu-id="7781f-135">Requirements</span></span>



| <span data-ttu-id="7781f-136">Требование</span><span class="sxs-lookup"><span data-stu-id="7781f-136">Requirement</span></span> | <span data-ttu-id="7781f-137">Значение</span><span class="sxs-lookup"><span data-stu-id="7781f-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7781f-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7781f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7781f-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7781f-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7781f-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7781f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7781f-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7781f-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7781f-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7781f-142">Namespace</span></span><br/>                | <span data-ttu-id="7781f-143">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7781f-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7781f-144">MOF</span><span class="sxs-lookup"><span data-stu-id="7781f-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7781f-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7781f-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7781f-146">DLL</span><span class="sxs-lookup"><span data-stu-id="7781f-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7781f-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7781f-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

