---
description: '\_Класс микросхем CIM представляет тип оборудования интегрированной цепи, включая ASIC, процессоры, микросхемы памяти и т. д.'
ms.assetid: 3c2b0023-5d02-49b9-90f5-d66eb8a103f0
ms.tgt_platform: multiple
title: Класс CIM_Chip
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chip
- CIM_Chip.Caption
- CIM_Chip.Description
- CIM_Chip.InstallDate
- CIM_Chip.Name
- CIM_Chip.Status
- CIM_Chip.CreationClassName
- CIM_Chip.Manufacturer
- CIM_Chip.Model
- CIM_Chip.OtherIdentifyingInfo
- CIM_Chip.PartNumber
- CIM_Chip.PoweredOn
- CIM_Chip.SerialNumber
- CIM_Chip.SKU
- CIM_Chip.Tag
- CIM_Chip.Version
- CIM_Chip.HotSwappable
- CIM_Chip.Removable
- CIM_Chip.Replaceable
- CIM_Chip.FormFactor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 953ae371edca42409246307b21aad69a02cf4a66
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496416"
---
# <a name="cim_chip-class"></a><span data-ttu-id="6776a-103">\_Класс микросхемы CIM</span><span class="sxs-lookup"><span data-stu-id="6776a-103">CIM\_Chip class</span></span>

