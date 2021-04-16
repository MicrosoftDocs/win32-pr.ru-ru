---
title: Средство компилятора веб-служб
description: Для поддержки модели службы wsutil.exe создает заголовок для использования на стороне клиента и службы. Он создает прокси-файл C для стороны клиента и файл заглушки C для службы, если это необходимо.
ms.assetid: 1c73297d-0d3d-421c-9e19-44a6012a5c65
keywords:
- Веб-службы средства компилятора веб-служб для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9931f228a36832fc83d84d584a151de41f5868d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104414208"
---
# <a name="web-service-compiler-tool"></a><span data-ttu-id="7b396-107">Средство компилятора веб-служб</span><span class="sxs-lookup"><span data-stu-id="7b396-107">Web Service Compiler Tool</span></span>

<span data-ttu-id="7b396-108">Для поддержки модели службы wsutil.exe создает заголовок для использования на стороне клиента и службы.</span><span class="sxs-lookup"><span data-stu-id="7b396-108">To support service model, wsutil.exe generates header to be used in both client and service side.</span></span> <span data-ttu-id="7b396-109">Он создает прокси-файл C для стороны клиента и файл заглушки C для службы, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="7b396-109">It generates C proxy file for client side, and C stub file for service side, as needed.</span></span>


<span data-ttu-id="7b396-110">Для поддержки [сериализации](serialization.md)компилятор создает заголовки для описаний элементов для определений глобальных элементов и все сведения об определении типа в прокси-файле, используемые ядром сериализации.</span><span class="sxs-lookup"><span data-stu-id="7b396-110">To support [serialization](serialization.md), the compiler generates headers for element descriptions for global element definitions, and all type definition information in proxy file to be consumed by the serialization engine.</span></span>

<span data-ttu-id="7b396-111">Использование</span><span class="sxs-lookup"><span data-stu-id="7b396-111">Usage</span></span>

<span data-ttu-id="7b396-112">**WsUtil.exe \[ Параметры командной строки для \[ переключения параметров \] :\]<filename>**</span><span class="sxs-lookup"><span data-stu-id="7b396-112">**WsUtil.exe \[command-line-switches \[switch-options\]:\]<filename>**</span></span>

<span data-ttu-id="7b396-113">параметры командной строки</span><span class="sxs-lookup"><span data-stu-id="7b396-113">command-line-switches</span></span>

<span data-ttu-id="7b396-114">Указывает WsUtil.exe параметров компилятора.</span><span class="sxs-lookup"><span data-stu-id="7b396-114">Specifies WsUtil.exe compiler options.</span></span> <span data-ttu-id="7b396-115">Параметры могут использоваться в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="7b396-115">Switches can appear in any order.</span></span> <span data-ttu-id="7b396-116">Тире ("-") и косая черта ("/") считаются одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="7b396-116">Dash ('-') and slash ('/') are treated as the same.</span></span>

<span data-ttu-id="7b396-117">Список параметров командной строки</span><span class="sxs-lookup"><span data-stu-id="7b396-117">List of command line options</span></span>

