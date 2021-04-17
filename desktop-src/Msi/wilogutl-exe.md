---
description: Wilogutl.exe помогает анализировать файлы журналов из установщик Windows установки и отображает предлагаемые решения для ошибок, обнаруженных в файле журнала.
ms.assetid: 09aa03ba-992f-47ab-999b-ebdfe85c1ea7
title: Wilogutl.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec81c3c82299a08fd947fbbecc7afd8a373252b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674492"
---
# <a name="wilogutlexe"></a><span data-ttu-id="e0c8a-103">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="e0c8a-103">Wilogutl.exe</span></span>

<span data-ttu-id="e0c8a-104">Wilogutl.exe помогает анализировать файлы журналов из установщик Windows установки и отображает предлагаемые решения для ошибок, обнаруженных в файле журнала.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-104">Wilogutl.exe assists the analysis of log files from a Windows Installer installation, and it displays suggested solutions to errors that are found in a log file.</span></span>

<span data-ttu-id="e0c8a-105">Некритические ошибки не отображаются.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-105">Non-critical errors are not displayed.</span></span> <span data-ttu-id="e0c8a-106">Wilogutl.exe можно запускать в тихом режиме или с помощью пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-106">Wilogutl.exe can be run in quiet mode or with a user interface (UI).</span></span> <span data-ttu-id="e0c8a-107">Средство создает отчеты в виде текстовых файлов как в пользовательском интерфейсе, так и в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-107">The tool generates reports as text files in both the UI and quiet modes.</span></span> <span data-ttu-id="e0c8a-108">Он лучше подходит для подробных установщик Windows файлов журналов, но также работает с журналами, не являющимися подробными.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-108">It works best with verbose Windows Installer log files, but also works with non-verbose logs.</span></span> <span data-ttu-id="e0c8a-109">Дополнительные сведения: [Ведение журналов](logging.md).</span><span class="sxs-lookup"><span data-stu-id="e0c8a-109">For more information, see [Logging](logging.md).</span></span>

