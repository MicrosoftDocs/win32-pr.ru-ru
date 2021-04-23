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
# <a name="property-set-display-name-dictionary"></a><span data-ttu-id="7c1f2-103">Словарь отображаемого имени набора свойств</span><span class="sxs-lookup"><span data-stu-id="7c1f2-103">Property Set Display Name Dictionary</span></span>

<span data-ttu-id="7c1f2-104">Словарь отображаемых имен свойств позволяет прикреплять значения свойств пользователям к свойствам, кроме тех, которые предоставляются индикатором типа.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-104">A dictionary of property display names enables property set users to attach meaning to properties - beyond those provided by the type indicator.</span></span>

## <a name="dictionary-structure"></a><span data-ttu-id="7c1f2-105">Структура словаря</span><span class="sxs-lookup"><span data-stu-id="7c1f2-105">Dictionary Structure</span></span>

<span data-ttu-id="7c1f2-106">Словарь содержит число записей в списке, за которым следует список записей словаря.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-106">The dictionary contains a count of entries in the list, followed by a list of dictionary entries.</span></span>

``` syntax
typedef struct tagDICTIONARY 
{ 
    DWORD  cEntries ;               // Count of entries in the list 
    ENTRY  rgEntry[ cEntries ] ;    // Property ID/String pair 
} DICTIONARY ;
```

## <a name="dictionary-entry-structure"></a><span data-ttu-id="7c1f2-107">Структура записи словаря</span><span class="sxs-lookup"><span data-stu-id="7c1f2-107">Dictionary Entry Structure</span></span>

<span data-ttu-id="7c1f2-108">Каждая запись словаря в списке представляет собой пару идентификатор/строка.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-108">Each dictionary entry in the list is a Property Identifier/String pair.</span></span> <span data-ttu-id="7c1f2-109">Ниже приведено определение псевдо-структуры для записи словаря.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-109">The following is a pseudo-structure definition for a dictionary entry.</span></span> <span data-ttu-id="7c1f2-110">Это псевдо-структура, так как член SZ \[ \] имеет переменную размер.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-110">It's a pseudo-structure because the sz\[\] member is variable in size.</span></span>

``` syntax
typedef struct tagENTRY 
{ 
    DWORD  propid ;    // Property ID 
    DWORD  cch ;       // Count of characters in the string 
    char  sz[cch];     // Zero-terminated string 
} ENTRY ;
```

## <a name="sample-dictionary"></a><span data-ttu-id="7c1f2-111">Пример словаря</span><span class="sxs-lookup"><span data-stu-id="7c1f2-111">Sample Dictionary</span></span>

<span data-ttu-id="7c1f2-112">Приведенный ниже пример перемещения данных на рынке может включать отображаемое имя "котировка акции" для всего набора и "символ-обозначение" для \_ СИМВОЛА PID.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-112">The following stock market data transfer example might include a displayable name "Stock Quote" for the entire set, and "Ticker Symbol" for PID\_SYMBOL.</span></span> <span data-ttu-id="7c1f2-113">Если набор свойств содержит только символ и словарь, то раздел набора свойств будет иметь байтовый поток, который выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-113">If a property set contained just a symbol and the dictionary, the property set section would have a byte stream that looked like the following.</span></span>

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

<span data-ttu-id="7c1f2-114">Имейте в виду следующие проблемы, касающиеся словарей набора свойств.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-114">Be aware of the following issues regarding property set dictionaries:</span></span>