<span data-ttu-id="6776a-104">Класс **\_ микросхем CIM** представляет тип оборудования интегрированной цепи, включая ASIC, процессоры, микросхемы памяти и т. д.</span><span class="sxs-lookup"><span data-stu-id="6776a-104">The **CIM\_Chip** class represents the type of integrated circuit hardware, including ASICs, processors, memory chips, and so on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6776a-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="6776a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6776a-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6776a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6776a-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="6776a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6776a-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="6776a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6776a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6776a-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B7A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Chip : CIM_PhysicalComponent
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
  uint16   FormFactor;
};
```

## <a name="members"></a><span data-ttu-id="6776a-110">Члены</span><span class="sxs-lookup"><span data-stu-id="6776a-110">Members</span></span>

<span data-ttu-id="6776a-111">Класс **\_ микросхем CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6776a-111">The **CIM\_Chip** class has these types of members:</span></span>

-   [<span data-ttu-id="6776a-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="6776a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6776a-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="6776a-113">Properties</span></span>

<span data-ttu-id="6776a-114">Класс **\_ микросхем CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6776a-114">The **CIM\_Chip** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6776a-115">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="6776a-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6776a-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6776a-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6776a-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6776a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6776a-118">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6776a-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6776a-119">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6776a-119">A short textual description of the object.</span></span>

<span data-ttu-id="6776a-120">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6776a-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6776a-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6776a-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6776a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6776a-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6776a-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6776a-124">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6776a-124">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6776a-125">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6776a-125">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6776a-126">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="6776a-126">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6776a-127">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-127">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6776a-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6776a-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6776a-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6776a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6776a-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6776a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6776a-131">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="6776a-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6776a-132">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6776a-132">A textual description of the object.</span></span>

<span data-ttu-id="6776a-133">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6776a-134">**формфактор**</span><span class="sxs-lookup"><span data-stu-id="6776a-134">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6776a-135">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6776a-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6776a-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6776a-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6776a-137">Конструктивный фактор для микросхемы.</span><span class="sxs-lookup"><span data-stu-id="6776a-137">Implementation form factor for the chip.</span></span> <span data-ttu-id="6776a-138">Можно указать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="6776a-138">The following values can be specified.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6776a-139">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="6776a-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6776a-140">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="6776a-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SIP"></span><span id="sip"></span>

<span data-ttu-id="6776a-141">**SIP** (2)</span><span class="sxs-lookup"><span data-stu-id="6776a-141">**SIP** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DIP"></span><span id="dip"></span>

<span data-ttu-id="6776a-142">**DIP** (3)</span><span class="sxs-lookup"><span data-stu-id="6776a-142">**DIP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIP"></span><span id="zip"></span>

<span data-ttu-id="6776a-143">**ZIP** (4)</span><span class="sxs-lookup"><span data-stu-id="6776a-143">**ZIP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOJ"></span><span id="soj"></span>

<span data-ttu-id="6776a-144">**СОЖ** (5)</span><span class="sxs-lookup"><span data-stu-id="6776a-144">**SOJ** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="6776a-145">**Собственная** (6)</span><span class="sxs-lookup"><span data-stu-id="6776a-145">**Proprietary** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SIMM"></span><span id="simm"></span>

<span data-ttu-id="6776a-146">**SIMM** (7)</span><span class="sxs-lookup"><span data-stu-id="6776a-146">**SIMM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DIMM"></span><span id="dimm"></span>

<span data-ttu-id="6776a-147">**Модули DIMM** (8)</span><span class="sxs-lookup"><span data-stu-id="6776a-147">**DIMM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="TSOP"></span><span id="tsop"></span>

<span data-ttu-id="6776a-148">**ТСОП** (9)</span><span class="sxs-lookup"><span data-stu-id="6776a-148">**TSOP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="PGA"></span><span id="pga"></span>

<span data-ttu-id="6776a-149">**PGA** (10)</span><span class="sxs-lookup"><span data-stu-id="6776a-149">**PGA** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="RIMM"></span><span id="rimm"></span>

<span data-ttu-id="6776a-150">**RIMM** (11)</span><span class="sxs-lookup"><span data-stu-id="6776a-150">**RIMM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SODIMM"></span><span id="sodimm"></span>

<span data-ttu-id="6776a-151">**Содимм** (12)</span><span class="sxs-lookup"><span data-stu-id="6776a-151">**SODIMM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SRIMM"></span><span id="srimm"></span>

<span data-ttu-id="6776a-152">**Сримм** (13)</span><span class="sxs-lookup"><span data-stu-id="6776a-152">**SRIMM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SMD"></span><span id="smd"></span>

<span data-ttu-id="6776a-153">**СМД** (14)</span><span class="sxs-lookup"><span data-stu-id="6776a-153">**SMD** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SSMP"></span><span id="ssmp"></span>

<span data-ttu-id="6776a-154">**ССМП** (15)</span><span class="sxs-lookup"><span data-stu-id="6776a-154">**SSMP** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="QFP"></span><span id="qfp"></span>

<span data-ttu-id="6776a-155">**КФП** (16)</span><span class="sxs-lookup"><span data-stu-id="6776a-155">**QFP** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="TQFP"></span><span id="tqfp"></span>

<span data-ttu-id="6776a-156">**Ткфп** (17)</span><span class="sxs-lookup"><span data-stu-id="6776a-156">**TQFP** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SOIC"></span><span id="soic"></span>

<span data-ttu-id="6776a-157">**Соик** (18)</span><span class="sxs-lookup"><span data-stu-id="6776a-157">**SOIC** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="LCC"></span><span id="lcc"></span>

<span data-ttu-id="6776a-158">**ЛКК** (19)</span><span class="sxs-lookup"><span data-stu-id="6776a-158">**LCC** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="PLCC"></span><span id="plcc"></span>

<span data-ttu-id="6776a-159">**Плкк** (20)</span><span class="sxs-lookup"><span data-stu-id="6776a-159">**PLCC** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="BGA"></span><span id="bga"></span>

<span data-ttu-id="6776a-160">**Корпус BGA** (21)</span><span class="sxs-lookup"><span data-stu-id="6776a-160">**BGA** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="FPBGA"></span><span id="fpbga"></span>

<span data-ttu-id="6776a-161">**Фпбга** (22)</span><span class="sxs-lookup"><span data-stu-id="6776a-161">**FPBGA** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="LGA"></span><span id="lga"></span>

<span data-ttu-id="6776a-162">**LGA** (23)</span><span class="sxs-lookup"><span data-stu-id="6776a-162">**LGA** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="FB-DIMM"></span><span id="fb-dimm"></span>

<span data-ttu-id="6776a-163">**FB-DIMM** (24)</span><span class="sxs-lookup"><span data-stu-id="6776a-163">**FB-DIMM** (24)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6776a-164">**хотсваппабле**</span><span class="sxs-lookup"><span data-stu-id="6776a-164">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6776a-165">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6776a-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6776a-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6776a-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6776a-167">Если задано **значение true**, пакет может быть горячим заменой.</span><span class="sxs-lookup"><span data-stu-id="6776a-167">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="6776a-168">Физический пакет может быть горячим заменой, если элемент может быть заменен физически другим (но эквивалентным) одним во время включения содержащего пакета.</span><span class="sxs-lookup"><span data-stu-id="6776a-168">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="6776a-169">Например, компонент вентилятора может быть рассчитан на горячую замену.</span><span class="sxs-lookup"><span data-stu-id="6776a-169">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="6776a-170">Все компоненты, доступные для горячей замены, по сути являются съемными и заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="6776a-170">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="6776a-171">Это свойство наследуется от [**CIM \_ фисикалкомпонент**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-171">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="6776a-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6776a-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6776a-173">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6776a-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6776a-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6776a-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6776a-175">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="6776a-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6776a-176">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="6776a-176">Indicates when the object was installed.</span></span> <span data-ttu-id="6776a-177">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="6776a-177">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6776a-178">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6776a-179">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="6776a-179">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6776a-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6776a-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6776a-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6776a-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6776a-182">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6776a-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6776a-183">Имя Организации, ответственной за создание физического элемента.</span><span class="sxs-lookup"><span data-stu-id="6776a-183">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="6776a-184">Дополнительные сведения см. в описании свойства **Vendor** [**\_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-184">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="6776a-185">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-185">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6776a-186">**Модель**</span><span class="sxs-lookup"><span data-stu-id="6776a-186">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6776a-187">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6776a-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6776a-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6776a-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6776a-189">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6776a-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6776a-190">Имя, по которому обычно известен физический элемент.</span><span class="sxs-lookup"><span data-stu-id="6776a-190">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="6776a-191">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-191">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6776a-192">**Name**</span><span class="sxs-lookup"><span data-stu-id="6776a-192">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6776a-193">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6776a-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6776a-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6776a-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6776a-195">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="6776a-195">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6776a-196">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="6776a-196">Label by which the object is known.</span></span> <span data-ttu-id="6776a-197">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="6776a-197">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6776a-198">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6776a-199">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="6776a-199">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6776a-200">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6776a-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6776a-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6776a-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6776a-202">Дополнительные данные, помимо сведений о тегах актива, которые можно использовать для поиска физического элемента.</span><span class="sxs-lookup"><span data-stu-id="6776a-202">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="6776a-203">Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива.</span><span class="sxs-lookup"><span data-stu-id="6776a-203">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="6776a-204">Обратите внимание, что если доступны только данные с штрих-кодом и они уникальны и могут использоваться в качестве ключа элемента, это свойство будет иметь значение null, а данные штрих-кода будут использоваться в качестве ключа класса в свойстве **Tag** .</span><span class="sxs-lookup"><span data-stu-id="6776a-204">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="6776a-205">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-205">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6776a-206">**партнумбер**</span><span class="sxs-lookup"><span data-stu-id="6776a-206">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6776a-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6776a-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6776a-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6776a-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6776a-209">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6776a-209">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6776a-210">Номер детали, назначенный Организацией, ответственной за производство или производство физического элемента.</span><span class="sxs-lookup"><span data-stu-id="6776a-210">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="6776a-211">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-211">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6776a-212">**повередон**</span><span class="sxs-lookup"><span data-stu-id="6776a-212">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6776a-213">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6776a-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6776a-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6776a-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6776a-215">**Значение true** показывает, что физический элемент включен.</span><span class="sxs-lookup"><span data-stu-id="6776a-215">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="6776a-216">В противном случае в данный момент он отключен.</span><span class="sxs-lookup"><span data-stu-id="6776a-216">Otherwise, it is currently off.</span></span>

<span data-ttu-id="6776a-217">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-217">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6776a-218">**Службе**</span><span class="sxs-lookup"><span data-stu-id="6776a-218">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6776a-219">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6776a-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6776a-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6776a-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6776a-221">Если **значение — true**, этот элемент предназначен для размещения в физическом контейнере, в котором он обычно обнаруживается и из него, без нарушения функций общей упаковки.</span><span class="sxs-lookup"><span data-stu-id="6776a-221">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="6776a-222">Пакет считается съемным, даже если питание должно быть выключено для выполнения удаления.</span><span class="sxs-lookup"><span data-stu-id="6776a-222">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="6776a-223">Если мощность может быть включена и пакет удален, то элемент является съемным и может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="6776a-223">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="6776a-224">Например, обновляемая Микросхема процессора является съемной.</span><span class="sxs-lookup"><span data-stu-id="6776a-224">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="6776a-225">Это свойство наследуется от [**CIM \_ фисикалкомпонент**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-225">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="6776a-226">**Заменяемый**</span><span class="sxs-lookup"><span data-stu-id="6776a-226">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6776a-227">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6776a-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6776a-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6776a-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6776a-229">Если **значение — true**, элемент может быть заменен физически отличающимся.</span><span class="sxs-lookup"><span data-stu-id="6776a-229">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="6776a-230">Например, некоторые компьютерные системы позволяют обновить основную микросхему процессора до одной из более высоких оценок.</span><span class="sxs-lookup"><span data-stu-id="6776a-230">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="6776a-231">В этом случае процессор считается заменяемым.</span><span class="sxs-lookup"><span data-stu-id="6776a-231">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="6776a-232">Все съемные компоненты по сути являются заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="6776a-232">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="6776a-233">Это свойство наследуется от [**CIM \_ фисикалкомпонент**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-233">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="6776a-234">**Номер**</span><span class="sxs-lookup"><span data-stu-id="6776a-234">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6776a-235">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6776a-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6776a-236">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6776a-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6776a-237">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6776a-237">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6776a-238">Номер, выделенный изготовителем, используемый для распознавания физического элемента.</span><span class="sxs-lookup"><span data-stu-id="6776a-238">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="6776a-239">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-239">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6776a-240">**SKU**</span><span class="sxs-lookup"><span data-stu-id="6776a-240">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6776a-241">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6776a-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6776a-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6776a-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6776a-243">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6776a-243">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6776a-244">Номер единицы складского учета для этого физического элемента.</span><span class="sxs-lookup"><span data-stu-id="6776a-244">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="6776a-245">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-245">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6776a-246">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="6776a-246">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6776a-247">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6776a-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6776a-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6776a-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6776a-249">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="6776a-249">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6776a-250">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="6776a-250">String that indicates the current status of the object.</span></span> <span data-ttu-id="6776a-251">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="6776a-251">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6776a-252">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="6776a-252">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6776a-253">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="6776a-253">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6776a-254">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="6776a-254">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6776a-255">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="6776a-255">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6776a-256">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="6776a-256">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6776a-257">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-257">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6776a-258">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="6776a-258">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6776a-259">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="6776a-259">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6776a-260">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="6776a-260">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6776a-261">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="6776a-261">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6776a-262">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="6776a-262">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6776a-263">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="6776a-263">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6776a-264">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="6776a-264">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6776a-265">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="6776a-265">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6776a-266">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="6776a-266">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6776a-267">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="6776a-267">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6776a-268">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="6776a-268">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6776a-269">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="6776a-269">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6776a-270">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="6776a-270">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6776a-271">**Тег**</span><span class="sxs-lookup"><span data-stu-id="6776a-271">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6776a-272">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6776a-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6776a-273">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6776a-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6776a-274">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6776a-274">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6776a-275">Однозначно идентифицирует физический элемент и служит ключом элемента.</span><span class="sxs-lookup"><span data-stu-id="6776a-275">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="6776a-276">Это свойство может содержать такие сведения, как тег актива или данные серийного номера.</span><span class="sxs-lookup"><span data-stu-id="6776a-276">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="6776a-277">Ключ для [**CIM \_ фисикалелемент**](cim-physicalelement.md) помещается очень высоким в иерархии объектов для независимого обнаружения оборудования или сущности, независимо от физического размещения в (или в) шкафов, адаптеров и т. д.</span><span class="sxs-lookup"><span data-stu-id="6776a-277">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="6776a-278">Например, съемный компонент, который можно использовать для горячей замены, может быть взят из содержащего его пакета (с областями видимости) и временно не используется.</span><span class="sxs-lookup"><span data-stu-id="6776a-278">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="6776a-279">Объект по-прежнему продолжает существовать и даже может быть вставлен в другой контейнер области.</span><span class="sxs-lookup"><span data-stu-id="6776a-279">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="6776a-280">Ключом для физического элемента является произвольная строка, которая определяется независимо от размещения или расположения, ориентированного на расположение.</span><span class="sxs-lookup"><span data-stu-id="6776a-280">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="6776a-281">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-281">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6776a-282">**Version**</span><span class="sxs-lookup"><span data-stu-id="6776a-282">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6776a-283">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6776a-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6776a-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6776a-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6776a-285">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6776a-285">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6776a-286">Указывает версию физического элемента.</span><span class="sxs-lookup"><span data-stu-id="6776a-286">Indicates the version of the physical element.</span></span>

<span data-ttu-id="6776a-287">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-287">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6776a-288">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6776a-288">Remarks</span></span>

<span data-ttu-id="6776a-289">Класс **\_ микросхемы CIM** является производным от [**CIM \_ фисикалкомпонент**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-289">The **CIM\_Chip** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

<span data-ttu-id="6776a-290">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="6776a-290">WMI does not implement this class.</span></span> <span data-ttu-id="6776a-291">Дополнительные сведения о классах, производных от **\_ микросхемы CIM**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-291">For more information about classes derived from **CIM\_Chip**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6776a-292">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="6776a-292">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6776a-293">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="6776a-293">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6776a-294">Требования</span><span class="sxs-lookup"><span data-stu-id="6776a-294">Requirements</span></span>



| <span data-ttu-id="6776a-295">Требование</span><span class="sxs-lookup"><span data-stu-id="6776a-295">Requirement</span></span> | <span data-ttu-id="6776a-296">Значение</span><span class="sxs-lookup"><span data-stu-id="6776a-296">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6776a-297">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6776a-297">Minimum supported client</span></span><br/> | <span data-ttu-id="6776a-298">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6776a-298">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6776a-299">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6776a-299">Minimum supported server</span></span><br/> | <span data-ttu-id="6776a-300">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6776a-300">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6776a-301">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6776a-301">Namespace</span></span><br/>                | <span data-ttu-id="6776a-302">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6776a-302">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6776a-303">MOF</span><span class="sxs-lookup"><span data-stu-id="6776a-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6776a-304"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6776a-304"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6776a-305">DLL</span><span class="sxs-lookup"><span data-stu-id="6776a-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6776a-306"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6776a-306"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6776a-307">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6776a-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6776a-308">**\_ФИСИКАЛКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="6776a-308">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> </dl>

 

