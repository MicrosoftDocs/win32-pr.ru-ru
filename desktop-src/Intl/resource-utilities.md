---
description: В этом разделе описываются две служебные программы, используемые для создания приложений MUI.
ms.assetid: 8ba94001-fc46-41e0-a071-0dc500a20753
title: Служебные программы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550cf283779a57bc5ca35f88d336646b061c3f1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999114"
---
# <a name="resource-utilities"></a><span data-ttu-id="63ee7-103">Служебные программы</span><span class="sxs-lookup"><span data-stu-id="63ee7-103">Resource Utilities</span></span>

<span data-ttu-id="63ee7-104">В этом разделе описываются две служебные программы, используемые для создания приложений MUI.</span><span class="sxs-lookup"><span data-stu-id="63ee7-104">This topic describes two utilities used to build MUI applications.</span></span> <span data-ttu-id="63ee7-105">Хотя МУИРКТ — это средство для многоязыкового интерфейса пользователя, MUI также использует стандартную служебную программу компилятора Windows RC.</span><span class="sxs-lookup"><span data-stu-id="63ee7-105">While MUIRCT is a MUI-specific tool, MUI also makes use of the standard Windows RC Compiler utility.</span></span> <span data-ttu-id="63ee7-106">Инструкции по использованию этих служебных программ приведены в разделе [Локализация ресурсов и создание приложения](localizing-resources-and-building-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="63ee7-106">Instructions for using these utilities are provided in [Localizing Resources and Building the Application](localizing-resources-and-building-the-application.md).</span></span>

## <a name="muirct-utility"></a><span data-ttu-id="63ee7-107">Служебная программа МУИРКТ</span><span class="sxs-lookup"><span data-stu-id="63ee7-107">MUIRCT Utility</span></span>

<span data-ttu-id="63ee7-108">МУИРКТ (Muirct.exe) — это служебная программа командной строки для разделения стандартного исполняемого файла в LN-файл и зависящие от языка файлы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63ee7-108">MUIRCT (Muirct.exe) is a command line utility for splitting a standard executable file into an LN file and language-specific (that is, localizable) resource files.</span></span> <span data-ttu-id="63ee7-109">Каждый из результирующих файлов содержит данные конфигурации ресурсов для сопоставления файлов.</span><span class="sxs-lookup"><span data-stu-id="63ee7-109">Each of the resulting files contains resource configuration data for file association.</span></span> <span data-ttu-id="63ee7-110">МУИРКТ входит в Microsoft Windows SDK для Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="63ee7-110">MUIRCT is included in the Microsoft Windows SDK for Windows Vista.</span></span>

> [!Note]  
> <span data-ttu-id="63ee7-111">Начиная с Windows Vista загрузчик ресурсов Win32 обновляется для загрузки ресурсов из файлов, зависящих от языка, а также из LN-файлов.</span><span class="sxs-lookup"><span data-stu-id="63ee7-111">Starting with Windows Vista, the Win32 resource loader is updated to load resources from language-specific files as well as from LN files.</span></span>

 

### <a name="muirct-usages"></a><span data-ttu-id="63ee7-112">Использование МУИРКТ</span><span class="sxs-lookup"><span data-stu-id="63ee7-112">MUIRCT Usages</span></span>

1.  <span data-ttu-id="63ee7-113">Разделите двоичные файлы на основной двоичный файл и MUI, основываясь на \_ файле конфигурации RC.</span><span class="sxs-lookup"><span data-stu-id="63ee7-113">Split binary into main binary and mui file based on rc\_config file.</span></span>

    `Muirct -q rc_config [-c checksum_file [-b LangID]] [-x LangID] [-g LangId]     [-f] [-m] [-v level] source_file [output_LN_file] [output_MUI_file]`

2.  <span data-ttu-id="63ee7-114">Извлеките контрольную сумму из файла контрольной суммы \_ и вставьте ее в выходной \_ файл.</span><span class="sxs-lookup"><span data-stu-id="63ee7-114">Extract checksum from checksum\_file and insert it in output\_file.</span></span>

    `Muirct -c checksum_file [-b LangID] -e output_file`

3.  <span data-ttu-id="63ee7-115">Рассчитайте контрольную сумму на основе файла контрольной суммы \_ и вставьте ее в выходной \_ файл.</span><span class="sxs-lookup"><span data-stu-id="63ee7-115">Calculate checksum based on checksum\_file and insert it in output\_file.</span></span>

    `Muirct  -c checksum_file [-b LangID] -q rc_config  -z output_file`

4.  <span data-ttu-id="63ee7-116">Дамп содержимого данных конфигурации ресурсов из входного \_ файла.</span><span class="sxs-lookup"><span data-stu-id="63ee7-116">Dump resource configuration data contents from input\_file.</span></span>

    `Muirct -d input_file`

### <a name="muirct-syntax"></a><span data-ttu-id="63ee7-117">Синтаксис МУИРКТ</span><span class="sxs-lookup"><span data-stu-id="63ee7-117">MUIRCT Syntax</span></span>

<span data-ttu-id="63ee7-118">МУИРКТ может осуществлять направление от параметров командной строки и (или) из файла конфигурации ресурса, указанного с помощью параметра-q.</span><span class="sxs-lookup"><span data-stu-id="63ee7-118">MUIRCT can take direction from command line switches and/or from a resource configuration file, specified using the -q switch.</span></span>


```C++
muirct [-h|-?] [ -c checksum_file] [-b langid]  ]
     [-g langid] [-q resource configuration file<RCF>] [-v level] [-x langid]
     [-e output_file]  [-z output_file] [-f] [-d MUI'ized file] [-m file_version]

source_filename [language_neutral_filename] [mui_filename]
```



<span data-ttu-id="63ee7-119">**Параметры и аргументы**</span><span class="sxs-lookup"><span data-stu-id="63ee7-119">**Switches and Arguments**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63ee7-120">-h |-?</span><span class="sxs-lookup"><span data-stu-id="63ee7-120">-h|-?</span></span></td>
<td><span data-ttu-id="63ee7-121">Отображает экран справки.</span><span class="sxs-lookup"><span data-stu-id="63ee7-121">Shows help screen.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ee7-122">-c</span><span class="sxs-lookup"><span data-stu-id="63ee7-122">-c</span></span></td>
<td><span data-ttu-id="63ee7-123">Задает входное checksum_file, из которого необходимо извлечь или вычислить контрольную сумму ресурса.</span><span class="sxs-lookup"><span data-stu-id="63ee7-123">Specifies the input checksum_file from which to extract or calculate the resource checksum.</span></span> <span data-ttu-id="63ee7-124">Checksum_file должен быть двоичным файлом Win32, содержащим локализуемые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="63ee7-124">Checksum_file must be a Win32 binary file containing localizable resources.</span></span> <span data-ttu-id="63ee7-125">Если checksum_file содержит ресурсы для нескольких языков, необходимо использовать параметр-b, чтобы указать, какие из них следует использовать в противном случае, МУИРКТ завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="63ee7-125">If checksum_file contains resources for more than one language, the -b switch must be used to specify which of these should be used otherwise MUIRCT fails.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ee7-126">-b</span><span class="sxs-lookup"><span data-stu-id="63ee7-126">-b</span></span></td>
<td><span data-ttu-id="63ee7-127">Указывает язык, используемый, когда checksum_file, заданный с помощью-c, содержит ресурсы на нескольких языках.</span><span class="sxs-lookup"><span data-stu-id="63ee7-127">Specifies the language to be used when the checksum_file specified with -c contains resources in multiple languages.</span></span> <span data-ttu-id="63ee7-128">Этот параметр можно использовать только совместно с параметром-c.</span><span class="sxs-lookup"><span data-stu-id="63ee7-128">This switch can only be used in conjunction with the -c switch.</span></span> <span data-ttu-id="63ee7-129">Идентификатор языка может быть в десятичном или шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="63ee7-129">The language identifier can be in decimal or hexadecimal format.</span></span> <span data-ttu-id="63ee7-130">МУИРКТ завершается ошибкой, если checksum_file содержит ресурсы на нескольких языках, а параметр-b не указан, или если язык, указанный параметром-b, не найден в checksum_file.</span><span class="sxs-lookup"><span data-stu-id="63ee7-130">MUIRCT fails if the checksum_file contains resources in multiple language and the -b is not specified or if the language specified by the -b switch cannot be found in the checksum_file.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ee7-131">-g</span><span class="sxs-lookup"><span data-stu-id="63ee7-131">-g</span></span></td>
<td><span data-ttu-id="63ee7-132">Указывает идентификатор языка, который будет включаться в качестве конечного языка в разделе данных конфигурации ресурсов в LN файле.</span><span class="sxs-lookup"><span data-stu-id="63ee7-132">Specifies the language ID to be included as the ultimate fallback language in the resource configuration data section of the LN file.</span></span> <span data-ttu-id="63ee7-133">Если загрузчику ресурсов не удается загрузить запрошенный MUI-файл из предпочтительных языков пользовательского интерфейса потока, в качестве последней попытки используется конечный язык.</span><span class="sxs-lookup"><span data-stu-id="63ee7-133">If the resource loader fails to load a requested .mui file from the thread preferred UI languages, it uses the ultimate fallback language as its last attempt.</span></span> <span data-ttu-id="63ee7-134">Значение LangID может быть указано в десятичном или шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="63ee7-134">The LangID value can be specified in decimal or hexadecimal format.</span></span> <span data-ttu-id="63ee7-135">Например, Английский (США) может быть указан в параметре-g 0x409 или-g 1033.</span><span class="sxs-lookup"><span data-stu-id="63ee7-135">For example English (United States) can be specified by -g 0x409 or -g 1033.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ee7-136">-Q</span><span class="sxs-lookup"><span data-stu-id="63ee7-136">-q</span></span></td>
<td><span data-ttu-id="63ee7-137">Указывает, что source_file необходимо разбить на output_LN_file и output_MUI_file в соответствии с разметкой файла rc_config.</span><span class="sxs-lookup"><span data-stu-id="63ee7-137">Specifies that the source_file is to be split into the output_LN_file and the output_MUI_file according to the rc_config file layout.</span></span> <span data-ttu-id="63ee7-138">Файл rc_config — это файл в формате XML, указывающий, какие ресурсы будут извлечены в MUI-файл и которые будут оставлены в LN-файле.</span><span class="sxs-lookup"><span data-stu-id="63ee7-138">The rc_config file is an XML formatted file that specifies which resources will be extracted to the .mui file and which will be left in the LN file.</span></span> <span data-ttu-id="63ee7-139">Rc_config может указывать распределение типов ресурсов и отдельных именованных элементов между output_LN_file и output_MUI_file.</span><span class="sxs-lookup"><span data-stu-id="63ee7-139">The rc_config can specify the distribution of resource types and individual named items between the output_LN_file and output_MUI_file.</span></span> <span data-ttu-id="63ee7-140">Source_file должен быть двоичным файлом Win32, который содержит ресурсы на одном языке, иначе МУИРКТ завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="63ee7-140">The source_file must be a Win32 binary that contains resources in a single language otherwise MUIRCT fails.</span></span> <span data-ttu-id="63ee7-141">МУИРКТ не разделяет файл, если он является независимым от языка, который указывается в файле только со значением идентификатора языка 0.</span><span class="sxs-lookup"><span data-stu-id="63ee7-141">MUIRCT does not split the file if it is language neutral which is indicated by having only language ID value 0 in the file.</span></span> <span data-ttu-id="63ee7-142">Output_LN_file и output_mui_file — это имена нейтрального к языку и MUI-файла, в который разбивается source_file.</span><span class="sxs-lookup"><span data-stu-id="63ee7-142">The output_LN_file and output_mui_file are the names of the language neutral and .mui file into which the source_file is split.</span></span> <span data-ttu-id="63ee7-143">Эти имена файлов являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="63ee7-143">These file names are optional.</span></span> <span data-ttu-id="63ee7-144">Если они не указаны, МУИРКТ добавляет расширения. LN и. MUI для source_file.</span><span class="sxs-lookup"><span data-stu-id="63ee7-144">If they are not specified, MUIRCT appends the extensions .ln and .mui to source_file.</span></span> <span data-ttu-id="63ee7-145">Как правило, &quot; расширение. LN следует удалять &quot; перед развертыванием файла.</span><span class="sxs-lookup"><span data-stu-id="63ee7-145">Typically you should remove the &quot;.ln&quot; extension before deploying the file.</span></span> <span data-ttu-id="63ee7-146">МУИРКТ связывает output_LN_file и output_MUI_file, вычисляя контрольную сумму на основе имени source_file и версии файла и вставляет результат в раздел конфигурации ресурсов каждого выходного файла.</span><span class="sxs-lookup"><span data-stu-id="63ee7-146">MUIRCT associates the output_LN_file and output_MUI_file by calculating a checksum based on the source_file name and file version and inserting the result into the resource configuration section of each output file.</span></span> <span data-ttu-id="63ee7-147">При использовании в сочетании с параметром-c параметр-q имеет приоритет.</span><span class="sxs-lookup"><span data-stu-id="63ee7-147">When used in conjunction with the -c switch, the -q switch takes precedence.</span></span> <span data-ttu-id="63ee7-148">Если файл rc_config, указанный с параметром-q, содержит контрольную сумму МУИРКТ игнорирует параметр-c и вставляет значение контрольной суммы из значения, rc_config файл в файлы LN и MUI.</span><span class="sxs-lookup"><span data-stu-id="63ee7-148">If the rc_config file supplied with the -q switch contains a checksum MUIRCT ignores the -c switch and inserts the checksum value from the value, rc_config file into the LN and.mui files.</span></span> <span data-ttu-id="63ee7-149">Если значение контрольной суммы не найдено в rc_config, МУИРКТ вычисляет контрольную сумму ресурса в зависимости от поведения параметра-c.</span><span class="sxs-lookup"><span data-stu-id="63ee7-149">If no checksum value is found in the rc_config, MUIRCT calculates the resource checksum based on the behavior of the -c switch.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ee7-150">-v</span><span class="sxs-lookup"><span data-stu-id="63ee7-150">-v</span></span></td>
<td><span data-ttu-id="63ee7-151">Указывает уровень вербосенесс для ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="63ee7-151">Specifies the level of verboseness for logging.</span></span> <span data-ttu-id="63ee7-152">Укажите 1, чтобы напечатать все основные сообщения об ошибках и результаты операций.</span><span class="sxs-lookup"><span data-stu-id="63ee7-152">Specify 1 to print all basic error messages and operation results.</span></span> <span data-ttu-id="63ee7-153">Укажите значение 2, чтобы также включить сведения о ресурсах (тип, имя, идентификатор языка), включенные в MUI-файл и LN File.</span><span class="sxs-lookup"><span data-stu-id="63ee7-153">Specify 2 to also include the resource information (type, name, language identifier) included in the .mui file and LN file.</span></span> <span data-ttu-id="63ee7-154">Значение по умолчанию —-v 1</span><span class="sxs-lookup"><span data-stu-id="63ee7-154">The default is -v 1</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ee7-155">-X</span><span class="sxs-lookup"><span data-stu-id="63ee7-155">-x</span></span></td>
<td><span data-ttu-id="63ee7-156">Указывает идентификатор языка, с помощью которого МУИРКТ помечает все типы ресурсов, добавленные в раздел Resource файла MUI.</span><span class="sxs-lookup"><span data-stu-id="63ee7-156">Specifies the language ID with which MUIRCT marks all resource types added to the resource section of the .mui file.</span></span> <span data-ttu-id="63ee7-157">Значение LangID может быть указано в десятичном или шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="63ee7-157">The LangID value can be specified in decimal or hexadecimal format.</span></span> <span data-ttu-id="63ee7-158">Например, Английский (США) можно указать с помощью-x 0x409 или-x 1033.</span><span class="sxs-lookup"><span data-stu-id="63ee7-158">For example English (United States) can be specified by -x 0x409 or -x 1033.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ee7-159">-E</span><span class="sxs-lookup"><span data-stu-id="63ee7-159">-e</span></span></td>
<td><span data-ttu-id="63ee7-160">Извлекает контрольную сумму ресурса, содержащуюся в checksum_file, предоставленном с параметром-c, и вставляет ее в указанный output_file.</span><span class="sxs-lookup"><span data-stu-id="63ee7-160">Extracts the resource checksum contained in the checksum_file provided with the -c switch and inserts it in the specified output_file.</span></span> <span data-ttu-id="63ee7-161">Если указан параметр-e, МУИРКТ игнорирует все переключатели, кроме параметра-c.</span><span class="sxs-lookup"><span data-stu-id="63ee7-161">When -e is specified, MUIRCT ignores all switches other than the -c switch.</span></span> <span data-ttu-id="63ee7-162">В этом случае checksum_file должен быть двоичным файлом Win32, содержащим раздел данных конфигурации ресурсов со значением контрольной суммы.</span><span class="sxs-lookup"><span data-stu-id="63ee7-162">In this case the checksum_file must be a Win32 binary file that contains a resource configuration data section with a checksum value.</span></span> <span data-ttu-id="63ee7-163">Output_file должен быть существующим файлом LN или MUI.</span><span class="sxs-lookup"><span data-stu-id="63ee7-163">The output_file must be an existing LN file or .mui file.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ee7-164">-Z</span><span class="sxs-lookup"><span data-stu-id="63ee7-164">-z</span></span></td>
<td><span data-ttu-id="63ee7-165">Вычисляет и вставляет данные контрольной суммы ресурсов в указанный выходной файл.</span><span class="sxs-lookup"><span data-stu-id="63ee7-165">Calculates and inserts resource checksum data in the specified output file.</span></span> <span data-ttu-id="63ee7-166">МУИРКТ базовые вычисления контрольной суммы для входных данных, входящих в параметр-c, и необязательного параметра-b.</span><span class="sxs-lookup"><span data-stu-id="63ee7-166">MUIRCT bases checksum calculation on the input provided with the -c switch, and the optional -b switch.</span></span> <span data-ttu-id="63ee7-167">Если указать выходной файл для параметра-z, который не существует, МУИРКТ завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="63ee7-167">If you specify an output file for the -z switch that does not exist, MUIRCT exits with a failure.</span></span><br/> <span data-ttu-id="63ee7-168">Пример. вычисляет контрольную сумму на основе локализуемых ресурсов в Notepad.exe и вставляет контрольную сумму в выходной файл Notepad2.exe.</span><span class="sxs-lookup"><span data-stu-id="63ee7-168">Example: Calculates the checksum based on localizable resources in Notepad.exe and inserts the checksum into the output file Notepad2.exe.</span></span><br/> <code>muirct -c notepad.exe -q myprog.rcconfig -z notepad2.exe</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ee7-169">-f</span><span class="sxs-lookup"><span data-stu-id="63ee7-169">-f</span></span></td>
<td><span data-ttu-id="63ee7-170">Позволяет создать файл MUI с ресурсом версии, который является единственным локализуемое ресурсом.</span><span class="sxs-lookup"><span data-stu-id="63ee7-170">Enables creating a .mui file with the version resource being the only localizable resource.</span></span> <span data-ttu-id="63ee7-171">По умолчанию МУИРКТ не разрешает это.</span><span class="sxs-lookup"><span data-stu-id="63ee7-171">By default, MUIRCT does not allow this.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ee7-172">-d</span><span class="sxs-lookup"><span data-stu-id="63ee7-172">-d</span></span></td>
<td><span data-ttu-id="63ee7-173">Находит и отображает данные конфигурации внедренных ресурсов в исходном файле.</span><span class="sxs-lookup"><span data-stu-id="63ee7-173">Locates and displays embedded resource configuration data in the source file.</span></span> <span data-ttu-id="63ee7-174">При указании этого параметра МУИРКТ игнорирует все остальные параметры командной строки.</span><span class="sxs-lookup"><span data-stu-id="63ee7-174">When you specify this switch, MUIRCT ignores all other command line options.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ee7-175">-M</span><span class="sxs-lookup"><span data-stu-id="63ee7-175">-m</span></span></td>
<td><span data-ttu-id="63ee7-176">Указывает номер версии, используемый при вычислении контрольной суммы для связывания output_LN_file и output_MUI_file.</span><span class="sxs-lookup"><span data-stu-id="63ee7-176">Specifies the version number to use when calculating the checksum for associating the output_LN_file and output_MUI_file.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ee7-177">source_filename</span><span class="sxs-lookup"><span data-stu-id="63ee7-177">source_filename</span></span></td>
<td><span data-ttu-id="63ee7-178">Имя локализованного двоичного файла исходного кода. подстановочные знаки использовать нельзя.</span><span class="sxs-lookup"><span data-stu-id="63ee7-178">Name of the localized binary source file; wildcards cannot be used.</span></span> <span data-ttu-id="63ee7-179">Этот файл может содержать только ресурсы на одном языке.</span><span class="sxs-lookup"><span data-stu-id="63ee7-179">This file can only contain resources in one language.</span></span> <span data-ttu-id="63ee7-180">Если в файле есть ресурсы на нескольких языках, МУИРКТ завершается ошибкой, если не используется параметр-b.</span><span class="sxs-lookup"><span data-stu-id="63ee7-180">If there are resources in multiple languages in the file, MUIRCT fails, unless the -b switch is used.</span></span> <span data-ttu-id="63ee7-181">Если файл содержит ресурсы с идентификаторами языка, имеющими только значение 0, МУИРКТ не разделяет файл, поскольку идентификатор языка 0 указывает на нейтральный язык.</span><span class="sxs-lookup"><span data-stu-id="63ee7-181">If the file contains resources with language identifiers having value 0 only, MUIRCT does not split the file because a language identifier of 0 indicates a neutral language.</span></span><br/> <span data-ttu-id="63ee7-182">Для параметра-d source_filename — это либо LN-файл, либо файл ресурсов, зависящий от языка, для которого МУИРКТ отображает данные конфигурации ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63ee7-182">For the -d switch, source_filename is either an LN file or a language-specific resource file for which MUIRCT is to display resource configuration data.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ee7-183">language_neutral_filename</span><span class="sxs-lookup"><span data-stu-id="63ee7-183">language_neutral_filename</span></span></td>
<td><span data-ttu-id="63ee7-184">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="63ee7-184">Optional.</span></span> <span data-ttu-id="63ee7-185">Имя LN файла.</span><span class="sxs-lookup"><span data-stu-id="63ee7-185">Name of LN file.</span></span> <span data-ttu-id="63ee7-186">Если не указать имя этого файла, МУИРКТ добавляет второе расширение &quot; . LN &quot; к имени исходного файла для использования в качестве имени файла, не зависящего от языка.</span><span class="sxs-lookup"><span data-stu-id="63ee7-186">If you do not specify the name of this file, MUIRCT appends a second extension &quot;.ln&quot; to the source file name to use as the language-neutral file name.</span></span> <span data-ttu-id="63ee7-187">Как правило, &quot; расширение. LN следует удалять &quot; перед развертыванием файла.</span><span class="sxs-lookup"><span data-stu-id="63ee7-187">Typically you should remove the &quot;.ln&quot; extension before deploying the file.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="63ee7-188">LN File не должен содержать строк или меню.</span><span class="sxs-lookup"><span data-stu-id="63ee7-188">The LN file should not contain strings or menus.</span></span> <span data-ttu-id="63ee7-189">Их следует удалить вручную.</span><span class="sxs-lookup"><span data-stu-id="63ee7-189">You should remove them manually.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ee7-190">mui_filename</span><span class="sxs-lookup"><span data-stu-id="63ee7-190">mui_filename</span></span></td>
<td><span data-ttu-id="63ee7-191">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="63ee7-191">Optional.</span></span> <span data-ttu-id="63ee7-192">Имя файла ресурсов, зависящего от языка.</span><span class="sxs-lookup"><span data-stu-id="63ee7-192">Name of language-specific resource file.</span></span> <span data-ttu-id="63ee7-193">Если имя не указано, МУИРКТ добавляет второе расширение &quot; MUI &quot; к имени исходного файла для использования в качестве имени файла. Как правило, МУИРКТ создает файл ресурсов, зависящий от языка.</span><span class="sxs-lookup"><span data-stu-id="63ee7-193">If you do not specify a name, MUIRCT appends a second extension &quot;.mui&quot; to the source file name to use as the file name.Normally, MUIRCT creates a language-specific resource file.</span></span> <span data-ttu-id="63ee7-194">Однако он не создает файл ресурсов, если выполняется одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="63ee7-194">However, it does not create a resource file if any of the following conditions exist:</span></span><br/>
<ul>
<li><span data-ttu-id="63ee7-195">В исходном двоичном файле нет локализуемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63ee7-195">No localizable resources are in the original binary file.</span></span></li>
<li><span data-ttu-id="63ee7-196">Единственный язык ресурсов, найденный в исходном двоичном файле, — это нейтральный язык.</span><span class="sxs-lookup"><span data-stu-id="63ee7-196">The only resource language found in the original binary file is the neutral language.</span></span></li>
<li><span data-ttu-id="63ee7-197">Исходный двоичный файл содержит ресурсы для более чем одного языка, не считая нейтральный язык.</span><span class="sxs-lookup"><span data-stu-id="63ee7-197">The original binary file has resources for more than one language, not counting the neutral language.</span></span> <span data-ttu-id="63ee7-198">Если двоичный файл содержит ресурсы для двух языков, и один из них является нейтральным языком, программа считает, что файл является одноязычным, и создает файл ресурсов, зависящий от языка, если есть локализуемые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="63ee7-198">If the binary file contains resources for two languages, and one of them is the neutral language, the utility considers the file to be monolingual and creates a language-specific resource file if there are localizable resources.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="muirct-language-output"></a><span data-ttu-id="63ee7-199">Выходные данные языка МУИРКТ</span><span class="sxs-lookup"><span data-stu-id="63ee7-199">MUIRCT Language Output</span></span>

<span data-ttu-id="63ee7-200">МУИРКТ выбирает значение атрибута «Ултиматефаллбакклангуаже» для вставки в данные конфигурации ресурса «LN File» в соответствии со следующим порядком, от наивысшего приоритета к наименьшему:</span><span class="sxs-lookup"><span data-stu-id="63ee7-200">MUIRCT chooses the "UltimateFallbackLanguage" attribute value to insert in the LN file resource configuration data based on the following order, from highest priority to lowest:</span></span>

1.  <span data-ttu-id="63ee7-201">Атрибут "Ултиматефаллбакклангуаже" в исходном файле конфигурации ресурса, если он передан в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="63ee7-201">"UltimateFallbackLanguage" attribute in the source resource configuration file, if one is passed in as input.</span></span>
2.  <span data-ttu-id="63ee7-202">Язык, указанный с помощью параметра-g.</span><span class="sxs-lookup"><span data-stu-id="63ee7-202">The language specified with the -g switch.</span></span>
3.  <span data-ttu-id="63ee7-203">Язык входного файла.</span><span class="sxs-lookup"><span data-stu-id="63ee7-203">Input file language.</span></span>

<span data-ttu-id="63ee7-204">МУИРКТ выбирает значение атрибута "Language" для вставки в данные конфигурации ресурсов MUI в соответствии со следующим порядком:</span><span class="sxs-lookup"><span data-stu-id="63ee7-204">MUIRCT picks the "language" attribute value to insert in the .mui file resource configuration data based on the following order:</span></span>

1.  <span data-ttu-id="63ee7-205">атрибут Language в файле конфигурации исходного ресурса, если он передается в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="63ee7-205">"language" attribute in the source resource configuration file, if one is passed in as input.</span></span>
2.  <span data-ttu-id="63ee7-206">Язык, заданный параметром-x (принудительный язык).</span><span class="sxs-lookup"><span data-stu-id="63ee7-206">The language specified by the -x switch (force language).</span></span>
3.  <span data-ttu-id="63ee7-207">Язык входного файла.</span><span class="sxs-lookup"><span data-stu-id="63ee7-207">Input file language.</span></span>

### <a name="muirct-checksum-handling"></a><span data-ttu-id="63ee7-208">Обработка контрольной суммы МУИРКТ</span><span class="sxs-lookup"><span data-stu-id="63ee7-208">MUIRCT Checksum Handling</span></span>

<span data-ttu-id="63ee7-209">Как правило, операционная система вычисляет контрольную сумму для ресурсов конкретного языка в файле, если не указать контрольную сумму через файл конфигурации ресурса.</span><span class="sxs-lookup"><span data-stu-id="63ee7-209">The operating system normally calculates the checksum over the language-specific resources in a file unless you specify the checksum through a resource configuration file.</span></span> <span data-ttu-id="63ee7-210">Если контрольная сумма одинакова для LN-файла и всех связанных с ними файлов ресурсов, а атрибут Language в конфигурации ресурсов в версии LN и зависит от языка, загрузчик ресурсов может успешно загрузить ресурсы.</span><span class="sxs-lookup"><span data-stu-id="63ee7-210">As long as the checksum is the same for the LN file and all associated language-specific resource files, and the language attribute in the resource configuration in the LN and language dependent match, the resource loader can successfully load resources.</span></span>

<span data-ttu-id="63ee7-211">МУИРКТ поддерживает несколько методов размещения соответствующих контрольных сумм в данных конфигурации ресурсов:</span><span class="sxs-lookup"><span data-stu-id="63ee7-211">MUIRCT supports several methods for placing appropriate checksums in the resource configuration data:</span></span>

1.  <span data-ttu-id="63ee7-212">Создайте исполняемый файл для каждого языка, содержащего как код, так и ресурсы.</span><span class="sxs-lookup"><span data-stu-id="63ee7-212">Build an executable for each language, containing both code and resources.</span></span> <span data-ttu-id="63ee7-213">После этого используйте МУИРКТ, чтобы разделить каждый из этих файлов в LN-файл и файл ресурсов, зависящий от языка.</span><span class="sxs-lookup"><span data-stu-id="63ee7-213">After this, use MUIRCT to split each of these files into an LN file and a language-specific resource file.</span></span> <span data-ttu-id="63ee7-214">МУИРКТ выполняется несколько раз, один раз для создания файла ресурсов для каждого языка.</span><span class="sxs-lookup"><span data-stu-id="63ee7-214">MUIRCT runs multiple times, once to generate a resource file for each language.</span></span> <span data-ttu-id="63ee7-215">Сборку можно выполнить следующими способами.</span><span class="sxs-lookup"><span data-stu-id="63ee7-215">You can perform the build in the following ways:</span></span>
    1.  <span data-ttu-id="63ee7-216">Используйте параметр-q, чтобы указать значение контрольной суммы в файле конфигурации ресурса.</span><span class="sxs-lookup"><span data-stu-id="63ee7-216">Use the -q switch to specify a checksum value in the resource configuration file.</span></span> <span data-ttu-id="63ee7-217">МУИРКТ помещает это значение во все вырабатываемые файлы и зависящие от языка файлы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63ee7-217">MUIRCT places this value in all the LN files and language-specific resource files produced.</span></span> <span data-ttu-id="63ee7-218">Для выбора этого значения необходимо принять стратегию, как описано далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="63ee7-218">You need to adopt a strategy for choosing this value, as described later in this topic.</span></span>
    2.  <span data-ttu-id="63ee7-219">Используйте параметр-c (и, при необходимости, параметр-b), чтобы выбрать один язык с ресурсами, из которых МУИРКТ извлекает контрольную сумму.</span><span class="sxs-lookup"><span data-stu-id="63ee7-219">Use the -c switch (and, optionally, the -b switch) to choose a single language having resources from which MUIRCT extracts the checksum.</span></span>
    3.  <span data-ttu-id="63ee7-220">Используйте параметр-z, чтобы выбрать один язык с ресурсами, из которых МУИРКТ всегда извлекает контрольную сумму.</span><span class="sxs-lookup"><span data-stu-id="63ee7-220">Use the -z switch to choose a single language having resources from which MUIRCT always extracts the checksum.</span></span> <span data-ttu-id="63ee7-221">Примените эту контрольную сумму после сборки файлов с помощью других методов.</span><span class="sxs-lookup"><span data-stu-id="63ee7-221">Apply this checksum after the files have been built using other methods.</span></span>
2.  <span data-ttu-id="63ee7-222">Создайте исполняемый файл, содержащий как код, так и ресурсы для одного языка.</span><span class="sxs-lookup"><span data-stu-id="63ee7-222">Build an executable containing both code and resources for a single language.</span></span> <span data-ttu-id="63ee7-223">После этого используйте МУИРКТ, чтобы разделить ресурсы между LN-файлом и файлом ресурсов, зависящим от языка.</span><span class="sxs-lookup"><span data-stu-id="63ee7-223">After this, use MUIRCT to split the resources between the LN file and the language-specific resource file.</span></span> <span data-ttu-id="63ee7-224">Наконец, используйте средство двоичной локализации для изменения результирующего файла ресурсов для каждого языка.</span><span class="sxs-lookup"><span data-stu-id="63ee7-224">Finally, use a binary localization tool to modify the resulting resource file for each language.</span></span>

<span data-ttu-id="63ee7-225">Наиболее распространенным соглашением для обработки контрольных сумм является базовая контрольная сумма ресурсов на английском (США).</span><span class="sxs-lookup"><span data-stu-id="63ee7-225">The most common convention for checksum handling is to base the checksum on the English (United States) resources.</span></span> <span data-ttu-id="63ee7-226">Вы можете принять другое соглашение, если оно соответствует каждому LN-файлу.</span><span class="sxs-lookup"><span data-stu-id="63ee7-226">You are free to adopt a different convention, as long as it is consistent for each LN file.</span></span> <span data-ttu-id="63ee7-227">Например, вполне допустимо, чтобы корпоративная Разработка программного обеспечения основывала контрольные суммы в программном обеспечении, основанном на французском (Франции) ресурсах, а не на английском (США) ресурсе, если все приложения имеют ресурсы для французского языка (Франция), на которых должны основываться контрольные суммы.</span><span class="sxs-lookup"><span data-stu-id="63ee7-227">For example, it is perfectly acceptable for a software development enterprise to base its checksums in the software it builds on French (France) resources instead of English (United States) resources, as long as all the applications have French (France) resources on which to base the checksums.</span></span> <span data-ttu-id="63ee7-228">Также можно использовать файл конфигурации ресурсов для присвоения контрольной суммы произвольного шестнадцатеричного значения до 16 шестнадцатеричных цифр.</span><span class="sxs-lookup"><span data-stu-id="63ee7-228">It is also acceptable to use the resource configuration file to assign an arbitrary hexadecimal value of up to 16 hexadecimal digits as a checksum.</span></span> <span data-ttu-id="63ee7-229">Последняя стратегия исключает эффективное использование ключей-z,-c и-b для МУИРКТ.</span><span class="sxs-lookup"><span data-stu-id="63ee7-229">This last strategy precludes the effective use of the -z, -c, and -b switches of MUIRCT.</span></span> <span data-ttu-id="63ee7-230">Для создания значений контрольной суммы требуется внедрение метода с помощью [**GuidGen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) или какого-либо другого средства.</span><span class="sxs-lookup"><span data-stu-id="63ee7-230">It requires adoption of a method using either [**GuidGen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) or some other tool to generate checksum values.</span></span> <span data-ttu-id="63ee7-231">Эта стратегия также требует настройки политики для определения необходимости изменения значения при добавлении новых локализуемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63ee7-231">This strategy also requires you to set up a policy for determining when to modify the value when adding new localizable resources.</span></span>

<span data-ttu-id="63ee7-232">Чтобы применить контрольную сумму "Английский (США)" ко всем файлам, можно использовать любой из описанных выше методов обработки контрольных сумм.</span><span class="sxs-lookup"><span data-stu-id="63ee7-232">To apply the English (United States) checksum to all files, you can use any of the checksum handling methods described above.</span></span> <span data-ttu-id="63ee7-233">Например, можно создать файл файла ресурсов LN и для конкретного языка для английского языка (США), а затем использовать параметр МУИРКТ-d для получения итоговой контрольной суммы.</span><span class="sxs-lookup"><span data-stu-id="63ee7-233">For example, you can generate the LN file and language-specific resource file for English (United States), then use the MUIRCT -d switch to obtain the resulting checksum.</span></span> <span data-ttu-id="63ee7-234">Эту контрольную сумму можно скопировать в файл конфигурации ресурса и использовать параметр-q с МУИРКТ, чтобы применить контрольную сумму ко всем остальным файлам.</span><span class="sxs-lookup"><span data-stu-id="63ee7-234">You can copy this checksum into your resource configuration file and use the -q switch with MUIRCT to apply the checksum to all other files.</span></span>

### <a name="use-of-a-resource-configuration-file-with-muirct"></a><span data-ttu-id="63ee7-235">Использование файла конфигурации ресурсов с МУИРКТ</span><span class="sxs-lookup"><span data-stu-id="63ee7-235">Use of a Resource Configuration File with MUIRCT</span></span>

<span data-ttu-id="63ee7-236">При использовании МУИРКТ можно указать данные конфигурации ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63ee7-236">You can specify resource configuration data when using MUIRCT.</span></span> <span data-ttu-id="63ee7-237">Независимо от того, предоставиле ли вы явно файл конфигурации ресурсов, все файлы ресурсов, относящиеся к конкретному языку, имеют данные конфигурации ресурсов, как и любой LN-файл со связанным файлом ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63ee7-237">Whether or not you explicitly supply a resource configuration file, every language-specific resource file has resource configuration data, as does any LN file with an associated resource file.</span></span> <span data-ttu-id="63ee7-238">Пример:</span><span class="sxs-lookup"><span data-stu-id="63ee7-238">For example:</span></span>

-   <span data-ttu-id="63ee7-239">Если вы используете параметр-q для указания файла конфигурации ресурса, но в исходном файле входных данных нет локализуемых ресурсов, файл ресурсов для конкретного языка не создается, а результирующий LN-файл не содержит данные конфигурации ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63ee7-239">If you use the -q switch to specify a resource configuration file, but there are no localizable resources in your input source file, no language-specific resource file is generated and the resulting LN file does not contain resource configuration data.</span></span> <span data-ttu-id="63ee7-240">Кроме того, если входной файл источника содержит многоязычные ресурсы, МУИРКТ не будет разделять файл.</span><span class="sxs-lookup"><span data-stu-id="63ee7-240">Also, if the input source file has multilingual resources, then MUIRCT won't split the file.</span></span>

> [!Note]  
> <span data-ttu-id="63ee7-241">В настоящее время поведение МУИРКТ не согласуется, если элемент Неутралресаурцес файла конфигурации ресурса не содержит элементов resourceType, а элемент localizedResources содержит строки и меню, например.</span><span class="sxs-lookup"><span data-stu-id="63ee7-241">Currently the behavior of MUIRCT is inconsistent when the neutralResources element of the resource configuration file contains no resourceType elements and the localizedResources element contains strings and menus, for example.</span></span> <span data-ttu-id="63ee7-242">В этом случае МУИРКТ разделяет ресурсы следующим образом:</span><span class="sxs-lookup"><span data-stu-id="63ee7-242">In such a case, MUIRCT splits the resources as follows:</span></span>
>
> -   <span data-ttu-id="63ee7-243">Все ресурсы в исходном двоичном файле (включая строки и меню) и ресурсы многоязыкового интерфейса пользователя помещаются в LN-файл.</span><span class="sxs-lookup"><span data-stu-id="63ee7-243">All resources in the original binary (including strings and menus), plus the MUI resources, are placed in the LN file.</span></span>
> -   <span data-ttu-id="63ee7-244">Строки, меню и ресурсы многоязыкового интерфейса пользователя помещаются в соответствующий файл ресурсов, зависящий от языка.</span><span class="sxs-lookup"><span data-stu-id="63ee7-244">Strings, menus, and MUI resources are placed in the appropriate language-specific resource file.</span></span>

 

### <a name="examples-for-using-muirct"></a><span data-ttu-id="63ee7-245">Примеры использования МУИРКТ</span><span class="sxs-lookup"><span data-stu-id="63ee7-245">Examples for Using MUIRCT</span></span>

<span data-ttu-id="63ee7-246">**Примеры стандартного использования**</span><span class="sxs-lookup"><span data-stu-id="63ee7-246">**Examples of Standard Usage**</span></span>


```C++
muirct -q mui.MMF bar.exe barnew.exe barnew.exe.mui

muirct -d myprog.exe.mui
```



<span data-ttu-id="63ee7-247">**Пример вывода выходных файлов с помощью параметра-d**</span><span class="sxs-lookup"><span data-stu-id="63ee7-247">**Example of LN File Output Using -d Switch**</span></span>

<span data-ttu-id="63ee7-248">Ниже приведен пример выходных данных конфигурации ресурсов из LN-файла, Shell32.dll с помощью параметра-d с МУИРКТ:</span><span class="sxs-lookup"><span data-stu-id="63ee7-248">Here is an example of the resource configuration data output from an LN file, Shell32.dll, using the -d switch with MUIRCT:</span></span>


```C++
Signature          -    fecdfecd
Length             -    148
RC Config Version  -    10000
FileType           -    11
SystemAttributes   -    100
UltimateFallback location    -  external
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    AVI FTR ORDERSTREAM TYPELIB UIFILE XML MUI
MainIDTypes        -    1 2 3 12 14 16 24
MuiNameTypes       -    MUI
MuiIDTypes         -    2 3 4 5 6 9 14 16
UltimateFallbackLanguage   -   en-US
```



<span data-ttu-id="63ee7-249">**Пример вывода файла ресурсов Language-Specific с помощью параметра-d**</span><span class="sxs-lookup"><span data-stu-id="63ee7-249">**Example of Language-Specific Resource File Output Using -d Switch**</span></span>

<span data-ttu-id="63ee7-250">Ниже приведен пример выходных данных конфигурации ресурсов из файла MUI Shell32.dll. MUI с помощью параметра-d для МУИРКТ:</span><span class="sxs-lookup"><span data-stu-id="63ee7-250">Here is an example of the resource configuration data output from a .mui file, Shell32.dll.mui, using the -d switch for MUIRCT:</span></span>


```C++
Signature          -    fecdfecd
Length             -     c8
RC Config Version  -    10000
FileType           -    12
SystemAttributes   -    100
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    MUI
MainIDTypes        -    2 3 4 5 6 9 14 16
Language           -    en-US
```



## <a name="rc-compiler-utility"></a><span data-ttu-id="63ee7-251">Служебная программа компилятора RC</span><span class="sxs-lookup"><span data-stu-id="63ee7-251">RC Compiler Utility</span></span>

<span data-ttu-id="63ee7-252">Компилятор RC (Rc.exe) — это служебная программа командной строки для компиляции файла скрипта определения ресурса (расширение RC) в файлы ресурсов (расширение RES).</span><span class="sxs-lookup"><span data-stu-id="63ee7-252">RC Compiler (Rc.exe) is a command line utility for compiling a resource definition script file (.rc extension) into resource files (.res extension).</span></span> <span data-ttu-id="63ee7-253">Компилятор RC включен в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="63ee7-253">RC Compiler is included in the Windows SDK.</span></span> <span data-ttu-id="63ee7-254">В этом документе объясняется только использование компилятора RC с возможностями загрузчика ресурсов, связанными с MUI.</span><span class="sxs-lookup"><span data-stu-id="63ee7-254">This document only explains the use of RC Compiler with MUI-related capabilities of the resource loader.</span></span> <span data-ttu-id="63ee7-255">Полные сведения о компиляторе см. в разделе [о файлах ресурсов](../menurc/about-resource-files.md).</span><span class="sxs-lookup"><span data-stu-id="63ee7-255">For complete information about the compiler, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

<span data-ttu-id="63ee7-256">Компилятор RC позволяет выполнять сборку из одного набора источников, LN-файла и отдельного файла ресурсов, зависящего от языка.</span><span class="sxs-lookup"><span data-stu-id="63ee7-256">RC Compiler allows you to build, from a single set of sources, an LN file and a separate language-specific resource file.</span></span> <span data-ttu-id="63ee7-257">Как и для МУИРКТ, файлы связаны с данными конфигурации ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63ee7-257">As for MUIRCT, the files are associated by resource configuration data.</span></span>

### <a name="rc-compiler-syntax-as-used-for-mui-resources"></a><span data-ttu-id="63ee7-258">Синтаксис компилятора RC, используемый для ресурсов MUI</span><span class="sxs-lookup"><span data-stu-id="63ee7-258">RC Compiler Syntax as Used for MUI Resources</span></span>

<span data-ttu-id="63ee7-259">Параметры компилятора RC подробно определяются при использовании версии- [кандидата](../menurc/using-rc-the-rc-command-line-.md).</span><span class="sxs-lookup"><span data-stu-id="63ee7-259">RC Compiler switches are defined in detail in [Using RC](../menurc/using-rc-the-rc-command-line-.md).</span></span> <span data-ttu-id="63ee7-260">В этом разделе определяются только параметры, используемые для создания ресурсов MUI.</span><span class="sxs-lookup"><span data-stu-id="63ee7-260">This section only defines the switches used to build MUI resources.</span></span> <span data-ttu-id="63ee7-261">Помните, что каждый параметр не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="63ee7-261">Remember that each switch is case-insensitive.</span></span> <span data-ttu-id="63ee7-262">Типы ресурсов считаются нейтральными к языку, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="63ee7-262">Resource types are assumed to be language-neutral unless otherwise indicated.</span></span>


```C++
rc [-h|-?] -fm mui_res_name [-q rc_config_file_name] [-g langid] [-g1 ] [-g2 version]
```



<span data-ttu-id="63ee7-263">**Параметры и аргументы**</span><span class="sxs-lookup"><span data-stu-id="63ee7-263">**Switches and Arguments**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63ee7-264">-h |-?</span><span class="sxs-lookup"><span data-stu-id="63ee7-264">-h|-?</span></span></td>
<td><span data-ttu-id="63ee7-265">Отображает экран справки.</span><span class="sxs-lookup"><span data-stu-id="63ee7-265">Shows help screen.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ee7-266">— FM</span><span class="sxs-lookup"><span data-stu-id="63ee7-266">-fm</span></span></td>
<td><span data-ttu-id="63ee7-267">Использует указанный файл ресурсов для зависящих от языка ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63ee7-267">Uses the specified resource file for language-specific resources.</span></span> <span data-ttu-id="63ee7-268">Обычно компилятор ресурсов создает файл ресурсов, зависящий от языка.</span><span class="sxs-lookup"><span data-stu-id="63ee7-268">Normally the resource compiler creates a language-specific resource file.</span></span> <span data-ttu-id="63ee7-269">Однако файл не создается, если выполняется одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="63ee7-269">However, it does not create the file if any of the following conditions exist:</span></span><br/>
<ul>
<li><span data-ttu-id="63ee7-270">В RC-файле нет локализуемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63ee7-270">There are no localizable resources in the .rc file.</span></span></li>
<li><span data-ttu-id="63ee7-271">Единственный язык ресурсов, найденный в RC-файле, — это нейтральный язык.</span><span class="sxs-lookup"><span data-stu-id="63ee7-271">The only resource language found in the .rc file is the neutral language.</span></span></li>
<li><span data-ttu-id="63ee7-272">RC-файл содержит ресурсы для более чем одного языка, не считая нейтральный язык.</span><span class="sxs-lookup"><span data-stu-id="63ee7-272">The .rc file has resources for more than one language, not counting the neutral language.</span></span> <span data-ttu-id="63ee7-273">Если RC-файл содержит ресурсы для двух языков, а один из них является нейтральным языком, компилятор считает, что файл является одноязычным.</span><span class="sxs-lookup"><span data-stu-id="63ee7-273">If the .rc file contains resources for two languages, and one of them is the neutral language, the compiler considers the file to be monolingual.</span></span> <span data-ttu-id="63ee7-274">При наличии локализуемых ресурсов компилятор создает файл ресурсов, зависящий от языка.</span><span class="sxs-lookup"><span data-stu-id="63ee7-274">If there are any localizable resources, the compiler creates a language-specific resource file.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ee7-275">-Q</span><span class="sxs-lookup"><span data-stu-id="63ee7-275">-q</span></span></td>
<td><span data-ttu-id="63ee7-276">Использует указанный файл конфигурации ресурсов для получения типов ресурсов для размещения в файле ресурсов для конкретного языка и в LN-файле.</span><span class="sxs-lookup"><span data-stu-id="63ee7-276">Uses the specified resource configuration file to obtain the resource types to place in the language-specific resource file and the LN file.</span></span> <span data-ttu-id="63ee7-277">Дополнительные сведения см. <a href="preparing-a-resource-configuration-file.md">в разделе Подготовка файла конфигурации ресурса</a>.</span><span class="sxs-lookup"><span data-stu-id="63ee7-277">For more information, see <a href="preparing-a-resource-configuration-file.md">Preparing a Resource Configuration File</a>.</span></span> <span data-ttu-id="63ee7-278">В качестве альтернативы этому параметру можно использовать параметры-j и-k, но рекомендуется использовать файл конфигурации ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63ee7-278">As an alternative to this switch, you can use the -j and -k switches, but it is preferred to use a resource configuration file.</span></span> <br/> <span data-ttu-id="63ee7-279">С помощью параметра-q с файлом конфигурации ресурсов можно реализовать разбиение на элементы и предоставить атрибуты, которые будут иметь конфигурацию двоичных ресурсов в LN и файле ресурсов, зависящем от языка.</span><span class="sxs-lookup"><span data-stu-id="63ee7-279">By using the -q switch with a resource configuration file, you can implement an item-based split and provide attributes that will end up with the binary resource configuration in the LN and language-specific resource file.</span></span> <span data-ttu-id="63ee7-280">Это разбиение невозможно с помощью ключей-j и-k.</span><span class="sxs-lookup"><span data-stu-id="63ee7-280">This split is not possible using the -j and -k switches.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="63ee7-281">Процесс разбиения компилятора RC не работает должным образом, если ресурсы и сведения о версии хранятся в разных файлах конфигурации ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63ee7-281">The RC Compiler split process does not work properly if you store resources and version information in different resource configuration files.</span></span> <span data-ttu-id="63ee7-282">В этом случае компилятор RC не разделяет сведения о версии.</span><span class="sxs-lookup"><span data-stu-id="63ee7-282">In this case, RC Compiler does not split the version information.</span></span> <span data-ttu-id="63ee7-283">Поэтому во время связывания файла ресурсов, относящегося к конкретному языку, возникает ошибка компоновщика, так как у файла нет ресурсов версии.</span><span class="sxs-lookup"><span data-stu-id="63ee7-283">Therefore a linker error occurs during linking of the language-specific resource file because the file does not have version resources.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ee7-284">-g</span><span class="sxs-lookup"><span data-stu-id="63ee7-284">-g</span></span></td>
<td><span data-ttu-id="63ee7-285">Указывает конечный идентификатор <a href="language-identifiers.md">базового языка</a> в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="63ee7-285">Specifies the ultimate <a href="language-identifiers.md">fallback language</a> identifier in hexadecimal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ee7-286">-G1</span><span class="sxs-lookup"><span data-stu-id="63ee7-286">-g1</span></span></td>
<td><span data-ttu-id="63ee7-287">Создает RES-файл MUI, даже если ресурсом версии является единственное локализуемое содержимое.</span><span class="sxs-lookup"><span data-stu-id="63ee7-287">Creates a MUI .res file even if the VERSION resource is the only localizable content.</span></span> <span data-ttu-id="63ee7-288">По умолчанию компилятор RC не создает RES-файл, если версия является единственным локализуемое ресурсом.</span><span class="sxs-lookup"><span data-stu-id="63ee7-288">By default, RC Compiler does not produce a .res file if VERSION is the only localizable resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ee7-289">-g2</span><span class="sxs-lookup"><span data-stu-id="63ee7-289">-g2</span></span></td>
<td><span data-ttu-id="63ee7-290">Указывает настраиваемый номер версии, используемый при вычислении контрольной суммы.</span><span class="sxs-lookup"><span data-stu-id="63ee7-290">Specifies the custom version number to use when calculating the checksum.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ee7-291">mui_res_name</span><span class="sxs-lookup"><span data-stu-id="63ee7-291">mui_res_name</span></span></td>
<td><span data-ttu-id="63ee7-292">Файл ресурсов для ресурсов, зависящих от языка.</span><span class="sxs-lookup"><span data-stu-id="63ee7-292">Resource file for language-specific resources.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ee7-293">rc_config_file_name</span><span class="sxs-lookup"><span data-stu-id="63ee7-293">rc_config_file_name</span></span></td>
<td><span data-ttu-id="63ee7-294">Файл конфигурации ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63ee7-294">Resource configuration file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ee7-295">langid</span><span class="sxs-lookup"><span data-stu-id="63ee7-295">langid</span></span></td>
<td><span data-ttu-id="63ee7-296">Идентификатор языка.</span><span class="sxs-lookup"><span data-stu-id="63ee7-296">Language identifier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ee7-297">version</span><span class="sxs-lookup"><span data-stu-id="63ee7-297">version</span></span></td>
<td><span data-ttu-id="63ee7-298">Пользовательский номер версии в формате, например &quot; 6.2.0.0 &quot; .</span><span class="sxs-lookup"><span data-stu-id="63ee7-298">Custom version number, in a format such as &quot;6.2.0.0&quot;.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="example-for-using-rc-compiler-to-build-mui-resources"></a><span data-ttu-id="63ee7-299">Пример использования компилятора RC для создания ресурсов многоязыкового интерфейса пользователя</span><span class="sxs-lookup"><span data-stu-id="63ee7-299">Example for Using RC Compiler to Build MUI Resources</span></span>

<span data-ttu-id="63ee7-300">Чтобы продемонстрировать операцию компилятора RC с ресурсами многоязыкового интерфейса пользователя, давайте рассмотрим следующую командную строку для файла ресурсов MyFile. rc:</span><span class="sxs-lookup"><span data-stu-id="63ee7-300">To illustrate RC Compiler operation with MUI resources, let's examine the following command line, for the resource file Myfile.rc:</span></span>


```C++
rc -fm myfile_res.res -q myfile.rcconfig myfile.rc
```



<span data-ttu-id="63ee7-301">Эта командная строка заставляет компилятор RC выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="63ee7-301">This command line causes RC Compiler to do the following:</span></span>

-   <span data-ttu-id="63ee7-302">Создайте файл ресурсов для конкретного языка MyFile \_ Res. Res и файл ресурсов, не зависящий от языка, который по умолчанию имеет значение MyFile. res на основе имени RC-файла.</span><span class="sxs-lookup"><span data-stu-id="63ee7-302">Create the language-specific resource file Myfile\_res.res and a language-neutral resource file that defaults to Myfile.res, based on the name of the .rc file.</span></span>
-   <span data-ttu-id="63ee7-303">Добавьте 2 (Item 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 \_ типы ресурсов My Type в файл Res, зависящий от языка, если они находятся в RC-файле.</span><span class="sxs-lookup"><span data-stu-id="63ee7-303">Add the 2 (item 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 MY\_TYPE resource types to the language-specific .res file if they are in the .rc file.</span></span>
-   <span data-ttu-id="63ee7-304">Добавьте тип ресурса 16, а также другие типы ресурсов, описанные в файле ресурсов, в файл с нейтральным языком. Res и в RES-файл, зависящий от языка.</span><span class="sxs-lookup"><span data-stu-id="63ee7-304">Add resource type 16, along with any other resource types described in the resource file to the language-neutral .res file and to the language-specific .res file.</span></span> <span data-ttu-id="63ee7-305">Обратите внимание, что в этом примере тип ресурса 16 добавляется в двух местах.</span><span class="sxs-lookup"><span data-stu-id="63ee7-305">Note that, in this example, resource type 16 is being added in two places.</span></span>
-   <span data-ttu-id="63ee7-306">Выберите значение атрибута «Ултиматефаллбакклангуаже», чтобы вставить данные конфигурации ресурса «LN file» на основе следующих критериев, упорядоченных от наивысшего приоритета к наименьшему:</span><span class="sxs-lookup"><span data-stu-id="63ee7-306">Choose the "UltimateFallbackLanguage" attribute value to insert into the LN file resource configuration data based on the following criteria, ordered from highest priority to lowest:</span></span>
    -   <span data-ttu-id="63ee7-307">Атрибут "Ултиматефаллбакклангуаже" в файле конфигурации ресурса, если он передан в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="63ee7-307">"UltimateFallbackLanguage" attribute in the resource configuration file if one is passed in as input.</span></span>
    -   <span data-ttu-id="63ee7-308">Значение атрибута language для вставки в данные конфигурации ресурсов на основе порядка языков компилятора RC (нейтральный к определенному языку язык файла ресурсов).</span><span class="sxs-lookup"><span data-stu-id="63ee7-308">Language attribute value to insert in the resource configuration data based on the RC Compiler language order (language-neutral and language-specific resource file language).</span></span> <span data-ttu-id="63ee7-309">Рекомендации включают в себя язык в RC-файле, значение языка параметра-GL и идентификатор 0x0409 для английского языка (США).</span><span class="sxs-lookup"><span data-stu-id="63ee7-309">Considerations include language in the .rc file, language value of the -gl switch, and identifier 0x0409 for English (United States).</span></span>

## <a name="remarks"></a><span data-ttu-id="63ee7-310">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63ee7-310">Remarks</span></span>

<span data-ttu-id="63ee7-311">Если включить в элемент Неутралресаурцес любой тип ресурса ICON (3), DIALOG (5), STRING (6) или VERSION (16), необходимо дублировать эту запись в элементе localizedResources в файле конфигурации ресурса.</span><span class="sxs-lookup"><span data-stu-id="63ee7-311">If you include any ICON(3), DIALOG(5), STRING(6), or VERSION(16) resource type in the neutralResources element, then you have to duplicate that entry in the localizedResources element in the resource configuration file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63ee7-312">См. также</span><span class="sxs-lookup"><span data-stu-id="63ee7-312">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63ee7-313">Справочник по многоязычному пользовательскому интерфейсу</span><span class="sxs-lookup"><span data-stu-id="63ee7-313">Multilingual User Interface Reference</span></span>](multilingual-user-interface-reference.md)
</dt> <dt>

[<span data-ttu-id="63ee7-314">Управление ресурсами MUI</span><span class="sxs-lookup"><span data-stu-id="63ee7-314">MUI Resource Management</span></span>](mui-resource-management.md)
</dt> <dt>

[<span data-ttu-id="63ee7-315">Локализация ресурсов и сборка приложения</span><span class="sxs-lookup"><span data-stu-id="63ee7-315">Localizing Resources and Building the Application</span></span>](localizing-resources-and-building-the-application.md)
</dt> </dl>

 

 