-   <span data-ttu-id="7c1f2-115">Свойство с ИДЕНТИФИКАТОРом 0 не имеет индикатора типа.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-115">Property ID 0 does not have a type indicator.</span></span> <span data-ttu-id="7c1f2-116">Тип данных **DWORD** , указывающий количество записей, расположенных в позиции индикатора типа.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-116">The **DWORD** data type that indicates the count of entries sits in the type-indicator position.</span></span>
-   <span data-ttu-id="7c1f2-117">Число символов в строке *Кч* содержит нуль символов, который завершает строку.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-117">The count of characters in the *cch* string includes the zero character that terminates the string.</span></span> <span data-ttu-id="7c1f2-118">Если кодовая страница набора свойств не является Юникодом, это поле фактически является числом **байтов** .</span><span class="sxs-lookup"><span data-stu-id="7c1f2-118">When the codepage of the property set is not Unicode, this field is actually a **byte** count.</span></span> <span data-ttu-id="7c1f2-119">Для наборов свойств с версией формата 0 значение этого счетчика не может превышать 256.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-119">For property sets with a format version of 0, this count may not exceed 256.</span></span> <span data-ttu-id="7c1f2-120">Для наборов свойств с версией формата 1 это количество может быть большим, чем разрешено общим размером набора свойств.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-120">For property sets with a format version of 1, this count may be as large as is allowed by the total property set size.</span></span>
-   <span data-ttu-id="7c1f2-121">Словарь является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-121">The dictionary is optional.</span></span> <span data-ttu-id="7c1f2-122">Не все имена свойств в наборе должны отображаться в словаре.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-122">Not all the names of properties in the set are required to appear in the dictionary.</span></span> <span data-ttu-id="7c1f2-123">И наоборот, не все имена в словаре должны соответствовать свойствам в наборе.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-123">Conversely, not all names in the dictionary are required to correspond to properties in the set.</span></span> <span data-ttu-id="7c1f2-124">В словаре должны опускаться записи для свойств, которые предположительно распознаются приложениями, которые управляют набором свойств.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-124">The dictionary should omit entries for properties assumed to be universally recognized by applications manipulating the property set.</span></span> <span data-ttu-id="7c1f2-125">Как правило, имена базовых наборов свойств для широко принятых стандартов опущены, но наборы свойств специального назначения могут включать словари для использования браузерами.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-125">Typically, names for the base property sets for widely-accepted standards are omitted, but special-purpose property sets may include dictionaries for use by browsers.</span></span>
-   <span data-ttu-id="7c1f2-126">Имена свойств в словаре хранятся в кодовой странице, указанной [свойством с идентификатором 1](/windows/desktop/Stg/reserved-property-identifiers).</span><span class="sxs-lookup"><span data-stu-id="7c1f2-126">Property names in the dictionary are stored in the code page indicated by [Property ID 1](/windows/desktop/Stg/reserved-property-identifiers).</span></span> <span data-ttu-id="7c1f2-127">Для кодовых страниц ANSI каждая запись словаря выдается по байтам.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-127">For ANSI code pages, each dictionary entry is byte-aligned.</span></span> <span data-ttu-id="7c1f2-128">Таким же интервал между именами свойств и ИДЕНТИФИКАТОРом 0 нет.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-128">Thus, there is no spacing between property names with Property ID 0.</span></span> <span data-ttu-id="7c1f2-129">Это единственный случай, когда значения типов **DWORD** (идентификатор свойства и имя свойства-длина **DWORD**) не должны быть согласованы в 32-разрядных границах.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-129">This is the only case where values of **DWORD** data types (the property ID and property name-length **DWORD** s) are not required to be aligned on 32-bit boundaries.</span></span> <span data-ttu-id="7c1f2-130">Для страниц в Юникоде каждая запись словаря имеет 32-разрядное соответствие.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-130">For Unicode pages, each dictionary entry is 32-bit aligned.</span></span>
-   <span data-ttu-id="7c1f2-131">Имена свойств, которые начинаются с двоичных символов Юникода, 0x0001 через 0x001F, зарезервированы для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-131">Property names that begin with the binary Unicode characters 0x0001 through 0x001F are reserved for future use.</span></span>
-   <span data-ttu-id="7c1f2-132">Имя свойства, связанное с ИДЕНТИФИКАТОРом свойства 0, представляет имя всего набора свойств.</span><span class="sxs-lookup"><span data-stu-id="7c1f2-132">The property name associated with Property ID 0 represents the name of the entire property set.</span></span>

 

 