-   <span data-ttu-id="7b396-118">@filename Указывает, что входной файл должен обрабатываться как файл ответов.</span><span class="sxs-lookup"><span data-stu-id="7b396-118">@filename Specifies that the input file should be treated as a response file.</span></span> <span data-ttu-id="7b396-119">Этот параметр можно использовать несколько раз в любом месте списка аргументов.</span><span class="sxs-lookup"><span data-stu-id="7b396-119">This option can be used multiple times, in any places in the argument list.</span></span>
-   <span data-ttu-id="7b396-120">/всдл: <filename> : <необязательный \_ URL-адрес> указывает, что входной файл должен обрабатываться как WSDL-файл.</span><span class="sxs-lookup"><span data-stu-id="7b396-120">/wsdl:<filename>:<optional\_url> Specifies that the input file should be treated as a wsdl file.</span></span> <span data-ttu-id="7b396-121">Допускается использование нескольких входных данных WSDL и обработка всех указанных WSDL-файлов.</span><span class="sxs-lookup"><span data-stu-id="7b396-121">Multiple wsdl inputs are allowed and all specified wsdl files are processed.</span></span> <span data-ttu-id="7b396-122">Необязательный \_ URL-адрес указывает расположение, из которого были получены метаданные.</span><span class="sxs-lookup"><span data-stu-id="7b396-122">The optional\_url specifies the location where the metadata was retrieved from.</span></span> <span data-ttu-id="7b396-123">Если необязательный \_ URL-адрес не указан, всутил внутренним образом создает уникальный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="7b396-123">If no optional\_url is specified, Wsutil generates a unique url internally.</span></span> <span data-ttu-id="7b396-124">См. также [Поддержка политик](policy-support.md).</span><span class="sxs-lookup"><span data-stu-id="7b396-124">See also [Policy Support](policy-support.md).</span></span>
-   <span data-ttu-id="7b396-125">/КССД: <filename> указывает, что входное имя файла должно рассматриваться как файл схемы.</span><span class="sxs-lookup"><span data-stu-id="7b396-125">/xsd:<filename> Specifies that the input filename should be treated as a schema file.</span></span> <span data-ttu-id="7b396-126">Разрешено несколько входных XSD-файлов, и все указанные файлы схемы обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="7b396-126">Multiple xsd inputs are allowed and all specified schema files are processed.</span></span>
-   <span data-ttu-id="7b396-127">/ВСП: <filename> : <необязательный \_ URL-адрес> указывает, что входное имя файла должно рассматриваться как метаданные политики.</span><span class="sxs-lookup"><span data-stu-id="7b396-127">/wsp:<filename>:<optional\_url> Specifies that the input filename should be treated as policy metadata.</span></span> <span data-ttu-id="7b396-128">Разрешено несколько входных файлов WSP, и все указанные файлы политики обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="7b396-128">Multiple wsp inputs are allowed and all specified policy files are processed.</span></span> <span data-ttu-id="7b396-129">Необязательный \_ URL-адрес указывает расположение, из которого были получены метаданные.</span><span class="sxs-lookup"><span data-stu-id="7b396-129">The optional\_url specifies the location where the metadata was retrieved from.</span></span> <span data-ttu-id="7b396-130">Если необязательный \_ URL-адрес не указан, всутил внутренним образом создает уникальный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="7b396-130">If no optional\_url is specified, Wsutil generates a unique url internally.</span></span> <span data-ttu-id="7b396-131">Файлы политики игнорируются, если указан флаг/нополици.</span><span class="sxs-lookup"><span data-stu-id="7b396-131">Policy files are ignored if /nopolicy flag is specified.</span></span> <span data-ttu-id="7b396-132">См. также [Поддержка политик](policy-support.md).</span><span class="sxs-lookup"><span data-stu-id="7b396-132">See also [Policy Support](policy-support.md).</span></span>
-   <span data-ttu-id="7b396-133">/нополици отключить обработку политики.</span><span class="sxs-lookup"><span data-stu-id="7b396-133">/nopolicy Disable policy processing.</span></span>
-   <span data-ttu-id="7b396-134">/out: <dirname> указывает имя каталога для выходных файлов</span><span class="sxs-lookup"><span data-stu-id="7b396-134">/out:<dirname> Specifies directory name for output files</span></span>
-   <span data-ttu-id="7b396-135">/ноклиент не создают заглушку на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="7b396-135">/noclient Do not generate the client side stub.</span></span>
-   <span data-ttu-id="7b396-136">/noservice не создают заглушку на стороне службы.</span><span class="sxs-lookup"><span data-stu-id="7b396-136">/noservice Do not generate the service side stub.</span></span>
-   <span data-ttu-id="7b396-137">/префикс: <string> начало указанной строки для всех созданных идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="7b396-137">/prefix:<string> Prepend specified string to all generated identifiers.</span></span>
-   <span data-ttu-id="7b396-138">/фуллнаме в начале нормализованного имени файла для созданных идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="7b396-138">/fullname Prepend normalized filename to generated identifiers.</span></span> <span data-ttu-id="7b396-139">По умолчанию только имя, указанное в атрибуте "Name", будет использоваться для создания идентификаторов для связанных описаний.</span><span class="sxs-lookup"><span data-stu-id="7b396-139">By default only name specified in "name" attribute will be used to generate identifiers for related descriptions.</span></span>
-   <span data-ttu-id="7b396-140">/стринг: <WS \_ string>\|<WCHAR \*> по умолчанию всутил создает WCHAR \* для XSD: String Type.</span><span class="sxs-lookup"><span data-stu-id="7b396-140">/string:<WS\_STRING>\|<WCHAR\*> By default, wsutil generates WCHAR\* for xsd:string type.</span></span> <span data-ttu-id="7b396-141">Приложение может использовать этот флаг для перезаписи этого поведения и создает строку WS \_ для XSD: Type.</span><span class="sxs-lookup"><span data-stu-id="7b396-141">Application can use this flag to overwrite that behavior, and generates WS\_STRING for xsd:type instead.</span></span>
-   <span data-ttu-id="7b396-142">/help Отображение справочного сообщения</span><span class="sxs-lookup"><span data-stu-id="7b396-142">/help Display help message</span></span>
-   <span data-ttu-id="7b396-143">/?</span><span class="sxs-lookup"><span data-stu-id="7b396-143">/?</span></span> <span data-ttu-id="7b396-144">То же, что и/Help</span><span class="sxs-lookup"><span data-stu-id="7b396-144">Same as /help</span></span>
-   <span data-ttu-id="7b396-145">Параметры обработки ошибок/w: x.</span><span class="sxs-lookup"><span data-stu-id="7b396-145">/W:x Error handling options.</span></span> <span data-ttu-id="7b396-146">Может быть W:0-W: 4 \| WX</span><span class="sxs-lookup"><span data-stu-id="7b396-146">Could be W:0-W:4 \| WX</span></span>
-   <span data-ttu-id="7b396-147">/nologo не создают сведения о компиляторе для вывода на консоль.</span><span class="sxs-lookup"><span data-stu-id="7b396-147">/nologo Do not generate compiler specific information on console output.</span></span>
-   <span data-ttu-id="7b396-148">/ностамп не создают специфические для компилятора сведения о созданных файлах.</span><span class="sxs-lookup"><span data-stu-id="7b396-148">/nostamp Do not generate compiler specific information on generated files.</span></span>

