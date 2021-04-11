---
description: Представляет сегмент записи файла. Это заголовок для каждого сегмента записи файла в главной таблице файлов (MFT).
ms.assetid: 4548ad49-1924-4888-8966-c45f8e453c6f
title: Структура FILE_RECORD_SEGMENT_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_RECORD_SEGMENT_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 293bb14dbaee0853aa1ef293502724458e02e26f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262520"
---
# <a name="file_record_segment_header-structure"></a><span data-ttu-id="da974-104">\_ \_ Структура заголовка сегмента записи файла \_</span><span class="sxs-lookup"><span data-stu-id="da974-104">FILE\_RECORD\_SEGMENT\_HEADER structure</span></span>

<span data-ttu-id="da974-105">\[Эта структура допустима только для томов NTFS версии 3; Он может быть изменен в будущих версиях.\]</span><span class="sxs-lookup"><span data-stu-id="da974-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="da974-106">Представляет сегмент записи файла.</span><span class="sxs-lookup"><span data-stu-id="da974-106">Represents the file record segment.</span></span> <span data-ttu-id="da974-107">Это заголовок для каждого сегмента записи файла в главной таблице файлов (MFT).</span><span class="sxs-lookup"><span data-stu-id="da974-107">This is the header for each file record segment in the master file table (MFT).</span></span>

## <a name="syntax"></a><span data-ttu-id="da974-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da974-108">Syntax</span></span>


```C++
typedef struct _FILE_RECORD_SEGMENT_HEADER {
  MULTI_SECTOR_HEADER   MultiSectorHeader;
  ULONGLONG             Reserved1;
  USHORT                SequenceNumber;
  USHORT                Reserved2;
  USHORT                FirstAttributeOffset;
  USHORT                Flags;
  ULONG                 Reserved3[2];
  FILE_REFERENCE        BaseFileRecordSegment;
  USHORT                Reserved4;
  UPDATE_SEQUENCE_ARRAY UpdateSequenceArray;
} FILE_RECORD_SEGMENT_HEADER, *PFILE_RECORD_SEGMENT_HEADER;
```



## <a name="members"></a><span data-ttu-id="da974-109">Члены</span><span class="sxs-lookup"><span data-stu-id="da974-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="da974-110">**мултисекторхеадер**</span><span class="sxs-lookup"><span data-stu-id="da974-110">**MultiSectorHeader**</span></span>
</dt> <dd>

<span data-ttu-id="da974-111">Заголовок в многосекционе, определенный диспетчером кэша.</span><span class="sxs-lookup"><span data-stu-id="da974-111">The multisector header defined by the cache manager.</span></span> <span data-ttu-id="da974-112">Структура [**\_ \_ заголовка с несколькими секторами**](multi-sector-header.md) всегда содержит подпись "File" и описание расположения и размера массива последовательностей обновления.</span><span class="sxs-lookup"><span data-stu-id="da974-112">The [**MULTI\_SECTOR\_HEADER**](multi-sector-header.md) structure always contains the signature "FILE" and a description of the location and size of the update sequence array.</span></span>

</dd> <dt>

<span data-ttu-id="da974-113">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="da974-113">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="da974-114">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="da974-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="da974-115">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="da974-115">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="da974-116">Порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="da974-116">The sequence number.</span></span> <span data-ttu-id="da974-117">Это значение увеличивается каждый раз при освобождении сегмента записи файла; значение 0, если сегмент не используется.</span><span class="sxs-lookup"><span data-stu-id="da974-117">This value is incremented each time that a file record segment is freed; it is 0 if the segment is not used.</span></span> <span data-ttu-id="da974-118">Поле **SequenceNumber** в ссылке на файл должно соответствовать содержимому этого поля; Если они не совпадают, ссылка на файл неверна и, вероятно, устарела.</span><span class="sxs-lookup"><span data-stu-id="da974-118">The **SequenceNumber** field of a file reference must match the contents of this field; if they do not match, the file reference is incorrect and probably obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="da974-119">**Reserved2**</span><span class="sxs-lookup"><span data-stu-id="da974-119">**Reserved2**</span></span>
</dt> <dd>

<span data-ttu-id="da974-120">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="da974-120">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="da974-121">**фирстаттрибутеоффсет**</span><span class="sxs-lookup"><span data-stu-id="da974-121">**FirstAttributeOffset**</span></span>
</dt> <dd>

<span data-ttu-id="da974-122">Смещение первой записи атрибута в байтах.</span><span class="sxs-lookup"><span data-stu-id="da974-122">The offset of the first attribute record, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="da974-123">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="da974-123">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="da974-124">Флаги файла.</span><span class="sxs-lookup"><span data-stu-id="da974-124">The file flags.</span></span>

<dl> <dt>

<span data-ttu-id="da974-125"><span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**Файл \_ \_ \_ \_ Используемый сегмент записи** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="da974-125"><span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**FILE\_RECORD\_SEGMENT\_IN\_USE** (0x0001)</span></span>
</dt> <dt>

<span data-ttu-id="da974-126"><span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**Файл \_ \_ \_ \_ Имеется индекс имени файла** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="da974-126"><span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**FILE\_FILE\_NAME\_INDEX\_PRESENT** (0x0002)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="da974-127">**Reserved3**</span><span class="sxs-lookup"><span data-stu-id="da974-127">**Reserved3**</span></span>
</dt> <dd>

<span data-ttu-id="da974-128">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="da974-128">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="da974-129">**басефилерекордсегмент**</span><span class="sxs-lookup"><span data-stu-id="da974-129">**BaseFileRecordSegment**</span></span>
</dt> <dd>

<span data-ttu-id="da974-130">Ссылка на файл основного сегмента записи файла для этого файла.</span><span class="sxs-lookup"><span data-stu-id="da974-130">A file reference to the base file record segment for this file.</span></span> <span data-ttu-id="da974-131">Если это базовая запись файла, значение равно 0.</span><span class="sxs-lookup"><span data-stu-id="da974-131">If this is the base file record, the value is 0.</span></span> <span data-ttu-id="da974-132">См [**. \_ \_ Справочник по сегментам MFT**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="da974-132">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="da974-133">**Reserved4**</span><span class="sxs-lookup"><span data-stu-id="da974-133">**Reserved4**</span></span>
</dt> <dd>

<span data-ttu-id="da974-134">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="da974-134">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="da974-135">**упдатесекуенцеаррай**</span><span class="sxs-lookup"><span data-stu-id="da974-135">**UpdateSequenceArray**</span></span>
</dt> <dd>

<span data-ttu-id="da974-136">Массив последовательностей обновления для защиты многосекционных передач сегмента записи файла.</span><span class="sxs-lookup"><span data-stu-id="da974-136">The update sequence array to protect multisector transfers of the file record segment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da974-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da974-137">Remarks</span></span>

<span data-ttu-id="da974-138">Обратите внимание, что для этой структуры нет связанного файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="da974-138">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="da974-139">Это определение структуры допустимо только для основной версии 3 и дополнительной версии 0 или 1, как сообщается [**фсктл \_ Получение \_ \_ \_ данных тома NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="da974-139">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="da974-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da974-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da974-141">Основная таблица файлов</span><span class="sxs-lookup"><span data-stu-id="da974-141">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
