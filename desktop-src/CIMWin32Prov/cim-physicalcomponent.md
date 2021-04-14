---
description: Класс CIM \_ фисикалкомпонент представляет компонент нижнего или базового уровня в пакете. Физический элемент, не являющийся ссылкой, соединителем или пакетом, является потомком (или членом) этого класса.
ms.assetid: 079874cd-5717-4662-a192-0ced16270bbd
ms.tgt_platform: multiple
title: Класс CIM_PhysicalComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalComponent
- CIM_PhysicalComponent.Caption
- CIM_PhysicalComponent.Description
- CIM_PhysicalComponent.InstallDate
- CIM_PhysicalComponent.Name
- CIM_PhysicalComponent.Status
- CIM_PhysicalComponent.CreationClassName
- CIM_PhysicalComponent.Manufacturer
- CIM_PhysicalComponent.Model
- CIM_PhysicalComponent.OtherIdentifyingInfo
- CIM_PhysicalComponent.PartNumber
- CIM_PhysicalComponent.PoweredOn
- CIM_PhysicalComponent.SerialNumber
- CIM_PhysicalComponent.SKU
- CIM_PhysicalComponent.Tag
- CIM_PhysicalComponent.Version
- CIM_PhysicalComponent.HotSwappable
- CIM_PhysicalComponent.Removable
- CIM_PhysicalComponent.Replaceable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e7e1db2c1d314b2d45816801643912dcf3b31bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496395"
---
# <a name="cim_physicalcomponent-class"></a><span data-ttu-id="e3d6b-104">\_Класс CIM фисикалкомпонент</span><span class="sxs-lookup"><span data-stu-id="e3d6b-104">CIM\_PhysicalComponent class</span></span>

