---
description: Если в коде используются универсальные типы данных, их можно скомпилировать для Юникода просто с помощью директивы препроцессора для определения &\# 0034; Юникод&\# 0034; перед \# инструкциями include для файлов заголовков.
ms.assetid: 1c9cbb18-9295-4847-86c1-d596668cbe57
title: Использование универсальных типов данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2604f87b12e86076bed47f509c6398fa8482b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684605"
---
# <a name="using-generic-data-types"></a><span data-ttu-id="561bf-103">Использование универсальных типов данных</span><span class="sxs-lookup"><span data-stu-id="561bf-103">Using Generic Data Types</span></span>

<span data-ttu-id="561bf-104">Если в коде используются универсальные типы данных, их можно скомпилировать для [Юникода](unicode.md) просто с помощью директивы препроцессора, чтобы определить "Unicode" перед инструкциями **\# include** для файлов заголовков.</span><span class="sxs-lookup"><span data-stu-id="561bf-104">If you use generic data types in your code, it can be compiled for [Unicode](unicode.md) simply by using a preprocessor directive to define "UNICODE" before the **\#include** statements for the header files.</span></span> <span data-ttu-id="561bf-105">Чтобы скомпилировать код кодовых [страниц Windows (ANSI)](code-pages.md), опустите определение "Unicode".</span><span class="sxs-lookup"><span data-stu-id="561bf-105">To compile the code for [Windows (ANSI) code pages](code-pages.md), omit the "UNICODE" definition.</span></span> <span data-ttu-id="561bf-106">Новые приложения Windows должны использовать Юникод, чтобы избежать несоответствий между различными кодовыми страницами и упростить локализацию.</span><span class="sxs-lookup"><span data-stu-id="561bf-106">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and simplify localization.</span></span>

<span data-ttu-id="561bf-107">Для создания исходного кода, который может быть скомпилирован либо для использования символов и строк Юникода, либо для использования символов и строк из кодовых страниц Windows:</span><span class="sxs-lookup"><span data-stu-id="561bf-107">To create source code that can be compiled either to use Unicode characters and strings or to use characters and strings from Windows code pages:</span></span>

1.  <span data-ttu-id="561bf-108">Для всех символьных и строковых типов, используемых для текста, используются универсальные типы данных, такие как TCHAR, LPTSTR и ЛПТЧ.</span><span class="sxs-lookup"><span data-stu-id="561bf-108">Use generic data types, such as TCHAR, LPTSTR, and LPTCH, for all character and string types used for text.</span></span> <span data-ttu-id="561bf-109">Дополнительные сведения об универсальных типах см. в разделе [типы данных Windows для строк](windows-data-types-for-strings.md).</span><span class="sxs-lookup"><span data-stu-id="561bf-109">For more about generic types, see [Windows Data Types for Strings](windows-data-types-for-strings.md).</span></span>
2.  <span data-ttu-id="561bf-110">Убедитесь, что указатели на нетекстовые буферы данных или двоичные байтовые массивы кодируются с помощью таких типов данных, как LPBYTE или ЛПВОРД, а не типа LPTSTR или ЛПТЧ.</span><span class="sxs-lookup"><span data-stu-id="561bf-110">Be sure that pointers to non-text data buffers or binary byte arrays are coded with data types such as LPBYTE or LPWORD, instead of the LPTSTR or LPTCH type.</span></span>
3.  <span data-ttu-id="561bf-111">Объявите указатели неопределенного типа явным образом как пустые указатели с помощью ЛПВОИД, как нужно.</span><span class="sxs-lookup"><span data-stu-id="561bf-111">Declare pointers of indeterminate type explicitly as void pointers by using LPVOID as appropriate.</span></span>
4.  <span data-ttu-id="561bf-112">Сделать арифметический тип, не зависящий от указателя.</span><span class="sxs-lookup"><span data-stu-id="561bf-112">Make pointer arithmetic type-independent.</span></span> <span data-ttu-id="561bf-113">Использование единиц размера TCHAR дает переменные размером 2 байта, если определен Юникод, и 1 байт, если Юникод не определен.</span><span class="sxs-lookup"><span data-stu-id="561bf-113">Using units of TCHAR size yields variables that are 2 bytes if UNICODE is defined, and 1 byte if UNICODE is not defined.</span></span> <span data-ttu-id="561bf-114">Использование арифметики указателей всегда возвращает число элементов, обозначенных указателем, независимо от размера элементов: 1 или 2 байта.</span><span class="sxs-lookup"><span data-stu-id="561bf-114">Using pointer arithmetic always returns the number of elements indicated by the pointer, whether the elements are 1 or 2 bytes in size.</span></span> <span data-ttu-id="561bf-115">Следующее выражение всегда получает количество элементов, независимо от того, определено ли значение Юникод.</span><span class="sxs-lookup"><span data-stu-id="561bf-115">The following expression always retrieves the number of elements, regardless of whether UNICODE is defined.</span></span>

    ```C++
    cCount = lpEnd - lpStart;
    ```

    

    <span data-ttu-id="561bf-116">Следующее выражение определяет количество используемых байтов.</span><span class="sxs-lookup"><span data-stu-id="561bf-116">The following expression determines the number of bytes used.</span></span>

    ```C++
    cByteCount = (lpEnd - lpStart) * sizeof(TCHAR);
    ```

    

    <span data-ttu-id="561bf-117">Нет необходимости изменять инструкцию, подобную следующей, поскольку шаг указателя указывает на следующий элемент символа.</span><span class="sxs-lookup"><span data-stu-id="561bf-117">There is no need to change a statement like the following one, because the pointer increment points to the next character element.</span></span>

    ```C++
    chNext = *++lpText;
    ```

    

