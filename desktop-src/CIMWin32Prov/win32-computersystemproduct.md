---
description: Представляет продукт. Сюда входят программное обеспечение и оборудование, используемые в данной компьютерной системе.
ms.assetid: 6241e703-4ce9-435f-bf36-4388e38a3ea5
ms.tgt_platform: multiple
title: Класс Win32_ComputerSystemProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProduct
- Win32_ComputerSystemProduct.Caption
- Win32_ComputerSystemProduct.Description
- Win32_ComputerSystemProduct.IdentifyingNumber
- Win32_ComputerSystemProduct.Name
- Win32_ComputerSystemProduct.SKUNumber
- Win32_ComputerSystemProduct.Vendor
- Win32_ComputerSystemProduct.Version
- Win32_ComputerSystemProduct.UUID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8cab3dc8679c606076eca2f5cf704867aa9833c9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141159"
---
# <a name="win32_computersystemproduct-class"></a><span data-ttu-id="32904-104">\_Класс Win32 компутерсистемпродукт</span><span class="sxs-lookup"><span data-stu-id="32904-104">Win32\_ComputerSystemProduct class</span></span>

<span data-ttu-id="32904-105">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ компутерсистемпродукт для Win32** представляет продукт.</span><span class="sxs-lookup"><span data-stu-id="32904-105">The **Win32\_ComputerSystemProduct** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a product.</span></span> <span data-ttu-id="32904-106">Сюда входят программное обеспечение и оборудование, используемые в данной компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="32904-106">This includes software and hardware used on this computer system.</span></span>

