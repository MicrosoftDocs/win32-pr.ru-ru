---
description: Сервер-источник позволяет клиенту получить точную версию исходных файлов, которые использовались для построения приложения.
ms.assetid: c7bf51ce-7fb4-49aa-ad33-e551b2c8362b
title: Исходный сервер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3d8d76c70b67c176126d8e424bd5b55b616697
ms.sourcegitcommit: bfb5d94f754d017307b4cc9d914a2716701331d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656723"
---
# <a name="source-server"></a><span data-ttu-id="b6e79-103">Исходный сервер</span><span class="sxs-lookup"><span data-stu-id="b6e79-103">Source Server</span></span>

<span data-ttu-id="b6e79-104">Сервер-источник позволяет клиенту получить точную версию исходных файлов, которые использовались для построения приложения.</span><span class="sxs-lookup"><span data-stu-id="b6e79-104">Source server enables a client to retrieve the exact version of the source files that were used to build an application.</span></span> <span data-ttu-id="b6e79-105">Поскольку исходный код модуля может изменяться в разных версиях и в течение нескольких лет, важно взглянуть на исходный код, который существовал при построении рассматриваемой версии модуля.</span><span class="sxs-lookup"><span data-stu-id="b6e79-105">Because the source code for a module can change between versions and over a course of years, it is important to look at the source code as it existed when the version of the module in question was built.</span></span>

<span data-ttu-id="b6e79-106">Исходный сервер получает соответствующие файлы из системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="b6e79-106">Source server retrieves the appropriate files from source control.</span></span> <span data-ttu-id="b6e79-107">Для использования исходного сервера приложение должно быть индексировано в исходном виде.</span><span class="sxs-lookup"><span data-stu-id="b6e79-107">To use source server, the application must have been source indexed.</span></span>

## <a name="source-indexing"></a><span data-ttu-id="b6e79-108">Индексирование исходного кода</span><span class="sxs-lookup"><span data-stu-id="b6e79-108">Source Indexing</span></span>

<span data-ttu-id="b6e79-109">Исходная система индексации представляет собой коллекцию исполняемых файлов и скриптов Perl.</span><span class="sxs-lookup"><span data-stu-id="b6e79-109">The source indexing system is a collection of executable files and Perl scripts.</span></span> <span data-ttu-id="b6e79-110">Для сценариев Perl требуется Perl 5,6 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="b6e79-110">The Perl scripts require Perl 5.6 or greater.</span></span>

<span data-ttu-id="b6e79-111">Как правило, двоичные файлы индексируются в процессе сборки после построения приложения.</span><span class="sxs-lookup"><span data-stu-id="b6e79-111">Generally, binaries are source indexed during the build process after the application has been built.</span></span> <span data-ttu-id="b6e79-112">Сведения, необходимые исходному серверу, хранятся в PDB-файлах.</span><span class="sxs-lookup"><span data-stu-id="b6e79-112">The information needed by source server is stored in the PDB files.</span></span>

<span data-ttu-id="b6e79-113">Сервер исходного кода в настоящее время поставляется со сценариями, которые должны работать со следующими системами управления версиями.</span><span class="sxs-lookup"><span data-stu-id="b6e79-113">Source server currently ships with scripts that should work with the following source-control systems.</span></span>

-   <span data-ttu-id="b6e79-114">Team Foundation Server</span><span class="sxs-lookup"><span data-stu-id="b6e79-114">Team Foundation Server</span></span>
-   <span data-ttu-id="b6e79-115">перфорце</span><span class="sxs-lookup"><span data-stu-id="b6e79-115">Perforce</span></span>
-   <span data-ttu-id="b6e79-116">Visual SourceSafe</span><span class="sxs-lookup"><span data-stu-id="b6e79-116">Visual SourceSafe</span></span>
-   <span data-ttu-id="b6e79-117">CVS</span><span class="sxs-lookup"><span data-stu-id="b6e79-117">CVS</span></span>
-   <span data-ttu-id="b6e79-118">Subversion</span><span class="sxs-lookup"><span data-stu-id="b6e79-118">Subversion</span></span>

<span data-ttu-id="b6e79-119">Можно также создать пользовательский скрипт для индексирования кода для другой системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="b6e79-119">You can also create a custom script to index your code for a different source-control system.</span></span>

<span data-ttu-id="b6e79-120">В следующей таблице перечислены средства исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="b6e79-120">The following table lists the source server tools.</span></span>