5.  <span data-ttu-id="561bf-118">Замените литеральные строки и символьные константы манифеста макросами.</span><span class="sxs-lookup"><span data-stu-id="561bf-118">Replace literal strings and manifest character constants with macros.</span></span> <span data-ttu-id="561bf-119">Измените такие выражения, как приведенные ниже.</span><span class="sxs-lookup"><span data-stu-id="561bf-119">Change expressions like the following one.</span></span>

    ```C++
    while(*lpFileName++ != '\\')
    {
        // ...
    }
    ```

    

    <span data-ttu-id="561bf-120">Используйте [**текстовый**](/windows/desktop/api/Winnt/nf-winnt-text) макрос, как показано ниже в этом выражении.</span><span class="sxs-lookup"><span data-stu-id="561bf-120">Use the [**TEXT**](/windows/desktop/api/Winnt/nf-winnt-text) macro as follows in this expression.</span></span>

    ```C++
    while(*lpFileName++ != TEXT('\\'))
    {
        // ...
    }
    ```

    

    <span data-ttu-id="561bf-121">[**Текстовый**](/windows/desktop/api/Winnt/nf-winnt-text) макрос приводит к тому, что строки будут оцениваться как L "строка", когда определен Юникод, а как "строка" в противном случае.</span><span class="sxs-lookup"><span data-stu-id="561bf-121">The [**TEXT**](/windows/desktop/api/Winnt/nf-winnt-text) macro causes strings to be evaluated as L"string" when UNICODE is defined, and as "string" otherwise.</span></span> <span data-ttu-id="561bf-122">Для упрощения управления переместите строковые литералы в ресурсы, особенно если они содержат символы вне диапазона ASCII (от 0x00 до 0x7F) или предоставляются в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="561bf-122">For easier management, move literal strings into resources, especially if they contain characters outside the ASCII range (0x00 through 0x7F) or are exposed at the user interface.</span></span> <span data-ttu-id="561bf-123">Для поддержки локализации приложения для разных национальных языков очень важно, чтобы все строки пользовательского интерфейса набыли в локализуемых ресурсах.</span><span class="sxs-lookup"><span data-stu-id="561bf-123">To support localization of your application for different national languages, it is very important for all user interface strings to be in localizable resources.</span></span>

6.  <span data-ttu-id="561bf-124">Используйте универсальные версии функций Windows.</span><span class="sxs-lookup"><span data-stu-id="561bf-124">Use the generic versions of the Windows functions.</span></span> <span data-ttu-id="561bf-125">Дополнительные сведения см. в разделе [соглашения для прототипов функций](conventions-for-function-prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="561bf-125">For more information, see [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span>
7.  <span data-ttu-id="561bf-126">Используйте универсальные версии стандартных строковых функций библиотеки C и не забудьте определить " \_ Unicode", а также "Unicode", как описано в [стандартных функциях c](standard-c-functions.md).</span><span class="sxs-lookup"><span data-stu-id="561bf-126">Use the generic versions of the standard C library string functions, and remember to define "\_UNICODE" as well as "UNICODE", as discussed in [Standard C Functions](standard-c-functions.md).</span></span>
8.  <span data-ttu-id="561bf-127">При адаптации приложения, изначально написанного для кодовых страниц Windows, не забудьте изменить код, который использует 255 в качестве самого крупного значения для символа.</span><span class="sxs-lookup"><span data-stu-id="561bf-127">If you are adapting an application originally written for Windows code pages, remember to change any code that relies on 255 as the largest value for a character.</span></span>

<span data-ttu-id="561bf-128">При компиляции кода, описанного выше, компилятор может создавать версии приложения на основе кодовой страницы в Юникоде и Windows из одного источника.</span><span class="sxs-lookup"><span data-stu-id="561bf-128">When you compile code that you have written as outlined above, the compiler can create both Unicode and Windows code page versions of your application from the same source.</span></span> <span data-ttu-id="561bf-129">В зависимости от определений Юникода универсальные функции разрешаются для создания тех же двоичных файлов, что и при написании кода исключительно для Юникода или исключительно для кодовых страниц Windows.</span><span class="sxs-lookup"><span data-stu-id="561bf-129">Depending on the definitions for UNICODE, the generic functions are resolved to produce the same binary files as if you wrote code exclusively for Unicode or exclusively for Windows code pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="561bf-130">См. также</span><span class="sxs-lookup"><span data-stu-id="561bf-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="561bf-131">Использование Юникода и кодировок</span><span class="sxs-lookup"><span data-stu-id="561bf-131">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 



