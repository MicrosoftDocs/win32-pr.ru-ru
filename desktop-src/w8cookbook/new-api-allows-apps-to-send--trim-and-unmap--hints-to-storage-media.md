---
title: Новый API позволяет приложениям отсылать подсказки "обрезать и отменить сопоставление" на носитель хранилища
description: Новый API позволяет приложениям отправить \ 0034; Обрезать и отменить сопоставление \ 0034; указания на носитель для хранения данных
ms.assetid: DDBC3592-BD4D-4826-83FE-387564DA07E8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e043c1188bda790b4ed151e8a79e1f7b4c6f0f9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "105691680"
---
# <a name="new-api-allows-apps-to-send-trim-and-unmap-hints-to-storage-media"></a><span data-ttu-id="fe62e-103">Новый API позволяет приложениям отсылать подсказки "обрезать и отменить сопоставление" на носитель хранилища</span><span class="sxs-lookup"><span data-stu-id="fe62e-103">New API allows apps to send "TRIM and Unmap" hints to storage media</span></span>

## <a name="platforms"></a><span data-ttu-id="fe62e-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="fe62e-104">Platforms</span></span>

<span data-ttu-id="fe62e-105">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="fe62e-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="fe62e-106">**Серверы** — Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fe62e-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="fe62e-107">Описание</span><span class="sxs-lookup"><span data-stu-id="fe62e-107">Description</span></span>

<span data-ttu-id="fe62e-108">Указания TRIM уведомляют диск о том, что определенные ранее выделенные секторы больше не требуются приложению и могут быть очищены.</span><span class="sxs-lookup"><span data-stu-id="fe62e-108">TRIM hints notify the drive that certain sectors that previously were allocated are no longer needed by the app and can be purged.</span></span> <span data-ttu-id="fe62e-109">Обычно это используется в том случае, если приложение создает большой объем памяти с помощью файла, а затем самостоятельно управляет выделением для файла (например, файлов виртуального жесткого диска).</span><span class="sxs-lookup"><span data-stu-id="fe62e-109">This is typically used when an app makes large space allocations via a file and then self-manages the allocations to the file (for example, Virtual Hard Disk files).</span></span>

<span data-ttu-id="fe62e-110">**Что такое TRIM?**</span><span class="sxs-lookup"><span data-stu-id="fe62e-110">**What is TRIM?**</span></span>