<span data-ttu-id="7b396-149">По умолчанию компилятор создает следующие файлы для WSDL-файла или WSDL, возвращаемые из обмена метаданными:</span><span class="sxs-lookup"><span data-stu-id="7b396-149">By default, the compiler generates the following files for WSDL file, or WSDL returned from metadata exchange:</span></span>

-   <span data-ttu-id="7b396-150">Прокси клиента ({inputfilename}. c)</span><span class="sxs-lookup"><span data-stu-id="7b396-150">Client proxy ({inputfilename}.c)</span></span>
-   <span data-ttu-id="7b396-151">Заглушка службы ({inputfilename}. c)</span><span class="sxs-lookup"><span data-stu-id="7b396-151">Service Stub ({inputfilename}.c)</span></span>
-   <span data-ttu-id="7b396-152">Заголовочный файл ({inputfilename}. h)</span><span class="sxs-lookup"><span data-stu-id="7b396-152">Header file ({inputfilename}.h)</span></span>

    <span data-ttu-id="7b396-153">Корневым элементом созданного имени файла является имя входного файла.</span><span class="sxs-lookup"><span data-stu-id="7b396-153">The root of the generated filename is the input file name.</span></span> <span data-ttu-id="7b396-154">Исходные расширения входных файлов сохраняются, чтобы предотвратить конфликт имен файлов для создаваемых файлов.</span><span class="sxs-lookup"><span data-stu-id="7b396-154">Original input file extensions are preserved to prevent file name collision for generated files.</span></span> <span data-ttu-id="7b396-155">По умолчанию клиент и заглушки службы создаются в одном файле с кодом заглушки службы, созданным после кода прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="7b396-155">By default client and service stubs are generated in the same file, with service stub code generated after the proxy code.</span></span>

    <span data-ttu-id="7b396-156">По умолчанию компилятор создает следующие файлы для XSD-файла для схемы, возвращаемой из обмена метаданными:</span><span class="sxs-lookup"><span data-stu-id="7b396-156">By default, the compiler generates the following files for a XSD file for schema returned from metadata exchange:</span></span>