<span data-ttu-id="e0c8a-110">Это средство доступно только в [компонентах Windows SDK для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="e0c8a-110">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e0c8a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0c8a-111">Syntax</span></span>

<span data-ttu-id="e0c8a-112">\**wilogutl.exe\*\*\*\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*</span><span class="sxs-lookup"><span data-stu-id="e0c8a-112">**wilogutl.exe** *\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*</span></span>

<span data-ttu-id="e0c8a-113">Для запуска в тихом режиме можно использовать следующие командные строки.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-113">You can use the following command lines to run in quiet mode.</span></span>

<span data-ttu-id="e0c8a-114">**вилогутл/q/l** *c: \\ мимсилог. log* **/o** *c \\ outputdir \\*</span><span class="sxs-lookup"><span data-stu-id="e0c8a-114">**wilogutl /q /l** *c:\\mymsilog.log* **/o** *c\\outputdir\\*</span></span>

<span data-ttu-id="e0c8a-115">**вилогутл/q/l** *c: \\ мимсилог. log*</span><span class="sxs-lookup"><span data-stu-id="e0c8a-115">**wilogutl /q /l** *c:\\mymsilog.log*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="e0c8a-116">Параметры командной строки</span><span class="sxs-lookup"><span data-stu-id="e0c8a-116">Command-Line Options</span></span>

<span data-ttu-id="e0c8a-117">Wilogutl.exe использует следующие параметры командной строки, не учитывающие регистр.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-117">Wilogutl.exe uses the following case insensitive command-line options.</span></span> <span data-ttu-id="e0c8a-118">Вместо косой черты можно использовать разделитель-тире.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-118">A dash delimiter can be used in place of a slash.</span></span>



| <span data-ttu-id="e0c8a-119">Параметр</span><span class="sxs-lookup"><span data-stu-id="e0c8a-119">Option</span></span> | <span data-ttu-id="e0c8a-120">Описание</span><span class="sxs-lookup"><span data-stu-id="e0c8a-120">Description</span></span>                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0c8a-121">нет</span><span class="sxs-lookup"><span data-stu-id="e0c8a-121">none</span></span>   | <span data-ttu-id="e0c8a-122">Выполняется в режиме пользовательского интерфейса без параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-122">Runs in UI mode—without command-line options.</span></span>                                                                                                                                                   |
| <span data-ttu-id="e0c8a-123">/q</span><span class="sxs-lookup"><span data-stu-id="e0c8a-123">/q</span></span>     | <span data-ttu-id="e0c8a-124">Указывает тихий режим.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-124">Specifies the quiet mode.</span></span> <span data-ttu-id="e0c8a-125">Wilogutl.exe создает файлы отчетов и не отображает пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-125">Wilogutl.exe generates report files and does not display a user interface.</span></span>                                                                                            |
| <span data-ttu-id="e0c8a-126">/l</span><span class="sxs-lookup"><span data-stu-id="e0c8a-126">/l</span></span>     | <span data-ttu-id="e0c8a-127">Указывает имя анализируемого файла журнала.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-127">Specifies the name of the log file to be analyzed.</span></span> <span data-ttu-id="e0c8a-128">Этот параметр является обязательным при работе в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-128">This option is required when using the quiet mode.</span></span>                                                                                           |
| <span data-ttu-id="e0c8a-129">/o</span><span class="sxs-lookup"><span data-stu-id="e0c8a-129">/o</span></span>     | <span data-ttu-id="e0c8a-130">Указывает выходной каталог для файлов отчетов.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-130">Specifies the output directory for report files.</span></span> <span data-ttu-id="e0c8a-131">Этот выходной путь используется только при работе в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-131">This output path is used only when running in quiet mode.</span></span> <span data-ttu-id="e0c8a-132">Если параметр не указан, отчеты помещаются в каталог C: \\ вилогресултс.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-132">If the option is not present, the reports are put in the C:\\WiLogResults directory.</span></span> |



 

<span data-ttu-id="e0c8a-133">При запуске в режиме пользовательского интерфейса Wilogutl.exe отображает следующие диалоговые окна.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-133">When run in UI mode, Wilogutl.exe displays the following dialog boxes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e0c8a-134">Имя</span><span class="sxs-lookup"><span data-stu-id="e0c8a-134">Name</span></span></th>
<th><span data-ttu-id="e0c8a-135">Описание</span><span class="sxs-lookup"><span data-stu-id="e0c8a-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e0c8a-136">установщик Windows подробный анализ журнала</span><span class="sxs-lookup"><span data-stu-id="e0c8a-136">Windows Installer Verbose Log Analyzer</span></span></td>
<td><span data-ttu-id="e0c8a-137">Диалоговое окно подробный анализ журнала установщик Windows позволяет пользователям выбрать файл журнала для анализа:</span><span class="sxs-lookup"><span data-stu-id="e0c8a-137">The Windows Installer Verbose Log Analyzer dialog box enables users to select a log file for analysis:</span></span>
<ul>
<li><span data-ttu-id="e0c8a-138">Кнопка <strong>Открыть</strong> открывает файл в блокноте.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-138">The <strong>Open</strong> button opens the file in Notepad.</span></span> <span data-ttu-id="e0c8a-139">Область предварительного просмотра можно использовать, чтобы убедиться, что выбран правильный файл журнала.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-139">The preview area can be used to verify that the correct log file has been selected.</span></span></li>
<li><span data-ttu-id="e0c8a-140">Кнопка « <strong>анализ</strong> » запускает анализ файла журнала и отображает диалоговое окно «подробное представление файла журнала».</span><span class="sxs-lookup"><span data-stu-id="e0c8a-140">The <strong>Analyze</strong> button begins log file analysis and displays the Detailed Log File View dialog box.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0c8a-141">Подробное представление файла журнала</span><span class="sxs-lookup"><span data-stu-id="e0c8a-141">Detailed Log File View</span></span></td>
<td><span data-ttu-id="e0c8a-142">В диалоговом окне подробный просмотр файла журнала отображаются сведения об ошибке в журнале.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-142">The Detailed Log File View dialog box displays logged error information.</span></span> <span data-ttu-id="e0c8a-143">Используйте кнопки <strong>назад</strong> и <strong>Далее</strong> для перемещения по нескольким ошибкам.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-143">Use the <strong>Back</strong> and <strong>Next</strong> buttons to navigate through multiple errors.</span></span> <span data-ttu-id="e0c8a-144">Чтобы отобразить некритические ошибки, установите флажок <strong>Показать пропущенные отладочные ошибки</strong> .</span><span class="sxs-lookup"><span data-stu-id="e0c8a-144">To display non-critical errors select the <strong>Show Ignored Debug Errors</strong> check box.</span></span> <span data-ttu-id="e0c8a-145">Отображается версия установщика на компьютере, используемом для запуска установленной в журнале установки.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-145">The installer version on the computer used to run the logged installation is displayed.</span></span> <span data-ttu-id="e0c8a-146">Если Записанная в журнал установка была запущена с повышенными разрешениями, флажок <strong>Установка с повышенными</strong> привилегиями установлен, а сведения содержатся в текстовых полях сведения о правах на стороне <strong>клиента</strong> и на <strong>стороне сервера</strong> .</span><span class="sxs-lookup"><span data-stu-id="e0c8a-146">If the logged installation was run with elevated permissions, the <strong>Elevated install</strong> check box is selected and information is provided in the <strong>Client Side Privilege Details</strong> and <strong>Server Side Privilege Details</strong> text boxes.</span></span> <span data-ttu-id="e0c8a-147">Диалоговое окно Подробный просмотр файла журнала содержит следующие кнопки.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-147">The Detailed Log File View dialog box contains the following buttons:</span></span><br/>
<ul>
<li><span data-ttu-id="e0c8a-148"><strong>Состояния</strong> - Отображение диалогового окна "состояния компонентов и компонентов".</span><span class="sxs-lookup"><span data-stu-id="e0c8a-148"><strong>States</strong> - Show the Feature and Component States dialog box.</span></span></li>
<li><span data-ttu-id="e0c8a-149"><strong>Свойства</strong> - Отображение диалогового окна «Свойства».</span><span class="sxs-lookup"><span data-stu-id="e0c8a-149"><strong>Properties</strong> - Show the Properties dialog box.</span></span></li>
<li><span data-ttu-id="e0c8a-150"><strong>Политики</strong> - Отображение диалогового окна политики.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-150"><strong>Policies</strong> - Show the Policies dialog box.</span></span></li>
<li><span data-ttu-id="e0c8a-151">Журнал с заметками <strong>HTML</strong> - Отображение журнала в виде HTML-файла с заметками.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-151"><strong>HTML Annotated Log</strong> - Show log as annotated HTML file.</span></span></li>
<li><span data-ttu-id="e0c8a-152"><strong>Сохранить результаты</strong> - Сохранение файлов отчетов в указанном каталоге.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-152"><strong>Save Results</strong> - Save report files to specified directory.</span></span></li>
<li><span data-ttu-id="e0c8a-153"><strong>Справка по</strong> - сообщению об ошибке Отображение справки по сообщениям об ошибках установщика.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-153"><strong>Error Message Help</strong> - Show installer error message help.</span></span></li>
<li><span data-ttu-id="e0c8a-154"><strong>Справка</strong> - Отображение справки по установщик Windows программе установки Log Analyzer.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-154"><strong>Help</strong> - Show help for Windows Installer Setup Log Analyzer.</span></span></li>
<li><span data-ttu-id="e0c8a-155"><strong>Чтение файла журнала</strong> - Отображение справочного документа по файлу журнала.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-155"><strong>How to Read a Log File</strong> - Show the log file help document.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0c8a-156">Состояния компонентов и компонентов</span><span class="sxs-lookup"><span data-stu-id="e0c8a-156">Feature and Component States</span></span></td>
<td><span data-ttu-id="e0c8a-157">В диалоговом окне <strong>состояния компонентов и компонентов</strong> отображаются состояния компонентов и компонентов.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-157">The <strong>Feature and Component States</strong> dialog box displays the states of features and components:</span></span>
<ul>
<li><span data-ttu-id="e0c8a-158">В столбце " <strong>компонент</strong> " отображается имя компонента в пакете установки.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-158">The <strong>Feature</strong> column shows the name for the feature in the installation package.</span></span></li>
<li><span data-ttu-id="e0c8a-159">В столбце <strong>Component (компонент</strong> ) отображается имя компонента в пакете установки.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-159">The <strong>Component</strong> column shows the name of the component in the installation package.</span></span></li>
<li><span data-ttu-id="e0c8a-160">В столбце <strong>установленные</strong> отображаются сведения о состоянии компонента или компонента в конце установки.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-160">The <strong>Installed</strong> column shows the feature or component's state at the end of the installation.</span></span></li>
<li><span data-ttu-id="e0c8a-161">В столбце <strong>запрос</strong> отображается выбор пользователя во время установки для состояния компонента или компонента.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-161">The <strong>Request</strong> column shows the user's selection during the installation for the feature or component's state.</span></span></li>
<li><span data-ttu-id="e0c8a-162">В столбце <strong>действие</strong> отображается действие, предпринимаемое установщиком для функции или компонента.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-162">The <strong>Action</strong> column shows the action taken by the installer for the feature or component.</span></span></li>
</ul>
<span data-ttu-id="e0c8a-163">Дополнительные сведения см. в разделе <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>мсижеткомпонентстате</strong></a> и <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>мсижетфеатурестате</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-163">For more information, see <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> and <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0c8a-164">Свойства</span><span class="sxs-lookup"><span data-stu-id="e0c8a-164">Properties</span></span></td>
<td><span data-ttu-id="e0c8a-165">В диалоговом окне Свойства отображаются установщик Windows <a href="properties.md">Свойства</a> и их значения в конце установки.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-165">The Properties dialog box shows Windows Installer <a href="properties.md">Properties</a> and their values at the end of the installation.</span></span> <span data-ttu-id="e0c8a-166">Свойства можно отсортировать по имени или по значению:</span><span class="sxs-lookup"><span data-stu-id="e0c8a-166">You can sort the properties by name or by value:</span></span>
<ul>
<li><span data-ttu-id="e0c8a-167">На вкладке <strong>клиент</strong> отображаются свойства и значения во время выполнения установки на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-167">The <strong>Client</strong> tab shows properties and values during the client side portion of the installation.</span></span></li>
<li><span data-ttu-id="e0c8a-168">На вкладке « <strong>сервер</strong> » отображаются свойства и значения во время серверной части установки.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-168">The <strong>Server</strong> tab shows properties and values during the server portion of the installation.</span></span></li>
<li><span data-ttu-id="e0c8a-169">На вкладке <strong>вложенные</strong> отображаются свойства и значения всех <a href="concurrent-installations.md">одновременных установок</a>.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-169">The <strong>Nested</strong> tab shows the properties and values of any <a href="concurrent-installations.md">Concurrent Installations</a>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0c8a-170">Политики</span><span class="sxs-lookup"><span data-stu-id="e0c8a-170">Policies</span></span></td>
<td><span data-ttu-id="e0c8a-171">В диалоговом окне политики отобразится <a href="system-policy.md">Системная политика</a> , установленная после установки.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-171">The Policies dialog box displays the <a href="system-policy.md">System Policy</a> set after the installation:</span></span>
<ul>
<li><span data-ttu-id="e0c8a-172">Значение 0 (нуль), установленное для политики, означает, что политика не включена.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-172">A value of 0 (zero) set for the policy means the policy is not enabled.</span></span></li>
<li><span data-ttu-id="e0c8a-173">Значение 1 (одно) означает, что политика включена.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-173">A value of 1 (one) means the policy is enabled.</span></span></li>
<li><span data-ttu-id="e0c8a-174">Значение?</span><span class="sxs-lookup"><span data-stu-id="e0c8a-174">A value of ?</span></span> <span data-ttu-id="e0c8a-175">(вопросительный знак) означает, что значение политики не записывается в журнал.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-175">(question mark) means the policy value is not recorded in the log.</span></span></li>
</ul>
<span data-ttu-id="e0c8a-176">Если требуется значение политики, которое отсутствует в журнале, попробуйте использовать Regedit.exe для проверки разделов реестра на компьютере, на котором произошел сбой установки.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-176">If you need a policy value that is not in the log, try using Regedit.exe to check the registry keys on the computer failing the installation.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="report-files"></a><span data-ttu-id="e0c8a-177">Файлы отчетов</span><span class="sxs-lookup"><span data-stu-id="e0c8a-177">Report Files</span></span>

<span data-ttu-id="e0c8a-178">При выполнении анализа в тихом режиме или нажатии кнопки **сохранить результаты** в диалоговом окне **Подробный просмотр представления файла журнала** средство установщик Windows Setup Analyzer создает три текстовых файла и файл журнала с заметками HTML.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-178">When performing a quiet mode analysis or clicking the **Save Results** button on the **Detailed Log File View** dialog, the Windows Installer Setup Analyzer tool generates three text files and an HTML annotated log file.</span></span>

<span data-ttu-id="e0c8a-179">В следующей таблице указаны имена и содержимое файлов отчетов.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-179">The following table identifies the names and contents in the report files.</span></span>



| <span data-ttu-id="e0c8a-180">Имя</span><span class="sxs-lookup"><span data-stu-id="e0c8a-180">Name</span></span>                      | <span data-ttu-id="e0c8a-181">Описание</span><span class="sxs-lookup"><span data-stu-id="e0c8a-181">Description</span></span>                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0c8a-182">LogFilename \_summary.txt</span><span class="sxs-lookup"><span data-stu-id="e0c8a-182">logfilename\_summary.txt</span></span>  | <span data-ttu-id="e0c8a-183">Обобщает файл журнала.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-183">Summarizes the log file.</span></span> <span data-ttu-id="e0c8a-184">Выводит сведения, отображаемые в диалоговом окне подробный просмотр файла журнала, и первая ошибка.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-184">Lists the information displayed by the Detailed Log File View dialog box and the first error.</span></span>         |
| <span data-ttu-id="e0c8a-185">LogFilename \_errors.txt</span><span class="sxs-lookup"><span data-stu-id="e0c8a-185">logfilename\_errors.txt</span></span>   | <span data-ttu-id="e0c8a-186">Определяет количество ошибок, ошибок и рекомендуемых решений.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-186">Identifies the number of errors, the errors, and recommended solutions.</span></span> <span data-ttu-id="e0c8a-187">В этом файле перечислены критические и некритические ошибки.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-187">This file lists both critical and non-critical errors.</span></span> |
| <span data-ttu-id="e0c8a-188">LogFilename \_policies.txt</span><span class="sxs-lookup"><span data-stu-id="e0c8a-188">logfilename\_policies.txt</span></span> | <span data-ttu-id="e0c8a-189">Определяет имена и значения политик, заданные в конце установки, как в диалоговом окне политики.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-189">Identifies the policy names and values set at the end of the installation as in the Policies dialog box.</span></span>                       |
| <span data-ttu-id="e0c8a-190">\_logfilename.htm сведений</span><span class="sxs-lookup"><span data-stu-id="e0c8a-190">details\_logfilename.htm</span></span>  | <span data-ttu-id="e0c8a-191">Журнал с заметками HTML с условными обозначениями для цветовой кодировки.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-191">An HTML annotated log with a legend for the color coding.</span></span>                                                                      |



 

## <a name="return-values"></a><span data-ttu-id="e0c8a-192">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e0c8a-192">Return Values</span></span>

<span data-ttu-id="e0c8a-193">Если для операций в тихом режиме передаются недопустимые аргументы командной строки, Wilogutl.exe не выполняет никаких действий и процесс возвращает одно из значений, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-193">If invalid command-line arguments are passed for quiet mode operations, Wilogutl.exe does nothing, and the process returns one of the values in the following table.</span></span>



| <span data-ttu-id="e0c8a-194">Значение</span><span class="sxs-lookup"><span data-stu-id="e0c8a-194">Value</span></span> | <span data-ttu-id="e0c8a-195">Значение</span><span class="sxs-lookup"><span data-stu-id="e0c8a-195">Meaning</span></span>                                                                 |
|-------|-------------------------------------------------------------------------|
| <span data-ttu-id="e0c8a-196">1</span><span class="sxs-lookup"><span data-stu-id="e0c8a-196">1</span></span>     | <span data-ttu-id="e0c8a-197">Указан неверный выходной каталог.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-197">Bad output directory is specified.</span></span>                                      |
| <span data-ttu-id="e0c8a-198">2</span><span class="sxs-lookup"><span data-stu-id="e0c8a-198">2</span></span>     | <span data-ttu-id="e0c8a-199">Указано неправильное имя файла журнала.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-199">Bad log file name is specified.</span></span>                                         |
| <span data-ttu-id="e0c8a-200">3</span><span class="sxs-lookup"><span data-stu-id="e0c8a-200">3</span></span>     | <span data-ttu-id="e0c8a-201">Передано/q, но в нем отсутствует необходимый параметр/l для имени файла журнала.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-201">Passed /q, but is missing the required switch /l for the log file name.</span></span> |
| <span data-ttu-id="e0c8a-202">4</span><span class="sxs-lookup"><span data-stu-id="e0c8a-202">4</span></span>     | <span data-ttu-id="e0c8a-203">Передано/l, но в нем отсутствует требуемый параметр/q для скрытого режима.</span><span class="sxs-lookup"><span data-stu-id="e0c8a-203">Passed /l, but is missing the required switch /q for quiet mode.</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e0c8a-204">См. также</span><span class="sxs-lookup"><span data-stu-id="e0c8a-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0c8a-205">Выпущенные версии, средства и распространяемые пакеты</span><span class="sxs-lookup"><span data-stu-id="e0c8a-205">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> <dt>

[<span data-ttu-id="e0c8a-206">Средства разработки установщик Windows</span><span class="sxs-lookup"><span data-stu-id="e0c8a-206">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> </dl>

 

 




