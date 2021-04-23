---
title: Имена в IStorage
description: Набор свойств определяется с помощью идентификатора формата (FMTID) в интерфейсе IPropertySetStorage.
ms.assetid: 5f8eba37-c589-413e-9971-7ecb01dc6734
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cef9417f2f5fad7fd17dcc3d431f1d3565a3843
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532495"
---
# <a name="names-in-istorage"></a><span data-ttu-id="f5a56-103">Имена в IStorage</span><span class="sxs-lookup"><span data-stu-id="f5a56-103">Names in IStorage</span></span>

<span data-ttu-id="f5a56-104">Набор свойств определяется с помощью идентификатора формата (FMTID) в интерфейсе [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) .</span><span class="sxs-lookup"><span data-stu-id="f5a56-104">A property set is identified with a format identifier (FMTID) in the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface.</span></span> <span data-ttu-id="f5a56-105">В интерфейсе [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) набор свойств имеет имя с завершающей нулем строкой Юникода с максимальной длиной 32 символов.</span><span class="sxs-lookup"><span data-stu-id="f5a56-105">In the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface, a property set is named with a null-terminated Unicode string with a maximum length of 32 characters.</span></span> <span data-ttu-id="f5a56-106">Чтобы обеспечить взаимодействие, необходимо установить сопоставление между FMTID и соответствующей строкой Юникода, заканчивающейся нулем.</span><span class="sxs-lookup"><span data-stu-id="f5a56-106">To enable interoperability, a mapping between an FMTID and a corresponding null-terminated Unicode string must be established.</span></span>

## <a name="converting-a-property-set-from-a-fmtid-to-a-string-name"></a><span data-ttu-id="f5a56-107">Преобразование набора свойств из FMTID в строковое имя</span><span class="sxs-lookup"><span data-stu-id="f5a56-107">Converting a property set from a FMTID to a string name</span></span>

<span data-ttu-id="f5a56-108">При преобразовании из FMTID в соответствующее строковое имя в Юникоде сначала убедитесь, что FMTID является хорошо известным значением, указанным в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f5a56-108">When converting from an FMTID to a corresponding Unicode string name, first verify that the FMTID is a well-known value, listed in the following table.</span></span> <span data-ttu-id="f5a56-109">Если это так, используйте соответствующее хорошо известное имя строки.</span><span class="sxs-lookup"><span data-stu-id="f5a56-109">If so, then use the corresponding well-known string name.</span></span>

| <span data-ttu-id="f5a56-110">FMTID</span><span class="sxs-lookup"><span data-stu-id="f5a56-110">FMTID</span></span>                                                                                | <span data-ttu-id="f5a56-111">Имя строки</span><span class="sxs-lookup"><span data-stu-id="f5a56-111">String name</span></span>                       | <span data-ttu-id="f5a56-112">Семантическ</span><span class="sxs-lookup"><span data-stu-id="f5a56-112">Semantic</span></span>                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f5a56-113">F29F85E0-4FF9-1068-AB91-08002B27B3D9</span><span class="sxs-lookup"><span data-stu-id="f5a56-113">F29F85E0-4FF9-1068-AB91-08002B27B3D9</span></span>                                                 | <span data-ttu-id="f5a56-114">" \\ 005SummaryInformation"</span><span class="sxs-lookup"><span data-stu-id="f5a56-114">"\\005SummaryInformation"</span></span>         | <span data-ttu-id="f5a56-115">Сводная информация о COM2</span><span class="sxs-lookup"><span data-stu-id="f5a56-115">COM2 summary information</span></span>                                         |
| <span data-ttu-id="f5a56-116">D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="f5a56-116">D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span><br/> | <span data-ttu-id="f5a56-117">" \\ 005DocumentSummaryInformation"</span><span class="sxs-lookup"><span data-stu-id="f5a56-117">"\\005DocumentSummaryInformation"</span></span> | <span data-ttu-id="f5a56-118">Сведения о документе Office и определяемые пользователем свойства.</span><span class="sxs-lookup"><span data-stu-id="f5a56-118">Office document summary information and user-defined properties.</span></span> |



 

