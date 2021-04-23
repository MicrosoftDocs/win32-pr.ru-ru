---
description: Стандартные библиотеки среды выполнения C содержат версии строковых функций в Юникоде UTF-16 (Расширенная кодировка), которые можно использовать с Юникодом и строковыми функциями, которые можно использовать с символами из однобайтовых кодировок (SBCS). Тип данных типа WCHAR в Юникоде совместим с типом данных WCHAR \_ t в ANSI C и предоставляет доступ к строковым функциям в Юникоде. Версии Юникода для функций начинаются с букв &\# 0034; wcs&\# 0034; (иногда &\# 0034; \_ WCS&\# 0034;). Тип данных CHAR, используемый для кодовых страниц, совместим с символьным типом данных char в ANSI C, чтобы разрешить доступ к функциям символьных строк. Версии символов функций начинаются с букв &\# 0034; str&\# 0034;. Существуют также специальные версии для двухбайтовых наборов символов (DBCS), начинающихся с букв &\# 0034; \_ MBS&\# 0034;.
ms.assetid: a86626c1-7f90-4924-bfdd-384729bd0cc5
title: Стандартные функции C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6247b3707f96908ef16d887462ba06573fd8dd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913523"
---
# <a name="standard-c-functions"></a><span data-ttu-id="def92-108">Стандартные функции C</span><span class="sxs-lookup"><span data-stu-id="def92-108">Standard C Functions</span></span>

<span data-ttu-id="def92-109">Стандартные библиотеки среды выполнения C содержат версии строковых функций в Юникоде UTF-16 (Расширенная кодировка), которые можно использовать с [Юникодом](unicode.md) и строковыми функциями, которые можно использовать с символами из [однобайтовых](single-byte-character-sets.md) кодировок (SBCS).</span><span class="sxs-lookup"><span data-stu-id="def92-109">The standard C runtime libraries contain both Unicode UTF-16 (wide character) versions of string functions that can be used with [Unicode](unicode.md) and byte-oriented versions of string functions that can be used with characters from [single-byte character sets](single-byte-character-sets.md) (SBCSs).</span></span> <span data-ttu-id="def92-110">Тип данных типа WCHAR в Юникоде совместим с типом данных WCHAR \_ t в ANSI C и предоставляет доступ к строковым функциям в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="def92-110">The Unicode data type WCHAR is compatible with the data type wchar\_t in ANSI C, and allows access to the Unicode string functions.</span></span> <span data-ttu-id="def92-111">Версии Юникода для функций начинаются с букв "WCS" (или иногда " \_ WCS").</span><span class="sxs-lookup"><span data-stu-id="def92-111">The Unicode versions of the functions start with the letters "wcs" (or sometimes "\_wcs").</span></span> <span data-ttu-id="def92-112">Тип данных CHAR, используемый для кодовых страниц, совместим с символьным типом данных char в ANSI C, чтобы разрешить доступ к функциям символьных строк.</span><span class="sxs-lookup"><span data-stu-id="def92-112">The data type CHAR used for code pages is compatible with the character data type char in ANSI C, to allow access to the character string functions.</span></span> <span data-ttu-id="def92-113">Версии символов функций начинаются с букв "str".</span><span class="sxs-lookup"><span data-stu-id="def92-113">The character versions of the functions start with the letters "str".</span></span> <span data-ttu-id="def92-114">Существуют также специальные версии для [двухбайтовых наборов символов](double-byte-character-sets.md) (DBCS), начинающихся с букв « \_ MBS».</span><span class="sxs-lookup"><span data-stu-id="def92-114">There are also special versions for [double-byte character sets](double-byte-character-sets.md) (DBCSs) that start with the letters "\_mbs".</span></span>

<span data-ttu-id="def92-115">Стандартные библиотеки среды выполнения C включают универсальные функции для всех стандартных строковых функций C.</span><span class="sxs-lookup"><span data-stu-id="def92-115">The standard C runtime libraries include generic functions for all standard C string functions.</span></span> <span data-ttu-id="def92-116">Они начинаются с " \_ TCS" и перечисляются в файле заголовка TCHAR. h.</span><span class="sxs-lookup"><span data-stu-id="def92-116">They start with "\_tcs" and are listed in the Tchar.h header file.</span></span> <span data-ttu-id="def92-117">Эти функции используют общий тип данных TCHAR.</span><span class="sxs-lookup"><span data-stu-id="def92-117">These functions use the generic TCHAR data type.</span></span>

