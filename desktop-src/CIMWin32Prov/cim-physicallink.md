---
description: Класс CIM \_ фисикаллинк представляет кабель физических элементов.
ms.assetid: 0d96cb7f-ca50-4eb2-b8d4-e749bbe67ad7
ms.tgt_platform: multiple
title: Класс CIM_PhysicalLink
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalLink
- CIM_PhysicalLink.Caption
- CIM_PhysicalLink.CreationClassName
- CIM_PhysicalLink.Description
- CIM_PhysicalLink.InstallDate
- CIM_PhysicalLink.Length
- CIM_PhysicalLink.Manufacturer
- CIM_PhysicalLink.MaxLength
- CIM_PhysicalLink.MediaType
- CIM_PhysicalLink.Model
- CIM_PhysicalLink.Name
- CIM_PhysicalLink.OtherIdentifyingInfo
- CIM_PhysicalLink.PartNumber
- CIM_PhysicalLink.PoweredOn
- CIM_PhysicalLink.SerialNumber
- CIM_PhysicalLink.SKU
- CIM_PhysicalLink.Status
- CIM_PhysicalLink.Tag
- CIM_PhysicalLink.Version
- CIM_PhysicalLink.Wired
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 659e73d9f5331d5c6648af00e147797dc6424130
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539161"
---
# <a name="cim_physicallink-class"></a><span data-ttu-id="45114-103">\_Класс CIM фисикаллинк</span><span class="sxs-lookup"><span data-stu-id="45114-103">CIM\_PhysicalLink class</span></span>