> [!Note]  
> <span data-ttu-id="f5a56-119">Набор свойств **документсуммаринформатион** и **пользователяопределенные** уникален в том, что он содержит два раздела.</span><span class="sxs-lookup"><span data-stu-id="f5a56-119">The **DocumentSummaryInformation** and **UserDefined** property set is unique in that it contains two sections.</span></span> <span data-ttu-id="f5a56-120">В любом другом наборе свойств не разрешается использовать несколько разделов.</span><span class="sxs-lookup"><span data-stu-id="f5a56-120">Multiple sections are not permitted in any other property set.</span></span> <span data-ttu-id="f5a56-121">Дополнительные сведения см. в разделе [структурированное хранилище упорядоченный формат набора свойств](structured-storage-serialized-property-set-format.md), а [также в наборе свойств документсуммаринформатион и пользователяопределенные](the-documentsummaryinformation-and-userdefined-property-sets.md).</span><span class="sxs-lookup"><span data-stu-id="f5a56-121">For more information, see [Structured Storage Serialized Property Set Format](structured-storage-serialized-property-set-format.md), and [The DocumentSummaryInformation and UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md).</span></span> <span data-ttu-id="f5a56-122">Первый раздел был определен как часть COM; второй был определен с помощью Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="f5a56-122">The first section was defined as part of COM; the second was defined by Microsoft Office.</span></span>

 

<span data-ttu-id="f5a56-123">Если FMTID не является хорошо известным значением, используйте следующую процедуру, чтобы алгоритмически сформировать строковое имя.</span><span class="sxs-lookup"><span data-stu-id="f5a56-123">If the FMTID is not a well-known value, then use the following procedure to algorithmically form a string name.</span></span>

<span data-ttu-id="f5a56-124">**Преобразование строкового имени в алгоритмически**</span><span class="sxs-lookup"><span data-stu-id="f5a56-124">**To algorithmically form a string name**</span></span>

1.  <span data-ttu-id="f5a56-125">При необходимости преобразуйте FMTID в порядковый номер с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="f5a56-125">Convert the FMTID to little-endian byte order, if necessary.</span></span>
2.  <span data-ttu-id="f5a56-126">Возьмите 128 бит FMTID и рассматривайте их как одну длинную битовую строку путем сцепления каждого байта вместе.</span><span class="sxs-lookup"><span data-stu-id="f5a56-126">Take the 128 bits of the FMTID and consider them as one long bit string by concatenating each of the bytes together.</span></span> <span data-ttu-id="f5a56-127">Первый бит 128-разрядного значения — это наименее значащий бит первого байта в памяти FMTID; последний бит 128-битного значения — это наиболее значимый бит последнего байта в памяти FMTID.</span><span class="sxs-lookup"><span data-stu-id="f5a56-127">The first bit of the 128 bit value is the least significant bit of the first byte in memory of the FMTID; the last bit of the 128 bit value is the most significant bit of the last byte in memory of the FMTID.</span></span> <span data-ttu-id="f5a56-128">Расширьте эти 128 бит на 130 бит, добавив два нулевых бита в конец.</span><span class="sxs-lookup"><span data-stu-id="f5a56-128">Extend these 128 bits to 130 bits by adding two zero bits to the end.</span></span>
3.  <span data-ttu-id="f5a56-129">Разделите 130 бит на группы из пяти бит; будет составлять 26 таких групп.</span><span class="sxs-lookup"><span data-stu-id="f5a56-129">Divide the 130 bits into groups of five bits; there will be 26 such groups.</span></span> <span data-ttu-id="f5a56-130">Рассмотрите каждую группу как целое число с обратным приоритетом.</span><span class="sxs-lookup"><span data-stu-id="f5a56-130">Consider each group as an integer with reversed bit precedence.</span></span> <span data-ttu-id="f5a56-131">Например, первый из 128 бит является наименее значащим битом первой группы из пяти бит; Пятый из 128 бит является наиболее значащим битом первой группы.</span><span class="sxs-lookup"><span data-stu-id="f5a56-131">For example, the first of the 128 bits is the least significant bit of the first group of five bits; the fifth of the 128 bits is the most significant bit of the first group.</span></span>
4.  <span data-ttu-id="f5a56-132">Сопоставьте каждое из этих целых чисел в виде индекса в массиве 32 символов: ABCDEFGHIJKLMNOPQRSTUVWXYZ012345.</span><span class="sxs-lookup"><span data-stu-id="f5a56-132">Map each of these integers as an index into the array of thirty-two characters: ABCDEFGHIJKLMNOPQRSTUVWXYZ012345.</span></span> <span data-ttu-id="f5a56-133">Это дает последовательность из 26 символов Юникода, в которой используются только символы в верхнем регистре и цифры.</span><span class="sxs-lookup"><span data-stu-id="f5a56-133">This yields a sequence of 26 Unicode characters that uses only uppercase characters and numerals.</span></span> <span data-ttu-id="f5a56-134">Вопросы с учетом регистра и без учета регистра не применяются, что приводит к уникальности каждого символа в языковом стандарте.</span><span class="sxs-lookup"><span data-stu-id="f5a56-134">Case sensitive and case insensitive considerations do not apply, causing each character to be unique in any locale.</span></span>
5.  <span data-ttu-id="f5a56-135">Создайте окончательную строку, объединив строку " \\ 005" в начале этих 26 символов, для общей длины в 27 символов.</span><span class="sxs-lookup"><span data-stu-id="f5a56-135">Create the final string by concatenating the string "\\005" onto the front of these 26 characters, for a total length of 27 characters.</span></span>

