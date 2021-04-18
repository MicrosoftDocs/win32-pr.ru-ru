---
description: Класс CIM \_ фисикалпаккаже представляет физические элементы, содержащие или ведущие другие компоненты. Примерами являются корпус стойки или плата адаптера.
ms.assetid: 9182d413-aa7e-4c2f-94fe-12e99980520c
ms.tgt_platform: multiple
title: Класс CIM_PhysicalPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalPackage
- CIM_PhysicalPackage.Caption
- CIM_PhysicalPackage.CreationClassName
- CIM_PhysicalPackage.Depth
- CIM_PhysicalPackage.Description
- CIM_PhysicalPackage.Height
- CIM_PhysicalPackage.HotSwappable
- CIM_PhysicalPackage.InstallDate
- CIM_PhysicalPackage.Manufacturer
- CIM_PhysicalPackage.Model
- CIM_PhysicalPackage.Name
- CIM_PhysicalPackage.OtherIdentifyingInfo
- CIM_PhysicalPackage.PartNumber
- CIM_PhysicalPackage.PoweredOn
- CIM_PhysicalPackage.Removable
- CIM_PhysicalPackage.Replaceable
- CIM_PhysicalPackage.SerialNumber
- CIM_PhysicalPackage.SKU
- CIM_PhysicalPackage.Status
- CIM_PhysicalPackage.Tag
- CIM_PhysicalPackage.Version
- CIM_PhysicalPackage.Weight
- CIM_PhysicalPackage.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1905467fd949e2c18d8be9e7a7bfff39ad8d1477
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656003"
---
# <a name="cim_physicalpackage-class"></a><span data-ttu-id="2d90d-104">\_Класс CIM фисикалпаккаже</span><span class="sxs-lookup"><span data-stu-id="2d90d-104">CIM\_PhysicalPackage class</span></span>