-   <span data-ttu-id="7b396-157">описания сериализации ({inputfilename}. c)</span><span class="sxs-lookup"><span data-stu-id="7b396-157">serialization descriptions ({inputfilename}.c)</span></span>
-   <span data-ttu-id="7b396-158">Заголовочный файл ({inputfilename}. h)</span><span class="sxs-lookup"><span data-stu-id="7b396-158">Header file ({inputfilename}.h)</span></span>

    <span data-ttu-id="7b396-159">Корневым именем файла является имя службы.</span><span class="sxs-lookup"><span data-stu-id="7b396-159">The root of the filename is the service name.</span></span>

<span data-ttu-id="7b396-160">Wsutil.exe создает раздел "метка" в начале всех созданных файлов, указывая параметр компилятора, версию средства, параметр командной строки и т. д. Этот раздел можно отключить с помощью параметра/ностамп, чтобы избежать шума при сравнении созданных файлов.</span><span class="sxs-lookup"><span data-stu-id="7b396-160">Wsutil.exe generates a "stamp" section at the beginning of all the generated files, indicating the compiler option, tool version, command line option applicable, etc. This section can be turned off by using /nostamp option to avoid noise with comparing generated files.</span></span>

<span data-ttu-id="7b396-161">Всутил не поддерживает скачивание метаданных</span><span class="sxs-lookup"><span data-stu-id="7b396-161">Wsutil does not support downloading metadata</span></span>

<span data-ttu-id="7b396-162">Компилятор всутил работает только из локального файла метаданных.</span><span class="sxs-lookup"><span data-stu-id="7b396-162">Wsutil compiler works from local metadata file only.</span></span> <span data-ttu-id="7b396-163">Средство не поддерживает скачивание метаданных из работающих веб-служб.</span><span class="sxs-lookup"><span data-stu-id="7b396-163">The tool does not support downloading metadata from running web services.</span></span> <span data-ttu-id="7b396-164">Разработчики могут использовать другие поддерживаемые средства WebService, такие как Svcutil, для загрузки метаданных на локальный компьютер, проверки сохраненных файлов и передачи этих файлов в wsutil.exe для компиляции.</span><span class="sxs-lookup"><span data-stu-id="7b396-164">Developers can use other supported webservice tools, like svcutil, to download metadata to local machine, inspect the saved files, and pass those files to wsutil.exe for compilation.</span></span>

<span data-ttu-id="7b396-165">Поддержка нескольких входных и выходных файлов</span><span class="sxs-lookup"><span data-stu-id="7b396-165">Multiple input/output file support</span></span>

<span data-ttu-id="7b396-166">WSDL и схема XML позволяют включать и импортировать определения из других пространств имен, указанных в других расположениях и файлах.</span><span class="sxs-lookup"><span data-stu-id="7b396-166">WSDL and XML schema allows including/importing definitions from other name spaces specified in other location/files.</span></span> <span data-ttu-id="7b396-167">Всутил поддерживает несколько входных данных схемы/WSDL/Policy и создают один набор заглушек или заголовка для каждого входного файла.</span><span class="sxs-lookup"><span data-stu-id="7b396-167">Wsutil supports multiple schema/wsdl/policy input, and generate one set of stub/header for each input files.</span></span> <span data-ttu-id="7b396-168">Всутил не соответствует инструкциям include и Import.</span><span class="sxs-lookup"><span data-stu-id="7b396-168">Wsutil does not follow through the include and import statements.</span></span> <span data-ttu-id="7b396-169">Вместо этого приложение должно передавать файлы, содержащие все необходимые пространства имен, всутил таким, что средство может разрешать все зависимости во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="7b396-169">Instead, application should pass in files containing all necessary namespaces to wsutil such that the tool can resolve all dependencies during compilation.</span></span>