| <span data-ttu-id="b6e79-121">Средство</span><span class="sxs-lookup"><span data-stu-id="b6e79-121">Tool</span></span>        | <span data-ttu-id="b6e79-122">Описание</span><span class="sxs-lookup"><span data-stu-id="b6e79-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6e79-123">Srcsrv.ini</span><span class="sxs-lookup"><span data-stu-id="b6e79-123">Srcsrv.ini</span></span>  | <span data-ttu-id="b6e79-124">Этот файл является главным списком всех серверов системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="b6e79-124">This file is the master list of all source control servers.</span></span> <span data-ttu-id="b6e79-125">Каждая запись имеет следующий формат:*MYSERVER* = *ServerInfo*</span><span class="sxs-lookup"><span data-stu-id="b6e79-125">Each entry has the following format:*MYSERVER*=*serverinfo*</span></span><br/> <span data-ttu-id="b6e79-126">При использовании Перфорце сведения о сервере состоят из полного сетевого пути к серверу, за которым следует двоеточие, за которым следует номер порта, который он использует.</span><span class="sxs-lookup"><span data-stu-id="b6e79-126">When using Perforce, the server info consists of the full network path to the server, followed by a colon, followed by the port number it uses.</span></span> <span data-ttu-id="b6e79-127">Пример:</span><span class="sxs-lookup"><span data-stu-id="b6e79-127">For example:</span></span><br/> <span data-ttu-id="b6e79-128">MYSERVER = Machine. Corp. Company. com: 1666</span><span class="sxs-lookup"><span data-stu-id="b6e79-128">MYSERVER=machine.corp.company.com:1666</span></span><br/> <span data-ttu-id="b6e79-129">Этот файл можно установить на компьютере, на котором работает отладчик.</span><span class="sxs-lookup"><span data-stu-id="b6e79-129">This file can be installed on the computer running the debugger.</span></span> <span data-ttu-id="b6e79-130">При запуске исходного сервера он просматривает Srcsrv.ini для значений; Эти значения будут переопределять сведения, содержащиеся в PDB-файле.</span><span class="sxs-lookup"><span data-stu-id="b6e79-130">When source server starts, it looks at Srcsrv.ini for values; these values will override the information contained in the PDB file.</span></span> <span data-ttu-id="b6e79-131">Это позволяет пользователям настроить отладчик для использования другого сервера системы управления версиями во время отладки.</span><span class="sxs-lookup"><span data-stu-id="b6e79-131">This enables users to configure a debugger to use an alternate source control server at debug time.</span></span><br/> <span data-ttu-id="b6e79-132">Дополнительные сведения см. в примере Srcsrv.ini установлен с помощью средств исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="b6e79-132">For more information, see the example Srcsrv.ini installed with the source server tools.</span></span><br/> |
| <span data-ttu-id="b6e79-133">SSINDEX. cmd</span><span class="sxs-lookup"><span data-stu-id="b6e79-133">Ssindex.cmd</span></span> | <span data-ttu-id="b6e79-134">Этот сценарий создает список файлов, возвращенных в систему управления версиями, и сведения о версии каждого файла.</span><span class="sxs-lookup"><span data-stu-id="b6e79-134">This script builds the list of files checked into source control along with the version information of each file.</span></span> <span data-ttu-id="b6e79-135">Он сохраняет подмножество этих сведений в PDB-файлах, созданных при построении приложения.</span><span class="sxs-lookup"><span data-stu-id="b6e79-135">It stores a subset of this information in the .pdb files generated when you built the application.</span></span> <span data-ttu-id="b6e79-136">Скрипт использует один из следующих модулей Perl для взаимодействия с системой управления версиями: P4.pm (Перфорце) или Vss.pm (исходный код — надежный). Для получения дополнительных сведений запустите сценарий с параметром-?.</span><span class="sxs-lookup"><span data-stu-id="b6e79-136">The script uses one of the following Perl modules to interface with source control: P4.pm (Perforce) or Vss.pm (Visual Source Safe).For more information, run the script with the -?</span></span> <span data-ttu-id="b6e79-137">или-??</span><span class="sxs-lookup"><span data-stu-id="b6e79-137">or -??</span></span> <span data-ttu-id="b6e79-138">(подробное описание справки) или просмотрите скрипт.</span><span class="sxs-lookup"><span data-stu-id="b6e79-138">(verbose help) option or examine the script.</span></span><br/>                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="b6e79-139">Srctool.exe</span><span class="sxs-lookup"><span data-stu-id="b6e79-139">Srctool.exe</span></span> | <span data-ttu-id="b6e79-140">Эта программа отображает список всех файлов, проиндексированных в PDB-файле.</span><span class="sxs-lookup"><span data-stu-id="b6e79-140">This utility lists all files indexed within a .pdb file.</span></span> <span data-ttu-id="b6e79-141">Для каждого файла отображается полный путь, сервер системы управления версиями и номер версии файла.</span><span class="sxs-lookup"><span data-stu-id="b6e79-141">For each file, it lists the full path, source control server, and version number of the file.</span></span> <span data-ttu-id="b6e79-142">Эти сведения можно использовать для получения файлов без использования исходного сервера. Для получения дополнительных сведений запустите программу с параметром/?.</span><span class="sxs-lookup"><span data-stu-id="b6e79-142">You can use this information to retrieve files without using the source server.For more information, run the utility with the /?</span></span> <span data-ttu-id="b6e79-143">(Создайте ветвь для и запустите запрос на вытягивание).</span><span class="sxs-lookup"><span data-stu-id="b6e79-143">option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="b6e79-144">Pdbstr.exe</span><span class="sxs-lookup"><span data-stu-id="b6e79-144">Pdbstr.exe</span></span>  | <span data-ttu-id="b6e79-145">Эта программа используется скриптами индексирования для вставки сведений системы управления версиями в альтернативный поток "SRCSRV" целевого PDB-файла.</span><span class="sxs-lookup"><span data-stu-id="b6e79-145">This utility is used by the indexing scripts to insert the version control information into the "srcsrv" alternate stream of the target .pdb file.</span></span> <span data-ttu-id="b6e79-146">Он также может считывать любой поток из PDB-файла.</span><span class="sxs-lookup"><span data-stu-id="b6e79-146">It can also read any stream from a .pdb file.</span></span> <span data-ttu-id="b6e79-147">Эти сведения можно использовать для проверки правильности работы сценариев индексирования. Для получения дополнительных сведений запустите программу с параметром/?.</span><span class="sxs-lookup"><span data-stu-id="b6e79-147">You can use this information to verify that the indexing scripts are working properly.For more information, run the utility with the /?</span></span> <span data-ttu-id="b6e79-148">(Создайте ветвь для и запустите запрос на вытягивание).</span><span class="sxs-lookup"><span data-stu-id="b6e79-148">option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="retrieving-the-source-file"></a><span data-ttu-id="b6e79-149">Получение исходного файла</span><span class="sxs-lookup"><span data-stu-id="b6e79-149">Retrieving the Source File</span></span>

