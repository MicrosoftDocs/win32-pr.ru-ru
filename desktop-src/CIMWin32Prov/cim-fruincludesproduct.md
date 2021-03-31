---
description: Класс CIM \_ фруинклудеспродукт указывает, что заменяемое поле (FRU) может состоять из других продуктов.
ms.assetid: e57dc7f5-4c5b-4ec4-9300-e080053955cb
ms.tgt_platform: multiple
title: Класс CIM_FRUIncludesProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRUIncludesProduct
- CIM_FRUIncludesProduct.Component
- CIM_FRUIncludesProduct.FRU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 196f0cc1f2e81312e5e695c34e0a492ac7c05389
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104273263"
---
# <a name="cim_fruincludesproduct-class"></a><span data-ttu-id="26320-103">\_Класс CIM фруинклудеспродукт</span><span class="sxs-lookup"><span data-stu-id="26320-103">CIM\_FRUIncludesProduct class</span></span>

<span data-ttu-id="26320-104">Класс **CIM \_ фруинклудеспродукт** указывает, что заменяемое поле (FRU) может состоять из других продуктов.</span><span class="sxs-lookup"><span data-stu-id="26320-104">The **CIM\_FRUIncludesProduct** class indicates that a field replaceable unit (FRU) may be composed of other products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="26320-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="26320-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="26320-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="26320-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="26320-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="26320-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="26320-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="26320-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="26320-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26320-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{87FEEDCA-DB2A-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_FRUIncludesProduct
{
  CIM_Product REF Component;
  CIM_FRU     REF FRU;
};
```

## <a name="members"></a><span data-ttu-id="26320-110">Члены</span><span class="sxs-lookup"><span data-stu-id="26320-110">Members</span></span>

<span data-ttu-id="26320-111">Класс **CIM \_ фруинклудеспродукт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="26320-111">The **CIM\_FRUIncludesProduct** class has these types of members:</span></span>

-   [<span data-ttu-id="26320-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="26320-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26320-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="26320-113">Properties</span></span>

<span data-ttu-id="26320-114">Класс **CIM \_ фруинклудеспродукт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="26320-114">The **CIM\_FRUIncludesProduct** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26320-115">**Компонент**</span><span class="sxs-lookup"><span data-stu-id="26320-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26320-116">Тип данных: **\_ продукт CIM**</span><span class="sxs-lookup"><span data-stu-id="26320-116">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="26320-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="26320-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26320-118">Ссылка на продукт, который является частью FRU.</span><span class="sxs-lookup"><span data-stu-id="26320-118">Reference to the product that is a part of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="26320-119">**ЭКСПЛУАТАЦИИ**</span><span class="sxs-lookup"><span data-stu-id="26320-119">**FRU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26320-120">Тип данных: **CIM \_ FRU**</span><span class="sxs-lookup"><span data-stu-id="26320-120">Data type: **CIM\_FRU**</span></span>
</dt> <dt>

<span data-ttu-id="26320-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="26320-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26320-122">Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="26320-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="26320-123">Ссылка на FRU.</span><span class="sxs-lookup"><span data-stu-id="26320-123">Reference to the FRU.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26320-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26320-124">Remarks</span></span>

<span data-ttu-id="26320-125">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="26320-125">WMI does not implement this class.</span></span>

<span data-ttu-id="26320-126">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="26320-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="26320-127">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="26320-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="26320-128">Требования</span><span class="sxs-lookup"><span data-stu-id="26320-128">Requirements</span></span>



| <span data-ttu-id="26320-129">Требование</span><span class="sxs-lookup"><span data-stu-id="26320-129">Requirement</span></span> | <span data-ttu-id="26320-130">Значение</span><span class="sxs-lookup"><span data-stu-id="26320-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26320-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26320-131">Minimum supported client</span></span><br/> | <span data-ttu-id="26320-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26320-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="26320-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26320-133">Minimum supported server</span></span><br/> | <span data-ttu-id="26320-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26320-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26320-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="26320-135">Namespace</span></span><br/>                | <span data-ttu-id="26320-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="26320-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="26320-137">MOF</span><span class="sxs-lookup"><span data-stu-id="26320-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26320-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26320-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="26320-139">DLL</span><span class="sxs-lookup"><span data-stu-id="26320-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26320-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26320-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

