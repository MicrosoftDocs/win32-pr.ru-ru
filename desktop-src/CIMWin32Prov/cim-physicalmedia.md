---
description: Класс CIM \_ фисикалмедиа представляет типы документации и среды хранения, такие как ленты, компакт-диски и т. д.
ms.assetid: ba258e53-4a82-4b30-aadd-54448841cd06
ms.tgt_platform: multiple
title: Класс CIM_PhysicalMedia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalMedia
- CIM_PhysicalMedia.Capacity
- CIM_PhysicalMedia.Caption
- CIM_PhysicalMedia.CleanerMedia
- CIM_PhysicalMedia.CreationClassName
- CIM_PhysicalMedia.Description
- CIM_PhysicalMedia.HotSwappable
- CIM_PhysicalMedia.InstallDate
- CIM_PhysicalMedia.Manufacturer
- CIM_PhysicalMedia.MediaDescription
- CIM_PhysicalMedia.MediaType
- CIM_PhysicalMedia.Model
- CIM_PhysicalMedia.Name
- CIM_PhysicalMedia.OtherIdentifyingInfo
- CIM_PhysicalMedia.PartNumber
- CIM_PhysicalMedia.PoweredOn
- CIM_PhysicalMedia.Removable
- CIM_PhysicalMedia.Replaceable
- CIM_PhysicalMedia.SerialNumber
- CIM_PhysicalMedia.SKU
- CIM_PhysicalMedia.Status
- CIM_PhysicalMedia.Tag
- CIM_PhysicalMedia.Version
- CIM_PhysicalMedia.WriteProtectOn
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f8709128c189956bba4bc371e0f5bfb30d67b49f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104273284"
---
# <a name="cim_physicalmedia-class"></a><span data-ttu-id="074ee-103">\_Класс CIM фисикалмедиа</span><span class="sxs-lookup"><span data-stu-id="074ee-103">CIM\_PhysicalMedia class</span></span>

