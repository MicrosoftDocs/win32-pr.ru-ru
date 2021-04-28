---
title: Работа со строками
description: Работа со строками
ms.assetid: 876ff8bb-67c3-4dcc-aa94-7fbd915c67dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4661c6b07a267d90e0fca05d04354c018be04527
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110972"
---
# <a name="working-with-strings"></a><span data-ttu-id="f3416-103">Работа со строками</span><span class="sxs-lookup"><span data-stu-id="f3416-103">Working with Strings</span></span>

<span data-ttu-id="f3416-104">Windows изначально поддерживает строки в Юникоде для элементов пользовательского интерфейса, имен файлов и т. д.</span><span class="sxs-lookup"><span data-stu-id="f3416-104">Windows natively supports Unicode strings for UI elements, file names, and so forth.</span></span> <span data-ttu-id="f3416-105">Юникод — предпочтительная кодировка символов, так как она поддерживает все наборы символов и языки.</span><span class="sxs-lookup"><span data-stu-id="f3416-105">Unicode is the preferred character encoding, because it supports all character sets and languages.</span></span> <span data-ttu-id="f3416-106">Windows представляет символы Юникода, используя кодировку UTF-16, в которой каждый символ кодируется как 16-разрядное значение.</span><span class="sxs-lookup"><span data-stu-id="f3416-106">Windows represents Unicode characters using UTF-16 encoding, in which each character is encoded as a 16-bit value.</span></span> <span data-ttu-id="f3416-107">Символы UTF-16 называются *расширенными* символами, чтобы отличать их от 8-разрядных символов ANSI.</span><span class="sxs-lookup"><span data-stu-id="f3416-107">UTF-16 characters are called *wide* characters, to distinguish them from 8-bit ANSI characters.</span></span> <span data-ttu-id="f3416-108">Компилятор Visual C++ поддерживает встроенный тип данных **WCHAR \_ t** для расширенных символов.</span><span class="sxs-lookup"><span data-stu-id="f3416-108">The Visual C++ compiler supports the built-in data type **wchar\_t** for wide characters.</span></span> <span data-ttu-id="f3416-109">Файл заголовка WinNT. h также определяет следующий **typedef**.</span><span class="sxs-lookup"><span data-stu-id="f3416-109">The header file WinNT.h also defines the following **typedef**.</span></span>


```C++
typedef wchar_t WCHAR;
```



<span data-ttu-id="f3416-110">Обе версии будут отображаться в примере кода MSDN.</span><span class="sxs-lookup"><span data-stu-id="f3416-110">You will see both versions in MSDN example code.</span></span> <span data-ttu-id="f3416-111">Чтобы объявить литерал расширенных символов или строковый литерал расширенных символов, добавьте **L** перед литералом.</span><span class="sxs-lookup"><span data-stu-id="f3416-111">To declare a wide-character literal or a wide-character string literal, put **L** before the literal.</span></span>


```C++
wchar_t a = L'a';
wchar_t *str = L"hello";
```



<span data-ttu-id="f3416-112">Вот некоторые другие определения типов, связанные со строками, которые вы увидите:</span><span class="sxs-lookup"><span data-stu-id="f3416-112">Here are some other string-related typedefs that you will see:</span></span>



| <span data-ttu-id="f3416-113">Typedef</span><span class="sxs-lookup"><span data-stu-id="f3416-113">Typedef</span></span>                   | <span data-ttu-id="f3416-114">Определение</span><span class="sxs-lookup"><span data-stu-id="f3416-114">Definition</span></span>       |
|---------------------------|------------------|
| <span data-ttu-id="f3416-115">**CHAR**</span><span class="sxs-lookup"><span data-stu-id="f3416-115">**CHAR**</span></span>                  | `char`           |
| <span data-ttu-id="f3416-116">**ПСТР** или **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="f3416-116">**PSTR** or **LPSTR**</span></span>     | `char*`          |
| <span data-ttu-id="f3416-117">**Пкстр** или **LPCSTR**</span><span class="sxs-lookup"><span data-stu-id="f3416-117">**PCSTR** or **LPCSTR**</span></span>   | `const char*`    |
| <span data-ttu-id="f3416-118">**Пвстр** или **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="f3416-118">**PWSTR** or **LPWSTR**</span></span>   | `wchar_t*`       |
| <span data-ttu-id="f3416-119">**Пквстр** или **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="f3416-119">**PCWSTR** or **LPCWSTR**</span></span> | `const wchar_t*` |



 

