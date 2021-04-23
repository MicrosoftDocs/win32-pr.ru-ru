---
title: Работа с определениями в IDL-файлах
description: На этой странице описывается, почему символы, определенные с помощью \ define, исчезают H-файлы, созданные компилятором MIDL, и что можно делать с ним. Это описание относится ко всем файлам, обрабатываемым MIDL, таким как файлы \. idl, \. ACF, \. h.
ms.assetid: 148dabda-96cc-4f7c-abc7-4bf78ac166ea
keywords:
- MIDL компилятора MIDL, работа с определениями
- Определяет MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4af77979824c2e76352d6f28bef72161249845d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067930"
---
# <a name="dealing-with-defines-in-idl-files"></a><span data-ttu-id="04dd2-106">Работа с \# определениями в IDL-файлах</span><span class="sxs-lookup"><span data-stu-id="04dd2-106">Dealing with \#defines in IDL Files</span></span>

<span data-ttu-id="04dd2-107">На этой странице описывается, почему символы, определенные с помощью инструкции **\# define** , исчезают из H-файлов, СОЗДАННЫХ компилятором MIDL, и что может быть сделано.</span><span class="sxs-lookup"><span data-stu-id="04dd2-107">This page describes why symbols defined with a **\#define** disappear from the MIDL compiler generated H files, and what can be done about it.</span></span> <span data-ttu-id="04dd2-108">Это пояснение относится ко всем файлам, обрабатываемым MIDL, таким как \* IDL-, \* ACF, \* h-файлы.</span><span class="sxs-lookup"><span data-stu-id="04dd2-108">This explanation applies to any files processed by MIDL, such as \*.idl, \*.acf, \*.h files.</span></span>

<span data-ttu-id="04dd2-109">**\# Неопределенность определения** символов является результатом того, что MIDL делегирует предварительную обработку входных файлов препроцессору.</span><span class="sxs-lookup"><span data-stu-id="04dd2-109">The disappearance of **\#define** symbols is a result of MIDL delegating the preprocessing of input files to a preprocessor.</span></span> <span data-ttu-id="04dd2-110">По умолчанию препроцессор является препроцессором C/C++ из среды сборки.</span><span class="sxs-lookup"><span data-stu-id="04dd2-110">By default, the preprocessor is a C/C++ preprocessor from the build environment.</span></span> <span data-ttu-id="04dd2-111">После предварительной обработки входной поток MIDL получает только \# директивы препроцессора Line.</span><span class="sxs-lookup"><span data-stu-id="04dd2-111">After preprocessing, the input stream MIDL receives has only \#line preprocessor directives.</span></span> <span data-ttu-id="04dd2-112">В частности, препроцессор выполняет откат всех определений макросов во входных файлах, поэтому MIDL не может обнаружить их присутствие.</span><span class="sxs-lookup"><span data-stu-id="04dd2-112">In particular, the preprocessor unrolls all macro definitions in input files, and therefore, MIDL cannot detect their presence.</span></span> <span data-ttu-id="04dd2-113">Следовательно, когда MIDL реплицирует определения типов из входного файла в созданный H файл, определения \# не реплицируются.</span><span class="sxs-lookup"><span data-stu-id="04dd2-113">Consequently, when MIDL replicates type definitions from an input file to the generated H file, the \#defines are not replicated.</span></span> <span data-ttu-id="04dd2-114">Поэтому не используйте \# определения непосредственно в IDL-файлах, если они будут использоваться позже из созданного H-файла.</span><span class="sxs-lookup"><span data-stu-id="04dd2-114">Therefore, do not use \#defines directly in IDL files if they are to be used later from the generated H file.</span></span>

<span data-ttu-id="04dd2-115">Рекомендуется использовать следующие четыре решения:</span><span class="sxs-lookup"><span data-stu-id="04dd2-115">The following four workarounds are recommended:</span></span>

