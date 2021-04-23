---
description: Представляет атрибуты базовых служб ввода-вывода (BIOS) компьютерной системы, установленных на компьютере.
ms.assetid: e4a5aaf0-0432-4517-97b7-ac05ffd10b5b
ms.tgt_platform: multiple
title: Класс Win32_BIOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BIOS
- Win32_BIOS.BiosCharacteristics
- Win32_BIOS.BIOSVersion
- Win32_BIOS.BuildNumber
- Win32_BIOS.Caption
- Win32_BIOS.CodeSet
- Win32_BIOS.CurrentLanguage
- Win32_BIOS.Description
- Win32_BIOS.EmbeddedControllerMajorVersion
- Win32_BIOS.EmbeddedControllerMinorVersion
- Win32_BIOS.IdentificationCode
- Win32_BIOS.InstallableLanguages
- Win32_BIOS.InstallDate
- Win32_BIOS.LanguageEdition
- Win32_BIOS.ListOfLanguages
- Win32_BIOS.Manufacturer
- Win32_BIOS.Name
- Win32_BIOS.OtherTargetOS
- Win32_BIOS.PrimaryBIOS
- Win32_BIOS.ReleaseDate
- Win32_BIOS.SerialNumber
- Win32_BIOS.SMBIOSBIOSVersion
- Win32_BIOS.SMBIOSMajorVersion
- Win32_BIOS.SMBIOSMinorVersion
- Win32_BIOS.SMBIOSPresent
- Win32_BIOS.SoftwareElementID
- Win32_BIOS.SoftwareElementState
- Win32_BIOS.Status
- Win32_BIOS.SystemBiosMajorVersion
- Win32_BIOS.SystemBiosMinorVersion
- Win32_BIOS.TargetOperatingSystem
- Win32_BIOS.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 53c1e953c9c1348a133cf4755ab04f6024c42034
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539236"
---
# <a name="win32_bios-class"></a><span data-ttu-id="68dfe-103">\_Класс Win32 BIOS</span><span class="sxs-lookup"><span data-stu-id="68dfe-103">Win32\_BIOS class</span></span>

<span data-ttu-id="68dfe-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ BIOS Win32** представляет атрибуты базовых служб ввода-вывода (BIOS) компьютерной системы, установленных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="68dfe-104">The **Win32\_BIOS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the attributes of the computer system's basic input/output services (BIOS) that are installed on a computer.</span></span>

<span data-ttu-id="68dfe-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="68dfe-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="68dfe-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="68dfe-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="68dfe-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68dfe-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_BIOS : CIM_BIOSElement
{
  uint16   BiosCharacteristics[];
  string   BIOSVersion[];
  string   BuildNumber;
  string   Caption;
  string   CodeSet;
  string   CurrentLanguage;
  string   Description;
  uint8    EmbeddedControllerMajorVersion;
  uint8    EmbeddedControllerMinorVersion;
  string   IdentificationCode;
  uint16   InstallableLanguages;
  datetime InstallDate;
  string   LanguageEdition;
  String   ListOfLanguages[];
  string   Manufacturer;
  string   Name;
  string   OtherTargetOS;
  boolean  PrimaryBIOS;
  datetime ReleaseDate;
  string   SerialNumber;
  string   SMBIOSBIOSVersion;
  uint16   SMBIOSMajorVersion;
  uint16   SMBIOSMinorVersion;
  boolean  SMBIOSPresent;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  string   Status;
  uint8    SystemBiosMajorVersion;
  uint8    SystemBiosMinorVersion;
  uint16   TargetOperatingSystem;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="68dfe-108">Члены</span><span class="sxs-lookup"><span data-stu-id="68dfe-108">Members</span></span>

<span data-ttu-id="68dfe-109">Класс **Win32 \_ BIOS** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="68dfe-109">The **Win32\_BIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="68dfe-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="68dfe-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68dfe-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="68dfe-111">Properties</span></span>

<span data-ttu-id="68dfe-112">Класс **Win32 \_ BIOS** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="68dfe-112">The **Win32\_BIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68dfe-113">**биосчарактеристикс**</span><span class="sxs-lookup"><span data-stu-id="68dfe-113">**BiosCharacteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-114">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="68dfe-114">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-116">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| характеристики BIOS типа SMBIOS 0 \| ")</span><span class="sxs-lookup"><span data-stu-id="68dfe-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|BIOS Characteristics")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-117">Массив характеристик BIOS, поддерживаемых системой, как определено в справочной спецификации BIOS по управлению системой.</span><span class="sxs-lookup"><span data-stu-id="68dfe-117">Array of BIOS characteristics supported by the system as defined by the System Management BIOS Reference Specification.</span></span>

<span data-ttu-id="68dfe-118">Это значение берется из статьи **характеристики BIOS** в структуре **информации BIOS** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68dfe-118">This value comes from the **BIOS Characteristics** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="68dfe-119">Возможные значения:.</span><span class="sxs-lookup"><span data-stu-id="68dfe-119">The possible values are.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="68dfe-120"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Зарезервировано** (0)</span><span class="sxs-lookup"><span data-stu-id="68dfe-120"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="68dfe-121"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Зарезервировано** (1)</span><span class="sxs-lookup"><span data-stu-id="68dfe-121"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="68dfe-122"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="68dfe-122"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>

<span data-ttu-id="68dfe-123"><span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>**Характеристики BIOS не поддерживаются** (3)</span><span class="sxs-lookup"><span data-stu-id="68dfe-123"><span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>**BIOS Characteristics Not Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-124"><span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>**Поддерживается ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="68dfe-124"><span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>**ISA is supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-125"><span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>**Поддерживается MCA** (5)</span><span class="sxs-lookup"><span data-stu-id="68dfe-125"><span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>**MCA is supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-126"><span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>**Поддерживается EISA** (6)</span><span class="sxs-lookup"><span data-stu-id="68dfe-126"><span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>**EISA is supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-127"><span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>**Поддерживается PCI** (7)</span><span class="sxs-lookup"><span data-stu-id="68dfe-127"><span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>**PCI is supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-128"><span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>**Плата PC Card (PCMCIA) поддерживается** (8)</span><span class="sxs-lookup"><span data-stu-id="68dfe-128"><span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>**PC Card (PCMCIA) is supported** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-129"><span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>**Поддерживается Самонастраивающийся** (9)</span><span class="sxs-lookup"><span data-stu-id="68dfe-129"><span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>**Plug and Play is supported** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-130"><span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>**Поддерживается APM** (10)</span><span class="sxs-lookup"><span data-stu-id="68dfe-130"><span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>**APM is supported** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>