<span data-ttu-id="b6e79-150">API DbgHelp предоставляет доступ к функциям исходного сервера с помощью функции [**симжетсаурцефиле**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) .</span><span class="sxs-lookup"><span data-stu-id="b6e79-150">The DbgHelp API provides access to source server functionality through the [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) function.</span></span> <span data-ttu-id="b6e79-151">Чтобы получить имя исходного файла для извлечения, вызовите функцию [**сименумсаурцефилес**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) или [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) .</span><span class="sxs-lookup"><span data-stu-id="b6e79-151">To retrieve the name of the source file to be retrieved, call the [**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) or [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) function.</span></span>

## <a name="using-source-server-with-a-debugger"></a><span data-ttu-id="b6e79-152">Использование исходного сервера с отладчиком</span><span class="sxs-lookup"><span data-stu-id="b6e79-152">Using Source Server with a Debugger</span></span>

<span data-ttu-id="b6e79-153">Чтобы использовать исходный сервер с WinDbg, KD, NTSD или CDB, убедитесь, что установлена последняя версия пакета средств отладки для Windows (версия 6,3 или более поздняя).</span><span class="sxs-lookup"><span data-stu-id="b6e79-153">To use the source server with WinDbg, KD, NTSD, or CDB, ensure that you have installed a recent version of the Debugging Tools for Windows package (version 6.3 or later).</span></span> <span data-ttu-id="b6e79-154">Затем включите SRV \* в команду. сркпас следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b6e79-154">Then, include srv\* in the .srcpath command as follows:</span></span>

<span data-ttu-id="b6e79-155">**\. сркпас SRV \* ;** _c: \\ mysource_</span><span class="sxs-lookup"><span data-stu-id="b6e79-155">**\.srcpath srv\*;**_c:\\mysource_</span></span>

<span data-ttu-id="b6e79-156">Обратите внимание, что этот пример также включает традиционный исходный путь.</span><span class="sxs-lookup"><span data-stu-id="b6e79-156">Note that this example also includes a traditional source path.</span></span> <span data-ttu-id="b6e79-157">Если отладчику не удается получить файл с исходного сервера, он будет искать по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="b6e79-157">If the debugger cannot retrieve the file from the source server, it will search the specified path.</span></span>

<span data-ttu-id="b6e79-158">Если исходный файл извлекается исходным сервером, он остается на жестком диске после завершения сеанса отладки.</span><span class="sxs-lookup"><span data-stu-id="b6e79-158">If a source file is retrieved by the source server, it will remain on your hard drive after the debugging session is over.</span></span> <span data-ttu-id="b6e79-159">Исходные файлы хранятся локально в подкаталоге src в каталоге установки средств отладки для Windows.</span><span class="sxs-lookup"><span data-stu-id="b6e79-159">Source files are stored locally in the src subdirectory of the Debugging Tools for Windows installation directory.</span></span>

## <a name="source-server-data-blocks"></a><span data-ttu-id="b6e79-160">Блоки данных на исходном сервере</span><span class="sxs-lookup"><span data-stu-id="b6e79-160">Source Server Data Blocks</span></span>

<span data-ttu-id="b6e79-161">Исходный сервер использует два блока данных в PDB-файле.</span><span class="sxs-lookup"><span data-stu-id="b6e79-161">Source server relies on two blocks of data within the PDB file.</span></span>

-   <span data-ttu-id="b6e79-162">Список исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="b6e79-162">Source file list.</span></span> <span data-ttu-id="b6e79-163">При построении модуля автоматически создается список полных путей к исходным файлам, используемым для построения модуля.</span><span class="sxs-lookup"><span data-stu-id="b6e79-163">Building a module automatically creates a list of fully qualified paths to the source files used to build the module.</span></span>
-   <span data-ttu-id="b6e79-164">Блок данных.</span><span class="sxs-lookup"><span data-stu-id="b6e79-164">Data block.</span></span> <span data-ttu-id="b6e79-165">При индексировании источника, как описано выше, добавляется альтернативный поток в PDB-файл с именем «srcsrv».</span><span class="sxs-lookup"><span data-stu-id="b6e79-165">Indexing the source as described previously adds an alternate stream to the PDB file named "srcsrv".</span></span> <span data-ttu-id="b6e79-166">Скрипт, который вставляет эти данные, зависит от конкретного процесса сборки и используемой системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="b6e79-166">The script that inserts this data is dependent on the specific build process and source control system in use.</span></span>

<span data-ttu-id="b6e79-167">В спецификации языка версии 1 блок данных разделен на три раздела: ini, Variables и Source Files.</span><span class="sxs-lookup"><span data-stu-id="b6e79-167">In the language specification version 1, the data block is divided into three sections: ini, variables, and source files.</span></span> <span data-ttu-id="b6e79-168">Он имеет следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="b6e79-168">It has the following syntax.</span></span>

