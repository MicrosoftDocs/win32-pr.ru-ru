---
title: Словарь отображаемого имени набора свойств
description: Словарь отображаемых имен свойств позволяет прикреплять значения свойств пользователям к свойствам, кроме тех, которые предоставляются индикатором типа.
ms.assetid: b6813a86-39d3-4754-86e4-51035a7c91d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd844b4d37d4f10434fc5b73f936b4b6565c1506
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792954"
---
# <a name="property-set-display-name-dictionary"></a>Словарь отображаемого имени набора свойств

Словарь отображаемых имен свойств позволяет прикреплять значения свойств пользователям к свойствам, кроме тех, которые предоставляются индикатором типа.

## <a name="dictionary-structure"></a>Структура словаря

Словарь содержит число записей в списке, за которым следует список записей словаря.

``` syntax
typedef struct tagDICTIONARY 
{ 
    DWORD  cEntries ;               // Count of entries in the list 
    ENTRY  rgEntry[ cEntries ] ;    // Property ID/String pair 
} DICTIONARY ;
```

## <a name="dictionary-entry-structure"></a>Структура записи словаря

Каждая запись словаря в списке представляет собой пару идентификатор/строка. Ниже приведено определение псевдо-структуры для записи словаря. Это псевдо-структура, так как член SZ \[ \] имеет переменную размер.

``` syntax
typedef struct tagENTRY 
{ 
    DWORD  propid ;    // Property ID 
    DWORD  cch ;       // Count of characters in the string 
    char  sz[cch];     // Zero-terminated string 
} ENTRY ;
```

## <a name="sample-dictionary"></a>Пример словаря

Приведенный ниже пример перемещения данных на рынке может включать отображаемое имя "котировка акции" для всего набора и "символ-обозначение" для \_ СИМВОЛА PID. Если набор свойств содержит только символ и словарь, то раздел набора свойств будет иметь байтовый поток, который выглядит следующим образом.

``` syntax
Offset     Bytes 
; Start of section 
0000    5C 01 00 00    ; DWORD size of section 
0004    04 00 00 00    ; DWORD number of properties in section 
 
; Start of PropID/Offset pairs 
0008    01 00 00 00    ; DWORD Property ID (1 == code page) 
000C    28 00 00 00    ; DWORD offset to property ID 
0010    00 00 00 80    ; DWORD Property ID (0x80000000 == locale
                                                 ID) 
0014    30 00 00 00    ; DWORD offset to property ID 
0018    00 00 00 00    ; DWORD Property ID (0 == dictionary) 
001C    38 00 00 00    ; DWORD offset to property ID 
0020    07 00 00 00    ; DWORD Property ID (7 == PID_SYMBOL)
0024    5C 01 00 00    ; DWORD offset to property ID
 
; Start of Property 1 (code page)
0028    01 00 00 00    ; DWORD type indicator (VT_12)
002C    B0 04          ; USHORT codepage (0x04b0 == 1200 ==
                                                 unicode)
002E    00 00          ; Pad to 32-bit boundary
 
; Start of Property 0x80000000 (Local ID)
0030    13 00 00 00    ; DWORD type indicator (VT_U14)
0034    09 04 00 00    ; ULONG locale ID (0x0409 == American 
                                                 English)
 
; Start of Property 0 (the dictionary)
0038    08 00 00 00    ; DWORD number of entries in dictionary
                             (Note:  No type indicator)
003C    00 00 00 00    ; DWORD propid == 0 (the dictionary)
0040    0C 00 00 00    ; DWORD cch == wcslen(L"Stock Quote") +
                                                 sizeof(L'\0') == 12
0044    L"Stock Quote" ; wchar_t wsz(12)
005C    05 00 00 00    ; DWORD propid == 5 (PID_HIGH)
0060    0B 00 00 00    ; DWORD cch == wcslen(L"High Price") + 
                                                 sizeof(L'\0') == 11
0064    L"High Price\0"; wchar_t wsz(11)
007A    00 00          ; padding for 32-bit alignment (necessary
                             because the codepage is unicode)
007C    07 00 00 00    ; DWORD propid == 7 (PID_SYMBOL)
0080    0E 00 00 00    ; DWORD cch - wcslen(L"Ticker Symbol\0") 
                             == 14
0084    L"Ticker Symbol\0" ; wchar_t wsz(14)
 
    // The dictionary would continue, but may not contain entries 
    // for every possible property, and may contain entries for 
    // properties that are not present. Entries are not required  
    // to be in order.
```

Имейте в виду следующие проблемы, касающиеся словарей набора свойств.

-   Свойство с ИДЕНТИФИКАТОРом 0 не имеет индикатора типа. Тип данных **DWORD** , указывающий количество записей, расположенных в позиции индикатора типа.
-   Число символов в строке *Кч* содержит нуль символов, который завершает строку. Если кодовая страница набора свойств не является Юникодом, это поле фактически является числом **байтов** . Для наборов свойств с версией формата 0 значение этого счетчика не может превышать 256. Для наборов свойств с версией формата 1 это количество может быть большим, чем разрешено общим размером набора свойств.
-   Словарь является необязательным. Не все имена свойств в наборе должны отображаться в словаре. И наоборот, не все имена в словаре должны соответствовать свойствам в наборе. В словаре должны опускаться записи для свойств, которые предположительно распознаются приложениями, которые управляют набором свойств. Как правило, имена базовых наборов свойств для широко принятых стандартов опущены, но наборы свойств специального назначения могут включать словари для использования браузерами.
-   Имена свойств в словаре хранятся в кодовой странице, указанной [свойством с идентификатором 1](/windows/desktop/Stg/reserved-property-identifiers). Для кодовых страниц ANSI каждая запись словаря выдается по байтам. Таким же интервал между именами свойств и ИДЕНТИФИКАТОРом 0 нет. Это единственный случай, когда значения типов **DWORD** (идентификатор свойства и имя свойства-длина **DWORD**) не должны быть согласованы в 32-разрядных границах. Для страниц в Юникоде каждая запись словаря имеет 32-разрядное соответствие.
-   Имена свойств, которые начинаются с двоичных символов Юникода, 0x0001 через 0x001F, зарезервированы для будущего использования.
-   Имя свойства, связанное с ИДЕНТИФИКАТОРом свойства 0, представляет имя всего набора свойств.

 

 