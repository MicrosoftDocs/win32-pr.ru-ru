---
description: '&Win32 \_ системслот \# 32; Класс WMI представляет физические точки подключения, включая порты, гнезда материнской платы и периферийные устройства, а также частные точки подключения.'
ms.assetid: 0bdce597-dcbe-4593-b0d6-68c3bfecd0ee
ms.tgt_platform: multiple
title: Класс Win32_SystemSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSlot
- Win32_SystemSlot.BusNumber
- Win32_SystemSlot.Caption
- Win32_SystemSlot.ConnectorPinout
- Win32_SystemSlot.ConnectorType
- Win32_SystemSlot.CreationClassName
- Win32_SystemSlot.CurrentUsage
- Win32_SystemSlot.Description
- Win32_SystemSlot.DeviceNumber
- Win32_SystemSlot.FunctionNumber
- Win32_SystemSlot.HeightAllowed
- Win32_SystemSlot.InstallDate
- Win32_SystemSlot.LengthAllowed
- Win32_SystemSlot.Manufacturer
- Win32_SystemSlot.MaxDataWidth
- Win32_SystemSlot.Model
- Win32_SystemSlot.Name
- Win32_SystemSlot.Number
- Win32_SystemSlot.OtherIdentifyingInfo
- Win32_SystemSlot.PartNumber
- Win32_SystemSlot.PMESignal
- Win32_SystemSlot.PoweredOn
- Win32_SystemSlot.PurposeDescription
- Win32_SystemSlot.SegmentGroupNumber
- Win32_SystemSlot.SerialNumber
- Win32_SystemSlot.Shared
- Win32_SystemSlot.SKU
- Win32_SystemSlot.SlotDesignation
- Win32_SystemSlot.SpecialPurpose
- Win32_SystemSlot.Status
- Win32_SystemSlot.SupportsHotPlug
- Win32_SystemSlot.Tag
- Win32_SystemSlot.ThermalRating
- Win32_SystemSlot.VccMixedVoltageSupport
- Win32_SystemSlot.Version
- Win32_SystemSlot.VppMixedVoltageSupport
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1e2913aa2d8850aae4fdad8fbca71f216cd848f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142667"
---
# <a name="win32_systemslot-class"></a><span data-ttu-id="444ba-103">\_Класс Win32 системслот</span><span class="sxs-lookup"><span data-stu-id="444ba-103">Win32\_SystemSlot class</span></span>

<span data-ttu-id="444ba-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ системслот для Win32** представляет физические точки подключения, включая порты, гнезду материнской платы и периферийные устройства, а также частные точки подключения.</span><span class="sxs-lookup"><span data-stu-id="444ba-104">The **Win32\_SystemSlot** [WMI class](../wmisdk/retrieving-a-class.md) represents physical connection points including ports, motherboard slots and peripherals, and proprietary connection points.</span></span>