``` syntax
SRCSRV: ini ------------------------------------------------ 
VERSION=1
VERCTRL=<source_control_str>
DATETIME=<date_time_str>
SRCSRV: variables ------------------------------------------ 
SRCSRVTRG=%sdtrg% 
SRCSRVCMD=%sdcmd% 
SRCSRVENV=var1=string1\bvar2=string2 
DEPOT=//depot 
SDCMD=sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%#%var4%
SDTRG=%targ%\%var2%\%fnbksl%(%var3%)\%var4%\%fnfile%(%var1%) 
WIN_SDKTOOLS= sserver.microsoft.com:4444 
SRCSRV: source files --------------------------------------- 
<path1>*<var2>*<var3>*<var4> 
<path2>*<var2>*<var3>*<var4> 
<path3>*<var2>*<var3>*<var4> 
<path4>*<var2>*<var3>*<var4> 
SRCSRV: end ------------------------------------------------
```

<span data-ttu-id="b6e79-169">Весь текст интерпретируется буквально, за исключением текста, заключенного в знаки процента (%).</span><span class="sxs-lookup"><span data-stu-id="b6e79-169">All text is interpreted literally, except for text enclosed in percent signs (%).</span></span> <span data-ttu-id="b6e79-170">Текст, заключенный в знаки процента, рассматривается как имя переменной для разрешения рекурсивно, если только это не одна из следующих функций:</span><span class="sxs-lookup"><span data-stu-id="b6e79-170">Text enclosed in percent signs is treated as a variable name to be resolved recursively, unless it is one of the following functions:</span></span>

<dl> <dt>

<span data-ttu-id="b6e79-171"><span id="_fnvar___"></span><span id="_FNVAR___"></span>% фнвар%()</span><span class="sxs-lookup"><span data-stu-id="b6e79-171"><span id="_fnvar___"></span><span id="_FNVAR___"></span>%fnvar%()</span></span>
</dt> <dd>

<span data-ttu-id="b6e79-172">Текст параметра должен быть заключен в знаки процента и обрабатываться как переменная для расширения.</span><span class="sxs-lookup"><span data-stu-id="b6e79-172">The parameter text should be enclosed in percent signs and treated as a variable to be expanded.</span></span>

</dd> <dt>

<span data-ttu-id="b6e79-173"><span id="_fnbksl___"></span><span id="_FNBKSL___"></span>% фнбксл%()</span><span class="sxs-lookup"><span data-stu-id="b6e79-173"><span id="_fnbksl___"></span><span id="_FNBKSL___"></span>%fnbksl%()</span></span>
</dt> <dd>

<span data-ttu-id="b6e79-174">Все косые черты (/) в тексте параметра должны быть заменены обратной косой чертой ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="b6e79-174">All forward slashes (/) in the parameter text should be replaced with backward slashes (\\).</span></span>

</dd> <dt>

<span data-ttu-id="b6e79-175"><span id="_fnfile___"></span><span id="_FNFILE___"></span>% фнфиле%()</span><span class="sxs-lookup"><span data-stu-id="b6e79-175"><span id="_fnfile___"></span><span id="_FNFILE___"></span>%fnfile%()</span></span>
</dt> <dd>

<span data-ttu-id="b6e79-176">Все сведения о пути в тексте параметра должны быть удалены, и останется только имя файла.</span><span class="sxs-lookup"><span data-stu-id="b6e79-176">All path information in the parameter text should be stripped out, leaving only the file name.</span></span>

</dd> </dl>

<span data-ttu-id="b6e79-177">В разделе ini содержатся переменные, описывающие требования.</span><span class="sxs-lookup"><span data-stu-id="b6e79-177">The ini section contains variables that describe the requirements.</span></span> <span data-ttu-id="b6e79-178">Скрипт индексирования может добавлять в этот раздел любое количество переменных.</span><span class="sxs-lookup"><span data-stu-id="b6e79-178">The indexing script can add any number of variables to this section.</span></span> <span data-ttu-id="b6e79-179">Ниже приведены примеры.</span><span class="sxs-lookup"><span data-stu-id="b6e79-179">The following are examples:</span></span>

<dl> <dt>

<span data-ttu-id="b6e79-180"><span id="VERSION"></span><span id="version"></span>Версия</span><span class="sxs-lookup"><span data-stu-id="b6e79-180"><span id="VERSION"></span><span id="version"></span>VERSION</span></span>
</dt> <dd>

<span data-ttu-id="b6e79-181">Версия спецификации языка.</span><span class="sxs-lookup"><span data-stu-id="b6e79-181">The language specification version.</span></span> <span data-ttu-id="b6e79-182">Это обязательная переменная.</span><span class="sxs-lookup"><span data-stu-id="b6e79-182">This variable is required.</span></span>

</dd> <dt>

<span data-ttu-id="b6e79-183"><span id="VERCTL"></span><span id="verctl"></span>верктл</span><span class="sxs-lookup"><span data-stu-id="b6e79-183"><span id="VERCTL"></span><span id="verctl"></span>VERCTL</span></span>
</dt> <dd>

