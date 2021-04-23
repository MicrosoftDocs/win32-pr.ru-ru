---
description: В этом разделе объясняется, как создать пользовательский словарь для распознавания рукописного текста.
ms.assetid: 83abf534-740c-44a3-bbd4-babb54f2930e
title: Создание пользовательских словарей для распознавания рукописного текста в Windows 7 и Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80b9b7b5a1d9dfadddd83825aea7d6f676439999
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692115"
---
# <a name="creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="10b56-103">Создание пользовательских словарей для распознавания рукописного текста в Windows 7 и Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="10b56-103">Creating Custom Dictionaries for Handwriting Recognition in Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="10b56-104">В этом разделе объясняется, как создать пользовательский словарь для распознавания рукописного текста.</span><span class="sxs-lookup"><span data-stu-id="10b56-104">This section explains how to create a custom dictionary for handwriting recognition.</span></span>

<span data-ttu-id="10b56-105">В операционной системе Windows 7 и операционной системе Windows Server 2008 R2 точность распознавания рукописного текста может быть значительно улучшена за счет использования пользовательских словарей.</span><span class="sxs-lookup"><span data-stu-id="10b56-105">In the Windows 7 operating system and the Windows Server 2008 R2 operating system, the accuracy of handwriting recognition can be significantly improved through the use of custom dictionaries.</span></span> <span data-ttu-id="10b56-106">Эти словари дополняют или заменяют системные словари, используемые для рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="10b56-106">These dictionaries supplement or replace system dictionaries used for handwriting.</span></span> <span data-ttu-id="10b56-107">Поддержка распознавания рукописного текста обеспечивается с помощью функции службы рукописного ввода, которую необходимо включить с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="10b56-107">Support for handwriting recognition is provided through the Ink and Handwriting Services feature that needs to be enabled through Server Manager.</span></span>

> [!Note]  
> <span data-ttu-id="10b56-108">Пользовательские словари можно установить для языка, только если установлен распознаватель рукописного ввода для этого языка.</span><span class="sxs-lookup"><span data-stu-id="10b56-108">Custom dictionaries can be installed for a language only if the handwriting recognizer for that language is installed.</span></span>

 

<span data-ttu-id="10b56-109">Существует два основных шага настройки пользовательского словаря для рукописного ввода:</span><span class="sxs-lookup"><span data-stu-id="10b56-109">There are two basic steps to setting up a custom dictionary for handwriting:</span></span>

-   <span data-ttu-id="10b56-110">Скомпилируйте список слов.</span><span class="sxs-lookup"><span data-stu-id="10b56-110">Compile a word list.</span></span> <span data-ttu-id="10b56-111">Компиляция создает скомпилированный пользовательский словарь (хврдикт-файл).</span><span class="sxs-lookup"><span data-stu-id="10b56-111">The compilation creates a compiled custom dictionary (.hwrdict) file.</span></span>
-   <span data-ttu-id="10b56-112">Установите скомпилированный пользовательский словарь.</span><span class="sxs-lookup"><span data-stu-id="10b56-112">Install the compiled custom dictionary.</span></span>

## <a name="compiling-a-word-list"></a><span data-ttu-id="10b56-113">Компиляция списка слов</span><span class="sxs-lookup"><span data-stu-id="10b56-113">Compiling a Word List</span></span>

<span data-ttu-id="10b56-114">Список слов для компиляции должен быть в текстовом формате и должен быть сохранен с использованием кодировки Юникода.</span><span class="sxs-lookup"><span data-stu-id="10b56-114">The word list to be compiled must be in plain-text format and should be saved using a Unicode encoding.</span></span> <span data-ttu-id="10b56-115">Другие кодировки работать не будут.</span><span class="sxs-lookup"><span data-stu-id="10b56-115">Other encodings will not work.</span></span> <span data-ttu-id="10b56-116">Каждая строка текстового файла принимается в виде одной записи в словаре.</span><span class="sxs-lookup"><span data-stu-id="10b56-116">Each line of the text file is taken as a single entry in the dictionary.</span></span> <span data-ttu-id="10b56-117">Разрешены записи многословных единиц, содержащие один или несколько пробелов.</span><span class="sxs-lookup"><span data-stu-id="10b56-117">Multiword units entries containing one or more spaces are allowed.</span></span> <span data-ttu-id="10b56-118">Пробелы в начале или конце строки игнорируются.</span><span class="sxs-lookup"><span data-stu-id="10b56-118">Spaces at the beginning or end of a line are ignored.</span></span>

