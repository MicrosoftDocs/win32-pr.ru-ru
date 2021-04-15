---
description: '\_Ассоциация ПРОДУКТСОФТВАРЕФЕАТУРЕС CIM определяет функции программного обеспечения для конкретного продукта.'
ms.assetid: cd6190f8-d86e-44c8-b506-48016a7c22e1
ms.tgt_platform: multiple
title: Класс CIM_ProductSoftwareFeatures
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductSoftwareFeatures
- CIM_ProductSoftwareFeatures.Component
- CIM_ProductSoftwareFeatures.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2d891d9465688d92c016217cecd8324588026535
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655761"
---
# <a name="cim_productsoftwarefeatures-class"></a><span data-ttu-id="57bf4-103">\_Класс CIM продуктсофтварефеатурес</span><span class="sxs-lookup"><span data-stu-id="57bf4-103">CIM\_ProductSoftwareFeatures class</span></span>

<span data-ttu-id="57bf4-104">Ассоциация **\_ продуктсофтварефеатурес CIM** определяет функции программного обеспечения для конкретного продукта.</span><span class="sxs-lookup"><span data-stu-id="57bf4-104">The **CIM\_ProductSoftwareFeatures** association identifies the software features for a particular product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="57bf4-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="57bf4-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="57bf4-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="57bf4-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="57bf4-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="57bf4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="57bf4-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="57bf4-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="57bf4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57bf4-109">Syntax</span></span>

``` syntax
[UUID("{7C39D12A-DB2B-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_ProductSoftwareFeatures
{
  CIM_SoftwareFeature REF Component;
  CIM_Product         REF Product;
};
```

## <a name="members"></a><span data-ttu-id="57bf4-110">Члены</span><span class="sxs-lookup"><span data-stu-id="57bf4-110">Members</span></span>

<span data-ttu-id="57bf4-111">Класс **CIM \_ продуктсофтварефеатурес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="57bf4-111">The **CIM\_ProductSoftwareFeatures** class has these types of members:</span></span>

-   [<span data-ttu-id="57bf4-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="57bf4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="57bf4-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="57bf4-113">Properties</span></span>

<span data-ttu-id="57bf4-114">Класс **CIM \_ продуктсофтварефеатурес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="57bf4-114">The **CIM\_ProductSoftwareFeatures** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="57bf4-115">**Компонент**</span><span class="sxs-lookup"><span data-stu-id="57bf4-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57bf4-116">Тип данных: **CIM \_ софтварефеатуре**</span><span class="sxs-lookup"><span data-stu-id="57bf4-116">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="57bf4-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="57bf4-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57bf4-118">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**слабая**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="57bf4-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="57bf4-119">Ссылка на компонент.</span><span class="sxs-lookup"><span data-stu-id="57bf4-119">Reference to the component.</span></span>

</dd> <dt>

<span data-ttu-id="57bf4-120">**Продукт**</span><span class="sxs-lookup"><span data-stu-id="57bf4-120">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57bf4-121">Тип данных: **\_ продукт CIM**</span><span class="sxs-lookup"><span data-stu-id="57bf4-121">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="57bf4-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="57bf4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57bf4-123">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="57bf4-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="57bf4-124">Ссылка на продукт.</span><span class="sxs-lookup"><span data-stu-id="57bf4-124">Reference to the product.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57bf4-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="57bf4-125">Remarks</span></span>

<span data-ttu-id="57bf4-126">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="57bf4-126">WMI does not implement this class.</span></span> <span data-ttu-id="57bf4-127">Классы WMI, производные от **CIM \_ продуктсофтварефеатурес**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="57bf4-127">For WMI classes derived from **CIM\_ProductSoftwareFeatures**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="57bf4-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="57bf4-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="57bf4-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="57bf4-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="57bf4-130">Требования</span><span class="sxs-lookup"><span data-stu-id="57bf4-130">Requirements</span></span>



| <span data-ttu-id="57bf4-131">Требование</span><span class="sxs-lookup"><span data-stu-id="57bf4-131">Requirement</span></span> | <span data-ttu-id="57bf4-132">Значение</span><span class="sxs-lookup"><span data-stu-id="57bf4-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57bf4-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57bf4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="57bf4-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57bf4-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="57bf4-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57bf4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="57bf4-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57bf4-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="57bf4-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="57bf4-137">Namespace</span></span><br/>                | <span data-ttu-id="57bf4-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="57bf4-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="57bf4-139">MOF</span><span class="sxs-lookup"><span data-stu-id="57bf4-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57bf4-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57bf4-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="57bf4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="57bf4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57bf4-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57bf4-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

