---
description: Представляет заголовок в виде многосекционной области.
ms.assetid: 0fad0e93-b940-4b52-be16-c5f177884dfb
title: Структура MULTI_SECTOR_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MULTI_SECTOR_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: ab21e17b83ae25286d2775d9dbd97dfd4cf493bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807061"
---
# <a name="multi_sector_header-structure"></a><span data-ttu-id="f1697-103">\_Структура заголовка с несколькими секторами \_</span><span class="sxs-lookup"><span data-stu-id="f1697-103">MULTI\_SECTOR\_HEADER structure</span></span>

<span data-ttu-id="f1697-104">\[Эта структура допустима только для томов NTFS версии 3; Он может быть изменен в будущих версиях.\]</span><span class="sxs-lookup"><span data-stu-id="f1697-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="f1697-105">Представляет заголовок в виде многосекционной области.</span><span class="sxs-lookup"><span data-stu-id="f1697-105">Represents the multisector header.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1697-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1697-106">Syntax</span></span>


```C++
typedef struct _MULTI_SECTOR_HEADER {
  UCHAR  Signature[4];
  USHORT UpdateSequenceArrayOffset;
  USHORT UpdateSequenceArraySize;
} MULTI_SECTOR_HEADER, *PMULTI_SECTOR_HEADER;
```



## <a name="members"></a><span data-ttu-id="f1697-107">Члены</span><span class="sxs-lookup"><span data-stu-id="f1697-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f1697-108">**Образец**</span><span class="sxs-lookup"><span data-stu-id="f1697-108">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="f1697-109">Сигнатура.</span><span class="sxs-lookup"><span data-stu-id="f1697-109">The signature.</span></span> <span data-ttu-id="f1697-110">Это значение является удобным для пользователя.</span><span class="sxs-lookup"><span data-stu-id="f1697-110">This value is a convenience to the user.</span></span>

</dd> <dt>

<span data-ttu-id="f1697-111">**упдатесекуенцеаррайоффсет**</span><span class="sxs-lookup"><span data-stu-id="f1697-111">**UpdateSequenceArrayOffset**</span></span>
</dt> <dd>

<span data-ttu-id="f1697-112">Смещение массива последовательностей обновления от начала этой структуры.</span><span class="sxs-lookup"><span data-stu-id="f1697-112">The offset to the update sequence array, from the start of this structure.</span></span> <span data-ttu-id="f1697-113">Массив последовательности обновления должен заканчиваться до последнего значения USHORT в первом секторе.</span><span class="sxs-lookup"><span data-stu-id="f1697-113">The update sequence array must end before the last USHORT value in the first sector.</span></span>

</dd> <dt>

<span data-ttu-id="f1697-114">**упдатесекуенцеаррайсизе**</span><span class="sxs-lookup"><span data-stu-id="f1697-114">**UpdateSequenceArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="f1697-115">Размер массива последовательностей обновления в байтах.</span><span class="sxs-lookup"><span data-stu-id="f1697-115">The size of the update sequence array, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1697-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1697-116">Remarks</span></span>

