---
description: В этом разделе содержится глоссарий технических терминов, используемых в документации по службе виртуальных дисков (VDS).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 1cf28cfb-ce96-4659-955d-0088bddcb9ce
title: Глоссарий службы виртуальных дисков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc8804f1aea832f59fcbcab65423e92e134939f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998605"
---
# <a name="virtual-disk-service-glossary"></a><span data-ttu-id="78d45-103">Глоссарий службы виртуальных дисков</span><span class="sxs-lookup"><span data-stu-id="78d45-103">Virtual Disk Service Glossary</span></span>

<span data-ttu-id="78d45-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="78d45-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="78d45-105">В этом разделе содержится глоссарий технических терминов, используемых в документации по службе виртуальных дисков (VDS).</span><span class="sxs-lookup"><span data-stu-id="78d45-105">This section provides a glossary of technical terms used in the Virtual Disk Service (VDS) documentation.</span></span>

<dl> <dt>

<span data-ttu-id="78d45-106"><span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**Конфигурация automagic**</span><span class="sxs-lookup"><span data-stu-id="78d45-106"><span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**automagic configuration**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-107">Аппаратный поставщик RAID, предоставляющий набор правил для выбора сопоставления логических блоков LUN на основе простых атрибутов.</span><span class="sxs-lookup"><span data-stu-id="78d45-107">Hardware RAID provider that supplies a set of rules for choosing LUN logical block remapping based on simple attributes.</span></span> <span data-ttu-id="78d45-108">Поставщики автоматических Magic также могут динамически изменять сопоставление для управления производительностью и сбоями.</span><span class="sxs-lookup"><span data-stu-id="78d45-108">Automagic providers can also dynamically alter the mapping for performance or fault management.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-109"><span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**подсказки automagic**</span><span class="sxs-lookup"><span data-stu-id="78d45-109"><span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**automagic hints**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-110">Сведения, предоставляемые поставщику automagic для указания конфигурации логического блока LUN.</span><span class="sxs-lookup"><span data-stu-id="78d45-110">Information supplied to an automagic provider to guide the LUN logical block configuration.</span></span> <span data-ttu-id="78d45-111">Указания содержат сведения о предполагаемой отказоустойчивости, физической атомарности и предполагаемом шаблоне доступа ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="78d45-111">Hints include information as to the desired fault tolerance, physical atomicity, and intended I/O access pattern.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-112"><span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**базовый диск**</span><span class="sxs-lookup"><span data-stu-id="78d45-112"><span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**basic disk**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-113">Диск, управляемый простейшим возможным поставщиком программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="78d45-113">A disk managed by the simplest possible software provider.</span></span> <span data-ttu-id="78d45-114">Базовый поставщик дисков поддерживает только тома, которые напрямую сопоставляются с структурами данных конфигурации секций.</span><span class="sxs-lookup"><span data-stu-id="78d45-114">The basic disk provider supports only volumes that directly map to partition configuration data structures.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-115"><span id="base.binding"></span><span id="BASE.BINDING"></span>**вязывания**</span><span class="sxs-lookup"><span data-stu-id="78d45-115"><span id="base.binding"></span><span id="BASE.BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-116">Выбор для набора сопоставлений с физическими ресурсами.</span><span class="sxs-lookup"><span data-stu-id="78d45-116">Selecting for a set of mappings to physical resources.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-117"><span id="base.convert"></span><span id="BASE.CONVERT"></span>**Функция**</span><span class="sxs-lookup"><span data-stu-id="78d45-117"><span id="base.convert"></span><span id="BASE.CONVERT"></span>**convert**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-118">Процесс преобразования базового диска в динамический диск.</span><span class="sxs-lookup"><span data-stu-id="78d45-118">The process of converting a basic disk to a dynamic disk.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-119"><span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**Настройка**</span><span class="sxs-lookup"><span data-stu-id="78d45-119"><span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**configuration**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-120">Коллекция операционных параметров, предоставляя сопоставление тома или LUN с физическими ресурсами.</span><span class="sxs-lookup"><span data-stu-id="78d45-120">A collection of the operating parameters that supply the mapping from a volume, or LUN, to physical resources.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-121"><span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**контроллера**</span><span class="sxs-lookup"><span data-stu-id="78d45-121"><span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**controller**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-122">Программная программа, содержащая логику выполнения для поставщика оборудования.</span><span class="sxs-lookup"><span data-stu-id="78d45-122">A software program that contains the runtime intelligence for a hardware provider.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-123"><span id="base.disk"></span><span id="BASE.DISK"></span>**свободного**</span><span class="sxs-lookup"><span data-stu-id="78d45-123"><span id="base.disk"></span><span id="BASE.DISK"></span>**disk**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-124">Физический диск или LUN аппаратного RAID-массива.</span><span class="sxs-lookup"><span data-stu-id="78d45-124">A physical disk or hardware RAID LUN.</span></span> <span data-ttu-id="78d45-125">Диски — это целевые объекты для загрузки операций ввода-вывода хранилища среды выполнения; Самонастраивающийся (PNP) не различает JBOD и LUN.</span><span class="sxs-lookup"><span data-stu-id="78d45-125">Disks are targets for runtime storage I/O load; Plug and Play (PNP) does not distinguish between JBOD and LUNs.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-126"><span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**диск Негнущийся**</span><span class="sxs-lookup"><span data-stu-id="78d45-126"><span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**disk platter**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-127">Подмножество пакетов, используемых для экспорта или импорта томов из пакета.</span><span class="sxs-lookup"><span data-stu-id="78d45-127">A subset of a pack used for exporting or importing volumes from a pack.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-128"><span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**дисковый пакет**</span><span class="sxs-lookup"><span data-stu-id="78d45-128"><span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**disk pack**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-129">См. раздел *Pack*.</span><span class="sxs-lookup"><span data-stu-id="78d45-129">See *pack*.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-130"><span id="base.drive"></span><span id="BASE.DRIVE"></span>**диск**</span><span class="sxs-lookup"><span data-stu-id="78d45-130"><span id="base.drive"></span><span id="BASE.DRIVE"></span>**drive**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-131">Физический диск в аппаратной подсистеме RAID.</span><span class="sxs-lookup"><span data-stu-id="78d45-131">A physical disk spindle within a hardware RAID subsystem.</span></span> <span data-ttu-id="78d45-132">Диски привязаны к LUN подсистемой.</span><span class="sxs-lookup"><span data-stu-id="78d45-132">Drives are bound into LUNs by the subsystem.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-133"><span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**динамический диск**</span><span class="sxs-lookup"><span data-stu-id="78d45-133"><span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**dynamic disk**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-134">Диск, управляемый поставщиком программного RAID-массива, с поддержкой гибкой настройки томов.</span><span class="sxs-lookup"><span data-stu-id="78d45-134">A disk managed by a software RAID provider with support for flexible volume reconfiguration.</span></span> <span data-ttu-id="78d45-135">Динамический диск использует секцию в качестве контейнера для томов; гарантированное сопоставление отсутствует.</span><span class="sxs-lookup"><span data-stu-id="78d45-135">A dynamic disk uses a partition as a container for volumes; there is no guaranteed mapping.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-136"><span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**явная конфигурация**</span><span class="sxs-lookup"><span data-stu-id="78d45-136"><span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**explicit configuration**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-137">Конфигурация с параметрами, включая тип тома и точный макет, для коллекции целевых томов.</span><span class="sxs-lookup"><span data-stu-id="78d45-137">A configuration with the parameters, including the volume type and the exact layout, for a collection of target volumes.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-138"><span id="base.export"></span><span id="BASE.EXPORT"></span>**программе**</span><span class="sxs-lookup"><span data-stu-id="78d45-138"><span id="base.export"></span><span id="BASE.EXPORT"></span>**export**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-139">Процесс перемещения Негнущийся диска и всех томов, содержащихся в негнущийся, из пакета.</span><span class="sxs-lookup"><span data-stu-id="78d45-139">The act of moving a disk platter and all volumes contained on that platter out of a pack.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-140"><span id="base.extent"></span><span id="BASE.EXTENT"></span>**экстент**</span><span class="sxs-lookup"><span data-stu-id="78d45-140"><span id="base.extent"></span><span id="BASE.EXTENT"></span>**extent**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-141">Непрерывный диапазон логических секторов, участвующих в одном томе или на диске.</span><span class="sxs-lookup"><span data-stu-id="78d45-141">A contiguous range of logical sectors contributing to a single volume or disk.</span></span> <span data-ttu-id="78d45-142">Экстент также может быть диапазоном нераспределенных секторов.</span><span class="sxs-lookup"><span data-stu-id="78d45-142">An extent can also be range of unallocated sectors.</span></span> <span data-ttu-id="78d45-143">Как правило, файловая система отображает сведения о экстенте для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="78d45-143">Commonly, a file system displays the extent details to an end-user.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-144"><span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**Таблица разделов GUID (GPT)**</span><span class="sxs-lookup"><span data-stu-id="78d45-144"><span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**GUID Partition Table (GPT)**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-145">Структуры, используемые встроенным по EFI.</span><span class="sxs-lookup"><span data-stu-id="78d45-145">Structures used by EFI firmware.</span></span> <span data-ttu-id="78d45-146">GPT — это один из двух форматов данных конфигурации программного обеспечения самого низкого уровня, используемых встроенным по платформы для размещения загрузочной операционной системы или другого исполняемого образа.</span><span class="sxs-lookup"><span data-stu-id="78d45-146">GPT is one of two lowest level software configuration data formats used by platform firmware to locate a bootable operating system or other executable image.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-147"><span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**Поставщик оборудования**</span><span class="sxs-lookup"><span data-stu-id="78d45-147"><span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**hardware provider**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-148">Набор программного обеспечения, которое выполняется на узле, адаптер шины и, возможно, внешняя подсистема хранения, которая работает вместе для управления LUN RAID.</span><span class="sxs-lookup"><span data-stu-id="78d45-148">A collection of software that executes on the host, a bus adapter, and possibly an external storage subsystem that works together to surface and manage RAID LUNs.</span></span> <span data-ttu-id="78d45-149">Поставщики оборудования для большинства внешних подсистем хранения содержат только программное обеспечение, основанное на основном режиме пользователя.</span><span class="sxs-lookup"><span data-stu-id="78d45-149">Hardware providers for most external storage subsystems contain only user-mode, host-based software.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-150"><span id="base.health"></span><span id="BASE.HEALTH"></span>**рабочего**</span><span class="sxs-lookup"><span data-stu-id="78d45-150"><span id="base.health"></span><span id="BASE.HEALTH"></span>**health**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-151">Текущее состояние управления сбоями тома или LUN.</span><span class="sxs-lookup"><span data-stu-id="78d45-151">The current fault-management status of a volume or a LUN.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-152"><span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**горячее резервирование**</span><span class="sxs-lookup"><span data-stu-id="78d45-152"><span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**hot sparing**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-153">Временное добавление плекса тома в том.</span><span class="sxs-lookup"><span data-stu-id="78d45-153">Temporarily adding a volume plex to a volume.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-154"><span id="base.import"></span><span id="BASE.IMPORT"></span>**импортиру**</span><span class="sxs-lookup"><span data-stu-id="78d45-154"><span id="base.import"></span><span id="BASE.IMPORT"></span>**import**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-155">Процедура перемещения диска Негнущийся и всех его томов в существующий пакет.</span><span class="sxs-lookup"><span data-stu-id="78d45-155">The act of moving a disk platter and all its volumes into an existing pack.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-156"><span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**только ряд дисков (JBOD)**</span><span class="sxs-lookup"><span data-stu-id="78d45-156"><span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**just a bunch of disks (JBOD)**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-157">Коллекция физических дисков без согласованного элемента управления, предоставляемого аппаратным RAID-устройством.</span><span class="sxs-lookup"><span data-stu-id="78d45-157">A collection of physical spindles without the coordinated control provided by a hardware RAID device.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-158"><span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**номер логического блока (ЛБН)**</span><span class="sxs-lookup"><span data-stu-id="78d45-158"><span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**logical block number (LBN)**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-159">Наименьшая адресация единиц хранения данных.</span><span class="sxs-lookup"><span data-stu-id="78d45-159">The smallest addressable unit of storage data.</span></span> <span data-ttu-id="78d45-160">ЛБН используется с протоколами команд ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="78d45-160">LBN is used with I/O command protocols.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-161"><span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**Сопоставление логических блоков**</span><span class="sxs-lookup"><span data-stu-id="78d45-161"><span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**logical block mapping**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-162">Преобразование логических блоков, представленных поставщику, на те, которые предоставляются поставщиком.</span><span class="sxs-lookup"><span data-stu-id="78d45-162">The transformation of the logical blocks presented to a provider to those exposed by the provider.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-163"><span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**номер логического устройства (LUN)**</span><span class="sxs-lookup"><span data-stu-id="78d45-163"><span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**logical unit number (LUN)**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-164">Физическая единица хранения, предоставляемая подсистемой аппаратных RAID-массивов.</span><span class="sxs-lookup"><span data-stu-id="78d45-164">A physically addressable storage unit as surfaced by a hardware RAID subsystem.</span></span> <span data-ttu-id="78d45-165">Этот термин также может ссылаться на идентификатор SCSI для единицы хранения.</span><span class="sxs-lookup"><span data-stu-id="78d45-165">This term can also refer to the SCSI identifier for the storage unit.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-166"><span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**Номер LUN**</span><span class="sxs-lookup"><span data-stu-id="78d45-166"><span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**LUN number**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-167">Число, которое поставщик оборудования VDS назначает LUN в массиве.</span><span class="sxs-lookup"><span data-stu-id="78d45-167">A number that a VDS hardware provider assigns to a LUN in an array.</span></span> <span data-ttu-id="78d45-168">Это не то же самое, что "логический номер устройства" в SCSI-адресе диска.</span><span class="sxs-lookup"><span data-stu-id="78d45-168">This is not the same as the "logical unit number" in the disk's SCSI address.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-169"><span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**Служба управления**</span><span class="sxs-lookup"><span data-stu-id="78d45-169"><span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**management service**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-170">Программа, которая выполняется по мере необходимости для выполнения настройки, мониторинга или обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="78d45-170">A software program that executes as needed to perform volume configuration, monitoring, or fault handling.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-171"><span id="base.mapping"></span><span id="BASE.MAPPING"></span>**Картограф**</span><span class="sxs-lookup"><span data-stu-id="78d45-171"><span id="base.mapping"></span><span id="BASE.MAPPING"></span>**mapping**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-172">Том, который доступен операционной системе и имеет соответствующее имя тома (буква диска).</span><span class="sxs-lookup"><span data-stu-id="78d45-172">A volume that is exposed to the operating system and has an associated volume name (a drive letter).</span></span> <span data-ttu-id="78d45-173">Том доступен для файловой системы.</span><span class="sxs-lookup"><span data-stu-id="78d45-173">A volume is accessible by a file system.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-174"><span id="base.masking"></span><span id="BASE.MASKING"></span>**маскирования**</span><span class="sxs-lookup"><span data-stu-id="78d45-174"><span id="base.masking"></span><span id="BASE.MASKING"></span>**masking**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-175">Диск не распознается операционной системой.</span><span class="sxs-lookup"><span data-stu-id="78d45-175">A disk not recognized by the operating system.</span></span> <span data-ttu-id="78d45-176">Диск может быть маскирован подсистемой аппаратных RAID-массивов, коммутатором, РЕЗЕРВИРОВАНием SCSI другим узлом компьютера или программным обеспечением в стеке диска.</span><span class="sxs-lookup"><span data-stu-id="78d45-176">A disk can be masked by the hardware RAID subsystem, switch, SCSI RESERVE by another computer host, or software in the disk stack.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-177"><span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**секционирование основной загрузочной записи (MBR)**</span><span class="sxs-lookup"><span data-stu-id="78d45-177"><span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**master boot record partitioning (MBR)**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-178">MBR — это один из двух форматов данных конфигурации программного обеспечения самого низкого уровня, который используется встроенным по BIOS для размещения загрузочного образа операционной системы.</span><span class="sxs-lookup"><span data-stu-id="78d45-178">MBR is one of two lowest level software configuration data formats, and is used by BIOS firmware to locate a bootable operating system image.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-179"><span id="base.member"></span><span id="BASE.MEMBER"></span>**участниками**</span><span class="sxs-lookup"><span data-stu-id="78d45-179"><span id="base.member"></span><span id="BASE.MEMBER"></span>**member**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-180">Коллекция Объединенных экстентов дисков, содержащихся на одном диске.</span><span class="sxs-lookup"><span data-stu-id="78d45-180">A collection of concatenated disk extents contained on one more disks.</span></span> <span data-ttu-id="78d45-181">Диск может участвовать только в одном члене тома.</span><span class="sxs-lookup"><span data-stu-id="78d45-181">A disk can contribute to only one member of a volume.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-182"><span id="base.mirror"></span><span id="BASE.MIRROR"></span>**Отображение**</span><span class="sxs-lookup"><span data-stu-id="78d45-182"><span id="base.mirror"></span><span id="BASE.MIRROR"></span>**mirror**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-183">Сопоставление томов или дисков, которое поддерживает две или более идентичные копии данных.</span><span class="sxs-lookup"><span data-stu-id="78d45-183">A volume or disk mapping that maintains two or more identical data copies.</span></span> <span data-ttu-id="78d45-184">Тип сопоставления называется также RAID-уровнем 1.</span><span class="sxs-lookup"><span data-stu-id="78d45-184">The type of mapping is also called RAID Level 1.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-185"><span id="base.pack"></span><span id="BASE.PACK"></span>**распаковк**</span><span class="sxs-lookup"><span data-stu-id="78d45-185"><span id="base.pack"></span><span id="BASE.PACK"></span>**pack**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-186">Коллекция логических томов и базовых дисков.</span><span class="sxs-lookup"><span data-stu-id="78d45-186">A collection of logical volumes and underlying disks.</span></span> <span data-ttu-id="78d45-187">Пакет — это единица транзитного замыкания для тома.</span><span class="sxs-lookup"><span data-stu-id="78d45-187">A pack is the unit of transitive closure for a volume.</span></span> <span data-ttu-id="78d45-188">Динамические пакеты дисков и группы дисков — это термины для одного и того же элемента.</span><span class="sxs-lookup"><span data-stu-id="78d45-188">Dynamic disk packs and disk groups are terms for the same item.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-189"><span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**полоса прочетности**</span><span class="sxs-lookup"><span data-stu-id="78d45-189"><span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**parity stripe**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-190">Сопоставление томов или дисков, которое поддерживает данные проверки четности и данных.</span><span class="sxs-lookup"><span data-stu-id="78d45-190">A volume or disk mapping that maintains parity check information as well as data.</span></span> <span data-ttu-id="78d45-191">Каждый поставщик предоставляет точную схему сопоставления и защиты.</span><span class="sxs-lookup"><span data-stu-id="78d45-191">Each vendor supplies the exact mapping and protection scheme.</span></span> <span data-ttu-id="78d45-192">Включает в себя RAID 3, 4, 5 и 6.</span><span class="sxs-lookup"><span data-stu-id="78d45-192">Includes RAID 3, 4, 5, and 6.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-193"><span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**Конфигурация с частичным направлением**</span><span class="sxs-lookup"><span data-stu-id="78d45-193"><span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**partially directed configuration**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-194">Конфигурация тома или диска не является полностью явной.</span><span class="sxs-lookup"><span data-stu-id="78d45-194">A volume or disk configuration that is not fully explicit.</span></span> <span data-ttu-id="78d45-195">Указаны тип привязки и коллекция целевых ресурсов; фактический макет — нет.</span><span class="sxs-lookup"><span data-stu-id="78d45-195">The binding type and a collection of target resources are specified; the actual layout is not.</span></span> <span data-ttu-id="78d45-196">Конфигурация с частичным назначением является наиболее распространенной конфигурацией тома.</span><span class="sxs-lookup"><span data-stu-id="78d45-196">Partially directed configuration is the most common volume configuration.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-197"><span id="base.partition"></span><span id="BASE.PARTITION"></span>**диска**</span><span class="sxs-lookup"><span data-stu-id="78d45-197"><span id="base.partition"></span><span id="BASE.PARTITION"></span>**partition**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-198">Непрерывный диапазон логических секторов, описываемый одной записью в структуре MBR или GPT.</span><span class="sxs-lookup"><span data-stu-id="78d45-198">A contiguous range of logical sectors described by a single entry in the MBR or GPT structure.</span></span> <span data-ttu-id="78d45-199">На базовых дисках разделы непосредственно соответствуют простым томам.</span><span class="sxs-lookup"><span data-stu-id="78d45-199">On basic disks, partitions directly correspond to simple volumes.</span></span> <span data-ttu-id="78d45-200">Структуры разделов являются общими для микропрограммы BIOS или EFI, а также операционной системы или другого загрузочного образа.</span><span class="sxs-lookup"><span data-stu-id="78d45-200">Partition structures are shared between the BIOS or EFI platform firmware and an operating system or other bootable image.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-201"><span id="base.path"></span><span id="BASE.PATH"></span>**путь**</span><span class="sxs-lookup"><span data-stu-id="78d45-201"><span id="base.path"></span><span id="BASE.PATH"></span>**path**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-202">Путь доступа с компьютера к диску или внешнему LUN оборудования.</span><span class="sxs-lookup"><span data-stu-id="78d45-202">The access path from a computer to a disk or external hardware LUN.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-203"><span id="base.plex"></span><span id="BASE.PLEX"></span>**плексов**</span><span class="sxs-lookup"><span data-stu-id="78d45-203"><span id="base.plex"></span><span id="BASE.PLEX"></span>**plex**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-204">Один член зеркального тома или LUN.</span><span class="sxs-lookup"><span data-stu-id="78d45-204">One member of a mirrored volume or LUN.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-205"><span id="base.port"></span><span id="BASE.PORT"></span>**порту**</span><span class="sxs-lookup"><span data-stu-id="78d45-205"><span id="base.port"></span><span id="BASE.PORT"></span>**port**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-206">Конечная точка пути на диске.</span><span class="sxs-lookup"><span data-stu-id="78d45-206">The endpoint of a path at a disk.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-207"><span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**избыточный массив независимых дисков (RAID)**</span><span class="sxs-lookup"><span data-stu-id="78d45-207"><span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**redundant array of independent disks (RAID)**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-208">Набор методов для управления несколькими дисками.</span><span class="sxs-lookup"><span data-stu-id="78d45-208">A collection of techniques for managing multiple disks.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-209"><span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**Служба времени выполнения**</span><span class="sxs-lookup"><span data-stu-id="78d45-209"><span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**runtime service**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-210">Программная программа, выполняемая на основе запроса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="78d45-210">A software program that executes on an I/O-request basis.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-211"><span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**простой диск**</span><span class="sxs-lookup"><span data-stu-id="78d45-211"><span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**simple disk**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-212">Диск, не подключенный к аппаратному RAID-контроллеру.</span><span class="sxs-lookup"><span data-stu-id="78d45-212">A spindle that is not connected to a hardware RAID controller.</span></span> <span data-ttu-id="78d45-213">См. также: только ряд дисков (JBOD).</span><span class="sxs-lookup"><span data-stu-id="78d45-213">See also Just a Bunch Of Disks (JBOD).</span></span>

