---
description: Класс CIM \_ фисикалконнектор представляет любой физический элемент, используемый для подключения к другим элементам. Любой объект, который может подключаться и передавать сигналы или мощь между двумя или более физическими элементами, является потомком (или членом) этого класса.
ms.assetid: cc135ae8-5ae1-4028-a2e3-a81db8694d9d
ms.tgt_platform: multiple
title: Класс CIM_PhysicalConnector
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalConnector
- CIM_PhysicalConnector.Caption
- CIM_PhysicalConnector.Description
- CIM_PhysicalConnector.InstallDate
- CIM_PhysicalConnector.Name
- CIM_PhysicalConnector.Status
- CIM_PhysicalConnector.CreationClassName
- CIM_PhysicalConnector.Manufacturer
- CIM_PhysicalConnector.Model
- CIM_PhysicalConnector.OtherIdentifyingInfo
- CIM_PhysicalConnector.PartNumber
- CIM_PhysicalConnector.PoweredOn
- CIM_PhysicalConnector.SerialNumber
- CIM_PhysicalConnector.SKU
- CIM_PhysicalConnector.Tag
- CIM_PhysicalConnector.Version
- CIM_PhysicalConnector.ConnectorPinout
- CIM_PhysicalConnector.ConnectorType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 106b8ab30296b77be550809771db3b0208485872
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655938"
---
# <a name="cim_physicalconnector-class"></a><span data-ttu-id="7d036-104">\_Класс CIM фисикалконнектор</span><span class="sxs-lookup"><span data-stu-id="7d036-104">CIM\_PhysicalConnector class</span></span>