<span data-ttu-id="68dfe-131"><span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>Обновление **BIOS (Flash)** (11)</span><span class="sxs-lookup"><span data-stu-id="68dfe-131"><span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>**BIOS is Upgradeable (Flash)** (11)</span></span>


</dt> <dd>

<span data-ttu-id="68dfe-132">BIOS является обновляемой (Flash)</span><span class="sxs-lookup"><span data-stu-id="68dfe-132">BIOS is Upgradable (Flash)</span></span>

</dd> <dt>

<span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>

<span data-ttu-id="68dfe-133"><span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>**Разрешена теневая версия BIOS** (12)</span><span class="sxs-lookup"><span data-stu-id="68dfe-133"><span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>**BIOS shadowing is allowed** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-134"><span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>**Корпоративное лицензирование (VESA) поддерживается** (13)</span><span class="sxs-lookup"><span data-stu-id="68dfe-134"><span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>**VL-VESA is supported** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>

<span data-ttu-id="68dfe-135"><span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>**Доступна поддержка ESCD** (14)</span><span class="sxs-lookup"><span data-stu-id="68dfe-135"><span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>**ESCD support is available** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-136"><span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>**Поддерживается загрузка с компакт-диска** (15)</span><span class="sxs-lookup"><span data-stu-id="68dfe-136"><span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>**Boot from CD is supported** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-137"><span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>**Поддерживается Выборочная загрузка** (16)</span><span class="sxs-lookup"><span data-stu-id="68dfe-137"><span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>**Selectable Boot is supported** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>

