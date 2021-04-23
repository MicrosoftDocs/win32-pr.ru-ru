---
description: Содержит сведения о распознавании файловой системы на диске, которые хранятся в загрузочном секторе томов (ноль сектора логического диска).
ms.assetid: d9c19e01-ff82-4bbc-9eb6-aac9dc5c34ac
title: Структура FILE_SYSTEM_RECOGNITION_STRUCTURE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_SYSTEM_RECOGNITION_STRUCTURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: c542b2b9ee1cd1696c7c95797c7df20aa02180cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080549"
---
# <a name="file_system_recognition_structure-structure"></a><span data-ttu-id="1b553-103">\_ \_ Структура распознавания файловой \_ системы</span><span class="sxs-lookup"><span data-stu-id="1b553-103">FILE\_SYSTEM\_RECOGNITION\_STRUCTURE structure</span></span>

<span data-ttu-id="1b553-104">Содержит сведения о распознавании файловой системы на диске, хранящиеся в загрузочном секторе тома (ноль в логическом секторе диска).</span><span class="sxs-lookup"><span data-stu-id="1b553-104">Contains the on-disk file system recognition information stored in the volume's boot sector (logical disk sector zero).</span></span>

<span data-ttu-id="1b553-105">Это внутренняя структура данных, недоступная в общедоступном заголовке и предоставляемая здесь для разработчиков файловой системы, желающих воспользоваться преимуществами распознавания файловой системы.</span><span class="sxs-lookup"><span data-stu-id="1b553-105">This is an internally-defined data structure not available in a public header and is provided here for file system developers who want to take advantage of file system recognition.</span></span> <span data-ttu-id="1b553-106">Дополнительные сведения см. в разделе [Распознавание файловой системы](file-system-recognition.md).</span><span class="sxs-lookup"><span data-stu-id="1b553-106">For more information, see [File System Recognition](file-system-recognition.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1b553-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b553-107">Syntax</span></span>


```C++
typedef struct _FILE_SYSTEM_RECOGNITION_STRUCTURE {
  UCHAR  Jmp[3];
  UCHAR  FsName[8];
  UCHAR  MustBeZero[5];
  ULONG  Identifier;
  USHORT Length;
  USHORT Checksum;
} FILE_SYSTEM_RECOGNITION_STRUCTURE;
```



## <a name="members"></a><span data-ttu-id="1b553-108">Члены</span><span class="sxs-lookup"><span data-stu-id="1b553-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="1b553-109">**Переход**</span><span class="sxs-lookup"><span data-stu-id="1b553-109">**Jmp**</span></span>
</dt> <dd>

<span data-ttu-id="1b553-110">Инструкция переход.</span><span class="sxs-lookup"><span data-stu-id="1b553-110">The JMP instruction.</span></span> <span data-ttu-id="1b553-111">Этот элемент данных не включается в значение, содержащееся в элементе данных **контрольной суммы** .</span><span class="sxs-lookup"><span data-stu-id="1b553-111">This data member is not included in the value contained in the **Checksum** data member.</span></span>

</dd> <dt>

<span data-ttu-id="1b553-112">**Имя файловой системы**</span><span class="sxs-lookup"><span data-stu-id="1b553-112">**FsName**</span></span>
</dt> <dd>

<span data-ttu-id="1b553-113">Имя файловой системы.</span><span class="sxs-lookup"><span data-stu-id="1b553-113">The file system name.</span></span> <span data-ttu-id="1b553-114">Это последовательность из 8 символов ASCII, представляющих нелокализованное удобное имя файловой системы, с которым отформатирован том.</span><span class="sxs-lookup"><span data-stu-id="1b553-114">This is a sequence of 8 ASCII characters that represents the nonlocalizable human-readable name of the file system the volume is formatted with.</span></span>

<span data-ttu-id="1b553-115">Эта строка находится в том же месте, что и имя файловой системы изготовителя оборудования на диске с обычной структурой блока параметров BIOS (БПБ).</span><span class="sxs-lookup"><span data-stu-id="1b553-115">This string is in the same place as the OEM file system name on a disk with a normal BIOS parameter block (BPB) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1b553-116">**мустбезеро**</span><span class="sxs-lookup"><span data-stu-id="1b553-116">**MustBeZero**</span></span>
</dt> <dd>

<span data-ttu-id="1b553-117">Зарезервированное пространство, содержащее все нули.</span><span class="sxs-lookup"><span data-stu-id="1b553-117">Reserved space that contains all zeros.</span></span>

<span data-ttu-id="1b553-118">Этот элемент данных перекрывает то, что обычно являются следующими элементами данных в БПБ:</span><span class="sxs-lookup"><span data-stu-id="1b553-118">This data member overlaps what normally are the following data members in a BPB:</span></span>

-   <span data-ttu-id="1b553-119">**битесперсектор**</span><span class="sxs-lookup"><span data-stu-id="1b553-119">**BytesPerSector**</span></span>
-   <span data-ttu-id="1b553-120">**секторсперклустер**</span><span class="sxs-lookup"><span data-stu-id="1b553-120">**SectorsPerCluster**</span></span>
-   <span data-ttu-id="1b553-121">**ресерведсекторкаунт**</span><span class="sxs-lookup"><span data-stu-id="1b553-121">**ReservedSectorCount**</span></span>

<span data-ttu-id="1b553-122">Поскольку эти элементы данных имеют нулевое значение, это должно быть достаточно для того, чтобы предыдущие ОС задали, что это не является допустимым БПБ и, таким образом, распознает том.</span><span class="sxs-lookup"><span data-stu-id="1b553-122">Because these data members are set to zero, this should be sufficient to cause earlier OSs to conclude that this is not a valid BPB and therefore recognize the volume.</span></span>

</dd> <dt>

<span data-ttu-id="1b553-123">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="1b553-123">**Identifier**</span></span>
</dt> <dd>

<span data-ttu-id="1b553-124">Идентификатор структуры.</span><span class="sxs-lookup"><span data-stu-id="1b553-124">A structure identifier.</span></span> <span data-ttu-id="1b553-125">Должен содержать значение 0x53525346, упорядоченное с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="1b553-125">Must contain the value 0x53525346 arranged in little-endian byte order.</span></span>

<span data-ttu-id="1b553-126">На этом этапе структуры данные выровняйтеся до 16 байт.</span><span class="sxs-lookup"><span data-stu-id="1b553-126">At this point in the structure, the data is aligned to 16 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1b553-127">**Длина**</span><span class="sxs-lookup"><span data-stu-id="1b553-127">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="1b553-128">Число байтов в этой структуре от начала до конца, включая элемент данных **Переход** .</span><span class="sxs-lookup"><span data-stu-id="1b553-128">The number of bytes in this structure, from the beginning to the end, including the **Jmp** data member.</span></span>

</dd> <dt>

<span data-ttu-id="1b553-129">**Вычислен**</span><span class="sxs-lookup"><span data-stu-id="1b553-129">**Checksum**</span></span>
</dt> <dd>

<span data-ttu-id="1b553-130">Двухбайтовое значение CHECKSUM, вычисленное для байтов, начиная с элемента данных **имя файловой системы** и заканчивая последним байтом этой структуры, за исключением элементов данных **Переход** и **CHECKSUM** .</span><span class="sxs-lookup"><span data-stu-id="1b553-130">A two-byte checksum calculated over the bytes starting at the **FsName** data member and ending at the last byte of this structure, excluding the **Jmp** and **Checksum** data members.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b553-131">Требования</span><span class="sxs-lookup"><span data-stu-id="1b553-131">Requirements</span></span>



| <span data-ttu-id="1b553-132">Требование</span><span class="sxs-lookup"><span data-stu-id="1b553-132">Requirement</span></span> | <span data-ttu-id="1b553-133">Значение</span><span class="sxs-lookup"><span data-stu-id="1b553-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="1b553-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b553-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1b553-135">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1b553-135">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="1b553-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b553-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1b553-137">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1b553-137">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1b553-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b553-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b553-139">Вычисление контрольной суммы распознавания файловой системы</span><span class="sxs-lookup"><span data-stu-id="1b553-139">Computing a File System Recognition Checksum</span></span>](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[<span data-ttu-id="1b553-140">Распознавание файловой системы</span><span class="sxs-lookup"><span data-stu-id="1b553-140">File System Recognition</span></span>](file-system-recognition.md)
</dt> <dt>

[<span data-ttu-id="1b553-141">**\_ \_ сведения о распознавании файловой системы \_**</span><span class="sxs-lookup"><span data-stu-id="1b553-141">**FILE\_SYSTEM\_RECOGNITION\_INFORMATION**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-file_system_recognition_information)
</dt> <dt>

[<span data-ttu-id="1b553-142">**\_ \_ \_ Распознавание файловых систем запросов \_ фсктл**</span><span class="sxs-lookup"><span data-stu-id="1b553-142">**FSCTL\_QUERY\_FILE\_SYSTEM\_RECOGNITION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