<span data-ttu-id="7b396-170">**WsUtil.exe/КССД: стокккуоте. xsd/всдл: стокккуоте. WSDL/всдл: stockquoteservice. WSDL**</span><span class="sxs-lookup"><span data-stu-id="7b396-170">**WsUtil.exe /xsd:stockquote.xsd /wsdl:stockquote.wsdl /wsdl:stockquoteservice.wsdl**</span></span>

<span data-ttu-id="7b396-171">всутил создает три набора выходных файлов:</span><span class="sxs-lookup"><span data-stu-id="7b396-171">wsutil generates three sets of output files:</span></span>

-   <span data-ttu-id="7b396-172">стокккуоте. xsd. c стокккуоте. xsd. h</span><span class="sxs-lookup"><span data-stu-id="7b396-172">stockquote.xsd.c stockquote.xsd.h</span></span>
-   <span data-ttu-id="7b396-173">стокккуоте. WSDL. c стокккуоте. WSDL. h</span><span class="sxs-lookup"><span data-stu-id="7b396-173">stockquote.wsdl.c stockquote.wsdl.h</span></span>
-   <span data-ttu-id="7b396-174">stockquoteservice. WSDL. h стокккуотесервицес. WSDL. c</span><span class="sxs-lookup"><span data-stu-id="7b396-174">stockquoteservice.wsdl.h stockquoteservices.wsdl.c</span></span>

<span data-ttu-id="7b396-175">Формат выходных файлов</span><span class="sxs-lookup"><span data-stu-id="7b396-175">Output file format</span></span>

<span data-ttu-id="7b396-176">Для каждого выходного файла всутил создает внешние доступные определения в файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="7b396-176">For each output file, wsutil generates externally available definitions in the header file.</span></span> <span data-ttu-id="7b396-177">В отличие от определений структуры C и прототипов функций-заглушек, все остальные определения, связанные с Web Services, инкапсулируются в глобальной структуре с нормализованным именем файла.</span><span class="sxs-lookup"><span data-stu-id="7b396-177">Other than C structure definitions and stub function prototypes, all the other web services related definitions are encapsulated in a global structure named with normalized filename.</span></span>

``` syntax
typedef struct _stockquote_wsdl {
  struct {
  ... // list of WS_STRUCT_DESCRIPTION for all global complex types.
  } globalTypes;
  struct {
  ... // WS_ELEMENT_DESCRIPTION for all global elements.
  } globalElements;
  struct {
  ...
  } messages;
  struct {
  ...
  } contracts;
} _stockquote_wsdl;

EXTERN_C _stockquote_wsdl stockquote_wsdl;
```

<span data-ttu-id="7b396-178">Обратите внимание, что для глобальной структуры созданы не все поля.</span><span class="sxs-lookup"><span data-stu-id="7b396-178">Notice that not all the fields are generated for the global structure.</span></span> <span data-ttu-id="7b396-179">Поле верхнего уровня создается только в том случае, если связанные определения указаны во входном файле.</span><span class="sxs-lookup"><span data-stu-id="7b396-179">A top level field is generated only when the related definitions are specified in the input file.</span></span> <span data-ttu-id="7b396-180">Например, для XSD-файлов не создаются поля Message, Operations и Contracts.</span><span class="sxs-lookup"><span data-stu-id="7b396-180">For example, no message, operations, and contracts fields are generated for xsd files.</span></span>

<span data-ttu-id="7b396-181">Уровни предупреждений и уровень ошибок</span><span class="sxs-lookup"><span data-stu-id="7b396-181">Warning Levels and error level</span></span>

<span data-ttu-id="7b396-182">Как и компилятор C, WsUtil.exe поддерживает четыре уровня предупреждений и один уровень ошибки:</span><span class="sxs-lookup"><span data-stu-id="7b396-182">Similar to C compiler, WsUtil.exe supports four warning levels and one error level:</span></span>

