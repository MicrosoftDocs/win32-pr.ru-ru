---
description: Класс CIM \_ продуктфисикалелементс представляет физические элементы, составляющие продукт.
ms.assetid: cf23098a-f61e-4778-883e-1a5138af3da0
ms.tgt_platform: multiple
title: Класс CIM_ProductPhysicalElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductPhysicalElements
- CIM_ProductPhysicalElements.Component
- CIM_ProductPhysicalElements.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a581293426c421de0dd76636a9f446f245f6ab32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141187"
---
# <a name="cim_productphysicalelements-class"></a><span data-ttu-id="8b543-103">\_Класс CIM продуктфисикалелементс</span><span class="sxs-lookup"><span data-stu-id="8b543-103">CIM\_ProductPhysicalElements class</span></span>

<span data-ttu-id="8b543-104">Класс **CIM \_ продуктфисикалелементс** представляет физические элементы, составляющие продукт.</span><span class="sxs-lookup"><span data-stu-id="8b543-104">The **CIM\_ProductPhysicalElements** class represents the physical elements that make up a product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8b543-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="8b543-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8b543-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8b543-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8b543-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="8b543-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="8b543-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="8b543-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b543-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b543-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{502F00A0-DB2B-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_ProductPhysicalElements
{
  CIM_PhysicalElement REF Component;
  CIM_Product         REF Product;
};
```

## <a name="members"></a><span data-ttu-id="8b543-110">Члены</span><span class="sxs-lookup"><span data-stu-id="8b543-110">Members</span></span>

<span data-ttu-id="8b543-111">Класс **CIM \_ продуктфисикалелементс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8b543-111">The **CIM\_ProductPhysicalElements** class has these types of members:</span></span>

-   [<span data-ttu-id="8b543-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="8b543-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b543-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="8b543-113">Properties</span></span>

<span data-ttu-id="8b543-114">Класс **CIM \_ продуктфисикалелементс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8b543-114">The **CIM\_ProductPhysicalElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b543-115">**Компонент**</span><span class="sxs-lookup"><span data-stu-id="8b543-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b543-116">Тип данных: **CIM \_ фисикалелемент**</span><span class="sxs-lookup"><span data-stu-id="8b543-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="8b543-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8b543-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b543-118">Ссылка на физический элемент, который является частью продукта.</span><span class="sxs-lookup"><span data-stu-id="8b543-118">Reference to the physical element that is part of the product.</span></span>

</dd> <dt>

<span data-ttu-id="8b543-119">**Продукт**</span><span class="sxs-lookup"><span data-stu-id="8b543-119">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b543-120">Тип данных: **\_ продукт CIM**</span><span class="sxs-lookup"><span data-stu-id="8b543-120">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="8b543-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8b543-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b543-122">Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="8b543-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="8b543-123">Ссылка на продукт.</span><span class="sxs-lookup"><span data-stu-id="8b543-123">Reference to the product.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b543-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b543-124">Remarks</span></span>

<span data-ttu-id="8b543-125">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="8b543-125">WMI does not implement this class.</span></span>

<span data-ttu-id="8b543-126">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="8b543-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8b543-127">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="8b543-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b543-128">Требования</span><span class="sxs-lookup"><span data-stu-id="8b543-128">Requirements</span></span>



| <span data-ttu-id="8b543-129">Требование</span><span class="sxs-lookup"><span data-stu-id="8b543-129">Requirement</span></span> | <span data-ttu-id="8b543-130">Значение</span><span class="sxs-lookup"><span data-stu-id="8b543-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b543-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b543-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8b543-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b543-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8b543-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b543-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8b543-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b543-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8b543-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8b543-135">Namespace</span></span><br/>                | <span data-ttu-id="8b543-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8b543-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8b543-137">MOF</span><span class="sxs-lookup"><span data-stu-id="8b543-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b543-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b543-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b543-139">DLL</span><span class="sxs-lookup"><span data-stu-id="8b543-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b543-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b543-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