-   <span data-ttu-id="04dd2-116">Используйте спецификацию объявления [**const**](const.md) .</span><span class="sxs-lookup"><span data-stu-id="04dd2-116">Use the [**const**](const.md) declaration specification.</span></span>
-   <span data-ttu-id="04dd2-117">Используйте отдельные файлы заголовков, которые импортируются или включаются в IDL-файл, а затем в исходный код C.</span><span class="sxs-lookup"><span data-stu-id="04dd2-117">Use separate header files that are imported or included in the IDL file, and later included in the C-source code.</span></span>
-   <span data-ttu-id="04dd2-118">Используйте константы перечисления в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="04dd2-118">Use enumeration constants in the IDL file.</span></span>
-   <span data-ttu-id="04dd2-119">Используйте [**\_ цитату cpp**](cpp-quote.md) для воспроизведения **\# определения** в создаваемом файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="04dd2-119">Use [**cpp\_quote**](cpp-quote.md) to reproduce **\#define** in the generated header file.</span></span>

<span data-ttu-id="04dd2-120">Константы манифеста можно воспроизвести с помощью **синтаксиса объявления константы IDL**.</span><span class="sxs-lookup"><span data-stu-id="04dd2-120">You can reproduce manifest constants using the **IDL constant-declaration syntax**.</span></span> <span data-ttu-id="04dd2-121">Обратите внимание, что [**константа**](const.md) в объявлении константы IDL отличается от семантики **const** C/C++ и просто вводит именованную константу для компиляции IDL.</span><span class="sxs-lookup"><span data-stu-id="04dd2-121">Note that the [**const**](const.md) in the IDL constant-declaration is different from C/C++ **const** semantics, and simply introduces a named constant for an IDL compilation.</span></span> <span data-ttu-id="04dd2-122">Пример:</span><span class="sxs-lookup"><span data-stu-id="04dd2-122">For example:</span></span>

``` syntax
const short ARRSIZE = 10
```

<span data-ttu-id="04dd2-123">В этом примере указывается, что **аррсизе** является константой со значением 10.</span><span class="sxs-lookup"><span data-stu-id="04dd2-123">This example specifies that **ARRSIZE** is a constant with a value of 10.</span></span> <span data-ttu-id="04dd2-124">Именованные константы можно использовать в деклараторах массивов IDL и в других местах, где программист C будет использовать определение манифеста.</span><span class="sxs-lookup"><span data-stu-id="04dd2-124">Named constants can be used in IDL array declarators and other places where a C programmer would use a manifest defines.</span></span> <span data-ttu-id="04dd2-125">Кроме того, этот синтаксис приводит к тому, что в файле заголовка создается следующая строка:</span><span class="sxs-lookup"><span data-stu-id="04dd2-125">In addition, this syntax results in the following line being generated in the header file:</span></span>

``` syntax
#define ARRSIZE 10
```

<span data-ttu-id="04dd2-126">Еще один способ обрабатывал **\#** операторы определения — упаковать их в отдельный файл заголовка либо в файл, посвященный **\#** определению инструкций, либо в файл, содержащий только определения типов.</span><span class="sxs-lookup"><span data-stu-id="04dd2-126">Another way to handle **\#** define statements is to package them in a separate header file, either into a file devoted to **\#** define statements or into a file that contains only type definitions.</span></span> <span data-ttu-id="04dd2-127">Файл, содержащий только директивы препроцессора, может быть безопасно добавлен и файлом IDL, и файлами C-source.</span><span class="sxs-lookup"><span data-stu-id="04dd2-127">A file that contains only preprocessor directives may be safely included both by the IDL file and the C-source files.</span></span> <span data-ttu-id="04dd2-128">Хотя директивы не будут доступны в файле заголовка, созданном компилятором MIDL, программа C-source может включать в себя отдельный файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="04dd2-128">Although the directives will not be available in the header file generated by the MIDL compiler, the C-source program can include the separate header file.</span></span> <span data-ttu-id="04dd2-129">Аналогичным образом файл заголовка с **\#** инструкциями define и определениями регулярных типов можно импортировать из IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="04dd2-129">In a similar fashion, a header file with **\#** define statements and regular type definitions can be imported from your IDL file.</span></span> <span data-ttu-id="04dd2-130">Этот подход инкапсулирует **\#** инструкции define и typedef, используя их в H-файле таким образом, что **\#** символы определения не используются непосредственно в ИМПОРТИРУЕМом IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="04dd2-130">This approach encapsulates the **\#** define and typedef statements by using them in an H file such that the **\#** define symbols are not used in the importing IDL file directly.</span></span> <span data-ttu-id="04dd2-131">Импорт файла заголовка или IDL в другой IDL предотвращает репликацию инструкций typedef в H-файл, созданный с помощью MIDL (что отличается от **\#** инструкций include).</span><span class="sxs-lookup"><span data-stu-id="04dd2-131">Importing a header or IDL file to another IDL file prevents the typedef statements from being replicated to the H file generated by MIDL (which is in contrast to **\#** include statements).</span></span> <span data-ttu-id="04dd2-132">Такой подход позволяет безопасно ссылаться на исходный файл заголовка из кода C в созданном H-файле без проблем с повторяющимися определениями.</span><span class="sxs-lookup"><span data-stu-id="04dd2-132">This approach allows the original header file to be safely referenced from the C code along the generated H file without having a problem with duplicated definitions.</span></span>