-   <span data-ttu-id="7b396-183">WsUtil.exe создает ошибки с неустранимыми сбоями, такими как недопустимый WSDL-файл, недопустимые параметры компилятора и т. д.</span><span class="sxs-lookup"><span data-stu-id="7b396-183">WsUtil.exe generates errors with unrecoverable failures, like invalid wsdl file, invalid compiler options etc.</span></span>
-   <span data-ttu-id="7b396-184">Всутил создает предупреждения W1 с серьезными устранимыми проблемами.</span><span class="sxs-lookup"><span data-stu-id="7b396-184">WsUtil generates W1 warnings with serious recoverable issues.</span></span> <span data-ttu-id="7b396-185">Компилятор может продолжить работать, но пользователь должен знать о возникшей ошибке.</span><span class="sxs-lookup"><span data-stu-id="7b396-185">The compiler can go on but user should be aware of the issue.</span></span> <span data-ttu-id="7b396-186">Например, предупреждение W1 будет создано при наличии неподдерживаемых атрибутов, например некоторых аспектов WSDL, в WSDL, которые не влияют на создание кода.</span><span class="sxs-lookup"><span data-stu-id="7b396-186">For example, a W1 warning will be generated if there are unsupported attributes, like some WSDL facets, in wsdl that does not affect code generation.</span></span>
-   <span data-ttu-id="7b396-187">Всутил создает предупреждения W2 с менее серьезными проблемами.</span><span class="sxs-lookup"><span data-stu-id="7b396-187">WsUtil generates W2 warnings with less serious problems.</span></span> <span data-ttu-id="7b396-188">Нет потерь функциональности, но разработчику приложения может быть необходимо иметь представление о том, что.</span><span class="sxs-lookup"><span data-stu-id="7b396-188">There is no lost of functionality, but application developer might want to know that.</span></span> <span data-ttu-id="7b396-189">Подобно поведениям, которые могут отличаться от других платформ.</span><span class="sxs-lookup"><span data-stu-id="7b396-189">Like behaviors that might be different from other platforms.</span></span>
-   <span data-ttu-id="7b396-190">Всутил создает предупреждения W3 с минимальным влиянием на созданный код.</span><span class="sxs-lookup"><span data-stu-id="7b396-190">WsUtil generates W3 warnings with minimal impact on generated code.</span></span> <span data-ttu-id="7b396-191">Например, wsutil.exe создает предупреждение W3, если Нормализованная строка отличается от исходной строки.</span><span class="sxs-lookup"><span data-stu-id="7b396-191">For example, wsutil.exe generates a W3 warning when normalized string is different from original string.</span></span>
-   <span data-ttu-id="7b396-192">Предупреждение W4 больше похоже на "информационные" предупреждения, а Всутил выдает ошибку W4 в таких случаях, как пропуск атрибута документации в WSDL.</span><span class="sxs-lookup"><span data-stu-id="7b396-192">W4 warning is more like "informational" warnings, and WsUtil issue W4 in cases like ignoring documentation attribute in WSDL.</span></span>
-   <span data-ttu-id="7b396-193">WX указывает компилятору обрабатывать предупреждение как ошибку.</span><span class="sxs-lookup"><span data-stu-id="7b396-193">WX indicates the compiler treats warning as error.</span></span> <span data-ttu-id="7b396-194">Например, всутил создает ошибку для всех предупреждений W1, если указан параметр/W: 1/WX.</span><span class="sxs-lookup"><span data-stu-id="7b396-194">For example, wsutil generates error for all W1 warnings if /W:1 /WX is specified.</span></span>

<span data-ttu-id="7b396-195">/W: {N} укажите, какой уровень предупреждений должен создаваться.</span><span class="sxs-lookup"><span data-stu-id="7b396-195">/W:{N} specify which level of warning message should be generated.</span></span> <span data-ttu-id="7b396-196">/W: 1 означает, что должны быть созданы предупреждения уровня 1 предупреждения, а предупреждения уровня предупреждения 2 и ниже должны быть маскированы и не созданы средством.</span><span class="sxs-lookup"><span data-stu-id="7b396-196">/W:1 means warning level 1 warnings should be generated, and warnings of warning level 2 and below should be masked and not generated by the tool.</span></span>

## <a name="fullname"></a><span data-ttu-id="7b396-197">/фуллнаме</span><span class="sxs-lookup"><span data-stu-id="7b396-197">/fullname</span></span>

