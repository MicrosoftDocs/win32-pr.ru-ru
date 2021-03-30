---
description: Класс CIM \_ компатиблепродукт представляет ассоциацию между продуктами, которая указывает, взаимодействуют ли два упоминаемых продукта, например, могут ли они быть установлены вместе, а также может ли один из них быть физическим контейнером для другого и т. д.
ms.assetid: d822b052-981a-4a66-8404-b4f5f4681502
ms.tgt_platform: multiple
title: Класс CIM_CompatibleProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CompatibleProduct
- CIM_CompatibleProduct.CompatibilityDescription
- CIM_CompatibleProduct.CompatibleProduct
- CIM_CompatibleProduct.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 94969b1f2e45a27e402e132a0b9593de413a653b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896106"
---
# <a name="cim_compatibleproduct-class"></a><span data-ttu-id="c051b-103">\_Класс CIM компатиблепродукт</span><span class="sxs-lookup"><span data-stu-id="c051b-103">CIM\_CompatibleProduct class</span></span>

<span data-ttu-id="c051b-104">Класс **CIM \_ компатиблепродукт** представляет ассоциацию между продуктами, которая указывает, взаимодействуют ли два упоминаемых продукта, например, могут ли они быть установлены вместе, а также может ли один из них быть физическим контейнером для другого и т. д.</span><span class="sxs-lookup"><span data-stu-id="c051b-104">The **CIM\_CompatibleProduct** class represents an association between products that indicates whether two referenced products are interoperable, such as whether they can be installed together, or whether one can be the physical container for the other, and so on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c051b-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="c051b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c051b-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c051b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c051b-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c051b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c051b-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="c051b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c051b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c051b-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{2F648FBA-DB22-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_CompatibleProduct
{
  string          CompatibilityDescription;
  CIM_Product REF CompatibleProduct;
  CIM_Product REF Product;
};
```

## <a name="members"></a><span data-ttu-id="c051b-110">Члены</span><span class="sxs-lookup"><span data-stu-id="c051b-110">Members</span></span>

<span data-ttu-id="c051b-111">Класс **CIM \_ компатиблепродукт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c051b-111">The **CIM\_CompatibleProduct** class has these types of members:</span></span>

-   [<span data-ttu-id="c051b-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="c051b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c051b-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="c051b-113">Properties</span></span>

<span data-ttu-id="c051b-114">Класс **CIM \_ компатиблепродукт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c051b-114">The **CIM\_CompatibleProduct** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c051b-115">**компатибилитидескриптион**</span><span class="sxs-lookup"><span data-stu-id="c051b-115">**CompatibilityDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c051b-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c051b-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c051b-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c051b-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c051b-118">Произвольная строка, которая определяет, как два ссылочных продукта являются взаимодействующими, совместимыми и существуют ли ограничения совместимости.</span><span class="sxs-lookup"><span data-stu-id="c051b-118">Free-form string that defines how the two referenced products are interoperable, compatible, and whether there are compatibility limitations.</span></span>

</dd> <dt>

<span data-ttu-id="c051b-119">**компатиблепродукт**</span><span class="sxs-lookup"><span data-stu-id="c051b-119">**CompatibleProduct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c051b-120">Тип данных: **\_ продукт CIM**</span><span class="sxs-lookup"><span data-stu-id="c051b-120">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="c051b-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c051b-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c051b-122">Ссылка на совместимый продукт.</span><span class="sxs-lookup"><span data-stu-id="c051b-122">Reference to the compatible product.</span></span>

</dd> <dt>

<span data-ttu-id="c051b-123">**Продукт**</span><span class="sxs-lookup"><span data-stu-id="c051b-123">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c051b-124">Тип данных: **\_ продукт CIM**</span><span class="sxs-lookup"><span data-stu-id="c051b-124">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="c051b-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c051b-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c051b-126">Ссылка на продукт, для которого определены совместимые предложения.</span><span class="sxs-lookup"><span data-stu-id="c051b-126">Reference to the product for which compatible offerings are defined.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c051b-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c051b-127">Remarks</span></span>

<span data-ttu-id="c051b-128">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="c051b-128">WMI does not implement this class.</span></span>

<span data-ttu-id="c051b-129">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="c051b-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c051b-130">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="c051b-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c051b-131">Требования</span><span class="sxs-lookup"><span data-stu-id="c051b-131">Requirements</span></span>



| <span data-ttu-id="c051b-132">Требование</span><span class="sxs-lookup"><span data-stu-id="c051b-132">Requirement</span></span> | <span data-ttu-id="c051b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="c051b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c051b-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c051b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c051b-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c051b-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c051b-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c051b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c051b-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c051b-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c051b-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c051b-138">Namespace</span></span><br/>                | <span data-ttu-id="c051b-139">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c051b-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c051b-140">MOF</span><span class="sxs-lookup"><span data-stu-id="c051b-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c051b-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c051b-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c051b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c051b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c051b-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c051b-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