<span data-ttu-id="68dfe-138"><span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>**BIOS ROM подключен к сокету** (17)</span><span class="sxs-lookup"><span data-stu-id="68dfe-138"><span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>**BIOS ROM is socketed** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-139"><span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>**Поддерживается загрузка с PC Card (PCMCIA)** (18)</span><span class="sxs-lookup"><span data-stu-id="68dfe-139"><span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>**Boot From PC Card (PCMCIA) is supported** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-140"><span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>**Поддерживается спецификация EDD (Улучшенный дисковый накопитель)** (19)</span><span class="sxs-lookup"><span data-stu-id="68dfe-140"><span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>**EDD (Enhanced Disk Drive) Specification is supported** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-141"><span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>**Int 13h — поддержка японских дискет для NEC 9800 1.2 МБ (3,5 \\ ", 1000 байт/сектор, 360 RPM)** (20)</span><span class="sxs-lookup"><span data-stu-id="68dfe-141"><span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>**Int 13h - Japanese Floppy for NEC 9800 1.2mb (3.5\\", 1k Bytes/Sector, 360 RPM) is supported** (20)</span></span>


</dt> <dd>

<span data-ttu-id="68dfe-142">Int 13h — японская дискета для NEC 9800 1.2 МБ (3,5, 1000 байт/сектор, 360 RPM)</span><span class="sxs-lookup"><span data-stu-id="68dfe-142">Int 13h - Japanese Floppy for NEC 9800 1.2mb (3.5, 1k Bytes/Sector, 360 RPM) is supported</span></span>

</dd> <dt>

<span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-143"><span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>**Int 13h — поддержка японских дискет для Toshiba 1.2 МБ (3,5 \\ ", 360 RPM)** (21)</span><span class="sxs-lookup"><span data-stu-id="68dfe-143"><span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>**Int 13h - Japanese Floppy for Toshiba 1.2mb (3.5\\", 360 RPM) is supported** (21)</span></span>


</dt> <dd>

<span data-ttu-id="68dfe-144">Int 13h — поддержка японских дискет для Toshiba 1.2 МБ (3,5, 360 RPM)</span><span class="sxs-lookup"><span data-stu-id="68dfe-144">Int 13h - Japanese Floppy for Toshiba 1.2mb (3.5, 360 RPM) is supported</span></span>

</dd> <dt>

<span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="68dfe-145"><span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h — 5,25 \\ "/360 КБ поддерживаются гибкие службы** (22)</span><span class="sxs-lookup"><span data-stu-id="68dfe-145"><span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 5.25\\" / 360 KB Floppy Services are supported** (22)</span></span>


</dt> <dd>

<span data-ttu-id="68dfe-146">Int 13h — поддерживаются гибкие службы 5,25/360 КБ</span><span class="sxs-lookup"><span data-stu-id="68dfe-146">Int 13h - 5.25 / 360 KB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="68dfe-147"><span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h — 5,25 \\ "поддерживаются гибкие службы/1.2MB** (23)</span><span class="sxs-lookup"><span data-stu-id="68dfe-147"><span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 5.25\\" /1.2MB Floppy Services are supported** (23)</span></span>


</dt> <dd>

<span data-ttu-id="68dfe-148">Int 13h — 5,25. поддерживаются гибкие службы/1.2MB.</span><span class="sxs-lookup"><span data-stu-id="68dfe-148">Int 13h - 5.25 /1.2MB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>

<span data-ttu-id="68dfe-149"><span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>**Int 13h — 3,5 \\ "/720 КБ поддерживаются гибкие службы** (24)</span><span class="sxs-lookup"><span data-stu-id="68dfe-149"><span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>**Int 13h - 3.5\\" / 720 KB Floppy Services are supported** (24)</span></span>


</dt> <dd>

<span data-ttu-id="68dfe-150">Int 13h — поддерживаются гибкие службы 3,5/720 КБ</span><span class="sxs-lookup"><span data-stu-id="68dfe-150">Int 13h - 3.5 / 720 KB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="68dfe-151"><span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h — 3,5 \\ "/2,88 МБ. поддерживаются гибкие службы** (25)</span><span class="sxs-lookup"><span data-stu-id="68dfe-151"><span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 3.5\\" / 2.88 MB Floppy Services are supported** (25)</span></span>


</dt> <dd>

<span data-ttu-id="68dfe-152">Int 13h — поддерживаются гибкие службы 3,5/2,88 МБ</span><span class="sxs-lookup"><span data-stu-id="68dfe-152">Int 13h - 3.5 / 2.88 MB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-153"><span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>**Int 5H, служба экрана печати поддерживается** (26)</span><span class="sxs-lookup"><span data-stu-id="68dfe-153"><span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>**Int 5h, Print Screen Service is supported** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="68dfe-154"><span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>**Int 9h, 8042 службы клавиатуры поддерживаются** (27)</span><span class="sxs-lookup"><span data-stu-id="68dfe-154"><span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>**Int 9h, 8042 Keyboard services are supported** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="68dfe-155"><span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>**Int 14h, последовательные службы поддерживаются** (28)</span><span class="sxs-lookup"><span data-stu-id="68dfe-155"><span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>**Int 14h, Serial Services are supported** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="68dfe-156"><span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>**Int 17h, службы принтера поддерживаются** (29)</span><span class="sxs-lookup"><span data-stu-id="68dfe-156"><span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>**Int 17h, printer services are supported** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="68dfe-157"><span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>**Int 10h, КГА/Mono Video Services поддерживаются** (30)</span><span class="sxs-lookup"><span data-stu-id="68dfe-157"><span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>**Int 10h, CGA/Mono Video Services are supported** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC_PC-98"></span><span id="nec_pc-98"></span>

<span data-ttu-id="68dfe-158"><span id="NEC_PC-98"></span><span id="nec_pc-98"></span>**NEC PC-98** (31)</span><span class="sxs-lookup"><span data-stu-id="68dfe-158"><span id="NEC_PC-98"></span><span id="nec_pc-98"></span>**NEC PC-98** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>

<span data-ttu-id="68dfe-159"><span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>**Поддерживается ACPI** (32)</span><span class="sxs-lookup"><span data-stu-id="68dfe-159"><span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>**ACPI supported** (32)</span></span>


</dt> <dd>

<span data-ttu-id="68dfe-160">Поддерживается ACPI</span><span class="sxs-lookup"><span data-stu-id="68dfe-160">ACPI is supported</span></span>

</dd> <dt>

<span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-161"><span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>**Поддерживается устаревшая поддержка USB** (33)</span><span class="sxs-lookup"><span data-stu-id="68dfe-161"><span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>**USB Legacy is supported** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-162"><span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>**Поддерживается AGP** (34)</span><span class="sxs-lookup"><span data-stu-id="68dfe-162"><span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>**AGP is supported** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-163"><span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>**Поддерживается загрузка с поддержкой I2O** (35)</span><span class="sxs-lookup"><span data-stu-id="68dfe-163"><span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>**I2O boot is supported** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-164"><span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>**Поддержка загрузки Ls-120** (36)</span><span class="sxs-lookup"><span data-stu-id="68dfe-164"><span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>**LS-120 boot is supported** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-165"><span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>**Поддерживается загрузка ATAPI ZIP Drive** (37)</span><span class="sxs-lookup"><span data-stu-id="68dfe-165"><span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>**ATAPI ZIP Drive boot is supported** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="68dfe-166"><span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>**1394. поддерживается загрузка** (38)</span><span class="sxs-lookup"><span data-stu-id="68dfe-166"><span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>**1394 boot is supported** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>

<span data-ttu-id="68dfe-167"><span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>**Поддержка интеллектуального аккумулятора** (39)</span><span class="sxs-lookup"><span data-stu-id="68dfe-167"><span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>**Smart Battery supported** (39)</span></span>


</dt> <dd>

<span data-ttu-id="68dfe-168">Поддерживается интеллектуальный аккумулятор</span><span class="sxs-lookup"><span data-stu-id="68dfe-168">Smart Battery is supported</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-169">40 47</span><span class="sxs-lookup"><span data-stu-id="68dfe-169">40 47</span></span>
</dt> <dd>

<span data-ttu-id="68dfe-170">Зарезервировано для поставщика BIOS</span><span class="sxs-lookup"><span data-stu-id="68dfe-170">Reserved for BIOS vendor</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-171">48 63</span><span class="sxs-lookup"><span data-stu-id="68dfe-171">48 63</span></span>
</dt> <dd>

<span data-ttu-id="68dfe-172">Зарезервировано для поставщика системы</span><span class="sxs-lookup"><span data-stu-id="68dfe-172">Reserved for system vendor</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="68dfe-173">**биосверсион**</span><span class="sxs-lookup"><span data-stu-id="68dfe-173">**BIOSVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-174">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="68dfe-174">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-176">Массив полной информации о BIOS System.</span><span class="sxs-lookup"><span data-stu-id="68dfe-176">Array of the complete system BIOS information.</span></span> <span data-ttu-id="68dfe-177">На многих компьютерах может быть несколько строк версии, которые хранятся в реестре и представляют сведения о системе BIOS.</span><span class="sxs-lookup"><span data-stu-id="68dfe-177">In many computers there can be several version strings that are stored in the registry and represent the system BIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-178">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="68dfe-178">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68dfe-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-181">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="68dfe-181">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-182">Внутренний идентификатор для этой компиляции этого программного элемента.</span><span class="sxs-lookup"><span data-stu-id="68dfe-182">Internal identifier for this compilation of this software element.</span></span>

<span data-ttu-id="68dfe-183">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="68dfe-183">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-184">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="68dfe-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68dfe-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-187">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="68dfe-187">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-188">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="68dfe-188">Short description of the object a one-line string.</span></span>

<span data-ttu-id="68dfe-189">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68dfe-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-190">**Исходный код**</span><span class="sxs-lookup"><span data-stu-id="68dfe-190">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-191">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68dfe-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-193">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="68dfe-193">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-194">Набор кодов, используемый этим программным элементом.</span><span class="sxs-lookup"><span data-stu-id="68dfe-194">Code set used by this software element.</span></span>

<span data-ttu-id="68dfe-195">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="68dfe-195">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-196">**куррентлангуаже**</span><span class="sxs-lookup"><span data-stu-id="68dfe-196">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68dfe-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-199">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 13 \| текущий язык")</span><span class="sxs-lookup"><span data-stu-id="68dfe-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 13\|Current Language")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-200">Имя текущего языка BIOS.</span><span class="sxs-lookup"><span data-stu-id="68dfe-200">Name of the current BIOS language.</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-201">**Описание**</span><span class="sxs-lookup"><span data-stu-id="68dfe-201">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-202">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68dfe-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-204">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="68dfe-204">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-205">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="68dfe-205">Description of the object.</span></span>

<span data-ttu-id="68dfe-206">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68dfe-206">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-207">**ембеддедконтроллермажорверсион**</span><span class="sxs-lookup"><span data-stu-id="68dfe-207">**EmbeddedControllerMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-208">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="68dfe-208">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-210">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| основной выпуск встроенного по контроллера SMBIOS 0)</span><span class="sxs-lookup"><span data-stu-id="68dfe-210">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|Embedded Controller Firmware Major Release")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-211">Основной выпуск встроенного по контроллера встроенного по.</span><span class="sxs-lookup"><span data-stu-id="68dfe-211">The major release of the embedded controller firmware.</span></span>