<span data-ttu-id="7b396-198">Этот параметр указывает, что WsUtil.exe создает полное имя для идентификаторов, чтобы избежать потенциальных конфликтов имен.</span><span class="sxs-lookup"><span data-stu-id="7b396-198">This option indicates that WsUtil.exe generates full name for identifiers to avoid potential name collision.</span></span> <span data-ttu-id="7b396-199">Например, в примере. XSD есть:</span><span class="sxs-lookup"><span data-stu-id="7b396-199">For example, in example.xsd we have:</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:element name="SimpleStruct">
   <xs:complexType>
    <xs:sequence>
     <xs:element name="a" type="xs:int" />
     <xs:element name="b" type="xs:int" />
    </xs:sequence>
   </xs:complexType>
  </xs:element>
 </wsdl:types>
</wsdl:definitions>
```

<span data-ttu-id="7b396-200">По умолчанию WsUtil.exe создает:</span><span class="sxs-lookup"><span data-stu-id="7b396-200">By default WsUtil.exe generates:</span></span>

``` syntax
typedef struct SimpleStruct {
  int a;
  int b;
};
```

<span data-ttu-id="7b396-201">Но если указан параметр командной строки/фуллнаме, вместо этого WsUtil.exe создает следующее определение структуры:</span><span class="sxs-lookup"><span data-stu-id="7b396-201">But if /fullname command line option is specified, WsUtil.exe generates the following structure definition instead:</span></span>

``` syntax
typedef struct exmaple_xsd_SimpleStruct {
  int a;
  int b;
};
```

## <a name="globalization"></a><span data-ttu-id="7b396-202">Глобализация</span><span class="sxs-lookup"><span data-stu-id="7b396-202">Globalization</span></span>

<span data-ttu-id="7b396-203">Средство не зависит от языка и может быть локализовано на разные языки.</span><span class="sxs-lookup"><span data-stu-id="7b396-203">The tool is language neutral and can be localized to different languages.</span></span> <span data-ttu-id="7b396-204">Все сообщения об ошибках и выходные данные консоли могут быть локализованы.</span><span class="sxs-lookup"><span data-stu-id="7b396-204">All error messages / console output can be localized.</span></span> <span data-ttu-id="7b396-205">Однако параметры командной строки остаются на английском языке.</span><span class="sxs-lookup"><span data-stu-id="7b396-205">However, the command line options remain in English.</span></span>

## <a name="environment-variable"></a><span data-ttu-id="7b396-206">Переменная среды</span><span class="sxs-lookup"><span data-stu-id="7b396-206">Environment Variable</span></span>

<span data-ttu-id="7b396-207">WsUtil.exe не использует переменные среды.</span><span class="sxs-lookup"><span data-stu-id="7b396-207">WsUtil.exe does not use any environment variables.</span></span>

## <a name="platform-independent"></a><span data-ttu-id="7b396-208">Не зависит от платформы</span><span class="sxs-lookup"><span data-stu-id="7b396-208">Platform independent</span></span>

<span data-ttu-id="7b396-209">Выходные файлы от WsUtil.exe не зависят от платформы.</span><span class="sxs-lookup"><span data-stu-id="7b396-209">Output files from WsUtil.exe are platform independent.</span></span> <span data-ttu-id="7b396-210">Код, зависящий от архитектуры, не создается в заглушке. компилятор C позаботится обо всех конкретных архитектурах.</span><span class="sxs-lookup"><span data-stu-id="7b396-210">There is no architecture dependent code generated in the stub; anything architecture specific will be taken care of by the C compiler.</span></span> <span data-ttu-id="7b396-211">Заглушку можно использовать на всех поддерживаемых платформах.</span><span class="sxs-lookup"><span data-stu-id="7b396-211">The stub can be used in all the platforms we support.</span></span>

<span data-ttu-id="7b396-212">Описание выходных данных wsutil.exe можно найти в разделе [Поддержка WSDL](wsdl-support.md) и [поддержка схемы](schema-support.md) .</span><span class="sxs-lookup"><span data-stu-id="7b396-212">Description for wsutil.exe output can be found at [WSDL support](wsdl-support.md) and [Schema support](schema-support.md) part.</span></span>

 

 