## <a name="unicode-and-ansi-functions"></a><span data-ttu-id="f3416-120">Функции Юникода и ANSI</span><span class="sxs-lookup"><span data-stu-id="f3416-120">Unicode and ANSI Functions</span></span>

<span data-ttu-id="f3416-121">Когда корпорация Майкрософт ввела в Windows поддержку Юникода, она облегчило переход, предоставляя два параллельных набора API — один для строк ANSI, а другой для строк Юникода.</span><span class="sxs-lookup"><span data-stu-id="f3416-121">When Microsoft introduced Unicode support to Windows, it eased the transition by providing two parallel sets of APIs, one for ANSI strings and the other for Unicode strings.</span></span> <span data-ttu-id="f3416-122">Например, существует две функции для задания текста в строке заголовка окна:</span><span class="sxs-lookup"><span data-stu-id="f3416-122">For example, there are two functions to set the text of a window's title bar:</span></span>

-   <span data-ttu-id="f3416-123">**Сетвиндовтекста** принимает строку ANSI.</span><span class="sxs-lookup"><span data-stu-id="f3416-123">**SetWindowTextA** takes an ANSI string.</span></span>
-   <span data-ttu-id="f3416-124">**Сетвиндовтекств** принимает строку в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="f3416-124">**SetWindowTextW** takes a Unicode string.</span></span>

<span data-ttu-id="f3416-125">На внутреннем уровне версия ANSI преобразует строку в Юникод.</span><span class="sxs-lookup"><span data-stu-id="f3416-125">Internally, the ANSI version translates the string to Unicode.</span></span> <span data-ttu-id="f3416-126">Заголовки Windows также определяют макрос, который разрешается в версию Юникода, если определен символ препроцессора `UNICODE` или если в противном случае используется версия ANSI.</span><span class="sxs-lookup"><span data-stu-id="f3416-126">The Windows headers also define a macro that resolves to the Unicode version when the preprocessor symbol `UNICODE` is defined or the ANSI version otherwise.</span></span>


```C++
#ifdef UNICODE
#define SetWindowText  SetWindowTextW
#else
#define SetWindowText  SetWindowTextA
#endif 
```



<span data-ttu-id="f3416-127">В библиотеке MSDN функция задокументирована под именем [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), хотя в действительности это имя макроса, а не имя самой функции.</span><span class="sxs-lookup"><span data-stu-id="f3416-127">In MSDN, the function is documented under the name [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), even though that is really the macro name, not the actual function name.</span></span>

<span data-ttu-id="f3416-128">Новые приложения всегда должны вызывать версии Юникода.</span><span class="sxs-lookup"><span data-stu-id="f3416-128">New applications should always call the Unicode versions.</span></span> <span data-ttu-id="f3416-129">Для многих языков мира требуется Юникод.</span><span class="sxs-lookup"><span data-stu-id="f3416-129">Many world languages require Unicode.</span></span> <span data-ttu-id="f3416-130">Если вы используете строки ANSI, локализация приложения будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="f3416-130">If you use ANSI strings, it will be impossible to localize your application.</span></span> <span data-ttu-id="f3416-131">Версии ANSI также менее эффективны, так как операционная система должна преобразовать строки ANSI в Юникод во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="f3416-131">The ANSI versions are also less efficient, because the operating system must convert the ANSI strings to Unicode at run time.</span></span> <span data-ttu-id="f3416-132">В зависимости от предпочтений можно вызывать функции Юникода явным образом, например **сетвиндовтекств**, или использовать макросы.</span><span class="sxs-lookup"><span data-stu-id="f3416-132">Depending on your preference, you can call the Unicode functions explicitly, such as **SetWindowTextW**, or use the macros.</span></span> <span data-ttu-id="f3416-133">Пример кода в MSDN обычно вызывает макросы, но эти две формы точно эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="f3416-133">The example code on MSDN typically calls the macros, but the two forms are exactly equivalent.</span></span> <span data-ttu-id="f3416-134">Большинство новых интерфейсов API в Windows имеют только версию Юникода, без соответствующей версии ANSI.</span><span class="sxs-lookup"><span data-stu-id="f3416-134">Most newer APIs in Windows have just a Unicode version, with no corresponding ANSI version.</span></span>

## <a name="tchars"></a><span data-ttu-id="f3416-135">тчарс</span><span class="sxs-lookup"><span data-stu-id="f3416-135">TCHARs</span></span>