<span data-ttu-id="f5a56-136">В следующем примере кода показано, как сопоставлять из FMTID со строкой свойства.</span><span class="sxs-lookup"><span data-stu-id="f5a56-136">The following example code shows how to map from an FMTID to a property string.</span></span>


```C++
#define CBIT_BYTE        8
#define CBIT_CHARMASK    5
#define CCH_MAP          (1 << CBIT_CHARMASK)    // 32
#define CHARMASK         (CCH_MAP - 1)           // 0x1f
 
CHAR awcMap[CCH_MAP + 1] = "abcdefghijklmnopqrstuvwxyz012345";
 
WCHAR MapChar(ULONG I) {
    return((WCHAR) awcMap[i & CHARMASK]);
    }
 
VOID GuidToPropertyStringName(GUID *pguid, WCHAR awcname[]) {
    BYTE *pb = (BYTE *) pguid;
    BYTE *pbEnd = pb + sizeof(*pguid);
    ULONG cbitRemain = CBIT_BYTE;
    WCHAR *pwc = awcname;
 
    *pwc++ = ((WCHAR) 0x0005);
    while (pb < pbEnd) {
        ULONG i = *pb >> (CBIT_BYTE - cbitRemain);
        if (cbitRemain >= CBIT_CHARMASK) {
            *pwc = MapChar(i);
            if (cbitRemain == CBIT_BYTE && 
                                    *pwc >= L'a' && *pwc <= L'z')
                {
                *pwc += (WCHAR) (L'A' - L'a');
                }
            pwc++;
            cbitRemain -= CBIT_CHARMASK;
            if (cbitRemain == 0) {
                pb++;
                cbitRemain = CBIT_BYTE;
                }
            }
        else {
            if (++pb < pbEnd) {
                i |= *pb << cbitRemain;
                }
            *pwc++ = MapChar(i);
            cbitRemain += CBIT_BYTE - CBIT_CHARMASK;
            }
        }
    *pwc = L'\0';
    }
```



## <a name="converting-a-property-set-from-a-string-name-to-a-fmtid"></a><span data-ttu-id="f5a56-137">Преобразование набора свойств из строкового имени в FMTID</span><span class="sxs-lookup"><span data-stu-id="f5a56-137">Converting a property set from a string name to a FMTID</span></span>

<span data-ttu-id="f5a56-138">Преобразователи имен строк свойств в идентификаторы GUID должны принимать строчные буквы как синонимы с аналогами в верхнем регистре.</span><span class="sxs-lookup"><span data-stu-id="f5a56-138">Converters of property string names to GUIDs should accept lowercase letters as synonymous with their uppercase counterparts.</span></span>

<span data-ttu-id="f5a56-139">В следующем примере кода показано, как сопоставлять строку свойства с FMTID.</span><span class="sxs-lookup"><span data-stu-id="f5a56-139">The following example code shows how to map from a property string to an FMTID.</span></span>