<span data-ttu-id="fe62e-111">Твердотельные накопители (SSD) обычно являются блочными устройствами флэш-памяти. Это означает, что когда данные записываются на SSD, они не могут быть перезаписаны на месте и должны быть записаны в любом месте до тех пор, пока блок не будет удален сборщиком мусора.</span><span class="sxs-lookup"><span data-stu-id="fe62e-111">Solid state drives (SSDs) are typically flash memory based block-erased devices; this means that when data is written to the SSD, it cannot be over-written in place and must be written elsewhere until the block can be garbage collected.</span></span> <span data-ttu-id="fe62e-112">Так как SSD не имеет внутреннего механизма для определения того, что определенные блоки удаляются и требуются другие.</span><span class="sxs-lookup"><span data-stu-id="fe62e-112">Since the SSD has no internal mechanism for determining that certain blocks are removed and others are needed.</span></span> <span data-ttu-id="fe62e-113">Единственным моментом, когда SSD может пометить сектор "грязный", является то, что он переносится.</span><span class="sxs-lookup"><span data-stu-id="fe62e-113">The only time the SSD can mark a sector ‘dirty’ is when it is over-written.</span></span> <span data-ttu-id="fe62e-114">В других случаях, например при удалении файла, SSD оставляет эти секторы, так как удаление выполняется только в виде основной таблицы файлов (MFT), а не в виде операции со всеми секторами файла.</span><span class="sxs-lookup"><span data-stu-id="fe62e-114">In other cases, such as when a file is deleted, the SSD retains these sectors because the deletion is performed as a master file table (MFT) change only, and not as an operation to all the sectors of the file.</span></span> <span data-ttu-id="fe62e-115">В Windows 7 мы представили стандартный способ связи с SSDs о секторах, которые больше не требуются.</span><span class="sxs-lookup"><span data-stu-id="fe62e-115">In Windows 7, we introduced a standard way of communicating with SSDs about sectors that are not needed any more.</span></span> <span data-ttu-id="fe62e-116">Эта команда определена в [спецификации T13](https://www.t13.org/Standards/Default.aspx?DocumentType=3) как команда Trim; NTFS отправляет команду TRIM для некоторых обычных встроенных операций, таких как "DeleteFile".</span><span class="sxs-lookup"><span data-stu-id="fe62e-116">This command is defined in the [T13 specification](https://www.t13.org/Standards/Default.aspx?DocumentType=3) as the TRIM command; NTFS sends the TRIM command for some normal inline operations such as “deletefile.”</span></span>

<span data-ttu-id="fe62e-117">**Другие способы обрезки в мире хранилища**</span><span class="sxs-lookup"><span data-stu-id="fe62e-117">**Other uses of TRIM in the storage world**</span></span>

<span data-ttu-id="fe62e-118">Как и в случае с SSDs, сети хранения данных (SAN) и новые реализации функциональных пространств в Windows 8 используют подсказки команд TRIM для управления пространствами в тонко подготовленных средах.</span><span class="sxs-lookup"><span data-stu-id="fe62e-118">Like SSDs, storage area networks (SANs) and the new Windows 8 feature Software Spaces implementations consume TRIM command hints to manage their spaces in thinly provisioned environments.</span></span> <span data-ttu-id="fe62e-119">San и программные пространства выделяют регионы хранения в размере больше секторов или кластеров (от 1 МБ до 1 ГБ).</span><span class="sxs-lookup"><span data-stu-id="fe62e-119">SANs and Software Spaces allocate regions of storage in sizes that are greater than sectors or clusters (anywhere from 1MB to 1GB).</span></span> <span data-ttu-id="fe62e-120">Когда они получают указания по УСЕЧЕНию для размера выделения (или больше размера выделения), SAN/SSD может отменить выделение региона для освобождения места для других файлов.</span><span class="sxs-lookup"><span data-stu-id="fe62e-120">When they receive TRIM hints for its allocation size (or greater than the allocation size), the SAN/SSD can de-allocate a region to free up the space for other files.</span></span> <span data-ttu-id="fe62e-121">Обычно они передают все подсказки по обрезке базовому носителю (SSD или HDD), чтобы они могли потреблять свободное пространство по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="fe62e-121">They typically pass through all TRIM hints to the underlying media (SSD or HDD) so that they can consume the freed up space as appropriate.</span></span> <span data-ttu-id="fe62e-122">Обычно они не перемещают данные для отмены распределения регионов, а также не отслеживают области обрезки до освобожденных регионов (если регион пуст).</span><span class="sxs-lookup"><span data-stu-id="fe62e-122">They do not typically move data around to de-allocate regions, nor do they keep track of TRIM areas to de-allocated regions (when the region is empty).</span></span>

<span data-ttu-id="fe62e-123">С тонкой подготовкой сети SAN используют передаваемые им указания по УСЕЧЕНию для снижения общего объема физической памяти, что снижает затраты.</span><span class="sxs-lookup"><span data-stu-id="fe62e-123">Thinly provisioned SANs use the TRIM hints that are passed to them to help reduce the overall physical storage footprint, hence reducing cost.</span></span> <span data-ttu-id="fe62e-124">[Спецификация T10 SCSI](https://www.t10.org) определяет команду "Отмена сопоставления" (аналогично команде Trim); Эта команда применима ко всем типам хранилищ, включая жесткие диски, твердотельные накопители и другие.</span><span class="sxs-lookup"><span data-stu-id="fe62e-124">The [T10 SCSI specification](https://www.t10.org) defines the ‘Unmap’ command (similar to the TRIM command); here the command is applicable to all kinds of storage including HDDs, SSDs, and others.</span></span> <span data-ttu-id="fe62e-125">Команда отмена сопоставления помогает удалить физические блоки из выделения SAN.</span><span class="sxs-lookup"><span data-stu-id="fe62e-125">The UnMap command helps to remove physical blocks from the SAN’s allocation.</span></span>

## <a name="how-to-use-the-new-api"></a><span data-ttu-id="fe62e-126">Как использовать новый API</span><span class="sxs-lookup"><span data-stu-id="fe62e-126">How to use the new API</span></span>


```
#define FSCTL_FILE_LEVEL_TRIM CTL_CODE(FILE_DEVICE_FILE_SYSTEM, 130, METHOD_BUFFERED, FILE_WRITE_DATA)

Where 
typedef struct _EXTENT_PAIR {
    ULONGLONG Offset;
    ULONGLONG Length;
} EXTENT_PAIR, *PEXTENT_PAIR;

typedef struct _FILE_LEVEL_TRIM {
    //
    // A count of how many Offset:Length pairs are given
    //
    DWORD PairCount;
    //
    // All the pairs.
    //
    EXTENT_PAIR Pairs[1];
} FILE_LEVEL_TRIM, *PFILE_LEVEL_TRIM;
```



<span data-ttu-id="fe62e-127">УСЕЧЕНИЕ файла передается через буфер, если это возможно или асинхронно (без буферизации) для команды DSM IOCTL устройства.</span><span class="sxs-lookup"><span data-stu-id="fe62e-127">File TRIM is passed via the buffer if possible or asynchronously (non-buffered) to the Device IOCTL DSM command TRIM.</span></span> <span data-ttu-id="fe62e-128">Она сопоставлена с командой TRIM для устройств ATA и командой отмены сопоставления для устройств SCSI.</span><span class="sxs-lookup"><span data-stu-id="fe62e-128">This is mapped to the TRIM command for ATA devices and UnMap command for SCSI devices.</span></span> <span data-ttu-id="fe62e-129">Код УСЕЧЕНИЯ файла отправляет регионы по одному согласно указанным выше экстентам.</span><span class="sxs-lookup"><span data-stu-id="fe62e-129">The file TRIM code sends the regions one-by-one as specified by the extents above.</span></span>

<span data-ttu-id="fe62e-130">УСЕЧЕНИЕ файлов не ждет возврата с устройства, так как команды TRIM и undefined определены как подсказки для базового носителя хранилища и коды возврата не ожидаются.</span><span class="sxs-lookup"><span data-stu-id="fe62e-130">File TRIM does not wait for returns from the device, because the TRIM and Unmap commands are defined as hints to the underlying storage media and return codes are not expected.</span></span>

<span data-ttu-id="fe62e-131">**Сквозной рабочий процесс:**</span><span class="sxs-lookup"><span data-stu-id="fe62e-131">**End-to-end workflow:**</span></span>

1.  <span data-ttu-id="fe62e-132">Обрезать файл вызова</span><span class="sxs-lookup"><span data-stu-id="fe62e-132">Call File Trim</span></span>
    1.  <span data-ttu-id="fe62e-133">УСЕЧЕНИЕ файла. проверяет входные данные на наличие ошибок</span><span class="sxs-lookup"><span data-stu-id="fe62e-133">File TRIM examines inputs for errors</span></span>
    2.  <span data-ttu-id="fe62e-134">УСЕЧЕНИЕ файлов разбивает экстенты на регионы LCN</span><span class="sxs-lookup"><span data-stu-id="fe62e-134">File TRIM breaks up the extents into LCN regions</span></span>
    3.  <span data-ttu-id="fe62e-135">УСЕЧЕНИЕ файла округляет вверх и вниз по неправильным регионам, передаваемым в TRIM</span><span class="sxs-lookup"><span data-stu-id="fe62e-135">File TRIM rounds up and down for mis-aligned regions that are passed into TRIM</span></span>
    4.  <span data-ttu-id="fe62e-136">УСЕЧЕНИЕ файлов очищает записи в кэше, связанные с областями УСЕЧЕНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe62e-136">File TRIM purges entries in the cache that relate to the TRIM areas</span></span>
    5.  <span data-ttu-id="fe62e-137">УСЕЧЕНИЕ файлов передает IOCTL \_ DSM (Trim) на регион</span><span class="sxs-lookup"><span data-stu-id="fe62e-137">File TRIM passes IOCTL\_DSM (Trim) per region</span></span>
2.  <span data-ttu-id="fe62e-138">УСЕЧЕНИЕ файла Возвращает или ошибку</span><span class="sxs-lookup"><span data-stu-id="fe62e-138">File TRIM returns or errors</span></span>
    1.  <span data-ttu-id="fe62e-139">Проверка на наличие ошибок выполняется по допустимости входных данных</span><span class="sxs-lookup"><span data-stu-id="fe62e-139">Error checking is done on input validity</span></span>
    2.  <span data-ttu-id="fe62e-140">Если допустимы только некоторые экстенты, то для полного вызова API возвращается одна ошибка.</span><span class="sxs-lookup"><span data-stu-id="fe62e-140">If only some of the extents are valid, one error is returned for the complete API call</span></span>

<span data-ttu-id="fe62e-141">**Варианты использования**</span><span class="sxs-lookup"><span data-stu-id="fe62e-141">**Use cases**</span></span>

<span data-ttu-id="fe62e-142">**Виртуальный жесткий диск-потребитель (VHD), подключенный к SSD:**</span><span class="sxs-lookup"><span data-stu-id="fe62e-142">**Consumer virtual hard disk (VHD) mounted on an SSD:**</span></span>

<span data-ttu-id="fe62e-143">Виртуальный жесткий диск изначально монтируется на чисто неиспользуемом носителе.</span><span class="sxs-lookup"><span data-stu-id="fe62e-143">The VHD is initially mounted on ‘clean’ unused media.</span></span> <span data-ttu-id="fe62e-144">По мере использования виртуального жесткого диска VHD использует части носителя хранилища для файлов и т. д. При удалении файлов на носителе эти файлы не удаляются из SSD, так как полный виртуальный жесткий диск хранится в виде одного файла на SSD.</span><span class="sxs-lookup"><span data-stu-id="fe62e-144">As the VHD is used, the VHD consumes parts of the storage media for files, etc. When it deletes files in the storage media, these files are not removed from the SSD since the complete VHD is stored as one file on the SSD.</span></span> <span data-ttu-id="fe62e-145">Среда Hyper-V вызывает УСЕЧЕНИЕ файлов для всех регионов, удаленных при выполнении Delete-file в среде VHD.</span><span class="sxs-lookup"><span data-stu-id="fe62e-145">The Hyper-V environment calls File TRIM for all regions that are deleted when delete-file occurs in the VHD environment.</span></span> <span data-ttu-id="fe62e-146">Усечения файлов \_ преобразуются в SSD, чтобы можно было оптимизировать производительность SSD.</span><span class="sxs-lookup"><span data-stu-id="fe62e-146">The File\_TRIMs are translated to the SSD so that the SSD performance can be optimized.</span></span>

<span data-ttu-id="fe62e-147">**Потребительский виртуальный жесткий диск, подключенный к виртуальной сети SAN с тонкой подготовкой:**</span><span class="sxs-lookup"><span data-stu-id="fe62e-147">**Consumer VHD mounted on a thinly provisioned SAN:**</span></span>

<span data-ttu-id="fe62e-148">Виртуальный жесткий диск изначально монтируется на одной минимальной версии среды с тонкой подготовкой.</span><span class="sxs-lookup"><span data-stu-id="fe62e-148">The VHD is initially mounted on one minimum slab of a thinly provisioned environment.</span></span> <span data-ttu-id="fe62e-149">По мере того как файлы хранятся на виртуальном жестком диске, объем хранилища VHD увеличивается на несколько слоев.</span><span class="sxs-lookup"><span data-stu-id="fe62e-149">As files are stored in the VHD, the storage footprint of the VHD grows in multiples of slabs.</span></span> <span data-ttu-id="fe62e-150">При удалении файлов на виртуальном жестком диске этот файл обращается \_ к базовой виртуальной сети SAN с тонкой подготовкой.</span><span class="sxs-lookup"><span data-stu-id="fe62e-150">When files are removed in the VHD, the Hyper-V calls File\_TRIM to the underlying thinly provisioned SAN.</span></span> <span data-ttu-id="fe62e-151">Если обрезка больше, чем гранулярность слоев, SAN теперь может удалить коллекцию и, таким образом, уменьшить объем виртуального жесткого диска в этой сети SAN.</span><span class="sxs-lookup"><span data-stu-id="fe62e-151">If the TRIMs are bigger than the SLAB granularity, the SAN can now remove a SLAB and hence reduce the footprint of the VHD on that SAN.</span></span>

<span data-ttu-id="fe62e-152">Если виртуальный жесткий диск находится на сервере под управлением Windows 8, то оптимизатор хранилища также будет отсылать УСЕЧЕНИЯ, чтобы уменьшить объем памяти виртуального жесткого диска в подключенном виртуальном жестком диске.</span><span class="sxs-lookup"><span data-stu-id="fe62e-152">If the VHD is resident on a Windows 8 based server, the Storage Optimizer will also send TRIMs to reduce the slab footprint of the VHD from within the mounted VHD.</span></span>

## <a name="tests"></a><span data-ttu-id="fe62e-153">Тесты</span><span class="sxs-lookup"><span data-stu-id="fe62e-153">Tests</span></span>

<span data-ttu-id="fe62e-154">В более ранних выпусках операционной системы нет сопоставимых API.</span><span class="sxs-lookup"><span data-stu-id="fe62e-154">There are no comparable APIs in earlier operating system releases.</span></span> <span data-ttu-id="fe62e-155">Фактический интерфейс API не должен влиять на производительность, хотя носитель для хранения данных (Если реализован правильно) может улучшить производительность записи.</span><span class="sxs-lookup"><span data-stu-id="fe62e-155">There should be no performance impact from the actual API itself, though the storage media (if implemented correctly) can show better write performance.</span></span> <span data-ttu-id="fe62e-156">API следует использовать очень осторожно; передаваться только те экстенты, которые больше не нужны, так как эти экстенты будут окончательно удалены с носителя хранилища.</span><span class="sxs-lookup"><span data-stu-id="fe62e-156">The API should be used very carefully; only extents that are no longer needed should be passed down as those extents will be permanently removed from the storage media.</span></span>

## <a name="resources"></a><span data-ttu-id="fe62e-157">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="fe62e-157">Resources</span></span>

-   [<span data-ttu-id="fe62e-158">Спецификация T13</span><span class="sxs-lookup"><span data-stu-id="fe62e-158">T13 specification</span></span>](http://www.t13.org/Standards/Default.aspx?DocumentType=3)
-   [<span data-ttu-id="fe62e-159">Спецификация T10 SCSI</span><span class="sxs-lookup"><span data-stu-id="fe62e-159">T10 SCSI specification</span></span>](https://www.t10.org/)

 

 




