---
description: Класс CIM \_ FRU представляет собой определенную поставщиком коллекцию продуктов и физических элементов, связанных с заменяемым элементом поля (FRU) для поддержки, обслуживания или обновления продукта в расположении клиента.
ms.assetid: 4464ec3a-5509-4e15-9020-4abb2edd2570
ms.tgt_platform: multiple
title: Класс CIM_FRU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRU
- CIM_FRU.Caption
- CIM_FRU.Description
- CIM_FRU.FRUNumber
- CIM_FRU.IdentifyingNumber
- CIM_FRU.Name
- CIM_FRU.RevisionLevel
- CIM_FRU.Vendor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d163c3c223159ad8e09aa6e36d63187ff0aa97f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807499"
---
# <a name="cim_fru-class"></a><span data-ttu-id="d8c10-103">\_Класс CIM FRU</span><span class="sxs-lookup"><span data-stu-id="d8c10-103">CIM\_FRU class</span></span>

<span data-ttu-id="d8c10-104">Класс **CIM \_ FRU** представляет собой определенную поставщиком коллекцию продуктов и физических элементов, связанных с заменяемым ЭЛЕМЕНТОМ поля (FRU) для поддержки, обслуживания или обновления продукта в расположении клиента.</span><span class="sxs-lookup"><span data-stu-id="d8c10-104">The **CIM\_FRU** class represents a vendor-defined collection of products and physical elements that are associated with a field replaceable unit (FRU) to support, maintain, or upgrade a product at the customer's location.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d8c10-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="d8c10-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d8c10-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d8c10-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d8c10-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="d8c10-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d8c10-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="d8c10-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8c10-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8c10-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{778C74EE-DB2A-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_FRU
{
  string Caption;
  string Description;
  string FRUNumber;
  string IdentifyingNumber;
  string Name;
  string RevisionLevel;
  string Vendor;
};
```

## <a name="members"></a><span data-ttu-id="d8c10-110">Члены</span><span class="sxs-lookup"><span data-stu-id="d8c10-110">Members</span></span>

<span data-ttu-id="d8c10-111">Класс **CIM \_ FRU** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d8c10-111">The **CIM\_FRU** class has these types of members:</span></span>

-   [<span data-ttu-id="d8c10-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="d8c10-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8c10-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="d8c10-113">Properties</span></span>

<span data-ttu-id="d8c10-114">Класс **CIM \_ FRU** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d8c10-114">The **CIM\_FRU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8c10-115">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="d8c10-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8c10-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d8c10-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8c10-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d8c10-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8c10-118">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d8c10-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d8c10-119">Краткое текстовое описание для FRU.</span><span class="sxs-lookup"><span data-stu-id="d8c10-119">Short textual description for the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="d8c10-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d8c10-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8c10-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d8c10-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8c10-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d8c10-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8c10-123">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| FRU \| 002,3 ")</span><span class="sxs-lookup"><span data-stu-id="d8c10-123">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.3")</span></span>
</dt> </dl>

<span data-ttu-id="d8c10-124">Описание FRU.</span><span class="sxs-lookup"><span data-stu-id="d8c10-124">Description of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="d8c10-125">**фрунумбер**</span><span class="sxs-lookup"><span data-stu-id="d8c10-125">**FRUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8c10-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d8c10-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8c10-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d8c10-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8c10-128">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| FRU \| 002,6 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d8c10-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.6"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d8c10-129">Сведения о заказе FRU.</span><span class="sxs-lookup"><span data-stu-id="d8c10-129">FRU ordering information.</span></span>

</dd> <dt>

<span data-ttu-id="d8c10-130">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="d8c10-130">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8c10-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d8c10-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8c10-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d8c10-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8c10-133">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| FRU \| 002,7 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d8c10-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.7"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d8c10-134">Идентификация программного обеспечения, например серийного номера или номера кристалла на микросхеме оборудования.</span><span class="sxs-lookup"><span data-stu-id="d8c10-134">Identification on software, such as a serial number, or a die number on a hardware chip.</span></span>

</dd> <dt>

<span data-ttu-id="d8c10-135">**Name**</span><span class="sxs-lookup"><span data-stu-id="d8c10-135">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8c10-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d8c10-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8c10-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d8c10-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8c10-138">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d8c10-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d8c10-139">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="d8c10-139">Label by which the object is known.</span></span>

</dd> <dt>

<span data-ttu-id="d8c10-140">**ревисионлевел**</span><span class="sxs-lookup"><span data-stu-id="d8c10-140">**RevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8c10-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d8c10-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8c10-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d8c10-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8c10-143">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| FRU \| 002,8 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d8c10-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.8"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d8c10-144">Уровень редакции FRU.</span><span class="sxs-lookup"><span data-stu-id="d8c10-144">Revision level of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="d8c10-145">**поставщик**</span><span class="sxs-lookup"><span data-stu-id="d8c10-145">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8c10-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d8c10-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8c10-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d8c10-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8c10-148">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| FRU \| 002,4 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d8c10-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.4"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d8c10-149">Имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="d8c10-149">Name of the supplier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8c10-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8c10-150">Remarks</span></span>

<span data-ttu-id="d8c10-151">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="d8c10-151">WMI does not implement this class.</span></span>

<span data-ttu-id="d8c10-152">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="d8c10-152">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d8c10-153">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="d8c10-153">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8c10-154">Требования</span><span class="sxs-lookup"><span data-stu-id="d8c10-154">Requirements</span></span>



| <span data-ttu-id="d8c10-155">Требование</span><span class="sxs-lookup"><span data-stu-id="d8c10-155">Requirement</span></span> | <span data-ttu-id="d8c10-156">Значение</span><span class="sxs-lookup"><span data-stu-id="d8c10-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c10-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d8c10-157">Minimum supported client</span></span><br/> | <span data-ttu-id="d8c10-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8c10-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d8c10-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d8c10-159">Minimum supported server</span></span><br/> | <span data-ttu-id="d8c10-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8c10-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d8c10-161">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d8c10-161">Namespace</span></span><br/>                | <span data-ttu-id="d8c10-162">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d8c10-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d8c10-163">MOF</span><span class="sxs-lookup"><span data-stu-id="d8c10-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8c10-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8c10-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8c10-165">DLL</span><span class="sxs-lookup"><span data-stu-id="d8c10-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8c10-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8c10-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

