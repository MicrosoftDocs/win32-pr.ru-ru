---
description: '\_Класс WMI портконнектор для Win32 представляет порты физического подключения, такие как DB-25-штырьковый, центроникс или PS/2.'
ms.assetid: 85788d1d-0641-4dba-b4ae-a84eb6c4992a
ms.tgt_platform: multiple
title: Класс Win32_PortConnector
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortConnector
- Win32_PortConnector.Caption
- Win32_PortConnector.ConnectorPinout
- Win32_PortConnector.ConnectorType
- Win32_PortConnector.CreationClassName
- Win32_PortConnector.Description
- Win32_PortConnector.ExternalReferenceDesignator
- Win32_PortConnector.InstallDate
- Win32_PortConnector.InternalReferenceDesignator
- Win32_PortConnector.Manufacturer
- Win32_PortConnector.Model
- Win32_PortConnector.Name
- Win32_PortConnector.OtherIdentifyingInfo
- Win32_PortConnector.PartNumber
- Win32_PortConnector.PortType
- Win32_PortConnector.PoweredOn
- Win32_PortConnector.SerialNumber
- Win32_PortConnector.SKU
- Win32_PortConnector.Status
- Win32_PortConnector.Tag
- Win32_PortConnector.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dcf9eea51d3a65ad07879cca3e47ae79bde92d53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262528"
---
# <a name="win32_portconnector-class"></a><span data-ttu-id="19dfc-103">\_Класс Win32 портконнектор</span><span class="sxs-lookup"><span data-stu-id="19dfc-103">Win32\_PortConnector class</span></span>

<span data-ttu-id="19dfc-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ портконнектор для Win32** представляет порты физического подключения, такие как DB-25-штырьковый, центроникс или PS/2.</span><span class="sxs-lookup"><span data-stu-id="19dfc-104">The **Win32\_PortConnector** [WMI class](../wmisdk/retrieving-a-class.md) represents physical connection ports, such as DB-25 pin male, Centronics, or PS/2.</span></span>

