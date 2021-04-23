---
description: Представляет адрес в основной таблице файлов (MFT). Адрес помечается с помощью циклического повторно используемого порядкового номера, который задается в момент, когда ссылка на сегмент MFT является допустимой.
ms.assetid: 59d83b95-83fb-4630-8ce4-f58441c748ab
title: Структура MFT_SEGMENT_REFERENCE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFT_SEGMENT_REFERENCE
api_type:
- NA
api_location: ''
ms.openlocfilehash: beabe7620dadd01b25b3556715b33e2f10c2c230
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140747"
---
# <a name="mft_segment_reference-structure"></a><span data-ttu-id="4ad8a-104">\_ \_ Структура ссылки на сегмент MFT</span><span class="sxs-lookup"><span data-stu-id="4ad8a-104">MFT\_SEGMENT\_REFERENCE structure</span></span>

<span data-ttu-id="4ad8a-105">\[Эта структура допустима только для томов NTFS версии 3; Он может быть изменен в будущих версиях.\]</span><span class="sxs-lookup"><span data-stu-id="4ad8a-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="4ad8a-106">Представляет адрес в основной таблице файлов (MFT).</span><span class="sxs-lookup"><span data-stu-id="4ad8a-106">Represents an address in the master file table (MFT).</span></span> <span data-ttu-id="4ad8a-107">Адрес помечается с помощью циклического повторно используемого порядкового номера, который задается в момент, когда ссылка на сегмент MFT является допустимой.</span><span class="sxs-lookup"><span data-stu-id="4ad8a-107">The address is tagged with a circularly reused sequence number that is set at the time the MFT segment reference was valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ad8a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ad8a-108">Syntax</span></span>


```C++
typedef struct _MFT_SEGMENT_REFERENCE {
  ULONG  SegmentNumberLowPart;
  USHORT SegmentNumberHighPart;
  USHORT SequenceNumber;
} MFT_SEGMENT_REFERENCE, *PMFT_SEGMENT_REFERENCE;
```



## <a name="members"></a><span data-ttu-id="4ad8a-109">Члены</span><span class="sxs-lookup"><span data-stu-id="4ad8a-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="4ad8a-110">**сегментнумберловпарт**</span><span class="sxs-lookup"><span data-stu-id="4ad8a-110">**SegmentNumberLowPart**</span></span>
</dt> <dd>

<span data-ttu-id="4ad8a-111">Нижняя часть номера сегмента.</span><span class="sxs-lookup"><span data-stu-id="4ad8a-111">The low part of the segment number.</span></span>

</dd> <dt>

<span data-ttu-id="4ad8a-112">**сегментнумберхигхпарт**</span><span class="sxs-lookup"><span data-stu-id="4ad8a-112">**SegmentNumberHighPart**</span></span>
</dt> <dd>

<span data-ttu-id="4ad8a-113">Старшая часть номера сегмента.</span><span class="sxs-lookup"><span data-stu-id="4ad8a-113">The high part of the segment number.</span></span>

</dd> <dt>

<span data-ttu-id="4ad8a-114">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="4ad8a-114">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="4ad8a-115">Ненулевой порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="4ad8a-115">The nonzero sequence number.</span></span> <span data-ttu-id="4ad8a-116">Значение 0 зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="4ad8a-116">The value 0 is reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ad8a-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ad8a-117">Remarks</span></span>

<span data-ttu-id="4ad8a-118">Обратите внимание, что для этой структуры нет связанного файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="4ad8a-118">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="4ad8a-119">Это определение структуры допустимо только для основной версии 3 и дополнительной версии 0 или 1, как сообщается [**фсктл \_ Получение \_ \_ \_ данных тома NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="4ad8a-119">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="4ad8a-120">Тип **данных \_ ссылки на файл** определяется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="4ad8a-120">The **FILE\_REFERENCE** data type is defined as follows.</span></span>

``` syntax
typedef MFT_SEGMENT_REFERENCE FILE_REFERENCE, *PFILE_REFERENCE;
```

## <a name="see-also"></a><span data-ttu-id="4ad8a-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ad8a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ad8a-122">Основная таблица файлов</span><span class="sxs-lookup"><span data-stu-id="4ad8a-122">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