<span data-ttu-id="b6e79-184">Строка, описывающая продукт системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="b6e79-184">A string that describes the source control product.</span></span> <span data-ttu-id="b6e79-185">Эта переменная является необязательной.</span><span class="sxs-lookup"><span data-stu-id="b6e79-185">This variable is optional.</span></span>

</dd> <dt>

<span data-ttu-id="b6e79-186"><span id="DATETIME"></span><span id="datetime"></span>DATETIME</span><span class="sxs-lookup"><span data-stu-id="b6e79-186"><span id="DATETIME"></span><span id="datetime"></span>DATETIME</span></span>
</dt> <dd>

<span data-ttu-id="b6e79-187">Строка, указывающая дату и время обработки PDB-файла.</span><span class="sxs-lookup"><span data-stu-id="b6e79-187">A string that indicates the date and time the PDB file was processed.</span></span> <span data-ttu-id="b6e79-188">Эта переменная является необязательной.</span><span class="sxs-lookup"><span data-stu-id="b6e79-188">This variable is optional.</span></span>

</dd> </dl>

<span data-ttu-id="b6e79-189">Раздел variables содержит переменные, описывающие извлечение файла из системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="b6e79-189">The variables section contains variables that describe how to extract a file from source control.</span></span> <span data-ttu-id="b6e79-190">Он также может использоваться для определения часто используемого текста в качестве переменных для уменьшения размера блока данных.</span><span class="sxs-lookup"><span data-stu-id="b6e79-190">It can also be used to define commonly used text as variables to reduce the size of the data block.</span></span>

<dl> <dt>

<span data-ttu-id="b6e79-191"><span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>срксрвтрг</span><span class="sxs-lookup"><span data-stu-id="b6e79-191"><span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>SRCSRVTRG</span></span>
</dt> <dd>

<span data-ttu-id="b6e79-192">Описывает, как создать целевой путь для извлеченного файла.</span><span class="sxs-lookup"><span data-stu-id="b6e79-192">Describes how to build the target path for the extracted file.</span></span> <span data-ttu-id="b6e79-193">Это обязательная переменная.</span><span class="sxs-lookup"><span data-stu-id="b6e79-193">This is a required variable.</span></span>

</dd> <dt>

<span data-ttu-id="b6e79-194"><span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>срксрвкмд</span><span class="sxs-lookup"><span data-stu-id="b6e79-194"><span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>SRCSRVCMD</span></span>
</dt> <dd>

<span data-ttu-id="b6e79-195">Описывает, как создать команду для извлечения файла из системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="b6e79-195">Describes how to build the command to extract the file from source control.</span></span> <span data-ttu-id="b6e79-196">Сюда входит имя исполняемого файла и параметры командной строки.</span><span class="sxs-lookup"><span data-stu-id="b6e79-196">This includes the name of the executable file and its command-line parameters.</span></span> <span data-ttu-id="b6e79-197">Это обязательная переменная.</span><span class="sxs-lookup"><span data-stu-id="b6e79-197">This is a required variable.</span></span>

</dd> <dt>

<span data-ttu-id="b6e79-198"><span id="SRCSRVENV"></span><span id="srcsrvenv"></span>срксрвенв</span><span class="sxs-lookup"><span data-stu-id="b6e79-198"><span id="SRCSRVENV"></span><span id="srcsrvenv"></span>SRCSRVENV</span></span>
</dt> <dd>

<span data-ttu-id="b6e79-199">Строка, в которой перечислены переменные среды, создаваемые при извлечении файлов.</span><span class="sxs-lookup"><span data-stu-id="b6e79-199">A string that lists environment variables to be created during the file extraction.</span></span> <span data-ttu-id="b6e79-200">Разделяйте несколько записей символом Backspace ( \\ b).</span><span class="sxs-lookup"><span data-stu-id="b6e79-200">Separate multiple entries with a backspace character (\\b).</span></span> <span data-ttu-id="b6e79-201">Это необязательная переменная.</span><span class="sxs-lookup"><span data-stu-id="b6e79-201">This is an optional variable.</span></span>

</dd> </dl>

<span data-ttu-id="b6e79-202">В разделе исходные файлы содержится запись для каждого индексируемого исходного файла.</span><span class="sxs-lookup"><span data-stu-id="b6e79-202">The source files section contains an entry for each source file that has been indexed.</span></span> <span data-ttu-id="b6e79-203">Содержимое каждой строки интерпретируется как переменные с именами VAR1, VAR2, VAR3 и т. д. до VAR10.</span><span class="sxs-lookup"><span data-stu-id="b6e79-203">The contents of each line are interpreted as variables with the names VAR1, VAR2, VAR3, and so on until VAR10.</span></span> <span data-ttu-id="b6e79-204">Переменные разделяются звездочками.</span><span class="sxs-lookup"><span data-stu-id="b6e79-204">The variables are separated by asterisks.</span></span> <span data-ttu-id="b6e79-205">Параметр VAR1 должен указывать полный путь к исходному файлу, как указано в других местах PDB-файла.</span><span class="sxs-lookup"><span data-stu-id="b6e79-205">VAR1 must specify the fully qualified path to the source file as listed elsewhere in the PDB file.</span></span> <span data-ttu-id="b6e79-206">Например, следующая строка:</span><span class="sxs-lookup"><span data-stu-id="b6e79-206">For example, the following line:</span></span>

``` syntax
c:\proj\src\file.cpp*TOOLS_PRJ*tools/mytool/src/file.cpp*3
```

