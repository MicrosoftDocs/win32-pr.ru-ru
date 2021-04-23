---
description: Набор тестов IFilter проверяет обработчики фильтров.
ms.assetid: 5ee02af1-1dc9-4d21-868f-4c439970b1ba
title: Тестирование обработчиков фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2a2b0b6a6728051ab22590a481ad23a7197692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144122"
---
# <a name="testing-filter-handlers"></a><span data-ttu-id="2ccac-103">Тестирование обработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="2ccac-103">Testing Filter Handlers</span></span>

<span data-ttu-id="2ccac-104">Набор тестов [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) проверяет обработчики фильтров.</span><span class="sxs-lookup"><span data-stu-id="2ccac-104">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite validates your filter handlers.</span></span> <span data-ttu-id="2ccac-105">Этот набор тестов выполняет следующие действия: вызов методов [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) и проверка возвращаемых значений на соответствие спецификации интерфейса **IFilter** ; и проверка того, что идентификаторы блоков уникальны и увеличиваются, что интерфейс **IFilter** ведет себя согласованно после повторной инициализации, и все вызовы методов **IFilter** с недопустимыми параметрами возвращают ожидаемые коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="2ccac-105">The test suite does so by: calling [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) methods and checking the returned values for compliance with the **IFilter** interface specification; and checking that chunk identifiers are unique and increasing, that the **IFilter** interface behaves consistently after re-initialization, and that any **IFilter** method calls with invalid parameters return expected error codes.</span></span> <span data-ttu-id="2ccac-106">Программы набора тестов также выводят дампы файлов, отфильтрованных обработчиком фильтров, и проверяют сведения о регистрации **IFilter** в реестре.</span><span class="sxs-lookup"><span data-stu-id="2ccac-106">The test suite programs also dump the output of a file filtered by a filter handler, and check the **IFilter** registration information in the registry.</span></span>