<span data-ttu-id="68dfe-212">Это значение берется из **основного выпуска встроенного по контроллера** в структуре **информации BIOS** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68dfe-212">This value comes from the **Embedded Controller Firmware Major Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="68dfe-213">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="68dfe-213">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-214">**ембеддедконтроллерминорверсион**</span><span class="sxs-lookup"><span data-stu-id="68dfe-214">**EmbeddedControllerMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-215">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="68dfe-215">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-216">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-217">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 0. \| дополнительный выпуск встроенного по контроллера")</span><span class="sxs-lookup"><span data-stu-id="68dfe-217">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|Embedded Controller Firmware Minor Release")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-218">Дополнительный выпуск встроенного по контроллера встроенного по.</span><span class="sxs-lookup"><span data-stu-id="68dfe-218">The minor release of the embedded controller firmware.</span></span>

<span data-ttu-id="68dfe-219">Это значение берется из **вспомогательного выпуска встроенного по контроллера** в структуре **информации о BIOS** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68dfe-219">This value comes from the **Embedded Controller Firmware Minor Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="68dfe-220">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="68dfe-220">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-221">**идентификатионкоде**</span><span class="sxs-lookup"><span data-stu-id="68dfe-221">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-222">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68dfe-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-224">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="68dfe-224">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-225">Идентификатор изготовителя для этого программного элемента.</span><span class="sxs-lookup"><span data-stu-id="68dfe-225">Manufacturer's identifier for this software element.</span></span> <span data-ttu-id="68dfe-226">Часто это будет единицей складского учета (SKU) или номером части.</span><span class="sxs-lookup"><span data-stu-id="68dfe-226">Often this will be a stock keeping unit (SKU) or a part number.</span></span>

<span data-ttu-id="68dfe-227">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="68dfe-227">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-228">**инсталлаблелангуажес**</span><span class="sxs-lookup"><span data-stu-id="68dfe-228">**InstallableLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-229">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68dfe-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-231">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 13, \| устанавливаемые языки")</span><span class="sxs-lookup"><span data-stu-id="68dfe-231">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 13\|Installable Languages")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-232">Число языков, доступных для установки в этой системе.</span><span class="sxs-lookup"><span data-stu-id="68dfe-232">Number of languages available for installation on this system.</span></span> <span data-ttu-id="68dfe-233">Язык может определять такие свойства, как необходимость в Юникоде и двунаправленном тексте.</span><span class="sxs-lookup"><span data-stu-id="68dfe-233">Language may determine properties such as the need for Unicode and bidirectional text.</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-234">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="68dfe-234">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-235">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="68dfe-235">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-236">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-237">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="68dfe-237">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-238">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="68dfe-238">Date and time the object was installed.</span></span> <span data-ttu-id="68dfe-239">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="68dfe-239">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="68dfe-240">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68dfe-240">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-241">**лангуажеедитион**</span><span class="sxs-lookup"><span data-stu-id="68dfe-241">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-242">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68dfe-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-244">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="68dfe-244">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-245">Языковой выпуск этого программного элемента.</span><span class="sxs-lookup"><span data-stu-id="68dfe-245">Language edition of this software element.</span></span> <span data-ttu-id="68dfe-246">Следует использовать коды языков, определенные в стандарте ISO 639.</span><span class="sxs-lookup"><span data-stu-id="68dfe-246">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="68dfe-247">Если программный элемент представляет многоязычную или международную версию продукта, следует использовать строку "многоязычный".</span><span class="sxs-lookup"><span data-stu-id="68dfe-247">Where the software element represents a multilingual or international version of a product, the string "multilingual" should be used.</span></span>

<span data-ttu-id="68dfe-248">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="68dfe-248">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-249">**листофлангуажес**</span><span class="sxs-lookup"><span data-stu-id="68dfe-249">**ListOfLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-250">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="68dfe-250">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-251">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-252">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 13 \| строк языка")</span><span class="sxs-lookup"><span data-stu-id="68dfe-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 13\|Language Strings")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-253">Массив имен доступных для установки языков с BIOS.</span><span class="sxs-lookup"><span data-stu-id="68dfe-253">Array of names of available BIOS-installable languages.</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-254">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="68dfe-254">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-255">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68dfe-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-257">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -система BIOS \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="68dfe-257">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-258">Изготовитель программного элемента.</span><span class="sxs-lookup"><span data-stu-id="68dfe-258">Manufacturer of this software element.</span></span>

<span data-ttu-id="68dfe-259">Это значение берется из элемента **Vendor** структуры сведений о **BIOS** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68dfe-259">This value comes from the **Vendor** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="68dfe-260">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="68dfe-260">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-261">**Name**</span><span class="sxs-lookup"><span data-stu-id="68dfe-261">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-262">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68dfe-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-264">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="68dfe-264">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-265">Имя, используемое для распознавания этого программного элемента.</span><span class="sxs-lookup"><span data-stu-id="68dfe-265">Name used to identify this software element.</span></span>

<span data-ttu-id="68dfe-266">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68dfe-266">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-267">**осертаржетос**</span><span class="sxs-lookup"><span data-stu-id="68dfe-267">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-268">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68dfe-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-269">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-270">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**модель \_ CIM**](cim-operatingsystem.md).**Осертипедескриптион**")</span><span class="sxs-lookup"><span data-stu-id="68dfe-270">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-271">Записывает изготовитель и тип операционной системы для программного элемента, если свойство **таржетоператингсистем** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="68dfe-271">Records the manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 (Other).</span></span> <span data-ttu-id="68dfe-272">Если **таржетоператингсистем** имеет значение 1, **осертаржетос** должно иметь значение, не равное NULL.</span><span class="sxs-lookup"><span data-stu-id="68dfe-272">When **TargetOperatingSystem** has a value of 1, **OtherTargetOS** must have a nonnull value.</span></span> <span data-ttu-id="68dfe-273">Для всех остальных значений параметра **таржетоператингсистем** **Осертаржетос** имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="68dfe-273">For all other values of **TargetOperatingSystem**, **OtherTargetOS** is **NULL**.</span></span>

<span data-ttu-id="68dfe-274">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="68dfe-274">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-275">**примарибиос**</span><span class="sxs-lookup"><span data-stu-id="68dfe-275">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-276">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="68dfe-276">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-277">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-278">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -система BIOS \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="68dfe-278">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-279">Если **значение равно true**, это основная BIOS компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="68dfe-279">If **TRUE**, this is the primary BIOS of the computer system.</span></span>