<span data-ttu-id="b6e79-207">интерпретируется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b6e79-207">is interpreted as follows:</span></span>

``` syntax
VAR1=c:\proj\src\file.cpp
VAR2=TOOLS_PRJ
VAR3=tools/mytool/src/file.cpp
VAR4=3
```

<span data-ttu-id="b6e79-208">В этом примере VAR4 — номер версии.</span><span class="sxs-lookup"><span data-stu-id="b6e79-208">In this example, VAR4 is a version number.</span></span> <span data-ttu-id="b6e79-209">Однако большинство систем управления версиями поддерживают метки файлов таким образом, чтобы можно было восстановить исходное состояние для данной сборки.</span><span class="sxs-lookup"><span data-stu-id="b6e79-209">However, most source control systems support labeling files in such a way that the source state for a given build can be restored.</span></span> <span data-ttu-id="b6e79-210">Таким образом, можно также использовать метку для сборки.</span><span class="sxs-lookup"><span data-stu-id="b6e79-210">Therefore, you could alternately use the label for the build.</span></span> <span data-ttu-id="b6e79-211">Образец блока данных можно изменить, чтобы он содержал переменную, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="b6e79-211">The sample data block could be modified to contain a variable such as the following:</span></span>

``` syntax
LABEL=BUILD47
```

<span data-ttu-id="b6e79-212">Затем, предполагается, что система управления версиями использует знак @ для обозначения метки, можно изменить переменную СРКСРВКМД следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b6e79-212">Then, presuming the source control system uses the at sign (@) to indicate a label, you could modify the SRCSRVCMD variable as follows:</span></span>

<span data-ttu-id="b6e79-213">**sd.exe-p% фнвар%(% var2%) Print-o% срксрвтрг%-q% хранилище%/%var3% @% метка%**</span><span class="sxs-lookup"><span data-stu-id="b6e79-213">**sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%@%label%**</span></span>

## <a name="how-source-server-works"></a><span data-ttu-id="b6e79-214">Принцип работы сервера исходного кода</span><span class="sxs-lookup"><span data-stu-id="b6e79-214">How Source Server Works</span></span>

<span data-ttu-id="b6e79-215">Клиент исходного сервера реализуется в Symsrv.dll.</span><span class="sxs-lookup"><span data-stu-id="b6e79-215">The source server client is implemented in Symsrv.dll.</span></span> <span data-ttu-id="b6e79-216">Клиент не извлекает сведения непосредственно из PDB-файла; в нем используется обработчик символов, например, реализованный в Dbghelp.dll.</span><span class="sxs-lookup"><span data-stu-id="b6e79-216">The client does not extract information directly from the PDB file; it uses a symbol handler such as the one implemented in Dbghelp.dll.</span></span> <span data-ttu-id="b6e79-217">По сути, это подсистема подстановки рекурсивных переменных, которая создает командную строку, которую можно использовать для извлечения правильного исходного файла из системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="b6e79-217">It is essentially a recursive variable substitution engine that creates a command line that can be used to extract the proper source file from the source control system.</span></span> <span data-ttu-id="b6e79-218">Код не должен вызывать Symsrv.dll напрямую.</span><span class="sxs-lookup"><span data-stu-id="b6e79-218">Your code should not call Symsrv.dll directly.</span></span> <span data-ttu-id="b6e79-219">Чтобы интегрировать функциональные возможности в приложение, используйте функцию [**симжетсаурцефиле**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) .</span><span class="sxs-lookup"><span data-stu-id="b6e79-219">To integrate its functionality into your application, use the [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) function.</span></span>

<span data-ttu-id="b6e79-220">Первая версия исходного сервера работает следующим образом.</span><span class="sxs-lookup"><span data-stu-id="b6e79-220">The first version of source server works as follows.</span></span> <span data-ttu-id="b6e79-221">Это поведение может измениться в будущих версиях.</span><span class="sxs-lookup"><span data-stu-id="b6e79-221">This behavior may change in future versions.</span></span>