<span data-ttu-id="444ba-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="444ba-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="444ba-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="444ba-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="444ba-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="444ba-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B91-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSlot : CIM_Slot
{
  uint32   BusNumber;
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  uint16   CurrentUsage;
  string   Description;
  uint32   DeviceNumber;
  uint32   FunctionNumber;
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
  boolean  PMESignal;
  boolean  PoweredOn;
  string   PurposeDescription;
  uint32   SegmentGroupNumber;
  string   SerialNumber;
  boolean  Shared;
  string   SKU;
  string   SlotDesignation;
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

## <a name="members"></a><span data-ttu-id="444ba-108">Члены</span><span class="sxs-lookup"><span data-stu-id="444ba-108">Members</span></span>

<span data-ttu-id="444ba-109">Класс **Win32 \_ системслот** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="444ba-109">The **Win32\_SystemSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="444ba-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="444ba-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="444ba-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="444ba-111">Properties</span></span>

<span data-ttu-id="444ba-112">Класс **Win32 \_ системслот** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="444ba-112">The **Win32\_SystemSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="444ba-113">**буснумбер**</span><span class="sxs-lookup"><span data-stu-id="444ba-113">**BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="444ba-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-116">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 9 \| номер шины")</span><span class="sxs-lookup"><span data-stu-id="444ba-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Bus Number")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-117">Номер шины SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="444ba-117">SMBIOS Bus Number.</span></span>

<span data-ttu-id="444ba-118">Это значение берется из элемента **номер шины** в структуре **системных слотов** в информации SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="444ba-118">This value comes from the **Bus Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="444ba-119">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="444ba-119">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="444ba-120">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="444ba-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="444ba-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-123">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="444ba-123">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-124">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="444ba-124">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="444ba-125">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-126">**коннекторпинаут**</span><span class="sxs-lookup"><span data-stu-id="444ba-126">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="444ba-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="444ba-129">Произвольная строка, описывающая конфигурацию ПИН-кода и использование сигнала физического соединителя.</span><span class="sxs-lookup"><span data-stu-id="444ba-129">Free-form string that describes the pin configuration and signal usage of a physical connector.</span></span>

<span data-ttu-id="444ba-130">Это свойство наследуется от [**CIM \_ фисикалконнектор**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-130">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-131">**коннектортипе**</span><span class="sxs-lookup"><span data-stu-id="444ba-131">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-132">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="444ba-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="444ba-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-134">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("коннектортипе"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("тип SMBIOS \| 9 \| " Тип слота ")</span><span class="sxs-lookup"><span data-stu-id="444ba-134">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Type")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-135">Массив физических атрибутов соединителя, используемого этим слотом.</span><span class="sxs-lookup"><span data-stu-id="444ba-135">Array of physical attributes of the connector that this slot uses.</span></span>

<span data-ttu-id="444ba-136">Это значение берется из элемента **типа слота** в структуре **системных слотов** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="444ba-136">This value comes from the **Slot Type** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="444ba-137">Это свойство наследуется от [**CIM \_ фисикалконнектор**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-137">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<span data-ttu-id="444ba-138">Возможные значения:.</span><span class="sxs-lookup"><span data-stu-id="444ba-138">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="444ba-139">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="444ba-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="444ba-140">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="444ba-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span data-ttu-id="444ba-141">**Штекер** (2)</span><span class="sxs-lookup"><span data-stu-id="444ba-141">**Male** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span data-ttu-id="444ba-142">**Женщина** (3)</span><span class="sxs-lookup"><span data-stu-id="444ba-142">**Female** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="444ba-143">**Экранированный** (4)</span><span class="sxs-lookup"><span data-stu-id="444ba-143">**Shielded** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span data-ttu-id="444ba-144">**Неэкранированный** (5)</span><span class="sxs-lookup"><span data-stu-id="444ba-144">**Unshielded** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span data-ttu-id="444ba-145">**SCSI (A) High-Density (50 ПИН-коды)** (6)</span><span class="sxs-lookup"><span data-stu-id="444ba-145">**SCSI (A) High-Density (50 pins)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span data-ttu-id="444ba-146">**SCSI (A) Low-Density (50 ПИН-коды)** (7)</span><span class="sxs-lookup"><span data-stu-id="444ba-146">**SCSI (A) Low-Density (50 pins)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span data-ttu-id="444ba-147">**High-Density SCSI (P) (68 ПИН-коды)** (8)</span><span class="sxs-lookup"><span data-stu-id="444ba-147">**SCSI (P) High-Density (68 pins)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span data-ttu-id="444ba-148">**SCSI SCA-I (80 ПИН)** (9)</span><span class="sxs-lookup"><span data-stu-id="444ba-148">**SCSI SCA-I (80 pins)** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span data-ttu-id="444ba-149">**SCSI SCA-II (80 контактов)** (10)</span><span class="sxs-lookup"><span data-stu-id="444ba-149">**SCSI SCA-II (80 pins)** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span data-ttu-id="444ba-150">**Fibre Channel SCSI (DB-9, медный)** (11)</span><span class="sxs-lookup"><span data-stu-id="444ba-150">**SCSI Fibre Channel (DB-9, Copper)** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span data-ttu-id="444ba-151">**Fibre Channel SCSI (Fibre)** (12)</span><span class="sxs-lookup"><span data-stu-id="444ba-151">**SCSI Fibre Channel (Fibre)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span data-ttu-id="444ba-152">**SCSI Fibre Channel SCA-II (40 ПИН)** (13)</span><span class="sxs-lookup"><span data-stu-id="444ba-152">**SCSI Fibre Channel SCA-II (40 pins)** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span data-ttu-id="444ba-153">**SCSI Fibre Channel SCA-II (20 контактов)** (14)</span><span class="sxs-lookup"><span data-stu-id="444ba-153">**SCSI Fibre Channel SCA-II (20 pins)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span data-ttu-id="444ba-154">**SCSI Fibre Channel БНК** (15)</span><span class="sxs-lookup"><span data-stu-id="444ba-154">**SCSI Fibre Channel BNC** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span data-ttu-id="444ba-155">**ATA 3-1/2 дюйма (40 контактов)** (16)</span><span class="sxs-lookup"><span data-stu-id="444ba-155">**ATA 3-1/2 Inch (40 pins)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span data-ttu-id="444ba-156">**ATA 2-1/2 дюйма (44 контактов)** (17)</span><span class="sxs-lookup"><span data-stu-id="444ba-156">**ATA 2-1/2 Inch (44 pins)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span data-ttu-id="444ba-157">**ATA-2** (18)</span><span class="sxs-lookup"><span data-stu-id="444ba-157">**ATA-2** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span data-ttu-id="444ba-158">**ATA-3** (19)</span><span class="sxs-lookup"><span data-stu-id="444ba-158">**ATA-3** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span data-ttu-id="444ba-159">**ATA/66** (20)</span><span class="sxs-lookup"><span data-stu-id="444ba-159">**ATA/66** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span data-ttu-id="444ba-160">**DB-9** (21)</span><span class="sxs-lookup"><span data-stu-id="444ba-160">**DB-9** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span data-ttu-id="444ba-161">**DB-15** (22)</span><span class="sxs-lookup"><span data-stu-id="444ba-161">**DB-15** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span data-ttu-id="444ba-162">**DB-25** (23)</span><span class="sxs-lookup"><span data-stu-id="444ba-162">**DB-25** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span data-ttu-id="444ba-163">**DB-36** (24)</span><span class="sxs-lookup"><span data-stu-id="444ba-163">**DB-36** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span data-ttu-id="444ba-164">**RS-232c** (25)</span><span class="sxs-lookup"><span data-stu-id="444ba-164">**RS-232C** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span data-ttu-id="444ba-165">**RS-422** (26)</span><span class="sxs-lookup"><span data-stu-id="444ba-165">**RS-422** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span data-ttu-id="444ba-166">**RS-423** (27)</span><span class="sxs-lookup"><span data-stu-id="444ba-166">**RS-423** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span data-ttu-id="444ba-167">**RS-485** (28)</span><span class="sxs-lookup"><span data-stu-id="444ba-167">**RS-485** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span data-ttu-id="444ba-168">**RS-449** (29)</span><span class="sxs-lookup"><span data-stu-id="444ba-168">**RS-449** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="444ba-169">**V. 35** (30)</span><span class="sxs-lookup"><span data-stu-id="444ba-169">**V.35** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span data-ttu-id="444ba-170">**X. 21** (31)</span><span class="sxs-lookup"><span data-stu-id="444ba-170">**X.21** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="444ba-171">**IEEE-488** (32)</span><span class="sxs-lookup"><span data-stu-id="444ba-171">**IEEE-488** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span data-ttu-id="444ba-172">**АУИ** (33)</span><span class="sxs-lookup"><span data-stu-id="444ba-172">**AUI** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span data-ttu-id="444ba-173">**UTP Категория 3** (34)</span><span class="sxs-lookup"><span data-stu-id="444ba-173">**UTP Category 3** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span data-ttu-id="444ba-174">**UTP Категория 4** (35)</span><span class="sxs-lookup"><span data-stu-id="444ba-174">**UTP Category 4** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span data-ttu-id="444ba-175">**UTP Category 5** (36)</span><span class="sxs-lookup"><span data-stu-id="444ba-175">**UTP Category 5** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span data-ttu-id="444ba-176">**БНК** (37)</span><span class="sxs-lookup"><span data-stu-id="444ba-176">**BNC** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span data-ttu-id="444ba-177">**RJ11** (38)</span><span class="sxs-lookup"><span data-stu-id="444ba-177">**RJ11** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span data-ttu-id="444ba-178">**RJ45** (39)</span><span class="sxs-lookup"><span data-stu-id="444ba-178">**RJ45** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span data-ttu-id="444ba-179">**Оптоволоконный микрофон** (40)</span><span class="sxs-lookup"><span data-stu-id="444ba-179">**Fiber MIC** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span data-ttu-id="444ba-180">**Apple АУИ** (41)</span><span class="sxs-lookup"><span data-stu-id="444ba-180">**Apple AUI** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span data-ttu-id="444ba-181">**Геопорт Apple** (42)</span><span class="sxs-lookup"><span data-stu-id="444ba-181">**Apple GeoPort** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="444ba-182">**PCI** (43)</span><span class="sxs-lookup"><span data-stu-id="444ba-182">**PCI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="444ba-183">**ISA** (44)</span><span class="sxs-lookup"><span data-stu-id="444ba-183">**ISA** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="444ba-184">**EISA** (45)</span><span class="sxs-lookup"><span data-stu-id="444ba-184">**EISA** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="444ba-185">**VESA** (46)</span><span class="sxs-lookup"><span data-stu-id="444ba-185">**VESA** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="444ba-186">**PCMCIA** (47)</span><span class="sxs-lookup"><span data-stu-id="444ba-186">**PCMCIA** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span data-ttu-id="444ba-187">**Тип PCMCIA I** (48)</span><span class="sxs-lookup"><span data-stu-id="444ba-187">**PCMCIA Type I** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="444ba-188">**PCMCIA типа II** (49)</span><span class="sxs-lookup"><span data-stu-id="444ba-188">**PCMCIA Type II** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="444ba-189">**PCMCIA типа III** (50)</span><span class="sxs-lookup"><span data-stu-id="444ba-189">**PCMCIA Type III** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span data-ttu-id="444ba-190">**Порт зв** (51)</span><span class="sxs-lookup"><span data-stu-id="444ba-190">**ZV Port** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="444ba-191">**CardBus** (52)</span><span class="sxs-lookup"><span data-stu-id="444ba-191">**CardBus** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="444ba-192">**USB** (53)</span><span class="sxs-lookup"><span data-stu-id="444ba-192">**USB** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="444ba-193">**IEEE 1394** (54)</span><span class="sxs-lookup"><span data-stu-id="444ba-193">**IEEE 1394** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="444ba-194">**Хиппи** (55)</span><span class="sxs-lookup"><span data-stu-id="444ba-194">**HIPPI** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span data-ttu-id="444ba-195">**Хссдк (6 контактов)** (56)</span><span class="sxs-lookup"><span data-stu-id="444ba-195">**HSSDC (6 pins)** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span data-ttu-id="444ba-196">**Гбик** (57)</span><span class="sxs-lookup"><span data-stu-id="444ba-196">**GBIC** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span data-ttu-id="444ba-197">**DIN** (58)</span><span class="sxs-lookup"><span data-stu-id="444ba-197">**DIN** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span data-ttu-id="444ba-198">**Мини-DIN** (59)</span><span class="sxs-lookup"><span data-stu-id="444ba-198">**Mini-DIN** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span data-ttu-id="444ba-199">**Micro-DIN** (60)</span><span class="sxs-lookup"><span data-stu-id="444ba-199">**Micro-DIN** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="444ba-200">**PS/2** (61)</span><span class="sxs-lookup"><span data-stu-id="444ba-200">**PS/2** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="444ba-201">**Инфракрасная связь** (62)</span><span class="sxs-lookup"><span data-stu-id="444ba-201">**Infrared** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="444ba-202">**HP-Хил** (63)</span><span class="sxs-lookup"><span data-stu-id="444ba-202">**HP-HIL** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span data-ttu-id="444ba-203">**Доступ. Bus** (64)</span><span class="sxs-lookup"><span data-stu-id="444ba-203">**Access.bus** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="444ba-204">**Нубус** (65)</span><span class="sxs-lookup"><span data-stu-id="444ba-204">**NuBus** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span data-ttu-id="444ba-205">**Центроникс** (66)</span><span class="sxs-lookup"><span data-stu-id="444ba-205">**Centronics** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span data-ttu-id="444ba-206">**Мини-центроникс** (67)</span><span class="sxs-lookup"><span data-stu-id="444ba-206">**Mini-Centronics** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span data-ttu-id="444ba-207">**Тип мини-центроникс — 14** (68)</span><span class="sxs-lookup"><span data-stu-id="444ba-207">**Mini-Centronics Type-14** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span data-ttu-id="444ba-208">**Mini-Центроникс Type-20** (69)</span><span class="sxs-lookup"><span data-stu-id="444ba-208">**Mini-Centronics Type-20** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span data-ttu-id="444ba-209">**Mini-Центроникс Type-26** (70)</span><span class="sxs-lookup"><span data-stu-id="444ba-209">**Mini-Centronics Type-26** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="444ba-210">**Мышь шины** (71)</span><span class="sxs-lookup"><span data-stu-id="444ba-210">**Bus Mouse** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span data-ttu-id="444ba-211">**ADB** (72)</span><span class="sxs-lookup"><span data-stu-id="444ba-211">**ADB** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="444ba-212">**AGP** (73)</span><span class="sxs-lookup"><span data-stu-id="444ba-212">**AGP** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="444ba-213">**Шина вме** (74)</span><span class="sxs-lookup"><span data-stu-id="444ba-213">**VME Bus** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span data-ttu-id="444ba-214">**VME64** (75)</span><span class="sxs-lookup"><span data-stu-id="444ba-214">**VME64** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="444ba-215">**Частный** (76)</span><span class="sxs-lookup"><span data-stu-id="444ba-215">**Proprietary** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span data-ttu-id="444ba-216">**Собственный слот карты процессора** (77)</span><span class="sxs-lookup"><span data-stu-id="444ba-216">**Proprietary Processor Card Slot** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span data-ttu-id="444ba-217">**Собственный слот карты памяти** (78)</span><span class="sxs-lookup"><span data-stu-id="444ba-217">**Proprietary Memory Card Slot** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span data-ttu-id="444ba-218">**Собственная Подплата ввода/вывода** (79)</span><span class="sxs-lookup"><span data-stu-id="444ba-218">**Proprietary I/O Riser Slot** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span data-ttu-id="444ba-219">**PCI-66** (80)</span><span class="sxs-lookup"><span data-stu-id="444ba-219">**PCI-66MHZ** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span data-ttu-id="444ba-220">**AGP2X** (81)</span><span class="sxs-lookup"><span data-stu-id="444ba-220">**AGP2X** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span data-ttu-id="444ba-221">**AGP4X** (82)</span><span class="sxs-lookup"><span data-stu-id="444ba-221">**AGP4X** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="444ba-222">**PC-98** (83)</span><span class="sxs-lookup"><span data-stu-id="444ba-222">**PC-98** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="444ba-223">**PC-98-хиресо** (84)</span><span class="sxs-lookup"><span data-stu-id="444ba-223">**PC-98-Hireso** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="444ba-224">**PC-H98** (85)</span><span class="sxs-lookup"><span data-stu-id="444ba-224">**PC-H98** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span data-ttu-id="444ba-225">**PC-98Note** (86)</span><span class="sxs-lookup"><span data-stu-id="444ba-225">**PC-98Note** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span data-ttu-id="444ba-226">**PC-98Full** (87)</span><span class="sxs-lookup"><span data-stu-id="444ba-226">**PC-98Full** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-X"></span><span id="pci-x"></span>

<span data-ttu-id="444ba-227">**PCI-X** (88)</span><span class="sxs-lookup"><span data-stu-id="444ba-227">**PCI-X** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_32_bit"></span><span id="sbus_ieee_1396-1993_32_bit"></span><span id="SBUS_IEEE_1396-1993_32_BIT"></span>

<span data-ttu-id="444ba-228">**СБУС IEEE 1396-1993 32, бит** (89)</span><span class="sxs-lookup"><span data-stu-id="444ba-228">**Sbus IEEE 1396-1993 32 bit** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_64_bit"></span><span id="sbus_ieee_1396-1993_64_bit"></span><span id="SBUS_IEEE_1396-1993_64_BIT"></span>

<span data-ttu-id="444ba-229">**СБУС IEEE 1396-1993 64, бит** (90)</span><span class="sxs-lookup"><span data-stu-id="444ba-229">**Sbus IEEE 1396-1993 64 bit** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="444ba-230">**MCA** (91)</span><span class="sxs-lookup"><span data-stu-id="444ba-230">**MCA** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="GIO"></span><span id="gio"></span>

<span data-ttu-id="444ba-231">**ГИО** (92)</span><span class="sxs-lookup"><span data-stu-id="444ba-231">**GIO** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="XIO"></span><span id="xio"></span>

<span data-ttu-id="444ba-232">**XIO** (93)</span><span class="sxs-lookup"><span data-stu-id="444ba-232">**XIO** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="HIO"></span><span id="hio"></span>

<span data-ttu-id="444ba-233">**Хио** (94)</span><span class="sxs-lookup"><span data-stu-id="444ba-233">**HIO** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="NGIO"></span><span id="ngio"></span>

<span data-ttu-id="444ba-234">**Нгио** (95)</span><span class="sxs-lookup"><span data-stu-id="444ba-234">**NGIO** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="PMC"></span><span id="pmc"></span>

<span data-ttu-id="444ba-235">**PMC** (96)</span><span class="sxs-lookup"><span data-stu-id="444ba-235">**PMC** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Future_I_O"></span><span id="future_i_o"></span><span id="FUTURE_I_O"></span>

<span data-ttu-id="444ba-236">**Будущие операции ввода-вывода** (97)</span><span class="sxs-lookup"><span data-stu-id="444ba-236">**Future I/O** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="InfiniBand"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

<span data-ttu-id="444ba-237">**InfiniBand** (98)</span><span class="sxs-lookup"><span data-stu-id="444ba-237">**InfiniBand** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP8X"></span><span id="agp8x"></span>

<span data-ttu-id="444ba-238">**AGP8X** (99)</span><span class="sxs-lookup"><span data-stu-id="444ba-238">**AGP8X** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-E"></span><span id="pci-e"></span>

<span data-ttu-id="444ba-239">**PCI-E** (100)</span><span class="sxs-lookup"><span data-stu-id="444ba-239">**PCI-E** (100)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="444ba-240">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="444ba-240">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-241">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="444ba-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-243">Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="444ba-243">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="444ba-244">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="444ba-244">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="444ba-245">При использовании с другими ключевыми свойствами класса это свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="444ba-245">When used with the other key properties of a class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="444ba-246">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-246">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-247">**куррентусаже**</span><span class="sxs-lookup"><span data-stu-id="444ba-247">**CurrentUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-248">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="444ba-248">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-249">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-250">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| Текущее использование SMBIOS Type 9 \| ")</span><span class="sxs-lookup"><span data-stu-id="444ba-250">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Current Usage")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-251">Состояние использования системного слота.</span><span class="sxs-lookup"><span data-stu-id="444ba-251">Status of system slot use.</span></span>

<span data-ttu-id="444ba-252">Это значение берется из **текущего члена использования** структуры **системных слотов** в информации SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="444ba-252">This value comes from the **Current Usage** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="444ba-253">Возможные значения:.</span><span class="sxs-lookup"><span data-stu-id="444ba-253">The possible values are.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="444ba-254">**Зарезервировано** (0)</span><span class="sxs-lookup"><span data-stu-id="444ba-254">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="444ba-255">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="444ba-255">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="444ba-256">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="444ba-256">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="444ba-257">**Доступно** (3)</span><span class="sxs-lookup"><span data-stu-id="444ba-257">**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_use"></span><span id="in_use"></span><span id="IN_USE"></span>

<span data-ttu-id="444ba-258">**Используется** (4)</span><span class="sxs-lookup"><span data-stu-id="444ba-258">**In use** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="444ba-259">**Описание**</span><span class="sxs-lookup"><span data-stu-id="444ba-259">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-260">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="444ba-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-261">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-262">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="444ba-262">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-263">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="444ba-263">Description of the object.</span></span>

<span data-ttu-id="444ba-264">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-264">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-265">**девиценумбер**</span><span class="sxs-lookup"><span data-stu-id="444ba-265">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-266">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="444ba-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-267">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-268">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 9 \| " номер устройства ")</span><span class="sxs-lookup"><span data-stu-id="444ba-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Device Number")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-269">Номер устройства SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="444ba-269">SMBIOS Device Number.</span></span>

<span data-ttu-id="444ba-270">Это значение берется из элемента " **номер устройства/функции** " в структуре **системных слотов** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="444ba-270">This value comes from the **Device/Function Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="444ba-271">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="444ba-271">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="444ba-272">**функтионнумбер**</span><span class="sxs-lookup"><span data-stu-id="444ba-272">**FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-273">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="444ba-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-275">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 9 \| номер функции")</span><span class="sxs-lookup"><span data-stu-id="444ba-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Function Number")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-276">Номер функции SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="444ba-276">SMBIOS Function Number.</span></span>