<span data-ttu-id="68dfe-280">Это свойство наследуется от [**CIM \_ биоселемент**](cim-bioselement.md).</span><span class="sxs-lookup"><span data-stu-id="68dfe-280">This property is inherited from [**CIM\_BIOSElement**](cim-bioselement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-281">**ReleaseDate**</span><span class="sxs-lookup"><span data-stu-id="68dfe-281">**ReleaseDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-282">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="68dfe-282">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-284">Дата выпуска Windows BIOS в формате UTC для YYYYMMDDHHMMSS. ММММММ (+-) OOO.</span><span class="sxs-lookup"><span data-stu-id="68dfe-284">Release date of the Windows BIOS in the Coordinated Universal Time (UTC) format of YYYYMMDDHHMMSS.MMMMMM(+-)OOO.</span></span>

<span data-ttu-id="68dfe-285">Это значение берется из статьи " **Дата выпуска BIOS** " в структуре **сведений о BIOS** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68dfe-285">This value comes from the **BIOS Release Date** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-286">**Номер**</span><span class="sxs-lookup"><span data-stu-id="68dfe-286">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-287">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68dfe-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-289">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Значение ComponentID \| 001,4 в DMTF</span><span class="sxs-lookup"><span data-stu-id="68dfe-289">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-290">Назначенный серийный номер программного элемента.</span><span class="sxs-lookup"><span data-stu-id="68dfe-290">Assigned serial number of the software element.</span></span>

<span data-ttu-id="68dfe-291">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="68dfe-291">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-292">**смбиосбиосверсион**</span><span class="sxs-lookup"><span data-stu-id="68dfe-292">**SMBIOSBIOSVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-293">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68dfe-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-295">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 0 \| версия BIOS")</span><span class="sxs-lookup"><span data-stu-id="68dfe-295">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|BIOS Version")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-296">Версия BIOS, сообщаемая SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68dfe-296">BIOS version as reported by SMBIOS.</span></span>

<span data-ttu-id="68dfe-297">Это значение берется из раздела **версия BIOS** в структуре **сведений о BIOS** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68dfe-297">This value comes from the **BIOS Version** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-298">**смбиосмажорверсион**</span><span class="sxs-lookup"><span data-stu-id="68dfe-298">**SMBIOSMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-299">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68dfe-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-301">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| ксмбиос- \| Version")</span><span class="sxs-lookup"><span data-stu-id="68dfe-301">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|CSMBios\|GetVersion")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-302">Основной номер версии SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68dfe-302">Major SMBIOS version number.</span></span> <span data-ttu-id="68dfe-303">Это свойство имеет **значение NULL** , если SMBIOS не найдена.</span><span class="sxs-lookup"><span data-stu-id="68dfe-303">This property is **NULL** if SMBIOS is not found.</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-304">**смбиосминорверсион**</span><span class="sxs-lookup"><span data-stu-id="68dfe-304">**SMBIOSMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-305">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68dfe-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-307">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| ксмбиос- \| Version")</span><span class="sxs-lookup"><span data-stu-id="68dfe-307">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|CSMBios\|GetVersion")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-308">Дополнительный номер версии SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68dfe-308">Minor SMBIOS version number.</span></span> <span data-ttu-id="68dfe-309">Это свойство имеет **значение NULL** , если SMBIOS не найдена.</span><span class="sxs-lookup"><span data-stu-id="68dfe-309">This property is **NULL** if SMBIOS is not found.</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-310">**смбиоспресент**</span><span class="sxs-lookup"><span data-stu-id="68dfe-310">**SMBIOSPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-311">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="68dfe-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-312">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-313">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| ксмбиос \| init")</span><span class="sxs-lookup"><span data-stu-id="68dfe-313">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|CSMBios\|Init")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-314">Если задано **значение true**, SMBIOS доступна на этой компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="68dfe-314">If **true**, the SMBIOS is available on this computer system.</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-315">**софтварилементид**</span><span class="sxs-lookup"><span data-stu-id="68dfe-315">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-316">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68dfe-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-318">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="68dfe-318">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-319">Идентификатор для этого программного элемента; предназначен для использования совместно с другими ключами для создания уникального представления этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="68dfe-319">Identifier for this software element; designed to be used in conjunction with other keys to create a unique representation of this instance.</span></span>

<span data-ttu-id="68dfe-320">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="68dfe-320">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-321">**софтварилементстате**</span><span class="sxs-lookup"><span data-stu-id="68dfe-321">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-322">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68dfe-322">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-324">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="68dfe-324">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-325">Состояние программного элемента.</span><span class="sxs-lookup"><span data-stu-id="68dfe-325">State of a software element.</span></span>

<span data-ttu-id="68dfe-326">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="68dfe-326">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="68dfe-327">Возможные значения:.</span><span class="sxs-lookup"><span data-stu-id="68dfe-327">The possible values are.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="68dfe-328">**Развертывание** (0)</span><span class="sxs-lookup"><span data-stu-id="68dfe-328">**Deployable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="68dfe-329">**Устанавливаемый** (1)</span><span class="sxs-lookup"><span data-stu-id="68dfe-329">**Installable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="68dfe-330">**Исполняемый файл** (2)</span><span class="sxs-lookup"><span data-stu-id="68dfe-330">**Executable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="68dfe-331">**Работает** (3)</span><span class="sxs-lookup"><span data-stu-id="68dfe-331">**Running** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="68dfe-332">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="68dfe-332">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-333">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68dfe-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-334">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-335">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="68dfe-335">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-336">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="68dfe-336">Current status of the object.</span></span> <span data-ttu-id="68dfe-337">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="68dfe-337">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="68dfe-338">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="68dfe-338">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="68dfe-339">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="68dfe-339">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="68dfe-340">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="68dfe-340">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="68dfe-341">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="68dfe-341">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="68dfe-342">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68dfe-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="68dfe-343">Возможные значения:.</span><span class="sxs-lookup"><span data-stu-id="68dfe-343">The possible values are.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="68dfe-344">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="68dfe-344">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="68dfe-345">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="68dfe-345">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="68dfe-346">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="68dfe-346">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="68dfe-347">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="68dfe-347">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="68dfe-348">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="68dfe-348">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="68dfe-349">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="68dfe-349">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="68dfe-350">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="68dfe-350">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="68dfe-351">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="68dfe-351">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="68dfe-352">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="68dfe-352">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="68dfe-353">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="68dfe-353">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="68dfe-354">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="68dfe-354">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="68dfe-355">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="68dfe-355">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="68dfe-356">**систембиосмажорверсион**</span><span class="sxs-lookup"><span data-stu-id="68dfe-356">**SystemBiosMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-357">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="68dfe-357">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-358">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-359">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| основной выпуск SMBIOS 0 System BIOS")</span><span class="sxs-lookup"><span data-stu-id="68dfe-359">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|System BIOS Major Release")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-360">Основной выпуск BIOS системы.</span><span class="sxs-lookup"><span data-stu-id="68dfe-360">The major release of the System BIOS.</span></span>

