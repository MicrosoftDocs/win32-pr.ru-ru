---
description: '\_Класс продукта CIM является конкретным классом, представляющим коллекцию физических элементов, программных функций и других продуктов, приобретенных как единое целое.'
ms.assetid: beb20f61-de39-4221-8d29-4727104518d5
ms.tgt_platform: multiple
title: Класс CIM_Product
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Product
- CIM_Product.Caption
- CIM_Product.Description
- CIM_Product.IdentifyingNumber
- CIM_Product.Name
- CIM_Product.SKUNumber
- CIM_Product.Vendor
- CIM_Product.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 16c8541a18185d721bbdcbf23acaeb67adf508c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807156"
---
# <a name="cim_product-class"></a><span data-ttu-id="0743a-103">\_Класс продукта CIM</span><span class="sxs-lookup"><span data-stu-id="0743a-103">CIM\_Product class</span></span>

<span data-ttu-id="0743a-104">Класс **\_ продукта CIM** является конкретным классом, представляющим коллекцию физических элементов, программных функций и других продуктов, приобретенных как единое целое.</span><span class="sxs-lookup"><span data-stu-id="0743a-104">The **CIM\_Product** class is a concrete class that represents a collection of physical elements, software features and, other products, acquired as a unit.</span></span> <span data-ttu-id="0743a-105">Приобретение подразумевает соглашение между поставщиком и потребителем, что может повлиять на лицензирование, поддержку и гарантию продукта.</span><span class="sxs-lookup"><span data-stu-id="0743a-105">Acquisition implies an agreement between the supplier and consumer, which can have implications on product licensing, support, and warranty.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0743a-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="0743a-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0743a-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0743a-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0743a-108">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="0743a-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0743a-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="0743a-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0743a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0743a-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B63-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Product
{
  string Caption;
  string Description;
  string IdentifyingNumber;
  string Name;
  string SKUNumber;
  string Vendor;
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="0743a-111">Члены</span><span class="sxs-lookup"><span data-stu-id="0743a-111">Members</span></span>

<span data-ttu-id="0743a-112">Класс **\_ продуктов CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0743a-112">The **CIM\_Product** class has these types of members:</span></span>

-   [<span data-ttu-id="0743a-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="0743a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0743a-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="0743a-114">Properties</span></span>

<span data-ttu-id="0743a-115">Класс **\_ продукта CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0743a-115">The **CIM\_Product** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0743a-116">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="0743a-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0743a-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0743a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0743a-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0743a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0743a-119">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0743a-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0743a-120">Краткое текстовое описание продукта.</span><span class="sxs-lookup"><span data-stu-id="0743a-120">Short textual description for the product.</span></span>

</dd> <dt>

<span data-ttu-id="0743a-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0743a-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0743a-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0743a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0743a-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0743a-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0743a-124">Текстовое описание продукта.</span><span class="sxs-lookup"><span data-stu-id="0743a-124">Textual description of the product.</span></span>

</dd> <dt>

<span data-ttu-id="0743a-125">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="0743a-125">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0743a-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0743a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0743a-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0743a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0743a-128">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Значение ComponentID \| 001,4 в DMTF</span><span class="sxs-lookup"><span data-stu-id="0743a-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="0743a-129">Идентификация продукта, например серийный номер программного обеспечения, номер кристалла микросхемы оборудования или (для некоммерческих продуктов) номер проекта.</span><span class="sxs-lookup"><span data-stu-id="0743a-129">Product identification, such as a serial number on software, a die number on a hardware chip, or (for noncommercial products) a project number.</span></span>

</dd> <dt>

<span data-ttu-id="0743a-130">**Name**</span><span class="sxs-lookup"><span data-stu-id="0743a-130">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0743a-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0743a-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0743a-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0743a-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0743a-133">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Значение ComponentID \| 001,2 в DMTF</span><span class="sxs-lookup"><span data-stu-id="0743a-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="0743a-134">Часто используемое название продукта.</span><span class="sxs-lookup"><span data-stu-id="0743a-134">Commonly used product name.</span></span>

</dd> <dt>

<span data-ttu-id="0743a-135">**скунумбер**</span><span class="sxs-lookup"><span data-stu-id="0743a-135">**SKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0743a-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0743a-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0743a-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0743a-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0743a-138">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0743a-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0743a-139">Сведения о единицах складского учета продукта (SKU).</span><span class="sxs-lookup"><span data-stu-id="0743a-139">Product's stock-keeping unit (SKU) information.</span></span>

</dd> <dt>

<span data-ttu-id="0743a-140">**поставщик**</span><span class="sxs-lookup"><span data-stu-id="0743a-140">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0743a-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0743a-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0743a-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0743a-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0743a-143">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Значение ComponentID \| 001,1 в DMTF</span><span class="sxs-lookup"><span data-stu-id="0743a-143">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="0743a-144">Название поставщика продукта или сущность, которая продает продукт (изготовитель, Торговый посредник, поставщик вычислительной техники и т. д.).</span><span class="sxs-lookup"><span data-stu-id="0743a-144">Name of the product's supplier, or the entity selling the product (the manufacturer, reseller, OEM, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="0743a-145">**Version**</span><span class="sxs-lookup"><span data-stu-id="0743a-145">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0743a-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0743a-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0743a-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0743a-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0743a-148">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Значение ComponentID \| 001,3 в DMTF</span><span class="sxs-lookup"><span data-stu-id="0743a-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="0743a-149">Сведения о версии продукта.</span><span class="sxs-lookup"><span data-stu-id="0743a-149">Product version information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0743a-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0743a-150">Remarks</span></span>

<span data-ttu-id="0743a-151">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="0743a-151">WMI does not implement this class.</span></span> <span data-ttu-id="0743a-152">Сведения о классах WMI, которые являются производными от **\_ продукта CIM**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0743a-152">For WMI classes that are derived from **CIM\_Product**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0743a-153">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="0743a-153">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0743a-154">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0743a-154">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0743a-155">Требования</span><span class="sxs-lookup"><span data-stu-id="0743a-155">Requirements</span></span>



| <span data-ttu-id="0743a-156">Требование</span><span class="sxs-lookup"><span data-stu-id="0743a-156">Requirement</span></span> | <span data-ttu-id="0743a-157">Значение</span><span class="sxs-lookup"><span data-stu-id="0743a-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0743a-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0743a-158">Minimum supported client</span></span><br/> | <span data-ttu-id="0743a-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0743a-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0743a-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0743a-160">Minimum supported server</span></span><br/> | <span data-ttu-id="0743a-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0743a-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0743a-162">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0743a-162">Namespace</span></span><br/>                | <span data-ttu-id="0743a-163">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0743a-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0743a-164">MOF</span><span class="sxs-lookup"><span data-stu-id="0743a-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0743a-165"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0743a-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0743a-166">DLL</span><span class="sxs-lookup"><span data-stu-id="0743a-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0743a-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0743a-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

