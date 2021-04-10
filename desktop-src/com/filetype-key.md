---
title: Ключ FileType
description: Используется Жетклассфиле для сопоставления шаблонов с различными байтами файлов в несоставном файле.
ms.assetid: ced23cdb-c184-43fe-ba37-fe1af8664b66
keywords:
- Ключ реестра FileType-COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2e331588b627ee5ce9a9c1b69631f1e8a1dbe4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068540"
---
# <a name="filetype-key"></a><span data-ttu-id="3b756-104">Ключ FileType</span><span class="sxs-lookup"><span data-stu-id="3b756-104">FileType Key</span></span>

<span data-ttu-id="3b756-105">Используется [**жетклассфиле**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) для сопоставления шаблонов с различными байтами файлов в несоставном файле.</span><span class="sxs-lookup"><span data-stu-id="3b756-105">Used by [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) to match patterns against various file bytes in a non-compound file.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="3b756-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="3b756-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\FileType
   {CLSID}
      n = offset, cb, mask, value
```

<dl> <dt>

<span data-ttu-id="3b756-107"><span id="offset"></span><span id="OFFSET"></span>*собой*</span><span class="sxs-lookup"><span data-stu-id="3b756-107"><span id="offset"></span><span id="OFFSET"></span>*offset*</span></span>
</dt> <dd>

<span data-ttu-id="3b756-108">Определяет, насколько далеко от начала или конца файла начинается сравнение.</span><span class="sxs-lookup"><span data-stu-id="3b756-108">Determines how far from the beginning or end of the file to begin the comparison.</span></span> <span data-ttu-id="3b756-109">Если смещение является отрицательным значением, сравнение начинается с конца файла за вычетом значения смещения.</span><span class="sxs-lookup"><span data-stu-id="3b756-109">If the offset is a negative value, the comparison begins from the end of the file minus the offset value.</span></span> <span data-ttu-id="3b756-110">Значение смещения является десятичным типом, если не предшествует "0x".</span><span class="sxs-lookup"><span data-stu-id="3b756-110">The offset value is a decimal type unless preceded by "0x".</span></span>

</dd> <dt>

<span data-ttu-id="3b756-111"><span id="cb"></span><span id="CB"></span>*CB*</span><span class="sxs-lookup"><span data-stu-id="3b756-111"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="3b756-112">Представляет длину в байтах от начала до конца файла.</span><span class="sxs-lookup"><span data-stu-id="3b756-112">Represents the length in bytes from the beginning to the end of the file.</span></span> <span data-ttu-id="3b756-113">Представляет диапазон байтов в файле.</span><span class="sxs-lookup"><span data-stu-id="3b756-113">Represents the byte range in the file.</span></span> <span data-ttu-id="3b756-114">Значение *CB* является десятичным, если не предшествует "0x".</span><span class="sxs-lookup"><span data-stu-id="3b756-114">The *cb* value is a decimal unless preceded by "0x".</span></span>

</dd> <dt>

<span data-ttu-id="3b756-115"><span id="mask"></span><span id="MASK"></span>*виде*</span><span class="sxs-lookup"><span data-stu-id="3b756-115"><span id="mask"></span><span id="MASK"></span>*mask*</span></span>
</dt> <dd>

<span data-ttu-id="3b756-116">Двоичное значение, используемое для маскирования, которое выполняется с помощью логической операции AND и диапазона байтов, заданного *offset* и *CB*.</span><span class="sxs-lookup"><span data-stu-id="3b756-116">A binary value used for masking, which is performed by using a logical AND operation, and the byte range specified by *offset* and *cb*.</span></span> <span data-ttu-id="3b756-117">Если это значение не указано, все байты задаются как все.</span><span class="sxs-lookup"><span data-stu-id="3b756-117">If this value is omitted, the bytes are set to all ones.</span></span> <span data-ttu-id="3b756-118">Это значение всегда является шестнадцатеричным.</span><span class="sxs-lookup"><span data-stu-id="3b756-118">This value is always hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="3b756-119"><span id="value"></span><span id="VALUE"></span>*значений*</span><span class="sxs-lookup"><span data-stu-id="3b756-119"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="3b756-120">Представляет шаблон, который должен совпадать для файла с этим типом файла.</span><span class="sxs-lookup"><span data-stu-id="3b756-120">Represents the pattern that must match for a file to be of this file type.</span></span> <span data-ttu-id="3b756-121">Шаблон используется для правильного обнаружения известного формата файла по его содержимому, а не по его расширению.</span><span class="sxs-lookup"><span data-stu-id="3b756-121">The pattern is used to properly identify a known file format from its contents, not by its extension.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b756-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b756-122">Remarks</span></span>

<span data-ttu-id="3b756-123">Записи используются функцией [**жетклассфиле**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) для сопоставления шаблонов с различными байтами файлов в несоставном файле.</span><span class="sxs-lookup"><span data-stu-id="3b756-123">Entries are used by the [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) function to match patterns against various file bytes in a non-compound file.</span></span> <span data-ttu-id="3b756-124">**Тип_файла** имеет подразделы CLSID, каждый из которых имеет ряд подразделов **0**, **1**, **2**, **3**.</span><span class="sxs-lookup"><span data-stu-id="3b756-124">**FileType** has CLSID subkeys, each of which has a series of subkeys **0**, **1**, **2**, **3**.</span></span> <span data-ttu-id="3b756-125">Эти значения содержат закономерности, которые, если таковые совпадают, дают указанный идентификатор CLSID.</span><span class="sxs-lookup"><span data-stu-id="3b756-125">These values contain patterns that, if one matches, yield the indicated CLSID.</span></span> <span data-ttu-id="3b756-126">Например, значение "0, 4, FFFFFFFF, ABCD1234" указывает, что первые 4 байта должны быть ABCD1234 в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="3b756-126">For example, a value of "0, 4, FFFFFFFF, ABCD1234" indicates that the first 4 bytes must be ABCD1234, in that order.</span></span> <span data-ttu-id="3b756-127">Значение "-4, 4, ФЕФЕФЕФЕ" указывает, что последние четыре байта в файле должны быть ФЕФЕФЕФЕ.</span><span class="sxs-lookup"><span data-stu-id="3b756-127">A value of "-4, 4, FEFEFEFE " indicates that the last four bytes in the file must be FEFEFEFE.</span></span> <span data-ttu-id="3b756-128">Если любой из шаблонов соответствует, возвращается идентификатор CLSID.</span><span class="sxs-lookup"><span data-stu-id="3b756-128">If either pattern matches, the CLSID is returned.</span></span>

<span data-ttu-id="3b756-129">Ключ **\_ \_ \\ \\ классов программного обеспечения файла hKey на локальном компьютере** соответствует **\_ \_ корневому ключу classes** , который был сохранен для совместимости с предыдущими версиями com.</span><span class="sxs-lookup"><span data-stu-id="3b756-129">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b756-130">См. также</span><span class="sxs-lookup"><span data-stu-id="3b756-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b756-131">**<\_ расширение файла>**</span><span class="sxs-lookup"><span data-stu-id="3b756-131">**<file\_extension>**</span></span>](-file-extension--key.md)
</dt> <dt>

[<span data-ttu-id="3b756-132">**жетклассфиле**</span><span class="sxs-lookup"><span data-stu-id="3b756-132">**GetClassFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