<span data-ttu-id="68dfe-361">Это значение берется из **основного выпуска BIOS** в структуре **информации о BIOS** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68dfe-361">This value comes from the **System BIOS Major Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="68dfe-362">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="68dfe-362">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-363">**систембиосминорверсион**</span><span class="sxs-lookup"><span data-stu-id="68dfe-363">**SystemBiosMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-364">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="68dfe-364">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-365">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-366">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 0. \| дополнительный выпуск BIOS системы")</span><span class="sxs-lookup"><span data-stu-id="68dfe-366">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|System BIOS Minor Release")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-367">Дополнительный выпуск BIOS системы.</span><span class="sxs-lookup"><span data-stu-id="68dfe-367">The minor release of the System BIOS.</span></span>

<span data-ttu-id="68dfe-368">Это значение берется из раздела " **дополнительный выпуск системной BIOS** " в структуре **информации о BIOS** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68dfe-368">This value comes from the **System BIOS Minor Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="68dfe-369">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="68dfe-369">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="68dfe-370">**таржетоператингсистем**</span><span class="sxs-lookup"><span data-stu-id="68dfe-370">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-371">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68dfe-371">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-372">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-373">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Сведения о программном компоненте DMTF \| 002,5 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**модель CIM \_**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="68dfe-373">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-374">Целевая операционная система программного элемента-владельца.</span><span class="sxs-lookup"><span data-stu-id="68dfe-374">Target operating system of the owning software element.</span></span>

<span data-ttu-id="68dfe-375">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="68dfe-375">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="68dfe-376">Возможные значения:.</span><span class="sxs-lookup"><span data-stu-id="68dfe-376">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="68dfe-377">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="68dfe-377">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="68dfe-378">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="68dfe-378">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="68dfe-379">**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="68dfe-379">**MACOS** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="68dfe-380">**Аттуникс** (3)</span><span class="sxs-lookup"><span data-stu-id="68dfe-380">**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="68dfe-381">**Дгукс** (4)</span><span class="sxs-lookup"><span data-stu-id="68dfe-381">**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="68dfe-382">**Декнт** (5)</span><span class="sxs-lookup"><span data-stu-id="68dfe-382">**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="68dfe-383">**Цифровая UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="68dfe-383">**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="68dfe-384">**Опенвмс** (7)</span><span class="sxs-lookup"><span data-stu-id="68dfe-384">**OpenVMS** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="68dfe-385">**Hpux** (8)</span><span class="sxs-lookup"><span data-stu-id="68dfe-385">**HPUX** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="68dfe-386">**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="68dfe-386">**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="68dfe-387">**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="68dfe-387">**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="68dfe-388">**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="68dfe-388">**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="68dfe-389">**ОС/2** (12)</span><span class="sxs-lookup"><span data-stu-id="68dfe-389">**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="68dfe-390">**Жававм** (13)</span><span class="sxs-lookup"><span data-stu-id="68dfe-390">**JavaVM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="68dfe-391">**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="68dfe-391">**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="68dfe-392">**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="68dfe-392">**WIN3x** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="68dfe-393">**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="68dfe-393">**WIN95** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="68dfe-394">**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="68dfe-394">**WIN98** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="68dfe-395">**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="68dfe-395">**WINNT** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="68dfe-396">**Wince** (19)</span><span class="sxs-lookup"><span data-stu-id="68dfe-396">**WINCE** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="68dfe-397">**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="68dfe-397">**NCR3000** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="68dfe-398">**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="68dfe-398">**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="68dfe-399">**Использование** (22)</span><span class="sxs-lookup"><span data-stu-id="68dfe-399">**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="68dfe-400">**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="68dfe-400">**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="68dfe-401">**Зависящая от UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="68dfe-401">**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="68dfe-402">**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="68dfe-402">**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="68dfe-403">**SCO опенсервер** (26)</span><span class="sxs-lookup"><span data-stu-id="68dfe-403">**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="68dfe-404">**Секуент** (27)</span><span class="sxs-lookup"><span data-stu-id="68dfe-404">**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="68dfe-405">**Ирикс** (28)</span><span class="sxs-lookup"><span data-stu-id="68dfe-405">**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="68dfe-406">**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="68dfe-406">**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="68dfe-407">**Сунос** (30)</span><span class="sxs-lookup"><span data-stu-id="68dfe-407">**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="68dfe-408">**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="68dfe-408">**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="68dfe-409">**Асериес** (32)</span><span class="sxs-lookup"><span data-stu-id="68dfe-409">**ASERIES** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="68dfe-410">**Тандемнск** (33)</span><span class="sxs-lookup"><span data-stu-id="68dfe-410">**TandemNSK** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="68dfe-411">**Тандемнт** (34)</span><span class="sxs-lookup"><span data-stu-id="68dfe-411">**TandemNT** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="68dfe-412">**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="68dfe-412">**BS2000** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="68dfe-413">**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="68dfe-413">**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="68dfe-414">**Линкс** (37)</span><span class="sxs-lookup"><span data-stu-id="68dfe-414">**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="68dfe-415">**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="68dfe-415">**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="68dfe-416">**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="68dfe-416">**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="68dfe-417">**Интерактивная UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="68dfe-417">**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="68dfe-418">**Бсдуникс** (41)</span><span class="sxs-lookup"><span data-stu-id="68dfe-418">**BSDUNIX** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="68dfe-419">**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="68dfe-419">**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="68dfe-420">**Нетбсд** (43)</span><span class="sxs-lookup"><span data-stu-id="68dfe-420">**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="68dfe-421">**GNU Хурд** (44)</span><span class="sxs-lookup"><span data-stu-id="68dfe-421">**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="68dfe-422">**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="68dfe-422">**OS9** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="68dfe-423">**Ядро машинного ядра** (46)</span><span class="sxs-lookup"><span data-stu-id="68dfe-423">**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="68dfe-424">**Inferno адский** (47)</span><span class="sxs-lookup"><span data-stu-id="68dfe-424">**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="68dfe-425">**Кнкс** (48)</span><span class="sxs-lookup"><span data-stu-id="68dfe-425">**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="68dfe-426">**Епок** (49)</span><span class="sxs-lookup"><span data-stu-id="68dfe-426">**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="68dfe-427">**Иксворкс** (50)</span><span class="sxs-lookup"><span data-stu-id="68dfe-427">**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="68dfe-428">**Вксворкс** (51)</span><span class="sxs-lookup"><span data-stu-id="68dfe-428">**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="68dfe-429">**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="68dfe-429">**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="68dfe-430">**Беос** (53)</span><span class="sxs-lookup"><span data-stu-id="68dfe-430">**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="68dfe-431">**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="68dfe-431">**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="68dfe-432">**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="68dfe-432">**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="68dfe-433">**Палмпилот** (56)</span><span class="sxs-lookup"><span data-stu-id="68dfe-433">**PalmPilot** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="68dfe-434">**Рапсодии** (57)</span><span class="sxs-lookup"><span data-stu-id="68dfe-434">**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="68dfe-435">**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="68dfe-435">**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="68dfe-436">**Выделенный** (59)</span><span class="sxs-lookup"><span data-stu-id="68dfe-436">**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="68dfe-437">**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="68dfe-437">**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="68dfe-438">**ТПФ** (61)</span><span class="sxs-lookup"><span data-stu-id="68dfe-438">**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="68dfe-439">**Version**</span><span class="sxs-lookup"><span data-stu-id="68dfe-439">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68dfe-440">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68dfe-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-441">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68dfe-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68dfe-442">Квалификаторы: [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("версия"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| оборудования \\ \\ Описание \\ \\ системы \| систембиосверсион")</span><span class="sxs-lookup"><span data-stu-id="68dfe-442">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HARDWARE\\\\Description\\\\System\|SystemBiosVersion")</span></span>
</dt> </dl>