```C++
#include "stdafx.h"
#define _INC_OLE
#include <windows.h>
#include <stdlib.h>
#include <stdio.h>
#include <string.h>
#include <ctype.h>
#define CBIT_CHARMASK 5
#define CBIT_BYTE     8
#define CBIT_GUID    (CBIT_BYTE * sizeof(GUID))
#define CWC_PROPSET  (1 + (CBIT_GUID + CBIT_CHARMASK-1)/CBIT_CHARMASK)
#define WC_PROPSET0  ((WCHAR) 0x0005)
#define CCH_MAP      (1 << CBIT_CHARMASK)        // 32
#define CHARMASK     (CCH_MAP - 1)            // 0x1f
CHAR awcMap[CCH_MAP + 1] = "abcdefghijklmnopqrstuvwxyz012345";
#define CALPHACHARS  ('z' - 'a' + 1)

GUID guidSummary =
{ 0xf29f85e0,0x4ff9, 0x1068,
{ 0xab, 0x91, 0x08, 0x00, 0x2b, 0x27, 0xb3, 0xd9 } };

WCHAR wszSummary[] = L"SummaryInformation";

GUID guidDocumentSummary =
    { 0xd5cdd502,
      0x2e9c, 0x101b,
      { 0x93, 0x97, 0x08, 0x00, 0x2b, 0x2c, 0xf9, 0xae } };

WCHAR wszDocumentSummary[] = L"DocumentSummaryInformation";
__inline WCHAR

MapChar(IN ULONG i)
{
    return((WCHAR) awcMap[i & CHARMASK]);
}

ULONG PropertySetNameToGuid(
    IN ULONG cwcname,
    IN WCHAR const awcname[],
    OUT GUID *pguid)
{
    ULONG Status = ERROR_INVALID_PARAMETER;
    WCHAR const *pwc = awcname;

    if (pwc[0] == WC_PROPSET0)
    {
        //Note: cwcname includes the WC_PROPSET0, and
        //sizeof(wsz...) includes the trailing L'\0', but
        //the comparison excludes both the leading
        //WC_PROPSET0 and the trailing L'\0'.
        if (cwcname == sizeof(wszSummary)/sizeof(WCHAR) &&
            wcsnicmp(&pwc[1], wszSummary, cwcname - 1) == 0)
        {
            *pguid = guidSummary;
            return(NO_ERROR);
        }
        if (cwcname == CWC_PROPSET)
        {
            ULONG cbit;
            BYTE *pb = (BYTE *) pguid - 1;
            ZeroMemory(pguid, sizeof(*pguid));
            for (cbit = 0; cbit < CBIT_GUID; cbit += 
            CBIT_CHARMASK)
            {
                ULONG cbitUsed = cbit % CBIT_BYTE;
                ULONG cbitStored;
                WCHAR wc;
                if (cbitUsed == 0)
                {
                    pb++;
                }
                wc = *++pwc - L'A';        //assume uppercase
                if (wc > CALPHACHARS)
                {
                    wc += (WCHAR) (L'A' - L'a'); //try lowercase
                    if (wc > CALPHACHARS)
                    {
                        wc += L'a' - L'0' + CALPHACHARS; 
                        if (wc > CHARMASK)
                        {
                            goto fail;       //invalid character
                        }
                    }
                }
                *pb |= (BYTE) (wc << cbitUsed);
                cbitStored = min(CBIT_BYTE - cbitUsed, 
                CBIT_CHARMASK);

                //If the translated bits will not fit in the 
                //current byte
                if (cbitStored < CBIT_CHARMASK)
                {
                    wc >>= CBIT_BYTE - cbitUsed;
                    if (cbit + cbitStored == CBIT_GUID)
                    {
                       if (wc != 0)
                       {
                           goto fail;        //extra bits
                       }
                       break;
                    }
                    pb++;
                    *pb |= (BYTE) wc;
                }
           }
           Status = NO_ERROR;
      }
    }
fail:
    return(Status);
}
```



<span data-ttu-id="f5a56-140">При попытке открыть существующий набор свойств в [IPropertySetStorage:: Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)значение (root) FMTID преобразуется в строку, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="f5a56-140">When attempting to open an existing property set, in [IPropertySetStorage::Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open), the (root) FMTID is converted to a string as described above.</span></span> <span data-ttu-id="f5a56-141">Если элемент [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) с таким именем существует, он используется.</span><span class="sxs-lookup"><span data-stu-id="f5a56-141">If an element of the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) of that name exists, it is used.</span></span> <span data-ttu-id="f5a56-142">В противном случае происходит сбой открытия.</span><span class="sxs-lookup"><span data-stu-id="f5a56-142">Otherwise, the open fails.</span></span>

<span data-ttu-id="f5a56-143">При создании набора свойств приведенное выше сопоставление определяет используемое строковое имя.</span><span class="sxs-lookup"><span data-stu-id="f5a56-143">When creating a new property set, the above mapping determines the string name used.</span></span>

 

 





