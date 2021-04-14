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
# <a name="names-in-istorage"></a>Имена в IStorage

Набор свойств определяется с помощью идентификатора формата (FMTID) в интерфейсе [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) . В интерфейсе [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) набор свойств имеет имя с завершающей нулем строкой Юникода с максимальной длиной 32 символов. Чтобы обеспечить взаимодействие, необходимо установить сопоставление между FMTID и соответствующей строкой Юникода, заканчивающейся нулем.

## <a name="converting-a-property-set-from-a-fmtid-to-a-string-name"></a>Преобразование набора свойств из FMTID в строковое имя

При преобразовании из FMTID в соответствующее строковое имя в Юникоде сначала убедитесь, что FMTID является хорошо известным значением, указанным в следующей таблице. Если это так, используйте соответствующее хорошо известное имя строки.

| FMTID                                                                                | Имя строки                       | Семантическ                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------------------|
| F29F85E0-4FF9-1068-AB91-08002B27B3D9                                                 | " \\ 005SummaryInformation"         | Сводная информация о COM2                                         |
| D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE<br/> | " \\ 005DocumentSummaryInformation" | Сведения о документе Office и определяемые пользователем свойства. |



 

> [!Note]  
> Набор свойств **документсуммаринформатион** и **пользователяопределенные** уникален в том, что он содержит два раздела. В любом другом наборе свойств не разрешается использовать несколько разделов. Дополнительные сведения см. в разделе [структурированное хранилище упорядоченный формат набора свойств](structured-storage-serialized-property-set-format.md), а [также в наборе свойств документсуммаринформатион и пользователяопределенные](the-documentsummaryinformation-and-userdefined-property-sets.md). Первый раздел был определен как часть COM; второй был определен с помощью Microsoft Office.

 

Если FMTID не является хорошо известным значением, используйте следующую процедуру, чтобы алгоритмически сформировать строковое имя.

**Преобразование строкового имени в алгоритмически**

1.  При необходимости преобразуйте FMTID в порядковый номер с прямым порядком байтов.
2.  Возьмите 128 бит FMTID и рассматривайте их как одну длинную битовую строку путем сцепления каждого байта вместе. Первый бит 128-разрядного значения — это наименее значащий бит первого байта в памяти FMTID; последний бит 128-битного значения — это наиболее значимый бит последнего байта в памяти FMTID. Расширьте эти 128 бит на 130 бит, добавив два нулевых бита в конец.
3.  Разделите 130 бит на группы из пяти бит; будет составлять 26 таких групп. Рассмотрите каждую группу как целое число с обратным приоритетом. Например, первый из 128 бит является наименее значащим битом первой группы из пяти бит; Пятый из 128 бит является наиболее значащим битом первой группы.
4.  Сопоставьте каждое из этих целых чисел в виде индекса в массиве 32 символов: ABCDEFGHIJKLMNOPQRSTUVWXYZ012345. Это дает последовательность из 26 символов Юникода, в которой используются только символы в верхнем регистре и цифры. Вопросы с учетом регистра и без учета регистра не применяются, что приводит к уникальности каждого символа в языковом стандарте.
5.  Создайте окончательную строку, объединив строку " \\ 005" в начале этих 26 символов, для общей длины в 27 символов.

В следующем примере кода показано, как сопоставлять из FMTID со строкой свойства.


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



## <a name="converting-a-property-set-from-a-string-name-to-a-fmtid"></a>Преобразование набора свойств из строкового имени в FMTID

Преобразователи имен строк свойств в идентификаторы GUID должны принимать строчные буквы как синонимы с аналогами в верхнем регистре.

В следующем примере кода показано, как сопоставлять строку свойства с FMTID.


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



При попытке открыть существующий набор свойств в [IPropertySetStorage:: Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)значение (root) FMTID преобразуется в строку, как описано выше. Если элемент [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) с таким именем существует, он используется. В противном случае происходит сбой открытия.

При создании набора свойств приведенное выше сопоставление определяет используемое строковое имя.

 

 