<span data-ttu-id="2ccac-107">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2ccac-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="2ccac-108">Вызов из командной строки</span><span class="sxs-lookup"><span data-stu-id="2ccac-108">Command-Line Invocation</span></span>](#command-line-invocation)
  - [<span data-ttu-id="2ccac-109">ifilttst.exe</span><span class="sxs-lookup"><span data-stu-id="2ccac-109">ifilttst.exe</span></span>](#ifilttstexe)
  - [<span data-ttu-id="2ccac-110">filtdump.exe</span><span class="sxs-lookup"><span data-stu-id="2ccac-110">filtdump.exe</span></span>](#filtdumpexe)
  - [<span data-ttu-id="2ccac-111">filtreg.exe</span><span class="sxs-lookup"><span data-stu-id="2ccac-111">filtreg.exe</span></span>](#filtregexe)
  - [<span data-ttu-id="2ccac-112">ifilttst.ini</span><span class="sxs-lookup"><span data-stu-id="2ccac-112">ifilttst.ini</span></span>](#ifilttstini)
- [<span data-ttu-id="2ccac-113">Тестовая процедура IFilter</span><span class="sxs-lookup"><span data-stu-id="2ccac-113">IFilter Test Procedure</span></span>](#ifilter-test-procedure)
  - [<span data-ttu-id="2ccac-114">Проверочный тест</span><span class="sxs-lookup"><span data-stu-id="2ccac-114">Validation Test</span></span>](#validation-test)
  - [<span data-ttu-id="2ccac-115">Проверка согласованности</span><span class="sxs-lookup"><span data-stu-id="2ccac-115">Consistency Test</span></span>](#consistency-test)
  - [<span data-ttu-id="2ccac-116">Недопустимый входной тест</span><span class="sxs-lookup"><span data-stu-id="2ccac-116">Invalid Input Test</span></span>](#invalid-input-test)
  - [<span data-ttu-id="2ccac-117">Тестирование различных конфигураций IFilter</span><span class="sxs-lookup"><span data-stu-id="2ccac-117">Testing Different IFilter Configurations</span></span>](#testing-different-ifilter-configurations)
- [<span data-ttu-id="2ccac-118">Проверка индексации зарегистрированных элементов</span><span class="sxs-lookup"><span data-stu-id="2ccac-118">Ensuring Registered Items Get Indexed</span></span>](#ensuring-registered-items-get-indexed)
  - [<span data-ttu-id="2ccac-119">Пример файла журнала</span><span class="sxs-lookup"><span data-stu-id="2ccac-119">Sample Log File</span></span>](#sample-log-file)
  - [<span data-ttu-id="2ccac-120">Пример файла дампа</span><span class="sxs-lookup"><span data-stu-id="2ccac-120">Sample Dump File</span></span>](#sample-dump-file)
- [<span data-ttu-id="2ccac-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2ccac-121">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="2ccac-122">См. также</span><span class="sxs-lookup"><span data-stu-id="2ccac-122">Related topics</span></span>](#related-topics)

> [!NOTE]  
> <span data-ttu-id="2ccac-123">Если новый обработчик фильтра для типа файла устанавливается в качестве замены для существующей регистрации фильтра, установщик должен сохранить текущую регистрацию и восстановить ее при удалении нового обработчика фильтра.</span><span class="sxs-lookup"><span data-stu-id="2ccac-123">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="2ccac-124">Механизм фильтрации цепочек отсутствует.</span><span class="sxs-lookup"><span data-stu-id="2ccac-124">There is no mechanism to chain filters.</span></span> <span data-ttu-id="2ccac-125">Таким образом, новый обработчик фильтра отвечает за репликацию всех необходимых функций старого фильтра.</span><span class="sxs-lookup"><span data-stu-id="2ccac-125">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>

## <a name="command-line-invocation"></a><span data-ttu-id="2ccac-126">Вызов Command-Line</span><span class="sxs-lookup"><span data-stu-id="2ccac-126">Command-Line Invocation</span></span>

<span data-ttu-id="2ccac-127">Набор тестов [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) состоит из трех приложений командной строки: [ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe)и [filtreg.exe](#filtregexe) и файла инициализации [ifilttst.ini](#ifilttstini).</span><span class="sxs-lookup"><span data-stu-id="2ccac-127">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite consists of three command-line applications - [ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe), and [filtreg.exe](#filtregexe) and an initialization file, [ifilttst.ini](#ifilttstini).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2ccac-128">В Windows 7 и более поздних версиях фильтры, написанные в управляемом коде, явным образом блокируются.</span><span class="sxs-lookup"><span data-stu-id="2ccac-128">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="2ccac-129">Фильтры должны быть написаны в машинном коде из-за потенциальных проблем с управлением версиями среды CLR при работе нескольких надстроек.</span><span class="sxs-lookup"><span data-stu-id="2ccac-129">Filters MUST be written in native code due to potential common language runtime (CLR) versioning issues with the process that multiple add-ins run in.</span></span>

### <a name="ifilttstexe"></a><span data-ttu-id="2ccac-130">ifilttst.exe</span><span class="sxs-lookup"><span data-stu-id="2ccac-130">ifilttst.exe</span></span>

<span data-ttu-id="2ccac-131">Программа ifilttst.exe выполняет несколько тестов для проверки обработчика фильтра.</span><span class="sxs-lookup"><span data-stu-id="2ccac-131">The ifilttst.exe program runs several tests to validate a filter handler.</span></span> <span data-ttu-id="2ccac-132">В следующем примере показано, как вызвать программу ifilttst.exe из командной строки:</span><span class="sxs-lookup"><span data-stu-id="2ccac-132">The following example illustrates how to invoke the ifilttst.exe program from the command line:</span></span>


```
ifilttst /i test.htm /l /d /v 1
```

<span data-ttu-id="2ccac-133">В этом примере выполняются следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="2ccac-133">The example performs the following tasks:</span></span>

- <span data-ttu-id="2ccac-134">Направляет программу для фильтрации файла test.htm</span><span class="sxs-lookup"><span data-stu-id="2ccac-134">Directs the program to filter the file test.htm</span></span>
- <span data-ttu-id="2ccac-135">Перенаправляет сообщения журнала в test.htm. log</span><span class="sxs-lookup"><span data-stu-id="2ccac-135">Redirects the log messages to test.htm.log</span></span>
- <span data-ttu-id="2ccac-136">Перенаправляет сообщения дампа в test.htm. dmp</span><span class="sxs-lookup"><span data-stu-id="2ccac-136">Redirects the dump messages to test.htm.dmp</span></span>
- <span data-ttu-id="2ccac-137">Задает уровень детализации 1</span><span class="sxs-lookup"><span data-stu-id="2ccac-137">Sets the verbosity to 1</span></span>

<span data-ttu-id="2ccac-138">Чтобы Предыдущая команда работала, три файла должны находиться в текущем рабочем каталоге: `test.htm` , [ifilttst.exe](#ifilttstexe)и [ifilttst.ini](#ifilttstini).</span><span class="sxs-lookup"><span data-stu-id="2ccac-138">For the preceding command to work, three files must be located in the current working directory: `test.htm`, [ifilttst.exe](#ifilttstexe), and [ifilttst.ini](#ifilttstini).</span></span> <span data-ttu-id="2ccac-139">Параметры командной строки перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2ccac-139">Command-line switches are listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2ccac-140">Переключение и возможные переменные</span><span class="sxs-lookup"><span data-stu-id="2ccac-140">Switch and possible variables</span></span></th>
<th><span data-ttu-id="2ccac-141">Описание</span><span class="sxs-lookup"><span data-stu-id="2ccac-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ccac-142"><strong>/i имя файла</strong></span><span class="sxs-lookup"><span data-stu-id="2ccac-142"><strong>/i file name</strong></span></span></td>
<td><span data-ttu-id="2ccac-143">Входной файл или каталог для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="2ccac-143">The input file or directory to be filtered.</span></span> <span data-ttu-id="2ccac-144">Имя файла может содержать подстановочные знаки <code>\*</code> и <code>?</code> .</span><span class="sxs-lookup"><span data-stu-id="2ccac-144">The file name can contain the wildcard characters <code>\*</code> and <code>?</code>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ccac-145"><strong>/l</strong></span><span class="sxs-lookup"><span data-stu-id="2ccac-145"><strong>/l</strong></span></span></td>
<td><span data-ttu-id="2ccac-146">Сообщения журнала направляются в файл, а не на экран.</span><span class="sxs-lookup"><span data-stu-id="2ccac-146">Log messages are directed to a file instead of the screen.</span></span> <span data-ttu-id="2ccac-147">Сообщения журнала описывают отдельные выполняемые тесты и результаты тестов с успехом или неудачей.</span><span class="sxs-lookup"><span data-stu-id="2ccac-147">Log messages describe the individual tests performed and the pass/fail results of the tests.</span></span> <span data-ttu-id="2ccac-148">Имя файла журнала совпадает с именем входного файла, но с расширением log.</span><span class="sxs-lookup"><span data-stu-id="2ccac-148">The log file name is the same as the input file name but with a .log extension.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ccac-149"><strong>/d</strong></span><span class="sxs-lookup"><span data-stu-id="2ccac-149"><strong>/d</strong></span></span></td>
<td><span data-ttu-id="2ccac-150">Сообщения дампа направляются в файл, а не на экран.</span><span class="sxs-lookup"><span data-stu-id="2ccac-150">Dump messages are directed to a file instead of the screen.</span></span> <span data-ttu-id="2ccac-151">Сообщения дампа описывают содержимое фрагментов.</span><span class="sxs-lookup"><span data-stu-id="2ccac-151">Dump messages describe the contents of the chunks.</span></span> <span data-ttu-id="2ccac-152">Структура блока создается дампом, если уровень детализации равен 3.</span><span class="sxs-lookup"><span data-stu-id="2ccac-152">The chunk structure is dumped when the verbosity level is 3.</span></span> <span data-ttu-id="2ccac-153">Имя файла дампа совпадает с именем входного файла, но с расширением DMP.</span><span class="sxs-lookup"><span data-stu-id="2ccac-153">The dump file name is the same as the input file name but with a .dmp extension.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ccac-154"><strong>/-л</strong></span><span class="sxs-lookup"><span data-stu-id="2ccac-154"><strong>/-l</strong></span></span></td>
<td><span data-ttu-id="2ccac-155">Отключить ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="2ccac-155">Disable logging.</span></span> <span data-ttu-id="2ccac-156">Этот флаг переопределяет <code>/l</code> параметр.</span><span class="sxs-lookup"><span data-stu-id="2ccac-156">This flag overrides the <code>/l</code> switch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ccac-157"><strong>/-д</strong></span><span class="sxs-lookup"><span data-stu-id="2ccac-157"><strong>/-d</strong></span></span></td>
<td><span data-ttu-id="2ccac-158">Отключение дампа.</span><span class="sxs-lookup"><span data-stu-id="2ccac-158">Disable dumping.</span></span> <span data-ttu-id="2ccac-159">Этот флаг переопределяет <code>/d</code> параметр.</span><span class="sxs-lookup"><span data-stu-id="2ccac-159">This flag overrides the <code>/d</code> switch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ccac-160"><strong>/v целое число</strong></span><span class="sxs-lookup"><span data-stu-id="2ccac-160"><strong>/v integer</strong></span></span></td>
<td><span data-ttu-id="2ccac-161">Уровень детализации.</span><span class="sxs-lookup"><span data-stu-id="2ccac-161">The verbosity level.</span></span> <span data-ttu-id="2ccac-162">По умолчанию используется значение 3.</span><span class="sxs-lookup"><span data-stu-id="2ccac-162">The default is 3.</span></span>
<ul>
<li><span data-ttu-id="2ccac-163">0 — тест записывает в журнал только сообщения об ошибках в интерфейсе <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2ccac-163">0 - The test logs only messages concerning specific <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> interface failures.</span></span> <span data-ttu-id="2ccac-164">Тест создает дамп содержимого фрагмента.</span><span class="sxs-lookup"><span data-stu-id="2ccac-164">The test dumps the chunk contents.</span></span></li>
<li><span data-ttu-id="2ccac-165">1 — тест заносит в журнал предупреждающие сообщения, а также для уровня 0.</span><span class="sxs-lookup"><span data-stu-id="2ccac-165">1 - The test logs warning messages as well as those for level 0.</span></span></li>
<li><span data-ttu-id="2ccac-166">2. тест записывает в журнал сообщения о тестах, пройденных, а также на уровне 1.</span><span class="sxs-lookup"><span data-stu-id="2ccac-166">2 - The test logs messages concerning tests that passed as well as those for level 1.</span></span></li>
<li><span data-ttu-id="2ccac-167">3. тест записывает информационные сообщения, а также для уровня 2.</span><span class="sxs-lookup"><span data-stu-id="2ccac-167">3 - The test logs informational messages as well as those for level 2.</span></span> <span data-ttu-id="2ccac-168">Кроме того, тест создает дамп структуры фрагмента.</span><span class="sxs-lookup"><span data-stu-id="2ccac-168">In addition, the test dumps the structure of the chunk.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ccac-169"><strong>/t целое</strong></span><span class="sxs-lookup"><span data-stu-id="2ccac-169"><strong>/t integer</strong></span></span></td>
<td><span data-ttu-id="2ccac-170">Число запускаемых потоков.</span><span class="sxs-lookup"><span data-stu-id="2ccac-170">The number of threads to launch.</span></span> <span data-ttu-id="2ccac-171">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="2ccac-171">The default is 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ccac-172"><strong>/r целое число</strong>]</span><span class="sxs-lookup"><span data-stu-id="2ccac-172"><strong>/r integer</strong>]</span></span></td>
<td><span data-ttu-id="2ccac-173">Рекурсивно фильтрует подкаталоги.</span><span class="sxs-lookup"><span data-stu-id="2ccac-173">Recursively filters subdirectories.</span></span> <span data-ttu-id="2ccac-174">Необязательный параметр целого числа задает глубину, до которой будет выполняться рекурсия.</span><span class="sxs-lookup"><span data-stu-id="2ccac-174">The optional integer parameter specifies the depth to which to exercise recursion.</span></span> <span data-ttu-id="2ccac-175">Если целое число не указано или целое число равно 0, предполагается полная рекурсия.</span><span class="sxs-lookup"><span data-stu-id="2ccac-175">If no integer is specified, or if the integer is 0, full recursion is assumed.</span></span> <span data-ttu-id="2ccac-176">По умолчанию глубина рекурсии равна 1.</span><span class="sxs-lookup"><span data-stu-id="2ccac-176">By default, the recursion depth is 1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ccac-177"><strong>/c целое</strong></span><span class="sxs-lookup"><span data-stu-id="2ccac-177"><strong>/c integer</strong></span></span></td>
<td><span data-ttu-id="2ccac-178">Число циклов.</span><span class="sxs-lookup"><span data-stu-id="2ccac-178">The number of times to loop.</span></span> <span data-ttu-id="2ccac-179">Если целое число равно 0, то тест циклически подбирается бесконечно.</span><span class="sxs-lookup"><span data-stu-id="2ccac-179">If the integer is 0, the test loops infinitely.</span></span> <span data-ttu-id="2ccac-180">По умолчанию тест циклически обрабатывается только один раз.</span><span class="sxs-lookup"><span data-stu-id="2ccac-180">By default, the test loops only once.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]  
> <span data-ttu-id="2ccac-181">Необходимо включить пробел между параметром командной строки и значением.</span><span class="sxs-lookup"><span data-stu-id="2ccac-181">You must include a space between the command line switch and the value.</span></span>

### <a name="filtdumpexe"></a><span data-ttu-id="2ccac-182">filtdump.exe</span><span class="sxs-lookup"><span data-stu-id="2ccac-182">filtdump.exe</span></span>

<span data-ttu-id="2ccac-183">Программа filtdump.exe загружает обработчик фильтра для указанного документа и выводит результат, созданный DLL-библиотекой [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="2ccac-183">The filtdump.exe program loads a filter handler for a specified document and prints the output produced by the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL.</span></span> <span data-ttu-id="2ccac-184">В следующем примере показано, как вызвать программу filtdump.exe.</span><span class="sxs-lookup"><span data-stu-id="2ccac-184">The following example illustrates how to invoke the filtdump.exe program.</span></span>

```
filtdump filename.ext
```
<span data-ttu-id="2ccac-185">Filtdump.exe использует метод [илоадфилтер:: лоадифилтер](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) для загрузки библиотеки DLL [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , подходящей для указанного расширения имени файла, и выводит результаты.</span><span class="sxs-lookup"><span data-stu-id="2ccac-185">Filtdump.exe uses the [ILoadFilter::LoadIFilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) method to load the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL appropriate for the specified file name extension and prints the results.</span></span> <span data-ttu-id="2ccac-186">Например, следующая команда указывает filtdump.exe загрузить обработчик фильтра smpfilt.dll для расширения SMP, извлечь весь текст и свойства из файла MyFile. SMP и распечатать результаты.</span><span class="sxs-lookup"><span data-stu-id="2ccac-186">For example, the following command instructs filtdump.exe to load the smpfilt.dll filter handler for the extension .smp, extract all text and properties from the file myfile.smp, and print the results.</span></span>

```
filtdump myfile.smp
```

### <a name="filtregexe"></a><span data-ttu-id="2ccac-187">filtreg.exe</span><span class="sxs-lookup"><span data-stu-id="2ccac-187">filtreg.exe</span></span>

<span data-ttu-id="2ccac-188">Программа filtreg.exe проверяет сведения об установке [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) в реестре.</span><span class="sxs-lookup"><span data-stu-id="2ccac-188">The filtreg.exe program inspects [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) installation information in the registry.</span></span> <span data-ttu-id="2ccac-189">Чтобы вызвать программу filtreg.exe из командной строки, введите ее имя, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="2ccac-189">You invoke the filtreg.exe program from the command line by typing its name, as in the following example.</span></span>

```
filtreg
```

<span data-ttu-id="2ccac-190">Filtreg.exe перечисляет все расширения имен файлов, имеющие связанные с ними обработчики фильтров, путем печати расширения имени файла и имени DLL-библиотеки [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) для расширения.</span><span class="sxs-lookup"><span data-stu-id="2ccac-190">Filtreg.exe enumerates all file name extensions that have filter handlers associated with them by printing the file name extension and the name of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL for the extension.</span></span> <span data-ttu-id="2ccac-191">Это простой способ проверки правильности установки **IFilter**.</span><span class="sxs-lookup"><span data-stu-id="2ccac-191">This is a simple way to verify the correct installation of an **IFilter**.</span></span>

### <a name="ifilttstini"></a><span data-ttu-id="2ccac-192">ifilttst.ini</span><span class="sxs-lookup"><span data-stu-id="2ccac-192">ifilttst.ini</span></span>

<span data-ttu-id="2ccac-193">Интерфейс [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) инициализируется путем вызова метода [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="2ccac-193">An [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface is initialized by calling the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span> <span data-ttu-id="2ccac-194">Метод **IFilter:: init** принимает следующие четыре параметра:</span><span class="sxs-lookup"><span data-stu-id="2ccac-194">The **IFilter::Init** method takes the following four parameters:</span></span>

1. <span data-ttu-id="2ccac-195">*грффлагс*</span><span class="sxs-lookup"><span data-stu-id="2ccac-195">*grfFlags*</span></span>
2. <span data-ttu-id="2ccac-196">*cAttributes*</span><span class="sxs-lookup"><span data-stu-id="2ccac-196">*cAttributes*</span></span>
3. <span data-ttu-id="2ccac-197">*ааттрибутес*</span><span class="sxs-lookup"><span data-stu-id="2ccac-197">*aAttributes*</span></span>
4. <span data-ttu-id="2ccac-198">*пдвфлагс*</span><span class="sxs-lookup"><span data-stu-id="2ccac-198">*pdwFlags*</span></span>

<span data-ttu-id="2ccac-199">Пользователь ifilttst.exe программы в наборе тестов [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) может указать значения этих параметров в файле с именем ifilttst.ini.</span><span class="sxs-lookup"><span data-stu-id="2ccac-199">The user of the ifilttst.exe program of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite can specify the values for these parameters in a file called ifilttst.ini.</span></span> <span data-ttu-id="2ccac-200">В следующей таблице описаны записи в файле ifilttst.ini, в которых указываются первые три параметра (входные параметры).</span><span class="sxs-lookup"><span data-stu-id="2ccac-200">The following table describes the entries in the ifilttst.ini file that specify the first three parameters(the input parameters).</span></span> <span data-ttu-id="2ccac-201">Пример файла см. в разделе [sample ifilttst.ini File](#sample-ifilttstini-file).</span><span class="sxs-lookup"><span data-stu-id="2ccac-201">For a sample file, see [Sample ifilttst.ini File](#sample-ifilttstini-file).</span></span>

> [!NOTE]  
> <span data-ttu-id="2ccac-202">Отсутствует запись в таблице для параметра *пдвфлагс* , так как это выходной параметр. перед вызовом метода [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) не обязательно иметь никаких специальных значений.</span><span class="sxs-lookup"><span data-stu-id="2ccac-202">There is no table entry for the *pdwFlags* parameter because it is an output parameter; it does not need to have any special value prior to the call to the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span>

 | <span data-ttu-id="2ccac-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="2ccac-203">Entry</span></span>         | <span data-ttu-id="2ccac-204">Описание</span><span class="sxs-lookup"><span data-stu-id="2ccac-204">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ccac-205">Флаги</span><span class="sxs-lookup"><span data-stu-id="2ccac-205">Flags</span></span>         | <span data-ttu-id="2ccac-206">Имена флагов [**\_ инициализации IFilter**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) , которые должны быть соединены оператором или для формирования параметра *грффлагс* метода [**IFILTER:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="2ccac-206">The names of the [**IFILTER\_INIT**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) flags that are to be joined by the OR operator to form the *grfFlags* parameter of the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span> <span data-ttu-id="2ccac-207">Имена флагов должны быть в верхнем регистре и в той же строке.</span><span class="sxs-lookup"><span data-stu-id="2ccac-207">The flag names must all be uppercase, and on the same line.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="2ccac-208">*cAttributes*</span><span class="sxs-lookup"><span data-stu-id="2ccac-208">*cAttributes*</span></span> | <span data-ttu-id="2ccac-209">Десятичное целое число, представляющее значение параметра *cAttributes* .</span><span class="sxs-lookup"><span data-stu-id="2ccac-209">A decimal integer representing the value of the *cAttributes* parameter.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="2ccac-210">*ааттрибутес*</span><span class="sxs-lookup"><span data-stu-id="2ccac-210">*aAttributes*</span></span> | <span data-ttu-id="2ccac-211">Эта запись должна начинаться с *ааттрибутес* и должна отличаться от других записей *ааттрибутес* в разделе.</span><span class="sxs-lookup"><span data-stu-id="2ccac-211">This entry must start with *aAttributes* and must be different from the other *aAttributes* entries within the section.</span></span> <span data-ttu-id="2ccac-212">Допустимые имена для записи *ааттрибутес* : *ааттрибутес*, *aAttributes1*, *aAttributes2* и т. д.</span><span class="sxs-lookup"><span data-stu-id="2ccac-212">Legal names for the *aAttributes* entry are: *aAttributes*, *aAttributes1*, *aAttributes2*, and so forth.</span></span> <span data-ttu-id="2ccac-213">Первый токен должен быть идентификатором GUID.</span><span class="sxs-lookup"><span data-stu-id="2ccac-213">The first token must be a GUID.</span></span> <span data-ttu-id="2ccac-214">GUID должен быть отформатирован точно так же, как показано в `[Test3]` разделе [примера файла ifilttst.ini](#sample-ifilttstini-file).</span><span class="sxs-lookup"><span data-stu-id="2ccac-214">The GUID must be formatted exactly as illustrated in the `[Test3]` section of the [Sample ifilttst.ini File](#sample-ifilttstini-file).</span></span> <span data-ttu-id="2ccac-215">Второй токен может быть идентификатором свойства (PID), состоящим из числа в шестнадцатеричном формате, или указателя на строку расширенных символов (LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="2ccac-215">The second token can be either a property identifier (PID) consisting of a number in hexadecimal notation, or a pointer to a wide character string (lpwstr).</span></span> <span data-ttu-id="2ccac-216">LPWSTR можно указать, заключив строку в двойные кавычки, как показано в `[Test6]` разделе примера файла ifilttst.ini.</span><span class="sxs-lookup"><span data-stu-id="2ccac-216">A lpwstr can be specified by enclosing the string in double quotes, as illustrated in the `[Test6]` section of the Sample ifilttst.ini File.</span></span> |

<span data-ttu-id="2ccac-217">Если флаги и записи *cAttributes* не указаны, они по умолчанию имеют значение 0.</span><span class="sxs-lookup"><span data-stu-id="2ccac-217">If the Flags and *cAttributes* entries are not specified, they default to 0.</span></span> <span data-ttu-id="2ccac-218">Если задать *cAttributes* равным 2, следует указать два имени *ааттрибутес* .</span><span class="sxs-lookup"><span data-stu-id="2ccac-218">If you set *cAttributes* equal to 2, you should specify two *aAttributes* names.</span></span> <span data-ttu-id="2ccac-219">В `[Test5]` разделе примера *cAttributes* имеет значение 1, но *ааттрибутес* не указаны.</span><span class="sxs-lookup"><span data-stu-id="2ccac-219">In the `[Test5]` section of the sample, *cAttributes* is 1, but no *aAttributes* have been specified.</span></span> <span data-ttu-id="2ccac-220">Затем тест вызывает метод [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) с *cAttributes* , равным 1, и *ааттрибутес* , равным **null**.</span><span class="sxs-lookup"><span data-stu-id="2ccac-220">The test then calls the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method with *cAttributes* equal to 1 and *aAttributes* equal to **NULL**.</span></span> <span data-ttu-id="2ccac-221">Это полезный тестовый случай, так как, скорее всего, вызовет нарушение прав доступа в методе **IFilter:: init** .</span><span class="sxs-lookup"><span data-stu-id="2ccac-221">This is a useful test case because it is likely to cause an access violation in the **IFilter::Init** method.</span></span>

<span data-ttu-id="2ccac-222">Если ifilttst.exe не удается найти файл с именем ifilttst.ini в рабочем каталоге, для инициализации объекта [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) используется конфигурация по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2ccac-222">If ifilttst.exe cannot find a file named ifilttst.ini in the working directory, a default configuration is used to initialize the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) object.</span></span> <span data-ttu-id="2ccac-223">В следующем примере показана конфигурация по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2ccac-223">The following example illustrates the default configuration.</span></span>

```
[default]
            grfFlags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

```

### <a name="sample-ifilttstini-file"></a><span data-ttu-id="2ccac-224">Пример файла ifilttst.ini</span><span class="sxs-lookup"><span data-stu-id="2ccac-224">Sample ifilttst.ini File</span></span>

<span data-ttu-id="2ccac-225">Файл ifilttst.ini организован в разделы, имя раздела которых заключено в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="2ccac-225">The ifilttst.ini file is organized in sections, with the section name enclosed in square brackets.</span></span> <span data-ttu-id="2ccac-226">В этом примере разделам присваиваются имена `[Test1]` , `[Test2]` и т. д.</span><span class="sxs-lookup"><span data-stu-id="2ccac-226">In the example, the sections are named `[Test1]`, `[Test2]`, and so forth.</span></span> <span data-ttu-id="2ccac-227">Все имена разделов должны быть уникальными.</span><span class="sxs-lookup"><span data-stu-id="2ccac-227">All section names must be unique.</span></span> <span data-ttu-id="2ccac-228">Тест считывает значения из первого раздела и инициализирует [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) с этими значениями.</span><span class="sxs-lookup"><span data-stu-id="2ccac-228">The test reads the values from the first section and initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) with those values.</span></span> <span data-ttu-id="2ccac-229">Затем выполняются все тесты с использованием этой конфигурации **IFilter** .</span><span class="sxs-lookup"><span data-stu-id="2ccac-229">Then all the tests are run using this **IFilter** configuration.</span></span> <span data-ttu-id="2ccac-230">Затем **IFilter** освобождается и повторно инициализируется с использованием параметров, перечисленных выше.</span><span class="sxs-lookup"><span data-stu-id="2ccac-230">Then the **IFilter** is released and reinitialized, using parameters that are listed above.</span></span> <span data-ttu-id="2ccac-231">Процесс повторяется до тех пор, пока все конфигурации не будут проверены.</span><span class="sxs-lookup"><span data-stu-id="2ccac-231">The process is repeated until all configurations are tested.</span></span>

```
; Only extract text from the object
            [Test1]
            Flags =
            cAttributes = 0

            // Get all attributes (text-type and internal value-type properties.
            [Test2]
            Flags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

            // This also extracts just text from the object (the GUID is PSGUID_STORAGE, and the propid is
            // PID_STG_CONTENTS).
            [Test3]
            Flags = IFILTER_INIT_CANON_PARAGRAPHS IFILTER_INIT_HARD_LINE_BREAKS
            cAttributes = 1
            aAttributes1 = b725f130-47ef-101a-a5f1-02608c9eebac 13

            // Only extract requested attribute from the html object (the GUID corresponds to the HTML IFilter.
            [Test4]
            Flags = IFILTER_INIT_CANON_HYPHENS IFILTER_INIT_CANON_SPACES
            cAttributes = 1
            aAttributes1 = 70eb7a10-55d9-11cf-b75b-00aa0051fe20 2

            // Question: what happens if cAttributes is nonzero, but aAttributes is empty?
            [Test5]
            Flags = IFILTER_INIT_CANON_SPACES IFILTER_INIT_APPLY_INDEX_ATTRIBUTES IFILTER_INIT_APPLY_OTHER_ATTRIBUTES
            cAttributes = 1

            // Here is an attribute with a lpwstr instead of a propid (the lpwstr is enclosed in quotes).
            // The GUID corresponds to the meta tag clsid for the HTML IFilter.
            [Test6]
            Flags =
            cAttributes = 1
            aAttributes1 = D1B5D3F0-C0B3-11CF-9A92-00A0C908DBF1 "GENERATOR"
```

## <a name="ifilter-test-procedure"></a><span data-ttu-id="2ccac-232">Тестовая процедура IFilter</span><span class="sxs-lookup"><span data-stu-id="2ccac-232">IFilter Test Procedure</span></span>

<span data-ttu-id="2ccac-233">После инициализации [**фильтра IFilter**](/windows/win32/api/filter/nn-filter-ifilter) программа ifilttst.exe выполняет ряд тестов на **IFilter**.</span><span class="sxs-lookup"><span data-stu-id="2ccac-233">After the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) has been initialized, the ifilttst.exe program conducts a series of tests on the **IFilter**.</span></span> <span data-ttu-id="2ccac-234">Помимо реализации процедур тестирования **IFilter** убедитесь, что реализация **IFilter** использует методы безопасного кода.</span><span class="sxs-lookup"><span data-stu-id="2ccac-234">In addition to following the **IFilter** test procedures, ensure that your **IFilter** implementation employs secure code practices.</span></span> <span data-ttu-id="2ccac-235">См. раздел «рекомендации по обеспечению безопасного кода для Windows Search» в разделе [Реализация обработчиков фильтров в Windows Search](-search-ifilter-constructing-filters.md).</span><span class="sxs-lookup"><span data-stu-id="2ccac-235">See "Secure Code Practices for Windows Search" in [Implementing Filter Handlers in Windows Search](-search-ifilter-constructing-filters.md).</span></span>

### <a name="validation-test"></a><span data-ttu-id="2ccac-236">Проверочный тест</span><span class="sxs-lookup"><span data-stu-id="2ccac-236">Validation Test</span></span>

<span data-ttu-id="2ccac-237">Проверочный тест проходит через объект по одному блоку за раз, проверяя каждый отдельный фрагмент и все коды возврата.</span><span class="sxs-lookup"><span data-stu-id="2ccac-237">The validation test steps through the object one chunk at a time, verifying each individual chunk and all return codes.</span></span> <span data-ttu-id="2ccac-238">Проверочный тест сохраняет все возвращенные структуры [**\_ блока статистики**](/windows/win32/api/filter/ns-filter-stat_chunk) в списке.</span><span class="sxs-lookup"><span data-stu-id="2ccac-238">The validation test saves all returned [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk) structures in a list.</span></span>

<span data-ttu-id="2ccac-239">Проверочный тест проверяет следующие условия.</span><span class="sxs-lookup"><span data-stu-id="2ccac-239">The validation test verifies the following conditions:</span></span>

- <span data-ttu-id="2ccac-240">[**\_ Блок stat**](/windows/win32/api/filter/ns-filter-stat_chunk).\*\* идентификаторы фрагментов идчунк должны быть уникальными и увеличиваться.</span><span class="sxs-lookup"><span data-stu-id="2ccac-240">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunk* chunk IDs must be unique and increasing.</span></span>
- <span data-ttu-id="2ccac-241">[**\_ Блок stat**](/windows/win32/api/filter/ns-filter-stat_chunk).*параметр flags* является распознаваемым состоянием блока, таким как [**чункстате**](/windows/win32/api/filter/ne-filter-chunkstate), текст фрагмента \_ или \_ константы ценабледхунк значений.</span><span class="sxs-lookup"><span data-stu-id="2ccac-241">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*flags* parameter is a recognized chunk state, such as [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate), CHUNK\_TEXT, or CenabledHUNK\_VALUE constants.</span></span>
- <span data-ttu-id="2ccac-242">[**\_ Блок stat**](/windows/win32/api/filter/ns-filter-stat_chunk).*параметр Бреактипе* является распознаваемым типом разрыва (0, 1, 2, 3, 4).</span><span class="sxs-lookup"><span data-stu-id="2ccac-242">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*breakType* parameter is a recognized break type (0, 1, 2, 3, 4).</span></span>
- <span data-ttu-id="2ccac-243">Если атрибуты инициализации [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) указывают, что **IFilter** должен возвращать только фрагменты, содержащие внутренние свойства типа значения, то *идчунксаурце* должен равняться 0.</span><span class="sxs-lookup"><span data-stu-id="2ccac-243">If the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) initialization attributes specify that the **IFilter** should return only chunks containing internal value-type properties, then *idChunkSource* must equal 0.</span></span>
- <span data-ttu-id="2ccac-244">Если фрагмент не является производным, то есть, если он не является внутренним свойством типа значения, то параметр [**stat- \_ блока**](/windows/win32/api/filter/ns-filter-stat_chunk).*Идчунксаурце* должен равняться **\_ блоку stat**.*Идчунк*.</span><span class="sxs-lookup"><span data-stu-id="2ccac-244">If the chunk is not derived that is, if it is not an internal value-type property, then [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunkSource* must equal **STAT\_CHUNK**.*idChunk*.</span></span>
- <span data-ttu-id="2ccac-245">[**IFilter::**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) noreturn возвращает S \_ ОК или другое допустимое возвращаемое значение, например фильтр \_ по \_ концу \_ \_ фрагментов, фильтр \_ e \_ \_ недоступен и т. д.</span><span class="sxs-lookup"><span data-stu-id="2ccac-245">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns S\_OK or other acceptable return value, such as FILTER\_E\_END\_OF\_CHUNKS, FILTER\_E\_LINK\_UNAVAILABLE, and so forth.</span></span>
- <span data-ttu-id="2ccac-246">Если фрагмент текста содержит текст, то функция [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) возвращает значение S \_ OK, фильтр \_ S \_ Last \_ Text или \_ фильтр \_ е \_ без \_ текста.</span><span class="sxs-lookup"><span data-stu-id="2ccac-246">If the chunk contains text, [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns S\_OK, FILTER\_S\_LAST\_TEXT, or FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="2ccac-247">Если [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) возвращает \_ \_ последний текст Filter S \_ , следующий вызов функции **IFilter:: GetText** вернет фильтр \_ E \_ без \_ \_ текста.</span><span class="sxs-lookup"><span data-stu-id="2ccac-247">If [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns FILTER\_S\_LAST\_TEXT, the next call to **IFilter::GetText** returns FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="2ccac-248">Если блок содержит значение, то функция [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) возвращает \_ ОК или фильтр \_ E \_ больше не \_ содержит \_ значений.</span><span class="sxs-lookup"><span data-stu-id="2ccac-248">If the chunk contains a value, [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns S\_OK or FILTER\_E\_NO\_MORE\_VALUES.</span></span>

### <a name="consistency-test"></a><span data-ttu-id="2ccac-249">Проверка согласованности</span><span class="sxs-lookup"><span data-stu-id="2ccac-249">Consistency Test</span></span>

<span data-ttu-id="2ccac-250">Программа ifilttxt.exe повторно инициализирует интерфейс [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) с теми же параметрами, что и в проверочном тесте, и выполняет проверку согласованности.</span><span class="sxs-lookup"><span data-stu-id="2ccac-250">The ifilttxt.exe program re-initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface with the same parameters as in the validation test and performs a consistency test.</span></span> <span data-ttu-id="2ccac-251">Если реализация **IFilter** была инициализирована с флагом "только индексирование [**IFilter \_ init**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) \_ init" \_ \_ , тест освобождает интерфейс **IFilter** и повторно привязывает его перед другим вызовом метода [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="2ccac-251">If the **IFilter** implementation has been initialized with the [**IFILTER\_INIT**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) IFILTER\_INIT\_INDEXING\_ONLY flag, the test releases the **IFilter** interface and re-binds it before making another call to the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span>

<span data-ttu-id="2ccac-252">Проверка согласованности проверяет следующие условия.</span><span class="sxs-lookup"><span data-stu-id="2ccac-252">The consistency test verifies the following conditions:</span></span>

- <span data-ttu-id="2ccac-253">Каждая [**Структура \_ блока stat**](/windows/win32/api/filter/ns-filter-stat_chunk) , возвращаемая методом [**IFilter::-блока**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) , идентична соответствующему **\_ блоку stat** , возвращенному в проверочном тесте.</span><span class="sxs-lookup"><span data-stu-id="2ccac-253">Each [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk) structure returned by the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) method is identical to the corresponding **STAT\_CHUNK** returned in the validation test.</span></span>
- <span data-ttu-id="2ccac-254">[**IFilter::**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) noreturn возвращает S \_ ОК или другое допустимое возвращаемое значение, например фильтр \_ по \_ концу \_ \_ фрагментов, фильтр \_ e \_ \_ недоступен и т. д.</span><span class="sxs-lookup"><span data-stu-id="2ccac-254">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns S\_OK or other acceptable return value, such as FILTER\_E\_END\_OF\_CHUNKS, FILTER\_E\_LINK\_UNAVAILABLE, and so forth.</span></span>

### <a name="invalid-input-test"></a><span data-ttu-id="2ccac-255">Недопустимый входной тест</span><span class="sxs-lookup"><span data-stu-id="2ccac-255">Invalid Input Test</span></span>

<span data-ttu-id="2ccac-256">Программа ifilttst.exe повторно инициализирует интерфейс [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) с теми же параметрами и выполняет Недопустимый входной тест.</span><span class="sxs-lookup"><span data-stu-id="2ccac-256">The ifilttst.exe program re-initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface with the same parameters,and performs an invalid input test.</span></span> <span data-ttu-id="2ccac-257">Этот тест проходит по одному фрагменту документа за раз при неправильном вызове функции, например при вызове метода [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) , если текущий Чак содержит текст.</span><span class="sxs-lookup"><span data-stu-id="2ccac-257">This test steps through the document one chunk at a time making function calls incorrectly, such as calling the [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) method when the current chuck contains text.</span></span> <span data-ttu-id="2ccac-258">Тест проверяет все коды возврата на соответствие спецификации **IFilter** .</span><span class="sxs-lookup"><span data-stu-id="2ccac-258">The test checks all return codes for compliance with the **IFilter** specification.</span></span>

<span data-ttu-id="2ccac-259">Недопустимый входной тест проверяет следующие условия.</span><span class="sxs-lookup"><span data-stu-id="2ccac-259">The invalid input test verifies the following conditions:</span></span>

- <span data-ttu-id="2ccac-260">Если текущий фрагмент содержит текст, функция [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) Возвращает фильтр \_ E \_ без \_ значений и вызов [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) завершается.</span><span class="sxs-lookup"><span data-stu-id="2ccac-260">If the current chunk contains text, [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns FILTER\_E\_NO\_VALUES, and a call to [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) succeeds.</span></span>
- <span data-ttu-id="2ccac-261">Если текущий блок содержит значение, [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) Возвращает фильтр \_ E \_ без \_ текста, а вызов [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="2ccac-261">If the current chunk contains a value, [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns FILTER\_E\_NO\_TEXT, and a call to [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) succeeds.</span></span>
- <span data-ttu-id="2ccac-262">Если предыдущий вызов функции [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) вернул фильтр \_ e \_ без \_ \_ текста, последовательные вызовы **IFilter:: GetText** возвращают фильтр \_ e \_ без \_ \_ текста.</span><span class="sxs-lookup"><span data-stu-id="2ccac-262">If the previous call to [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returned FILTER\_E\_NO\_MORE\_TEXT, successive calls to **IFilter::GetText** return FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="2ccac-263">Если предыдущий вызов функции [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) вернул фильтр \_ e \_ больше \_ \_ значений, последовательные вызовы функции **IFilter:: GetValue** возвращают фильтр \_ e \_ больше не имеют \_ \_ значений.</span><span class="sxs-lookup"><span data-stu-id="2ccac-263">If the previous call to [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returned FILTER\_E\_NO\_MORE\_VALUES, successive calls to **IFilter::GetValue** return FILTER\_E\_NO\_MORE\_VALUES.</span></span>
- <span data-ttu-id="2ccac-264">Если предыдущий вызов функции [**IFilter::**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) NORETURN вернул фильтр по \_ \_ концу \_ \_ фрагментов, последовательные вызовы **IFilter::** noreturn возвращают фильтр по \_ \_ концу \_ \_ фрагментов.</span><span class="sxs-lookup"><span data-stu-id="2ccac-264">If the previous call to [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returned FILTER\_E\_END\_OF\_CHUNKS, successive calls to **IFilter::GetChunk** return FILTER\_E\_END\_OF\_CHUNKS.</span></span>

> [!NOTE]  
> <span data-ttu-id="2ccac-265">Недопустимый входной тест сравнивает текущие структуры фрагментов с теми, которые возвращены в проверочном тесте, чтобы убедиться, что они идентичны.</span><span class="sxs-lookup"><span data-stu-id="2ccac-265">The invalid input test compares the current chunk structures to those returned in the validation test to make sure they are identical.</span></span>

### <a name="testing-different-ifilter-configurations"></a><span data-ttu-id="2ccac-266">Тестирование различных конфигураций IFilter</span><span class="sxs-lookup"><span data-stu-id="2ccac-266">Testing Different IFilter Configurations</span></span>

<span data-ttu-id="2ccac-267">Программа ifilttst.exe освобождает интерфейс [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) и выполняет повторную привязку, при этом инициализирует его со следующим набором параметров.</span><span class="sxs-lookup"><span data-stu-id="2ccac-267">The ifilttst.exe program releases the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface and rebinds, this time initializing it with the next set of parameters.</span></span> <span data-ttu-id="2ccac-268">Тест повторяет цикл: проверочный тест, тест согласованности и недопустимый входной тест, пока не будут протестированы все требуемые конфигурации **IFilter** , указанные в файле [ifilttst.ini](#ifilttstini) .</span><span class="sxs-lookup"><span data-stu-id="2ccac-268">The test repeats the cycle: validation test, consistency test, and invalid input test, until all the desired **IFilter** configurations specified in [ifilttst.ini](#ifilttstini) file have been tested.</span></span>

## <a name="ensuring-registered-items-get-indexed"></a><span data-ttu-id="2ccac-269">Проверка индексации зарегистрированных элементов</span><span class="sxs-lookup"><span data-stu-id="2ccac-269">Ensuring Registered Items Get Indexed</span></span>

<span data-ttu-id="2ccac-270">Окончательная проверка [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) гарантирует, что **IFilter** будет правильно зарегистрирована и вызвана для индексации элементов, которые вы зарегистрировали для использования.</span><span class="sxs-lookup"><span data-stu-id="2ccac-270">The final test of your [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ensures that your **IFilter** is properly registered and that it is invoked to index the items that you registered to use it.</span></span> <span data-ttu-id="2ccac-271">Можно использовать диспетчер каталогов для инициации повторного индексирования или использования диспетчера области сканирования (CSM) для настройки правил по умолчанию, указывающих URL-адреса, которые должен обходить индексатор.</span><span class="sxs-lookup"><span data-stu-id="2ccac-271">You can use the Catalog Manager to initiate re-indexing, or use the Crawl Scope Manager (CSM) to set up default rules indicating the URLs that you want the indexer to crawl.</span></span> <span data-ttu-id="2ccac-272">После завершения индексирования используйте пользовательский интерфейс поиска Windows для поиска строки в содержимом или свойствах элементов.</span><span class="sxs-lookup"><span data-stu-id="2ccac-272">After indexing is complete, use the Windows Search UI to search for a string in the content or properties of items.</span></span> <span data-ttu-id="2ccac-273">Если элементы были проиндексированы, они будут отображаться в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="2ccac-273">If the items were indexed, they will appear in the search results.</span></span>

<span data-ttu-id="2ccac-274">Дополнительные сведения о повторной индексации см. в разделе [Использование диспетчера каталогов](-search-3x-wds-mngidx-catalog-manager.md) и [диспетчера области сканирования](-search-3x-wds-extidx-csm.md).</span><span class="sxs-lookup"><span data-stu-id="2ccac-274">For more information about re-indexing, see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span> <span data-ttu-id="2ccac-275">В образце кода Реиндексматчингурлс показаны способы указания файлов для повторного индексирования и способа.</span><span class="sxs-lookup"><span data-stu-id="2ccac-275">The ReindexMatchingUrls code sample demonstrates ways to specify which files to re-index and how.</span></span> <span data-ttu-id="2ccac-276">В образце кода Кравлскопекоммандлине показано, как определить параметры командной строки для операций индексирования диспетчера области сканирования (CSM).</span><span class="sxs-lookup"><span data-stu-id="2ccac-276">The CrawlScopeCommandLine code sample demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.</span></span> <span data-ttu-id="2ccac-277">Оба примера кода доступны на сайте [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span><span class="sxs-lookup"><span data-stu-id="2ccac-277">Both code samples are available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span></span>

### <a name="sample-log-file"></a><span data-ttu-id="2ccac-278">Пример файла журнала</span><span class="sxs-lookup"><span data-stu-id="2ccac-278">Sample Log File</span></span>

<span data-ttu-id="2ccac-279">По запросу программа Ifilttst.exe может создать журнал, содержащий описание действий, выполняемых во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="2ccac-279">Upon request, the Ifilttst.exe program can produce a log containing a description of the steps it takes during execution.</span></span> <span data-ttu-id="2ccac-280">Следующие примеры являются выдержками из файла журнала с уровнем детализации, равным максимально возможное значение 3.</span><span class="sxs-lookup"><span data-stu-id="2ccac-280">The following examples are excerpts from a log file, with the verbosity set to the highest possible value 3.</span></span>

```
            1. INFO----**** New configuration ****
            2.
            3. Section name : Test2
            4. grfFlags     : 63
            5. cAttributes  : 0
            6. aAttributes  : NONE
            7. pdwFlags     : 0
            8.
            9. INFO----Successfully bound filter.
            10.
            11. PASS----Init() returned a valid value for pdwFlags.
            12.
            13. INFO----Successfully initialized filter.
            14.
            15. INFO----Performing validation test. In this part of the test, the chunks structures
            16.         returned by the IFilter are checked for correctness, and the return values
            17.         of the IFilter calls are checked.
            18.
            19. PASS----GetChunk() succeeded.
            20.
            21. PASS----The current chunk has a legal value for the flags field.

```

<span data-ttu-id="2ccac-281">Первая строка представляет собой информационное сообщение, указывающее, что новая конфигурация загружена из файла ifilttst.ini.</span><span class="sxs-lookup"><span data-stu-id="2ccac-281">The first line is an informational message, indicating that a new configuration has been loaded from the ifilttst.ini file.</span></span> <span data-ttu-id="2ccac-282">Line (3) указывает имя раздела в файле ifilttst.ini, из которого считывается текущая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="2ccac-282">Line (3) indicates the section name in the ifilttst.ini file from which the current configuration has been read.</span></span> <span data-ttu-id="2ccac-283">Строки (с 4) по (7). перечисление параметров в [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init).</span><span class="sxs-lookup"><span data-stu-id="2ccac-283">Lines (4) through (7) list the parameters to [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init).</span></span> <span data-ttu-id="2ccac-284">Строки, начинающиеся с `INFO` , являются информационными сообщениями о привязке [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) и запуске проверки.</span><span class="sxs-lookup"><span data-stu-id="2ccac-284">The lines starting with `INFO` are informational messages about the binding of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) and the start of the validation test.</span></span> <span data-ttu-id="2ccac-285">Строки, начинающиеся с `PASS` , — это сообщения о конкретных тестах, которые прошли.</span><span class="sxs-lookup"><span data-stu-id="2ccac-285">Lines starting with `PASS` are messages regarding specific tests that have passed.</span></span>

<span data-ttu-id="2ccac-286">Строка в следующем примере журнала является предупреждением.</span><span class="sxs-lookup"><span data-stu-id="2ccac-286">The line in the following log example is a warning.</span></span> <span data-ttu-id="2ccac-287">Предупреждения вызывают проблемы с поведением [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , которое является проблематичным, хотя и юридическим.</span><span class="sxs-lookup"><span data-stu-id="2ccac-287">Warnings call attention to [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) behavior that is problematic, although legal.</span></span> <span data-ttu-id="2ccac-288">Это предупреждение означает, что метод [**IFilter::**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) gettext вернул текстовый фрагмент, который не содержит текста.</span><span class="sxs-lookup"><span data-stu-id="2ccac-288">This warning indicates that the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) method has returned a text chunk that contains no text.</span></span>

```
WARNING-First call to GetText() returned FILTER_E_NO_MORE_TEXT.
```

<span data-ttu-id="2ccac-289">В следующем примере появляется сообщение об ошибке, указывающее, что [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) выдал незапрошенный фрагмент.</span><span class="sxs-lookup"><span data-stu-id="2ccac-289">The following example error message indicates that the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitted a chunk that was not requested.</span></span>

```
            ERROR---The IFilter has emitted a chunk which it was not requested to emit.
            Check the initialization parameters in section Test1 of the initialization file.
            INFO----Current chunk propid : 0x5
```

<span data-ttu-id="2ccac-290">В случае этого примера сообщения об ошибке [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) выдал фрагмент с идентификатором PID `0x5` .</span><span class="sxs-lookup"><span data-stu-id="2ccac-290">In the case of this example error message, the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitted a chunk with a PID of `0x5`.</span></span> <span data-ttu-id="2ccac-291">Проверка раздела `[Test1]` в ifilttst.ini покажет, что **Фильтр IFilter** был настроен так, чтобы не выдавал блоки с этим PID.</span><span class="sxs-lookup"><span data-stu-id="2ccac-291">Inspection of section `[Test1]` in ifilttst.ini would show that the **IFilter** was configured to not emit chunks with this PID.</span></span> <span data-ttu-id="2ccac-292">Например, если ни один из методов инициализации IFILTER не применяет \_ \_ \_ \_ атрибуты индекса \_ и инициализация IFilter не \_ применяют \_ другие \_ атрибуты, указанные в записи flags, а если *cAttributes* — 0, то **IFILTER** выдаст только фрагменты с идентификатором PID `0x13` и соответствующим \_ \_ содержимому PID STG.</span><span class="sxs-lookup"><span data-stu-id="2ccac-292">For example, if neither IFILTER\_INIT\_APPLY\_INDEX\_ATTRIBUTES nor IFILTER\_INIT\_APPLY\_OTHER\_ATTRIBUTES were specified in the Flags entry and if *cAttributes* were 0, then **IFilter** would emit only chunks with a PID of `0x13` and corresponding to PID\_STG\_CONTENTS.</span></span>

### <a name="sample-dump-file"></a><span data-ttu-id="2ccac-293">Пример файла дампа</span><span class="sxs-lookup"><span data-stu-id="2ccac-293">Sample Dump File</span></span>

<span data-ttu-id="2ccac-294">По запросу программа Ifilttst.exe может создать дамп, содержащий фрагменты, которые он находит, и их содержимое.</span><span class="sxs-lookup"><span data-stu-id="2ccac-294">Upon request, the Ifilttst.exe program can produce a dump containing the chunks it finds and their content.</span></span> <span data-ttu-id="2ccac-295">Следующий пример является выдержкой из такого файла дампа.</span><span class="sxs-lookup"><span data-stu-id="2ccac-295">The following example is an excerpt from such a dump file.</span></span>

```
                1. Chunk ID: ........... 2
                2. Chunk Break Type: ... END OF SENTENCE
                3. Chunk State: ........ TEXT
                4. Chunk Locale: ....... 0x411
                5. Chunk Source ID: .... 2
                6. Chunk Start Source .. 0x0
                7. Chunk Length Source . 0x0
                8. GUID ................ b725f130-47ef-101a-a5f1-02608c9eebac
                9. Property ID ......... 0x13

                10. This is a HTML IFilter test page

                11. Chunk ID: ........... 3
                12. Chunk Break Type: ... END OF SENTENCE
                13. Chunk State: ........ TEXT
                14. Chunk Locale: ....... 0x411
                15. Chunk Source ID: .... 2
                16. Chunk Start Source .. 0x0
                17. Chunk Length Source . 0x0
                18. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                19. Property ID ......... 0x2

                20. This is a HTML IFilter test page

                21. Chunk ID: ........... 4
                22. Chunk Break Type: ... END OF SENTENCE
                23. Chunk State: ........ VALUE
                24. Chunk Locale: ....... 0x411
                25. Chunk Source ID: .... 2
                26. Chunk Start Source .. 0x0
                27. Chunk Length Source . 0x0
                28. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                29. Property ID ......... 0x2

                30. This is an HTML IFilter test page
```

<span data-ttu-id="2ccac-296">Первые девять строк описывают текущую структуру фрагмента.</span><span class="sxs-lookup"><span data-stu-id="2ccac-296">The first nine lines describe the current chunk structure.</span></span> <span data-ttu-id="2ccac-297">Идентификатор GUID и идентификатор процесса соответствуют \_ содержимому псгуид Storage/PID \_ STG \_ .</span><span class="sxs-lookup"><span data-stu-id="2ccac-297">The GUID and the PID correspond to PSGUID\_STORAGE / PID\_STG\_CONTENTS.</span></span> <span data-ttu-id="2ccac-298">Это блок, содержащий обычный текст.</span><span class="sxs-lookup"><span data-stu-id="2ccac-298">This is a chunk containing plain text.</span></span> <span data-ttu-id="2ccac-299">Текст находится в следующей структуре блоков:</span><span class="sxs-lookup"><span data-stu-id="2ccac-299">The text is in the following chunk structure:</span></span>

```
10. This is an HTML IFilter test page
```

<span data-ttu-id="2ccac-300">Следующий фрагмент кода, начиная с строки 11, имеет другой GUID, соответствующий `HTML IFilter` , и другой идентификатор процесса, соответствующий HTML href.</span><span class="sxs-lookup"><span data-stu-id="2ccac-300">The next chunk, starting at line 11, has a different GUID, corresponding to the `HTML IFilter`, and a different PID, corresponding to an HTML HREF.</span></span> <span data-ttu-id="2ccac-301">Это внутреннее свойство типа значения, экспортируемое `HTML IFilter` .</span><span class="sxs-lookup"><span data-stu-id="2ccac-301">This is an internal value-type property, exported by the `HTML IFilter`.</span></span>

<span data-ttu-id="2ccac-302">Следующий фрагмент кода, начинающийся в строке 21, имеет тот же идентификатор GUID и идентификатор процесса, но его состояние блока — `VALUE` вместо `TEXT` .</span><span class="sxs-lookup"><span data-stu-id="2ccac-302">The next chunk, starting at line 21, has the same GUID and PID, but its chunk state is `VALUE` instead of `TEXT`.</span></span> <span data-ttu-id="2ccac-303">Обратите внимание, что текст в этих двух последних фрагментах такой же, как и для первого фрагмента.</span><span class="sxs-lookup"><span data-stu-id="2ccac-303">Note that the text in these last two chunks is the same as for the first chunk.</span></span> <span data-ttu-id="2ccac-304">Но поскольку [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) предназначен для трех атрибутов (обычный текст, HTML href в качестве текста и HTML href как значение) для применения к этой фразе, результаты выдаются в трех отдельных блоках.</span><span class="sxs-lookup"><span data-stu-id="2ccac-304">But because the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is designed for three attributes (plain text, HTML HREF as text, and HTML HREF as a value) to be applied to this phrase, the results are emitted in three separate chunks.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ccac-305">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2ccac-305">Additional Resources</span></span>

- <span data-ttu-id="2ccac-306">Пример кода [ифилтерсампле](-search-sample-ifiltersample.md) , доступный на [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), демонстрирует создание базового класса IFilter для реализации интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="2ccac-306">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="2ccac-307">Общие сведения о процессе индексирования см. [в разделе процесс индексирования](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2ccac-307">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="2ccac-308">Общие сведения о типах файлов см. в разделе [типы файлов](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="2ccac-308">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="2ccac-309">Сведения о запросе атрибутов сопоставления файлов для типа файлов см. в разделе [перцеиведтипес, системфилеассоЦиатионс и регистрация приложения](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2ccac-309">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ccac-310">См. также</span><span class="sxs-lookup"><span data-stu-id="2ccac-310">Related topics</span></span>

[<span data-ttu-id="2ccac-311">Разработка обработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="2ccac-311">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="2ccac-312">О обработчиках фильтров в поиске Windows</span><span class="sxs-lookup"><span data-stu-id="2ccac-312">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="2ccac-313">Рекомендации по созданию обработчиков фильтров в поиске Windows</span><span class="sxs-lookup"><span data-stu-id="2ccac-313">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="2ccac-314">Возвращение свойств из обработчика фильтра</span><span class="sxs-lookup"><span data-stu-id="2ccac-314">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="2ccac-315">Обработчики фильтров, поставляемые с Windows</span><span class="sxs-lookup"><span data-stu-id="2ccac-315">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)

[<span data-ttu-id="2ccac-316">Реализация обработчиков фильтров в поиске Windows</span><span class="sxs-lookup"><span data-stu-id="2ccac-316">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="2ccac-317">Регистрация обработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="2ccac-317">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