<span data-ttu-id="68dfe-443">Версия BIOS.</span><span class="sxs-lookup"><span data-stu-id="68dfe-443">Version of the BIOS.</span></span> <span data-ttu-id="68dfe-444">Эта строка создается изготовителем BIOS.</span><span class="sxs-lookup"><span data-stu-id="68dfe-444">This string is created by the BIOS manufacturer.</span></span>

<span data-ttu-id="68dfe-445">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="68dfe-445">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68dfe-446">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68dfe-446">Remarks</span></span>

<span data-ttu-id="68dfe-447">Класс **Win32 \_ BIOS** является производным от [**CIM \_ биоселемент**](cim-bioselement.md).</span><span class="sxs-lookup"><span data-stu-id="68dfe-447">The **Win32\_BIOS** class is derived from [**CIM\_BIOSElement**](cim-bioselement.md).</span></span>

<span data-ttu-id="68dfe-448">Свойства в классе **Win32 \_ BIOS** могут изменяться для определенной компьютерной системы, имеющей ту же самую версию BIOS, например загрузку с использованием устаревшего режима BIOS и загрузки через режим BIOS UEFI.</span><span class="sxs-lookup"><span data-stu-id="68dfe-448">The properties in the **Win32\_BIOS** class may change for a specific computer system with the same BIOS, for example booting through a legacy BIOS mode vs. booting through UEFI BIOS mode.</span></span> <span data-ttu-id="68dfe-449">Однако свойства, полученные из структур SMBIOS, должны остаться прежними.</span><span class="sxs-lookup"><span data-stu-id="68dfe-449">However the properties retrieved from the SMBIOS structures should remain the same.</span></span>

## <a name="examples"></a><span data-ttu-id="68dfe-450">Примеры</span><span class="sxs-lookup"><span data-stu-id="68dfe-450">Examples</span></span>