<span data-ttu-id="10b56-119">Пользовательский словарь компилируется из командной строки.</span><span class="sxs-lookup"><span data-stu-id="10b56-119">A custom dictionary is compiled from a command line.</span></span> <span data-ttu-id="10b56-120">Чтобы скомпилировать словарь, Откройте командное окно, перейдите к папке, содержащей список слов, и запустите HwrComp.exe с параметрами командной строки, которые необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="10b56-120">To compile a dictionary, open a command window, navigate to the folder containing the word list, and then run HwrComp.exe with the command-line options you want to use.</span></span>

<span data-ttu-id="10b56-121">В следующем примере показан синтаксис использования параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="10b56-121">The following example shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrcomp       [-lang <localename>] [-type <type>]
    [-comment <comment>]
    [-o <dictfile.hwrdict>]
    <inputfile>
     
```

### <a name="explanation-of-options"></a><span data-ttu-id="10b56-122">Объяснение параметров</span><span class="sxs-lookup"><span data-stu-id="10b56-122">Explanation of Options</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="10b56-123">Параметр</span><span class="sxs-lookup"><span data-stu-id="10b56-123">Parameter</span></span></th>
<th><span data-ttu-id="10b56-124">Описание</span><span class="sxs-lookup"><span data-stu-id="10b56-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10b56-125">-lang <localename></span><span class="sxs-lookup"><span data-stu-id="10b56-125">-lang <localename></span></span></td>
<td><span data-ttu-id="10b56-126">Указанное имя языкового стандарта, назначенное скомпилированному файлу пользовательского словаря.</span><span class="sxs-lookup"><span data-stu-id="10b56-126">The specified locale name assigned to the compiled custom dictionary file.</span></span> <span data-ttu-id="10b56-127">Аргумент <localename> имеет вид языкового региона.</span><span class="sxs-lookup"><span data-stu-id="10b56-127">The argument <localename> has the form language-REGION.</span></span> <span data-ttu-id="10b56-128">Примером этого является en-US, обозначающий английский язык в США регионе.</span><span class="sxs-lookup"><span data-stu-id="10b56-128">An example of this is en-US, which signifies the English language in the United States region.</span></span> <span data-ttu-id="10b56-129">Примеры этой формы см. в разделе [константы и строки идентификатора языка](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="10b56-129">For examples of this form, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span> <span data-ttu-id="10b56-130">Следующие языки поддерживаются для Windows 7 и Windows Server 2008 R2 с помощью этой функции: en-US, EN-GB, en-CA, en-AU, de-DE, de-CH, fr-FR, ES-ES, es-MX, ES-AR, ИТ-IT, nl-NL, NL-найдет, PT-BR, PT-PT, da-DK, SV-SE, NetBIOS-нет, nn-NO, Fi-FI, PL-PL, cs-CZ, ru-RU, RO-RO, SR-ЛАТН-CS, SR-Цирл-CS, CA-ES и HR-HR.</span><span class="sxs-lookup"><span data-stu-id="10b56-130">The following languages are supported for Windows 7 and Windows Server 2008 R2 by this feature: en-US, en-GB, en-CA, en-AU, de-DE, de-CH, fr-FR, es-ES, es-MX, es-AR, it-IT, nl-NL, nl-BE, pt-BR, pt-PT, da-DK, sv-SE, nb-NO, nn-NO, fi-FI, pl-PL, cs-CZ, ru-RU, ro-RO, sr-Latn-CS, sr-Cyrl-CS, ca-ES and hr-HR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10b56-131">-Тип <type></span><span class="sxs-lookup"><span data-stu-id="10b56-131">-type <type></span></span></td>
<td><span data-ttu-id="10b56-132">Аргумент Option <type> представляет собой однострочное объединение ресурса по использованию в качестве основного списка слов (первичного) или дополнения к главному списку слов (дополнительный), за которым следует фактическое имя списка слов, к которому применяется ресурс (например, словарь или фамилия).</span><span class="sxs-lookup"><span data-stu-id="10b56-132">The option argument <type> is a single-string concatenation of the resource's use as either the main word list (PRIMARY) or as a supplement to the main word list (SECONDARY) followed by the actual word list name to which the resource is applied (such as DICTIONARY or SURNAME).</span></span> <span data-ttu-id="10b56-133">Возможные следующие значения.</span><span class="sxs-lookup"><span data-stu-id="10b56-133">The following are possible values:</span></span>
<ul>
<li><span data-ttu-id="10b56-134">ОСНОВНОЙ-CITYNAME-СПИСОК</span><span class="sxs-lookup"><span data-stu-id="10b56-134">PRIMARY-CITYNAME-LIST</span></span></li>
<li><span data-ttu-id="10b56-135">ОСНОВНОЙ-COUNTRYNAME-СПИСОК</span><span class="sxs-lookup"><span data-stu-id="10b56-135">PRIMARY-COUNTRYNAME-LIST</span></span></li>
<li><span data-ttu-id="10b56-136">ОСНОВНОЙ-КАУНТРИШОРТНАМЕ-СПИСОК</span><span class="sxs-lookup"><span data-stu-id="10b56-136">PRIMARY-COUNTRYSHORTNAME-LIST</span></span></li>
<li><span data-ttu-id="10b56-137">ОСНОВНОЙ СЛОВАРЬ</span><span class="sxs-lookup"><span data-stu-id="10b56-137">PRIMARY-DICTIONARY</span></span></li>
<li><span data-ttu-id="10b56-138">ОСНОВНОЙ-GIVENNAME-СПИСОК</span><span class="sxs-lookup"><span data-stu-id="10b56-138">PRIMARY-GIVENNAME-LIST</span></span></li>
<li><span data-ttu-id="10b56-139">ОСНОВНОЙ-STATEORPROVINCE-СПИСОК</span><span class="sxs-lookup"><span data-stu-id="10b56-139">PRIMARY-STATEORPROVINCE-LIST</span></span></li>
<li><span data-ttu-id="10b56-140">ОСНОВНОЙ-СТРИТНАМЕ-СПИСОК</span><span class="sxs-lookup"><span data-stu-id="10b56-140">PRIMARY-STREETNAME-LIST</span></span></li>
<li><span data-ttu-id="10b56-141">СПИСОК "ОСНОВНОЙ-ФАМИЛИЯ"</span><span class="sxs-lookup"><span data-stu-id="10b56-141">PRIMARY-SURNAME-LIST</span></span></li>
<li><span data-ttu-id="10b56-142">ВТОРИЧНЫЙ CITYNAME-СПИСОК</span><span class="sxs-lookup"><span data-stu-id="10b56-142">SECONDARY-CITYNAME-LIST</span></span></li>
<li><span data-ttu-id="10b56-143">ВТОРИЧНЫЙ COUNTRYNAME-СПИСОК</span><span class="sxs-lookup"><span data-stu-id="10b56-143">SECONDARY-COUNTRYNAME-LIST</span></span></li>
<li><span data-ttu-id="10b56-144">ВТОРИЧНЫЙ КАУНТРИШОРТНАМЕ-СПИСОК</span><span class="sxs-lookup"><span data-stu-id="10b56-144">SECONDARY-COUNTRYSHORTNAME-LIST</span></span></li>
<li><span data-ttu-id="10b56-145">ВСПОМОГАТЕЛЬНЫЙ СЛОВАРЬ</span><span class="sxs-lookup"><span data-stu-id="10b56-145">SECONDARY-DICTIONARY</span></span></li>
<li><span data-ttu-id="10b56-146">ВТОРИЧНЫЙ ЕМАИЛСМТП-СПИСОК</span><span class="sxs-lookup"><span data-stu-id="10b56-146">SECONDARY-EMAILSMTP-LIST</span></span></li>
<li><span data-ttu-id="10b56-147">ВТОРИЧНЫЙ ЕМАИЛУСЕРНАМЕ-СПИСОК</span><span class="sxs-lookup"><span data-stu-id="10b56-147">SECONDARY-EMAILUSERNAME-LIST</span></span></li>
<li><span data-ttu-id="10b56-148">ВТОРИЧНЫЙ GIVENNAME-СПИСОК</span><span class="sxs-lookup"><span data-stu-id="10b56-148">SECONDARY-GIVENNAME-LIST</span></span></li>
<li><span data-ttu-id="10b56-149">ВТОРИЧНЫЙ STATEORPROVINCE-СПИСОК</span><span class="sxs-lookup"><span data-stu-id="10b56-149">SECONDARY-STATEORPROVINCE-LIST</span></span></li>
<li><span data-ttu-id="10b56-150">ВТОРИЧНЫЙ СТРИТНАМЕ-СПИСОК</span><span class="sxs-lookup"><span data-stu-id="10b56-150">SECONDARY-STREETNAME-LIST</span></span></li>
<li><span data-ttu-id="10b56-151">ДОПОЛНИТЕЛЬНЫЙ-ФАМИЛИЯ-СПИСОК</span><span class="sxs-lookup"><span data-stu-id="10b56-151">SECONDARY-SURNAME-LIST</span></span></li>
<li><span data-ttu-id="10b56-152">СПИСОК ВТОРИЧНЫХ URL-АДРЕСОВ</span><span class="sxs-lookup"><span data-stu-id="10b56-152">SECONDARY-URL-LIST</span></span></li>
</ul>
<span data-ttu-id="10b56-153">Если значение типа начинается с префикса PRIMARY, скомпилированный словарь после установки будет заменять системный словарь для этого языка.</span><span class="sxs-lookup"><span data-stu-id="10b56-153">If a type value starts with the prefix PRIMARY, the compiled dictionary, after it is installed, will replace the system dictionary for that language.</span></span> <span data-ttu-id="10b56-154">Значение "основной словарь" представляет основной системный словарь для языка.</span><span class="sxs-lookup"><span data-stu-id="10b56-154">The value PRIMARY-DICTIONARY represents the main system dictionary for a language.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="10b56-155">При замене системного словаря не выполняется никаких действий для исходного содержимого системного словаря, так как замена действует только до тех пор, пока не будет удален пользовательский словарь.</span><span class="sxs-lookup"><span data-stu-id="10b56-155">Replacing a system dictionary does nothing to the original system dictionary content, as the replacement is in effect only until the custom dictionary has been removed.</span></span>
</blockquote>
<br/> <span data-ttu-id="10b56-156">Если значение типа начинается с префикса ВТОРИЧной РЕПЛИКи, скомпилированный словарь будет дополнять системный словарь без его замены.</span><span class="sxs-lookup"><span data-stu-id="10b56-156">If a type value starts with the prefix SECONDARY, the compiled dictionary will supplement the system dictionary without replacing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10b56-157">-Комментарий</span><span class="sxs-lookup"><span data-stu-id="10b56-157">-comment</span></span> <comment></td>
<td><span data-ttu-id="10b56-158">Указанный комментарий компилируется в файл словаря.</span><span class="sxs-lookup"><span data-stu-id="10b56-158">The specified comment is compiled into the dictionary file.</span></span> <span data-ttu-id="10b56-159">Комментарий должен быть единственной строкой и содержать не более 64 символов.</span><span class="sxs-lookup"><span data-stu-id="10b56-159">The comment must be a single string and no longer than 64 characters.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10b56-160">-o <dictfile.hwrdict></span><span class="sxs-lookup"><span data-stu-id="10b56-160">-o <dictfile.hwrdict></span></span></td>
<td><span data-ttu-id="10b56-161">Выходные данные записываются в имя файла, заданное параметром <dictfile.hwrdict> .</span><span class="sxs-lookup"><span data-stu-id="10b56-161">Output is written to the file name specified by <dictfile.hwrdict>.</span></span><br/> <span data-ttu-id="10b56-162">Если этот параметр отсутствует, имя выходного файла берется из исходного имени входного файла, а расширение входного файла заменено на. хврдикт.</span><span class="sxs-lookup"><span data-stu-id="10b56-162">If this option is missing, the output file name is derived from the original input file name, with the input file extension replaced by .hwrdict.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="defaults"></a><span data-ttu-id="10b56-163">Умолчания;</span><span class="sxs-lookup"><span data-stu-id="10b56-163">Defaults</span></span>

<span data-ttu-id="10b56-164">Если параметры не указаны, используются значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="10b56-164">If no parameters are specified, the default option values are</span></span>

<span data-ttu-id="10b56-165">-lang <current input language> -тип вспомогательный словарь</span><span class="sxs-lookup"><span data-stu-id="10b56-165">-lang <current input language> -type SECONDARY-DICTIONARY</span></span>

### <a name="examples"></a><span data-ttu-id="10b56-166">Примеры</span><span class="sxs-lookup"><span data-stu-id="10b56-166">Examples</span></span>

<span data-ttu-id="10b56-167">Следующий код компилирует входной файл mylist1.txt, применяет значения параметров по умолчанию и создает выходной файл mylist1. хврдикт.</span><span class="sxs-lookup"><span data-stu-id="10b56-167">The following compiles the input file mylist1.txt, applies the default option values, and creates the output file mylist1.hwrdict.</span></span>

``` syntax
hwrcomp mylist1.txt
```

<span data-ttu-id="10b56-168">В отличие от этого, приведенный ниже код компилирует mylist1.txt в myrsrc1. хврдикт, но назначает "Английский (США)" (EN-US) в качестве языка и дополнительного СЛОВАРЯ в качестве типа.</span><span class="sxs-lookup"><span data-stu-id="10b56-168">In contrast, the following compiles mylist1.txt into myrsrc1.hwrdict, but assigns "English (US)" (en-US) as the language and SECONDARY-DICTIONARY as the type.</span></span>

``` syntax
hwrcomp -lang en-US -type SECONDARY-DICTIONARY -o myrsrc1 mylist1.txt 
```

## <a name="installing-a-compiled-custom-dictionary"></a><span data-ttu-id="10b56-169">Установка скомпилированного пользовательского словаря</span><span class="sxs-lookup"><span data-stu-id="10b56-169">Installing a Compiled Custom Dictionary</span></span>

<span data-ttu-id="10b56-170">HwrComp.exe создает файл хврдикт, который находится в двоичном формате, используемом распознавателем рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="10b56-170">HwrComp.exe creates a .hwrdict file, which is in a binary format usable by a handwriting recognizer.</span></span> <span data-ttu-id="10b56-171">Этот файл можно установить на любой компьютер под Windows 7 или Windows Server 2008 R2, поддерживающий распознавание рукописного текста.</span><span class="sxs-lookup"><span data-stu-id="10b56-171">This file can be installed on any computer running Windows 7 or Windows Server 2008 R2 that supports handwriting recognition.</span></span> <span data-ttu-id="10b56-172">Словарь устанавливается либо для текущего пользователя, либо для всех пользователей на компьютере.</span><span class="sxs-lookup"><span data-stu-id="10b56-172">A dictionary is installed either for just the current user or for all users on a machine.</span></span>

<span data-ttu-id="10b56-173">Скомпилированный файл пользовательского словаря можно установить из командной строки с помощью средства HwrReg.exe.</span><span class="sxs-lookup"><span data-stu-id="10b56-173">A compiled custom dictionary file can be installed from the command line using the tool HwrReg.exe.</span></span> <span data-ttu-id="10b56-174">Это средство полезно, если требуется переопределить некоторые значения конфигурации, которые либо компилируются в файл, либо значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="10b56-174">This tool is useful if you wish to override some of the configuration values that either are compiled into the file or are the default values.</span></span> <span data-ttu-id="10b56-175">HwrReg.exe можно выполнять двумя способами: в режиме проверки/установки и в режиме списка или удаления.</span><span class="sxs-lookup"><span data-stu-id="10b56-175">There are two ways to run HwrReg.exe: in check/install mode and in list/remove mode.</span></span>

### <a name="running-hwrregexe-in-checkinstall-mode"></a><span data-ttu-id="10b56-176">Выполнение HwrReg.exe в режиме проверки/установки</span><span class="sxs-lookup"><span data-stu-id="10b56-176">Running HwrReg.exe in Check/Install Mode</span></span>

<span data-ttu-id="10b56-177">Этот режим предназначен для файлов пользовательских словарей, которые еще не установлены.</span><span class="sxs-lookup"><span data-stu-id="10b56-177">This mode is for custom dictionary files that have not yet been installed.</span></span> <span data-ttu-id="10b56-178">Ниже приведен синтаксис использования параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="10b56-178">The following shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrreg        [-check]
    [-lang <localename>] 
    [-scope {all|me}]
    [-noprompt] 
    <dictfile.hwrdict>
```