-   <span data-ttu-id="b6e79-222">Клиент вызывает функцию **срксрвинит** с целевым путем для использования в качестве основы для всех извлечений исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="b6e79-222">The client calls the **SrcSrvInit** function with the target path to be used as a base for all source file extractions.</span></span> <span data-ttu-id="b6e79-223">Этот путь сохраняется в переменной коне.</span><span class="sxs-lookup"><span data-stu-id="b6e79-223">It stores this path in the TARG variable.</span></span>
-   <span data-ttu-id="b6e79-224">Клиент извлекает поток SRCSRV из PDB-файла при загрузке модуля PDB и вызывает функцию **срксрвлоадмодуле** для передачи блока данных на исходный сервер.</span><span class="sxs-lookup"><span data-stu-id="b6e79-224">The client extracts the Srcsrv stream from the PDB when the module PDB is loaded and calls the **SrcSrvLoadModule** function to pass the data block to source server.</span></span>
-   <span data-ttu-id="b6e79-225">Когда DBGHELP извлекает исходный файл, клиент вызывает функцию **срксрвжетфиле** для получения исходных файлов из системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="b6e79-225">When Dbghelp retrieves a source file, the client calls the **SrcSrvGetFile** function to retrieve the source files from source control.</span></span>
-   <span data-ttu-id="b6e79-226">Исходный сервер выполняет поиск записи, соответствующей запрошенному файлу, в записи в блоке данных в файле исходного кода.</span><span class="sxs-lookup"><span data-stu-id="b6e79-226">Source server searches the source file entries in the data block for an entry that matches the requested file.</span></span> <span data-ttu-id="b6e79-227">Он заполняет параметр VAR1 на VAR *n* содержимым записи с исходным файлом.</span><span class="sxs-lookup"><span data-stu-id="b6e79-227">It fills VAR1 to VAR *n* with the contents of the source file entry.</span></span> <span data-ttu-id="b6e79-228">Затем она расширяет переменную СРКСРВТРГ, используя VAR1 для VAR *n*.</span><span class="sxs-lookup"><span data-stu-id="b6e79-228">Next, it expands the SRCSRVTRG variable using VAR1 to VAR *n*.</span></span> <span data-ttu-id="b6e79-229">Если файл уже находится в этом расположении, он возвращает расположение вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="b6e79-229">If the file is already in this location, it returns the location to the caller.</span></span> <span data-ttu-id="b6e79-230">В противном случае он расширяет переменную СРКСРВКМД для создания команды, необходимой для получения файла из системы управления версиями и его копирования в целевое расположение.</span><span class="sxs-lookup"><span data-stu-id="b6e79-230">Otherwise, it expands the SRCSRVCMD variable to build the command needed to retrieve the file from source control and copy it to the target location.</span></span> <span data-ttu-id="b6e79-231">Наконец, он выполняет эту команду.</span><span class="sxs-lookup"><span data-stu-id="b6e79-231">Finally, it executes this command.</span></span>

## <a name="creating-a-source-control-provider-module"></a><span data-ttu-id="b6e79-232">Создание модуля поставщика системы управления версиями</span><span class="sxs-lookup"><span data-stu-id="b6e79-232">Creating a Source Control Provider Module</span></span>

<span data-ttu-id="b6e79-233">Исходный сервер включает модули поставщика для Перфорце (p4.pm) и Visual Source Сейф (vss.pm).</span><span class="sxs-lookup"><span data-stu-id="b6e79-233">The source server includes provider modules for Perforce (p4.pm) and Visual Source Safe (vss.pm).</span></span> <span data-ttu-id="b6e79-234">Чтобы создать собственный модуль поставщика, необходимо реализовать следующий набор интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="b6e79-234">To create your own provider module, you must implement the following set of interfaces.</span></span>

<dl> <dt>

<span data-ttu-id="b6e79-235"><span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module:: Симплеусаже ()**</span><span class="sxs-lookup"><span data-stu-id="b6e79-235"><span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module::SimpleUsage()**</span></span>
</dt> <dd>

<span data-ttu-id="b6e79-236">Назначение. отображает сведения об использовании простых модулей в STDOUT.</span><span class="sxs-lookup"><span data-stu-id="b6e79-236">Purpose: Displays simple module usage information to STDOUT.</span></span>

<span data-ttu-id="b6e79-237">Параметры: нет</span><span class="sxs-lookup"><span data-stu-id="b6e79-237">Parameters: None</span></span>

<span data-ttu-id="b6e79-238">Возвращаемое значение: нет</span><span class="sxs-lookup"><span data-stu-id="b6e79-238">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="b6e79-239"><span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module:: Вербосеусаже ()**</span><span class="sxs-lookup"><span data-stu-id="b6e79-239"><span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module::VerboseUsage()**</span></span>
</dt> <dd>

<span data-ttu-id="b6e79-240">Назначение. отображает подробные сведения об использовании модуля в STDOUT.</span><span class="sxs-lookup"><span data-stu-id="b6e79-240">Purpose: Displays in-depth module usage information to STDOUT.</span></span>

<span data-ttu-id="b6e79-241">Параметры: нет</span><span class="sxs-lookup"><span data-stu-id="b6e79-241">Parameters: None</span></span>

<span data-ttu-id="b6e79-242">Возвращаемое значение: нет</span><span class="sxs-lookup"><span data-stu-id="b6e79-242">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="b6e79-243"><span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module:: New ( \@ коммандаргументс)**</span><span class="sxs-lookup"><span data-stu-id="b6e79-243"><span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module::new(\@CommandArguments)**</span></span>
</dt> <dd>

<span data-ttu-id="b6e79-244">Назначение. Инициализирует экземпляр модуля поставщика.</span><span class="sxs-lookup"><span data-stu-id="b6e79-244">Purpose: Initializes an instance of the provider module.</span></span>

<span data-ttu-id="b6e79-245">Parameters: все @ARGV аргументы, не распознаваемые SSIndex. cmd как общие аргументы.</span><span class="sxs-lookup"><span data-stu-id="b6e79-245">Parameters: All @ARGV arguments that were not recognized by SSIndex.cmd as being general arguments.</span></span>

<span data-ttu-id="b6e79-246">Возвращаемое значение: ссылка, которую можно использовать в последующих операциях.</span><span class="sxs-lookup"><span data-stu-id="b6e79-246">Return value: A reference that can be used in later operations.</span></span>

</dd> <dt>

<span data-ttu-id="b6e79-247"><span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref->Гасерфилеинформатион ($SourcePath, $ServerHashReference)**</span><span class="sxs-lookup"><span data-stu-id="b6e79-247"><span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref->GatherFileInformation($SourcePath, $ServerHashReference)**</span></span>
</dt> <dd>