<span data-ttu-id="f3416-136">Когда приложения, необходимые для поддержки Windows NT, а также Windows 95, Windows 98 и Windows Me, имели смысл компилировать один и тот же код для строк ANSI или Юникод в зависимости от целевой платформы.</span><span class="sxs-lookup"><span data-stu-id="f3416-136">Back when applications needed to support both Windows NT as well as Windows 95, Windows 98, and Windows Me, it was useful to compile the same code for either ANSI or Unicode strings, depending on the target platform.</span></span> <span data-ttu-id="f3416-137">Для этого Windows SDK предоставляет макросы, которые сопоставляют строки с Юникодом или ANSI в зависимости от платформы.</span><span class="sxs-lookup"><span data-stu-id="f3416-137">To this end, the Windows SDK provides macros that map strings to Unicode or ANSI, depending on the platform.</span></span>



| <span data-ttu-id="f3416-138">Макрос</span><span class="sxs-lookup"><span data-stu-id="f3416-138">Macro</span></span>     | <span data-ttu-id="f3416-139">Юникод</span><span class="sxs-lookup"><span data-stu-id="f3416-139">Unicode</span></span>   | <span data-ttu-id="f3416-140">ANSI</span><span class="sxs-lookup"><span data-stu-id="f3416-140">ANSI</span></span>   |
|-----------|-----------|--------|
| <span data-ttu-id="f3416-141">TCHAR</span><span class="sxs-lookup"><span data-stu-id="f3416-141">TCHAR</span></span>     | `wchar_t` | `char` |
| <span data-ttu-id="f3416-142">ТЕКСТ ("x")</span><span class="sxs-lookup"><span data-stu-id="f3416-142">TEXT("x")</span></span> | `L"x"`    | `"x"`  |



 

<span data-ttu-id="f3416-143">Например, приведенный ниже код</span><span class="sxs-lookup"><span data-stu-id="f3416-143">For example, the following code:</span></span>


```C++
SetWindowText(TEXT("My Application"));
```



<span data-ttu-id="f3416-144">разрешается в одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="f3416-144">resolves to one of the following:</span></span>


```C++
SetWindowTextW(L"My Application"); // Unicode function with wide-character string.

SetWindowTextA("My Application");  // ANSI function.
```



<span data-ttu-id="f3416-145">Макросы **Text** и **TCHAR** менее полезны в настоящее время, так как все приложения должны использовать Юникод.</span><span class="sxs-lookup"><span data-stu-id="f3416-145">The **TEXT** and **TCHAR** macros are less useful today, because all applications should use Unicode.</span></span> <span data-ttu-id="f3416-146">Однако они могут отображаться в старом коде и в некоторых примерах кода MSDN.</span><span class="sxs-lookup"><span data-stu-id="f3416-146">However, you might see them in older code and in some of the MSDN code examples.</span></span>

<span data-ttu-id="f3416-147">Заголовки библиотек времени выполнения Microsoft C определяют аналогичный набор макросов.</span><span class="sxs-lookup"><span data-stu-id="f3416-147">The headers for the Microsoft C run-time libraries define a similar set of macros.</span></span> <span data-ttu-id="f3416-148">Например, **\_ ткслен** разрешается в **strlen** , если `_UNICODE` не определен. в противном случае он разрешается в **wcslen**, который является версией **strlen** для расширенных символов.</span><span class="sxs-lookup"><span data-stu-id="f3416-148">For example, **\_tcslen** resolves to **strlen** if `_UNICODE` is undefined; otherwise it resolves to **wcslen**, which is the wide-character version of **strlen**.</span></span>


```C++
#ifdef _UNICODE
#define _tcslen     wcslen
#else
#define _tcslen     strlen
#endif 
```



<span data-ttu-id="f3416-149">Будьте внимательны: в некоторых заголовках используется символ препроцессора `UNICODE` , а другие используют `_UNICODE` префикс подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="f3416-149">Be careful: Some headers use the preprocessor symbol `UNICODE`, others use `_UNICODE` with an underscore prefix.</span></span> <span data-ttu-id="f3416-150">Всегда определяйте оба символа.</span><span class="sxs-lookup"><span data-stu-id="f3416-150">Always define both symbols.</span></span> <span data-ttu-id="f3416-151">Visual C++ задает их обоими по умолчанию при создании нового проекта.</span><span class="sxs-lookup"><span data-stu-id="f3416-151">Visual C++ sets them both by default when you create a new project.</span></span>

## <a name="next"></a><span data-ttu-id="f3416-152">Следующая</span><span class="sxs-lookup"><span data-stu-id="f3416-152">Next</span></span>

[<span data-ttu-id="f3416-153">Что такое окно?</span><span class="sxs-lookup"><span data-stu-id="f3416-153">What Is a Window?</span></span>](what-is-a-window-.md)

 

 
