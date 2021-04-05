---
description: Windows SDK предоставляет прототипы функций в универсальных, кодовых страницах Windows и версиях Юникода.
ms.assetid: 601d24b0-11bb-48fa-a257-207c3acee226
title: Правила обозначения прототипов функций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951860f72870dcbbcb88572f379e39dc843ecb11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910123"
---
# <a name="conventions-for-function-prototypes"></a><span data-ttu-id="b5670-103">Правила обозначения прототипов функций</span><span class="sxs-lookup"><span data-stu-id="b5670-103">Conventions for Function Prototypes</span></span>

<span data-ttu-id="b5670-104">Windows SDK предоставляет прототипы функций в универсальных, [кодовых страницах Windows](code-pages.md)и версиях [Юникода](unicode.md) .</span><span class="sxs-lookup"><span data-stu-id="b5670-104">The Windows SDK provides function prototypes in generic, [Windows code page](code-pages.md), and [Unicode](unicode.md) versions.</span></span> <span data-ttu-id="b5670-105">Прототипы могут быть скомпилированы для создания прототипов кодовых страниц Windows или прототипов Юникода.</span><span class="sxs-lookup"><span data-stu-id="b5670-105">The prototypes can be compiled to produce either Windows code page prototypes or Unicode prototypes.</span></span> <span data-ttu-id="b5670-106">Все три прототипа обсуждаются в этом разделе и иллюстрируются примерами кода для функции [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="b5670-106">All three prototypes are discussed in this topic and are illustrated by code samples for the [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) function.</span></span>

<span data-ttu-id="b5670-107">Ниже приведен пример универсального прототипа.</span><span class="sxs-lookup"><span data-stu-id="b5670-107">The following is an example of a generic prototype.</span></span>


```C++
BOOL SetWindowText(
  HWND hwnd,
  LPCTSTR lpText
);
```



<span data-ttu-id="b5670-108">Файл заголовка предоставляет универсальное имя функции, реализованное как макрос.</span><span class="sxs-lookup"><span data-stu-id="b5670-108">The header file provides the generic function name implemented as a macro.</span></span>


```C++
#ifdef UNICODE
#define SetWindowText SetWindowTextW
#else
#define SetWindowText SetWindowTextA
#endif // !UNICODE
```



<span data-ttu-id="b5670-109">Препроцессор расширяет макрос на кодовую страницу Windows или имя функции Юникода.</span><span class="sxs-lookup"><span data-stu-id="b5670-109">The preprocessor expands the macro into either the Windows code page or Unicode function name.</span></span> <span data-ttu-id="b5670-110">Буква "A" (ANSI) или "W" (Юникод) добавляется в конце имени универсальной функции, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="b5670-110">The letter "A" (ANSI) or "W" (Unicode) is added at the end of the generic function name, as appropriate.</span></span> <span data-ttu-id="b5670-111">Затем файл заголовка предоставляет два отдельных прототипа: один для кодовых страниц Windows и один для Юникода, как показано в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="b5670-111">The header file then provides two specific prototypes, one for Windows code pages and one for Unicode, as shown in the following examples.</span></span>


```C++
BOOL SetWindowTextA(
  HWND hwnd,
  LPCSTR lpText
);
```




```C++
BOOL SetWindowTextW(
  HWND hwnd,
  LPCWSTR lpText
);
```



<span data-ttu-id="b5670-112">Как описано в разделах [типы данных Windows для строк](windows-data-types-for-strings.md), прототип универсальной функции использует тип данных LPCTSTR для параметра Text.</span><span class="sxs-lookup"><span data-stu-id="b5670-112">As explained in [Windows Data Types for Strings](windows-data-types-for-strings.md), the generic function prototype uses the data type LPCTSTR for the text parameter.</span></span> <span data-ttu-id="b5670-113">Однако прототип кодовой страницы Windows использует тип LPCSTR, а прототип Юникода — LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="b5670-113">However, the Windows code page prototype uses the type LPCSTR, and the Unicode prototype uses LPCWSTR.</span></span>

<span data-ttu-id="b5670-114">Для всех функций с текстовыми аргументами приложения должны, как правило, использоваться универсальные прототипы функций.</span><span class="sxs-lookup"><span data-stu-id="b5670-114">For all functions with text arguments, applications should normally use the generic function prototypes.</span></span> <span data-ttu-id="b5670-115">Если приложение определяет "UNICODE" перед инструкциями **\# include** для файлов заголовков или во время компиляции, инструкции будут скомпилированы в функции Юникода.</span><span class="sxs-lookup"><span data-stu-id="b5670-115">If an application defines "UNICODE" either before the **\#include** statements for the header files or during compilation, the statements will be compiled into Unicode functions.</span></span>

> [!Note]  
> <span data-ttu-id="b5670-116">Новые приложения Windows должны использовать Юникод, чтобы избежать несоответствий между различными кодовыми страницами и простотой локализации.</span><span class="sxs-lookup"><span data-stu-id="b5670-116">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and for ease of localization.</span></span> <span data-ttu-id="b5670-117">Они должны быть написаны с помощью универсальных функций и должны определять Юникод, чтобы компилировать функции в функции Юникода.</span><span class="sxs-lookup"><span data-stu-id="b5670-117">They should be written with generic functions, and should define UNICODE to compile the functions into Unicode functions.</span></span> <span data-ttu-id="b5670-118">В некоторых местах, где приложение должно работать с 8-разрядными символьными данными, оно может явно использовать функции для кодовых страниц Windows.</span><span class="sxs-lookup"><span data-stu-id="b5670-118">In the few places where an application must work with 8-bit character data, it can make explicit use of the functions for Windows code pages.</span></span>

 

<span data-ttu-id="b5670-119">Приложение должно всегда использовать универсальный прототип функции с универсальными строковыми и символьными типами.</span><span class="sxs-lookup"><span data-stu-id="b5670-119">Your application should always use a generic function prototype with the generic string and character types.</span></span> <span data-ttu-id="b5670-120">Все имена функций, оканчивающиеся на заглавную «W», принимают параметры в Юникоде (расширенные символы).</span><span class="sxs-lookup"><span data-stu-id="b5670-120">All function names that end with an uppercase "W" take Unicode, that is, wide character, parameters.</span></span> <span data-ttu-id="b5670-121">Некоторые функции существуют только в версиях Юникода и могут использоваться только с соответствующими типами данных.</span><span class="sxs-lookup"><span data-stu-id="b5670-121">Some functions exist only in Unicode versions and can be used only with the appropriate data types.</span></span> <span data-ttu-id="b5670-122">Например, [**лЦидтолокаленаме**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) и [**локаленаметолЦид**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) имеют только версии Юникода.</span><span class="sxs-lookup"><span data-stu-id="b5670-122">For example, [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) and [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) have only Unicode versions.</span></span>

<span data-ttu-id="b5670-123">В разделе "требования" в справочной документации по каждой функции Юникода и кодировки содержится информация о версиях функций, реализованных поддерживаемыми операционными системами.</span><span class="sxs-lookup"><span data-stu-id="b5670-123">The Requirements section in the reference documentation for each Unicode and character set function provides information on the function versions implemented by supported operating systems.</span></span> <span data-ttu-id="b5670-124">Если включена строка, начинающаяся с "Unicode", функция имеет отдельные версии кодовых страниц в Юникоде и Windows.</span><span class="sxs-lookup"><span data-stu-id="b5670-124">If a line beginning with "Unicode" is included, the function has separate Unicode and Windows code page versions.</span></span>

> [!Note]  
> <span data-ttu-id="b5670-125">Если функция имеет параметр длины для символьной строки, ее длина должна задокументирована как количество значений TCHAR в строке.</span><span class="sxs-lookup"><span data-stu-id="b5670-125">When a function has a length parameter for a character string, the length should be documented as a count of TCHAR values in the string.</span></span> <span data-ttu-id="b5670-126">Этот тип данных относится к байтам для версий кодовой страницы Windows функции или 16-разрядных слов для версий Юникода.</span><span class="sxs-lookup"><span data-stu-id="b5670-126">This data type refers to bytes for Windows code page versions of the function or 16-bit words for Unicode versions.</span></span> <span data-ttu-id="b5670-127">Однако функции, требующие или возвращающие указатели на нетипизированные блоки памяти, такие как функция [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) , обычно имеют размер в байтах, независимо от используемого прототипа.</span><span class="sxs-lookup"><span data-stu-id="b5670-127">However, functions that require or return pointers to untyped memory blocks, such as the [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) function, generally take a size in bytes, regardless of the prototype that is used.</span></span> <span data-ttu-id="b5670-128">Если выделение нетипизированной памяти предназначено для строки, приложение должно умножить число символов на sizeof (TCHAR).</span><span class="sxs-lookup"><span data-stu-id="b5670-128">If the allocation of untyped memory is for a string, the application must multiply the number of characters by sizeof(TCHAR).</span></span> <span data-ttu-id="b5670-129">Дополнительные сведения см. [в разделе Использование универсальных типов данных](using-generic-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="b5670-129">For additional information, see [Using Generic Data Types](using-generic-data-types.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b5670-130">См. также</span><span class="sxs-lookup"><span data-stu-id="b5670-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5670-131">Юникод в Windows API</span><span class="sxs-lookup"><span data-stu-id="b5670-131">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