<span data-ttu-id="7d036-105">Класс **CIM \_ фисикалконнектор** представляет любой физический элемент, используемый для подключения к другим элементам.</span><span class="sxs-lookup"><span data-stu-id="7d036-105">The **CIM\_PhysicalConnector** class represents any physical element that is used to connect to other elements.</span></span> <span data-ttu-id="7d036-106">Любой объект, который может подключаться и передавать сигналы или мощь между двумя или более физическими элементами, является потомком (или членом) этого класса.</span><span class="sxs-lookup"><span data-stu-id="7d036-106">Any object that can connect and transmit signals or power between two or more physical elements is a descendant (or member) of this class.</span></span> <span data-ttu-id="7d036-107">Например, слоты и соединители D-Shell являются типами физических соединителей.</span><span class="sxs-lookup"><span data-stu-id="7d036-107">For example, slots and D-shell connectors are types of physical connectors.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7d036-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="7d036-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7d036-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7d036-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7d036-110">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="7d036-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="7d036-111">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="7d036-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d036-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d036-112">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B84-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalConnector : CIM_PhysicalElement
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
  string   ConnectorPinout;
  uint16   ConnectorType[];
};
```

## <a name="members"></a><span data-ttu-id="7d036-113">Члены</span><span class="sxs-lookup"><span data-stu-id="7d036-113">Members</span></span>

<span data-ttu-id="7d036-114">Класс **CIM \_ фисикалконнектор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7d036-114">The **CIM\_PhysicalConnector** class has these types of members:</span></span>

-   [<span data-ttu-id="7d036-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="7d036-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d036-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="7d036-116">Properties</span></span>

<span data-ttu-id="7d036-117">Класс **CIM \_ фисикалконнектор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7d036-117">The **CIM\_PhysicalConnector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7d036-118">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="7d036-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d036-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d036-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d036-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d036-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d036-121">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7d036-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7d036-122">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="7d036-122">A short textual description of the object.</span></span>

<span data-ttu-id="7d036-123">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d036-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d036-124">**коннекторпинаут**</span><span class="sxs-lookup"><span data-stu-id="7d036-124">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d036-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d036-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d036-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d036-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d036-127">Произвольная строка, описывающая конфигурацию ПИН-кода и использование сигнала физическим соединителем.</span><span class="sxs-lookup"><span data-stu-id="7d036-127">Free-form string that describes the pin configuration and signal use of a physical connector.</span></span>

</dd> <dt>

<span data-ttu-id="7d036-128">**коннектортипе**</span><span class="sxs-lookup"><span data-stu-id="7d036-128">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d036-129">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="7d036-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7d036-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d036-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d036-131">Тип физического соединителя.</span><span class="sxs-lookup"><span data-stu-id="7d036-131">Type of physical connector.</span></span> <span data-ttu-id="7d036-132">Массив задается, чтобы разрешить Описание сочетаний сведений о соединителях.</span><span class="sxs-lookup"><span data-stu-id="7d036-132">An array is specified to allow the description of combinations of connector information.</span></span> <span data-ttu-id="7d036-133">Например, одна запись массива может указывать RS-232, другой DB-25, а третья запись может определять соединитель как "папа".</span><span class="sxs-lookup"><span data-stu-id="7d036-133">For example, one array entry could specify RS-232, another DB-25, and a third entry could define the connector as "male".</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7d036-134">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="7d036-134">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7d036-135">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="7d036-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span data-ttu-id="7d036-136">**Штекер** (2)</span><span class="sxs-lookup"><span data-stu-id="7d036-136">**Male** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span data-ttu-id="7d036-137">**Женщина** (3)</span><span class="sxs-lookup"><span data-stu-id="7d036-137">**Female** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="7d036-138">**Экранированный** (4)</span><span class="sxs-lookup"><span data-stu-id="7d036-138">**Shielded** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span data-ttu-id="7d036-139">**Неэкранированный** (5)</span><span class="sxs-lookup"><span data-stu-id="7d036-139">**Unshielded** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span data-ttu-id="7d036-140">**SCSI (A) High-Density (50 ПИН-коды)** (6)</span><span class="sxs-lookup"><span data-stu-id="7d036-140">**SCSI (A) High-Density (50 pins)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span data-ttu-id="7d036-141">**SCSI (A) Low-Density (50 ПИН-коды)** (7)</span><span class="sxs-lookup"><span data-stu-id="7d036-141">**SCSI (A) Low-Density (50 pins)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span data-ttu-id="7d036-142">**High-Density SCSI (P) (68 ПИН-коды)** (8)</span><span class="sxs-lookup"><span data-stu-id="7d036-142">**SCSI (P) High-Density (68 pins)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span data-ttu-id="7d036-143">**SCSI SCA-I (80 ПИН)** (9)</span><span class="sxs-lookup"><span data-stu-id="7d036-143">**SCSI SCA-I (80 pins)** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span data-ttu-id="7d036-144">**SCSI SCA-II (80 контактов)** (10)</span><span class="sxs-lookup"><span data-stu-id="7d036-144">**SCSI SCA-II (80 pins)** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span data-ttu-id="7d036-145">**Fibre Channel SCSI (DB-9, медный)** (11)</span><span class="sxs-lookup"><span data-stu-id="7d036-145">**SCSI Fibre Channel (DB-9, Copper)** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span data-ttu-id="7d036-146">**Fibre Channel SCSI (Fibre)** (12)</span><span class="sxs-lookup"><span data-stu-id="7d036-146">**SCSI Fibre Channel (Fibre)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span data-ttu-id="7d036-147">**SCSI Fibre Channel SCA-II (40 ПИН)** (13)</span><span class="sxs-lookup"><span data-stu-id="7d036-147">**SCSI Fibre Channel SCA-II (40 pins)** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span data-ttu-id="7d036-148">**SCSI Fibre Channel SCA-II (20 контактов)** (14)</span><span class="sxs-lookup"><span data-stu-id="7d036-148">**SCSI Fibre Channel SCA-II (20 pins)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span data-ttu-id="7d036-149">**SCSI Fibre Channel БНК** (15)</span><span class="sxs-lookup"><span data-stu-id="7d036-149">**SCSI Fibre Channel BNC** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span data-ttu-id="7d036-150">**ATA 3-1/2 дюйма (40 контактов)** (16)</span><span class="sxs-lookup"><span data-stu-id="7d036-150">**ATA 3-1/2 Inch (40 pins)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span data-ttu-id="7d036-151">**ATA 2-1/2 дюйма (44 контактов)** (17)</span><span class="sxs-lookup"><span data-stu-id="7d036-151">**ATA 2-1/2 Inch (44 pins)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span data-ttu-id="7d036-152">**ATA-2** (18)</span><span class="sxs-lookup"><span data-stu-id="7d036-152">**ATA-2** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span data-ttu-id="7d036-153">**ATA-3** (19)</span><span class="sxs-lookup"><span data-stu-id="7d036-153">**ATA-3** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span data-ttu-id="7d036-154">**ATA/66** (20)</span><span class="sxs-lookup"><span data-stu-id="7d036-154">**ATA/66** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span data-ttu-id="7d036-155">**DB-9** (21)</span><span class="sxs-lookup"><span data-stu-id="7d036-155">**DB-9** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span data-ttu-id="7d036-156">**DB-15** (22)</span><span class="sxs-lookup"><span data-stu-id="7d036-156">**DB-15** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span data-ttu-id="7d036-157">**DB-25** (23)</span><span class="sxs-lookup"><span data-stu-id="7d036-157">**DB-25** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span data-ttu-id="7d036-158">**DB-36** (24)</span><span class="sxs-lookup"><span data-stu-id="7d036-158">**DB-36** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span data-ttu-id="7d036-159">**RS-232c** (25)</span><span class="sxs-lookup"><span data-stu-id="7d036-159">**RS-232C** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span data-ttu-id="7d036-160">**RS-422** (26)</span><span class="sxs-lookup"><span data-stu-id="7d036-160">**RS-422** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span data-ttu-id="7d036-161">**RS-423** (27)</span><span class="sxs-lookup"><span data-stu-id="7d036-161">**RS-423** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span data-ttu-id="7d036-162">**RS-485** (28)</span><span class="sxs-lookup"><span data-stu-id="7d036-162">**RS-485** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span data-ttu-id="7d036-163">**RS-449** (29)</span><span class="sxs-lookup"><span data-stu-id="7d036-163">**RS-449** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="7d036-164">**V. 35** (30)</span><span class="sxs-lookup"><span data-stu-id="7d036-164">**V.35** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span data-ttu-id="7d036-165">**X. 21** (31)</span><span class="sxs-lookup"><span data-stu-id="7d036-165">**X.21** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="7d036-166">**IEEE-488** (32)</span><span class="sxs-lookup"><span data-stu-id="7d036-166">**IEEE-488** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span data-ttu-id="7d036-167">**АУИ** (33)</span><span class="sxs-lookup"><span data-stu-id="7d036-167">**AUI** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span data-ttu-id="7d036-168">**UTP Категория 3** (34)</span><span class="sxs-lookup"><span data-stu-id="7d036-168">**UTP Category 3** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span data-ttu-id="7d036-169">**UTP Категория 4** (35)</span><span class="sxs-lookup"><span data-stu-id="7d036-169">**UTP Category 4** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span data-ttu-id="7d036-170">**UTP Category 5** (36)</span><span class="sxs-lookup"><span data-stu-id="7d036-170">**UTP Category 5** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span data-ttu-id="7d036-171">**БНК** (37)</span><span class="sxs-lookup"><span data-stu-id="7d036-171">**BNC** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span data-ttu-id="7d036-172">**RJ11** (38)</span><span class="sxs-lookup"><span data-stu-id="7d036-172">**RJ11** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span data-ttu-id="7d036-173">**RJ45** (39)</span><span class="sxs-lookup"><span data-stu-id="7d036-173">**RJ45** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span data-ttu-id="7d036-174">**Оптоволоконный микрофон** (40)</span><span class="sxs-lookup"><span data-stu-id="7d036-174">**Fiber MIC** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span data-ttu-id="7d036-175">**Apple АУИ** (41)</span><span class="sxs-lookup"><span data-stu-id="7d036-175">**Apple AUI** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span data-ttu-id="7d036-176">**Геопорт Apple** (42)</span><span class="sxs-lookup"><span data-stu-id="7d036-176">**Apple GeoPort** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="7d036-177">**PCI** (43)</span><span class="sxs-lookup"><span data-stu-id="7d036-177">**PCI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="7d036-178">**ISA** (44)</span><span class="sxs-lookup"><span data-stu-id="7d036-178">**ISA** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="7d036-179">**EISA** (45)</span><span class="sxs-lookup"><span data-stu-id="7d036-179">**EISA** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="7d036-180">**VESA** (46)</span><span class="sxs-lookup"><span data-stu-id="7d036-180">**VESA** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="7d036-181">**PCMCIA** (47)</span><span class="sxs-lookup"><span data-stu-id="7d036-181">**PCMCIA** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span data-ttu-id="7d036-182">**Тип PCMCIA I** (48)</span><span class="sxs-lookup"><span data-stu-id="7d036-182">**PCMCIA Type I** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="7d036-183">**PCMCIA типа II** (49)</span><span class="sxs-lookup"><span data-stu-id="7d036-183">**PCMCIA Type II** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="7d036-184">**PCMCIA типа III** (50)</span><span class="sxs-lookup"><span data-stu-id="7d036-184">**PCMCIA Type III** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span data-ttu-id="7d036-185">**Порт зв** (51)</span><span class="sxs-lookup"><span data-stu-id="7d036-185">**ZV Port** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="7d036-186">**CardBus** (52)</span><span class="sxs-lookup"><span data-stu-id="7d036-186">**CardBus** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="7d036-187">**USB** (53)</span><span class="sxs-lookup"><span data-stu-id="7d036-187">**USB** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="7d036-188">**IEEE 1394** (54)</span><span class="sxs-lookup"><span data-stu-id="7d036-188">**IEEE 1394** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="7d036-189">**Хиппи** (55)</span><span class="sxs-lookup"><span data-stu-id="7d036-189">**HIPPI** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span data-ttu-id="7d036-190">**Хссдк (6 контактов)** (56)</span><span class="sxs-lookup"><span data-stu-id="7d036-190">**HSSDC (6 pins)** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span data-ttu-id="7d036-191">**Гбик** (57)</span><span class="sxs-lookup"><span data-stu-id="7d036-191">**GBIC** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span data-ttu-id="7d036-192">**DIN** (58)</span><span class="sxs-lookup"><span data-stu-id="7d036-192">**DIN** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span data-ttu-id="7d036-193">**Мини-DIN** (59)</span><span class="sxs-lookup"><span data-stu-id="7d036-193">**Mini-DIN** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span data-ttu-id="7d036-194">**Micro-DIN** (60)</span><span class="sxs-lookup"><span data-stu-id="7d036-194">**Micro-DIN** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="7d036-195">**PS/2** (61)</span><span class="sxs-lookup"><span data-stu-id="7d036-195">**PS/2** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="7d036-196">**Инфракрасная связь** (62)</span><span class="sxs-lookup"><span data-stu-id="7d036-196">**Infrared** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="7d036-197">**HP-Хил** (63)</span><span class="sxs-lookup"><span data-stu-id="7d036-197">**HP-HIL** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span data-ttu-id="7d036-198">**Доступ. Bus** (64)</span><span class="sxs-lookup"><span data-stu-id="7d036-198">**Access.bus** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="7d036-199">**Нубус** (65)</span><span class="sxs-lookup"><span data-stu-id="7d036-199">**NuBus** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span data-ttu-id="7d036-200">**Центроникс** (66)</span><span class="sxs-lookup"><span data-stu-id="7d036-200">**Centronics** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span data-ttu-id="7d036-201">**Мини-центроникс** (67)</span><span class="sxs-lookup"><span data-stu-id="7d036-201">**Mini-Centronics** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span data-ttu-id="7d036-202">**Тип мини-центроникс — 14** (68)</span><span class="sxs-lookup"><span data-stu-id="7d036-202">**Mini-Centronics Type-14** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span data-ttu-id="7d036-203">**Mini-Центроникс Type-20** (69)</span><span class="sxs-lookup"><span data-stu-id="7d036-203">**Mini-Centronics Type-20** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span data-ttu-id="7d036-204">**Mini-Центроникс Type-26** (70)</span><span class="sxs-lookup"><span data-stu-id="7d036-204">**Mini-Centronics Type-26** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="7d036-205">**Мышь шины** (71)</span><span class="sxs-lookup"><span data-stu-id="7d036-205">**Bus Mouse** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span data-ttu-id="7d036-206">**ADB** (72)</span><span class="sxs-lookup"><span data-stu-id="7d036-206">**ADB** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="7d036-207">**AGP** (73)</span><span class="sxs-lookup"><span data-stu-id="7d036-207">**AGP** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="7d036-208">**Шина вме** (74)</span><span class="sxs-lookup"><span data-stu-id="7d036-208">**VME Bus** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span data-ttu-id="7d036-209">**VME64** (75)</span><span class="sxs-lookup"><span data-stu-id="7d036-209">**VME64** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="7d036-210">**Частный** (76)</span><span class="sxs-lookup"><span data-stu-id="7d036-210">**Proprietary** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span data-ttu-id="7d036-211">**Собственный слот карты процессора** (77)</span><span class="sxs-lookup"><span data-stu-id="7d036-211">**Proprietary Processor Card Slot** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span data-ttu-id="7d036-212">**Собственный слот карты памяти** (78)</span><span class="sxs-lookup"><span data-stu-id="7d036-212">**Proprietary Memory Card Slot** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span data-ttu-id="7d036-213">**Собственная Подплата ввода/вывода** (79)</span><span class="sxs-lookup"><span data-stu-id="7d036-213">**Proprietary I/O Riser Slot** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span data-ttu-id="7d036-214">**PCI-66** (80)</span><span class="sxs-lookup"><span data-stu-id="7d036-214">**PCI-66MHZ** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span data-ttu-id="7d036-215">**AGP2X** (81)</span><span class="sxs-lookup"><span data-stu-id="7d036-215">**AGP2X** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span data-ttu-id="7d036-216">**AGP4X** (82)</span><span class="sxs-lookup"><span data-stu-id="7d036-216">**AGP4X** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="7d036-217">**PC-98** (83)</span><span class="sxs-lookup"><span data-stu-id="7d036-217">**PC-98** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="7d036-218">**PC-98-хиресо** (84)</span><span class="sxs-lookup"><span data-stu-id="7d036-218">**PC-98-Hireso** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="7d036-219">**PC-H98** (85)</span><span class="sxs-lookup"><span data-stu-id="7d036-219">**PC-H98** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span data-ttu-id="7d036-220">**PC-98Note** (86)</span><span class="sxs-lookup"><span data-stu-id="7d036-220">**PC-98Note** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span data-ttu-id="7d036-221">**PC-98Full** (87)</span><span class="sxs-lookup"><span data-stu-id="7d036-221">**PC-98Full** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="SSA_SCSI"></span><span id="ssa_scsi"></span>

<span data-ttu-id="7d036-222">**Адаптер SSA SCSI** (88)</span><span class="sxs-lookup"><span data-stu-id="7d036-222">**SSA SCSI** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Circular"></span><span id="circular"></span><span id="CIRCULAR"></span>

<span data-ttu-id="7d036-223">**Циклический** (89)</span><span class="sxs-lookup"><span data-stu-id="7d036-223">**Circular** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="On_Board_IDE_Connector"></span><span id="on_board_ide_connector"></span><span id="ON_BOARD_IDE_CONNECTOR"></span>

<span data-ttu-id="7d036-224">**Встроенный соединитель IDE** (90)</span><span class="sxs-lookup"><span data-stu-id="7d036-224">**On Board IDE Connector** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="On_Board_Floppy_Connector"></span><span id="on_board_floppy_connector"></span><span id="ON_BOARD_FLOPPY_CONNECTOR"></span>

<span data-ttu-id="7d036-225">**Разъем флоппи-дисковода** (91)</span><span class="sxs-lookup"><span data-stu-id="7d036-225">**On Board Floppy Connector** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="9_Pin_Dual_Inline"></span><span id="9_pin_dual_inline"></span><span id="9_PIN_DUAL_INLINE"></span>

<span data-ttu-id="7d036-226">**9-штырьковый двухрядный** (92)</span><span class="sxs-lookup"><span data-stu-id="7d036-226">**9 Pin Dual Inline** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="25_Pin_Dual_Inline"></span><span id="25_pin_dual_inline"></span><span id="25_PIN_DUAL_INLINE"></span>

<span data-ttu-id="7d036-227">**25-контактный двойной текст** (93)</span><span class="sxs-lookup"><span data-stu-id="7d036-227">**25 Pin Dual Inline** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>

<span data-ttu-id="7d036-228">**50. закрепление двух встраиваемых систем** (94)</span><span class="sxs-lookup"><span data-stu-id="7d036-228">**50 Pin Dual Inline** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="68_Pin_Dual_Inline"></span><span id="68_pin_dual_inline"></span><span id="68_PIN_DUAL_INLINE"></span>

<span data-ttu-id="7d036-229">**68. закрепление двух встраиваемых систем** (95)</span><span class="sxs-lookup"><span data-stu-id="7d036-229">**68 Pin Dual Inline** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="On_Board_Sound_Connector"></span><span id="on_board_sound_connector"></span><span id="ON_BOARD_SOUND_CONNECTOR"></span>

<span data-ttu-id="7d036-230">**Звуковой разъем на доске** (96)</span><span class="sxs-lookup"><span data-stu-id="7d036-230">**On Board Sound Connector** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>

<span data-ttu-id="7d036-231">**Мини-гнездо** (97)</span><span class="sxs-lookup"><span data-stu-id="7d036-231">**Mini-jack** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-X"></span><span id="pci-x"></span>

<span data-ttu-id="7d036-232">**PCI-X** (98)</span><span class="sxs-lookup"><span data-stu-id="7d036-232">**PCI-X** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_32_bit"></span><span id="sbus_ieee_1396-1993_32_bit"></span><span id="SBUS_IEEE_1396-1993_32_BIT"></span>

<span data-ttu-id="7d036-233">**СБУС IEEE 1396-1993 32, бит** (99)</span><span class="sxs-lookup"><span data-stu-id="7d036-233">**Sbus IEEE 1396-1993 32 bit** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_64_bit"></span><span id="sbus_ieee_1396-1993_64_bit"></span><span id="SBUS_IEEE_1396-1993_64_BIT"></span>

<span data-ttu-id="7d036-234">**СБУС IEEE 1396-1993 64, бит** (100)</span><span class="sxs-lookup"><span data-stu-id="7d036-234">**Sbus IEEE 1396-1993 64 bit** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="7d036-235">**MCA** (101)</span><span class="sxs-lookup"><span data-stu-id="7d036-235">**MCA** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="GIO"></span><span id="gio"></span>

<span data-ttu-id="7d036-236">**ГИО** (102)</span><span class="sxs-lookup"><span data-stu-id="7d036-236">**GIO** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="XIO"></span><span id="xio"></span>

<span data-ttu-id="7d036-237">**XIO** (103)</span><span class="sxs-lookup"><span data-stu-id="7d036-237">**XIO** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="HIO"></span><span id="hio"></span>

<span data-ttu-id="7d036-238">**Хио** (104)</span><span class="sxs-lookup"><span data-stu-id="7d036-238">**HIO** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="NGIO"></span><span id="ngio"></span>

<span data-ttu-id="7d036-239">**Нгио** (105)</span><span class="sxs-lookup"><span data-stu-id="7d036-239">**NGIO** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="PMC"></span><span id="pmc"></span>

<span data-ttu-id="7d036-240">**PMC** (106)</span><span class="sxs-lookup"><span data-stu-id="7d036-240">**PMC** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="MTRJ"></span><span id="mtrj"></span>

<span data-ttu-id="7d036-241">**Мтрж** (107)</span><span class="sxs-lookup"><span data-stu-id="7d036-241">**MTRJ** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="VF-45"></span><span id="vf-45"></span>

<span data-ttu-id="7d036-242">**VF-45** (108)</span><span class="sxs-lookup"><span data-stu-id="7d036-242">**VF-45** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Future_I_O"></span><span id="future_i_o"></span><span id="FUTURE_I_O"></span>

<span data-ttu-id="7d036-243">**Будущие операции ввода-вывода** (109)</span><span class="sxs-lookup"><span data-stu-id="7d036-243">**Future I/O** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="SC"></span><span id="sc"></span>

<span data-ttu-id="7d036-244">**SC** (110)</span><span class="sxs-lookup"><span data-stu-id="7d036-244">**SC** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="SG"></span><span id="sg"></span>

<span data-ttu-id="7d036-245">**SG** (111)</span><span class="sxs-lookup"><span data-stu-id="7d036-245">**SG** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrical"></span><span id="electrical"></span><span id="ELECTRICAL"></span>

<span data-ttu-id="7d036-246">**Электрический** (112)</span><span class="sxs-lookup"><span data-stu-id="7d036-246">**Electrical** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical"></span><span id="optical"></span><span id="OPTICAL"></span>

<span data-ttu-id="7d036-247">**Оптический** (113)</span><span class="sxs-lookup"><span data-stu-id="7d036-247">**Optical** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Ribbon"></span><span id="ribbon"></span><span id="RIBBON"></span>

<span data-ttu-id="7d036-248">**Лента** (114)</span><span class="sxs-lookup"><span data-stu-id="7d036-248">**Ribbon** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="GLM"></span><span id="glm"></span>

<span data-ttu-id="7d036-249">**GLM** (115)</span><span class="sxs-lookup"><span data-stu-id="7d036-249">**GLM** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="1x9"></span><span id="1X9"></span>

<span data-ttu-id="7d036-250">**1x9** (116)</span><span class="sxs-lookup"><span data-stu-id="7d036-250">**1x9** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini_SG"></span><span id="mini_sg"></span><span id="MINI_SG"></span>

<span data-ttu-id="7d036-251">**Мини-SG** (117)</span><span class="sxs-lookup"><span data-stu-id="7d036-251">**Mini SG** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="LC"></span><span id="lc"></span>

<span data-ttu-id="7d036-252">**LC** (118)</span><span class="sxs-lookup"><span data-stu-id="7d036-252">**LC** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSC"></span><span id="hssc"></span>

<span data-ttu-id="7d036-253">**Хсск** (119)</span><span class="sxs-lookup"><span data-stu-id="7d036-253">**HSSC** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="VHDCI_Shielded__68_pins_"></span><span id="vhdci_shielded__68_pins_"></span><span id="VHDCI_SHIELDED__68_PINS_"></span>

<span data-ttu-id="7d036-254">**ВхдЦи экранированный (68 ПИН-кода)** (120)</span><span class="sxs-lookup"><span data-stu-id="7d036-254">**VHDCI Shielded (68 pins)** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="InfiniBand"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

<span data-ttu-id="7d036-255">**InfiniBand** (121)</span><span class="sxs-lookup"><span data-stu-id="7d036-255">**InfiniBand** (121)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7d036-256">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7d036-256">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d036-257">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d036-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d036-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d036-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d036-259">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7d036-259">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7d036-260">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7d036-260">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7d036-261">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="7d036-261">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="7d036-262">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d036-262">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d036-263">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7d036-263">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d036-264">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d036-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d036-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d036-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d036-266">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="7d036-266">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7d036-267">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="7d036-267">A textual description of the object.</span></span>

<span data-ttu-id="7d036-268">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d036-268">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d036-269">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7d036-269">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d036-270">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7d036-270">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7d036-271">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d036-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d036-272">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="7d036-272">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7d036-273">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="7d036-273">Indicates when the object was installed.</span></span> <span data-ttu-id="7d036-274">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="7d036-274">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7d036-275">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d036-275">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d036-276">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="7d036-276">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d036-277">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d036-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d036-278">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d036-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d036-279">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7d036-279">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7d036-280">Имя Организации, ответственной за создание физического элемента.</span><span class="sxs-lookup"><span data-stu-id="7d036-280">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="7d036-281">Дополнительные сведения см. в описании свойства **Vendor** [**\_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="7d036-281">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="7d036-282">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d036-282">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d036-283">**Модель**</span><span class="sxs-lookup"><span data-stu-id="7d036-283">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d036-284">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d036-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d036-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d036-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d036-286">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7d036-286">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7d036-287">Имя, по которому обычно известен физический элемент.</span><span class="sxs-lookup"><span data-stu-id="7d036-287">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="7d036-288">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d036-288">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d036-289">**Name**</span><span class="sxs-lookup"><span data-stu-id="7d036-289">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d036-290">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d036-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d036-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d036-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d036-292">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="7d036-292">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7d036-293">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="7d036-293">Label by which the object is known.</span></span> <span data-ttu-id="7d036-294">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="7d036-294">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="7d036-295">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d036-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d036-296">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="7d036-296">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d036-297">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d036-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d036-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d036-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d036-299">Дополнительные данные, помимо сведений о тегах актива, которые можно использовать для поиска физического элемента.</span><span class="sxs-lookup"><span data-stu-id="7d036-299">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="7d036-300">Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива.</span><span class="sxs-lookup"><span data-stu-id="7d036-300">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="7d036-301">Обратите внимание, что если доступны только данные с штрих-кодом и они уникальны и могут использоваться в качестве ключа элемента, это свойство будет иметь значение null, а данные штрих-кода будут использоваться в качестве ключа класса в свойстве **Tag** .</span><span class="sxs-lookup"><span data-stu-id="7d036-301">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="7d036-302">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d036-302">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d036-303">**партнумбер**</span><span class="sxs-lookup"><span data-stu-id="7d036-303">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d036-304">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d036-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d036-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d036-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d036-306">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7d036-306">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7d036-307">Номер детали, назначенный Организацией, ответственной за производство или производство физического элемента.</span><span class="sxs-lookup"><span data-stu-id="7d036-307">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="7d036-308">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d036-308">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d036-309">**повередон**</span><span class="sxs-lookup"><span data-stu-id="7d036-309">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d036-310">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7d036-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7d036-311">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d036-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d036-312">**Значение true** показывает, что физический элемент включен.</span><span class="sxs-lookup"><span data-stu-id="7d036-312">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="7d036-313">В противном случае в данный момент он отключен.</span><span class="sxs-lookup"><span data-stu-id="7d036-313">Otherwise, it is currently off.</span></span>

<span data-ttu-id="7d036-314">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d036-314">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d036-315">**Номер**</span><span class="sxs-lookup"><span data-stu-id="7d036-315">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d036-316">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d036-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d036-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d036-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d036-318">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7d036-318">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7d036-319">Номер, выделенный изготовителем, используемый для распознавания физического элемента.</span><span class="sxs-lookup"><span data-stu-id="7d036-319">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="7d036-320">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d036-320">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d036-321">**SKU**</span><span class="sxs-lookup"><span data-stu-id="7d036-321">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d036-322">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d036-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d036-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d036-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d036-324">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7d036-324">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7d036-325">Номер единицы складского учета для этого физического элемента.</span><span class="sxs-lookup"><span data-stu-id="7d036-325">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="7d036-326">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d036-326">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d036-327">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="7d036-327">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d036-328">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d036-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d036-329">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d036-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d036-330">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="7d036-330">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7d036-331">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="7d036-331">String that indicates the current status of the object.</span></span> <span data-ttu-id="7d036-332">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="7d036-332">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="7d036-333">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="7d036-333">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="7d036-334">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="7d036-334">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="7d036-335">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="7d036-335">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7d036-336">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="7d036-336">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7d036-337">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="7d036-337">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7d036-338">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d036-338">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7d036-339">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="7d036-339">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7d036-340">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="7d036-340">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7d036-341">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="7d036-341">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7d036-342">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="7d036-342">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7d036-343">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="7d036-343">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7d036-344">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="7d036-344">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7d036-345">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="7d036-345">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7d036-346">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="7d036-346">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7d036-347">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="7d036-347">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7d036-348">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="7d036-348">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7d036-349">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="7d036-349">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7d036-350">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="7d036-350">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7d036-351">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="7d036-351">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7d036-352">**Тег**</span><span class="sxs-lookup"><span data-stu-id="7d036-352">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d036-353">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d036-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d036-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d036-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d036-355">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7d036-355">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7d036-356">Однозначно идентифицирует физический элемент и служит ключом элемента.</span><span class="sxs-lookup"><span data-stu-id="7d036-356">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="7d036-357">Это свойство может содержать такие сведения, как тег актива или данные серийного номера.</span><span class="sxs-lookup"><span data-stu-id="7d036-357">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="7d036-358">Ключ для [**CIM \_ фисикалелемент**](cim-physicalelement.md) помещается очень высоким в иерархии объектов для независимого обнаружения оборудования или сущности, независимо от физического размещения в (или в) шкафов, адаптеров и т. д.</span><span class="sxs-lookup"><span data-stu-id="7d036-358">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="7d036-359">Например, съемный компонент, который можно использовать для горячей замены, может быть взят из содержащего его пакета (с областями видимости) и временно не используется.</span><span class="sxs-lookup"><span data-stu-id="7d036-359">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="7d036-360">Объект по-прежнему продолжает существовать и даже может быть вставлен в другой контейнер области.</span><span class="sxs-lookup"><span data-stu-id="7d036-360">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="7d036-361">Ключом для физического элемента является произвольная строка, которая определяется независимо от размещения или расположения, ориентированного на расположение.</span><span class="sxs-lookup"><span data-stu-id="7d036-361">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="7d036-362">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d036-362">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d036-363">**Version**</span><span class="sxs-lookup"><span data-stu-id="7d036-363">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d036-364">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d036-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d036-365">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d036-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d036-366">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7d036-366">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7d036-367">Указывает версию физического элемента.</span><span class="sxs-lookup"><span data-stu-id="7d036-367">Indicates the version of the physical element.</span></span>

<span data-ttu-id="7d036-368">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d036-368">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d036-369">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d036-369">Remarks</span></span>

<span data-ttu-id="7d036-370">Класс **CIM \_ фисикалконнектор** является производным от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d036-370">The **CIM\_PhysicalConnector** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="7d036-371">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="7d036-371">WMI does not implement this class.</span></span> <span data-ttu-id="7d036-372">Сведения о классах WMI, которые являются производными от **CIM \_ фисикалконнектор**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7d036-372">For WMI classes that are derived from **CIM\_PhysicalConnector**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="7d036-373">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="7d036-373">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7d036-374">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="7d036-374">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d036-375">Требования</span><span class="sxs-lookup"><span data-stu-id="7d036-375">Requirements</span></span>



| <span data-ttu-id="7d036-376">Требование</span><span class="sxs-lookup"><span data-stu-id="7d036-376">Requirement</span></span> | <span data-ttu-id="7d036-377">Значение</span><span class="sxs-lookup"><span data-stu-id="7d036-377">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d036-378">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d036-378">Minimum supported client</span></span><br/> | <span data-ttu-id="7d036-379">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d036-379">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7d036-380">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d036-380">Minimum supported server</span></span><br/> | <span data-ttu-id="7d036-381">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d036-381">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7d036-382">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7d036-382">Namespace</span></span><br/>                | <span data-ttu-id="7d036-383">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7d036-383">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7d036-384">MOF</span><span class="sxs-lookup"><span data-stu-id="7d036-384">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d036-385"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d036-385"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d036-386">DLL</span><span class="sxs-lookup"><span data-stu-id="7d036-386">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d036-387"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d036-387"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d036-388">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d036-388">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d036-389">**\_ФИСИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="7d036-389">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

