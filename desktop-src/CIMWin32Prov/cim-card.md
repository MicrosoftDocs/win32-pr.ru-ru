---
description: '\_Класс карты CIM представляет тип физического контейнера, который может быть подключен к другой плате или плате размещения или сам по себе является платой или материнской картой в корпусе.'
ms.assetid: edbbfe43-c8e8-4cde-9507-e0a248c15ca7
ms.tgt_platform: multiple
title: Класс CIM_Card
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Card
- CIM_Card.Caption
- CIM_Card.Description
- CIM_Card.InstallDate
- CIM_Card.Name
- CIM_Card.Status
- CIM_Card.CreationClassName
- CIM_Card.Manufacturer
- CIM_Card.Model
- CIM_Card.OtherIdentifyingInfo
- CIM_Card.PartNumber
- CIM_Card.PoweredOn
- CIM_Card.SerialNumber
- CIM_Card.SKU
- CIM_Card.Tag
- CIM_Card.Version
- CIM_Card.Depth
- CIM_Card.Height
- CIM_Card.HotSwappable
- CIM_Card.Removable
- CIM_Card.Replaceable
- CIM_Card.Weight
- CIM_Card.Width
- CIM_Card.HostingBoard
- CIM_Card.RequirementsDescription
- CIM_Card.RequiresDaughterBoard
- CIM_Card.SlotLayout
- CIM_Card.SpecialRequirements
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b10478e5d0e34020f64d8775e857d9fa6af94d11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655950"
---
# <a name="cim_card-class"></a><span data-ttu-id="88fa5-103">\_Класс карты CIM</span><span class="sxs-lookup"><span data-stu-id="88fa5-103">CIM\_Card class</span></span>