<span data-ttu-id="f1697-117">Обратите внимание, что для этой структуры нет связанного файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="f1697-117">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="f1697-118">Это определение структуры допустимо только для основной версии 3 и дополнительной версии 0 или 1, как сообщается [**фсктл \_ Получение \_ \_ \_ данных тома NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="f1697-118">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="f1697-119">Многосекторный заголовок и массив последовательностей обновления обеспечивают обнаружение неполных передач на нескольких секторах для устройств, размер физического сектора которых больше или равен индексу Stride (512) или не переносит секторы в неупорядоченном виде.</span><span class="sxs-lookup"><span data-stu-id="f1697-119">The multisector header and update sequence array provide detection of incomplete multisector transfers for devices that either have a physical sector size greater than or equal to the sequence number stride (512) or that do not transfer sectors out of order.</span></span> <span data-ttu-id="f1697-120">Если существует устройство, размер сектора которого меньше, чем шаг порядкового номера, и иногда передает секторы вне последовательности, то массив последовательности обновления не будет обеспечивать абсолютное обнаружение незавершенных передач.</span><span class="sxs-lookup"><span data-stu-id="f1697-120">If a device exists that has a sector size smaller than the sequence number stride and it sometimes transfers sectors out of order, then the update sequence array will not provide absolute detection of incomplete transfers.</span></span> <span data-ttu-id="f1697-121">Порядковый номер имеет небольшое количество, чтобы обеспечить абсолютную защиту для всех известных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="f1697-121">The sequence number stride is set to a small enough number to provide absolute protection for all known hard disks.</span></span> <span data-ttu-id="f1697-122">Это значение не меньше или может быть чрезмерным временем выполнения или небольшими затратами времени.</span><span class="sxs-lookup"><span data-stu-id="f1697-122">It is not set any smaller or there might be excessive run time or space overhead.</span></span>

<span data-ttu-id="f1697-123">Массив последовательностей обновления состоит из массива значений *n* **UShort** , где *n* — размер защищаемой структуры, разделенной порядковым номером STRIDE.</span><span class="sxs-lookup"><span data-stu-id="f1697-123">The update sequence array consists of an array of *n* **USHORT** values, where *n* is the size of the structure being protected divided by the sequence number stride.</span></span> <span data-ttu-id="f1697-124">Первое слово содержит порядковый номер обновления, который является циклическим счетчиком количества операций, содержащихся в структуре, записанной на диск.</span><span class="sxs-lookup"><span data-stu-id="f1697-124">The first word contains the update sequence number, which is a cyclical counter of the number of times the containing structure has been written to disk.</span></span> <span data-ttu-id="f1697-125">Далее представлены *n* сохраненных значений **UShort** , которые были перезаписаны порядковым номером обновления во время последнего занесения содержащей его структуры на диск.</span><span class="sxs-lookup"><span data-stu-id="f1697-125">Next are the *n* saved **USHORT** values that were overwritten by the update sequence number the last time the containing structure was written to disk.</span></span>

<span data-ttu-id="f1697-126">Каждый раз, когда защищенная структура собирается записываться на диск, Последнее слово в каждом порядковом номере STRIDE сохраняется в соответствующую ему точку в массиве порядковых номеров, а затем перезаписывается следующим порядковым номером обновления.</span><span class="sxs-lookup"><span data-stu-id="f1697-126">Each time the protected structure is about to be written to disk, the last word in each sequence number stride is saved to its respective position in the sequence number array, then it is overwritten with the next update sequence number.</span></span> <span data-ttu-id="f1697-127">После записи или при считывании структуры сохраненное слово из массива порядковых номеров восстанавливается до фактической его расположения в структуре.</span><span class="sxs-lookup"><span data-stu-id="f1697-127">After the write, or whenever the structure is read, the saved word from the sequence number array is restored to its actual position in the structure.</span></span> <span data-ttu-id="f1697-128">Перед восстановлением сохраненных слов при чтении все порядковые номера в конце каждого шага сравниваются с фактическим порядковым номером в начале массива.</span><span class="sxs-lookup"><span data-stu-id="f1697-128">Before restoring the saved words on reads, all the sequence numbers at the end of each stride are compared with the actual sequence number at the start of the array.</span></span> <span data-ttu-id="f1697-129">Если какое-либо из этих сравнений не равно, обнаружено неудачное Многосекторное перемещение.</span><span class="sxs-lookup"><span data-stu-id="f1697-129">If any of these comparisons are not equal, then a failed multisector transfer has been detected.</span></span>

<span data-ttu-id="f1697-130">Размер массива определяется размером содержащей его структуры.</span><span class="sxs-lookup"><span data-stu-id="f1697-130">The size of the array is determined by the size of the containing structure.</span></span> <span data-ttu-id="f1697-131">Массив последовательностей обновления должен быть включен в конец заголовка структуры, с которой он защищается из-за его размера переменной.</span><span class="sxs-lookup"><span data-stu-id="f1697-131">The update sequence array should be included at the end of the header of the structure it is protecting because of its variable size.</span></span> <span data-ttu-id="f1697-132">Пользователь должен убедиться, что для содержащей структуры зарезервировано правильное место: (размер структуры/512 + 1) \* sizeof (UShort).</span><span class="sxs-lookup"><span data-stu-id="f1697-132">The user must ensure that the correct space is reserved for the containing structure: (size of structure / 512 + 1) \* sizeof(USHORT).</span></span>

## <a name="see-also"></a><span data-ttu-id="f1697-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1697-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1697-134">Основная таблица файлов</span><span class="sxs-lookup"><span data-stu-id="f1697-134">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