</dd> <dt>

<span data-ttu-id="78d45-214"><span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**поставщик программного обеспечения**</span><span class="sxs-lookup"><span data-stu-id="78d45-214"><span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**software provider**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-215">Программное обеспечение на основе узла, которое предоставляет логические тома и работает с дисками.</span><span class="sxs-lookup"><span data-stu-id="78d45-215">Host-based software that exposes logical volumes and operates on disks.</span></span> <span data-ttu-id="78d45-216">Поставщик программного обеспечения включает в себя службы среды выполнения режима ядра, данные конфигурации и службы управления пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="78d45-216">A software provider includes kernel-mode runtime services, configuration data, and user-mode management services.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-217"><span id="base.span"></span><span id="BASE.SPAN"></span>**размещать**</span><span class="sxs-lookup"><span data-stu-id="78d45-217"><span id="base.span"></span><span id="BASE.SPAN"></span>**span**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-218">Линейное сопоставление томов или дисков для нескольких ненепрерывных дисков или экстентов диска.</span><span class="sxs-lookup"><span data-stu-id="78d45-218">A volume or disk linear mapping of multiple discontinuous disk or drive extents.</span></span> <span data-ttu-id="78d45-219">Экстенты могут быть на одном или нескольких дисках или LUN.</span><span class="sxs-lookup"><span data-stu-id="78d45-219">The extents can be on one or more spindles or LUNs.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-220"><span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**spindle**</span><span class="sxs-lookup"><span data-stu-id="78d45-220"><span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**spindle**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-221">Физическая единица дискового хранилища.</span><span class="sxs-lookup"><span data-stu-id="78d45-221">A physical unit of disk storage.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-222"><span id="base.stacking"></span><span id="BASE.STACKING"></span>**наложение**</span><span class="sxs-lookup"><span data-stu-id="78d45-222"><span id="base.stacking"></span><span id="BASE.STACKING"></span>**stacking**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-223">Процесс создания тома или LUN путем выполнения нескольких операций сопоставления логических блоков.</span><span class="sxs-lookup"><span data-stu-id="78d45-223">The act of constructing a volume or LUN by performing more than one logical block mapping operation.</span></span> <span data-ttu-id="78d45-224">Примером является зеркальный чередующийся том.</span><span class="sxs-lookup"><span data-stu-id="78d45-224">An example is a mirrored striped volume.</span></span> <span data-ttu-id="78d45-225">Наиболее распространенное построение стека происходит при использовании программного RAID-массива в LUN, созданном аппаратным RAID-массивом.</span><span class="sxs-lookup"><span data-stu-id="78d45-225">The most common stacking occurs when software RAID is used across LUNs constructed by hardware RAID.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-226"><span id="base.stripe"></span><span id="BASE.STRIPE"></span>**Наборы**</span><span class="sxs-lookup"><span data-stu-id="78d45-226"><span id="base.stripe"></span><span id="BASE.STRIPE"></span>**stripe**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-227">Сопоставление томов или дисков, которое выполняет чередование непрерывных экстентов на нескольких томах, дисках или дисках.</span><span class="sxs-lookup"><span data-stu-id="78d45-227">A volume or disk mapping that interleaves contiguous extents across multiple volumes, disks, or drives.</span></span> <span data-ttu-id="78d45-228">Это сопоставление также называется RAID 0.</span><span class="sxs-lookup"><span data-stu-id="78d45-228">This mapping is also called RAID 0.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-229"><span id="base.status"></span><span id="BASE.STATUS"></span>**состояние**</span><span class="sxs-lookup"><span data-stu-id="78d45-229"><span id="base.status"></span><span id="BASE.STATUS"></span>**status**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-230">Текущая доступность тома, диска или диска.</span><span class="sxs-lookup"><span data-stu-id="78d45-230">The current availability of a volume, disk, or drive.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-231"><span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**подсистемы**</span><span class="sxs-lookup"><span data-stu-id="78d45-231"><span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**subsystem**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-232">Создание экземпляра программного обеспечения поставщика оборудования.</span><span class="sxs-lookup"><span data-stu-id="78d45-232">The instantiation of hardware-provider software.</span></span> <span data-ttu-id="78d45-233">Подсистема содержит по крайней мере один контроллер и один диск.</span><span class="sxs-lookup"><span data-stu-id="78d45-233">A subsystem contains at least one controller and one drive.</span></span> <span data-ttu-id="78d45-234">Если подсистема является внешней по отношению к компьютеру, один или несколько сетевых путей соединяют подсистему с компьютером.</span><span class="sxs-lookup"><span data-stu-id="78d45-234">If the subsystem is external to the computer, one or more network paths connect the subsystem to the computer.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-235"><span id="base.jello"></span><span id="BASE.JELLO"></span>**состояние перехода**</span><span class="sxs-lookup"><span data-stu-id="78d45-235"><span id="base.jello"></span><span id="BASE.JELLO"></span>**transition state**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-236">Состояние логического с физическим сопоставлением, которое будет изменено.</span><span class="sxs-lookup"><span data-stu-id="78d45-236">Status of the logical to physical mapping that is undergoing change.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-237"><span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**неинициализированный диск**</span><span class="sxs-lookup"><span data-stu-id="78d45-237"><span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**uninitialized disk**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-238">Диск, который не является членом пакета.</span><span class="sxs-lookup"><span data-stu-id="78d45-238">A disk that is not a member of a pack.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-239"><span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**немаскированный диск**</span><span class="sxs-lookup"><span data-stu-id="78d45-239"><span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**unmasked disk**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-240">Диск, видимый операционной системе.</span><span class="sxs-lookup"><span data-stu-id="78d45-240">A disk that is visible to the operating system.</span></span> <span data-ttu-id="78d45-241">Содержимое немаскированного диска видимо для диспетчеров программных томов, файловых систем и т. д.</span><span class="sxs-lookup"><span data-stu-id="78d45-241">The contents of an unmasked disk are visible to software volume managers, file systems, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="78d45-242"><span id="base.volume"></span><span id="BASE.VOLUME"></span>**тома**</span><span class="sxs-lookup"><span data-stu-id="78d45-242"><span id="base.volume"></span><span id="BASE.VOLUME"></span>**volume**</span></span>
</dt> <dd>

<span data-ttu-id="78d45-243">Ряд экстентов диска, привязанных к практически непрерывному диапазону логических блоков.</span><span class="sxs-lookup"><span data-stu-id="78d45-243">A number of disk extents bound into a virtually contiguous range of logical blocks.</span></span> <span data-ttu-id="78d45-244">Доступ к тому можно получить с помощью буквы диска, подключенной папки или пути GUID тома.</span><span class="sxs-lookup"><span data-stu-id="78d45-244">A volume can be accessed through a drive letter, a mounted folder, or a volume GUID path.</span></span>

</dd> </dl>

 

 
