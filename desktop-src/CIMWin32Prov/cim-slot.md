---
description: '\_Класс слота CIM представляет соединители, в которые вставляются пакеты.'
ms.assetid: bcb1bdb5-fb1a-47ed-9450-dca38edca0eb
ms.tgt_platform: multiple
title: Класс CIM_Slot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Slot
- CIM_Slot.Caption
- CIM_Slot.ConnectorPinout
- CIM_Slot.ConnectorType
- CIM_Slot.CreationClassName
- CIM_Slot.Description
- CIM_Slot.HeightAllowed
- CIM_Slot.InstallDate
- CIM_Slot.LengthAllowed
- CIM_Slot.Manufacturer
- CIM_Slot.MaxDataWidth
- CIM_Slot.Model
- CIM_Slot.Name
- CIM_Slot.Number
- CIM_Slot.OtherIdentifyingInfo
- CIM_Slot.PartNumber
- CIM_Slot.PoweredOn
- CIM_Slot.PurposeDescription
- CIM_Slot.SerialNumber
- CIM_Slot.SKU
- CIM_Slot.SpecialPurpose
- CIM_Slot.Status
- CIM_Slot.SupportsHotPlug
- CIM_Slot.Tag
- CIM_Slot.ThermalRating
- CIM_Slot.VccMixedVoltageSupport
- CIM_Slot.Version
- CIM_Slot.VppMixedVoltageSupport
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73a63c8cd200096aa132d8205691669d765e54f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496626"
---
# <a name="cim_slot-class"></a><span data-ttu-id="03ac2-103">\_Класс слота CIM</span><span class="sxs-lookup"><span data-stu-id="03ac2-103">CIM\_Slot class</span></span>

