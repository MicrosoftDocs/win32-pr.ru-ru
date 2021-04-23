---
description: Представляет устройство, которое может использовать носители для хранения и извлечения данных.
ms.assetid: c63b1731-dbc0-4e5e-acb8-cd91b5569dd2
title: Класс CIM_MediaAccessDevice (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice
- CIM_MediaAccessDevice.Capabilities
- CIM_MediaAccessDevice.CapabilityDescriptions
- CIM_MediaAccessDevice.ErrorMethodology
- CIM_MediaAccessDevice.CompressionMethod
- CIM_MediaAccessDevice.NumberOfMediaSupported
- CIM_MediaAccessDevice.MaxMediaSize
- CIM_MediaAccessDevice.DefaultBlockSize
- CIM_MediaAccessDevice.MaxBlockSize
- CIM_MediaAccessDevice.MinBlockSize
- CIM_MediaAccessDevice.NeedsCleaning
- CIM_MediaAccessDevice.MediaIsLocked
- CIM_MediaAccessDevice.Security
- CIM_MediaAccessDevice.LastCleaned
- CIM_MediaAccessDevice.MaxAccessTime
- CIM_MediaAccessDevice.UncompressedDataRate
- CIM_MediaAccessDevice.LoadTime
- CIM_MediaAccessDevice.UnloadTime
- CIM_MediaAccessDevice.MountCount
- CIM_MediaAccessDevice.TimeOfLastMount
- CIM_MediaAccessDevice.TotalMountTime
- CIM_MediaAccessDevice.UnitsDescription
- CIM_MediaAccessDevice.MaxUnitsBeforeCleaning
- CIM_MediaAccessDevice.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 616148f6749f3ec00d019a903e8f9046d3aba602
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684736"
---
# <a name="cim_mediaaccessdevice-class-hyper-v-management"></a><span data-ttu-id="9c0e4-103">Класс CIM_MediaAccessDevice (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-103">CIM_MediaAccessDevice class (Hyper-V management)</span></span>

<span data-ttu-id="9c0e4-104">Представляет устройство, которое может использовать носители для хранения и извлечения данных.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-104">Represents a device that can use media to store and retrieve data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c0e4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c0e4-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices"), AMENDMENT]
class CIM_MediaAccessDevice : CIM_LogicalDevice
{
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   ErrorMethodology;
  string   CompressionMethod;
  uint32   NumberOfMediaSupported;
  uint64   MaxMediaSize;
  uint64   DefaultBlockSize;
  uint64   MaxBlockSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  boolean  MediaIsLocked;
  uint16   Security;
  datetime LastCleaned;
  uint64   MaxAccessTime;
  uint32   UncompressedDataRate;
  uint64   LoadTime;
  uint64   UnloadTime;
  uint64   MountCount;
  datetime TimeOfLastMount;
  uint64   TotalMountTime;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning;
  uint64   UnitsUsed;
};
```

## <a name="members"></a><span data-ttu-id="9c0e4-106">Члены</span><span class="sxs-lookup"><span data-stu-id="9c0e4-106">Members</span></span>

<span data-ttu-id="9c0e4-107">Класс **CIM \_ медиаакцессдевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9c0e4-107">The **CIM\_MediaAccessDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="9c0e4-108">Методы</span><span class="sxs-lookup"><span data-stu-id="9c0e4-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="9c0e4-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="9c0e4-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9c0e4-110">Методы</span><span class="sxs-lookup"><span data-stu-id="9c0e4-110">Methods</span></span>

<span data-ttu-id="9c0e4-111">Класс **CIM \_ медиаакцессдевице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-111">The **CIM\_MediaAccessDevice** class has these methods.</span></span>



| <span data-ttu-id="9c0e4-112">Метод</span><span class="sxs-lookup"><span data-stu-id="9c0e4-112">Method</span></span>                                               | <span data-ttu-id="9c0e4-113">Описание</span><span class="sxs-lookup"><span data-stu-id="9c0e4-113">Description</span></span>                                                            |
|:-----------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="9c0e4-114">**локкмедиа**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-114">**LockMedia**</span></span>](cim-mediaaccessdevice-lockmedia.md) | <span data-ttu-id="9c0e4-115">Блокирует и разблокирует съемные носители на устройстве доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-115">Locks and unlocks removable media in a media access device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9c0e4-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="9c0e4-116">Properties</span></span>

<span data-ttu-id="9c0e4-117">Класс **CIM \_ медиаакцессдевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-117">The **CIM\_MediaAccessDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c0e4-118">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-118">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-119">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9c0e4-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-121">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Устройства хранения DMTF \| 001,9 "," MIF. \|Устройства хранения DMTF \| 001,11 "," MIF. \|Устройства хранения DMTF \| 001,12 "," MIF. \|Диски DMTF \| 003,7 "," MIF. DMTF- \| диск \| 001,2 "," MIF. \|Жесткий диск DMTF \| 001,4 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ медиаакцессдевице**.**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="9c0e4-121">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7", "MIF.DMTF\|Host Disk\|001.2", "MIF.DMTF\|Host Disk\|001.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-122">Массив, содержащий возможности устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-122">An array that contains the capabilities of the media access device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9c0e4-123">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-123">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9c0e4-124">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-124">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="9c0e4-125">**Последовательный доступ** (2)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-125">**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="9c0e4-126">**Произвольный доступ** (3)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-126">**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="9c0e4-127">**Поддерживает запись** (4)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-127">**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="9c0e4-128">**Шифрование** (5)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-128">**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="9c0e4-129">**Сжатие** (6)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-129">**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="9c0e4-130">**Поддерживает** съемные носители (7)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-130">**Supports Removeable Media** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="9c0e4-131">**Очистка вручную** (8)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-131">**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="9c0e4-132">**Автоматическая очистка** (9)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-132">**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="9c0e4-133">**Интеллектуальное уведомление** (10)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-133">**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="9c0e4-134">**Поддержка двусторонних носителей** (11)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-134">**Supports Dual Sided Media** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="9c0e4-135">**Извлечение с отключением не требуется** (12)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-135">**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9c0e4-136">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-136">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-137">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-137">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-139">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ медиаакцессдевице**.**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="9c0e4-139">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-140">Массив описаний характеристик для элементов в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="9c0e4-140">An array of feature descriptions for the items in the **Capabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="9c0e4-141">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-141">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-144">Имя алгоритма или средства, используемого устройством для поддержки сжатия.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-144">The name of the algorithm or tool used by the device to support compression.</span></span>

<span data-ttu-id="9c0e4-145">Если тип сжатия не указан, можно использовать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="9c0e4-145">If a compression type is not specified, one of the following values can be used:</span></span>

-   <span data-ttu-id="9c0e4-146">Неизвестная поддержка сжатия неизвестна или не указана.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-146">"Unknown"   compression support is unknown or not specified.</span></span>
-   <span data-ttu-id="9c0e4-147">"Сжатое" Сжатие поддерживается, но тип неизвестен или не указан.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-147">"Compressed"   compression is supported but the type is unknown or unspecified.</span></span>
-   <span data-ttu-id="9c0e4-148">"Не сжато" устройство не поддерживает возможности сжатия.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-148">"Not Compressed"   the device does not support compression capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="9c0e4-149">**дефаултблокксизе**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-149">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-150">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-152">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **Пунит** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="9c0e4-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-153">Размер блока по умолчанию для устройства (в байтах).</span><span class="sxs-lookup"><span data-stu-id="9c0e4-153">The default block size, in bytes, for the device.</span></span>

</dd> <dt>

<span data-ttu-id="9c0e4-154">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-154">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-157">Тип обнаружения и исправления ошибок, поддерживаемых устройством.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-157">The type of error detection and correction supported by the device.</span></span>

</dd> <dt>

<span data-ttu-id="9c0e4-158">**ластклеанед**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-158">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-159">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-159">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-161">Дата и время последней очистки устройства.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-161">The date and time when the device was last cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="9c0e4-162">**лоадтиме**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-162">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-163">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-163">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-165">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунды"), **Пунит** ("Second \* 10 ^-3")</span><span class="sxs-lookup"><span data-stu-id="9c0e4-165">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-166">Время, затрачиваемое устройством на чтение или запись носителя после загрузки устройства (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="9c0e4-166">The time it takes, in milliseconds, for the device to be able to read or write a media after the device starts loading.</span></span> <span data-ttu-id="9c0e4-167">Например, для дисков это интервал между диском, который не передается на диск, сообщает о том, что он готов к операциям чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-167">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write operations.</span></span> <span data-ttu-id="9c0e4-168">Для ленточных накопителей это начинается при вставке носителя и заканчивается, когда устройство сообщает о готовности к работе для приложения.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-168">For tape drives, this starts when media is inserted and ends when the drive reports that it is ready for an application.</span></span> <span data-ttu-id="9c0e4-169">Обычно это находится в области ленты ленты (BOT).</span><span class="sxs-lookup"><span data-stu-id="9c0e4-169">This is usually at the tape's beginning-of-tape (BOT) area.</span></span>

</dd> <dt>

<span data-ttu-id="9c0e4-170">**максакцесстиме**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-170">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-171">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-173">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунды"), **Пунит** ("Second \* 10 ^-3")</span><span class="sxs-lookup"><span data-stu-id="9c0e4-173">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-174">Максимальное время доступа к носителю в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-174">The maximum access time of the media, in milliseconds.</span></span> <span data-ttu-id="9c0e4-175">Для диска это означает полный поиск и полную задержку вращения.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-175">For a disk drive, this represents full seek and full rotational delay.</span></span> <span data-ttu-id="9c0e4-176">Для ленточных накопителей этот элемент представляет собой поиск с начала ленты до наиболее физической отдаленной точки.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-176">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span>

</dd> <dt>

<span data-ttu-id="9c0e4-177">**максблокксизе**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-177">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-178">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-180">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **Пунит** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="9c0e4-180">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-181">Максимальный размер блока в байтах для носителя, доступного устройству.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-181">The maximum block size, in bytes, for media accessed by the device.</span></span>

</dd> <dt>

<span data-ttu-id="9c0e4-182">**максмедиасизе**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-182">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-183">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-185">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Устройства с последовательным доступом DMTF \| 001,2 "," MIF. \|Жесткий диск DMTF \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="9c0e4-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2", "MIF.DMTF\|Host Disk\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-186">Максимальный размер носителя, поддерживаемого этим устройством (в килобайтах).</span><span class="sxs-lookup"><span data-stu-id="9c0e4-186">The maximum size, in kilobytes, of media supported by this device.</span></span>

</dd> <dt>

<span data-ttu-id="9c0e4-187">**максунитсбефореклеанинг**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-187">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-188">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-190">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ медиаакцессдевице**.**Унитсдескриптион**")</span><span class="sxs-lookup"><span data-stu-id="9c0e4-190">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**UnitsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-191">Максимальное число единиц, которое можно использовать до очистки устройства.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-191">The maximum number of units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="9c0e4-192">**Унитсдескриптион** определяет, как тип единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-192">**UnitsDescription** defines how the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="9c0e4-193">**медиаислоккед**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-193">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-194">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-196">**значение true** , если носитель заблокирован на устройстве и не может быть извлечен. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-196">**true** if the media is locked in the device and can not be ejected; otherwise, **false**.</span></span> <span data-ttu-id="9c0e4-197">Для несъемных устройств это значение должно быть **равно true**.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-197">For non-removable devices, this value should be **true**.</span></span>

</dd> <dt>

<span data-ttu-id="9c0e4-198">**минблокксизе**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-198">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-199">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-199">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-201">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **Пунит** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="9c0e4-201">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-202">Минимальный размер блока (в байтах) для носителя, доступного устройству.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-202">The minimum block size, in bytes, for media accessed by the device.</span></span>

</dd> <dt>

<span data-ttu-id="9c0e4-203">**маунткаунт**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-203">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-204">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-206">Квалификаторы: **Счетчик**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-206">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-207">Количество случаев, когда носитель был подключен для передачи данных или для очистки устройства.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-207">The number of times that media has been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="9c0e4-208">Если устройство не поддерживает съемные носители, это свойство должно иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-208">If the device does not support removable media, this property should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="9c0e4-209">**нидсклеанинг**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-209">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-210">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-212">**значение true** , если устройству требуется очистка; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-212">**true** if the device needs cleaning; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="9c0e4-213">Свойство **capabilities** указывает, возможна ли ручная или автоматическая очистка.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-213">The **Capabilities** property indicates whether manual or automatic cleaning is possible.</span></span>

 

</dd> <dt>

<span data-ttu-id="9c0e4-214">**нумберофмедиасуппортед**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-214">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-215">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-215">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-216">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-217">Если устройство поддерживает несколько отдельных носителей, это свойство определяет максимальное число, которое может поддерживаться или вставляться.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-217">If the device supports multiple individual media, this property defines the maximum number which can be supported or inserted.</span></span>

</dd> <dt>

<span data-ttu-id="9c0e4-218">**Безопасность**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-218">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-219">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-221">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Диски DMTF \| 003,22 ")</span><span class="sxs-lookup"><span data-stu-id="9c0e4-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Disks\|003.22")</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-222">Операционная безопасность для устройства.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-222">The operational security for the device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9c0e4-223">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-223">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9c0e4-224">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-224">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="9c0e4-225">**Нет** (3)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-225">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Only"></span><span id="read_only"></span><span id="READ_ONLY"></span>

<span data-ttu-id="9c0e4-226">**Только для чтения** (4)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-226">**Read Only** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Locked_Out"></span><span id="locked_out"></span><span id="LOCKED_OUT"></span>

<span data-ttu-id="9c0e4-227">**Заблокировано** (5)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-227">**Locked Out** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

<span data-ttu-id="9c0e4-228">**Обход загрузки** (6)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-228">**Boot Bypass** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass_and_Read_Only"></span><span id="boot_bypass_and_read_only"></span><span id="BOOT_BYPASS_AND_READ_ONLY"></span>

<span data-ttu-id="9c0e4-229">**Только для чтения и обхода загрузки** (7)</span><span class="sxs-lookup"><span data-stu-id="9c0e4-229">**Boot Bypass and Read Only** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9c0e4-230">**тимеофластмаунт**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-230">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-231">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-231">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-233">Последняя дата и время подключения носителя к устройству.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-233">The most recent date and time when media was mounted on the device.</span></span> <span data-ttu-id="9c0e4-234">Это свойство используется только устройствами, поддерживающими съемные носители.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-234">This property is only used by devices that support removable media.</span></span>

</dd> <dt>

<span data-ttu-id="9c0e4-235">**тоталмаунттиме**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-235">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-236">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-236">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-237">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-238">Время в секундах, в течение которого носитель был подключен для передачи данных или для очистки устройства.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-238">The time, in seconds, that media has been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="9c0e4-239">Если устройство не поддерживает съемные носители, это свойство должно иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-239">If the device does not support removable media, this property should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="9c0e4-240">**ункомпресседдатарате**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-240">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-241">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-243">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("килобайт в секунду"), **Пунит** ("байт/сек \* 10 ^ 3")</span><span class="sxs-lookup"><span data-stu-id="9c0e4-243">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes per Second"), **PUnit** ("byte / second \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-244">Постоянная скорость передачи данных в килобайтах, с которой устройство может выполнять чтение и запись на носитель.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-244">The sustained data transfer rate in kilobytes at which the device can read and write to a media.</span></span> <span data-ttu-id="9c0e4-245">Это постоянная скорость необработанных данных.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-245">This is a sustained, raw data rate.</span></span> <span data-ttu-id="9c0e4-246">В этом свойстве не следует сообщать о максимальной скорости или тарифах с сжатием.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-246">Maximum rates or rates with compression should not be reported in this property.</span></span>

</dd> <dt>

<span data-ttu-id="9c0e4-247">**унитсдескриптион**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-247">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-248">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-249">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-250">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ медиаакцессдевице**.**Максунитсбефореклеанинг**","**CIM \_ медиаакцессдевице**.**Унитсусед**")</span><span class="sxs-lookup"><span data-stu-id="9c0e4-250">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**MaxUnitsBeforeCleaning**", "**CIM\_MediaAccessDevice**.**UnitsUsed**")</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-251">Описывает тип единицы для свойств **максунитсбефореклеанинг** и **унитсусед** .</span><span class="sxs-lookup"><span data-stu-id="9c0e4-251">Describes the unit type of the **MaxUnitsBeforeCleaning** and **UnitsUsed** properties.</span></span>

</dd> <dt>

<span data-ttu-id="9c0e4-252">**унитсусед**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-252">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-253">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-253">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-255">Квалификаторы: [**датчик**](/windows/desktop/WmiSdk/standard-qualifiers), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ медиаакцессдевице**.**Унитсдескриптион**","**CIM \_ медиаакцессдевице**.**Максунитсбефореклеанинг**")</span><span class="sxs-lookup"><span data-stu-id="9c0e4-255">Qualifiers: [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**UnitsDescription**", "**CIM\_MediaAccessDevice**.**MaxUnitsBeforeCleaning**")</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-256">Число единиц, используемых устройством.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-256">The number of units used by the device.</span></span> <span data-ttu-id="9c0e4-257">Это свойство используется, чтобы определить, когда устройство должно быть очищено.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-257">This property is used to determine when the device should be cleaned.</span></span> <span data-ttu-id="9c0e4-258">**Унитсдескриптион** определяет, как тип единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-258">**UnitsDescription** defines how the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="9c0e4-259">**унлоадтиме**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-259">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0e4-260">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-260">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-261">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c0e4-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c0e4-262">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунды"), **Пунит** ("Second \* 10 ^-3")</span><span class="sxs-lookup"><span data-stu-id="9c0e4-262">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="9c0e4-263">Время в миллисекундах, необходимое для перехода устройства из чтения или записи носителя в выгружаемый поток.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-263">The time it takes, in milliseconds, for the device to transition from reading or writing media to unloading.</span></span> <span data-ttu-id="9c0e4-264">Например, для дисков это интервал между диском, который вращается с номинальной скоростью, и диск не вращается.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-264">For example, for disk drives, this is the interval between a disk spinning at nominal speeds and a disk not spinning.</span></span> <span data-ttu-id="9c0e4-265">Для накопителей на магнитной ленте это время, когда носитель будет полностью извлечен и доступен элементу выбора или оператору-человеку.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-265">For tape drives, this is the time for a media to go from its BOT to being fully ejected and accessible to a picker element or human operator.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c0e4-266">Требования</span><span class="sxs-lookup"><span data-stu-id="9c0e4-266">Requirements</span></span>



| <span data-ttu-id="9c0e4-267">Требование</span><span class="sxs-lookup"><span data-stu-id="9c0e4-267">Requirement</span></span> | <span data-ttu-id="9c0e4-268">Значение</span><span class="sxs-lookup"><span data-stu-id="9c0e4-268">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c0e4-269">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c0e4-269">Minimum supported client</span></span><br/> | <span data-ttu-id="9c0e4-270">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9c0e4-270">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="9c0e4-271">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c0e4-271">Minimum supported server</span></span><br/> | <span data-ttu-id="9c0e4-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9c0e4-272">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="9c0e4-273">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9c0e4-273">Namespace</span></span><br/>                | <span data-ttu-id="9c0e4-274">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9c0e4-274">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9c0e4-275">MOF</span><span class="sxs-lookup"><span data-stu-id="9c0e4-275">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c0e4-276"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c0e4-276"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c0e4-277">DLL</span><span class="sxs-lookup"><span data-stu-id="9c0e4-277">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c0e4-278"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9c0e4-278"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9c0e4-279">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c0e4-279">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c0e4-280">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="9c0e4-280">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