<span data-ttu-id="32904-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="32904-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="32904-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="32904-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="32904-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32904-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B96-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystemProduct : CIM_Product
{
  string Caption;
  string Description;
  string IdentifyingNumber;
  string Name;
  string SKUNumber;
  string Vendor;
  string Version;
  string UUID;
};
```

## <a name="members"></a><span data-ttu-id="32904-110">Члены</span><span class="sxs-lookup"><span data-stu-id="32904-110">Members</span></span>

<span data-ttu-id="32904-111">Класс **Win32 \_ компутерсистемпродукт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="32904-111">The **Win32\_ComputerSystemProduct** class has these types of members:</span></span>

-   [<span data-ttu-id="32904-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="32904-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32904-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="32904-113">Properties</span></span>

<span data-ttu-id="32904-114">Класс **Win32 \_ компутерсистемпродукт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="32904-114">The **Win32\_ComputerSystemProduct** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32904-115">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="32904-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32904-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="32904-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32904-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="32904-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32904-118">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="32904-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="32904-119">Краткое текстовое описание продукта.</span><span class="sxs-lookup"><span data-stu-id="32904-119">Short textual description for the product.</span></span>

<span data-ttu-id="32904-120">Это свойство наследуется [**от \_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="32904-120">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="32904-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="32904-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32904-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="32904-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32904-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="32904-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32904-124">Текстовое описание продукта.</span><span class="sxs-lookup"><span data-stu-id="32904-124">Textual description of the product.</span></span>

<span data-ttu-id="32904-125">Это свойство наследуется [**от \_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="32904-125">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="32904-126">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="32904-126">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32904-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="32904-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32904-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="32904-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32904-129">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Значение ComponentID \| 001,4 в DMTF</span><span class="sxs-lookup"><span data-stu-id="32904-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="32904-130">Идентификация продукта, например серийный номер программного обеспечения, номер кристалла микросхемы оборудования или (для некоммерческих продуктов) номер проекта.</span><span class="sxs-lookup"><span data-stu-id="32904-130">Product identification, such as a serial number on software, a die number on a hardware chip, or (for noncommercial products) a project number.</span></span>

<span data-ttu-id="32904-131">Это свойство наследуется [**от \_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="32904-131">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="32904-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="32904-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32904-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="32904-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32904-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="32904-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32904-135">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Значение ComponentID \| 001,2 в DMTF</span><span class="sxs-lookup"><span data-stu-id="32904-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="32904-136">Часто используемое название продукта.</span><span class="sxs-lookup"><span data-stu-id="32904-136">Commonly used product name.</span></span>

<span data-ttu-id="32904-137">Это свойство наследуется [**от \_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="32904-137">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="32904-138">**скунумбер**</span><span class="sxs-lookup"><span data-stu-id="32904-138">**SKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32904-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="32904-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32904-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="32904-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32904-141">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="32904-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="32904-142">Сведения о единицах складского учета продукта (SKU).</span><span class="sxs-lookup"><span data-stu-id="32904-142">Product's stock-keeping unit (SKU) information.</span></span>

<span data-ttu-id="32904-143">Это свойство наследуется [**от \_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="32904-143">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="32904-144">**UUID**</span><span class="sxs-lookup"><span data-stu-id="32904-144">**UUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32904-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="32904-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32904-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="32904-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32904-147">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 1 \| UUID")</span><span class="sxs-lookup"><span data-stu-id="32904-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|UUID")</span></span>
</dt> </dl>

<span data-ttu-id="32904-148">Универсальный уникальный идентификатор (UUID) для этого продукта.</span><span class="sxs-lookup"><span data-stu-id="32904-148">Universally unique identifier (UUID) for this product.</span></span> <span data-ttu-id="32904-149">UUID — это 128-разрядный идентификатор, который гарантированно отличается от других созданных UUID.</span><span class="sxs-lookup"><span data-stu-id="32904-149">A UUID is a 128-bit identifier that is guaranteed to be different from other generated UUIDs.</span></span> <span data-ttu-id="32904-150">Если UUID недоступен, используется UUID всех нулей.</span><span class="sxs-lookup"><span data-stu-id="32904-150">If a UUID is not available, a UUID of all zeros is used.</span></span>

<span data-ttu-id="32904-151">Это значение берется из **UUID** в структуре **сведений о системе** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="32904-151">This value comes from the **UUID** member of the **System Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="32904-152">**поставщик**</span><span class="sxs-lookup"><span data-stu-id="32904-152">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32904-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="32904-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32904-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="32904-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32904-155">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Значение ComponentID \| 001,1 в DMTF</span><span class="sxs-lookup"><span data-stu-id="32904-155">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="32904-156">Название поставщика продукта или сущность, которая продает продукт (изготовитель, Торговый посредник, поставщик вычислительной техники и т. д.).</span><span class="sxs-lookup"><span data-stu-id="32904-156">Name of the product's supplier, or the entity selling the product (the manufacturer, reseller, OEM, and so on).</span></span>

<span data-ttu-id="32904-157">Это свойство наследуется [**от \_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="32904-157">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="32904-158">**Version**</span><span class="sxs-lookup"><span data-stu-id="32904-158">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32904-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="32904-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32904-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="32904-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32904-161">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Значение ComponentID \| 001,3 в DMTF</span><span class="sxs-lookup"><span data-stu-id="32904-161">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="32904-162">Сведения о версии продукта.</span><span class="sxs-lookup"><span data-stu-id="32904-162">Product version information.</span></span>

<span data-ttu-id="32904-163">Это свойство наследуется [**от \_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="32904-163">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32904-164">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32904-164">Remarks</span></span>

<span data-ttu-id="32904-165">Класс **Win32 \_ компутерсистемпродукт** является производным от [**\_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="32904-165">The **Win32\_ComputerSystemProduct** class is derived from [**CIM\_Product**](cim-product.md).</span></span>

## <a name="examples"></a><span data-ttu-id="32904-166">Примеры</span><span class="sxs-lookup"><span data-stu-id="32904-166">Examples</span></span>

<span data-ttu-id="32904-167">Пример [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell в коллекции TechNet использует для получения списка нерабочего оборудования, использующего инструментарий WMI, в **Win32 \_ компутерсистемпродукт** .</span><span class="sxs-lookup"><span data-stu-id="32904-167">The [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell sample on TechNet Gallery uses to **Win32\_ComputerSystemProduct** to retrieve a list of non-working hardware using WMI.</span></span>

## <a name="requirements"></a><span data-ttu-id="32904-168">Требования</span><span class="sxs-lookup"><span data-stu-id="32904-168">Requirements</span></span>



| <span data-ttu-id="32904-169">Требование</span><span class="sxs-lookup"><span data-stu-id="32904-169">Requirement</span></span> | <span data-ttu-id="32904-170">Значение</span><span class="sxs-lookup"><span data-stu-id="32904-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32904-171">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32904-171">Minimum supported client</span></span><br/> | <span data-ttu-id="32904-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32904-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="32904-173">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32904-173">Minimum supported server</span></span><br/> | <span data-ttu-id="32904-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32904-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="32904-175">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="32904-175">Namespace</span></span><br/>                | <span data-ttu-id="32904-176">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="32904-176">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="32904-177">MOF</span><span class="sxs-lookup"><span data-stu-id="32904-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32904-178"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32904-178"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="32904-179">DLL</span><span class="sxs-lookup"><span data-stu-id="32904-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32904-180"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32904-180"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32904-181">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32904-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32904-182">**\_Продукт CIM**</span><span class="sxs-lookup"><span data-stu-id="32904-182">**CIM\_Product**</span></span>](cim-product.md)
</dt> <dt>

<span data-ttu-id="32904-183">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="32904-183">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