<span data-ttu-id="04dd2-133">Использование констант перечисления в IDL-файле также эффективно.</span><span class="sxs-lookup"><span data-stu-id="04dd2-133">Use of enumeration constants in the IDL file is also effective.</span></span> <span data-ttu-id="04dd2-134">Эти константы можно использовать в константных выражениях в IDL, например в деклараторах массивов.</span><span class="sxs-lookup"><span data-stu-id="04dd2-134">These constants can be used in constant expressions in IDL, for example, in array declarators.</span></span> <span data-ttu-id="04dd2-135">Константы перечисления не удаляются на ранних этапах компиляции MIDL с помощью препроцессора компилятора C-Compiler, поэтому константы перечисления доступны в файле заголовка, созданном компилятором MIDL.</span><span class="sxs-lookup"><span data-stu-id="04dd2-135">Enumeration constants are not removed during the early phases of MIDL compilation by the C-compiler preprocessor, so enumeration constants are available in the header file generated by the MIDL compiler.</span></span> <span data-ttu-id="04dd2-136">Рассмотрим следующий оператор.</span><span class="sxs-lookup"><span data-stu-id="04dd2-136">Consider the following statement:</span></span>

``` syntax
typedef enum midlworkaround { MAXSTRINGCOUNT = 300 };
```

<span data-ttu-id="04dd2-137">Эта инструкция не будет удалена во время компиляции MIDL с помощью препроцессора C, а typedef будет реплицирован в созданный H файл.</span><span class="sxs-lookup"><span data-stu-id="04dd2-137">This statement will not be removed during MIDL compilation by the C preprocessor and the typedef will be replicated to the generated H file.</span></span> <span data-ttu-id="04dd2-138">Константа МАКССТРИНГКАУНТ доступна для программ C-source, которые включают файл заголовка, созданный компилятором MIDL.</span><span class="sxs-lookup"><span data-stu-id="04dd2-138">The constant MAXSTRINGCOUNT is available to C-source programs that include the header file generated by the MIDL compiler.</span></span>

<span data-ttu-id="04dd2-139">И, наконец [**, \_ директива**](cpp-quote.md) языка MIDL для записи произвольной строки может быть использована в созданном H файле.</span><span class="sxs-lookup"><span data-stu-id="04dd2-139">Finally, the [**cpp\_quote**](cpp-quote.md) directive of MIDL can be used to write out an arbitrary string directly into the generated H file.</span></span> <span data-ttu-id="04dd2-140">Например, чтобы получить константу манифеста, которая ранее использовалась на этой странице с помощью **cpp- \_ цитаты**, можно использовать следующую инструкцию:</span><span class="sxs-lookup"><span data-stu-id="04dd2-140">For example, to get the manifest constant used previously on this page with **cpp\_quote**, the following statement can be used:</span></span>

``` syntax
cpp_quote ("#define ARRSIZE 10")
```

<span data-ttu-id="04dd2-141">Эта инструкция приводит к формированию следующей строки в файле заголовка:</span><span class="sxs-lookup"><span data-stu-id="04dd2-141">This statement results in the following line being generated in the header file:</span></span>

``` syntax
#define ARRSIZE 10
```

 

 