<span data-ttu-id="074ee-104">Класс **CIM \_ фисикалмедиа** представляет типы документации и среды хранения, такие как ленты, компакт-диски и т. д.</span><span class="sxs-lookup"><span data-stu-id="074ee-104">The **CIM\_PhysicalMedia** class represents types of documentation and storage medium, such as tapes, CD ROMs, and so on.</span></span> <span data-ttu-id="074ee-105">Этот класс обычно используется для нахождение и управление съемными носителями (а также мультимедиа, запечатанным устройством доступа к носителю как к одному пакету, например жестким дискам).</span><span class="sxs-lookup"><span data-stu-id="074ee-105">This class is typically used to locate and manage removable media (versus media sealed with the media access device as a single package, such as hard disks).</span></span> <span data-ttu-id="074ee-106">Однако запечатанные носители также можно моделировать с помощью этого класса, если носитель связан с физическим пакетом с помощью отношения [**CIM \_ паккажедкомпонент**](cim-packagedcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="074ee-106">Sealed media, however, can also be modeled using this class when the media is associated with the physical package using the [**CIM\_PackagedComponent**](cim-packagedcomponent.md) relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="074ee-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="074ee-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="074ee-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="074ee-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="074ee-109">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="074ee-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="074ee-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="074ee-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="074ee-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="074ee-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalMedia : CIM_PhysicalComponent
{
  uint64   Capacity;
  string   Caption;
  boolean  CleanerMedia;
  string   CreationClassName;
  string   Description;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   MediaDescription;
  uint16   MediaType;
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
  boolean  WriteProtectOn;
};
```

## <a name="members"></a><span data-ttu-id="074ee-112">Члены</span><span class="sxs-lookup"><span data-stu-id="074ee-112">Members</span></span>

<span data-ttu-id="074ee-113">Класс **CIM \_ фисикалмедиа** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="074ee-113">The **CIM\_PhysicalMedia** class has these types of members:</span></span>

-   [<span data-ttu-id="074ee-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="074ee-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="074ee-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="074ee-115">Properties</span></span>

<span data-ttu-id="074ee-116">Класс **CIM \_ фисикалмедиа** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="074ee-116">The **CIM\_PhysicalMedia** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="074ee-117">**Производительность**</span><span class="sxs-lookup"><span data-stu-id="074ee-117">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-118">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="074ee-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074ee-120">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="074ee-120">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="074ee-121">Число байтов, которые могут быть считаны или записаны на носитель.</span><span class="sxs-lookup"><span data-stu-id="074ee-121">Number of bytes that can be read from, or written to, a media.</span></span> <span data-ttu-id="074ee-122">Это свойство неприменимо к жесткому копированию (документации) или носителю.</span><span class="sxs-lookup"><span data-stu-id="074ee-122">This property is not applicable to hard copy (documentation) or cleaner media.</span></span> <span data-ttu-id="074ee-123">Сжатие данных не следует предполагать, так как оно увеличит значение в этом свойстве.</span><span class="sxs-lookup"><span data-stu-id="074ee-123">Data compression should not be assumed, as it would increase the value in this property.</span></span> <span data-ttu-id="074ee-124">Для лент предполагается, что на носителе не записаны метки файлов или пробелы.</span><span class="sxs-lookup"><span data-stu-id="074ee-124">For tapes, it should be assumed that no file marks or blank space areas are recorded on the media.</span></span>

<span data-ttu-id="074ee-125">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="074ee-125">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="074ee-126">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="074ee-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="074ee-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074ee-129">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="074ee-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="074ee-130">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="074ee-130">Short textual description of the object.</span></span>

<span data-ttu-id="074ee-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="074ee-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="074ee-132">**клеанермедиа**</span><span class="sxs-lookup"><span data-stu-id="074ee-132">**CleanerMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-133">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="074ee-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074ee-135">Если **значение равно true**, физический носитель используется для целей очистки, а не для хранения данных.</span><span class="sxs-lookup"><span data-stu-id="074ee-135">If **TRUE**, the physical media is used for cleaning purposes, not data storage.</span></span>

</dd> <dt>

<span data-ttu-id="074ee-136">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="074ee-136">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="074ee-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074ee-139">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="074ee-139">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="074ee-140">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="074ee-140">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="074ee-141">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="074ee-141">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="074ee-142">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="074ee-142">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="074ee-143">**Описание**</span><span class="sxs-lookup"><span data-stu-id="074ee-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="074ee-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074ee-146">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="074ee-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="074ee-147">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="074ee-147">Textual description of the object.</span></span>

<span data-ttu-id="074ee-148">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="074ee-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="074ee-149">**хотсваппабле**</span><span class="sxs-lookup"><span data-stu-id="074ee-149">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-150">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="074ee-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074ee-152">Если задано **значение true**, пакет может быть горячим заменой.</span><span class="sxs-lookup"><span data-stu-id="074ee-152">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="074ee-153">Физический пакет может быть горячим заменой, если элемент может быть заменен физически другим (но эквивалентным) одним во время включения содержащего пакета.</span><span class="sxs-lookup"><span data-stu-id="074ee-153">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="074ee-154">Например, компонент вентилятора может быть рассчитан на горячую замену.</span><span class="sxs-lookup"><span data-stu-id="074ee-154">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="074ee-155">Все компоненты, доступные для горячей замены, по сути являются съемными и заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="074ee-155">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="074ee-156">Это свойство наследуется от [**CIM \_ фисикалкомпонент**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="074ee-156">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="074ee-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="074ee-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-158">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="074ee-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074ee-160">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="074ee-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="074ee-161">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="074ee-161">Date and time the object was installed.</span></span> <span data-ttu-id="074ee-162">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="074ee-162">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="074ee-163">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="074ee-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="074ee-164">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="074ee-164">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="074ee-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074ee-167">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="074ee-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="074ee-168">Имя Организации, ответственной за создание физического элемента.</span><span class="sxs-lookup"><span data-stu-id="074ee-168">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="074ee-169">Дополнительные сведения см. в описании свойства **Vendor** [**\_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="074ee-169">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="074ee-170">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="074ee-170">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="074ee-171">**MediaDescription**</span><span class="sxs-lookup"><span data-stu-id="074ee-171">**MediaDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="074ee-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074ee-174">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ фисикалмедиа**.**MediaType**)</span><span class="sxs-lookup"><span data-stu-id="074ee-174">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalMedia**.**MediaType**")</span></span>
</dt> </dl>

<span data-ttu-id="074ee-175">Дополнительные сведения о перечислении **mediaType** .</span><span class="sxs-lookup"><span data-stu-id="074ee-175">Additional detail related to the **MediaType** enumeration.</span></span> <span data-ttu-id="074ee-176">Например, если задано значение 3 ("картридж QIC"), это свойство указывает, является ли лента широкой или 1/4 дюйма, предварительно отформатированным, Траван совместимым и т. д.</span><span class="sxs-lookup"><span data-stu-id="074ee-176">For example, if value 3 ("QIC Cartridge") is specified, this property would indicate whether the tape is wide or 1/4 inch, pre-formatted, Travan compatible, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="074ee-177">**Мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="074ee-177">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-178">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="074ee-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074ee-180">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ фисикалмедиа**.**MediaDescription**")</span><span class="sxs-lookup"><span data-stu-id="074ee-180">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalMedia**.**MediaDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="074ee-181">Тип физического носителя.</span><span class="sxs-lookup"><span data-stu-id="074ee-181">Type of physical media.</span></span> <span data-ttu-id="074ee-182">Свойство **MediaDescription** обеспечивает более явное определение типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="074ee-182">The **MediaDescription** property provides more explicit definition of the media type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="074ee-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="074ee-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="074ee-184"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="074ee-184"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>

<span data-ttu-id="074ee-185"><span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>**Ленточный картридж** (2)</span><span class="sxs-lookup"><span data-stu-id="074ee-185"><span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>**Tape Cartridge** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>

<span data-ttu-id="074ee-186"><span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>**Картридж QIC** (3)</span><span class="sxs-lookup"><span data-stu-id="074ee-186"><span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>**QIC Cartridge** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>

<span data-ttu-id="074ee-187"><span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>**Картридж AIT** (4)</span><span class="sxs-lookup"><span data-stu-id="074ee-187"><span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>**AIT Cartridge** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>

<span data-ttu-id="074ee-188"><span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>**Картридж DTF** (5)</span><span class="sxs-lookup"><span data-stu-id="074ee-188"><span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>**DTF Cartridge** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>

<span data-ttu-id="074ee-189"><span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>**Картридж dat** (6)</span><span class="sxs-lookup"><span data-stu-id="074ee-189"><span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>**DAT Cartridge** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>

<span data-ttu-id="074ee-190"><span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>**Ленточный картридж 8mm** (7)</span><span class="sxs-lookup"><span data-stu-id="074ee-190"><span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>**8mm Tape Cartridge** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>

<span data-ttu-id="074ee-191"><span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>**Ленточный картридж 19mm** (8)</span><span class="sxs-lookup"><span data-stu-id="074ee-191"><span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>**19mm Tape Cartridge** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>

<span data-ttu-id="074ee-192"><span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>**Картридж DLT** (9)</span><span class="sxs-lookup"><span data-stu-id="074ee-192"><span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>**DLT Cartridge** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>

<span data-ttu-id="074ee-193"><span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>**Дюймовый** Ленточный картридж (10)</span><span class="sxs-lookup"><span data-stu-id="074ee-193"><span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>**Half-Inch Magnetic Tape Cartridge** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>

<span data-ttu-id="074ee-194"><span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>**Кассетный диск** (11)</span><span class="sxs-lookup"><span data-stu-id="074ee-194"><span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>**Cartridge Disk** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>

<span data-ttu-id="074ee-195"><span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>**Диск Жаз** (12)</span><span class="sxs-lookup"><span data-stu-id="074ee-195"><span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>**JAZ Disk** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>

<span data-ttu-id="074ee-196"><span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>**ZIP-диск** (13)</span><span class="sxs-lookup"><span data-stu-id="074ee-196"><span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>**ZIP Disk** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>

<span data-ttu-id="074ee-197"><span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>**Диск сикуест** (14)</span><span class="sxs-lookup"><span data-stu-id="074ee-197"><span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>**SyQuest Disk** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>

<span data-ttu-id="074ee-198"><span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>**Winchester съемный диск** (15)</span><span class="sxs-lookup"><span data-stu-id="074ee-198"><span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>**Winchester Removable Disk** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="074ee-199"><span id="CD-ROM"></span><span id="cd-rom"></span>**Компакт-** диск (16)</span><span class="sxs-lookup"><span data-stu-id="074ee-199"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>

<span data-ttu-id="074ee-200"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span><span class="sxs-lookup"><span data-stu-id="074ee-200"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-I"></span><span id="cd-i"></span>

<span data-ttu-id="074ee-201"><span id="CD-I"></span><span id="cd-i"></span>**Компакт-I** (18)</span><span class="sxs-lookup"><span data-stu-id="074ee-201"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>

<span data-ttu-id="074ee-202"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**Записываемый компакт-диск** (19)</span><span class="sxs-lookup"><span data-stu-id="074ee-202"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD Recordable** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="WORM"></span><span id="worm"></span>

<span data-ttu-id="074ee-203"><span id="WORM"></span><span id="worm"></span>**Червь** (20)</span><span class="sxs-lookup"><span data-stu-id="074ee-203"><span id="WORM"></span><span id="worm"></span>**WORM** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>

<span data-ttu-id="074ee-204"><span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>**Магнитооптических** (21)</span><span class="sxs-lookup"><span data-stu-id="074ee-204"><span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>**Magneto-Optical** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD"></span><span id="dvd"></span>

<span data-ttu-id="074ee-205"><span id="DVD"></span><span id="dvd"></span>**DVD-диск** (22)</span><span class="sxs-lookup"><span data-stu-id="074ee-205"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_RW"></span><span id="dvd_rw"></span>

<span data-ttu-id="074ee-206"><span id="DVD_RW"></span><span id="dvd_rw"></span>**DVD + RW** (23)</span><span class="sxs-lookup"><span data-stu-id="074ee-206"><span id="DVD_RW"></span><span id="dvd_rw"></span>**DVD+RW** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RAM"></span><span id="dvd-ram"></span>

<span data-ttu-id="074ee-207"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span><span class="sxs-lookup"><span data-stu-id="074ee-207"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-ROM"></span><span id="dvd-rom"></span>

<span data-ttu-id="074ee-208"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span><span class="sxs-lookup"><span data-stu-id="074ee-208"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>

<span data-ttu-id="074ee-209"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-видео** (26)</span><span class="sxs-lookup"><span data-stu-id="074ee-209"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-Video** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>

<span data-ttu-id="074ee-210"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**Дивкс** (27)</span><span class="sxs-lookup"><span data-stu-id="074ee-210"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**Divx** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>

<span data-ttu-id="074ee-211"><span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>**Дискета/дискета** (28)</span><span class="sxs-lookup"><span data-stu-id="074ee-211"><span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>**Floppy/Diskette** (28)</span></span>


</dt> <dd>

<span data-ttu-id="074ee-212">Гибкий диск</span><span class="sxs-lookup"><span data-stu-id="074ee-212">Floppy disk</span></span>

</dd> <dt>

<span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>

<span data-ttu-id="074ee-213"><span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>**Жесткий диск** (29)</span><span class="sxs-lookup"><span data-stu-id="074ee-213"><span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>**Hard Disk** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>

<span data-ttu-id="074ee-214"><span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>**Карта памяти** (30)</span><span class="sxs-lookup"><span data-stu-id="074ee-214"><span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>**Memory Card** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>

<span data-ttu-id="074ee-215"><span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>**Твердое копирование** (31)</span><span class="sxs-lookup"><span data-stu-id="074ee-215"><span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>**Hard Copy** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>

<span data-ttu-id="074ee-216"><span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>**Диск клик** (32)</span><span class="sxs-lookup"><span data-stu-id="074ee-216"><span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>**Clik Disk** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-RW"></span><span id="cd-rw"></span>

<span data-ttu-id="074ee-217"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span><span class="sxs-lookup"><span data-stu-id="074ee-217"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-DA"></span><span id="cd-da"></span>

<span data-ttu-id="074ee-218"><span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34)</span><span class="sxs-lookup"><span data-stu-id="074ee-218"><span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_"></span><span id="cd_"></span>

<span data-ttu-id="074ee-219"><span id="CD_"></span><span id="cd_"></span>**CD +** (35)</span><span class="sxs-lookup"><span data-stu-id="074ee-219"><span id="CD_"></span><span id="cd_"></span>**CD+** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>

<span data-ttu-id="074ee-220"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**Записываемый DVD-диск** (36)</span><span class="sxs-lookup"><span data-stu-id="074ee-220"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD Recordable** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RW"></span><span id="dvd-rw"></span>

<span data-ttu-id="074ee-221"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span><span class="sxs-lookup"><span data-stu-id="074ee-221"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>

<span data-ttu-id="074ee-222"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**Аудио DVD** (38)</span><span class="sxs-lookup"><span data-stu-id="074ee-222"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-Audio** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-5"></span><span id="dvd-5"></span>

<span data-ttu-id="074ee-223"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span><span class="sxs-lookup"><span data-stu-id="074ee-223"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-9"></span><span id="dvd-9"></span>

<span data-ttu-id="074ee-224"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span><span class="sxs-lookup"><span data-stu-id="074ee-224"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-10"></span><span id="dvd-10"></span>

<span data-ttu-id="074ee-225"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span><span class="sxs-lookup"><span data-stu-id="074ee-225"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-18"></span><span id="dvd-18"></span>

<span data-ttu-id="074ee-226"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span><span class="sxs-lookup"><span data-stu-id="074ee-226"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>

<span data-ttu-id="074ee-227"><span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>**Магнитооптических с возможностью перезаписи** (43)</span><span class="sxs-lookup"><span data-stu-id="074ee-227"><span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>**Magneto-Optical Rewriteable** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>

<span data-ttu-id="074ee-228"><span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>**Однократная оптическая запись** (44)</span><span class="sxs-lookup"><span data-stu-id="074ee-228"><span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>**Magneto-Optical Write Once** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>

<span data-ttu-id="074ee-229"><span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>**Магнитооптических с возможностью перезаписи (лимдов)** (45)</span><span class="sxs-lookup"><span data-stu-id="074ee-229"><span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>**Magneto-Optical Rewriteable (LIMDOW)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>

<span data-ttu-id="074ee-230"><span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>**Однократная запись изменения этапа** (46)</span><span class="sxs-lookup"><span data-stu-id="074ee-230"><span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>**Phase Change Write Once** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>

<span data-ttu-id="074ee-231"><span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>**Перезаписываемый этап изменения** (47)</span><span class="sxs-lookup"><span data-stu-id="074ee-231"><span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>**Phase Change Rewriteable** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>

<span data-ttu-id="074ee-232"><span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>**Изменение фазы с двумя перезаписываемыми** (48)</span><span class="sxs-lookup"><span data-stu-id="074ee-232"><span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>**Phase Change Dual Rewriteable** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>

<span data-ttu-id="074ee-233"><span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>**Аблативе** однократная запись (49)</span><span class="sxs-lookup"><span data-stu-id="074ee-233"><span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>**Ablative Write Once** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>

<span data-ttu-id="074ee-234"><span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>**Запись ближнего поля** (50)</span><span class="sxs-lookup"><span data-stu-id="074ee-234"><span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>**Near Field Recording** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>

<span data-ttu-id="074ee-235"><span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>**Миникик** (51)</span><span class="sxs-lookup"><span data-stu-id="074ee-235"><span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>**MiniQic** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>

<span data-ttu-id="074ee-236"><span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>**Траван** (52)</span><span class="sxs-lookup"><span data-stu-id="074ee-236"><span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>**Travan** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>

<span data-ttu-id="074ee-237"><span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>**8Mm металлическая частица** (53)</span><span class="sxs-lookup"><span data-stu-id="074ee-237"><span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>**8mm Metal Particle** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>

<span data-ttu-id="074ee-238"><span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>**8Mm Advanced металла евапорате** (54)</span><span class="sxs-lookup"><span data-stu-id="074ee-238"><span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>**8mm Advanced Metal Evaporate** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NCTP"></span><span id="nctp"></span>

<span data-ttu-id="074ee-239"><span id="NCTP"></span><span id="nctp"></span>**НКТП** (55)</span><span class="sxs-lookup"><span data-stu-id="074ee-239"><span id="NCTP"></span><span id="nctp"></span>**NCTP** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>

<span data-ttu-id="074ee-240"><span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>**LTO Ultrium** (56)</span><span class="sxs-lookup"><span data-stu-id="074ee-240"><span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>**LTO Ultrium** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>

<span data-ttu-id="074ee-241"><span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>**LTO акцелис** (57)</span><span class="sxs-lookup"><span data-stu-id="074ee-241"><span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>**LTO Accelis** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>

<span data-ttu-id="074ee-242"><span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>**9. запись на ленту** (58)</span><span class="sxs-lookup"><span data-stu-id="074ee-242"><span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>**9 Track Tape** (58)</span></span>


</dt> <dd>

<span data-ttu-id="074ee-243">9. запись ленты</span><span class="sxs-lookup"><span data-stu-id="074ee-243">9-track tape</span></span>

</dd> <dt>

<span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>

<span data-ttu-id="074ee-244"><span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>**18. запись на ленту** (59)</span><span class="sxs-lookup"><span data-stu-id="074ee-244"><span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>**18 Track Tape** (59)</span></span>


</dt> <dd>

<span data-ttu-id="074ee-245">18. запись ленты</span><span class="sxs-lookup"><span data-stu-id="074ee-245">18-track tape</span></span>

</dd> <dt>

<span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>

<span data-ttu-id="074ee-246"><span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>**36. запись на магнитную ленту** (60)</span><span class="sxs-lookup"><span data-stu-id="074ee-246"><span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>**36 Track Tape** (60)</span></span>


</dt> <dd>

<span data-ttu-id="074ee-247">36. запись на ленту</span><span class="sxs-lookup"><span data-stu-id="074ee-247">36-track tape</span></span>

</dd> <dt>

<span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>

<span data-ttu-id="074ee-248"><span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>**Магстар 3590** (61)</span><span class="sxs-lookup"><span data-stu-id="074ee-248"><span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>**Magstar 3590** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>

<span data-ttu-id="074ee-249"><span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>**МАГСТАР MP** (62)</span><span class="sxs-lookup"><span data-stu-id="074ee-249"><span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>**Magstar MP** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>

<span data-ttu-id="074ee-250"><span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>**Лента D2** (63)</span><span class="sxs-lookup"><span data-stu-id="074ee-250"><span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>**D2 Tape** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>

<span data-ttu-id="074ee-251"><span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>**Лента — мелкий DST** (64)</span><span class="sxs-lookup"><span data-stu-id="074ee-251"><span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>**Tape - DST Small** (64)</span></span>


</dt> <dd>

<span data-ttu-id="074ee-252">Лента DST маленький</span><span class="sxs-lookup"><span data-stu-id="074ee-252">Tape   DST small</span></span>

</dd> <dt>

<span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>

<span data-ttu-id="074ee-253"><span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>**Лента — средний DST** (65)</span><span class="sxs-lookup"><span data-stu-id="074ee-253"><span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>**Tape - DST Medium** (65)</span></span>


</dt> <dd>

<span data-ttu-id="074ee-254">Средняя DST на ленту</span><span class="sxs-lookup"><span data-stu-id="074ee-254">Tape   DST medium</span></span>

</dd> <dt>

<span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>

<span data-ttu-id="074ee-255"><span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>**Лента — крупный DST** (66)</span><span class="sxs-lookup"><span data-stu-id="074ee-255"><span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>**Tape - DST Large** (66)</span></span>


</dt> <dd>

<span data-ttu-id="074ee-256">Большой DST на магнитной ленте</span><span class="sxs-lookup"><span data-stu-id="074ee-256">Tape   DST large</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="074ee-257">**Модель**</span><span class="sxs-lookup"><span data-stu-id="074ee-257">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-258">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="074ee-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074ee-260">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="074ee-260">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="074ee-261">Имя, по которому обычно известен физический элемент.</span><span class="sxs-lookup"><span data-stu-id="074ee-261">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="074ee-262">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="074ee-262">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="074ee-263">**Name**</span><span class="sxs-lookup"><span data-stu-id="074ee-263">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-264">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="074ee-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074ee-266">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="074ee-266">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="074ee-267">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="074ee-267">Label by which the object is known.</span></span> <span data-ttu-id="074ee-268">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="074ee-268">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="074ee-269">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="074ee-269">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="074ee-270">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="074ee-270">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-271">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="074ee-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-272">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074ee-273">Дополнительные данные, помимо сведений о тегах актива, которые можно использовать для поиска физического элемента.</span><span class="sxs-lookup"><span data-stu-id="074ee-273">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="074ee-274">Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива.</span><span class="sxs-lookup"><span data-stu-id="074ee-274">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="074ee-275">Обратите внимание, что если доступны только данные с штрих-кодом и они уникальны и могут использоваться в качестве ключа элемента, это свойство будет иметь значение null, а данные штрих-кода будут использоваться в качестве ключа класса в свойстве **Tag** .</span><span class="sxs-lookup"><span data-stu-id="074ee-275">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="074ee-276">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="074ee-276">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="074ee-277">**партнумбер**</span><span class="sxs-lookup"><span data-stu-id="074ee-277">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-278">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="074ee-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074ee-280">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="074ee-280">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="074ee-281">Номер детали, назначенный Организацией, ответственной за производство или производство физического элемента.</span><span class="sxs-lookup"><span data-stu-id="074ee-281">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="074ee-282">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="074ee-282">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="074ee-283">**повередон**</span><span class="sxs-lookup"><span data-stu-id="074ee-283">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-284">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="074ee-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074ee-286">**Значение true** показывает, что физический элемент включен.</span><span class="sxs-lookup"><span data-stu-id="074ee-286">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="074ee-287">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="074ee-287">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="074ee-288">**Службе**</span><span class="sxs-lookup"><span data-stu-id="074ee-288">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-289">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="074ee-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-290">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074ee-291">Если **значение — true**, этот элемент предназначен для размещения в физическом контейнере, в котором он обычно обнаруживается и из него, без нарушения функций общей упаковки.</span><span class="sxs-lookup"><span data-stu-id="074ee-291">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="074ee-292">Пакет считается съемным, даже если питание должно быть выключено для выполнения удаления.</span><span class="sxs-lookup"><span data-stu-id="074ee-292">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="074ee-293">Если мощность может быть включена и пакет удален, то элемент является съемным и может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="074ee-293">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="074ee-294">Например, необновляемая Микросхема процессора является съемной.</span><span class="sxs-lookup"><span data-stu-id="074ee-294">For example, an ungradable processor chip is removable.</span></span>

<span data-ttu-id="074ee-295">Это свойство наследуется от [**CIM \_ фисикалкомпонент**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="074ee-295">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="074ee-296">**Заменяемый**</span><span class="sxs-lookup"><span data-stu-id="074ee-296">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-297">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="074ee-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074ee-299">Если **значение — true**, элемент может быть заменен физически отличающимся.</span><span class="sxs-lookup"><span data-stu-id="074ee-299">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="074ee-300">Например, некоторые компьютерные системы позволяют обновить основную микросхему процессора до одной из более высоких оценок.</span><span class="sxs-lookup"><span data-stu-id="074ee-300">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="074ee-301">В этом случае процессор считается заменяемым.</span><span class="sxs-lookup"><span data-stu-id="074ee-301">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="074ee-302">Все съемные компоненты по сути являются заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="074ee-302">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="074ee-303">Это свойство наследуется от [**CIM \_ фисикалкомпонент**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="074ee-303">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="074ee-304">**Номер**</span><span class="sxs-lookup"><span data-stu-id="074ee-304">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-305">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="074ee-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074ee-307">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="074ee-307">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="074ee-308">Номер, выделенный изготовителем, используемый для распознавания физического элемента.</span><span class="sxs-lookup"><span data-stu-id="074ee-308">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="074ee-309">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="074ee-309">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="074ee-310">**SKU**</span><span class="sxs-lookup"><span data-stu-id="074ee-310">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-311">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="074ee-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-312">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074ee-313">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="074ee-313">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="074ee-314">Номер единицы хранения для физического элемента.</span><span class="sxs-lookup"><span data-stu-id="074ee-314">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="074ee-315">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="074ee-315">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="074ee-316">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="074ee-316">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-317">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="074ee-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074ee-319">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="074ee-319">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="074ee-320">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="074ee-320">Current status of the object.</span></span>

<span data-ttu-id="074ee-321">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="074ee-321">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="074ee-322">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="074ee-322">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="074ee-323">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="074ee-323">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="074ee-324">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="074ee-324">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="074ee-325">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="074ee-325">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="074ee-326">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="074ee-326">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="074ee-327">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="074ee-327">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="074ee-328">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="074ee-328">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="074ee-329">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="074ee-329">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="074ee-330">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="074ee-330">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="074ee-331">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="074ee-331">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="074ee-332">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="074ee-332">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="074ee-333">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="074ee-333">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="074ee-334">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="074ee-334">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="074ee-335">**Тег**</span><span class="sxs-lookup"><span data-stu-id="074ee-335">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-336">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="074ee-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074ee-338">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="074ee-338">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="074ee-339">Произвольная строка, однозначно идентифицирующая физический элемент и служащая в качестве ключа элемента.</span><span class="sxs-lookup"><span data-stu-id="074ee-339">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="074ee-340">Это свойство может содержать такие сведения, как тег актива или данные серийного номера.</span><span class="sxs-lookup"><span data-stu-id="074ee-340">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="074ee-341">Ключ для [**CIM \_ фисикалелемент**](cim-physicalelement.md) помещается очень высоким в иерархии объектов для независимого обнаружения оборудования или сущности, независимо от физического размещения в (или в) шкафов, адаптеров и т. д.</span><span class="sxs-lookup"><span data-stu-id="074ee-341">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="074ee-342">Например, съемный компонент, который можно использовать для горячей замены, может быть взят из содержащего его пакета (с областями видимости) и временно не используется.</span><span class="sxs-lookup"><span data-stu-id="074ee-342">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="074ee-343">Объект по-прежнему продолжает существовать и даже может быть вставлен в другой контейнер области.</span><span class="sxs-lookup"><span data-stu-id="074ee-343">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="074ee-344">Ключом для физического элемента является произвольная строка, которая определяется независимо от размещения или расположения, ориентированного на расположение.</span><span class="sxs-lookup"><span data-stu-id="074ee-344">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="074ee-345">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="074ee-345">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="074ee-346">**Version**</span><span class="sxs-lookup"><span data-stu-id="074ee-346">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-347">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="074ee-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-348">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074ee-349">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="074ee-349">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="074ee-350">Версия физического элемента.</span><span class="sxs-lookup"><span data-stu-id="074ee-350">Version of the physical element.</span></span>

<span data-ttu-id="074ee-351">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="074ee-351">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="074ee-352">**вритепротектон**</span><span class="sxs-lookup"><span data-stu-id="074ee-352">**WriteProtectOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074ee-353">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="074ee-353">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="074ee-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="074ee-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074ee-355">Если **значение — true**, носитель защищен от записи физическим механизмом, например с вкладкой "Защита" на гибком диске.</span><span class="sxs-lookup"><span data-stu-id="074ee-355">If **TRUE**, the media is currently write-protected by a physical mechanism, such as a protect tab on a floppy disk.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="074ee-356">Комментарии</span><span class="sxs-lookup"><span data-stu-id="074ee-356">Remarks</span></span>

<span data-ttu-id="074ee-357">Класс **CIM \_ фисикалмедиа** является производным от [**CIM \_ фисикалкомпонент**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="074ee-357">The **CIM\_PhysicalMedia** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

<span data-ttu-id="074ee-358">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="074ee-358">WMI does not implement this class.</span></span>

<span data-ttu-id="074ee-359">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="074ee-359">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="074ee-360">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="074ee-360">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="074ee-361">Требования</span><span class="sxs-lookup"><span data-stu-id="074ee-361">Requirements</span></span>



| <span data-ttu-id="074ee-362">Требование</span><span class="sxs-lookup"><span data-stu-id="074ee-362">Requirement</span></span> | <span data-ttu-id="074ee-363">Значение</span><span class="sxs-lookup"><span data-stu-id="074ee-363">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="074ee-364">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="074ee-364">Minimum supported client</span></span><br/> | <span data-ttu-id="074ee-365">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="074ee-365">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="074ee-366">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="074ee-366">Minimum supported server</span></span><br/> | <span data-ttu-id="074ee-367">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="074ee-367">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="074ee-368">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="074ee-368">Namespace</span></span><br/>                | <span data-ttu-id="074ee-369">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="074ee-369">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="074ee-370">MOF</span><span class="sxs-lookup"><span data-stu-id="074ee-370">MOF</span></span><br/>                      | <dl> <span data-ttu-id="074ee-371"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="074ee-371"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="074ee-372">DLL</span><span class="sxs-lookup"><span data-stu-id="074ee-372">DLL</span></span><br/>                      | <dl> <span data-ttu-id="074ee-373"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="074ee-373"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="074ee-374">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="074ee-374">See also</span></span>

<dl> <dt>

[<span data-ttu-id="074ee-375">**\_ФИСИКАЛКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="074ee-375">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> </dl>

 