<span data-ttu-id="19dfc-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="19dfc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="19dfc-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="19dfc-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="19dfc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19dfc-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B92-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PortConnector : CIM_PhysicalConnector
{
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  string   Description;
  string   ExternalReferenceDesignator;
  datetime InstallDate;
  string   InternalReferenceDesignator;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint16   PortType;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="19dfc-108">Члены</span><span class="sxs-lookup"><span data-stu-id="19dfc-108">Members</span></span>

<span data-ttu-id="19dfc-109">Класс **Win32 \_ портконнектор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="19dfc-109">The **Win32\_PortConnector** class has these types of members:</span></span>

-   [<span data-ttu-id="19dfc-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="19dfc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19dfc-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="19dfc-111">Properties</span></span>

<span data-ttu-id="19dfc-112">Класс **Win32 \_ портконнектор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="19dfc-112">The **Win32\_PortConnector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19dfc-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="19dfc-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19dfc-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19dfc-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19dfc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-116">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="19dfc-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="19dfc-117">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="19dfc-117">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="19dfc-118">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="19dfc-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-119">**коннекторпинаут**</span><span class="sxs-lookup"><span data-stu-id="19dfc-119">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19dfc-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19dfc-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19dfc-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19dfc-122">Закрепите конфигурацию и использование сигнала физического соединителя.</span><span class="sxs-lookup"><span data-stu-id="19dfc-122">Pin configuration and signal usage of a physical connector.</span></span>

<span data-ttu-id="19dfc-123">Это свойство наследуется от [**CIM \_ фисикалконнектор**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="19dfc-123">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-124">**коннектортипе**</span><span class="sxs-lookup"><span data-stu-id="19dfc-124">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19dfc-125">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="19dfc-125">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19dfc-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-127">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("коннектортипе"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 8 \| внутренний/внешний соединитель")</span><span class="sxs-lookup"><span data-stu-id="19dfc-127">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Internal/External Connector Type")</span></span>
</dt> </dl>

<span data-ttu-id="19dfc-128">Массив физических атрибутов соединителя, используемого этим портом.</span><span class="sxs-lookup"><span data-stu-id="19dfc-128">Array of physical attributes of the connector used by this port.</span></span>

<span data-ttu-id="19dfc-129">Это свойство наследуется от [**CIM \_ фисикалконнектор**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="19dfc-129">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span> <span data-ttu-id="19dfc-130">В следующем списке перечислены значения.</span><span class="sxs-lookup"><span data-stu-id="19dfc-130">The following list lists the values.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="19dfc-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="19dfc-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="19dfc-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="19dfc-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span data-ttu-id="19dfc-133"><span id="Male"></span><span id="male"></span><span id="MALE"></span>**Штекер** (2)</span><span class="sxs-lookup"><span data-stu-id="19dfc-133"><span id="Male"></span><span id="male"></span><span id="MALE"></span>**Male** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span data-ttu-id="19dfc-134"><span id="Female"></span><span id="female"></span><span id="FEMALE"></span>**Женщина** (3)</span><span class="sxs-lookup"><span data-stu-id="19dfc-134"><span id="Female"></span><span id="female"></span><span id="FEMALE"></span>**Female** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="19dfc-135"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Экранированный** (4)</span><span class="sxs-lookup"><span data-stu-id="19dfc-135"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Shielded** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span data-ttu-id="19dfc-136"><span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>**Неэкранированный** (5)</span><span class="sxs-lookup"><span data-stu-id="19dfc-136"><span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>**Unshielded** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span data-ttu-id="19dfc-137"><span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>**SCSI (A) High-Density (50 ПИН-коды)** (6)</span><span class="sxs-lookup"><span data-stu-id="19dfc-137"><span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>**SCSI (A) High-Density (50 pins)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span data-ttu-id="19dfc-138"><span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>**SCSI (A) Low-Density (50 ПИН-коды)** (7)</span><span class="sxs-lookup"><span data-stu-id="19dfc-138"><span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>**SCSI (A) Low-Density (50 pins)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span data-ttu-id="19dfc-139"><span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>**High-Density SCSI (P) (68 ПИН-коды)** (8)</span><span class="sxs-lookup"><span data-stu-id="19dfc-139"><span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>**SCSI (P) High-Density (68 pins)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span data-ttu-id="19dfc-140"><span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>**SCSI SCA-I (80 ПИН)** (9)</span><span class="sxs-lookup"><span data-stu-id="19dfc-140"><span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>**SCSI SCA-I (80 pins)** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span data-ttu-id="19dfc-141"><span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>**SCSI SCA-II (80 контактов)** (10)</span><span class="sxs-lookup"><span data-stu-id="19dfc-141"><span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>**SCSI SCA-II (80 pins)** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span data-ttu-id="19dfc-142"><span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>**Fibre Channel SCSI (DB-9, медный)** (11)</span><span class="sxs-lookup"><span data-stu-id="19dfc-142"><span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>**SCSI Fibre Channel (DB-9, Copper)** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span data-ttu-id="19dfc-143"><span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>**Fibre Channel SCSI (Fibre)** (12)</span><span class="sxs-lookup"><span data-stu-id="19dfc-143"><span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>**SCSI Fibre Channel (Fibre)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span data-ttu-id="19dfc-144"><span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>**SCSI Fibre Channel SCA-II (40 ПИН)** (13)</span><span class="sxs-lookup"><span data-stu-id="19dfc-144"><span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>**SCSI Fibre Channel SCA-II (40 pins)** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span data-ttu-id="19dfc-145"><span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>**SCSI Fibre Channel SCA-II (20 контактов)** (14)</span><span class="sxs-lookup"><span data-stu-id="19dfc-145"><span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>**SCSI Fibre Channel SCA-II (20 pins)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span data-ttu-id="19dfc-146"><span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>**SCSI Fibre Channel БНК** (15)</span><span class="sxs-lookup"><span data-stu-id="19dfc-146"><span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>**SCSI Fibre Channel BNC** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span data-ttu-id="19dfc-147"><span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>**ATA 3-1/2 дюйма (40 контактов)** (16)</span><span class="sxs-lookup"><span data-stu-id="19dfc-147"><span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>**ATA 3-1/2 Inch (40 pins)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span data-ttu-id="19dfc-148"><span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>**ATA 2-1/2 дюйма (44 контактов)** (17)</span><span class="sxs-lookup"><span data-stu-id="19dfc-148"><span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>**ATA 2-1/2 Inch (44 pins)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span data-ttu-id="19dfc-149"><span id="ATA-2"></span><span id="ata-2"></span>**ATA-2** (18)</span><span class="sxs-lookup"><span data-stu-id="19dfc-149"><span id="ATA-2"></span><span id="ata-2"></span>**ATA-2** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span data-ttu-id="19dfc-150"><span id="ATA-3"></span><span id="ata-3"></span>**ATA-3** (19)</span><span class="sxs-lookup"><span data-stu-id="19dfc-150"><span id="ATA-3"></span><span id="ata-3"></span>**ATA-3** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span data-ttu-id="19dfc-151"><span id="ATA_66"></span><span id="ata_66"></span>**ATA/66** (20)</span><span class="sxs-lookup"><span data-stu-id="19dfc-151"><span id="ATA_66"></span><span id="ata_66"></span>**ATA/66** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span data-ttu-id="19dfc-152"><span id="DB-9"></span><span id="db-9"></span>**DB-9** (21)</span><span class="sxs-lookup"><span data-stu-id="19dfc-152"><span id="DB-9"></span><span id="db-9"></span>**DB-9** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span data-ttu-id="19dfc-153"><span id="DB-15"></span><span id="db-15"></span>**DB-15** (22)</span><span class="sxs-lookup"><span data-stu-id="19dfc-153"><span id="DB-15"></span><span id="db-15"></span>**DB-15** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span data-ttu-id="19dfc-154"><span id="DB-25"></span><span id="db-25"></span>**DB-25** (23)</span><span class="sxs-lookup"><span data-stu-id="19dfc-154"><span id="DB-25"></span><span id="db-25"></span>**DB-25** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span data-ttu-id="19dfc-155"><span id="DB-36"></span><span id="db-36"></span>**DB-36** (24)</span><span class="sxs-lookup"><span data-stu-id="19dfc-155"><span id="DB-36"></span><span id="db-36"></span>**DB-36** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span data-ttu-id="19dfc-156"><span id="RS-232C"></span><span id="rs-232c"></span>**RS-232c** (25)</span><span class="sxs-lookup"><span data-stu-id="19dfc-156"><span id="RS-232C"></span><span id="rs-232c"></span>**RS-232C** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span data-ttu-id="19dfc-157"><span id="RS-422"></span><span id="rs-422"></span>**RS-422** (26)</span><span class="sxs-lookup"><span data-stu-id="19dfc-157"><span id="RS-422"></span><span id="rs-422"></span>**RS-422** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span data-ttu-id="19dfc-158"><span id="RS-423"></span><span id="rs-423"></span>**RS-423** (27)</span><span class="sxs-lookup"><span data-stu-id="19dfc-158"><span id="RS-423"></span><span id="rs-423"></span>**RS-423** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span data-ttu-id="19dfc-159"><span id="RS-485"></span><span id="rs-485"></span>**RS-485** (28)</span><span class="sxs-lookup"><span data-stu-id="19dfc-159"><span id="RS-485"></span><span id="rs-485"></span>**RS-485** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span data-ttu-id="19dfc-160"><span id="RS-449"></span><span id="rs-449"></span>**RS-449** (29)</span><span class="sxs-lookup"><span data-stu-id="19dfc-160"><span id="RS-449"></span><span id="rs-449"></span>**RS-449** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="19dfc-161"><span id="v.35"></span>**V. 35** (30)</span><span class="sxs-lookup"><span data-stu-id="19dfc-161"><span id="v.35"></span>**V.35** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span data-ttu-id="19dfc-162"><span id="x.21"></span>**X. 21** (31)</span><span class="sxs-lookup"><span data-stu-id="19dfc-162"><span id="x.21"></span>**X.21** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="19dfc-163"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (32)</span><span class="sxs-lookup"><span data-stu-id="19dfc-163"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span data-ttu-id="19dfc-164"><span id="AUI"></span><span id="aui"></span>**АУИ** (33)</span><span class="sxs-lookup"><span data-stu-id="19dfc-164"><span id="AUI"></span><span id="aui"></span>**AUI** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span data-ttu-id="19dfc-165"><span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>**UTP Категория 3** (34)</span><span class="sxs-lookup"><span data-stu-id="19dfc-165"><span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>**UTP Category 3** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span data-ttu-id="19dfc-166"><span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>**UTP Категория 4** (35)</span><span class="sxs-lookup"><span data-stu-id="19dfc-166"><span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>**UTP Category 4** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span data-ttu-id="19dfc-167"><span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>**UTP Category 5** (36)</span><span class="sxs-lookup"><span data-stu-id="19dfc-167"><span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>**UTP Category 5** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span data-ttu-id="19dfc-168"><span id="BNC"></span><span id="bnc"></span>**БНК** (37)</span><span class="sxs-lookup"><span data-stu-id="19dfc-168"><span id="BNC"></span><span id="bnc"></span>**BNC** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span data-ttu-id="19dfc-169"><span id="RJ11"></span><span id="rj11"></span>**RJ11** (38)</span><span class="sxs-lookup"><span data-stu-id="19dfc-169"><span id="RJ11"></span><span id="rj11"></span>**RJ11** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span data-ttu-id="19dfc-170"><span id="RJ45"></span><span id="rj45"></span>**RJ45** (39)</span><span class="sxs-lookup"><span data-stu-id="19dfc-170"><span id="RJ45"></span><span id="rj45"></span>**RJ45** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span data-ttu-id="19dfc-171"><span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>**Оптоволоконный микрофон** (40)</span><span class="sxs-lookup"><span data-stu-id="19dfc-171"><span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>**Fiber MIC** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span data-ttu-id="19dfc-172"><span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>**Apple АУИ** (41)</span><span class="sxs-lookup"><span data-stu-id="19dfc-172"><span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>**Apple AUI** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span data-ttu-id="19dfc-173"><span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>**Геопорт Apple** (42)</span><span class="sxs-lookup"><span data-stu-id="19dfc-173"><span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>**Apple GeoPort** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="19dfc-174"><span id="PCI"></span><span id="pci"></span>**PCI** (43)</span><span class="sxs-lookup"><span data-stu-id="19dfc-174"><span id="PCI"></span><span id="pci"></span>**PCI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="19dfc-175"><span id="ISA"></span><span id="isa"></span>**ISA** (44)</span><span class="sxs-lookup"><span data-stu-id="19dfc-175"><span id="ISA"></span><span id="isa"></span>**ISA** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="19dfc-176"><span id="EISA"></span><span id="eisa"></span>**EISA** (45)</span><span class="sxs-lookup"><span data-stu-id="19dfc-176"><span id="EISA"></span><span id="eisa"></span>**EISA** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="19dfc-177"><span id="VESA"></span><span id="vesa"></span>**VESA** (46)</span><span class="sxs-lookup"><span data-stu-id="19dfc-177"><span id="VESA"></span><span id="vesa"></span>**VESA** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="19dfc-178"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (47)</span><span class="sxs-lookup"><span data-stu-id="19dfc-178"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span data-ttu-id="19dfc-179"><span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>**Тип PCMCIA I** (48)</span><span class="sxs-lookup"><span data-stu-id="19dfc-179"><span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>**PCMCIA Type I** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="19dfc-180"><span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>**PCMCIA типа II** (49)</span><span class="sxs-lookup"><span data-stu-id="19dfc-180"><span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>**PCMCIA Type II** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="19dfc-181"><span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>**PCMCIA типа III** (50)</span><span class="sxs-lookup"><span data-stu-id="19dfc-181"><span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>**PCMCIA Type III** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span data-ttu-id="19dfc-182"><span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>**Порт зв** (51)</span><span class="sxs-lookup"><span data-stu-id="19dfc-182"><span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>**ZV Port** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="19dfc-183"><span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>**CardBus** (52)</span><span class="sxs-lookup"><span data-stu-id="19dfc-183"><span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>**CardBus** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="19dfc-184"><span id="USB"></span><span id="usb"></span>**USB** (53)</span><span class="sxs-lookup"><span data-stu-id="19dfc-184"><span id="USB"></span><span id="usb"></span>**USB** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="19dfc-185"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (54)</span><span class="sxs-lookup"><span data-stu-id="19dfc-185"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="19dfc-186"><span id="HIPPI"></span><span id="hippi"></span>**Хиппи** (55)</span><span class="sxs-lookup"><span data-stu-id="19dfc-186"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span data-ttu-id="19dfc-187"><span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>**Хссдк (6 контактов)** (56)</span><span class="sxs-lookup"><span data-stu-id="19dfc-187"><span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>**HSSDC (6 pins)** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span data-ttu-id="19dfc-188"><span id="GBIC"></span><span id="gbic"></span>**Гбик** (57)</span><span class="sxs-lookup"><span data-stu-id="19dfc-188"><span id="GBIC"></span><span id="gbic"></span>**GBIC** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span data-ttu-id="19dfc-189"><span id="DIN"></span><span id="din"></span>**DIN** (58)</span><span class="sxs-lookup"><span data-stu-id="19dfc-189"><span id="DIN"></span><span id="din"></span>**DIN** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span data-ttu-id="19dfc-190"><span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>**Мини-DIN** (59)</span><span class="sxs-lookup"><span data-stu-id="19dfc-190"><span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>**Mini-DIN** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span data-ttu-id="19dfc-191"><span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>**Micro-DIN** (60)</span><span class="sxs-lookup"><span data-stu-id="19dfc-191"><span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>**Micro-DIN** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="19dfc-192"><span id="PS_2"></span><span id="ps_2"></span>**PS/2** (61)</span><span class="sxs-lookup"><span data-stu-id="19dfc-192"><span id="PS_2"></span><span id="ps_2"></span>**PS/2** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="19dfc-193"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Инфракрасная связь** (62)</span><span class="sxs-lookup"><span data-stu-id="19dfc-193"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="19dfc-194"><span id="HP-HIL"></span><span id="hp-hil"></span>**HP-Хил** (63)</span><span class="sxs-lookup"><span data-stu-id="19dfc-194"><span id="HP-HIL"></span><span id="hp-hil"></span>**HP-HIL** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span data-ttu-id="19dfc-195"><span id="access.bus"></span><span id="ACCESS.BUS"></span>**Доступ. Bus** (64)</span><span class="sxs-lookup"><span data-stu-id="19dfc-195"><span id="access.bus"></span><span id="ACCESS.BUS"></span>**Access.bus** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="19dfc-196"><span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>**Нубус** (65)</span><span class="sxs-lookup"><span data-stu-id="19dfc-196"><span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>**NuBus** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span data-ttu-id="19dfc-197"><span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>**Центроникс** (66)</span><span class="sxs-lookup"><span data-stu-id="19dfc-197"><span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>**Centronics** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span data-ttu-id="19dfc-198"><span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>**Мини-центроникс** (67)</span><span class="sxs-lookup"><span data-stu-id="19dfc-198"><span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>**Mini-Centronics** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span data-ttu-id="19dfc-199"><span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>**Тип мини-центроникс — 14** (68)</span><span class="sxs-lookup"><span data-stu-id="19dfc-199"><span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>**Mini-Centronics Type-14** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span data-ttu-id="19dfc-200"><span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>**Mini-Центроникс Type-20** (69)</span><span class="sxs-lookup"><span data-stu-id="19dfc-200"><span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>**Mini-Centronics Type-20** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span data-ttu-id="19dfc-201"><span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>**Mini-Центроникс Type-26** (70)</span><span class="sxs-lookup"><span data-stu-id="19dfc-201"><span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>**Mini-Centronics Type-26** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="19dfc-202"><span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>**Мышь шины** (71)</span><span class="sxs-lookup"><span data-stu-id="19dfc-202"><span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>**Bus Mouse** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span data-ttu-id="19dfc-203"><span id="ADB"></span><span id="adb"></span>**ADB** (72)</span><span class="sxs-lookup"><span data-stu-id="19dfc-203"><span id="ADB"></span><span id="adb"></span>**ADB** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="19dfc-204"><span id="AGP"></span><span id="agp"></span>**AGP** (73)</span><span class="sxs-lookup"><span data-stu-id="19dfc-204"><span id="AGP"></span><span id="agp"></span>**AGP** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="19dfc-205"><span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>**Шина вме** (74)</span><span class="sxs-lookup"><span data-stu-id="19dfc-205"><span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>**VME Bus** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span data-ttu-id="19dfc-206"><span id="VME64"></span><span id="vme64"></span>**VME64** (75)</span><span class="sxs-lookup"><span data-stu-id="19dfc-206"><span id="VME64"></span><span id="vme64"></span>**VME64** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="19dfc-207"><span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>**Частный** (76)</span><span class="sxs-lookup"><span data-stu-id="19dfc-207"><span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>**Proprietary** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span data-ttu-id="19dfc-208"><span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>**Собственный слот карты процессора** (77)</span><span class="sxs-lookup"><span data-stu-id="19dfc-208"><span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>**Proprietary Processor Card Slot** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span data-ttu-id="19dfc-209"><span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>**Собственный слот карты памяти** (78)</span><span class="sxs-lookup"><span data-stu-id="19dfc-209"><span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>**Proprietary Memory Card Slot** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span data-ttu-id="19dfc-210"><span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>**Собственная Подплата ввода/вывода** (79)</span><span class="sxs-lookup"><span data-stu-id="19dfc-210"><span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>**Proprietary I/O Riser Slot** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span data-ttu-id="19dfc-211"><span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>**PCI-66** (80)</span><span class="sxs-lookup"><span data-stu-id="19dfc-211"><span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>**PCI-66MHZ** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span data-ttu-id="19dfc-212"><span id="AGP2X"></span><span id="agp2x"></span>**AGP2X** (81)</span><span class="sxs-lookup"><span data-stu-id="19dfc-212"><span id="AGP2X"></span><span id="agp2x"></span>**AGP2X** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span data-ttu-id="19dfc-213"><span id="AGP4X"></span><span id="agp4x"></span>**AGP4X** (82)</span><span class="sxs-lookup"><span data-stu-id="19dfc-213"><span id="AGP4X"></span><span id="agp4x"></span>**AGP4X** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="19dfc-214"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (83)</span><span class="sxs-lookup"><span data-stu-id="19dfc-214"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>

<span data-ttu-id="19dfc-215"><span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>**PC-98Hireso** (84)</span><span class="sxs-lookup"><span data-stu-id="19dfc-215"><span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>**PC-98Hireso** (84)</span></span>


</dt> <dd>

<span data-ttu-id="19dfc-216">PC-98-Хиресо</span><span class="sxs-lookup"><span data-stu-id="19dfc-216">PC-98-Hireso</span></span>

</dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="19dfc-217"><span id="PC-H98"></span><span id="pc-h98"></span>**PC-H98** (85)</span><span class="sxs-lookup"><span data-stu-id="19dfc-217"><span id="PC-H98"></span><span id="pc-h98"></span>**PC-H98** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span data-ttu-id="19dfc-218"><span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>**PC-98Note** (86)</span><span class="sxs-lookup"><span data-stu-id="19dfc-218"><span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>**PC-98Note** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span data-ttu-id="19dfc-219"><span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>**PC-98Full** (87)</span><span class="sxs-lookup"><span data-stu-id="19dfc-219"><span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>**PC-98Full** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>

<span data-ttu-id="19dfc-220"><span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>**Мини-гнездо** (88)</span><span class="sxs-lookup"><span data-stu-id="19dfc-220"><span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>**Mini-Jack** (88)</span></span>


</dt> <dd>

<span data-ttu-id="19dfc-221">АДАПТЕР SSA SCSI</span><span class="sxs-lookup"><span data-stu-id="19dfc-221">SSA SCSI</span></span>

</dd> <dt>

<span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>

<span data-ttu-id="19dfc-222"><span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>**На платной дискете** (89)</span><span class="sxs-lookup"><span data-stu-id="19dfc-222"><span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>**On Board Floppy** (89)</span></span>


</dt> <dd>

<span data-ttu-id="19dfc-223">Кольцевая</span><span class="sxs-lookup"><span data-stu-id="19dfc-223">Circular</span></span>

</dd> <dt>

<span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>

<span data-ttu-id="19dfc-224"><span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>**9-штырьковый двухрядный (вывод 10 для вырезания)** (90)</span><span class="sxs-lookup"><span data-stu-id="19dfc-224"><span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>**9 Pin Dual Inline (pin 10 cut)** (90)</span></span>


</dt> <dd>

<span data-ttu-id="19dfc-225">Соединитель IDE платы</span><span class="sxs-lookup"><span data-stu-id="19dfc-225">On Board IDE Connector</span></span>

</dd> <dt>

<span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>

<span data-ttu-id="19dfc-226"><span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>**25-контактный двойной текст (ПИН 26 вырезан)** (91)</span><span class="sxs-lookup"><span data-stu-id="19dfc-226"><span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>**25 Pin Dual Inline (pin 26 cut)** (91)</span></span>


</dt> <dd>

<span data-ttu-id="19dfc-227">Разъем флоппи-дисковода</span><span class="sxs-lookup"><span data-stu-id="19dfc-227">On Board Floppy Connector</span></span>

</dd> <dt>

<span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>

<span data-ttu-id="19dfc-228"><span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>**50. закрепление двух встраиваемых систем** (92)</span><span class="sxs-lookup"><span data-stu-id="19dfc-228"><span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>**50 Pin Dual Inline** (92)</span></span>


</dt> <dd>

<span data-ttu-id="19dfc-229">9. закрепление двух встроенных</span><span class="sxs-lookup"><span data-stu-id="19dfc-229">9 Pin Dual Inline</span></span>

</dd> <dt>

<span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>

<span data-ttu-id="19dfc-230"><span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>**68. закрепление двух встраиваемых систем** (93)</span><span class="sxs-lookup"><span data-stu-id="19dfc-230"><span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>**68 Pin Dual Inline** (93)</span></span>


</dt> <dd>

<span data-ttu-id="19dfc-231">25-контактный двойной текст</span><span class="sxs-lookup"><span data-stu-id="19dfc-231">25 Pin Dual Inline</span></span>

</dd> <dt>

<span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>

<span data-ttu-id="19dfc-232"><span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>**На платном звуковом вводе с компакт-диска** (94)</span><span class="sxs-lookup"><span data-stu-id="19dfc-232"><span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>**On Board Sound Input from CD-ROM** (94)</span></span>


</dt> <dd>

<span data-ttu-id="19dfc-233">50. закрепление двух встроенных</span><span class="sxs-lookup"><span data-stu-id="19dfc-233">50 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-234">95</span><span class="sxs-lookup"><span data-stu-id="19dfc-234">95</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-235">68. закрепление двух встроенных</span><span class="sxs-lookup"><span data-stu-id="19dfc-235">68 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-236">96</span><span class="sxs-lookup"><span data-stu-id="19dfc-236">96</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-237">Звуковой разъем на доске</span><span class="sxs-lookup"><span data-stu-id="19dfc-237">On Board Sound Connector</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-238">97</span><span class="sxs-lookup"><span data-stu-id="19dfc-238">97</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-239">Mini-Jack</span><span class="sxs-lookup"><span data-stu-id="19dfc-239">Mini-Jack</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-240">98</span><span class="sxs-lookup"><span data-stu-id="19dfc-240">98</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-241">PCI-X</span><span class="sxs-lookup"><span data-stu-id="19dfc-241">PCI-X</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-242">99</span><span class="sxs-lookup"><span data-stu-id="19dfc-242">99</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-243">Сбус IEEE 1396-1993 32, бит</span><span class="sxs-lookup"><span data-stu-id="19dfc-243">Sbus IEEE 1396-1993 32 Bit</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-244">100</span><span class="sxs-lookup"><span data-stu-id="19dfc-244">100</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-245">Сбус IEEE 1396-1993 64, бит</span><span class="sxs-lookup"><span data-stu-id="19dfc-245">Sbus IEEE 1396-1993 64 Bit</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-246">101</span><span class="sxs-lookup"><span data-stu-id="19dfc-246">101</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-247">MCA</span><span class="sxs-lookup"><span data-stu-id="19dfc-247">MCA</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-248">102</span><span class="sxs-lookup"><span data-stu-id="19dfc-248">102</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-249">гио</span><span class="sxs-lookup"><span data-stu-id="19dfc-249">GIO</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-250">103</span><span class="sxs-lookup"><span data-stu-id="19dfc-250">103</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-251">XIO</span><span class="sxs-lookup"><span data-stu-id="19dfc-251">XIO</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-252">104</span><span class="sxs-lookup"><span data-stu-id="19dfc-252">104</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-253">хио</span><span class="sxs-lookup"><span data-stu-id="19dfc-253">HIO</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-254">105</span><span class="sxs-lookup"><span data-stu-id="19dfc-254">105</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-255">нгио</span><span class="sxs-lookup"><span data-stu-id="19dfc-255">NGIO</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-256">106</span><span class="sxs-lookup"><span data-stu-id="19dfc-256">106</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-257">PMC</span><span class="sxs-lookup"><span data-stu-id="19dfc-257">PMC</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-258">107</span><span class="sxs-lookup"><span data-stu-id="19dfc-258">107</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-259">мтрж</span><span class="sxs-lookup"><span data-stu-id="19dfc-259">MTRJ</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-260">108</span><span class="sxs-lookup"><span data-stu-id="19dfc-260">108</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-261">VF-45</span><span class="sxs-lookup"><span data-stu-id="19dfc-261">VF-45</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-262">109</span><span class="sxs-lookup"><span data-stu-id="19dfc-262">109</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-263">Будущие операции ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="19dfc-263">Future I/O</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-264">110</span><span class="sxs-lookup"><span data-stu-id="19dfc-264">110</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-265">SC</span><span class="sxs-lookup"><span data-stu-id="19dfc-265">SC</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-266">111</span><span class="sxs-lookup"><span data-stu-id="19dfc-266">111</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-267">SG</span><span class="sxs-lookup"><span data-stu-id="19dfc-267">SG</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-268">112</span><span class="sxs-lookup"><span data-stu-id="19dfc-268">112</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-269">Электричество</span><span class="sxs-lookup"><span data-stu-id="19dfc-269">Electrical</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-270">113</span><span class="sxs-lookup"><span data-stu-id="19dfc-270">113</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-271">Лазер</span><span class="sxs-lookup"><span data-stu-id="19dfc-271">Optical</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-272">114</span><span class="sxs-lookup"><span data-stu-id="19dfc-272">114</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-273">Лента</span><span class="sxs-lookup"><span data-stu-id="19dfc-273">Ribbon</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-274">115</span><span class="sxs-lookup"><span data-stu-id="19dfc-274">115</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-275">GLM</span><span class="sxs-lookup"><span data-stu-id="19dfc-275">GLM</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-276">116</span><span class="sxs-lookup"><span data-stu-id="19dfc-276">116</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-277">1x9</span><span class="sxs-lookup"><span data-stu-id="19dfc-277">1x9</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-278">117</span><span class="sxs-lookup"><span data-stu-id="19dfc-278">117</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-279">Мини-SG</span><span class="sxs-lookup"><span data-stu-id="19dfc-279">Mini SG</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-280">118</span><span class="sxs-lookup"><span data-stu-id="19dfc-280">118</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-281">LC</span><span class="sxs-lookup"><span data-stu-id="19dfc-281">LC</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-282">119</span><span class="sxs-lookup"><span data-stu-id="19dfc-282">119</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-283">хсск</span><span class="sxs-lookup"><span data-stu-id="19dfc-283">HSSC</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-284">120</span><span class="sxs-lookup"><span data-stu-id="19dfc-284">120</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-285">ВХДЦИ экранированный (68 контактов)</span><span class="sxs-lookup"><span data-stu-id="19dfc-285">VHDCI Shielded (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-286">121</span><span class="sxs-lookup"><span data-stu-id="19dfc-286">121</span></span>
</dt> <dd>

<span data-ttu-id="19dfc-287">InfiniBand</span><span class="sxs-lookup"><span data-stu-id="19dfc-287">InfiniBand</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="19dfc-288">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="19dfc-288">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19dfc-289">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19dfc-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-290">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19dfc-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-291">Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="19dfc-291">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="19dfc-292">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="19dfc-292">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="19dfc-293">При использовании с другими ключевыми свойствами класса свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="19dfc-293">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="19dfc-294">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="19dfc-294">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-295">**Описание**</span><span class="sxs-lookup"><span data-stu-id="19dfc-295">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19dfc-296">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19dfc-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-297">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19dfc-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-298">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="19dfc-298">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="19dfc-299">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="19dfc-299">Description of the object.</span></span>

<span data-ttu-id="19dfc-300">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="19dfc-300">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-301">**екстерналреференцедесигнатор**</span><span class="sxs-lookup"><span data-stu-id="19dfc-301">**ExternalReferenceDesignator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19dfc-302">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19dfc-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19dfc-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-304">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 8, \| обозначение внешней ссылки")</span><span class="sxs-lookup"><span data-stu-id="19dfc-304">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|External Reference Designator")</span></span>
</dt> </dl>

<span data-ttu-id="19dfc-305">Указатель внешней ссылки на порт.</span><span class="sxs-lookup"><span data-stu-id="19dfc-305">External reference designator of the port.</span></span> <span data-ttu-id="19dfc-306">Обозначения внешних ссылок — это идентификаторы, которые определяют тип и использование порта.</span><span class="sxs-lookup"><span data-stu-id="19dfc-306">External reference designators are identifiers that determine the type and use of the port.</span></span>

<span data-ttu-id="19dfc-307">Пример: "COM1"</span><span class="sxs-lookup"><span data-stu-id="19dfc-307">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-308">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="19dfc-308">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19dfc-309">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="19dfc-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19dfc-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-311">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="19dfc-311">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="19dfc-312">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="19dfc-312">Date and time the object is installed.</span></span> <span data-ttu-id="19dfc-313">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="19dfc-313">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="19dfc-314">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="19dfc-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-315">**интерналреференцедесигнатор**</span><span class="sxs-lookup"><span data-stu-id="19dfc-315">**InternalReferenceDesignator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19dfc-316">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19dfc-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19dfc-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-318">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| \| обозначение внутренней ссылки SMBIOS Type 8")</span><span class="sxs-lookup"><span data-stu-id="19dfc-318">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Internal Reference Designator")</span></span>
</dt> </dl>

<span data-ttu-id="19dfc-319">Внутреннее обозначение указателя порта.</span><span class="sxs-lookup"><span data-stu-id="19dfc-319">Internal reference designator of the port.</span></span> <span data-ttu-id="19dfc-320">Обозначения внутренних ссылок зависят от производителя и определяют расположение или использование порта на плате.</span><span class="sxs-lookup"><span data-stu-id="19dfc-320">Internal reference designators are specific to the manufacturer, and identify the circuit board location or use of the port.</span></span>

<span data-ttu-id="19dfc-321">Пример: "J101"</span><span class="sxs-lookup"><span data-stu-id="19dfc-321">Example: "J101"</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-322">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="19dfc-322">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19dfc-323">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19dfc-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19dfc-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-325">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="19dfc-325">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="19dfc-326">Имя Организации, ответственной за создание физического элемента.</span><span class="sxs-lookup"><span data-stu-id="19dfc-326">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="19dfc-327">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="19dfc-327">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-328">**Модель**</span><span class="sxs-lookup"><span data-stu-id="19dfc-328">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19dfc-329">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19dfc-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19dfc-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-331">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="19dfc-331">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="19dfc-332">Имя физического элемента.</span><span class="sxs-lookup"><span data-stu-id="19dfc-332">Name for the physical element.</span></span>

<span data-ttu-id="19dfc-333">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="19dfc-333">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-334">**Name**</span><span class="sxs-lookup"><span data-stu-id="19dfc-334">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19dfc-335">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19dfc-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19dfc-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-337">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="19dfc-337">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="19dfc-338">Метка для объекта.</span><span class="sxs-lookup"><span data-stu-id="19dfc-338">Label for the object.</span></span> <span data-ttu-id="19dfc-339">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="19dfc-339">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="19dfc-340">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="19dfc-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="19dfc-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19dfc-342">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19dfc-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19dfc-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19dfc-344">Дополнительные данные, помимо сведений о тегах актива, которые можно использовать для поиска физического элемента.</span><span class="sxs-lookup"><span data-stu-id="19dfc-344">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="19dfc-345">Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива.</span><span class="sxs-lookup"><span data-stu-id="19dfc-345">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="19dfc-346">Если только данные штрих-кода доступны и уникальны или могут использоваться в качестве ключа элемента, это свойство имеет **значение NULL** , а данные штрих-кода используются в качестве ключа класса в свойстве Tag.</span><span class="sxs-lookup"><span data-stu-id="19dfc-346">If only bar code data is available and unique or able to be used as an element key, this property is **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="19dfc-347">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="19dfc-347">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-348">**партнумбер**</span><span class="sxs-lookup"><span data-stu-id="19dfc-348">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19dfc-349">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19dfc-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-350">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19dfc-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-351">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="19dfc-351">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="19dfc-352">Номер детали, назначенный Организацией, ответственной за производство или производство физического элемента.</span><span class="sxs-lookup"><span data-stu-id="19dfc-352">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="19dfc-353">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="19dfc-353">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-354">**Порта**</span><span class="sxs-lookup"><span data-stu-id="19dfc-354">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19dfc-355">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="19dfc-355">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19dfc-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-357">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("тип SMBIOS \| 8 \| типа порта")</span><span class="sxs-lookup"><span data-stu-id="19dfc-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Port Type")</span></span>
</dt> </dl>

<span data-ttu-id="19dfc-358">Функция порта.</span><span class="sxs-lookup"><span data-stu-id="19dfc-358">Function of the port.</span></span> <span data-ttu-id="19dfc-359">В следующем списке перечислены значения.</span><span class="sxs-lookup"><span data-stu-id="19dfc-359">The following list lists the values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="19dfc-360">**Нет** (0)</span><span class="sxs-lookup"><span data-stu-id="19dfc-360">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_XT_AT_Compatible"></span><span id="parallel_port_xt_at_compatible"></span><span id="PARALLEL_PORT_XT_AT_COMPATIBLE"></span>

<span data-ttu-id="19dfc-361">**Параллельный порт XT/AT-совместимый** (1)</span><span class="sxs-lookup"><span data-stu-id="19dfc-361">**Parallel Port XT/AT Compatible** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_PS_2"></span><span id="parallel_port_ps_2"></span><span id="PARALLEL_PORT_PS_2"></span>

<span data-ttu-id="19dfc-362">**Параллельный порт PS/2** (2)</span><span class="sxs-lookup"><span data-stu-id="19dfc-362">**Parallel Port PS/2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_ECP"></span><span id="parallel_port_ecp"></span><span id="PARALLEL_PORT_ECP"></span>

<span data-ttu-id="19dfc-363">**Параллельный порт ECP** (3)</span><span class="sxs-lookup"><span data-stu-id="19dfc-363">**Parallel Port ECP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_EPP"></span><span id="parallel_port_epp"></span><span id="PARALLEL_PORT_EPP"></span>

<span data-ttu-id="19dfc-364">**Параллельный порт EPP** (4)</span><span class="sxs-lookup"><span data-stu-id="19dfc-364">**Parallel Port EPP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_ECP_EPP"></span><span id="parallel_port_ecp_epp"></span><span id="PARALLEL_PORT_ECP_EPP"></span>

<span data-ttu-id="19dfc-365">**Параллельный порт ECP/EPP** (5)</span><span class="sxs-lookup"><span data-stu-id="19dfc-365">**Parallel Port ECP/EPP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_XT_AT_Compatible"></span><span id="serial_port_xt_at_compatible"></span><span id="SERIAL_PORT_XT_AT_COMPATIBLE"></span>

<span data-ttu-id="19dfc-366">**XT/AT-совместимый последовательный порт** (6)</span><span class="sxs-lookup"><span data-stu-id="19dfc-366">**Serial Port XT/AT Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16450_Compatible"></span><span id="serial_port_16450_compatible"></span><span id="SERIAL_PORT_16450_COMPATIBLE"></span>

<span data-ttu-id="19dfc-367">**Совместимый последовательный порт 16450** (7)</span><span class="sxs-lookup"><span data-stu-id="19dfc-367">**Serial Port 16450 Compatible** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16550_Compatible"></span><span id="serial_port_16550_compatible"></span><span id="SERIAL_PORT_16550_COMPATIBLE"></span>

<span data-ttu-id="19dfc-368">**Совместимый последовательный порт 16550** (8)</span><span class="sxs-lookup"><span data-stu-id="19dfc-368">**Serial Port 16550 Compatible** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16550A_Compatible"></span><span id="serial_port_16550a_compatible"></span><span id="SERIAL_PORT_16550A_COMPATIBLE"></span>

<span data-ttu-id="19dfc-369">**Совместимый с последовательным портом 16550A** (9)</span><span class="sxs-lookup"><span data-stu-id="19dfc-369">**Serial Port 16550A Compatible** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Port"></span><span id="scsi_port"></span><span id="SCSI_PORT"></span>

<span data-ttu-id="19dfc-370">**Порт SCSI** (10)</span><span class="sxs-lookup"><span data-stu-id="19dfc-370">**SCSI Port** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="MIDI_Port"></span><span id="midi_port"></span><span id="MIDI_PORT"></span>

<span data-ttu-id="19dfc-371">**Порт MIDI** (11)</span><span class="sxs-lookup"><span data-stu-id="19dfc-371">**MIDI Port** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Joy_Stick_Port"></span><span id="joy_stick_port"></span><span id="JOY_STICK_PORT"></span>

<span data-ttu-id="19dfc-372">**Порт джойстика** (12)</span><span class="sxs-lookup"><span data-stu-id="19dfc-372">**Joy Stick Port** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Keyboard_Port"></span><span id="keyboard_port"></span><span id="KEYBOARD_PORT"></span>

<span data-ttu-id="19dfc-373">**Порт клавиатуры** (13)</span><span class="sxs-lookup"><span data-stu-id="19dfc-373">**Keyboard Port** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_Port"></span><span id="mouse_port"></span><span id="MOUSE_PORT"></span>

<span data-ttu-id="19dfc-374">**Порт мыши** (14)</span><span class="sxs-lookup"><span data-stu-id="19dfc-374">**Mouse Port** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SSA_SCSI"></span><span id="ssa_scsi"></span>

<span data-ttu-id="19dfc-375">**Адаптер SSA SCSI** (15)</span><span class="sxs-lookup"><span data-stu-id="19dfc-375">**SSA SCSI** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="19dfc-376">**USB** (16)</span><span class="sxs-lookup"><span data-stu-id="19dfc-376">**USB** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FireWire__IEEE_P1394_"></span><span id="firewire__ieee_p1394_"></span><span id="FIREWIRE__IEEE_P1394_"></span>

<span data-ttu-id="19dfc-377">**FireWire (IEEE P1394)** (17)</span><span class="sxs-lookup"><span data-stu-id="19dfc-377">**FireWire (IEEE P1394)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="19dfc-378">**PCMCIA типа II** (18)</span><span class="sxs-lookup"><span data-stu-id="19dfc-378">**PCMCIA Type II** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="19dfc-379">**PCMCIA типа II** (19)</span><span class="sxs-lookup"><span data-stu-id="19dfc-379">**PCMCIA Type II** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="19dfc-380">**PCMCIA типа III** (20)</span><span class="sxs-lookup"><span data-stu-id="19dfc-380">**PCMCIA Type III** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Cardbus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="19dfc-381">**CardBus** (21)</span><span class="sxs-lookup"><span data-stu-id="19dfc-381">**Cardbus** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Bus_Port"></span><span id="access_bus_port"></span><span id="ACCESS_BUS_PORT"></span>

<span data-ttu-id="19dfc-382">**Порт шины доступа** (22)</span><span class="sxs-lookup"><span data-stu-id="19dfc-382">**Access Bus Port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_II"></span><span id="scsi_ii"></span>

<span data-ttu-id="19dfc-383">**SCSI II** (23)</span><span class="sxs-lookup"><span data-stu-id="19dfc-383">**SCSI II** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Wide"></span><span id="scsi_wide"></span><span id="SCSI_WIDE"></span>

<span data-ttu-id="19dfc-384">**Ширина SCSI** (24)</span><span class="sxs-lookup"><span data-stu-id="19dfc-384">**SCSI Wide** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="19dfc-385">**PC-98** (25)</span><span class="sxs-lookup"><span data-stu-id="19dfc-385">**PC-98** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="19dfc-386">**PC-98-хиресо** (26)</span><span class="sxs-lookup"><span data-stu-id="19dfc-386">**PC-98-Hireso** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="19dfc-387">**PC-H98** (27)</span><span class="sxs-lookup"><span data-stu-id="19dfc-387">**PC-H98** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_Port"></span><span id="video_port"></span><span id="VIDEO_PORT"></span>

<span data-ttu-id="19dfc-388">**Порт видео** (28)</span><span class="sxs-lookup"><span data-stu-id="19dfc-388">**Video Port** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Audio_Port"></span><span id="audio_port"></span><span id="AUDIO_PORT"></span>

<span data-ttu-id="19dfc-389">**Порт аудиоподсистемы** (29)</span><span class="sxs-lookup"><span data-stu-id="19dfc-389">**Audio Port** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Port"></span><span id="modem_port"></span><span id="MODEM_PORT"></span>

<span data-ttu-id="19dfc-390">**Порт модема** (30)</span><span class="sxs-lookup"><span data-stu-id="19dfc-390">**Modem Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Port"></span><span id="network_port"></span><span id="NETWORK_PORT"></span>

<span data-ttu-id="19dfc-391">**Сетевой порт** (31)</span><span class="sxs-lookup"><span data-stu-id="19dfc-391">**Network Port** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="19dfc-392">**Совместимость с 8251** (32)</span><span class="sxs-lookup"><span data-stu-id="19dfc-392">**8251 Compatible** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_FIFO_Compatible"></span><span id="8251_fifo_compatible"></span><span id="8251_FIFO_COMPATIBLE"></span>

<span data-ttu-id="19dfc-393">**8251. совместимость с FIFO** (33)</span><span class="sxs-lookup"><span data-stu-id="19dfc-393">**8251 FIFO Compatible** (33)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="19dfc-394">**повередон**</span><span class="sxs-lookup"><span data-stu-id="19dfc-394">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19dfc-395">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="19dfc-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-396">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19dfc-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19dfc-397">**Значение true** показывает, что физический элемент включен.</span><span class="sxs-lookup"><span data-stu-id="19dfc-397">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="19dfc-398">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="19dfc-398">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-399">**Номер**</span><span class="sxs-lookup"><span data-stu-id="19dfc-399">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19dfc-400">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19dfc-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-401">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19dfc-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-402">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="19dfc-402">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="19dfc-403">Номер, выделенный изготовителем, используемый для обнаружения физического элемента.</span><span class="sxs-lookup"><span data-stu-id="19dfc-403">Manufacturer-allocated number used to identify a physical element.</span></span>

<span data-ttu-id="19dfc-404">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="19dfc-404">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-405">**SKU**</span><span class="sxs-lookup"><span data-stu-id="19dfc-405">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19dfc-406">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19dfc-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-407">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19dfc-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-408">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="19dfc-408">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="19dfc-409">Номер единицы хранения для физического элемента.</span><span class="sxs-lookup"><span data-stu-id="19dfc-409">Stock keeping unit number for a physical element.</span></span>

<span data-ttu-id="19dfc-410">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="19dfc-410">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-411">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="19dfc-411">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19dfc-412">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19dfc-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19dfc-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-414">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="19dfc-414">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="19dfc-415">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="19dfc-415">Current status of the object.</span></span> <span data-ttu-id="19dfc-416">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="19dfc-416">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="19dfc-417">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="19dfc-417">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="19dfc-418">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="19dfc-418">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="19dfc-419">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="19dfc-419">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="19dfc-420">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="19dfc-420">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="19dfc-421">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="19dfc-421">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="19dfc-422">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="19dfc-422">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="19dfc-423">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="19dfc-423">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="19dfc-424">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="19dfc-424">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="19dfc-425">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="19dfc-425">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="19dfc-426">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="19dfc-426">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="19dfc-427">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="19dfc-427">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="19dfc-428">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="19dfc-428">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="19dfc-429">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="19dfc-429">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="19dfc-430">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="19dfc-430">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="19dfc-431">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="19dfc-431">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="19dfc-432">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="19dfc-432">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="19dfc-433">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="19dfc-433">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="19dfc-434">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="19dfc-434">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="19dfc-435">**Тег**</span><span class="sxs-lookup"><span data-stu-id="19dfc-435">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19dfc-436">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19dfc-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-437">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19dfc-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-438">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**reoverride**](../wmisdk/standard-qualifiers.md) ("тег"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="19dfc-438">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="19dfc-439">Уникальный идентификатор соединения с портом в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="19dfc-439">Unique identifier of a port connection on the computer system.</span></span>

<span data-ttu-id="19dfc-440">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="19dfc-440">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="19dfc-441">Пример: "соединитель порта 1"</span><span class="sxs-lookup"><span data-stu-id="19dfc-441">Example: "Port Connector 1"</span></span>

</dd> <dt>

<span data-ttu-id="19dfc-442">**Version**</span><span class="sxs-lookup"><span data-stu-id="19dfc-442">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19dfc-443">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19dfc-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-444">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19dfc-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19dfc-445">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="19dfc-445">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="19dfc-446">Версия физического элемента.</span><span class="sxs-lookup"><span data-stu-id="19dfc-446">Version of the physical element.</span></span>

<span data-ttu-id="19dfc-447">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="19dfc-447">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19dfc-448">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19dfc-448">Remarks</span></span>

<span data-ttu-id="19dfc-449">Класс **Win32 \_ портконнектор** является производным от [**CIM \_ фисикалконнектор**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="19dfc-449">The **Win32\_PortConnector** class is derived from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19dfc-450">Требования</span><span class="sxs-lookup"><span data-stu-id="19dfc-450">Requirements</span></span>



| <span data-ttu-id="19dfc-451">Требование</span><span class="sxs-lookup"><span data-stu-id="19dfc-451">Requirement</span></span> | <span data-ttu-id="19dfc-452">Значение</span><span class="sxs-lookup"><span data-stu-id="19dfc-452">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19dfc-453">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19dfc-453">Minimum supported client</span></span><br/> | <span data-ttu-id="19dfc-454">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19dfc-454">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="19dfc-455">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19dfc-455">Minimum supported server</span></span><br/> | <span data-ttu-id="19dfc-456">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19dfc-456">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="19dfc-457">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="19dfc-457">Namespace</span></span><br/>                | <span data-ttu-id="19dfc-458">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="19dfc-458">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="19dfc-459">MOF</span><span class="sxs-lookup"><span data-stu-id="19dfc-459">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19dfc-460"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19dfc-460"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="19dfc-461">DLL</span><span class="sxs-lookup"><span data-stu-id="19dfc-461">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19dfc-462"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19dfc-462"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19dfc-463">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19dfc-463">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19dfc-464">**\_ФИСИКАЛКОННЕКТОР CIM**</span><span class="sxs-lookup"><span data-stu-id="19dfc-464">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> <dt>

[<span data-ttu-id="19dfc-465">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="19dfc-465">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