<span data-ttu-id="2d90d-105">Класс **CIM \_ фисикалпаккаже** представляет физические элементы, содержащие или ведущие другие компоненты.</span><span class="sxs-lookup"><span data-stu-id="2d90d-105">The **CIM\_PhysicalPackage** class represents physical elements that contain or host other components.</span></span> <span data-ttu-id="2d90d-106">Примерами являются корпус стойки или плата адаптера.</span><span class="sxs-lookup"><span data-stu-id="2d90d-106">Examples are a rack enclosure or an adapter card.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2d90d-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="2d90d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2d90d-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2d90d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2d90d-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="2d90d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2d90d-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="2d90d-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d90d-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d90d-111">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B6E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalPackage : CIM_PhysicalElement
{
  string   Caption;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="2d90d-112">Члены</span><span class="sxs-lookup"><span data-stu-id="2d90d-112">Members</span></span>

<span data-ttu-id="2d90d-113">Класс **CIM \_ фисикалпаккаже** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2d90d-113">The **CIM\_PhysicalPackage** class has these types of members:</span></span>

-   [<span data-ttu-id="2d90d-114">Методы</span><span class="sxs-lookup"><span data-stu-id="2d90d-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="2d90d-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="2d90d-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2d90d-116">Методы</span><span class="sxs-lookup"><span data-stu-id="2d90d-116">Methods</span></span>

<span data-ttu-id="2d90d-117">Класс **CIM \_ фисикалпаккаже** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2d90d-117">The **CIM\_PhysicalPackage** class has these methods.</span></span>



| <span data-ttu-id="2d90d-118">Метод</span><span class="sxs-lookup"><span data-stu-id="2d90d-118">Method</span></span>                                                                   | <span data-ttu-id="2d90d-119">Описание</span><span class="sxs-lookup"><span data-stu-id="2d90d-119">Description</span></span>                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d90d-120">**Является совместимым**</span><span class="sxs-lookup"><span data-stu-id="2d90d-120">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-physicalpackage.md) | <span data-ttu-id="2d90d-121">Проверяет, может ли связанный физический элемент быть включен в физический пакет или вставлен в него.</span><span class="sxs-lookup"><span data-stu-id="2d90d-121">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="2d90d-122">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="2d90d-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2d90d-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="2d90d-123">Properties</span></span>

<span data-ttu-id="2d90d-124">Класс **CIM \_ фисикалпаккаже** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2d90d-124">The **CIM\_PhysicalPackage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2d90d-125">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="2d90d-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2d90d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-128">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2d90d-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-129">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="2d90d-129">Short textual description of the object.</span></span>

<span data-ttu-id="2d90d-130">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d90d-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d90d-131">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2d90d-131">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2d90d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-134">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2d90d-134">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-135">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2d90d-135">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2d90d-136">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="2d90d-136">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2d90d-137">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d90d-137">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d90d-138">**Depth**</span><span class="sxs-lookup"><span data-stu-id="2d90d-138">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-139">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="2d90d-139">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-141">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="2d90d-141">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-142">Глубина физического пакета в дюймах.</span><span class="sxs-lookup"><span data-stu-id="2d90d-142">Depth of the physical package, in inches.</span></span>

</dd> <dt>

<span data-ttu-id="2d90d-143">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2d90d-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2d90d-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-146">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="2d90d-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-147">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="2d90d-147">Textual description of the object.</span></span>

<span data-ttu-id="2d90d-148">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d90d-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d90d-149">**Height**</span><span class="sxs-lookup"><span data-stu-id="2d90d-149">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-150">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="2d90d-150">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-152">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="2d90d-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-153">Высота физического пакета в дюймах.</span><span class="sxs-lookup"><span data-stu-id="2d90d-153">Height of the physical package, in inches.</span></span>

</dd> <dt>

<span data-ttu-id="2d90d-154">**хотсваппабле**</span><span class="sxs-lookup"><span data-stu-id="2d90d-154">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-155">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2d90d-155">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-157">Если задано **значение true**, пакет может быть горячим заменой.</span><span class="sxs-lookup"><span data-stu-id="2d90d-157">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="2d90d-158">Физический пакет может быть горячим заменой, если элемент может быть заменен физически другим (но эквивалентным) одним во время включения содержащего пакета.</span><span class="sxs-lookup"><span data-stu-id="2d90d-158">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="2d90d-159">Например, компонент вентилятора может быть рассчитан на горячую замену.</span><span class="sxs-lookup"><span data-stu-id="2d90d-159">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="2d90d-160">Все компоненты, доступные для горячей замены, по сути являются съемными и заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="2d90d-160">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="2d90d-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2d90d-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-162">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2d90d-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-164">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="2d90d-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-165">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="2d90d-165">Date and time the object was installed.</span></span> <span data-ttu-id="2d90d-166">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="2d90d-166">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="2d90d-167">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d90d-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d90d-168">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="2d90d-168">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-169">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2d90d-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-171">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2d90d-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-172">Имя Организации, которая создала физический элемент.</span><span class="sxs-lookup"><span data-stu-id="2d90d-172">Name of the organization that produced the physical element.</span></span> <span data-ttu-id="2d90d-173">Дополнительные сведения см. в описании свойства **Vendor** [**\_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="2d90d-173">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="2d90d-174">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d90d-174">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d90d-175">**Модель**</span><span class="sxs-lookup"><span data-stu-id="2d90d-175">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-176">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2d90d-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-178">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2d90d-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-179">Имя, по которому обычно известен физический элемент.</span><span class="sxs-lookup"><span data-stu-id="2d90d-179">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="2d90d-180">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d90d-180">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d90d-181">**Name**</span><span class="sxs-lookup"><span data-stu-id="2d90d-181">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2d90d-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-184">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="2d90d-184">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-185">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="2d90d-185">Label by which the object is known.</span></span> <span data-ttu-id="2d90d-186">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="2d90d-186">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2d90d-187">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d90d-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d90d-188">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="2d90d-188">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2d90d-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-191">Дополнительные данные, помимо сведений о тегах актива, которые можно использовать для поиска физического элемента.</span><span class="sxs-lookup"><span data-stu-id="2d90d-191">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="2d90d-192">Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива.</span><span class="sxs-lookup"><span data-stu-id="2d90d-192">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="2d90d-193">Обратите внимание, что если доступны только данные с штрих-кодом и они уникальны и могут использоваться в качестве ключа элемента, это свойство будет иметь значение null, а данные штрих-кода будут использоваться в качестве ключа класса в свойстве **Tag** .</span><span class="sxs-lookup"><span data-stu-id="2d90d-193">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="2d90d-194">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d90d-194">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d90d-195">**партнумбер**</span><span class="sxs-lookup"><span data-stu-id="2d90d-195">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-196">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2d90d-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-198">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2d90d-198">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-199">Номер детали, назначенный Организацией, которая создала или изготовлена физический элемент.</span><span class="sxs-lookup"><span data-stu-id="2d90d-199">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="2d90d-200">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d90d-200">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d90d-201">**повередон**</span><span class="sxs-lookup"><span data-stu-id="2d90d-201">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-202">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2d90d-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-204">**Значение true** показывает, что физический элемент включен.</span><span class="sxs-lookup"><span data-stu-id="2d90d-204">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="2d90d-205">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d90d-205">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d90d-206">**Службе**</span><span class="sxs-lookup"><span data-stu-id="2d90d-206">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-207">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2d90d-207">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-209">Если **значение — true**, пакет предназначен для размещения в физическом контейнере, в котором он обычно обнаруживается и из него, без нарушения функций общей упаковки.</span><span class="sxs-lookup"><span data-stu-id="2d90d-209">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="2d90d-210">Пакет считается съемным, даже если питание должно быть выключено для выполнения удаления.</span><span class="sxs-lookup"><span data-stu-id="2d90d-210">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="2d90d-211">Если мощность может быть включена и пакет удален, то элемент является съемным и может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="2d90d-211">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="2d90d-212">Например, обновляемая Микросхема процессора является съемной.</span><span class="sxs-lookup"><span data-stu-id="2d90d-212">For example, an upgradeable processor chip is removable.</span></span>

</dd> <dt>

<span data-ttu-id="2d90d-213">**Заменяемый**</span><span class="sxs-lookup"><span data-stu-id="2d90d-213">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-214">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2d90d-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-216">Если **значение — true**, элемент может быть заменен физически отличающимся.</span><span class="sxs-lookup"><span data-stu-id="2d90d-216">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="2d90d-217">Например, некоторые компьютерные системы позволяют обновить основную микросхему процессора до одной из более высоких оценок.</span><span class="sxs-lookup"><span data-stu-id="2d90d-217">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="2d90d-218">В этом случае процессор считается заменяемым.</span><span class="sxs-lookup"><span data-stu-id="2d90d-218">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="2d90d-219">Все съемные компоненты по сути являются заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="2d90d-219">All removable components are inherently replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="2d90d-220">**Номер**</span><span class="sxs-lookup"><span data-stu-id="2d90d-220">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-221">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2d90d-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-223">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2d90d-223">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-224">Номер, выделенный изготовителем, используемый для распознавания физического элемента.</span><span class="sxs-lookup"><span data-stu-id="2d90d-224">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="2d90d-225">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d90d-225">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d90d-226">**SKU**</span><span class="sxs-lookup"><span data-stu-id="2d90d-226">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2d90d-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-229">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2d90d-229">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-230">Номер единицы хранения для физического элемента.</span><span class="sxs-lookup"><span data-stu-id="2d90d-230">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="2d90d-231">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d90d-231">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d90d-232">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="2d90d-232">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-233">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2d90d-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-235">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="2d90d-235">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-236">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="2d90d-236">Current status of the object.</span></span>

<span data-ttu-id="2d90d-237">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d90d-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2d90d-238">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="2d90d-238">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2d90d-239">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="2d90d-239">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2d90d-240">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="2d90d-240">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2d90d-241">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="2d90d-241">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2d90d-242">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="2d90d-242">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2d90d-243">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="2d90d-243">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2d90d-244">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="2d90d-244">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2d90d-245">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="2d90d-245">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2d90d-246">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="2d90d-246">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2d90d-247">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="2d90d-247">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2d90d-248">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="2d90d-248">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2d90d-249">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="2d90d-249">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2d90d-250">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="2d90d-250">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2d90d-251">**Тег**</span><span class="sxs-lookup"><span data-stu-id="2d90d-251">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-252">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2d90d-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-253">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-254">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2d90d-254">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-255">Произвольная строка, однозначно идентифицирующая физический элемент и служащая в качестве ключа элемента.</span><span class="sxs-lookup"><span data-stu-id="2d90d-255">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="2d90d-256">Это свойство может содержать такие сведения, как тег актива или данные серийного номера.</span><span class="sxs-lookup"><span data-stu-id="2d90d-256">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="2d90d-257">Ключ для [**CIM \_ фисикалелемент**](cim-physicalelement.md) помещается очень высоким в иерархии объектов для независимого обнаружения оборудования или сущности, независимо от физического размещения в (или в) шкафов, адаптеров и т. д.</span><span class="sxs-lookup"><span data-stu-id="2d90d-257">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="2d90d-258">Например, съемный компонент, который можно использовать для горячей замены, может быть взят из содержащего его пакета (с областями видимости) и временно не используется.</span><span class="sxs-lookup"><span data-stu-id="2d90d-258">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="2d90d-259">Объект по-прежнему продолжает существовать и даже может быть вставлен в другой контейнер области.</span><span class="sxs-lookup"><span data-stu-id="2d90d-259">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="2d90d-260">Ключом для физического элемента является произвольная строка, которая определяется независимо от размещения или расположения, ориентированного на расположение.</span><span class="sxs-lookup"><span data-stu-id="2d90d-260">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="2d90d-261">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d90d-261">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d90d-262">**Version**</span><span class="sxs-lookup"><span data-stu-id="2d90d-262">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-263">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2d90d-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-264">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-265">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2d90d-265">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-266">Версия физического элемента.</span><span class="sxs-lookup"><span data-stu-id="2d90d-266">Version of the physical element.</span></span>

<span data-ttu-id="2d90d-267">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d90d-267">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d90d-268">**Weight**</span><span class="sxs-lookup"><span data-stu-id="2d90d-268">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-269">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="2d90d-269">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-271">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("фунты")</span><span class="sxs-lookup"><span data-stu-id="2d90d-271">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-272">Вес физического пакета (в фунтах).</span><span class="sxs-lookup"><span data-stu-id="2d90d-272">Weight of the physical package, in pounds.</span></span>

</dd> <dt>

<span data-ttu-id="2d90d-273">**Width**</span><span class="sxs-lookup"><span data-stu-id="2d90d-273">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d90d-274">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="2d90d-274">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d90d-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d90d-276">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="2d90d-276">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="2d90d-277">Ширина физического пакета в дюймах.</span><span class="sxs-lookup"><span data-stu-id="2d90d-277">Width of the physical package, in inches.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d90d-278">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2d90d-278">Remarks</span></span>

<span data-ttu-id="2d90d-279">Класс **CIM \_ фисикалпаккаже** является производным от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d90d-279">The **CIM\_PhysicalPackage** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="2d90d-280">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="2d90d-280">WMI does not implement this class.</span></span> <span data-ttu-id="2d90d-281">Сведения о классах WMI, которые являются производными от **CIM \_ фисикалпаккаже**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2d90d-281">For WMI classes that are derived from **CIM\_PhysicalPackage**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="2d90d-282">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="2d90d-282">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2d90d-283">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="2d90d-283">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d90d-284">Требования</span><span class="sxs-lookup"><span data-stu-id="2d90d-284">Requirements</span></span>



| <span data-ttu-id="2d90d-285">Требование</span><span class="sxs-lookup"><span data-stu-id="2d90d-285">Requirement</span></span> | <span data-ttu-id="2d90d-286">Значение</span><span class="sxs-lookup"><span data-stu-id="2d90d-286">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d90d-287">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d90d-287">Minimum supported client</span></span><br/> | <span data-ttu-id="2d90d-288">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d90d-288">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2d90d-289">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d90d-289">Minimum supported server</span></span><br/> | <span data-ttu-id="2d90d-290">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d90d-290">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2d90d-291">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2d90d-291">Namespace</span></span><br/>                | <span data-ttu-id="2d90d-292">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2d90d-292">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2d90d-293">MOF</span><span class="sxs-lookup"><span data-stu-id="2d90d-293">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d90d-294"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d90d-294"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d90d-295">DLL</span><span class="sxs-lookup"><span data-stu-id="2d90d-295">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d90d-296"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d90d-296"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d90d-297">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d90d-297">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d90d-298">**\_ФИСИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="2d90d-298">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