### <a name="explanation-of-options"></a><span data-ttu-id="10b56-179">Объяснение параметров</span><span class="sxs-lookup"><span data-stu-id="10b56-179">Explanation of Options</span></span>



| <span data-ttu-id="10b56-180">Параметр</span><span class="sxs-lookup"><span data-stu-id="10b56-180">Parameter</span></span>                | <span data-ttu-id="10b56-181">Описание</span><span class="sxs-lookup"><span data-stu-id="10b56-181">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10b56-182">— Проверка</span><span class="sxs-lookup"><span data-stu-id="10b56-182">-check</span></span>                   | <span data-ttu-id="10b56-183">Файл словаря проверяется без установки.</span><span class="sxs-lookup"><span data-stu-id="10b56-183">The dictionary file is verified without being installed.</span></span> <span data-ttu-id="10b56-184">Параметр check позволяет отобразить комментарий файла и сведения о регистрации, которые будут использоваться для установки файла.</span><span class="sxs-lookup"><span data-stu-id="10b56-184">The  check option displays the file's comment, plus the registration information that would be used to install the file.</span></span> <span data-ttu-id="10b56-185">Этот параметр полезен для проверки сведений о регистрации до выполнения установки.</span><span class="sxs-lookup"><span data-stu-id="10b56-185">This option is useful for verifying registration information before the installation is performed.</span></span> <br/> <span data-ttu-id="10b56-186">Если этот параметр отсутствует, HwrReg.exe устанавливает пользовательский словарь.</span><span class="sxs-lookup"><span data-stu-id="10b56-186">If this option is missing, HwrReg.exe installs the custom dictionary.</span></span><br/>  |
|  <span data-ttu-id="10b56-187">lang <localename></span><span class="sxs-lookup"><span data-stu-id="10b56-187">lang <localename></span></span> | <span data-ttu-id="10b56-188">Файл словаря проверяется без установки.</span><span class="sxs-lookup"><span data-stu-id="10b56-188">The dictionary file is verified without being installed.</span></span> <span data-ttu-id="10b56-189">Параметр check позволяет отобразить комментарий файла и сведения о регистрации, которые будут использоваться для установки файла.</span><span class="sxs-lookup"><span data-stu-id="10b56-189">The  check option displays the file's comment, plus the registration information that would be used to install the file.</span></span> <span data-ttu-id="10b56-190">Этот параметр полезен для проверки сведений о регистрации до выполнения установки.</span><span class="sxs-lookup"><span data-stu-id="10b56-190">This option is useful for verifying registration information before the installation is performed.</span></span> <br/> <span data-ttu-id="10b56-191">Если этот параметр отсутствует, HwrReg.exe устанавливает пользовательский словарь.</span><span class="sxs-lookup"><span data-stu-id="10b56-191">If this option is missing, HwrReg.exe installs the custom dictionary.</span></span> <br/> |
|  <span data-ttu-id="10b56-192">область {все \| Me}</span><span class="sxs-lookup"><span data-stu-id="10b56-192">scope {all\|me}</span></span>         | <span data-ttu-id="10b56-193">Пользовательский словарь устанавливается либо для всех пользователей (область все), либо только для текущего пользователя (область Me).</span><span class="sxs-lookup"><span data-stu-id="10b56-193">The custom dictionary is installed either for all users ( scope all) or for just the current user ( scope me).</span></span> <span data-ttu-id="10b56-194">Для установки с областью ALL необходимо, чтобы команда была запущена в командной строке с повышенными привилегиями; в противном случае будет возвращен код ошибки.</span><span class="sxs-lookup"><span data-stu-id="10b56-194">Installing with  scope all requires the command to be run in an elevated command prompt; otherwise, an error code will be returned.</span></span> <br/> <span data-ttu-id="10b56-195">Если этот параметр отсутствует, установка ограничивается только текущим пользователем.</span><span class="sxs-lookup"><span data-stu-id="10b56-195">If this option is missing, the installation is scoped to just the current user.</span></span><br/>                          |
|  <span data-ttu-id="10b56-196">noprompt</span><span class="sxs-lookup"><span data-stu-id="10b56-196">noprompt</span></span>                | <span data-ttu-id="10b56-197">HwrReg.exe не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="10b56-197">HwrReg.exe does not prompt for confirmation.</span></span> <span data-ttu-id="10b56-198">Это может быть полезно при запуске hwrReg.exe из скрипта.</span><span class="sxs-lookup"><span data-stu-id="10b56-198">This can be useful when running hwrReg.exe from a script.</span></span> <br/>                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="10b56-199">В следующем примере выполняется установка пользовательского словаря myrsrc1. хврдикт для языка "Датский (Дания)" (da DK) с областью по умолчанию "только текущий пользователь".</span><span class="sxs-lookup"><span data-stu-id="10b56-199">The following example installs the custom dictionary myrsrc1.hwrdict for language "Danish (Denmark)" (da DK), with the default scope of just the current user.</span></span>