<span data-ttu-id="444ba-277">Это значение берется из элемента " **номер устройства/функции** " в структуре **системных слотов** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="444ba-277">This value comes from the **Device/Function Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="444ba-278">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="444ba-278">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="444ba-279">**хеигхталловед**</span><span class="sxs-lookup"><span data-stu-id="444ba-279">**HeightAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-280">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="444ba-280">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-282">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="444ba-282">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-283">Максимальная высота платы адаптера, которую можно вставить в гнездо (в дюймах).</span><span class="sxs-lookup"><span data-stu-id="444ba-283">Maximum height of an adapter card that can be inserted into the slot—in inches.</span></span>

<span data-ttu-id="444ba-284">Это свойство наследуется [**от \_ области CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-284">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-285">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="444ba-285">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-286">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="444ba-286">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-287">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-288">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="444ba-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-289">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="444ba-289">Date and time the object is installed.</span></span> <span data-ttu-id="444ba-290">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="444ba-290">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="444ba-291">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-291">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-292">**ленгсалловед**</span><span class="sxs-lookup"><span data-stu-id="444ba-292">**LengthAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-293">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="444ba-293">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-295">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="444ba-295">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-296">Максимальная длина платы адаптера, которую можно вставить в гнездо (в дюймах).</span><span class="sxs-lookup"><span data-stu-id="444ba-296">Maximum length of an adapter card that can be inserted into the slot—in inches.</span></span>

<span data-ttu-id="444ba-297">Это свойство наследуется [**от \_ области CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-297">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-298">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="444ba-298">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-299">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="444ba-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-301">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="444ba-301">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="444ba-302">Имя Организации, которая создает физический элемент.</span><span class="sxs-lookup"><span data-stu-id="444ba-302">Name of the organization that produces the physical element.</span></span>

<span data-ttu-id="444ba-303">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-303">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-304">**максдатавидс**</span><span class="sxs-lookup"><span data-stu-id="444ba-304">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-305">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="444ba-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-307">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("максдатавидс"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIF. \|Системный слот DMTF \| 004,3 "), [**единиц**](../wmisdk/standard-qualifiers.md) (" бит ")</span><span class="sxs-lookup"><span data-stu-id="444ba-307">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("MaxDataWidth"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.3"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-308">Максимальная длина шины адаптеров, которую можно вставить в этот слот, в битах.</span><span class="sxs-lookup"><span data-stu-id="444ba-308">Maximum bus width of adapter cards that can be inserted into this slot—in bits.</span></span> <span data-ttu-id="444ba-309">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="444ba-309">This can be one of the following values.</span></span>

<span data-ttu-id="444ba-310">Это значение берется из элемента **Ширина шины данных** в структуре **системных слотов** в информации SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="444ba-310">This value comes from the **Slot Data Bus Width** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="444ba-311">Это свойство наследуется [**от \_ области CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-311">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="444ba-312">Возможные значения:.</span><span class="sxs-lookup"><span data-stu-id="444ba-312">The possible values are.</span></span>

<dt>

<span id="8"></span>

<span data-ttu-id="444ba-313"><span id="8"></span>**8** (0)</span><span class="sxs-lookup"><span data-stu-id="444ba-313"><span id="8"></span>**8** (0)</span></span>


</dt> <dd>

<span data-ttu-id="444ba-314">Максимальная ширина данных (в битах): 8</span><span class="sxs-lookup"><span data-stu-id="444ba-314">Maximum data width (bits): 8</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="444ba-315"><span id="16"></span>**16** (1)</span><span class="sxs-lookup"><span data-stu-id="444ba-315"><span id="16"></span>**16** (1)</span></span>


</dt> <dd>

<span data-ttu-id="444ba-316">Максимальная ширина данных (в битах): 16</span><span class="sxs-lookup"><span data-stu-id="444ba-316">Maximum data width (bits): 16</span></span>

</dd> <dt>

<span id="32"></span>

<span data-ttu-id="444ba-317"><span id="32"></span>**32** (2)</span><span class="sxs-lookup"><span data-stu-id="444ba-317"><span id="32"></span>**32** (2)</span></span>


</dt> <dd>

<span data-ttu-id="444ba-318">Максимальная ширина данных (в битах): 32</span><span class="sxs-lookup"><span data-stu-id="444ba-318">Maximum data width (bits): 32</span></span>

</dd> <dt>

<span id="64"></span>

<span data-ttu-id="444ba-319"><span id="64"></span>**64** (3)</span><span class="sxs-lookup"><span data-stu-id="444ba-319"><span id="64"></span>**64** (3)</span></span>


</dt> <dd>

<span data-ttu-id="444ba-320">Максимальная ширина данных (в битах): 64</span><span class="sxs-lookup"><span data-stu-id="444ba-320">Maximum data width (bits): 64</span></span>

</dd> <dt>

<span id="128"></span>

<span data-ttu-id="444ba-321"><span id="128"></span>**128** (4)</span><span class="sxs-lookup"><span data-stu-id="444ba-321"><span id="128"></span>**128** (4)</span></span>


</dt> <dd>

<span data-ttu-id="444ba-322">Максимальная ширина данных (в битах): 128</span><span class="sxs-lookup"><span data-stu-id="444ba-322">Maximum data width (bits): 128</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="444ba-323">**Модель**</span><span class="sxs-lookup"><span data-stu-id="444ba-323">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-324">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="444ba-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-326">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="444ba-326">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="444ba-327">Имя физического элемента.</span><span class="sxs-lookup"><span data-stu-id="444ba-327">Name for the physical element.</span></span>

<span data-ttu-id="444ba-328">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-328">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-329">**Name**</span><span class="sxs-lookup"><span data-stu-id="444ba-329">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-330">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="444ba-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-332">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="444ba-332">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-333">Метка для объекта.</span><span class="sxs-lookup"><span data-stu-id="444ba-333">Label for the object.</span></span> <span data-ttu-id="444ba-334">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="444ba-334">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="444ba-335">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-335">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-336">**Число**</span><span class="sxs-lookup"><span data-stu-id="444ba-336">**Number**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-337">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="444ba-337">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="444ba-339">Номер физического слота, который можно использовать в качестве индекса в таблице системных слотов, независимо от того, является ли этот слот физически пустым.</span><span class="sxs-lookup"><span data-stu-id="444ba-339">Physical slot number that can be used as an index into a system slot table, whether or not that slot is physically empty.</span></span>

<span data-ttu-id="444ba-340">Это значение берется из элемента **идентификатора слота** в структуре **системных слотов** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="444ba-340">This value comes from the **Slot ID** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="444ba-341">Это свойство наследуется [**от \_ области CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-341">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-342">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="444ba-342">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-343">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="444ba-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-344">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="444ba-345">Дополнительные данные (то есть больше, чем сведения о тегах актива), которые можно использовать для поиска физического элемента.</span><span class="sxs-lookup"><span data-stu-id="444ba-345">Additional data (that is, more than the asset tag information), that can be used to identify a physical element.</span></span> <span data-ttu-id="444ba-346">Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива.</span><span class="sxs-lookup"><span data-stu-id="444ba-346">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="444ba-347">Обратите внимание, что если доступны только данные штрих-кода и они уникальны или могут использоваться в качестве ключа элемента, это свойство имеет **значение NULL**, а данные штрихкода используются в качестве ключа класса в свойстве **Tag** .</span><span class="sxs-lookup"><span data-stu-id="444ba-347">Note that if only bar code data is available, and it is unique or can be used as an element key, this property is **NULL**, and the bar code data is used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="444ba-348">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-348">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-349">**партнумбер**</span><span class="sxs-lookup"><span data-stu-id="444ba-349">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-350">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="444ba-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-352">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="444ba-352">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="444ba-353">Номер детали, который производитель или производитель назначает физическому элементу.</span><span class="sxs-lookup"><span data-stu-id="444ba-353">Part number that the producer or manufacturer assigns to the physical element.</span></span>

<span data-ttu-id="444ba-354">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-355">**пмесигнал**</span><span class="sxs-lookup"><span data-stu-id="444ba-355">**PMESignal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-356">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="444ba-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-357">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-358">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| \| характеристики гнезда SMBIOS типа 9")</span><span class="sxs-lookup"><span data-stu-id="444ba-358">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Characteristics 2")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-359">Если задано **значение true**, этот слот поддерживает сигнал управления питанием шины PCI (PME).</span><span class="sxs-lookup"><span data-stu-id="444ba-359">If **TRUE**, the PCI bus Power Management Enabled (PME) signal is supported by this slot.</span></span>

<span data-ttu-id="444ba-360">Это значение берется из элемента " **характеристики слота 2** " в структуре **системных слотов** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="444ba-360">This value comes from the **Slot Characteristics 2** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="444ba-361">**повередон**</span><span class="sxs-lookup"><span data-stu-id="444ba-361">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-362">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="444ba-362">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="444ba-364">**Значение true** показывает, что физический элемент включен.</span><span class="sxs-lookup"><span data-stu-id="444ba-364">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="444ba-365">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-365">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-366">**пурпоседескриптион**</span><span class="sxs-lookup"><span data-stu-id="444ba-366">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-367">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="444ba-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-368">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-369">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**\_ область CIM**](cim-slot.md)".**СпеЦиалпурпосе**")</span><span class="sxs-lookup"><span data-stu-id="444ba-369">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Slot**](cim-slot.md).**SpecialPurpose**")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-370">Произвольная строка, описывающая, как этот слот физически уникален и может содержать специальные типы оборудования.</span><span class="sxs-lookup"><span data-stu-id="444ba-370">Free-form string that describes how this slot is physically unique and may hold special types of hardware.</span></span> <span data-ttu-id="444ba-371">Это свойство имеет значение только в том случае, если соответствующее свойство **спеЦиалпурпосе** имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="444ba-371">This property only has meaning when the corresponding property **SpecialPurpose** is **TRUE**.</span></span>

<span data-ttu-id="444ba-372">Это свойство наследуется [**от \_ области CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-372">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-373">**сегментграупнумбер**</span><span class="sxs-lookup"><span data-stu-id="444ba-373">**SegmentGroupNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-374">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="444ba-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-376">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 9 \| номер группы сегментов")</span><span class="sxs-lookup"><span data-stu-id="444ba-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Segment Group Number")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-377">Номер группы сегментов SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="444ba-377">SMBIOS Segment Group Number.</span></span>

<span data-ttu-id="444ba-378">Это значение берется из раздела **номер группы сегментов** в структуре **системных слотов** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="444ba-378">This value comes from the **Segment Group Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="444ba-379">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="444ba-379">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="444ba-380">**Номер**</span><span class="sxs-lookup"><span data-stu-id="444ba-380">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-381">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="444ba-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-383">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="444ba-383">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="444ba-384">Номер, выделенный изготовителем, используемый для распознавания физического элемента.</span><span class="sxs-lookup"><span data-stu-id="444ba-384">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="444ba-385">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-385">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-386">**Общий**</span><span class="sxs-lookup"><span data-stu-id="444ba-386">**Shared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-387">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="444ba-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-389">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| \| характеристики разъема SMBIOS 9" 1 ")</span><span class="sxs-lookup"><span data-stu-id="444ba-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Characteristics 1")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-390">Если **значение — true**, два или более слота совместно используют расположение на основной плате, например общий слот PCI/EISA.</span><span class="sxs-lookup"><span data-stu-id="444ba-390">If **TRUE**, two or more slots share a location on the baseboard, such as a PCI/EISA shared slot.</span></span>