<span data-ttu-id="88fa5-104">Класс **\_ карты CIM** представляет тип физического контейнера, который может быть подключен к другой плате или плате размещения или сам по себе является платой или материнской картой в корпусе.</span><span class="sxs-lookup"><span data-stu-id="88fa5-104">The **CIM\_Card** class represents a type of physical container that can be plugged into another card or hosting board, or is itself a hosting board/motherboard in a chassis.</span></span> <span data-ttu-id="88fa5-105">Этот класс включает любой пакет, который способен поддерживать сигналы и предоставляет точку подключения для физических компонентов, таких как микросхемы или другие физические пакеты, такие как другие карты.</span><span class="sxs-lookup"><span data-stu-id="88fa5-105">This class includes any package that is capable of carrying signals and providing a mounting point for physical components, such as chips or other physical packages, such as other cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="88fa5-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="88fa5-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="88fa5-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="88fa5-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="88fa5-108">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="88fa5-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="88fa5-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="88fa5-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="88fa5-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88fa5-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B76-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Card : CIM_PhysicalPackage
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
  real32   Depth;
  real32   Height;
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
  real32   Weight;
  real32   Width;
  boolean  HostingBoard;
  string   RequirementsDescription;
  boolean  RequiresDaughterBoard;
  string   SlotLayout;
  boolean  SpecialRequirements;
};
```

## <a name="members"></a><span data-ttu-id="88fa5-111">Члены</span><span class="sxs-lookup"><span data-stu-id="88fa5-111">Members</span></span>

<span data-ttu-id="88fa5-112">Класс **" \_ карта CIM** " имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="88fa5-112">The **CIM\_Card** class has these types of members:</span></span>

-   [<span data-ttu-id="88fa5-113">Методы</span><span class="sxs-lookup"><span data-stu-id="88fa5-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="88fa5-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="88fa5-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="88fa5-115">Методы</span><span class="sxs-lookup"><span data-stu-id="88fa5-115">Methods</span></span>

<span data-ttu-id="88fa5-116">Класс **\_ карты CIM** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="88fa5-116">The **CIM\_Card** class has these methods.</span></span>



| <span data-ttu-id="88fa5-117">Метод</span><span class="sxs-lookup"><span data-stu-id="88fa5-117">Method</span></span>                                                        | <span data-ttu-id="88fa5-118">Описание</span><span class="sxs-lookup"><span data-stu-id="88fa5-118">Description</span></span>                                                                                                                                    |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88fa5-119">**Является совместимым**</span><span class="sxs-lookup"><span data-stu-id="88fa5-119">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-card.md) | <span data-ttu-id="88fa5-120">Проверяет, может ли связанный физический элемент быть включен или вставлен в физический пакет.</span><span class="sxs-lookup"><span data-stu-id="88fa5-120">Verifies whether the referenced physical element may be contained by or inserted into the physical package.</span></span> <span data-ttu-id="88fa5-121">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="88fa5-121">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="88fa5-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="88fa5-122">Properties</span></span>

<span data-ttu-id="88fa5-123">Класс **\_ карты CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="88fa5-123">The **CIM\_Card** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88fa5-124">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="88fa5-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88fa5-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-127">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="88fa5-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-128">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="88fa5-128">A short textual description of the object.</span></span>

<span data-ttu-id="88fa5-129">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-130">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="88fa5-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88fa5-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-133">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="88fa5-133">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-134">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="88fa5-134">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="88fa5-135">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="88fa5-135">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="88fa5-136">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-136">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-137">**Depth**</span><span class="sxs-lookup"><span data-stu-id="88fa5-137">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-138">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="88fa5-138">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-140">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="88fa5-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-141">Глубина физического пакета в дюймах.</span><span class="sxs-lookup"><span data-stu-id="88fa5-141">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="88fa5-142">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-142">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-143">**Описание**</span><span class="sxs-lookup"><span data-stu-id="88fa5-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88fa5-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-146">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="88fa5-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-147">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="88fa5-147">A textual description of the object.</span></span>

<span data-ttu-id="88fa5-148">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-149">**Height**</span><span class="sxs-lookup"><span data-stu-id="88fa5-149">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-150">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="88fa5-150">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-152">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="88fa5-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-153">Высота физического пакета в дюймах.</span><span class="sxs-lookup"><span data-stu-id="88fa5-153">Height of the physical package, in inches.</span></span>

<span data-ttu-id="88fa5-154">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-154">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-155">**хостингбоард**</span><span class="sxs-lookup"><span data-stu-id="88fa5-155">**HostingBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-156">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="88fa5-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-158">При **значении true** эта карта является материнской платой или, в общем случае, основной платой в корпусе.</span><span class="sxs-lookup"><span data-stu-id="88fa5-158">If **TRUE**, this card is a motherboard or, more generically, a baseboard in a chassis.</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-159">**хотсваппабле**</span><span class="sxs-lookup"><span data-stu-id="88fa5-159">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-160">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="88fa5-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-162">Если задано **значение true**, пакет может быть горячим заменой.</span><span class="sxs-lookup"><span data-stu-id="88fa5-162">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="88fa5-163">Физический пакет может быть горячим заменой, если элемент может быть заменен физически другим (но эквивалентным) одним во время включения содержащего пакета.</span><span class="sxs-lookup"><span data-stu-id="88fa5-163">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="88fa5-164">Например, компонент вентилятора может быть рассчитан на горячую замену.</span><span class="sxs-lookup"><span data-stu-id="88fa5-164">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="88fa5-165">Все компоненты, доступные для горячей замены, по сути являются съемными и заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="88fa5-165">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="88fa5-166">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-166">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-167">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="88fa5-167">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-168">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="88fa5-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-170">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="88fa5-170">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-171">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="88fa5-171">Indicates when the object was installed.</span></span> <span data-ttu-id="88fa5-172">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="88fa5-172">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="88fa5-173">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-174">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="88fa5-174">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88fa5-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-177">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="88fa5-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-178">Имя Организации, ответственной за создание физического элемента.</span><span class="sxs-lookup"><span data-stu-id="88fa5-178">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="88fa5-179">Дополнительные сведения см. в описании свойства **Vendor** [**\_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-179">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="88fa5-180">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-180">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-181">**Модель**</span><span class="sxs-lookup"><span data-stu-id="88fa5-181">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88fa5-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-184">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="88fa5-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-185">Имя, по которому обычно известен физический элемент.</span><span class="sxs-lookup"><span data-stu-id="88fa5-185">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="88fa5-186">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-186">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-187">**Name**</span><span class="sxs-lookup"><span data-stu-id="88fa5-187">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-188">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88fa5-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-190">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="88fa5-190">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-191">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="88fa5-191">Label by which the object is known.</span></span> <span data-ttu-id="88fa5-192">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="88fa5-192">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="88fa5-193">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-194">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="88fa5-194">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-195">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88fa5-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-197">Дополнительные данные, помимо сведений о тегах актива, которые можно использовать для поиска физического элемента.</span><span class="sxs-lookup"><span data-stu-id="88fa5-197">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="88fa5-198">Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива.</span><span class="sxs-lookup"><span data-stu-id="88fa5-198">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="88fa5-199">Обратите внимание, что если доступны только данные с штрих-кодом и они уникальны и могут использоваться в качестве ключа элемента, это свойство будет иметь значение null, а данные штрих-кода будут использоваться в качестве ключа класса в свойстве **Tag** .</span><span class="sxs-lookup"><span data-stu-id="88fa5-199">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="88fa5-200">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-200">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-201">**партнумбер**</span><span class="sxs-lookup"><span data-stu-id="88fa5-201">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-202">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88fa5-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-204">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="88fa5-204">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-205">Номер детали, назначенный Организацией, ответственной за производство или производство физического элемента.</span><span class="sxs-lookup"><span data-stu-id="88fa5-205">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="88fa5-206">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-206">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-207">**повередон**</span><span class="sxs-lookup"><span data-stu-id="88fa5-207">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-208">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="88fa5-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-210">**Значение true** показывает, что физический элемент включен.</span><span class="sxs-lookup"><span data-stu-id="88fa5-210">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="88fa5-211">В противном случае в данный момент он отключен.</span><span class="sxs-lookup"><span data-stu-id="88fa5-211">Otherwise, it is currently off.</span></span>

<span data-ttu-id="88fa5-212">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-212">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-213">**Службе**</span><span class="sxs-lookup"><span data-stu-id="88fa5-213">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-214">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="88fa5-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-216">Если **значение — true**, пакет предназначен для размещения в физическом контейнере, в котором он обычно обнаруживается и из него, без нарушения функций общей упаковки.</span><span class="sxs-lookup"><span data-stu-id="88fa5-216">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="88fa5-217">Пакет считается съемным, даже если питание должно быть выключено для выполнения удаления.</span><span class="sxs-lookup"><span data-stu-id="88fa5-217">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="88fa5-218">Если мощность может быть включена и пакет удален, то элемент является съемным и может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="88fa5-218">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="88fa5-219">Например, обновляемая Микросхема процессора является съемной.</span><span class="sxs-lookup"><span data-stu-id="88fa5-219">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="88fa5-220">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-220">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-221">**Заменяемый**</span><span class="sxs-lookup"><span data-stu-id="88fa5-221">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-222">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="88fa5-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-224">Если **значение — true**, элемент может быть заменен физически отличающимся.</span><span class="sxs-lookup"><span data-stu-id="88fa5-224">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="88fa5-225">Например, некоторые компьютерные системы позволяют обновить основную микросхему процессора до одной из более высоких оценок.</span><span class="sxs-lookup"><span data-stu-id="88fa5-225">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="88fa5-226">В этом случае процессор считается заменяемым.</span><span class="sxs-lookup"><span data-stu-id="88fa5-226">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="88fa5-227">Все съемные компоненты по сути являются заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="88fa5-227">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="88fa5-228">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-228">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-229">**рекуирементсдескриптион**</span><span class="sxs-lookup"><span data-stu-id="88fa5-229">**RequirementsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-230">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88fa5-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-232">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ карта CIM**".**СпеЦиалрекуирементс**")</span><span class="sxs-lookup"><span data-stu-id="88fa5-232">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Card**.**SpecialRequirements**")</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-233">Произвольная строка, описывающая, каким образом карта физически уникальна от других карточек.</span><span class="sxs-lookup"><span data-stu-id="88fa5-233">Free-form string that describes the ways in which the card is physically unique from other cards.</span></span> <span data-ttu-id="88fa5-234">Это свойство имеет значение только в том случае, если соответствующее свойство логического свойства **спеЦиалрекуирементс** имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="88fa5-234">This property only has meaning when the corresponding Boolean property, **SpecialRequirements**, is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-235">**рекуиресдаугхтербоард**</span><span class="sxs-lookup"><span data-stu-id="88fa5-235">**RequiresDaughterBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-236">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="88fa5-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-237">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-238">Если задано **значение true**, то требуется по крайней мере одна даугхтербоард или вспомогательная карта.</span><span class="sxs-lookup"><span data-stu-id="88fa5-238">If **TRUE**, to function properly, at least one daughterboard or auxiliary card is required.</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-239">**Номер**</span><span class="sxs-lookup"><span data-stu-id="88fa5-239">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-240">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88fa5-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-242">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="88fa5-242">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-243">Номер, выделенный изготовителем, используемый для распознавания физического элемента.</span><span class="sxs-lookup"><span data-stu-id="88fa5-243">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="88fa5-244">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-244">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-245">**SKU**</span><span class="sxs-lookup"><span data-stu-id="88fa5-245">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-246">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88fa5-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-248">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="88fa5-248">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-249">Номер единицы складского учета для этого физического элемента.</span><span class="sxs-lookup"><span data-stu-id="88fa5-249">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="88fa5-250">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-250">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-251">**слотлайаут**</span><span class="sxs-lookup"><span data-stu-id="88fa5-251">**SlotLayout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-252">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88fa5-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-254">Произвольная строка, описывающая положение слота, типичное использование, ограничения, отдельные интервалы между гнездами и другие сведения, относящиеся к слотам на карточке.</span><span class="sxs-lookup"><span data-stu-id="88fa5-254">Free-form string that describes the slot positioning, typical usage, restrictions, individual slot spacings, or other pertinent information for the slots on a card.</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-255">**спеЦиалрекуирементс**</span><span class="sxs-lookup"><span data-stu-id="88fa5-255">**SpecialRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-256">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="88fa5-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-258">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ карта CIM**".**Рекуирементсдескриптион**")</span><span class="sxs-lookup"><span data-stu-id="88fa5-258">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Card**.**RequirementsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-259">Если **значение — true**, карта физически уникальна по отношению к другим картам того же типа и, следовательно, требует специального слота.</span><span class="sxs-lookup"><span data-stu-id="88fa5-259">If **TRUE**, the card is physically unique from other cards of the same type and, therefore, requires a special slot.</span></span> <span data-ttu-id="88fa5-260">Например, для двойной широкой карты требуется два слота.</span><span class="sxs-lookup"><span data-stu-id="88fa5-260">For example, a double-wide card requires two slots.</span></span> <span data-ttu-id="88fa5-261">Другим примером является то, что определенную карту можно использовать для одной и той же общей функции с другими картами, но для нее требуется специальный слот (например, очень длинный). в то же время другие карты можно разместить в любом доступном слоте.</span><span class="sxs-lookup"><span data-stu-id="88fa5-261">Another example is when a certain card can be used for the same general function as other cards, but requires a special slot (extra long, for example); whereas, other cards can be placed in any available slot.</span></span> <span data-ttu-id="88fa5-262">Если **значение — true**, соответствующее свойство **рекуирементсдескриптион** должно задавать природу уникальности или назначения карты.</span><span class="sxs-lookup"><span data-stu-id="88fa5-262">If **TRUE**, the corresponding **RequirementsDescription** property should specify the nature of the uniqueness or purpose of the card.</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-263">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="88fa5-263">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-264">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88fa5-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-266">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="88fa5-266">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-267">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="88fa5-267">String that indicates the current status of the object.</span></span> <span data-ttu-id="88fa5-268">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="88fa5-268">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="88fa5-269">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="88fa5-269">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="88fa5-270">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="88fa5-270">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="88fa5-271">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="88fa5-271">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="88fa5-272">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="88fa5-272">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="88fa5-273">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="88fa5-273">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="88fa5-274">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-274">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="88fa5-275">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="88fa5-275">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="88fa5-276">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="88fa5-276">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="88fa5-277">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="88fa5-277">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="88fa5-278">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="88fa5-278">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88fa5-279">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="88fa5-279">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="88fa5-280">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="88fa5-280">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="88fa5-281">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="88fa5-281">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="88fa5-282">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="88fa5-282">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="88fa5-283">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="88fa5-283">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="88fa5-284">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="88fa5-284">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="88fa5-285">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="88fa5-285">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="88fa5-286">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="88fa5-286">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="88fa5-287">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="88fa5-287">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88fa5-288">**Тег**</span><span class="sxs-lookup"><span data-stu-id="88fa5-288">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-289">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88fa5-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-290">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-291">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="88fa5-291">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-292">Однозначно идентифицирует физический элемент и служит ключом элемента.</span><span class="sxs-lookup"><span data-stu-id="88fa5-292">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="88fa5-293">Это свойство может содержать такие сведения, как тег актива или данные серийного номера.</span><span class="sxs-lookup"><span data-stu-id="88fa5-293">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="88fa5-294">Ключ для [**CIM \_ фисикалелемент**](cim-physicalelement.md) помещается очень высоким в иерархии объектов для независимого обнаружения оборудования или сущности, независимо от физического размещения в (или в) шкафов, адаптеров и т. д.</span><span class="sxs-lookup"><span data-stu-id="88fa5-294">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="88fa5-295">Например, съемный компонент, который можно использовать для горячей замены, может быть взят из содержащего его пакета (с областями видимости) и временно не используется.</span><span class="sxs-lookup"><span data-stu-id="88fa5-295">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="88fa5-296">Объект по-прежнему продолжает существовать и даже может быть вставлен в другой контейнер области.</span><span class="sxs-lookup"><span data-stu-id="88fa5-296">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="88fa5-297">Ключом для физического элемента является произвольная строка, которая определяется независимо от размещения или расположения, ориентированного на расположение.</span><span class="sxs-lookup"><span data-stu-id="88fa5-297">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="88fa5-298">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-298">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-299">**Version**</span><span class="sxs-lookup"><span data-stu-id="88fa5-299">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-300">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88fa5-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-302">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="88fa5-302">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-303">Указывает версию физического элемента.</span><span class="sxs-lookup"><span data-stu-id="88fa5-303">Indicates the version of the physical element.</span></span>

<span data-ttu-id="88fa5-304">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-304">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-305">**Weight**</span><span class="sxs-lookup"><span data-stu-id="88fa5-305">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-306">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="88fa5-306">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-307">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-308">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("фунты")</span><span class="sxs-lookup"><span data-stu-id="88fa5-308">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-309">Вес физического пакета (в фунтах).</span><span class="sxs-lookup"><span data-stu-id="88fa5-309">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="88fa5-310">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-310">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="88fa5-311">**Width**</span><span class="sxs-lookup"><span data-stu-id="88fa5-311">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88fa5-312">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="88fa5-312">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88fa5-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88fa5-314">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="88fa5-314">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="88fa5-315">Ширина физического пакета в дюймах.</span><span class="sxs-lookup"><span data-stu-id="88fa5-315">Width of the physical package, in inches.</span></span>

<span data-ttu-id="88fa5-316">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-316">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88fa5-317">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88fa5-317">Remarks</span></span>

<span data-ttu-id="88fa5-318">Класс **\_ карты CIM** является производным от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-318">The **CIM\_Card** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

<span data-ttu-id="88fa5-319">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="88fa5-319">WMI does not implement this class.</span></span> <span data-ttu-id="88fa5-320">Дополнительные сведения о классах, производных от **CIM \_ Card**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-320">For more information about classes derived from **CIM\_Card**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="88fa5-321">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="88fa5-321">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="88fa5-322">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="88fa5-322">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="88fa5-323">Требования</span><span class="sxs-lookup"><span data-stu-id="88fa5-323">Requirements</span></span>



| <span data-ttu-id="88fa5-324">Требование</span><span class="sxs-lookup"><span data-stu-id="88fa5-324">Requirement</span></span> | <span data-ttu-id="88fa5-325">Значение</span><span class="sxs-lookup"><span data-stu-id="88fa5-325">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88fa5-326">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88fa5-326">Minimum supported client</span></span><br/> | <span data-ttu-id="88fa5-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88fa5-327">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="88fa5-328">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88fa5-328">Minimum supported server</span></span><br/> | <span data-ttu-id="88fa5-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88fa5-329">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="88fa5-330">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="88fa5-330">Namespace</span></span><br/>                | <span data-ttu-id="88fa5-331">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="88fa5-331">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="88fa5-332">MOF</span><span class="sxs-lookup"><span data-stu-id="88fa5-332">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88fa5-333"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88fa5-333"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="88fa5-334">DLL</span><span class="sxs-lookup"><span data-stu-id="88fa5-334">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88fa5-335"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88fa5-335"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88fa5-336">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88fa5-336">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88fa5-337">**\_ФИСИКАЛПАККАЖЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="88fa5-337">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 