``` syntax
hwrreg -lang da-DK myrsrc1.hwrdict 
```

### <a name="running-hwrregexe-in-listremove-mode"></a><span data-ttu-id="10b56-200">Выполнение HwrReg.exe в режиме списка или удаления</span><span class="sxs-lookup"><span data-stu-id="10b56-200">Running HwrReg.exe in List/Remove Mode</span></span>

<span data-ttu-id="10b56-201">В этом режиме отображаются или удаляются установленные пользовательские словари.</span><span class="sxs-lookup"><span data-stu-id="10b56-201">This mode either lists or removes installed custom dictionaries.</span></span> <span data-ttu-id="10b56-202">Ниже приведен синтаксис использования параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="10b56-202">The following shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrreg        [-lang <localename>] 
    [-scope {all|me}] 
    [-type <type>]
    -list | -remove
```

### <a name="explanation-of-options"></a><span data-ttu-id="10b56-203">Объяснение параметров</span><span class="sxs-lookup"><span data-stu-id="10b56-203">Explanation of Options</span></span>



| <span data-ttu-id="10b56-204">Параметр</span><span class="sxs-lookup"><span data-stu-id="10b56-204">Parameter</span></span>                | <span data-ttu-id="10b56-205">Описание</span><span class="sxs-lookup"><span data-stu-id="10b56-205">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <span data-ttu-id="10b56-206">lang <localename></span><span class="sxs-lookup"><span data-stu-id="10b56-206">lang <localename></span></span> | <span data-ttu-id="10b56-207">Словари, зарегистрированные только для этого имени языкового стандарта, перечислены или удалены.</span><span class="sxs-lookup"><span data-stu-id="10b56-207">The dictionaries registered for only this locale name are listed or removed.</span></span> <span data-ttu-id="10b56-208">Аргумент <localename> имеет языковую область формы.</span><span class="sxs-lookup"><span data-stu-id="10b56-208">The argument <localename> has the form language REGION.</span></span> <span data-ttu-id="10b56-209">Примеры этой формы см. в разделе [константы и строки идентификатора языка](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="10b56-209">For examples of this form, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span> <br/> <span data-ttu-id="10b56-210">Если этот параметр отсутствует, будут перечислены или удалены словари для всех языков.</span><span class="sxs-lookup"><span data-stu-id="10b56-210">If this option is missing, dictionaries for all languages are listed or removed.</span></span><br/> |
|  <span data-ttu-id="10b56-211">область {все \| Me}</span><span class="sxs-lookup"><span data-stu-id="10b56-211">scope {all\|me}</span></span>         | <span data-ttu-id="10b56-212">Пользовательский словарь устанавливается либо для всех пользователей (область все), либо только для текущего пользователя (область Me).</span><span class="sxs-lookup"><span data-stu-id="10b56-212">The custom dictionary is installed either for all users ( scope all) or for just the current user ( scope me).</span></span> <span data-ttu-id="10b56-213">Для установки с областью ALL необходимо, чтобы команда была запущена в командной строке с повышенными привилегиями; в противном случае будет возвращен код ошибки.</span><span class="sxs-lookup"><span data-stu-id="10b56-213">Installing with  scope all requires the command to be run in an elevated command prompt; otherwise, an error code will be returned.</span></span> <br/> <span data-ttu-id="10b56-214">Если этот параметр отсутствует, установка ограничивается только текущим пользователем.</span><span class="sxs-lookup"><span data-stu-id="10b56-214">If this option is missing, the installation is scoped to just the current user.</span></span><br/>                      |
|  <span data-ttu-id="10b56-215">Тип <type></span><span class="sxs-lookup"><span data-stu-id="10b56-215">type <type></span></span>       | <span data-ttu-id="10b56-216">Выводит или удаляет только те словари, которые зарегистрированы в указанном типе.</span><span class="sxs-lookup"><span data-stu-id="10b56-216">Lists or removes only dictionaries that are registered with the specified type.</span></span><br/> <span data-ttu-id="10b56-217">Если этот параметр отсутствует, все типы словарей будут перечислены или удалены.</span><span class="sxs-lookup"><span data-stu-id="10b56-217">If this option is missing, all dictionary types are listed or removed.</span></span> <span data-ttu-id="10b56-218">Установка или удаление пользовательского словаря другого типа (например, основного COUNTRYNAME-списка) может повлиять на распознавание рукописного текста в других контекстах.</span><span class="sxs-lookup"><span data-stu-id="10b56-218">Installing or removing a custom dictionary of another type (such as PRIMARY-COUNTRYNAME-LIST) may affect handwriting recognition in other contexts.</span></span> <br/>                                              |
|  <span data-ttu-id="10b56-219">list</span><span class="sxs-lookup"><span data-stu-id="10b56-219">list</span></span>                    | <span data-ttu-id="10b56-220">Список всех установленных словарей, соответствующих другим параметрам.</span><span class="sxs-lookup"><span data-stu-id="10b56-220">Lists all installed dictionaries that match the other options.</span></span><br/> <span data-ttu-id="10b56-221">Если этот параметр отсутствует, необходимо указать параметр Remove.</span><span class="sxs-lookup"><span data-stu-id="10b56-221">If this option is missing, the option  remove must be specified.</span></span><br/>                                                                                                                                                                                                                          |
|  <span data-ttu-id="10b56-222">remove</span><span class="sxs-lookup"><span data-stu-id="10b56-222">remove</span></span>                  | <span data-ttu-id="10b56-223">Запрашивает удаление любого словаря, который соответствует другим параметрам.</span><span class="sxs-lookup"><span data-stu-id="10b56-223">Prompts for removal of any dictionary that matches the other options.</span></span><br/> <span data-ttu-id="10b56-224">Если этот параметр отсутствует, должен быть указан список параметров.</span><span class="sxs-lookup"><span data-stu-id="10b56-224">If this option is missing, the option  list must be specified.</span></span><br/>                                                                                                                                                                                                                     |



 

### <a name="examples"></a><span data-ttu-id="10b56-225">Примеры</span><span class="sxs-lookup"><span data-stu-id="10b56-225">Examples</span></span>

<span data-ttu-id="10b56-226">Ниже перечислены словари с языком «английский (США)» (EN US) и «основной словарь», которые устанавливаются только для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="10b56-226">The following lists dictionaries that have language "English (US)" (en US) and type PRIMARY DICTIONARY and that are installed for just the current user.</span></span>

``` syntax
hwrreg -list -lang en-US -type PRIMARY-DICTIONARY
                  