<span data-ttu-id="b6e79-248">Назначение. позволяет модулю собирать требуемые исходные сведения об индексировании для каталога, указанного параметром $SourcePath.</span><span class="sxs-lookup"><span data-stu-id="b6e79-248">Purpose: Enables the module to gather the required source indexing information for the directory specified by the $SourcePath parameter.</span></span> <span data-ttu-id="b6e79-249">Модуль не должен считать, что эта запись будет вызываться только один раз для каждого экземпляра объекта, так как SSIndex. cmd может вызывать его несколько раз для разных путей.</span><span class="sxs-lookup"><span data-stu-id="b6e79-249">The module should not assume that this entry will be called only once for each object instance, as SSIndex.cmd may call it multiple times for different paths.</span></span>

<span data-ttu-id="b6e79-250">Параметры: (1) локальный каталог, содержащий индексируемый источник.</span><span class="sxs-lookup"><span data-stu-id="b6e79-250">Parameters: (1) The local directory containing the source to be indexed.</span></span> <span data-ttu-id="b6e79-251">(2) ссылка на хэш, содержащий все записи из указанного файла Srcsrv.ini.</span><span class="sxs-lookup"><span data-stu-id="b6e79-251">(2) A reference to a hash containing all of the entries from the specified Srcsrv.ini file.</span></span>

<span data-ttu-id="b6e79-252">Возвращаемое значение: нет</span><span class="sxs-lookup"><span data-stu-id="b6e79-252">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="b6e79-253"><span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $objref->FileInfo ($LocalFile)**</span><span class="sxs-lookup"><span data-stu-id="b6e79-253"><span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $objref->GetFileInfo($LocalFile)**</span></span>
</dt> <dd>

<span data-ttu-id="b6e79-254">Назначение. предоставляет необходимые сведения для извлечения одного конкретного файла из системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="b6e79-254">Purpose: Provides the necessary information to extract a single, specific file from the source control system.</span></span>

<span data-ttu-id="b6e79-255">Параметры: полное имя файла</span><span class="sxs-lookup"><span data-stu-id="b6e79-255">Parameters: A fully qualified file name</span></span>

<span data-ttu-id="b6e79-256">Возвращаемое значение: (1) хэш-ссылка на переменные, необходимые для интерпретации возвращаемого $FileEntry.</span><span class="sxs-lookup"><span data-stu-id="b6e79-256">Return value: (1) A hash reference of the variables necessary to interpret the returned $FileEntry.</span></span> <span data-ttu-id="b6e79-257">SSIndex. cmd кэширует эти переменные для каждого исходного файла, используемого одним файлом отладки, чтобы уменьшить объем данных, записываемых в поток исходного индекса.</span><span class="sxs-lookup"><span data-stu-id="b6e79-257">SSIndex.cmd caches these variables for every source file used by a single debug file to reduce the amount of information written to the source index stream.</span></span> <span data-ttu-id="b6e79-258">(2) запись файла, записываемого в поток исходного индекса, чтобы разрешить SrcSrv.dll извлечение этого файла из системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="b6e79-258">(2) The file entry to be written to the source index stream to allow SrcSrv.dll to extract this file from source control.</span></span> <span data-ttu-id="b6e79-259">Точный формат этой строки зависит от системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="b6e79-259">The exact format of this line is specific to the source control system.</span></span>

</dd> <dt>

<span data-ttu-id="b6e79-260"><span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName ()**</span><span class="sxs-lookup"><span data-stu-id="b6e79-260"><span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName()**</span></span>
</dt> <dd>

<span data-ttu-id="b6e79-261">Назначение. предоставляет описательную строку для обнаружения поставщика системы управления версиями для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="b6e79-261">Purpose: Provides a descriptive string to identify the source control provider to the end user.</span></span>

<span data-ttu-id="b6e79-262">Параметры: нет</span><span class="sxs-lookup"><span data-stu-id="b6e79-262">Parameters: None</span></span>

<span data-ttu-id="b6e79-263">Возвращаемое значение: описательное имя системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="b6e79-263">Return value: The descriptive name of the source control system.</span></span>

</dd> <dt>

<span data-ttu-id="b6e79-264"><span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->Саурцестреамвариаблес ()**</span><span class="sxs-lookup"><span data-stu-id="b6e79-264"><span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->SourceStreamVariables()**</span></span>
</dt> <dd>

<span data-ttu-id="b6e79-265">Назначение. позволяет поставщику системы управления версиями добавлять определенные переменные системы управления версиями в исходный поток для каждого файла отладки.</span><span class="sxs-lookup"><span data-stu-id="b6e79-265">Purpose: Enables the source control provider to add source control specific variables to the source stream for each debug file.</span></span> <span data-ttu-id="b6e79-266">В примерах модулей этот метод используется для записи требуемой \_ команды Extract и извлечения \_ целевых переменных.</span><span class="sxs-lookup"><span data-stu-id="b6e79-266">The sample modules use this method for writing the required EXTRACT\_CMD and EXTRACT\_TARGET variables.</span></span>

<span data-ttu-id="b6e79-267">Параметры: нет</span><span class="sxs-lookup"><span data-stu-id="b6e79-267">Parameters: None</span></span>

<span data-ttu-id="b6e79-268">Возвращаемое значение: список записей для переменных исходного потока.</span><span class="sxs-lookup"><span data-stu-id="b6e79-268">Return value: The list of entries for the source stream variables.</span></span>

</dd> </dl>

 

 