<span data-ttu-id="03ac2-104">Класс **\_ слота CIM** представляет соединители, в которые вставляются пакеты.</span><span class="sxs-lookup"><span data-stu-id="03ac2-104">The **CIM\_Slot** class represents connectors into which packages are inserted.</span></span> <span data-ttu-id="03ac2-105">Например, физический пакет, который является диском, можно вставить в гнездо SCA, или карту (подкласс [CIM \_ фисикалпаккаже](cim-physicalpackage.md)) можно вставить в 16-, 32-или 64-битный слот расширения на доске размещения.</span><span class="sxs-lookup"><span data-stu-id="03ac2-105">For example, a physical package that is a disk drive can be inserted into an SCA slot, or a card (a subclass of [CIM\_PhysicalPackage](cim-physicalpackage.md)) can be inserted into a 16-, 32-, or 64-bit expansion slot on a hosting board.</span></span> <span data-ttu-id="03ac2-106">В качестве примеров второго варианта используются разъемы PCI или PCMCIA типа III.</span><span class="sxs-lookup"><span data-stu-id="03ac2-106">PCI or PCMCIA Type III Slots are examples of the latter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03ac2-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="03ac2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="03ac2-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="03ac2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="03ac2-109">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="03ac2-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="03ac2-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="03ac2-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="03ac2-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03ac2-111">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B86-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Slot : CIM_PhysicalConnector
{
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  string   Description;
  real32   HeightAllowed;
  datetime InstallDate;
  real32   LengthAllowed;
  string   Manufacturer;
  uint16   MaxDataWidth;
  string   Model;
  string   Name;
  uint16   Number;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   PurposeDescription;
  string   SerialNumber;
  string   SKU;
  boolean  SpecialPurpose;
  string   Status;
  boolean  SupportsHotPlug;
  string   Tag;
  uint32   ThermalRating;
  uint16   VccMixedVoltageSupport[];
  string   Version;
  uint16   VppMixedVoltageSupport[];
};
```

## <a name="members"></a><span data-ttu-id="03ac2-112">Члены</span><span class="sxs-lookup"><span data-stu-id="03ac2-112">Members</span></span>

<span data-ttu-id="03ac2-113">Класс **\_ слота CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="03ac2-113">The **CIM\_Slot** class has these types of members:</span></span>

-   [<span data-ttu-id="03ac2-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="03ac2-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03ac2-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="03ac2-115">Properties</span></span>

<span data-ttu-id="03ac2-116">Класс **\_ слота CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="03ac2-116">The **CIM\_Slot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03ac2-117">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="03ac2-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03ac2-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-120">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="03ac2-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-121">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="03ac2-121">Short textual description of the object.</span></span>

<span data-ttu-id="03ac2-122">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03ac2-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-123">**коннекторпинаут**</span><span class="sxs-lookup"><span data-stu-id="03ac2-123">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03ac2-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-126">Произвольная строка, описывающая конфигурацию ПИН-кода и использование сигнала физическим соединителем.</span><span class="sxs-lookup"><span data-stu-id="03ac2-126">Free-form string that describes the pin configuration and signal use of a physical connector.</span></span>

<span data-ttu-id="03ac2-127">Это свойство наследуется от [**CIM \_ фисикалконнектор**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="03ac2-127">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-128">**коннектортипе**</span><span class="sxs-lookup"><span data-stu-id="03ac2-128">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-129">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="03ac2-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-131">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("коннектортипе"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Системный слот DMTF \| 004,2 ")</span><span class="sxs-lookup"><span data-stu-id="03ac2-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ConnectorType"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.2")</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-132">Тип физического соединителя.</span><span class="sxs-lookup"><span data-stu-id="03ac2-132">Type of physical connector.</span></span> <span data-ttu-id="03ac2-133">Массив задается, чтобы разрешить Описание сочетаний сведений о соединителях.</span><span class="sxs-lookup"><span data-stu-id="03ac2-133">An array is specified to allow the description of combinations of connector information.</span></span> <span data-ttu-id="03ac2-134">Например, одна запись массива может указывать RS-232, другой DB-25, а третья — в качестве соединителя "папа".</span><span class="sxs-lookup"><span data-stu-id="03ac2-134">For example, one array entry could specify RS-232, another DB-25, and a third could define the connector as "Male".</span></span>

<span data-ttu-id="03ac2-135">Это свойство наследуется от [**CIM \_ фисикалконнектор**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="03ac2-135">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<dt>

<span data-ttu-id="03ac2-136">0</span><span class="sxs-lookup"><span data-stu-id="03ac2-136">0</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-137">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="03ac2-137">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-138">1</span><span class="sxs-lookup"><span data-stu-id="03ac2-138">1</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-139">Другое</span><span class="sxs-lookup"><span data-stu-id="03ac2-139">Other</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-140">2</span><span class="sxs-lookup"><span data-stu-id="03ac2-140">2</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-141">Муж.</span><span class="sxs-lookup"><span data-stu-id="03ac2-141">Male</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-142">3</span><span class="sxs-lookup"><span data-stu-id="03ac2-142">3</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-143">Жен.</span><span class="sxs-lookup"><span data-stu-id="03ac2-143">Female</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-144">4</span><span class="sxs-lookup"><span data-stu-id="03ac2-144">4</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-145">Экранирование</span><span class="sxs-lookup"><span data-stu-id="03ac2-145">Shielded</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-146">5</span><span class="sxs-lookup"><span data-stu-id="03ac2-146">5</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-147">Неэкранированной</span><span class="sxs-lookup"><span data-stu-id="03ac2-147">Unshielded</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-148">6</span><span class="sxs-lookup"><span data-stu-id="03ac2-148">6</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-149">SCSI (A) с высокой плотностью (50 ПИН-коды)</span><span class="sxs-lookup"><span data-stu-id="03ac2-149">SCSI (A) High-density (50 pins)</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-150">7</span><span class="sxs-lookup"><span data-stu-id="03ac2-150">7</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-151">SCSI (A) с низкой плотностью (50 ПИН-коды)</span><span class="sxs-lookup"><span data-stu-id="03ac2-151">SCSI (A) Low-density (50 pins)</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-152">8</span><span class="sxs-lookup"><span data-stu-id="03ac2-152">8</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-153">SCSI (P) высокой плотности (68 ПИН-кодов)</span><span class="sxs-lookup"><span data-stu-id="03ac2-153">SCSI (P) High-density (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-154">9</span><span class="sxs-lookup"><span data-stu-id="03ac2-154">9</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-155">SCSI SCA-I (80 контактов)</span><span class="sxs-lookup"><span data-stu-id="03ac2-155">SCSI SCA-I (80 pins)</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-156">10</span><span class="sxs-lookup"><span data-stu-id="03ac2-156">10</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-157">SCSI SCA-II (80 контактов)</span><span class="sxs-lookup"><span data-stu-id="03ac2-157">SCSI SCA-II (80 pins)</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-158">11</span><span class="sxs-lookup"><span data-stu-id="03ac2-158">11</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-159">Fibre Channel SCSI (DB-9, медный)</span><span class="sxs-lookup"><span data-stu-id="03ac2-159">SCSI Fibre Channel (DB-9, Copper)</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-160">12</span><span class="sxs-lookup"><span data-stu-id="03ac2-160">12</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-161">Fibre Channel SCSI (Fibre)</span><span class="sxs-lookup"><span data-stu-id="03ac2-161">SCSI Fibre Channel (Fibre)</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-162">13</span><span class="sxs-lookup"><span data-stu-id="03ac2-162">13</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-163">SCSI Fibre Channel SCA-II (40 контактов)</span><span class="sxs-lookup"><span data-stu-id="03ac2-163">SCSI Fibre Channel SCA-II (40 pins)</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-164">14</span><span class="sxs-lookup"><span data-stu-id="03ac2-164">14</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-165">SCSI Fibre Channel SCA-II (20 контактов)</span><span class="sxs-lookup"><span data-stu-id="03ac2-165">SCSI Fibre Channel SCA-II (20 pins)</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-166">15</span><span class="sxs-lookup"><span data-stu-id="03ac2-166">15</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-167">SCSI Fibre Channel БНК</span><span class="sxs-lookup"><span data-stu-id="03ac2-167">SCSI Fibre Channel BNC</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-168">16</span><span class="sxs-lookup"><span data-stu-id="03ac2-168">16</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-169">ATA 3-1/2 дюйма (40 контактов)</span><span class="sxs-lookup"><span data-stu-id="03ac2-169">ATA 3-1/2 Inch (40 pins)</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-170">17</span><span class="sxs-lookup"><span data-stu-id="03ac2-170">17</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-171">ATA 2-1/2 дюйма (44 контактов)</span><span class="sxs-lookup"><span data-stu-id="03ac2-171">ATA 2-1/2 Inch (44 pins)</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-172">18</span><span class="sxs-lookup"><span data-stu-id="03ac2-172">18</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-173">ATA-2</span><span class="sxs-lookup"><span data-stu-id="03ac2-173">ATA-2</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-174">19</span><span class="sxs-lookup"><span data-stu-id="03ac2-174">19</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-175">ATA-3</span><span class="sxs-lookup"><span data-stu-id="03ac2-175">ATA-3</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-176">20</span><span class="sxs-lookup"><span data-stu-id="03ac2-176">20</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-177">ATA/66</span><span class="sxs-lookup"><span data-stu-id="03ac2-177">ATA/66</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-178">21</span><span class="sxs-lookup"><span data-stu-id="03ac2-178">21</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-179">DB-9</span><span class="sxs-lookup"><span data-stu-id="03ac2-179">DB-9</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-180">22</span><span class="sxs-lookup"><span data-stu-id="03ac2-180">22</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-181">DB-15</span><span class="sxs-lookup"><span data-stu-id="03ac2-181">DB-15</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-182">23</span><span class="sxs-lookup"><span data-stu-id="03ac2-182">23</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-183">DB-25</span><span class="sxs-lookup"><span data-stu-id="03ac2-183">DB-25</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-184">24</span><span class="sxs-lookup"><span data-stu-id="03ac2-184">24</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-185">DB-36</span><span class="sxs-lookup"><span data-stu-id="03ac2-185">DB-36</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-186">25</span><span class="sxs-lookup"><span data-stu-id="03ac2-186">25</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-187">RS-232C</span><span class="sxs-lookup"><span data-stu-id="03ac2-187">RS-232C</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-188">26</span><span class="sxs-lookup"><span data-stu-id="03ac2-188">26</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-189">RS-422</span><span class="sxs-lookup"><span data-stu-id="03ac2-189">RS-422</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-190">27</span><span class="sxs-lookup"><span data-stu-id="03ac2-190">27</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-191">RS-423</span><span class="sxs-lookup"><span data-stu-id="03ac2-191">RS-423</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-192">28</span><span class="sxs-lookup"><span data-stu-id="03ac2-192">28</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-193">RS-485</span><span class="sxs-lookup"><span data-stu-id="03ac2-193">RS-485</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-194">29</span><span class="sxs-lookup"><span data-stu-id="03ac2-194">29</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-195">RS-449</span><span class="sxs-lookup"><span data-stu-id="03ac2-195">RS-449</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-196">30</span><span class="sxs-lookup"><span data-stu-id="03ac2-196">30</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-197">V. 35</span><span class="sxs-lookup"><span data-stu-id="03ac2-197">V.35</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-198">31</span><span class="sxs-lookup"><span data-stu-id="03ac2-198">31</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-199">X. 21</span><span class="sxs-lookup"><span data-stu-id="03ac2-199">X.21</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-200">32</span><span class="sxs-lookup"><span data-stu-id="03ac2-200">32</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-201">IEEE-488</span><span class="sxs-lookup"><span data-stu-id="03ac2-201">IEEE-488</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-202">33</span><span class="sxs-lookup"><span data-stu-id="03ac2-202">33</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-203">ауи</span><span class="sxs-lookup"><span data-stu-id="03ac2-203">AUI</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-204">34</span><span class="sxs-lookup"><span data-stu-id="03ac2-204">34</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-205">UTP Категория 3</span><span class="sxs-lookup"><span data-stu-id="03ac2-205">UTP Category 3</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-206">35</span><span class="sxs-lookup"><span data-stu-id="03ac2-206">35</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-207">UTP Категория 4</span><span class="sxs-lookup"><span data-stu-id="03ac2-207">UTP Category 4</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-208">36</span><span class="sxs-lookup"><span data-stu-id="03ac2-208">36</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-209">UTP Категория 5</span><span class="sxs-lookup"><span data-stu-id="03ac2-209">UTP Category 5</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-210">37</span><span class="sxs-lookup"><span data-stu-id="03ac2-210">37</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-211">бнк</span><span class="sxs-lookup"><span data-stu-id="03ac2-211">BNC</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-212">38</span><span class="sxs-lookup"><span data-stu-id="03ac2-212">38</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-213">RJ11</span><span class="sxs-lookup"><span data-stu-id="03ac2-213">RJ11</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-214">39</span><span class="sxs-lookup"><span data-stu-id="03ac2-214">39</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-215">RJ45</span><span class="sxs-lookup"><span data-stu-id="03ac2-215">RJ45</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-216">40</span><span class="sxs-lookup"><span data-stu-id="03ac2-216">40</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-217">Оптоволоконный микрофон</span><span class="sxs-lookup"><span data-stu-id="03ac2-217">Fiber MIC</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-218">41</span><span class="sxs-lookup"><span data-stu-id="03ac2-218">41</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-219">Apple АУИ</span><span class="sxs-lookup"><span data-stu-id="03ac2-219">Apple AUI</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-220">42</span><span class="sxs-lookup"><span data-stu-id="03ac2-220">42</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-221">Геопорт Apple</span><span class="sxs-lookup"><span data-stu-id="03ac2-221">Apple GeoPort</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-222">43</span><span class="sxs-lookup"><span data-stu-id="03ac2-222">43</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-223">PCI</span><span class="sxs-lookup"><span data-stu-id="03ac2-223">PCI</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-224">44</span><span class="sxs-lookup"><span data-stu-id="03ac2-224">44</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-225">ISA</span><span class="sxs-lookup"><span data-stu-id="03ac2-225">ISA</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-226">45</span><span class="sxs-lookup"><span data-stu-id="03ac2-226">45</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-227">ИСПОЛЬЗУЕТ</span><span class="sxs-lookup"><span data-stu-id="03ac2-227">EISA</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-228">46</span><span class="sxs-lookup"><span data-stu-id="03ac2-228">46</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-229">VESA</span><span class="sxs-lookup"><span data-stu-id="03ac2-229">VESA</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-230">47</span><span class="sxs-lookup"><span data-stu-id="03ac2-230">47</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-231">СТАНДАРТ</span><span class="sxs-lookup"><span data-stu-id="03ac2-231">PCMCIA</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-232">48</span><span class="sxs-lookup"><span data-stu-id="03ac2-232">48</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-233">Тип PCMCIA I</span><span class="sxs-lookup"><span data-stu-id="03ac2-233">PCMCIA Type I</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-234">49</span><span class="sxs-lookup"><span data-stu-id="03ac2-234">49</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-235">PCMCIA типа II</span><span class="sxs-lookup"><span data-stu-id="03ac2-235">PCMCIA Type II</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-236">50</span><span class="sxs-lookup"><span data-stu-id="03ac2-236">50</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-237">PCMCIA типа III</span><span class="sxs-lookup"><span data-stu-id="03ac2-237">PCMCIA Type III</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-238">51</span><span class="sxs-lookup"><span data-stu-id="03ac2-238">51</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-239">Порт зв</span><span class="sxs-lookup"><span data-stu-id="03ac2-239">ZV Port</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-240">52</span><span class="sxs-lookup"><span data-stu-id="03ac2-240">52</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-241">CardBus</span><span class="sxs-lookup"><span data-stu-id="03ac2-241">CardBus</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-242">53</span><span class="sxs-lookup"><span data-stu-id="03ac2-242">53</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-243">USB</span><span class="sxs-lookup"><span data-stu-id="03ac2-243">USB</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-244">54</span><span class="sxs-lookup"><span data-stu-id="03ac2-244">54</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-245">IEEE 1394</span><span class="sxs-lookup"><span data-stu-id="03ac2-245">IEEE 1394</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-246">55</span><span class="sxs-lookup"><span data-stu-id="03ac2-246">55</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-247">хиппи</span><span class="sxs-lookup"><span data-stu-id="03ac2-247">HIPPI</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-248">56</span><span class="sxs-lookup"><span data-stu-id="03ac2-248">56</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-249">ХССДК (6 контактов)</span><span class="sxs-lookup"><span data-stu-id="03ac2-249">HSSDC (6 pins)</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-250">57</span><span class="sxs-lookup"><span data-stu-id="03ac2-250">57</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-251">гбик</span><span class="sxs-lookup"><span data-stu-id="03ac2-251">GBIC</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-252">58</span><span class="sxs-lookup"><span data-stu-id="03ac2-252">58</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-253">DIN</span><span class="sxs-lookup"><span data-stu-id="03ac2-253">DIN</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-254">59</span><span class="sxs-lookup"><span data-stu-id="03ac2-254">59</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-255">Мини-DIN</span><span class="sxs-lookup"><span data-stu-id="03ac2-255">Mini-DIN</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-256">60</span><span class="sxs-lookup"><span data-stu-id="03ac2-256">60</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-257">Micro-DIN</span><span class="sxs-lookup"><span data-stu-id="03ac2-257">Micro-DIN</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-258">61</span><span class="sxs-lookup"><span data-stu-id="03ac2-258">61</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-259">PS/2</span><span class="sxs-lookup"><span data-stu-id="03ac2-259">PS/2</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-260">62</span><span class="sxs-lookup"><span data-stu-id="03ac2-260">62</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-261">Инфракрасная связь</span><span class="sxs-lookup"><span data-stu-id="03ac2-261">Infrared</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-262">63</span><span class="sxs-lookup"><span data-stu-id="03ac2-262">63</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-263">HP-ХИЛ</span><span class="sxs-lookup"><span data-stu-id="03ac2-263">HP-HIL</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-264">64</span><span class="sxs-lookup"><span data-stu-id="03ac2-264">64</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-265">Доступ. Bus</span><span class="sxs-lookup"><span data-stu-id="03ac2-265">Access.bus</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-266">65</span><span class="sxs-lookup"><span data-stu-id="03ac2-266">65</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-267">нубус</span><span class="sxs-lookup"><span data-stu-id="03ac2-267">NuBus</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-268">66</span><span class="sxs-lookup"><span data-stu-id="03ac2-268">66</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-269">центроникс</span><span class="sxs-lookup"><span data-stu-id="03ac2-269">Centronics</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-270">67</span><span class="sxs-lookup"><span data-stu-id="03ac2-270">67</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-271">Mini-Centronics</span><span class="sxs-lookup"><span data-stu-id="03ac2-271">Mini-Centronics</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-272">68</span><span class="sxs-lookup"><span data-stu-id="03ac2-272">68</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-273">Тип Mini-Centronics-14</span><span class="sxs-lookup"><span data-stu-id="03ac2-273">Mini-Centronics Type-14</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-274">69</span><span class="sxs-lookup"><span data-stu-id="03ac2-274">69</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-275">Тип Mini-Centronics-20</span><span class="sxs-lookup"><span data-stu-id="03ac2-275">Mini-Centronics Type-20</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-276">70</span><span class="sxs-lookup"><span data-stu-id="03ac2-276">70</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-277">Тип Mini-Centronics-26</span><span class="sxs-lookup"><span data-stu-id="03ac2-277">Mini-Centronics Type-26</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-278">71</span><span class="sxs-lookup"><span data-stu-id="03ac2-278">71</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-279">Мышь шины</span><span class="sxs-lookup"><span data-stu-id="03ac2-279">Bus Mouse</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-280">72</span><span class="sxs-lookup"><span data-stu-id="03ac2-280">72</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-281">ADB</span><span class="sxs-lookup"><span data-stu-id="03ac2-281">ADB</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-282">73</span><span class="sxs-lookup"><span data-stu-id="03ac2-282">73</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-283">ИНТЕРФЕЙСА</span><span class="sxs-lookup"><span data-stu-id="03ac2-283">AGP</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-284">74</span><span class="sxs-lookup"><span data-stu-id="03ac2-284">74</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-285">Шина вме</span><span class="sxs-lookup"><span data-stu-id="03ac2-285">VME Bus</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-286">75</span><span class="sxs-lookup"><span data-stu-id="03ac2-286">75</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-287">VME64</span><span class="sxs-lookup"><span data-stu-id="03ac2-287">VME64</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-288">76</span><span class="sxs-lookup"><span data-stu-id="03ac2-288">76</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-289">Частный</span><span class="sxs-lookup"><span data-stu-id="03ac2-289">Proprietary</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-290">77</span><span class="sxs-lookup"><span data-stu-id="03ac2-290">77</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-291">Собственный слот карты процессора</span><span class="sxs-lookup"><span data-stu-id="03ac2-291">Proprietary Processor Card Slot</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-292">78</span><span class="sxs-lookup"><span data-stu-id="03ac2-292">78</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-293">Собственный слот карты памяти</span><span class="sxs-lookup"><span data-stu-id="03ac2-293">Proprietary Memory Card Slot</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-294">79</span><span class="sxs-lookup"><span data-stu-id="03ac2-294">79</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-295">Собственная подплата ввода/вывода</span><span class="sxs-lookup"><span data-stu-id="03ac2-295">Proprietary I/O Riser Slot</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-296">80</span><span class="sxs-lookup"><span data-stu-id="03ac2-296">80</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-297">PCI-66 МГЦ</span><span class="sxs-lookup"><span data-stu-id="03ac2-297">PCI-66MHZ</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-298">81</span><span class="sxs-lookup"><span data-stu-id="03ac2-298">81</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-299">AGP2X</span><span class="sxs-lookup"><span data-stu-id="03ac2-299">AGP2X</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-300">82</span><span class="sxs-lookup"><span data-stu-id="03ac2-300">82</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-301">AGP4X</span><span class="sxs-lookup"><span data-stu-id="03ac2-301">AGP4X</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-302">83</span><span class="sxs-lookup"><span data-stu-id="03ac2-302">83</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-303">PC-98</span><span class="sxs-lookup"><span data-stu-id="03ac2-303">PC-98</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-304">84</span><span class="sxs-lookup"><span data-stu-id="03ac2-304">84</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-305">PC-98-Хиресо</span><span class="sxs-lookup"><span data-stu-id="03ac2-305">PC-98-Hireso</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-306">85</span><span class="sxs-lookup"><span data-stu-id="03ac2-306">85</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-307">PC-H98</span><span class="sxs-lookup"><span data-stu-id="03ac2-307">PC-H98</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-308">86</span><span class="sxs-lookup"><span data-stu-id="03ac2-308">86</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-309">PC-98Note</span><span class="sxs-lookup"><span data-stu-id="03ac2-309">PC-98Note</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-310">87</span><span class="sxs-lookup"><span data-stu-id="03ac2-310">87</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-311">PC-98Full</span><span class="sxs-lookup"><span data-stu-id="03ac2-311">PC-98Full</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-312">88</span><span class="sxs-lookup"><span data-stu-id="03ac2-312">88</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-313">АДАПТЕР SSA SCSI</span><span class="sxs-lookup"><span data-stu-id="03ac2-313">SSA SCSI</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-314">89</span><span class="sxs-lookup"><span data-stu-id="03ac2-314">89</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-315">Кольцевая</span><span class="sxs-lookup"><span data-stu-id="03ac2-315">Circular</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-316">90</span><span class="sxs-lookup"><span data-stu-id="03ac2-316">90</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-317">Соединитель IDE платы</span><span class="sxs-lookup"><span data-stu-id="03ac2-317">On Board IDE Connector</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-318">91</span><span class="sxs-lookup"><span data-stu-id="03ac2-318">91</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-319">Разъем флоппи-дисковода</span><span class="sxs-lookup"><span data-stu-id="03ac2-319">On Board Floppy Connector</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-320">92</span><span class="sxs-lookup"><span data-stu-id="03ac2-320">92</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-321">9. закрепление двух встроенных</span><span class="sxs-lookup"><span data-stu-id="03ac2-321">9 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-322">93</span><span class="sxs-lookup"><span data-stu-id="03ac2-322">93</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-323">25-контактный двойной текст</span><span class="sxs-lookup"><span data-stu-id="03ac2-323">25 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-324">94</span><span class="sxs-lookup"><span data-stu-id="03ac2-324">94</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-325">50. закрепление двух встроенных</span><span class="sxs-lookup"><span data-stu-id="03ac2-325">50 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-326">95</span><span class="sxs-lookup"><span data-stu-id="03ac2-326">95</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-327">68. закрепление двух встроенных</span><span class="sxs-lookup"><span data-stu-id="03ac2-327">68 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-328">96</span><span class="sxs-lookup"><span data-stu-id="03ac2-328">96</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-329">Звуковой разъем на доске</span><span class="sxs-lookup"><span data-stu-id="03ac2-329">On Board Sound Connector</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-330">97</span><span class="sxs-lookup"><span data-stu-id="03ac2-330">97</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-331">Мини-гнездо</span><span class="sxs-lookup"><span data-stu-id="03ac2-331">Mini-jack</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-332">98</span><span class="sxs-lookup"><span data-stu-id="03ac2-332">98</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-333">PCI-X</span><span class="sxs-lookup"><span data-stu-id="03ac2-333">PCI-X</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-334">99</span><span class="sxs-lookup"><span data-stu-id="03ac2-334">99</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-335">Сбус IEEE 1396-1993 32, бит</span><span class="sxs-lookup"><span data-stu-id="03ac2-335">Sbus IEEE 1396-1993 32 bit</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-336">100</span><span class="sxs-lookup"><span data-stu-id="03ac2-336">100</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-337">Сбус IEEE 1396-1993 64, бит</span><span class="sxs-lookup"><span data-stu-id="03ac2-337">Sbus IEEE 1396-1993 64 bit</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-338">101</span><span class="sxs-lookup"><span data-stu-id="03ac2-338">101</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-339">MCA</span><span class="sxs-lookup"><span data-stu-id="03ac2-339">MCA</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-340">102</span><span class="sxs-lookup"><span data-stu-id="03ac2-340">102</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-341">гио</span><span class="sxs-lookup"><span data-stu-id="03ac2-341">GIO</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-342">103</span><span class="sxs-lookup"><span data-stu-id="03ac2-342">103</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-343">XIO</span><span class="sxs-lookup"><span data-stu-id="03ac2-343">XIO</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-344">104</span><span class="sxs-lookup"><span data-stu-id="03ac2-344">104</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-345">хио</span><span class="sxs-lookup"><span data-stu-id="03ac2-345">HIO</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-346">105</span><span class="sxs-lookup"><span data-stu-id="03ac2-346">105</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-347">нгио</span><span class="sxs-lookup"><span data-stu-id="03ac2-347">NGIO</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-348">106</span><span class="sxs-lookup"><span data-stu-id="03ac2-348">106</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-349">PMC</span><span class="sxs-lookup"><span data-stu-id="03ac2-349">PMC</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-350">107</span><span class="sxs-lookup"><span data-stu-id="03ac2-350">107</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-351">мтрж</span><span class="sxs-lookup"><span data-stu-id="03ac2-351">MTRJ</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-352">108</span><span class="sxs-lookup"><span data-stu-id="03ac2-352">108</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-353">VF-45</span><span class="sxs-lookup"><span data-stu-id="03ac2-353">VF-45</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-354">109</span><span class="sxs-lookup"><span data-stu-id="03ac2-354">109</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-355">Будущие операции ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="03ac2-355">Future I/O</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-356">110</span><span class="sxs-lookup"><span data-stu-id="03ac2-356">110</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-357">SC</span><span class="sxs-lookup"><span data-stu-id="03ac2-357">SC</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-358">111</span><span class="sxs-lookup"><span data-stu-id="03ac2-358">111</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-359">SG</span><span class="sxs-lookup"><span data-stu-id="03ac2-359">SG</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-360">112</span><span class="sxs-lookup"><span data-stu-id="03ac2-360">112</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-361">Электричество</span><span class="sxs-lookup"><span data-stu-id="03ac2-361">Electrical</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-362">113</span><span class="sxs-lookup"><span data-stu-id="03ac2-362">113</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-363">Лазер</span><span class="sxs-lookup"><span data-stu-id="03ac2-363">Optical</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-364">114</span><span class="sxs-lookup"><span data-stu-id="03ac2-364">114</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-365">Лента</span><span class="sxs-lookup"><span data-stu-id="03ac2-365">Ribbon</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-366">115</span><span class="sxs-lookup"><span data-stu-id="03ac2-366">115</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-367">GLM</span><span class="sxs-lookup"><span data-stu-id="03ac2-367">GLM</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-368">116</span><span class="sxs-lookup"><span data-stu-id="03ac2-368">116</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-369">1x9</span><span class="sxs-lookup"><span data-stu-id="03ac2-369">1x9</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-370">117</span><span class="sxs-lookup"><span data-stu-id="03ac2-370">117</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-371">Мини-SG</span><span class="sxs-lookup"><span data-stu-id="03ac2-371">Mini SG</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-372">118</span><span class="sxs-lookup"><span data-stu-id="03ac2-372">118</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-373">LC</span><span class="sxs-lookup"><span data-stu-id="03ac2-373">LC</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-374">119</span><span class="sxs-lookup"><span data-stu-id="03ac2-374">119</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-375">хсск</span><span class="sxs-lookup"><span data-stu-id="03ac2-375">HSSC</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-376">120</span><span class="sxs-lookup"><span data-stu-id="03ac2-376">120</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-377">ВХДЦИ экранированный (68 контактов)</span><span class="sxs-lookup"><span data-stu-id="03ac2-377">VHDCI Shielded (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-378">121</span><span class="sxs-lookup"><span data-stu-id="03ac2-378">121</span></span>
</dt> <dd>

<span data-ttu-id="03ac2-379">InfiniBand</span><span class="sxs-lookup"><span data-stu-id="03ac2-379">InfiniBand</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="03ac2-380">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="03ac2-380">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-381">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03ac2-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-383">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="03ac2-383">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-384">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="03ac2-384">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="03ac2-385">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="03ac2-385">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="03ac2-386">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="03ac2-386">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-387">**Описание**</span><span class="sxs-lookup"><span data-stu-id="03ac2-387">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-388">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03ac2-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-389">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-389">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-390">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="03ac2-390">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-391">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="03ac2-391">Textual description of the object.</span></span>

<span data-ttu-id="03ac2-392">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03ac2-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-393">**хеигхталловед**</span><span class="sxs-lookup"><span data-stu-id="03ac2-393">**HeightAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-394">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="03ac2-394">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-395">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-396">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="03ac2-396">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-397">Максимальная высота платы адаптера в дюймах, которую можно вставить в слот.</span><span class="sxs-lookup"><span data-stu-id="03ac2-397">Maximum height, in inches, of an adapter card that can be inserted into the slot.</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-398">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="03ac2-398">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-399">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="03ac2-399">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-400">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-401">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="03ac2-401">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-402">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="03ac2-402">Date and time the object was installed.</span></span> <span data-ttu-id="03ac2-403">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="03ac2-403">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="03ac2-404">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03ac2-404">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-405">**ленгсалловед**</span><span class="sxs-lookup"><span data-stu-id="03ac2-405">**LengthAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-406">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="03ac2-406">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-407">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-408">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="03ac2-408">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-409">Максимальная длина платы адаптера в дюймах, которую можно вставить в слот.</span><span class="sxs-lookup"><span data-stu-id="03ac2-409">Maximum length, in inches, of an adapter card that can be inserted into the slot.</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-410">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="03ac2-410">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-411">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03ac2-411">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-412">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-413">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="03ac2-413">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-414">Организация, создавшая физический элемент.</span><span class="sxs-lookup"><span data-stu-id="03ac2-414">Organization that produced the physical element.</span></span> <span data-ttu-id="03ac2-415">Дополнительные сведения см. в описании свойства **Vendor** [**\_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="03ac2-415">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="03ac2-416">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="03ac2-416">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-417">**максдатавидс**</span><span class="sxs-lookup"><span data-stu-id="03ac2-417">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-418">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03ac2-418">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-419">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-420">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Системный слот DMTF \| 004,3 "), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) (" бит ")</span><span class="sxs-lookup"><span data-stu-id="03ac2-420">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-421">Максимальная ширина шины (в битах) карт адаптеров, которые можно вставить в слот.</span><span class="sxs-lookup"><span data-stu-id="03ac2-421">Maximum bus width, in bits, of adapter cards that can be inserted into the slot.</span></span>

<dt>

<span id="8"></span>

<span data-ttu-id="03ac2-422">**8** (0)</span><span class="sxs-lookup"><span data-stu-id="03ac2-422">**8** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="16"></span>

<span data-ttu-id="03ac2-423">**16** (1)</span><span class="sxs-lookup"><span data-stu-id="03ac2-423">**16** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="32"></span>

<span data-ttu-id="03ac2-424">**32** (2)</span><span class="sxs-lookup"><span data-stu-id="03ac2-424">**32** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="64"></span>

<span data-ttu-id="03ac2-425">**64** (3)</span><span class="sxs-lookup"><span data-stu-id="03ac2-425">**64** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="128"></span>

<span data-ttu-id="03ac2-426">**128** (4)</span><span class="sxs-lookup"><span data-stu-id="03ac2-426">**128** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03ac2-427">**Модель**</span><span class="sxs-lookup"><span data-stu-id="03ac2-427">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-428">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03ac2-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-429">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-430">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="03ac2-430">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-431">Имя, по которому обычно известен физический элемент.</span><span class="sxs-lookup"><span data-stu-id="03ac2-431">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="03ac2-432">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="03ac2-432">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-433">**Name**</span><span class="sxs-lookup"><span data-stu-id="03ac2-433">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-434">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03ac2-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-435">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-436">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="03ac2-436">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-437">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="03ac2-437">Label by which the object is known.</span></span> <span data-ttu-id="03ac2-438">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="03ac2-438">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="03ac2-439">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03ac2-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-440">**Число**</span><span class="sxs-lookup"><span data-stu-id="03ac2-440">**Number**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-441">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03ac2-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-442">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-443">Номер физического слота, который можно использовать в качестве индекса в таблице системных слотов, чтобы определить, является ли слот физически занятым.</span><span class="sxs-lookup"><span data-stu-id="03ac2-443">Physical slot number, which can be used as an index into a system slot table, to determine whether the slot is physically occupied.</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-444">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="03ac2-444">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-445">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03ac2-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-446">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-447">Дополнительные данные, помимо сведений о тегах актива, которые можно использовать для поиска физического элемента.</span><span class="sxs-lookup"><span data-stu-id="03ac2-447">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="03ac2-448">Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива.</span><span class="sxs-lookup"><span data-stu-id="03ac2-448">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="03ac2-449">Обратите внимание, что если доступны только данные с штрих-кодом и они уникальны и могут использоваться в качестве ключа элемента, это свойство будет иметь значение null, а данные штрих-кода будут использоваться в качестве ключа класса в свойстве **Tag** .</span><span class="sxs-lookup"><span data-stu-id="03ac2-449">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="03ac2-450">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="03ac2-450">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-451">**партнумбер**</span><span class="sxs-lookup"><span data-stu-id="03ac2-451">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-452">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03ac2-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-453">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-454">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="03ac2-454">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-455">Номер детали, назначенный Организацией, которая создала или изготовлена физический элемент.</span><span class="sxs-lookup"><span data-stu-id="03ac2-455">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="03ac2-456">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="03ac2-456">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-457">**повередон**</span><span class="sxs-lookup"><span data-stu-id="03ac2-457">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-458">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="03ac2-458">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-459">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-460">**Значение true** показывает, что физический элемент включен.</span><span class="sxs-lookup"><span data-stu-id="03ac2-460">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="03ac2-461">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="03ac2-461">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-462">**пурпоседескриптион**</span><span class="sxs-lookup"><span data-stu-id="03ac2-462">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-463">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03ac2-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-464">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-465">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ область CIM**".**СпеЦиалпурпосе**")</span><span class="sxs-lookup"><span data-stu-id="03ac2-465">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Slot**.**SpecialPurpose**")</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-466">Произвольная строка, описывающая, как этот слот физически уникален и может содержать специальные типы оборудования.</span><span class="sxs-lookup"><span data-stu-id="03ac2-466">Free-form string that describes how this slot is physically unique and that it may hold special types of hardware.</span></span> <span data-ttu-id="03ac2-467">Это свойство имеет значение, только если соответствующее логическое свойство **спеЦиалпурпосе** имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="03ac2-467">This property only has meaning when the corresponding Boolean **SpecialPurpose** property is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-468">**Номер**</span><span class="sxs-lookup"><span data-stu-id="03ac2-468">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-469">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03ac2-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-470">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-471">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="03ac2-471">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-472">Номер, выделенный изготовителем, используемый для распознавания физического элемента.</span><span class="sxs-lookup"><span data-stu-id="03ac2-472">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="03ac2-473">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="03ac2-473">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-474">**SKU**</span><span class="sxs-lookup"><span data-stu-id="03ac2-474">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-475">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03ac2-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-476">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-477">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="03ac2-477">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-478">Номер единицы хранения для физического элемента.</span><span class="sxs-lookup"><span data-stu-id="03ac2-478">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="03ac2-479">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="03ac2-479">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-480">**спеЦиалпурпосе**</span><span class="sxs-lookup"><span data-stu-id="03ac2-480">**SpecialPurpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-481">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="03ac2-481">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-482">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-483">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ область CIM**".**Пурпоседескриптион**")</span><span class="sxs-lookup"><span data-stu-id="03ac2-483">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Slot**.**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-484">Если **значение равно true**, слот физически уникален и может содержать специальные типы оборудования (например, разъем для графического процессора).</span><span class="sxs-lookup"><span data-stu-id="03ac2-484">If **TRUE**, the slot is physically unique and may hold special types of hardware, (for example, a graphics processor slot).</span></span> <span data-ttu-id="03ac2-485">Если **значение — true**, свойство **пурпоседескриптион** должно указывать, как сегмент является уникальным или назначением слота.</span><span class="sxs-lookup"><span data-stu-id="03ac2-485">If **TRUE**, the **PurposeDescription** property should specify how the slot is unique or the slot's purpose.</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-486">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="03ac2-486">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-487">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03ac2-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-488">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-489">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="03ac2-489">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-490">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="03ac2-490">Current status of the object.</span></span> <span data-ttu-id="03ac2-491">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03ac2-491">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="03ac2-492">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="03ac2-492">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="03ac2-493">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="03ac2-493">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="03ac2-494">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="03ac2-494">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="03ac2-495">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="03ac2-495">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03ac2-496">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="03ac2-496">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="03ac2-497">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="03ac2-497">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="03ac2-498">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="03ac2-498">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="03ac2-499">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="03ac2-499">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="03ac2-500">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="03ac2-500">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="03ac2-501">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="03ac2-501">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="03ac2-502">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="03ac2-502">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="03ac2-503">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="03ac2-503">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="03ac2-504">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="03ac2-504">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03ac2-505">**суппортшотплуг**</span><span class="sxs-lookup"><span data-stu-id="03ac2-505">**SupportsHotPlug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-506">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="03ac2-506">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-507">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-508">Если **значение — true**, слот поддерживает горячее подключение адаптеров.</span><span class="sxs-lookup"><span data-stu-id="03ac2-508">If **TRUE**, the slot supports hot-plugging of adapter cards.</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-509">**Тег**</span><span class="sxs-lookup"><span data-stu-id="03ac2-509">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-510">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03ac2-510">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-511">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-512">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="03ac2-512">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-513">Произвольная строка, однозначно идентифицирующая физический элемент и служащая в качестве ключа элемента.</span><span class="sxs-lookup"><span data-stu-id="03ac2-513">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="03ac2-514">Это свойство может содержать такие сведения, как тег актива или данные серийного номера.</span><span class="sxs-lookup"><span data-stu-id="03ac2-514">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="03ac2-515">Ключ для [**CIM \_ фисикалелемент**](cim-physicalelement.md) помещается очень высоким в иерархии объектов для независимого обнаружения оборудования или сущности независимо от физического размещения в (или в) шкафов, адаптеров и т. д.</span><span class="sxs-lookup"><span data-stu-id="03ac2-515">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware/entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="03ac2-516">Например, съемный компонент, который можно использовать для горячей замены, может быть взят из содержащего его пакета (с областями видимости) и временно не используется.</span><span class="sxs-lookup"><span data-stu-id="03ac2-516">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="03ac2-517">Объект по-прежнему продолжает существовать и даже может быть вставлен в другой контейнер области.</span><span class="sxs-lookup"><span data-stu-id="03ac2-517">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="03ac2-518">Ключом для физического элемента является произвольная строка, которая определяется независимо от размещения или расположения, ориентированного на расположение.</span><span class="sxs-lookup"><span data-stu-id="03ac2-518">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="03ac2-519">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="03ac2-519">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-520">**сермалратинг**</span><span class="sxs-lookup"><span data-stu-id="03ac2-520">**ThermalRating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-521">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03ac2-521">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-522">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-523">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Системный слот DMTF \| 004,11 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" МВт ")</span><span class="sxs-lookup"><span data-stu-id="03ac2-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-524">Максимальное рассеяние температуры слота в МВт.</span><span class="sxs-lookup"><span data-stu-id="03ac2-524">Maximum thermal dissipation of the slot, in milliwatts.</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-525">**вккмикседволтажесуппорт**</span><span class="sxs-lookup"><span data-stu-id="03ac2-525">**VccMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-526">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="03ac2-526">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-527">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-527">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-528">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Системный слот DMTF \| 004,9 ")</span><span class="sxs-lookup"><span data-stu-id="03ac2-528">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-529">Напряжение VCC, поддерживаемое слотом.</span><span class="sxs-lookup"><span data-stu-id="03ac2-529">Vcc voltage supported by the slot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03ac2-530">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="03ac2-530">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="03ac2-531">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="03ac2-531">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="03ac2-532">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="03ac2-532">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="03ac2-533">**5** в (3)</span><span class="sxs-lookup"><span data-stu-id="03ac2-533">**5V** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03ac2-534">**Version**</span><span class="sxs-lookup"><span data-stu-id="03ac2-534">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-535">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03ac2-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-536">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-536">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-537">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="03ac2-537">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-538">Версия физического элемента.</span><span class="sxs-lookup"><span data-stu-id="03ac2-538">Version of the physical element.</span></span>

<span data-ttu-id="03ac2-539">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="03ac2-539">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03ac2-540">**вппмикседволтажесуппорт**</span><span class="sxs-lookup"><span data-stu-id="03ac2-540">**VppMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ac2-541">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="03ac2-541">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-542">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03ac2-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03ac2-543">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Системный слот DMTF \| 004,10 ")</span><span class="sxs-lookup"><span data-stu-id="03ac2-543">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.10")</span></span>
</dt> </dl>

<span data-ttu-id="03ac2-544">Напряжение VPP, поддерживаемое слотом.</span><span class="sxs-lookup"><span data-stu-id="03ac2-544">Vpp voltage supported by the slot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03ac2-545">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="03ac2-545">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="03ac2-546">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="03ac2-546">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="03ac2-547">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="03ac2-547">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="03ac2-548">**5** в (3)</span><span class="sxs-lookup"><span data-stu-id="03ac2-548">**5V** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

<span data-ttu-id="03ac2-549">**12** в (4)</span><span class="sxs-lookup"><span data-stu-id="03ac2-549">**12V** (4)</span></span>


<span data-ttu-id="03ac2-550"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="03ac2-550"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="03ac2-551">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03ac2-551">Remarks</span></span>

<span data-ttu-id="03ac2-552">Класс **\_ слота CIM** является производным от [**CIM \_ фисикалконнектор**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="03ac2-552">The **CIM\_Slot** class is derived from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<span data-ttu-id="03ac2-553">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="03ac2-553">WMI does not implement this class.</span></span> <span data-ttu-id="03ac2-554">Сведения о классах WMI, производных от **\_ области CIM**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="03ac2-554">For WMI classes derived from **CIM\_Slot**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="03ac2-555">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="03ac2-555">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="03ac2-556">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="03ac2-556">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="03ac2-557">Требования</span><span class="sxs-lookup"><span data-stu-id="03ac2-557">Requirements</span></span>



| <span data-ttu-id="03ac2-558">Требование</span><span class="sxs-lookup"><span data-stu-id="03ac2-558">Requirement</span></span> | <span data-ttu-id="03ac2-559">Значение</span><span class="sxs-lookup"><span data-stu-id="03ac2-559">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03ac2-560">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="03ac2-560">Minimum supported client</span></span><br/> | <span data-ttu-id="03ac2-561">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03ac2-561">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03ac2-562">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="03ac2-562">Minimum supported server</span></span><br/> | <span data-ttu-id="03ac2-563">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03ac2-563">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03ac2-564">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="03ac2-564">Namespace</span></span><br/>                | <span data-ttu-id="03ac2-565">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="03ac2-565">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="03ac2-566">MOF</span><span class="sxs-lookup"><span data-stu-id="03ac2-566">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03ac2-567"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03ac2-567"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="03ac2-568">DLL</span><span class="sxs-lookup"><span data-stu-id="03ac2-568">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03ac2-569"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03ac2-569"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03ac2-570">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03ac2-570">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03ac2-571">**\_ФИСИКАЛКОННЕКТОР CIM**</span><span class="sxs-lookup"><span data-stu-id="03ac2-571">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> </dl>

 