<span data-ttu-id="68dfe-451">Пример " [Get-компутеринфо-запрос компьютера с локального/удаленного компьютера" (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell в коллекции TechNet использует несколько вызовов оборудования и программного обеспечения, включая **Win32 \_ BIOS**, для вывода сведений о локальной или удаленной системе.</span><span class="sxs-lookup"><span data-stu-id="68dfe-451">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_BIOS**, to display information about a local or remote system.</span></span>

<span data-ttu-id="68dfe-452">Образец VBScript " [Создание системной информации как XML-иерархии](https://Gallery.TechNet.Microsoft.Com/Generate-system-information-3f40629f) " в коллекции TechNet использует ряд вызовов к оборудованию и программному обеспечению, включая **Win32 \_ BIOS**, для создания XML-представления системы с помощью вывода XML вручную.</span><span class="sxs-lookup"><span data-stu-id="68dfe-452">The [Generate system information as XML hierarchy](https://Gallery.TechNet.Microsoft.Com/Generate-system-information-3f40629f) VBScript sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_BIOS**, to generate an XML representation of a system using a manual XML output.</span></span>

<span data-ttu-id="68dfe-453">В следующем примере кода PowerShell для возврата характеристик BIOS используется **Win32 \_ BIOS** .</span><span class="sxs-lookup"><span data-stu-id="68dfe-453">The following PowerShell code sample uses **Win32\_BIOS** to return characteristics of the BIOS</span></span>


```PowerShell
# wmi-win32_bios.ps1
# Demonstrates use of Win32_Bios WMI class
# Thomas Lee - tfl@psp.co.uk



# Helper function to return characterics of the BIOS
function get-WmiBiosCharacteristics {
param ([uint16] $char)

# parse and return values

If ($char -le 39) {

switch ($char) {
0   {"00-Reserved"}
1   {"01-Reserved"}
2   {"02-Unknown"}
3   {"03-BIOS Characteristics Not Supported"}
4   {"04-ISA is supported"}
5   {"05-MCA is supported"}
6   {"06-EISA is supported"}
7   {"07-PCI is supported"}
8   {"08-PC Card (PCMCIA) is supported"}
9   {"09-Plug and Play is supported"}
10  {"10-APM is supported"}
11  {"11-BIOS is Upgradable (Flash)"}
12  {"12-BIOS shadowing is allowed"}
13  {"13-VL-VESA is supported"}
14  {"14-ESCD support is available"}
15  {"15-Boot from CD is supported"}
16  {"16-Selectable Boot is supported"}
17  {"17-BIOS ROM is socketed"}
18  {"18-Boot From PC Card (PCMCIA) is supported"}
19  {"19-EDD (Enhanced Disk Drive) Specification is supported"}
20  {"20-Int 13h - Japanese Floppy for NEC 9800 1.2mb (3.5, 1k Bytes/Sector, 360 RPM) is supported"}
21  {"21-Int 13h - Japanese Floppy for Toshiba 1.2mb (3.5, 360 RPM) is supported"}
22  {"22-Int 13h - 5.25 / 360 KB Floppy Services are supported"}
23  {"23-Int 13h - 5.25 /1.2MB Floppy Services are supported"}
24  {"24-Int 13h - 3.5 / 720 KB Floppy Services are supported"}
25  {"25-Int 13h - 3.5 / 2.88 MB Floppy Services are supported"}
26  {"26-Int 5h, Print Screen Service is supported"}
27  {"27-Int 9h, 8042 Keyboard services are supported"}
28  {"28-Int 14h, Serial Services are supported"}
29  {"29-Int 17h, printer services are supported"}
30  {"30-Int 10h, CGA/Mono Video Services are supported"}
31  {"31-NEC PC-98"}
32  {"32-ACPI supported"}
33  {"33-USB Legacy is supported"}
34  {"34-AGP is supported"}
35  {"35-I2O boot is supported"}
36  {"36-LS-120 boot is supported"}
37  {"37-ATAPI ZIP Drive boot is supported"}
38  {"38-1394 boot is supported"}
39  {"39-Smart Battery supported"}
}
Return
}

If ($char -ge 40 -and $char -le 45) {
          "{0}-Reserved for BIOS vendor" -f $char
return
}

If ($char -ge 48 -and $char -le 63) {
           "{0}-Reserved for system vendor" -f $char
return
}
"{0}-Unknown Value " -f $char
}

# Get BIOS information from WMI
$bios = Get-WMIObject Win32_Bios

# Display BIOS Details
"Win32_Bios WMI Information"
"Bios Characteristics"
foreach ($ch in $bios.BiosCharacteristics) {
"                      :  {0}" -f  (Get-WmiBiosCharacteristics($ch))
} 
"Bios Version          :  {0}" -f $bios.BiosVersion
"Codeset               :  {0}" -f $bios.Codeset
"CurrentLanguage       :  {0}" -f $bios.CurrentLanguage
"Description           :  {0}" -f $bios.Description
"IdentificatonCode     :  {0}" -f $bios.IdentificatonCode
"InstallableLanguages  :  {0}" -f $bios.InstallableLanguages
"InstallDate           :  {0}" -f $bios.InstallDate 
"LanguageEdition       :  {0}" -f $bios.LanguageEdition
"ListOfLanguages       :  {0}" -f $bios.ListOfLanguages
"Manufacturer          :  {0}" -f $bios.Manufacturer
"OtherTargetOS         :  {0}" -f $bios.OtherTargetOS
"PrimaryBIOS           :  {0}" -f $bios.PrimaryBIOS
"ReleaseDate           :  {0}" -f $bios.ReleaseDate
"SerialNumber          :  {0}" -f $bios.SerialNumber
"SMBIOSBIOSVersion     :  {0}" -f $bios.SMBIOSBIOSVersion
"SMBIOSMajorVersion    :  {0}" -f $bios.SMBIOSMajorVersion
"SMBIOSMinorVersion    :  {0}" -f $bios.SMBIOSMinorVersion
"SoftwareElementID     :  {0}" -f $bios.SoftwareElementID 
"SoftwareElementState  :  {0}" -f $bios.SoftwareElementState
"TargetOperatingSystem :  {0}" -f $bios.TargetOperatingSystem
"Version               :  {0}" -f $bios.Version 
```



<span data-ttu-id="68dfe-454">Предыдущий пример кода возвращает следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="68dfe-454">The previous code sample returns the following information:</span></span>

``` syntax
Win32_Bios WMI Information
Bios Characteristics
                      :  04-ISA is supported
                      :  07-PCI is supported
                      :  08-PC Card (PCMCIA) is supported
                      :  09-Plug and Play is supported
                      :  11-BIOS is Upgradable (Flash)
                      :  12-BIOS shadowing is allowed
                      :  15-Boot from CD is supported
                      :  16-Selectable Boot is supported
                      :  24-Int 13h - 3.5 / 720 KB Floppy Services are supported
                      :  26-Int 5h, Print Screen Service is supported
                      :  27-Int 9h, 8042 Keyboard services are supported
                      :  28-Int 14h, Serial Services are supported
                      :  29-Int 17h, printer services are supported
                      :  30-Int 10h, CGA/Mono Video Services are supported
                      :  32-ACPI supported
                      :  33-USB Legacy is supported
                      :  34-AGP is supported
                      :  39-Smart Battery supported
                      :  40-Reserved for BIOS vendor
                      :  41-Reserved for BIOS vendor
                      :  42-Reserved for BIOS vendor
                      :  58-Reserved for system vendor
                      :  74-Unknown Value
Bios Version          :  DELL   - 27d60a0d
Codeset               :
CurrentLanguage       :  en|US|iso8859-1
Description           :  Phoenix ROM BIOS PLUS Version 1.10 A04
IdentificatonCode     :
InstallableLanguages  :  1
InstallDate           :
LanguageEdition       :
ListOfLanguages       :  en|US|iso8859-1
Manufacturer          :  Dell Inc.
OtherTargetOS         :
PrimaryBIOS           :  True
ReleaseDate           :  20061013000000.000000+000
SerialNumber          :  DDC2H2J
SMBIOSBIOSVersion     :  A04
SMBIOSMajorVersion    :  2
SMBIOSMinorVersion    :  4
SoftwareElementID     :  Phoenix ROM BIOS PLUS Version 1.10 A04
SoftwareElementState  :  3
TargetOperatingSystem :  0
Version               :  DELL   - 27d60a0d
```

## <a name="requirements"></a><span data-ttu-id="68dfe-455">Требования</span><span class="sxs-lookup"><span data-stu-id="68dfe-455">Requirements</span></span>



| <span data-ttu-id="68dfe-456">Требование</span><span class="sxs-lookup"><span data-stu-id="68dfe-456">Requirement</span></span> | <span data-ttu-id="68dfe-457">Значение</span><span class="sxs-lookup"><span data-stu-id="68dfe-457">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68dfe-458">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68dfe-458">Minimum supported client</span></span><br/> | <span data-ttu-id="68dfe-459">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68dfe-459">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68dfe-460">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68dfe-460">Minimum supported server</span></span><br/> | <span data-ttu-id="68dfe-461">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68dfe-461">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68dfe-462">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="68dfe-462">Namespace</span></span><br/>                | <span data-ttu-id="68dfe-463">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="68dfe-463">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="68dfe-464">MOF</span><span class="sxs-lookup"><span data-stu-id="68dfe-464">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68dfe-465"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68dfe-465"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="68dfe-466">DLL</span><span class="sxs-lookup"><span data-stu-id="68dfe-466">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68dfe-467"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68dfe-467"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68dfe-468">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68dfe-468">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68dfe-469">**\_БИОСЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="68dfe-469">**CIM\_BIOSElement**</span></span>](cim-bioselement.md)
</dt> <dt>

[<span data-ttu-id="68dfe-470">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="68dfe-470">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