<span data-ttu-id="444ba-391">Это значение берется из **раздела характеристики слота 1** в структуре **системных слотов** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="444ba-391">This value comes from the **Slot Characteristics 1** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="444ba-392">**SKU**</span><span class="sxs-lookup"><span data-stu-id="444ba-392">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-393">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="444ba-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-394">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-395">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="444ba-395">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="444ba-396">Номер единицы хранения для физического элемента.</span><span class="sxs-lookup"><span data-stu-id="444ba-396">Stockkeeping unit number for the physical element.</span></span>

<span data-ttu-id="444ba-397">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-397">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-398">**слотдесигнатион**</span><span class="sxs-lookup"><span data-stu-id="444ba-398">**SlotDesignation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-399">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="444ba-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-400">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-401">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| обозначение типа SMBIOS 9 \| ")</span><span class="sxs-lookup"><span data-stu-id="444ba-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Designation")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-402">Строка SMBIOS, которая определяет обозначение системного слота на материнской плате.</span><span class="sxs-lookup"><span data-stu-id="444ba-402">SMBIOS string that identifies the system slot designation of the slot on the motherboard.</span></span>

<span data-ttu-id="444ba-403">Пример: "PCI-1"</span><span class="sxs-lookup"><span data-stu-id="444ba-403">Example: "PCI-1"</span></span>

