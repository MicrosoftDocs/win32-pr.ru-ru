---
description: '\_Ассоциация ПРОДУКТПАРЕНТЧИЛД CIM определяет иерархию "родители-потомки" между продуктами. Например, продукт может быть объединен с другими продуктами.'
ms.assetid: 244576fd-8dae-4554-b80b-0cac58c93037
ms.tgt_platform: multiple
title: Класс CIM_ProductParentChild
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductParentChild
- CIM_ProductParentChild.Child
- CIM_ProductParentChild.Parent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3a5fd34cc3dffc6d5c8df7f7a76d9cada7856d57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538561"
---
# <a name="cim_productparentchild-class"></a><span data-ttu-id="92192-104">\_Класс CIM продуктпарентчилд</span><span class="sxs-lookup"><span data-stu-id="92192-104">CIM\_ProductParentChild class</span></span>

<span data-ttu-id="92192-105">Ассоциация **\_ продуктпарентчилд CIM** определяет иерархию "родители-потомки" между продуктами.</span><span class="sxs-lookup"><span data-stu-id="92192-105">The **CIM\_ProductParentChild** association defines a parent-child hierarchy among products.</span></span> <span data-ttu-id="92192-106">Например, продукт может быть объединен с другими продуктами.</span><span class="sxs-lookup"><span data-stu-id="92192-106">For example, a product can come bundled with other products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="92192-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="92192-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="92192-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="92192-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="92192-109">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="92192-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="92192-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="92192-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="92192-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92192-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{3E24D5A6-DB2B-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_ProductParentChild
{
  CIM_Product REF Child;
  CIM_Product REF Parent;
};
```

## <a name="members"></a><span data-ttu-id="92192-112">Члены</span><span class="sxs-lookup"><span data-stu-id="92192-112">Members</span></span>

<span data-ttu-id="92192-113">Класс **CIM \_ продуктпарентчилд** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="92192-113">The **CIM\_ProductParentChild** class has these types of members:</span></span>

-   [<span data-ttu-id="92192-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="92192-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92192-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="92192-115">Properties</span></span>

<span data-ttu-id="92192-116">Класс **CIM \_ продуктпарентчилд** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="92192-116">The **CIM\_ProductParentChild** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92192-117">**Дочерний**</span><span class="sxs-lookup"><span data-stu-id="92192-117">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92192-118">Тип данных: **\_ продукт CIM**</span><span class="sxs-lookup"><span data-stu-id="92192-118">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="92192-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92192-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92192-120">Ссылка на дочерний продукт в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="92192-120">Reference to the child product in the association.</span></span>

</dd> <dt>

<span data-ttu-id="92192-121">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="92192-121">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92192-122">Тип данных: **\_ продукт CIM**</span><span class="sxs-lookup"><span data-stu-id="92192-122">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="92192-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92192-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92192-124">Квалификаторы: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="92192-124">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="92192-125">Ссылка на родительский продукт в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="92192-125">Reference to the parent product in the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92192-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92192-126">Remarks</span></span>

<span data-ttu-id="92192-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="92192-127">WMI does not implement this class.</span></span>

<span data-ttu-id="92192-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="92192-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="92192-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="92192-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="92192-130">Требования</span><span class="sxs-lookup"><span data-stu-id="92192-130">Requirements</span></span>



| <span data-ttu-id="92192-131">Требование</span><span class="sxs-lookup"><span data-stu-id="92192-131">Requirement</span></span> | <span data-ttu-id="92192-132">Значение</span><span class="sxs-lookup"><span data-stu-id="92192-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92192-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92192-133">Minimum supported client</span></span><br/> | <span data-ttu-id="92192-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92192-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="92192-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92192-135">Minimum supported server</span></span><br/> | <span data-ttu-id="92192-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92192-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="92192-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="92192-137">Namespace</span></span><br/>                | <span data-ttu-id="92192-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="92192-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="92192-139">MOF</span><span class="sxs-lookup"><span data-stu-id="92192-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92192-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92192-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="92192-141">DLL</span><span class="sxs-lookup"><span data-stu-id="92192-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92192-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92192-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

