---
description: Класс CIM \_ продуктпродуктдепенденци представляет ассоциацию между двумя продуктами, которая указывает, что один из них должен быть установлен или отсутствовать для работы другого. Это концептуально эквивалентно \_ ассоциации CIM сервицесервицедепенденци.
ms.assetid: 898b9993-3bdc-4a7c-98c1-ed960014ace8
ms.tgt_platform: multiple
title: Класс CIM_ProductProductDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductProductDependency
- CIM_ProductProductDependency.DependentProduct
- CIM_ProductProductDependency.RequiredProduct
- CIM_ProductProductDependency.TypeOfDependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 094800b3a2d50d7be4039d5850f9ac1d3f236a40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072393"
---
# <a name="cim_productproductdependency-class"></a><span data-ttu-id="6b757-104">\_Класс CIM продуктпродуктдепенденци</span><span class="sxs-lookup"><span data-stu-id="6b757-104">CIM\_ProductProductDependency class</span></span>

<span data-ttu-id="6b757-105">Класс **CIM \_ продуктпродуктдепенденци** представляет ассоциацию между двумя продуктами, которая указывает, что один из них должен быть установлен или отсутствовать для работы другого.</span><span class="sxs-lookup"><span data-stu-id="6b757-105">The **CIM\_ProductProductDependency** class represents an association between two products, which indicates that one must be installed or absent for the other to function.</span></span> <span data-ttu-id="6b757-106">Это концептуально эквивалентно ассоциации [**CIM \_ сервицесервицедепенденци**](cim-serviceservicedependency.md) .</span><span class="sxs-lookup"><span data-stu-id="6b757-106">This is conceptually equivalent to the [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b757-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="6b757-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6b757-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6b757-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6b757-109">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="6b757-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6b757-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="6b757-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b757-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b757-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{65878E68-DB2B-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductProductDependency
{
  CIM_Product REF DependentProduct;
  CIM_Product REF RequiredProduct;
  uint16          TypeOfDependency;
};
```

## <a name="members"></a><span data-ttu-id="6b757-112">Члены</span><span class="sxs-lookup"><span data-stu-id="6b757-112">Members</span></span>

<span data-ttu-id="6b757-113">Класс **CIM \_ продуктпродуктдепенденци** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6b757-113">The **CIM\_ProductProductDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="6b757-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="6b757-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b757-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="6b757-115">Properties</span></span>

<span data-ttu-id="6b757-116">Класс **CIM \_ продуктпродуктдепенденци** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6b757-116">The **CIM\_ProductProductDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b757-117">**депендентпродукт**</span><span class="sxs-lookup"><span data-stu-id="6b757-117">**DependentProduct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b757-118">Тип данных: **\_ продукт CIM**</span><span class="sxs-lookup"><span data-stu-id="6b757-118">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="6b757-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b757-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b757-120">Ссылка на продукт, который зависит от другого продукта.</span><span class="sxs-lookup"><span data-stu-id="6b757-120">Reference to the product that is dependent on another product.</span></span>

</dd> <dt>

<span data-ttu-id="6b757-121">**рекуиредпродукт**</span><span class="sxs-lookup"><span data-stu-id="6b757-121">**RequiredProduct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b757-122">Тип данных: **\_ продукт CIM**</span><span class="sxs-lookup"><span data-stu-id="6b757-122">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="6b757-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b757-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b757-124">Ссылка на необходимый продукт.</span><span class="sxs-lookup"><span data-stu-id="6b757-124">Reference to the required product.</span></span>

</dd> <dt>

<span data-ttu-id="6b757-125">**типеофдепенденци**</span><span class="sxs-lookup"><span data-stu-id="6b757-125">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b757-126">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b757-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b757-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b757-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b757-128">Характер зависимости продукта.</span><span class="sxs-lookup"><span data-stu-id="6b757-128">Nature of the product dependency.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6b757-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="6b757-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6b757-130">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="6b757-130">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6b757-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="6b757-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6b757-132">Другое</span><span class="sxs-lookup"><span data-stu-id="6b757-132">Other.</span></span>

</dd> <dt>

<span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>

<span data-ttu-id="6b757-133"><span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>**Продукт должен быть установлен** (2)</span><span class="sxs-lookup"><span data-stu-id="6b757-133"><span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>**Product Must Be Installed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6b757-134">Продукт должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="6b757-134">Product must be installed.</span></span>

</dd> <dt>

<span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>

<span data-ttu-id="6b757-135"><span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>**Продукт не должен быть установлен** (3)</span><span class="sxs-lookup"><span data-stu-id="6b757-135"><span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>**Product Must Not Be Installed** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6b757-136">Продукт не должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="6b757-136">Product must not be installed.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b757-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b757-137">Remarks</span></span>

<span data-ttu-id="6b757-138">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="6b757-138">WMI does not implement this class.</span></span>

<span data-ttu-id="6b757-139">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="6b757-139">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6b757-140">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="6b757-140">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b757-141">Требования</span><span class="sxs-lookup"><span data-stu-id="6b757-141">Requirements</span></span>



| <span data-ttu-id="6b757-142">Требование</span><span class="sxs-lookup"><span data-stu-id="6b757-142">Requirement</span></span> | <span data-ttu-id="6b757-143">Значение</span><span class="sxs-lookup"><span data-stu-id="6b757-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b757-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b757-144">Minimum supported client</span></span><br/> | <span data-ttu-id="6b757-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b757-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6b757-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b757-146">Minimum supported server</span></span><br/> | <span data-ttu-id="6b757-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b757-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6b757-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6b757-148">Namespace</span></span><br/>                | <span data-ttu-id="6b757-149">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6b757-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6b757-150">MOF</span><span class="sxs-lookup"><span data-stu-id="6b757-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b757-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b757-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b757-152">DLL</span><span class="sxs-lookup"><span data-stu-id="6b757-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b757-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b757-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