<span data-ttu-id="444ba-404">Это значение берется из элемента " **Обозначение слота** " структуры **системных слотов** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="444ba-404">This value comes from the **Slot Designation** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="444ba-405">**спеЦиалпурпосе**</span><span class="sxs-lookup"><span data-stu-id="444ba-405">**SpecialPurpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-406">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="444ba-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-407">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-408">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**\_ область CIM**](cim-slot.md)".**Пурпоседескриптион**")</span><span class="sxs-lookup"><span data-stu-id="444ba-408">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Slot**](cim-slot.md).**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-409">Если **значение равно true**, этот слот физически уникален и может содержать специальные типы оборудования, например разъем для графического процессора.</span><span class="sxs-lookup"><span data-stu-id="444ba-409">If **TRUE**, this slot is physically unique and may hold special types of hardware, such as a graphics processor slot.</span></span> <span data-ttu-id="444ba-410">Если **значение — true**, **пурпоседескриптион** должен указывать природу уникальности или назначения слота.</span><span class="sxs-lookup"><span data-stu-id="444ba-410">If **TRUE**, then **PurposeDescription** should specify the nature of the uniqueness or purpose of the slot.</span></span>

<span data-ttu-id="444ba-411">Это свойство наследуется [**от \_ области CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-411">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-412">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="444ba-412">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-413">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="444ba-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-414">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-415">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="444ba-415">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-416">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="444ba-416">Current status of the object.</span></span> <span data-ttu-id="444ba-417">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="444ba-417">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="444ba-418">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="444ba-418">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="444ba-419">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="444ba-419">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="444ba-420">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="444ba-420">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="444ba-421">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="444ba-421">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="444ba-422">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-422">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="444ba-423">Возможные значения:.</span><span class="sxs-lookup"><span data-stu-id="444ba-423">The possible values are.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="444ba-424">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="444ba-424">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="444ba-425">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="444ba-425">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="444ba-426">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="444ba-426">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="444ba-427">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="444ba-427">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="444ba-428">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="444ba-428">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="444ba-429">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="444ba-429">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="444ba-430">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="444ba-430">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="444ba-431">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="444ba-431">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="444ba-432">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="444ba-432">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="444ba-433">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="444ba-433">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="444ba-434">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="444ba-434">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="444ba-435">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="444ba-435">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="444ba-436">**суппортшотплуг**</span><span class="sxs-lookup"><span data-stu-id="444ba-436">**SupportsHotPlug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-437">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="444ba-437">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-438">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="444ba-439">Если **значение — true**, слот поддерживает горячее подключение адаптеров.</span><span class="sxs-lookup"><span data-stu-id="444ba-439">If **TRUE**, the slot supports hot-plugging of adapter cards.</span></span>

<span data-ttu-id="444ba-440">Это значение берется из элемента " **характеристики слота 2** " в структуре **системных слотов** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="444ba-440">This value comes from the **Slot Characteristics 2** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="444ba-441">Это свойство наследуется [**от \_ области CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-441">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-442">**Тег**</span><span class="sxs-lookup"><span data-stu-id="444ba-442">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-443">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="444ba-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-444">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-445">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**reoverride**](../wmisdk/standard-qualifiers.md) ("тег"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="444ba-445">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-446">Системный слот, представленный экземпляром этого класса.</span><span class="sxs-lookup"><span data-stu-id="444ba-446">System slot represented by an instance of this class.</span></span>

<span data-ttu-id="444ba-447">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-447">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="444ba-448">Пример: "системный слот 1"</span><span class="sxs-lookup"><span data-stu-id="444ba-448">Example: "System Slot 1"</span></span>

</dd> <dt>

<span data-ttu-id="444ba-449">**сермалратинг**</span><span class="sxs-lookup"><span data-stu-id="444ba-449">**ThermalRating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-450">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="444ba-450">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-451">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-452">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Системный слот DMTF \| 004,11 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" МВт ")</span><span class="sxs-lookup"><span data-stu-id="444ba-452">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-453">Максимальное рассеяние температуры слота в МВт.</span><span class="sxs-lookup"><span data-stu-id="444ba-453">Maximum thermal dissipation of the slot in milliwatts.</span></span>

<span data-ttu-id="444ba-454">Это свойство наследуется [**от \_ области CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-454">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-455">**вккмикседволтажесуппорт**</span><span class="sxs-lookup"><span data-stu-id="444ba-455">**VccMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-456">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="444ba-456">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="444ba-457">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-458">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Системный слот DMTF \| 004,9 ")</span><span class="sxs-lookup"><span data-stu-id="444ba-458">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-459">Массив целых чисел с перечислимыми значениями, указывающий Напряжение VCC, поддерживаемое этим слотом.</span><span class="sxs-lookup"><span data-stu-id="444ba-459">Array of enumerated integers indicating the Vcc voltage supported by this slot.</span></span>

<span data-ttu-id="444ba-460">Это значение берется из **раздела характеристики слота 1** в структуре **системных слотов** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="444ba-460">This value comes from the **Slot Characteristics 1** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="444ba-461">Это свойство наследуется [**от \_ области CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-461">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="444ba-462">Возможные значения:.</span><span class="sxs-lookup"><span data-stu-id="444ba-462">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="444ba-463">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="444ba-463">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="444ba-464">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="444ba-464">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="444ba-465">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="444ba-465">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="444ba-466">**5** в (3)</span><span class="sxs-lookup"><span data-stu-id="444ba-466">**5V** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="444ba-467">**Version**</span><span class="sxs-lookup"><span data-stu-id="444ba-467">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-468">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="444ba-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="444ba-469">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-470">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="444ba-470">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="444ba-471">Версия физического элемента.</span><span class="sxs-lookup"><span data-stu-id="444ba-471">Version of the physical element.</span></span>

<span data-ttu-id="444ba-472">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-472">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="444ba-473">**вппмикседволтажесуппорт**</span><span class="sxs-lookup"><span data-stu-id="444ba-473">**VppMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="444ba-474">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="444ba-474">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="444ba-475">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="444ba-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="444ba-476">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Системный слот DMTF \| 004,10 ")</span><span class="sxs-lookup"><span data-stu-id="444ba-476">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.10")</span></span>
</dt> </dl>

<span data-ttu-id="444ba-477">Массив целых чисел с перечислимыми значениями, которые указывают на напряжение VPP, поддерживаемое этим слотом.</span><span class="sxs-lookup"><span data-stu-id="444ba-477">Array of enumerated integers indicating the Vpp voltage supported by this slot.</span></span>

<span data-ttu-id="444ba-478">Это свойство наследуется [**от \_ области CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-478">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="444ba-479">Возможные значения:.</span><span class="sxs-lookup"><span data-stu-id="444ba-479">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="444ba-480">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="444ba-480">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="444ba-481">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="444ba-481">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="444ba-482">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="444ba-482">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="444ba-483">**5** в (3)</span><span class="sxs-lookup"><span data-stu-id="444ba-483">**5V** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

<span data-ttu-id="444ba-484">**12** в (4)</span><span class="sxs-lookup"><span data-stu-id="444ba-484">**12V** (4)</span></span>


<span data-ttu-id="444ba-485"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="444ba-485"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="444ba-486">Комментарии</span><span class="sxs-lookup"><span data-stu-id="444ba-486">Remarks</span></span>

<span data-ttu-id="444ba-487">Класс **Win32 \_ системслот** является производным от [**\_ области CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="444ba-487">The **Win32\_SystemSlot** class is derived from [**CIM\_Slot**](cim-slot.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="444ba-488">Требования</span><span class="sxs-lookup"><span data-stu-id="444ba-488">Requirements</span></span>



| <span data-ttu-id="444ba-489">Требование</span><span class="sxs-lookup"><span data-stu-id="444ba-489">Requirement</span></span> | <span data-ttu-id="444ba-490">Значение</span><span class="sxs-lookup"><span data-stu-id="444ba-490">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="444ba-491">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="444ba-491">Minimum supported client</span></span><br/> | <span data-ttu-id="444ba-492">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="444ba-492">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="444ba-493">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="444ba-493">Minimum supported server</span></span><br/> | <span data-ttu-id="444ba-494">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="444ba-494">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="444ba-495">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="444ba-495">Namespace</span></span><br/>                | <span data-ttu-id="444ba-496">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="444ba-496">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="444ba-497">MOF</span><span class="sxs-lookup"><span data-stu-id="444ba-497">MOF</span></span><br/>                      | <dl> <span data-ttu-id="444ba-498"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="444ba-498"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="444ba-499">DLL</span><span class="sxs-lookup"><span data-stu-id="444ba-499">DLL</span></span><br/>                      | <dl> <span data-ttu-id="444ba-500"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="444ba-500"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="444ba-501">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="444ba-501">See also</span></span>

<dl> <dt>

[<span data-ttu-id="444ba-502">**\_Слот CIM**</span><span class="sxs-lookup"><span data-stu-id="444ba-502">**CIM\_Slot**</span></span>](cim-slot.md)
</dt> <dt>

[<span data-ttu-id="444ba-503">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="444ba-503">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