```

<span data-ttu-id="10b56-227">Аналогичным образом в следующем примере удаляются словари, соответствующие одному и тому же критерию.</span><span class="sxs-lookup"><span data-stu-id="10b56-227">Similarly, the following removes dictionaries that match the same criteria.</span></span>

``` syntax
hwrreg -remove -lang en-US -type PRIMARY-DICTIONARY
                  
```

## <a name="general-notes-on-custom-dictionaries"></a><span data-ttu-id="10b56-228">Общие замечания о пользовательских словарях</span><span class="sxs-lookup"><span data-stu-id="10b56-228">General Notes on Custom Dictionaries</span></span>

-   <span data-ttu-id="10b56-229">При установке двух пользовательских словарей, имеющих одинаковый тип, язык и область, вторая установка перезапишет первую.</span><span class="sxs-lookup"><span data-stu-id="10b56-229">If you install two custom dictionaries that have the same type, language, and scope, the second installation will overwrite the first.</span></span>
-   <span data-ttu-id="10b56-230">Если установить два пользовательских словаря с одинаковым типом и языком, но с разными областями (один для всех пользователей и один для текущего пользователя), словарь, установленный для текущего пользователя, имеет приоритет, и словарь, установленный для всех пользователей, игнорируется.</span><span class="sxs-lookup"><span data-stu-id="10b56-230">If you install two custom dictionaries with the same type and language, but with different scopes (one for all users, and one for the current user), the dictionary installed for the current user takes precedence, and the dictionary installed for all users is ignored.</span></span>

 