<span data-ttu-id="45114-104">Класс **CIM \_ фисикаллинк** представляет кабель физических элементов.</span><span class="sxs-lookup"><span data-stu-id="45114-104">The **CIM\_PhysicalLink** class represents the cabling of physical elements.</span></span> <span data-ttu-id="45114-105">Например, последовательные или Ethernet-кабели и инфракрасные связи должны быть подклассами (если определены дополнительные свойства или ассоциации) или экземплярами **CIM \_ фисикаллинк**.</span><span class="sxs-lookup"><span data-stu-id="45114-105">For example, serial or Ethernet cables and infrared links would be subclasses (if additional properties or associations are defined) or instances of **CIM\_PhysicalLink**.</span></span> <span data-ttu-id="45114-106">Как правило, многие физические кабели в пределах физического пакета или сети не моделируются.</span><span class="sxs-lookup"><span data-stu-id="45114-106">Typically, the numerous physical cables within a physical package or network are not modeled.</span></span> <span data-ttu-id="45114-107">Однако, если кабели или связи являются критически важными компонентами или ресурсами-тегами компании, можно создать экземпляры объектов с помощью этого класса или одного из его классов-потомков.</span><span class="sxs-lookup"><span data-stu-id="45114-107">However, when the cables or links are critical components or tagged assets of the company, the objects can be instantiated using this class or one of its descendant classes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="45114-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="45114-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="45114-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="45114-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="45114-110">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="45114-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="45114-111">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="45114-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="45114-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45114-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B82-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalLink : CIM_PhysicalElement
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  real64   Length;
  string   Manufacturer;
  real64   MaxLength;
  uint16   MediaType;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
  boolean  Wired;
};
```

## <a name="members"></a><span data-ttu-id="45114-113">Члены</span><span class="sxs-lookup"><span data-stu-id="45114-113">Members</span></span>

<span data-ttu-id="45114-114">Класс **CIM \_ фисикаллинк** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="45114-114">The **CIM\_PhysicalLink** class has these types of members:</span></span>

-   [<span data-ttu-id="45114-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="45114-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="45114-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="45114-116">Properties</span></span>

<span data-ttu-id="45114-117">Класс **CIM \_ фисикаллинк** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="45114-117">The **CIM\_PhysicalLink** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45114-118">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="45114-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45114-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="45114-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45114-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45114-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45114-121">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="45114-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="45114-122">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="45114-122">Short textual description of the object.</span></span>

<span data-ttu-id="45114-123">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45114-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45114-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="45114-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45114-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="45114-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45114-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45114-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45114-127">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="45114-127">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="45114-128">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="45114-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="45114-129">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="45114-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="45114-130">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="45114-130">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45114-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="45114-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45114-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="45114-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45114-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45114-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45114-134">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="45114-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="45114-135">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="45114-135">Textual description of the object.</span></span>

<span data-ttu-id="45114-136">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45114-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45114-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="45114-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45114-138">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="45114-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="45114-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45114-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45114-140">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="45114-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="45114-141">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="45114-141">Date and time the object was installed.</span></span> <span data-ttu-id="45114-142">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="45114-142">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="45114-143">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45114-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45114-144">**Длина**</span><span class="sxs-lookup"><span data-stu-id="45114-144">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45114-145">Тип данных: **real64**</span><span class="sxs-lookup"><span data-stu-id="45114-145">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="45114-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45114-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45114-147">Квалификаторы: [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("футы")</span><span class="sxs-lookup"><span data-stu-id="45114-147">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("feet")</span></span>
</dt> </dl>

<span data-ttu-id="45114-148">Текущая длина физической связи в футах.</span><span class="sxs-lookup"><span data-stu-id="45114-148">Current length of the physical link, in feet.</span></span> <span data-ttu-id="45114-149">Для некоторых подключений, особенно беспроводных технологий, это свойство может быть неприменимо и должно оставаться неинициализированным.</span><span class="sxs-lookup"><span data-stu-id="45114-149">For some connections, especially wireless technologies, this property might not be applicable and should be left uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="45114-150">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="45114-150">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45114-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="45114-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45114-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45114-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45114-153">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="45114-153">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="45114-154">Имя Организации, ответственной за создание физического элемента.</span><span class="sxs-lookup"><span data-stu-id="45114-154">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="45114-155">Дополнительные сведения см. в описании свойства **Vendor** [**\_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="45114-155">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="45114-156">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="45114-156">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45114-157">**MaxLength**</span><span class="sxs-lookup"><span data-stu-id="45114-157">**MaxLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45114-158">Тип данных: **real64**</span><span class="sxs-lookup"><span data-stu-id="45114-158">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="45114-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45114-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45114-160">Квалификаторы: [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("футы")</span><span class="sxs-lookup"><span data-stu-id="45114-160">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("feet")</span></span>
</dt> </dl>

<span data-ttu-id="45114-161">Максимальная длина физической связи в футах.</span><span class="sxs-lookup"><span data-stu-id="45114-161">Maximum length of the physical link in feet.</span></span>

</dd> <dt>

<span data-ttu-id="45114-162">**Мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="45114-162">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45114-163">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45114-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45114-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45114-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45114-165">Тип носителя, через который проходит сигнал передачи.</span><span class="sxs-lookup"><span data-stu-id="45114-165">Type of media through which transmission signals pass.</span></span> <span data-ttu-id="45114-166">К общим сетевым носителям относятся витая пара, коаксиальный и оптоволоконный кабель.</span><span class="sxs-lookup"><span data-stu-id="45114-166">Common network media include twisted-pair, coaxial, and fiber-optic cable.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="45114-167">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="45114-167">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="45114-168">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="45114-168">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat1"></span><span id="cat1"></span><span id="CAT1"></span>

<span data-ttu-id="45114-169">**Cat1** (2)</span><span class="sxs-lookup"><span data-stu-id="45114-169">**Cat1** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat2"></span><span id="cat2"></span><span id="CAT2"></span>

<span data-ttu-id="45114-170">**Cat2** (3)</span><span class="sxs-lookup"><span data-stu-id="45114-170">**Cat2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat3"></span><span id="cat3"></span><span id="CAT3"></span>

<span data-ttu-id="45114-171">**Cat3** (4)</span><span class="sxs-lookup"><span data-stu-id="45114-171">**Cat3** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat4"></span><span id="cat4"></span><span id="CAT4"></span>

<span data-ttu-id="45114-172">**Cat4** (5)</span><span class="sxs-lookup"><span data-stu-id="45114-172">**Cat4** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat5"></span><span id="cat5"></span><span id="CAT5"></span>

<span data-ttu-id="45114-173">**CAT5** (6)</span><span class="sxs-lookup"><span data-stu-id="45114-173">**Cat5** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="50-ohm_Coaxial"></span><span id="50-ohm_coaxial"></span><span id="50-OHM_COAXIAL"></span>

<span data-ttu-id="45114-174">**коаксиальный кабель 50 ом** (7)</span><span class="sxs-lookup"><span data-stu-id="45114-174">**50-ohm Coaxial** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="75-ohm_Coaxial"></span><span id="75-ohm_coaxial"></span><span id="75-OHM_COAXIAL"></span>

<span data-ttu-id="45114-175">**коаксиальный кабель 75 ом** (8)</span><span class="sxs-lookup"><span data-stu-id="45114-175">**75-ohm Coaxial** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="100-ohm_Coaxial"></span><span id="100-ohm_coaxial"></span><span id="100-OHM_COAXIAL"></span>

<span data-ttu-id="45114-176">**коаксиальный кабель 100 ом** (9)</span><span class="sxs-lookup"><span data-stu-id="45114-176">**100-ohm Coaxial** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber-optic"></span><span id="fiber-optic"></span><span id="FIBER-OPTIC"></span>

<span data-ttu-id="45114-177">**Fiber-оптика** (10)</span><span class="sxs-lookup"><span data-stu-id="45114-177">**Fiber-optic** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP"></span><span id="utp"></span>

<span data-ttu-id="45114-178">**UTP** (11)</span><span class="sxs-lookup"><span data-stu-id="45114-178">**UTP** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="STP"></span><span id="stp"></span>

<span data-ttu-id="45114-179">**STP** (12)</span><span class="sxs-lookup"><span data-stu-id="45114-179">**STP** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Ribbon_Cable"></span><span id="ribbon_cable"></span><span id="RIBBON_CABLE"></span>

<span data-ttu-id="45114-180">**Шлейф** (13)</span><span class="sxs-lookup"><span data-stu-id="45114-180">**Ribbon Cable** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Twinaxial"></span><span id="twinaxial"></span><span id="TWINAXIAL"></span>

<span data-ttu-id="45114-181">**Твинаксиал** (14)</span><span class="sxs-lookup"><span data-stu-id="45114-181">**Twinaxial** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_9um"></span><span id="optical_9um"></span><span id="OPTICAL_9UM"></span>

<span data-ttu-id="45114-182">**Оптические 9um** (15)</span><span class="sxs-lookup"><span data-stu-id="45114-182">**Optical 9um** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_50um"></span><span id="optical_50um"></span><span id="OPTICAL_50UM"></span>

<span data-ttu-id="45114-183">**Оптический 50um** (16)</span><span class="sxs-lookup"><span data-stu-id="45114-183">**Optical 50um** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_62.5um"></span><span id="optical_62.5um"></span><span id="OPTICAL_62.5UM"></span>

<span data-ttu-id="45114-184">**Оптическая 62,5 UM** (17)</span><span class="sxs-lookup"><span data-stu-id="45114-184">**Optical 62.5um** (17)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="45114-185">**Модель**</span><span class="sxs-lookup"><span data-stu-id="45114-185">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45114-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="45114-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45114-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45114-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45114-188">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="45114-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="45114-189">Имя, по которому обычно известен физический элемент.</span><span class="sxs-lookup"><span data-stu-id="45114-189">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="45114-190">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="45114-190">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45114-191">**Name**</span><span class="sxs-lookup"><span data-stu-id="45114-191">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45114-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="45114-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45114-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45114-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45114-194">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="45114-194">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="45114-195">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="45114-195">Label by which the object is known.</span></span> <span data-ttu-id="45114-196">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="45114-196">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="45114-197">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45114-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45114-198">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="45114-198">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45114-199">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="45114-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45114-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45114-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45114-201">Дополнительные данные, помимо сведений о тегах актива, которые можно использовать для поиска физического элемента.</span><span class="sxs-lookup"><span data-stu-id="45114-201">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="45114-202">Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива.</span><span class="sxs-lookup"><span data-stu-id="45114-202">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="45114-203">Обратите внимание, что если доступны только данные с штрих-кодом и они уникальны и могут использоваться в качестве ключа элемента, это свойство будет иметь значение null, а данные штрих-кода будут использоваться в качестве ключа класса в свойстве **Tag** .</span><span class="sxs-lookup"><span data-stu-id="45114-203">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="45114-204">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="45114-204">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45114-205">**партнумбер**</span><span class="sxs-lookup"><span data-stu-id="45114-205">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45114-206">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="45114-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45114-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45114-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45114-208">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="45114-208">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="45114-209">Номер детали, назначенный Организацией, ответственной за производство или производство физического элемента.</span><span class="sxs-lookup"><span data-stu-id="45114-209">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="45114-210">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="45114-210">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45114-211">**повередон**</span><span class="sxs-lookup"><span data-stu-id="45114-211">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45114-212">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="45114-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45114-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45114-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45114-214">**Значение true** показывает, что физический элемент включен.</span><span class="sxs-lookup"><span data-stu-id="45114-214">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="45114-215">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="45114-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45114-216">**Номер**</span><span class="sxs-lookup"><span data-stu-id="45114-216">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45114-217">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="45114-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45114-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45114-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45114-219">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="45114-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="45114-220">Номер, выделенный изготовителем, используемый для распознавания физического элемента.</span><span class="sxs-lookup"><span data-stu-id="45114-220">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="45114-221">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="45114-221">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45114-222">**SKU**</span><span class="sxs-lookup"><span data-stu-id="45114-222">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45114-223">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="45114-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45114-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45114-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45114-225">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="45114-225">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="45114-226">Номер единицы хранения для физического элемента.</span><span class="sxs-lookup"><span data-stu-id="45114-226">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="45114-227">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="45114-227">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45114-228">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="45114-228">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45114-229">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="45114-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45114-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45114-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45114-231">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="45114-231">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="45114-232">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="45114-232">Current status of the object.</span></span>

<span data-ttu-id="45114-233">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45114-233">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="45114-234">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="45114-234">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="45114-235">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="45114-235">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="45114-236">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="45114-236">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="45114-237">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="45114-237">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="45114-238">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="45114-238">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="45114-239">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="45114-239">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="45114-240">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="45114-240">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="45114-241">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="45114-241">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="45114-242">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="45114-242">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="45114-243">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="45114-243">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="45114-244">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="45114-244">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="45114-245">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="45114-245">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="45114-246">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="45114-246">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="45114-247">**Тег**</span><span class="sxs-lookup"><span data-stu-id="45114-247">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45114-248">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="45114-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45114-249">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45114-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45114-250">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="45114-250">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="45114-251">Произвольная строка, однозначно идентифицирующая физический элемент и служащая в качестве ключа элемента.</span><span class="sxs-lookup"><span data-stu-id="45114-251">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="45114-252">Это свойство может содержать такие сведения, как тег актива или данные серийного номера.</span><span class="sxs-lookup"><span data-stu-id="45114-252">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="45114-253">Ключ для [**CIM \_ фисикалелемент**](cim-physicalelement.md) помещается очень высоким в иерархии объектов для независимого обнаружения оборудования или сущности, независимо от физического размещения в (или в) шкафов, адаптеров и т. д.</span><span class="sxs-lookup"><span data-stu-id="45114-253">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="45114-254">Например, съемный компонент, который можно использовать для горячей замены, может быть взят из содержащего его пакета (с областями видимости) и временно не используется.</span><span class="sxs-lookup"><span data-stu-id="45114-254">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="45114-255">Объект по-прежнему продолжает существовать и даже может быть вставлен в другой контейнер области.</span><span class="sxs-lookup"><span data-stu-id="45114-255">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="45114-256">Ключом для физического элемента является произвольная строка, которая определяется независимо от размещения или расположения, ориентированного на расположение.</span><span class="sxs-lookup"><span data-stu-id="45114-256">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="45114-257">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="45114-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45114-258">**Version**</span><span class="sxs-lookup"><span data-stu-id="45114-258">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45114-259">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="45114-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45114-260">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45114-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45114-261">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="45114-261">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="45114-262">Версия физического элемента.</span><span class="sxs-lookup"><span data-stu-id="45114-262">Version of the physical element.</span></span>

<span data-ttu-id="45114-263">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="45114-263">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45114-264">**Проводных**</span><span class="sxs-lookup"><span data-stu-id="45114-264">**Wired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45114-265">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="45114-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45114-266">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45114-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45114-267">Если **значение равно true**, физическая связь является кабелем.</span><span class="sxs-lookup"><span data-stu-id="45114-267">If **TRUE**, the physical link is a cable.</span></span> <span data-ttu-id="45114-268">В противном случае это беспроводное подключение.</span><span class="sxs-lookup"><span data-stu-id="45114-268">Otherwise, it is a wireless connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45114-269">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45114-269">Remarks</span></span>

<span data-ttu-id="45114-270">Класс **CIM \_ фисикаллинк** является производным от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="45114-270">The **CIM\_PhysicalLink** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="45114-271">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="45114-271">WMI does not implement this class.</span></span>

<span data-ttu-id="45114-272">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="45114-272">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="45114-273">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="45114-273">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="45114-274">Требования</span><span class="sxs-lookup"><span data-stu-id="45114-274">Requirements</span></span>



| <span data-ttu-id="45114-275">Требование</span><span class="sxs-lookup"><span data-stu-id="45114-275">Requirement</span></span> | <span data-ttu-id="45114-276">Значение</span><span class="sxs-lookup"><span data-stu-id="45114-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45114-277">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45114-277">Minimum supported client</span></span><br/> | <span data-ttu-id="45114-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45114-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="45114-279">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45114-279">Minimum supported server</span></span><br/> | <span data-ttu-id="45114-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45114-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="45114-281">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="45114-281">Namespace</span></span><br/>                | <span data-ttu-id="45114-282">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="45114-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="45114-283">MOF</span><span class="sxs-lookup"><span data-stu-id="45114-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45114-284"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45114-284"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="45114-285">DLL</span><span class="sxs-lookup"><span data-stu-id="45114-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45114-286"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45114-286"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45114-287">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45114-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45114-288">**\_ФИСИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="45114-288">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