<span data-ttu-id="e3d6b-105">Класс **CIM \_ фисикалкомпонент** представляет компонент нижнего или базового уровня в пакете.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-105">The **CIM\_PhysicalComponent** class represents a low-level or basic component within a package.</span></span> <span data-ttu-id="e3d6b-106">Физический элемент, не являющийся ссылкой, соединителем или пакетом, является потомком (или членом) этого класса.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-106">A physical element that is not a link, connector, or package is a descendant (or member) of this class.</span></span> <span data-ttu-id="e3d6b-107">Например, набор микросхем UART на внутренней плате модема будет подклассом (если определены дополнительные свойства или ассоциации) или экземпляром **CIM \_ фисикалкомпонент**.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-107">For example, the UART chipset on an internal modem card would be a subclass (if additional properties or associations are defined) or an instance of **CIM\_PhysicalComponent**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e3d6b-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e3d6b-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e3d6b-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e3d6b-110">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e3d6b-111">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3d6b-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3d6b-112">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B78-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalComponent : CIM_PhysicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
};
```

## <a name="members"></a><span data-ttu-id="e3d6b-113">Члены</span><span class="sxs-lookup"><span data-stu-id="e3d6b-113">Members</span></span>

<span data-ttu-id="e3d6b-114">Класс **CIM \_ фисикалкомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e3d6b-114">The **CIM\_PhysicalComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="e3d6b-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="e3d6b-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e3d6b-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="e3d6b-116">Properties</span></span>

<span data-ttu-id="e3d6b-117">Класс **CIM \_ фисикалкомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-117">The **CIM\_PhysicalComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e3d6b-118">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d6b-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3d6b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-121">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e3d6b-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e3d6b-122">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-122">A short textual description of the object.</span></span>

<span data-ttu-id="e3d6b-123">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e3d6b-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3d6b-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d6b-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3d6b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-127">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e3d6b-127">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e3d6b-128">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e3d6b-129">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e3d6b-130">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e3d6b-130">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3d6b-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d6b-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3d6b-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-134">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="e3d6b-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e3d6b-135">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-135">A textual description of the object.</span></span>

<span data-ttu-id="e3d6b-136">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e3d6b-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3d6b-137">**хотсваппабле**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-137">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d6b-138">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3d6b-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3d6b-140">Если задано **значение true**, пакет может быть горячим заменой.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-140">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="e3d6b-141">Физический пакет может быть горячим заменой, если элемент может быть заменен физически другим (но эквивалентным) одним во время включения содержащего пакета.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-141">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="e3d6b-142">Например, компонент вентилятора может быть рассчитан на горячую замену.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-142">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="e3d6b-143">Все компоненты, доступные для горячей замены, по сути являются съемными и заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-143">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="e3d6b-144">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-144">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d6b-145">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-145">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3d6b-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-147">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="e3d6b-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e3d6b-148">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-148">Indicates when the object was installed.</span></span> <span data-ttu-id="e3d6b-149">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-149">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e3d6b-150">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e3d6b-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3d6b-151">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-151">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d6b-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3d6b-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-154">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e3d6b-154">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e3d6b-155">Имя Организации, ответственной за создание физического элемента.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-155">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="e3d6b-156">Дополнительные сведения см. в описании свойства **Vendor** [**\_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="e3d6b-156">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="e3d6b-157">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e3d6b-157">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3d6b-158">**Модель**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-158">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d6b-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3d6b-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-161">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e3d6b-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e3d6b-162">Имя, по которому обычно известен физический элемент.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-162">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="e3d6b-163">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e3d6b-163">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3d6b-164">**Name**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-164">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d6b-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3d6b-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-167">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="e3d6b-167">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e3d6b-168">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-168">Label by which the object is known.</span></span> <span data-ttu-id="e3d6b-169">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-169">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e3d6b-170">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e3d6b-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3d6b-171">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-171">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d6b-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3d6b-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3d6b-174">Дополнительные данные, помимо сведений о тегах актива, которые можно использовать для поиска физического элемента.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-174">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="e3d6b-175">Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-175">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="e3d6b-176">Обратите внимание, что если доступны только данные с штрих-кодом и они уникальны и могут использоваться в качестве ключа элемента, это свойство будет иметь значение null, а данные штрих-кода будут использоваться в качестве ключа класса в свойстве **Tag** .</span><span class="sxs-lookup"><span data-stu-id="e3d6b-176">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="e3d6b-177">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e3d6b-177">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3d6b-178">**партнумбер**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-178">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d6b-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3d6b-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-181">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e3d6b-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e3d6b-182">Номер детали, назначенный Организацией, ответственной за производство или производство физического элемента.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-182">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="e3d6b-183">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e3d6b-183">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3d6b-184">**повередон**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-184">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d6b-185">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3d6b-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3d6b-187">**Значение true** показывает, что физический элемент включен.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-187">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="e3d6b-188">В противном случае в данный момент он отключен.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-188">Otherwise, it is currently off.</span></span>

<span data-ttu-id="e3d6b-189">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e3d6b-189">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3d6b-190">**Службе**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-190">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d6b-191">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3d6b-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3d6b-193">Если **значение — true**, этот элемент предназначен для размещения в физическом контейнере, в котором он обычно обнаруживается и из него, без нарушения функций общей упаковки.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-193">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="e3d6b-194">Пакет считается съемным, даже если питание должно быть выключено для выполнения удаления.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-194">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="e3d6b-195">Если мощность может быть включена и пакет удален, то элемент является съемным и может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-195">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="e3d6b-196">Например, обновляемая Микросхема процессора является съемной.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-196">For example, an upgradeable processor chip is removable.</span></span>

</dd> <dt>

<span data-ttu-id="e3d6b-197">**Заменяемый**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-197">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d6b-198">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3d6b-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3d6b-200">Если **значение — true**, элемент может быть заменен физически отличающимся.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-200">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="e3d6b-201">Например, некоторые компьютерные системы позволяют обновить основную микросхему процессора до одной из более высоких оценок.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-201">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="e3d6b-202">В этом случае процессор считается заменяемым.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-202">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="e3d6b-203">Все съемные компоненты по сути являются заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-203">All removable components are inherently replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="e3d6b-204">**Номер**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-204">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d6b-205">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3d6b-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-207">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e3d6b-207">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e3d6b-208">Номер, выделенный изготовителем, используемый для распознавания физического элемента.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-208">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="e3d6b-209">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e3d6b-209">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3d6b-210">**SKU**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-210">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d6b-211">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3d6b-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-213">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e3d6b-213">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e3d6b-214">Номер единицы складского учета для этого физического элемента.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-214">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="e3d6b-215">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e3d6b-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3d6b-216">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-216">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d6b-217">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3d6b-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-219">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="e3d6b-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e3d6b-220">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-220">String that indicates the current status of the object.</span></span> <span data-ttu-id="e3d6b-221">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-221">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="e3d6b-222">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="e3d6b-222">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="e3d6b-223">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="e3d6b-223">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="e3d6b-224">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="e3d6b-224">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e3d6b-225">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-225">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e3d6b-226">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-226">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e3d6b-227">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e3d6b-227">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e3d6b-228">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="e3d6b-228">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e3d6b-229">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="e3d6b-229">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e3d6b-230">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="e3d6b-230">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e3d6b-231">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="e3d6b-231">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e3d6b-232">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="e3d6b-232">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e3d6b-233">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="e3d6b-233">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e3d6b-234">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="e3d6b-234">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e3d6b-235">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="e3d6b-235">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e3d6b-236">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="e3d6b-236">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e3d6b-237">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="e3d6b-237">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e3d6b-238">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="e3d6b-238">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e3d6b-239">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="e3d6b-239">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e3d6b-240">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="e3d6b-240">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e3d6b-241">**Тег**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-241">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d6b-242">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3d6b-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-244">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e3d6b-244">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e3d6b-245">Однозначно идентифицирует физический элемент и служит ключом элемента.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-245">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="e3d6b-246">Это свойство может содержать такие сведения, как тег актива или данные серийного номера.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-246">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="e3d6b-247">Ключ для [**CIM \_ фисикалелемент**](cim-physicalelement.md) помещается очень высоким в иерархии объектов для независимого обнаружения оборудования или сущности, независимо от физического размещения в (или в) шкафов, адаптеров и т. д.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-247">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="e3d6b-248">Например, съемный компонент, который можно использовать для горячей замены, может быть взят из содержащего его пакета (с областями видимости) и временно не используется.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-248">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="e3d6b-249">Объект по-прежнему продолжает существовать и даже может быть вставлен в другой контейнер области.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-249">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="e3d6b-250">Ключом для физического элемента является произвольная строка, которая определяется независимо от размещения или расположения, ориентированного на расположение.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-250">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="e3d6b-251">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e3d6b-251">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3d6b-252">**Version**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-252">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d6b-253">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3d6b-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3d6b-255">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e3d6b-255">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e3d6b-256">Указывает версию физического элемента.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-256">Indicates the version of the physical element.</span></span>

<span data-ttu-id="e3d6b-257">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e3d6b-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3d6b-258">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3d6b-258">Remarks</span></span>

<span data-ttu-id="e3d6b-259">Класс **CIM \_ фисикалкомпонент** является производным от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e3d6b-259">The **CIM\_PhysicalComponent** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="e3d6b-260">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-260">WMI does not implement this class.</span></span> <span data-ttu-id="e3d6b-261">Классы WMI, производные от **CIM \_ фисикалкомпонент**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e3d6b-261">For WMI classes derived from **CIM\_PhysicalComponent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e3d6b-262">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-262">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e3d6b-263">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="e3d6b-263">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3d6b-264">Требования</span><span class="sxs-lookup"><span data-stu-id="e3d6b-264">Requirements</span></span>



| <span data-ttu-id="e3d6b-265">Требование</span><span class="sxs-lookup"><span data-stu-id="e3d6b-265">Requirement</span></span> | <span data-ttu-id="e3d6b-266">Значение</span><span class="sxs-lookup"><span data-stu-id="e3d6b-266">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3d6b-267">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3d6b-267">Minimum supported client</span></span><br/> | <span data-ttu-id="e3d6b-268">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3d6b-268">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e3d6b-269">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3d6b-269">Minimum supported server</span></span><br/> | <span data-ttu-id="e3d6b-270">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3d6b-270">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e3d6b-271">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e3d6b-271">Namespace</span></span><br/>                | <span data-ttu-id="e3d6b-272">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e3d6b-272">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e3d6b-273">MOF</span><span class="sxs-lookup"><span data-stu-id="e3d6b-273">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3d6b-274"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3d6b-274"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3d6b-275">DLL</span><span class="sxs-lookup"><span data-stu-id="e3d6b-275">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3d6b-276"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3d6b-276"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3d6b-277">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3d6b-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3d6b-278">**\_ФИСИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="e3d6b-278">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