<span data-ttu-id="def92-118">Приложение должно добавить следующие строки для использования универсальных функций и компиляции для Юникода.</span><span class="sxs-lookup"><span data-stu-id="def92-118">An application must add the following lines to use the generic functions and compile for Unicode.</span></span>


```C++
#define _UNICODE

#include <tchar.h>
#include <wchar.h>
```



<span data-ttu-id="def92-119">Обратите внимание, что оба файла Tchar. h и WCHAR. h являются обязательными, и для \_ переменной в Юникоде также требуется символ подчеркивания в начале.</span><span class="sxs-lookup"><span data-stu-id="def92-119">Note that both the Tchar.h and Wchar.h files are required, and that the leading underscore on the \_UNICODE variable is also required.</span></span> <span data-ttu-id="def92-120">Эта номенклатура относится к стандартной библиотеке C.</span><span class="sxs-lookup"><span data-stu-id="def92-120">This nomenclature is specific to the standard C library.</span></span> <span data-ttu-id="def92-121">"Юникод", отображаемый без подчеркивания, предназначен для сред выполнения Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="def92-121">"UNICODE" rendered without the underscore is for the Microsoft Windows runtimes.</span></span>

<span data-ttu-id="def92-122">Функции [wcstombs](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l) и [функции mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l) могут выполнять преобразование из кодировки, поддерживаемой стандартной библиотекой C, в Юникод и обратно, с некоторыми ограничениями.</span><span class="sxs-lookup"><span data-stu-id="def92-122">The [wcstombs](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l) and [mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l) functions can convert from the character set supported by the standard C library to Unicode and back, with some limitations.</span></span> <span data-ttu-id="def92-123">Дополнительные сведения о переводе строк в Юникод и обратно см. в разделе [Преобразование между строковыми типами](translation-between-string-types.md).</span><span class="sxs-lookup"><span data-stu-id="def92-123">For more information about translating strings to and from Unicode, see [Translation Between String Types](translation-between-string-types.md).</span></span>

<span data-ttu-id="def92-124">Функция [printf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) , определенная в файле Tchar. h, поддерживает те же спецификации формата, что и функции печати стрсафе. h, например [**стрингкбпринтф**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa).</span><span class="sxs-lookup"><span data-stu-id="def92-124">The [printf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) function defined in Tchar.h supports the same format specifications as the Strsafe.h print functions, for example [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa).</span></span> <span data-ttu-id="def92-125">Аналогичным образом TCHAR. h определяет функцию [wprintf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) , в которой строка формата является строкой в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="def92-125">Similarly, Tchar.h defines a [wprintf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) function, in which the format string itself is a Unicode string.</span></span>

> [!Caution]  
> <span data-ttu-id="def92-126">Низкая обработка буфера фрагментацией во многих проблемах безопасности, связанных с переполнением буфера.</span><span class="sxs-lookup"><span data-stu-id="def92-126">Poor buffer handling is implicated in many security issues that involve buffer overruns.</span></span> <span data-ttu-id="def92-127">См. раздел [Справочник по стрсафе. h](../menurc/strsafe-ovw.md).</span><span class="sxs-lookup"><span data-stu-id="def92-127">See [Strsafe.h Reference](../menurc/strsafe-ovw.md).</span></span> <span data-ttu-id="def92-128">Функции, определенные в Стрсафе. h, обеспечивают дополнительную обработку для правильной обработки буфера в коде.</span><span class="sxs-lookup"><span data-stu-id="def92-128">The functions defined in Strsafe.h provide additional processing for proper buffer handling in your code.</span></span> <span data-ttu-id="def92-129">Они предназначены для замены встроенных аналогов C/C++, а также конкретных реализаций Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="def92-129">They are intended to replace their built-in C/C++ counterparts as well as specific Microsoft Windows implementations.</span></span> <span data-ttu-id="def92-130">Дополнительные сведения см. в разделе [вопросы безопасности: международные функции](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="def92-130">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="def92-131">См. также</span><span class="sxs-lookup"><span data-stu-id="def92-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="def92-132">Юникод в Windows API</span><span class="sxs-lookup"><span data-stu-id="def92-132">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
