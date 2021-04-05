---
description: Библиотека DbgHelp использует путь поиска символов для поиска отладочных символов (PDB-и DBG-файлов). Путь поиска может состоять из одного или нескольких элементов пути, разделенных точкой с запятой.
ms.assetid: 3527f589-285b-4cdf-b024-17920971a904
title: Пути к символам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 977772e45c345e1e990dc038fccd852d17d279dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990481"
---
# <a name="symbol-paths"></a><span data-ttu-id="69546-104">Пути к символам</span><span class="sxs-lookup"><span data-stu-id="69546-104">Symbol Paths</span></span>

<span data-ttu-id="69546-105">Библиотека DbgHelp использует путь поиска символов для поиска отладочных символов (PDB-и DBG-файлов).</span><span class="sxs-lookup"><span data-stu-id="69546-105">The DbgHelp library uses the symbol search path to locate debug symbols (.pdb and .dbg files).</span></span> <span data-ttu-id="69546-106">Путь поиска может состоять из одного или нескольких элементов пути, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="69546-106">The search path can be made up of one or more path elements separated by semicolons.</span></span>

## <a name="specifying-search-paths"></a><span data-ttu-id="69546-107">Указание путей поиска</span><span class="sxs-lookup"><span data-stu-id="69546-107">Specifying Search Paths</span></span>

