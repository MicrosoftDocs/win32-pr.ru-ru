---
description: Класс CIM \_ продуктсуппорт представляет связь между продуктом и поддержкой доступа, которая передает сведения о получении поддержки для продукта.
ms.assetid: 61c62556-0cf3-438c-b9c7-152505bf7ed6
ms.tgt_platform: multiple
title: Класс CIM_ProductSupport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductSupport
- CIM_ProductSupport.Product
- CIM_ProductSupport.Support
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8d1b39e1eef8f9686eee66c629120feaea51c778
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655760"
---
# <a name="cim_productsupport-class"></a><span data-ttu-id="0e34c-103">\_Класс CIM продуктсуппорт</span><span class="sxs-lookup"><span data-stu-id="0e34c-103">CIM\_ProductSupport class</span></span>

<span data-ttu-id="0e34c-104">Класс **CIM \_ продуктсуппорт** представляет связь между продуктом и поддержкой доступа, которая передает сведения о получении поддержки для продукта.</span><span class="sxs-lookup"><span data-stu-id="0e34c-104">The **CIM\_ProductSupport** class represents an association between product and support access that conveys how support is obtained for the product.</span></span> <span data-ttu-id="0e34c-105">Для продукта доступны различные типы поддержки. один и тот же объект поддержки может предоставить помощь для нескольких продуктов.</span><span class="sxs-lookup"><span data-stu-id="0e34c-105">Various types of support are available for a product; the same support object can provide assistance for multiple products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0e34c-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="0e34c-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0e34c-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0e34c-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0e34c-108">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="0e34c-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0e34c-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="0e34c-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e34c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e34c-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8D6D6880-DB2B-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductSupport
{
  CIM_Product       REF Product;
  CIM_SupportAccess REF Support;
};
```

## <a name="members"></a><span data-ttu-id="0e34c-111">Члены</span><span class="sxs-lookup"><span data-stu-id="0e34c-111">Members</span></span>

<span data-ttu-id="0e34c-112">Класс **CIM \_ продуктсуппорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0e34c-112">The **CIM\_ProductSupport** class has these types of members:</span></span>

-   [<span data-ttu-id="0e34c-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="0e34c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e34c-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="0e34c-114">Properties</span></span>

<span data-ttu-id="0e34c-115">Класс **CIM \_ продуктсуппорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0e34c-115">The **CIM\_ProductSupport** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e34c-116">**Продукт**</span><span class="sxs-lookup"><span data-stu-id="0e34c-116">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e34c-117">Тип данных: **\_ продукт CIM**</span><span class="sxs-lookup"><span data-stu-id="0e34c-117">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="0e34c-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e34c-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e34c-119">Ссылка на продукт.</span><span class="sxs-lookup"><span data-stu-id="0e34c-119">Reference to the product.</span></span>

</dd> <dt>

<span data-ttu-id="0e34c-120">**Поддержка**</span><span class="sxs-lookup"><span data-stu-id="0e34c-120">**Support**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e34c-121">Тип данных: **CIM \_ суппортакцесс**</span><span class="sxs-lookup"><span data-stu-id="0e34c-121">Data type: **CIM\_SupportAccess**</span></span>
</dt> <dt>

<span data-ttu-id="0e34c-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e34c-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e34c-123">Ссылка на службу поддержки продукта.</span><span class="sxs-lookup"><span data-stu-id="0e34c-123">Reference to the product support.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e34c-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e34c-124">Remarks</span></span>

<span data-ttu-id="0e34c-125">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="0e34c-125">WMI does not implement this class.</span></span>

<span data-ttu-id="0e34c-126">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="0e34c-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0e34c-127">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0e34c-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e34c-128">Требования</span><span class="sxs-lookup"><span data-stu-id="0e34c-128">Requirements</span></span>



| <span data-ttu-id="0e34c-129">Требование</span><span class="sxs-lookup"><span data-stu-id="0e34c-129">Requirement</span></span> | <span data-ttu-id="0e34c-130">Значение</span><span class="sxs-lookup"><span data-stu-id="0e34c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e34c-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e34c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0e34c-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e34c-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0e34c-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e34c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0e34c-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e34c-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0e34c-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0e34c-135">Namespace</span></span><br/>                | <span data-ttu-id="0e34c-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0e34c-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0e34c-137">MOF</span><span class="sxs-lookup"><span data-stu-id="0e34c-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e34c-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e34c-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e34c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="0e34c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e34c-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e34c-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




