---
description: Класс CIM \_ продуктфру представляет связь между продуктом и заменяемым элементом поля (FRU), который предоставляет сведения о компонентах продукта, которые были или заменяются.
ms.assetid: 15d682e5-cd90-4fc4-8fff-e3fe1d2a0ac4
ms.tgt_platform: multiple
title: Класс CIM_ProductFRU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductFRU
- CIM_ProductFRU.FRU
- CIM_ProductFRU.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b141d16adb50c5bc3f8d6be682a90aa4921061ef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141190"
---
# <a name="cim_productfru-class"></a><span data-ttu-id="65440-103">\_Класс CIM продуктфру</span><span class="sxs-lookup"><span data-stu-id="65440-103">CIM\_ProductFRU class</span></span>

<span data-ttu-id="65440-104">Класс **CIM \_ продуктфру** представляет связь между продуктом и заменяемым ЭЛЕМЕНТОМ поля (FRU), который предоставляет сведения о компонентах продукта, которые были или заменяются.</span><span class="sxs-lookup"><span data-stu-id="65440-104">The **CIM\_ProductFRU** class represents an association between the product and a field replaceable unit (FRU), which provides information about product components that have been, or are being replaced.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65440-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="65440-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="65440-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="65440-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="65440-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="65440-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="65440-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="65440-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="65440-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65440-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{EB98A1B2-DB36-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductFRU
{
  CIM_FRU     REF FRU;
  CIM_Product REF Product;
};
```

## <a name="members"></a><span data-ttu-id="65440-110">Члены</span><span class="sxs-lookup"><span data-stu-id="65440-110">Members</span></span>

<span data-ttu-id="65440-111">Класс **CIM \_ продуктфру** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="65440-111">The **CIM\_ProductFRU** class has these types of members:</span></span>

-   [<span data-ttu-id="65440-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="65440-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="65440-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="65440-113">Properties</span></span>

<span data-ttu-id="65440-114">Класс **CIM \_ продуктфру** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="65440-114">The **CIM\_ProductFRU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="65440-115">**ЭКСПЛУАТАЦИИ**</span><span class="sxs-lookup"><span data-stu-id="65440-115">**FRU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65440-116">Тип данных: **CIM \_ FRU**</span><span class="sxs-lookup"><span data-stu-id="65440-116">Data type: **CIM\_FRU**</span></span>
</dt> <dt>

<span data-ttu-id="65440-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65440-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65440-118">Ссылка на FRU.</span><span class="sxs-lookup"><span data-stu-id="65440-118">Reference to the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="65440-119">**Продукт**</span><span class="sxs-lookup"><span data-stu-id="65440-119">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65440-120">Тип данных: **\_ продукт CIM**</span><span class="sxs-lookup"><span data-stu-id="65440-120">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="65440-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65440-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65440-122">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="65440-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="65440-123">Ссылка на продукт, к которому применяется FRU.</span><span class="sxs-lookup"><span data-stu-id="65440-123">Reference to the product to which the FRU is applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65440-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65440-124">Remarks</span></span>

<span data-ttu-id="65440-125">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="65440-125">WMI does not implement this class.</span></span>

<span data-ttu-id="65440-126">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="65440-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="65440-127">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="65440-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="65440-128">Требования</span><span class="sxs-lookup"><span data-stu-id="65440-128">Requirements</span></span>



| <span data-ttu-id="65440-129">Требование</span><span class="sxs-lookup"><span data-stu-id="65440-129">Requirement</span></span> | <span data-ttu-id="65440-130">Значение</span><span class="sxs-lookup"><span data-stu-id="65440-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65440-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65440-131">Minimum supported client</span></span><br/> | <span data-ttu-id="65440-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65440-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="65440-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65440-133">Minimum supported server</span></span><br/> | <span data-ttu-id="65440-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65440-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="65440-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="65440-135">Namespace</span></span><br/>                | <span data-ttu-id="65440-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="65440-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="65440-137">MOF</span><span class="sxs-lookup"><span data-stu-id="65440-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65440-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65440-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="65440-139">DLL</span><span class="sxs-lookup"><span data-stu-id="65440-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65440-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65440-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