<span data-ttu-id="69546-108">Чтобы указать, где обработчик символов будет искать файлы символов в каталогах дисков, вызовите функцию [**симсетсеарчпас**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) .</span><span class="sxs-lookup"><span data-stu-id="69546-108">To specify where the symbol handler will search disk directories for symbol files, call the [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) function.</span></span> <span data-ttu-id="69546-109">Кроме того, можно указать путь поиска символов в параметре *усерсеарчпас* функции [**симинитиализе**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="69546-109">Alternatively, you can specify a symbol search path in the *UserSearchPath* parameter of the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span>

<span data-ttu-id="69546-110">Параметр *усерсеарчпас* в [**Симинитиализе**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) и параметр *SearchPath* в [**симсетсеарчпас**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) принимают указатель на строку, завершающуюся нулем, которая указывает путь или последовательность путей, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="69546-110">The *UserSearchPath* parameter in [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) and the *SearchPath* parameter in [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) take a pointer to a null-terminated string that specifies a path, or series of paths separated by a semicolon.</span></span> <span data-ttu-id="69546-111">Обработчик символов использует эти пути для поиска файлов символов.</span><span class="sxs-lookup"><span data-stu-id="69546-111">The symbol handler uses these paths to search for symbol files.</span></span> <span data-ttu-id="69546-112">Если этот параметр имеет **значение NULL**, обработчик символов выполняет поиск в каталоге, содержащем модуль, для которого выполняется поиск символов.</span><span class="sxs-lookup"><span data-stu-id="69546-112">If this parameter is **NULL**, the symbol handler searches the directory that contains the module for which symbols are being searched.</span></span> <span data-ttu-id="69546-113">В противном случае, если этот параметр указан как значение, отличное от **null** , обработчик символов сначала ищет пути, заданные приложением, перед поиском в каталоге модуля.</span><span class="sxs-lookup"><span data-stu-id="69546-113">Otherwise, if this parameter is specified as a non-**NULL** value, the symbol handler first searches the paths set by the application before searching the module directory.</span></span> <span data-ttu-id="69546-114">Если задать \_ \_ путь к символам NT \_ или \_ \_ \_ \_ переменную среды NT Alt Path, обработчик символов выполняет поиск файлов символов в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="69546-114">If you set the \_NT\_SYMBOL\_PATH or \_NT\_ALT\_SYMBOL\_PATH environment variable, the symbol handler searches for symbol files in the following order:</span></span>

1. <span data-ttu-id="69546-115">\_ \_ \_ Переменная среды Path для символов NT.</span><span class="sxs-lookup"><span data-stu-id="69546-115">The \_NT\_SYMBOL\_PATH environment variable.</span></span>
2. <span data-ttu-id="69546-116">\_ \_ Переменная среды для альтернативного \_ пути к символам NT \_ .</span><span class="sxs-lookup"><span data-stu-id="69546-116">The \_NT\_ALT\_SYMBOL\_PATH environment variable.</span></span>
3. <span data-ttu-id="69546-117">Каталог, содержащий соответствующий модуль.</span><span class="sxs-lookup"><span data-stu-id="69546-117">The directory that contains the corresponding module.</span></span>

<span data-ttu-id="69546-118">Чтобы получить пути поиска, вызовите функцию [**симжетсеарчпас**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) .</span><span class="sxs-lookup"><span data-stu-id="69546-118">To retrieve the search paths, call the [**SymGetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) function.</span></span>

<span data-ttu-id="69546-119">Путь поиска для файлов базы данных программы (PDB) отличается от пути для файлов отладки (dbg).</span><span class="sxs-lookup"><span data-stu-id="69546-119">The search path for program database (.pdb) files is different than the path for debug (.dbg) files.</span></span> <span data-ttu-id="69546-120">Алгоритм определяется функциональными возможностями библиотеки символов.</span><span class="sxs-lookup"><span data-stu-id="69546-120">The algorithm is determined by the functionality of the symbol library.</span></span> <span data-ttu-id="69546-121">По умолчанию Microsoft Visual C/C++ создает символы формата Microsoft, отделяет их от изображения и помещает их в отдельный PDB-файл.</span><span class="sxs-lookup"><span data-stu-id="69546-121">By default, Microsoft Visual C/C++ creates Microsoft format symbols, strips them from the image, and places them in a separate .pdb file.</span></span> <span data-ttu-id="69546-122">Как правило, PDB-файл будет находиться в каталоге, содержащем исполняемый образ.</span><span class="sxs-lookup"><span data-stu-id="69546-122">Typically, the .pdb file will be located in the directory that contains the executable image.</span></span> <span data-ttu-id="69546-123">Visual C/C++ внедряет абсолютный путь к PDB-файлу в исполняемом образе.</span><span class="sxs-lookup"><span data-stu-id="69546-123">Visual C/C++ embeds the absolute path to the .pdb file in the executable image.</span></span> <span data-ttu-id="69546-124">Если обработчик символов не может найти PDB-файл в этом расположении или если PDB-файл был перемещен в другой каталог, обработчик символов обнаружит PDB-файл, используя путь поиска, описанный для DBG-файлов.</span><span class="sxs-lookup"><span data-stu-id="69546-124">If the symbol handler cannot find the .pdb file in that location or if the .pdb file was moved to another directory, the symbol handler will locate the .pdb file using the search path described for .dbg files.</span></span>

## <a name="path-element-types"></a><span data-ttu-id="69546-125">Типы элементов Path</span><span class="sxs-lookup"><span data-stu-id="69546-125">Path Element Types</span></span>

<span data-ttu-id="69546-126">Существует три типа элементов Path.</span><span class="sxs-lookup"><span data-stu-id="69546-126">There are three types of path elements.</span></span>

### <a name="standard-path-element"></a><span data-ttu-id="69546-127">Стандартный элемент Path</span><span class="sxs-lookup"><span data-stu-id="69546-127">Standard Path Element</span></span>

<span data-ttu-id="69546-128">Поиск по стандартному элементу Path осуществляется путем просмотра корня каталога, указанного в элементе Path.</span><span class="sxs-lookup"><span data-stu-id="69546-128">A standard path element is searched by looking in the root of the directory specified by the path element.</span></span> <span data-ttu-id="69546-129">Обработчик символов также выполняет поиск в подкаталоге "Symbols", соответствующем расширению файла модуля, для которого ищутся символы.</span><span class="sxs-lookup"><span data-stu-id="69546-129">The symbol handler also looks in a subdirectory of "symbols" that matches the file extension of the module that symbols are being looked for.</span></span> <span data-ttu-id="69546-130">Обычно это "DLL", "exe" или "sys".</span><span class="sxs-lookup"><span data-stu-id="69546-130">This is typically "dll", "exe", or "sys".</span></span> <span data-ttu-id="69546-131">Наконец, он ищет в подкаталоге «Symbols» каталог с тем же именем, что и у расширения.</span><span class="sxs-lookup"><span data-stu-id="69546-131">Lastly, it looks in a subdirectory called "symbols" with a directory of the same name as the extension.</span></span> <span data-ttu-id="69546-132">Например, если элемент пути к символу имеет значение "c: \\ мисимболс" и файл, для которого выполняется поиск символов, имеет значение "boo.dll", поиск выполняется в следующих каталогах.</span><span class="sxs-lookup"><span data-stu-id="69546-132">For example, if the symbol path element is "c:\\mySymbols" and the file that symbols are being searched for is "boo.dll", then the following directories would be searched.</span></span>

- <span data-ttu-id="69546-133">c: \\ мисимболс</span><span class="sxs-lookup"><span data-stu-id="69546-133">c:\\mySymbols</span></span>  
- <span data-ttu-id="69546-134">c: \\ мисимболс \\ DLL</span><span class="sxs-lookup"><span data-stu-id="69546-134">c:\\mySymbols\\dll</span></span>  
- <span data-ttu-id="69546-135">c: \\ \\ DLL- \\ Библиотека символов мисимболс</span><span class="sxs-lookup"><span data-stu-id="69546-135">c:\\mySymbols\\symbols\\dll</span></span>  

<span data-ttu-id="69546-136">Обработчик символов использует эту логику для поиска по любому элементу пути, который не соответствует критериям, чтобы быть *сервером символов* или *кэшем* (как описано ниже).</span><span class="sxs-lookup"><span data-stu-id="69546-136">The symbol handler uses this logic to search any path element that does not meet the criteria to be a *symbol server* or *cache* (described below).</span></span>

### <a name="symbol-server-path-element"></a><span data-ttu-id="69546-137">Элемент Path сервера символов</span><span class="sxs-lookup"><span data-stu-id="69546-137">Symbol Server Path Element</span></span>

<span data-ttu-id="69546-138">Элемент пути *сервера символов* использует специальную технологию, которая может найти символ, который является точным соответствием для рассматриваемого модуля.</span><span class="sxs-lookup"><span data-stu-id="69546-138">A *symbol server* path element uses special technology that can locate a symbol that is an exact match for the module in question.</span></span> <span data-ttu-id="69546-139">Дополнительные сведения см. [в разделе Использование SymSrv](using-symsrv.md) .</span><span class="sxs-lookup"><span data-stu-id="69546-139">See [Using SymSrv](using-symsrv.md) for more details.</span></span>

<span data-ttu-id="69546-140">Обработчик символов обрабатывает элемент Path как сервер символов, если он начинается с текста "SRV \* ".</span><span class="sxs-lookup"><span data-stu-id="69546-140">The symbol handler treats a path element as a symbol server if it begins with the text, "srv\*".</span></span>

> [!Note]  
> <span data-ttu-id="69546-141">Если текст "SRV \* " не указан, но фактический элемент пути является хранилищем сервера символов, обработчик символов будет действовать так, как если \* бы был указан "SRV".</span><span class="sxs-lookup"><span data-stu-id="69546-141">If the "srv\*" text is not specified but the actual path element is a symbol server store, then the symbol handler will act as if "srv\*" were specified.</span></span> <span data-ttu-id="69546-142">Обработчик символов выполняет это определение, выполняя поиск файла с именем "pingme.txt" в корневом каталоге указанного пути.</span><span class="sxs-lookup"><span data-stu-id="69546-142">The symbol handler makes this determination by searching for the existence of a file called "pingme.txt" in the root directory of the specified path.</span></span>

 

### <a name="cache-path-element"></a><span data-ttu-id="69546-143">Элемент пути кэша</span><span class="sxs-lookup"><span data-stu-id="69546-143">Cache Path Element</span></span>

<span data-ttu-id="69546-144">Элемент пути к *кэшу* — это разновидность элемента пути сервера символов.</span><span class="sxs-lookup"><span data-stu-id="69546-144">A *cache* path element is a variation on a symbol server path element.</span></span>

<span data-ttu-id="69546-145">Этот каталог ищется как любой другой сервер символов.</span><span class="sxs-lookup"><span data-stu-id="69546-145">This directory is searched like any other symbol server.</span></span> <span data-ttu-id="69546-146">Однако если символ не найден здесь и находится в элементе Path, расположенном в цепочке путей к символам, то символ будет скопирован и сохранен на сервере символов, указанном в этом элементе.</span><span class="sxs-lookup"><span data-stu-id="69546-146">However, if the symbol is not found here and it is found in a path element farther down the chain of the symbol path, then the symbol will be copied and stored in the symbol server specified in this element.</span></span>

<span data-ttu-id="69546-147">Обработчик символов обрабатывает элемент Path как элемент кэша, если начинается с текста "Cache \* ".</span><span class="sxs-lookup"><span data-stu-id="69546-147">The symbol handler treats a path element as a cache element if it begins with the text, "cache\*".</span></span> <span data-ttu-id="69546-148">Чтобы указать кэш в "c: \\ микаче", используйте элемент пути к символам "Cache \* c: \\ микаче".</span><span class="sxs-lookup"><span data-stu-id="69546-148">To specify a cache in "c:\\myCache", use a symbol path element of "cache\*c:\\myCache".</span></span>

## <a name="example-search-path"></a><span data-ttu-id="69546-149">Пример пути поиска</span><span class="sxs-lookup"><span data-stu-id="69546-149">Example Search Path</span></span>

<span data-ttu-id="69546-150">Чтобы увидеть, как это работает, задайте путь поиска.</span><span class="sxs-lookup"><span data-stu-id="69546-150">To see how this works, set this search path.</span></span>

`cache*c:\myCache;srv*\\symbols\symbols`

<!-- 
See example from https://docs.microsoft.com/windows-hardware/drivers/debugger/symbol-path
cache*c:\MySymbols;srv*https://msdl.microsoft.com/download/symbols
-->

<span data-ttu-id="69546-151">Ниже приведен список подробных выходных данных обработчика символов при поиске NTDLL. PDB с использованием указанного выше пути поиска.</span><span class="sxs-lookup"><span data-stu-id="69546-151">The following is a listing of the symbol handler's verbose output while searching for ntdll.pdb, using the above listed search path.</span></span>

```
DBGHELP: .\ntdll.pdb - file not found
DBGHELP: .\dll\ntdll.pdb - file not found
DBGHELP: .\symbols\dll\ntdll.pdb - file not found
SYMSRV: c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb not found
SYMSRV: ntdll.pdb from \\symbols\symbols: 10497024 bytes - copied
DBGHELP: c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb already cached
DBGHELP: ntdll - private symbols & lines
c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb
```

<span data-ttu-id="69546-152">Первые три строки выходных данных показывают обработчик символов, обрабатывающий первый элемент пути `.` .</span><span class="sxs-lookup"><span data-stu-id="69546-152">The first three lines of output show the symbol handler processing the first path element of `.`.</span></span> <span data-ttu-id="69546-153">Это стандартный элемент пути.</span><span class="sxs-lookup"><span data-stu-id="69546-153">This is a standard path element.</span></span>

<span data-ttu-id="69546-154">В четвертой строке показан обработчик символов, использующий сервер символов для поиска файла во втором элементе Path, `cache*c:\myCache` который является элементом пути к кэшу.</span><span class="sxs-lookup"><span data-stu-id="69546-154">The fourth line shows the symbol handler using the symbol server to look for the file in the second path element of `cache*c:\myCache` which is a cache path element.</span></span>

<span data-ttu-id="69546-155">Пятая строка показывает, что файл находится в третьем элементе Path объекта `srv*\\symbols\symbols` , который является элементом пути сервера символов.</span><span class="sxs-lookup"><span data-stu-id="69546-155">The fifth line shows the file is found in the third path element of `srv*\\symbols\symbols`, which is a symbol server path element.</span></span>

<span data-ttu-id="69546-156">Шестая строка показывает, что файл копируется в кэш.</span><span class="sxs-lookup"><span data-stu-id="69546-156">The sixth line shows that the file is copied to the cache.</span></span>

<span data-ttu-id="69546-157">Последние две строки, открываемые файлом из кэша.</span><span class="sxs-lookup"><span data-stu-id="69546-157">The last two lines that the file is opened from the cache.</span></span>
