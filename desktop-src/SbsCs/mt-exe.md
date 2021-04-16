---
description: Файл Mt.exe — это средство, создающее подписанные файлы и каталоги. Он доступен в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows. Mt.exe требует, чтобы файл, указанный в манифесте, присутствовал в том же каталоге, что и манифест.
ms.assetid: 37f010ee-2658-4547-9871-c913201042de
title: Mt.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df654a943bad272a091dc6ac20cc1dcdab1731a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650470"
---
# <a name="mtexe"></a>Mt.exe

Файл Mt.exe — это средство, создающее подписанные файлы и каталоги. Он доступен в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows. Mt.exe требует, чтобы файл, указанный в манифесте, присутствовал в том же каталоге, что и манифест.

Mt.exe создает хэши, используя реализацию CryptoAPI алгоритма безопасного хэширования (SHA-1). Дополнительные сведения о хэш-алгоритмах см. в разделе [алгоритмы хэширования и подписи](/windows/desktop/SecCrypto/hash-and-signature-algorithms). Хэши вставляются в теги **файла** в манифесте в виде шестнадцатеричной строки. В настоящее время средство создает только хэши SHA-1, хотя файлы в манифестах могут использовать другие схемы хэширования.

Mt.exe использует Makecat.exe для создания файлов каталога (. cat) из файлов определения каталога (. CDF). Это средство заполняет стандартный шаблон CDF именем и расположением манифеста. Его можно использовать с Makecat.exe для создания каталога сборок.

Версия Mt.exe, предоставляемая в последних версиях Windows SDK, также может использоваться для создания манифестов для управляемых сборок и неуправляемых параллельных сборок.

## <a name="syntax"></a>Синтаксис

**mt.exe \[ -manifest** _<Component1. manifest><component2. манифест>_ *_\] \[ -Identity:_* *<identity string> * **\] \[ -RGS:** _<файл1. RGS>_* _\] \[ -tlb:_ *_<file2. tlb>_* _\] \[ -DLL:_ *_<file3.dll>_* _\] \[ -Places:_ - *_<XML filename>_* _\] \[ манажедассемблинаме:_ *_<managed assembly>_* _\] \[ -No dependency \] \[ -Category- \] \[ out_ : *_<output manifest name>_* _\] \[ -инпутресаурце:_ *_<file4>_* _; \[ \# \]_ *_><0 \_ идентификатор ресурса><1_* _\] \[ -аутпутресаурце:_ *_<file5>_* _\[ \# ; \]_ *_><2 \_ идентификатор ресурса><3_* _\] \[ -—:_ *_<file6>_* _\[ \# ; \]_ *_><4 Resource \_ ID><5_* _\] \[ -хашупдате \[ :_ *_<path to files>_* _\] \] \[ -макекдфс \] \[ -проверять \_ Манифест \] \[ — проверять \_ \_ хэши файлов:_ *_<path to files>_* _\] \[ -канонизировать \] \[ — проверять \_ наличие \_ дубликатов \] \[ -нелоготипов \] \[ -verbose \]_*

## <a name="command-line-options"></a>Параметры командной строки

В Mt.exe используются следующие параметры командной строки без учета регистра.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Параметр</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-manifest</td>
<td>Указывает имя файла манифеста. Чтобы изменить один манифест, укажите имя файла манифеста. Например, Component. manifest.<br/> Чтобы объединить несколько манифестов, укажите здесь имена исходных манифестов. Укажите имя обновленного манифеста с помощью параметров <strong>-out</strong>, <strong>-аутпутресаурце</strong>или <strong>-—</strong> . Например, следующая командная строка запрашивает операцию, которая объединяет два манифеста, man1. manifest и man2. manifest, в новый манифест, man3. manifest.<br/> <strong>mt.exe-manifest man1. манифест man2. manifest-out: man3. manifest</strong><br/>
<blockquote>
[!Note]<br />
Без двоеточия (:) параметр является обязательным при использовании параметра <strong>-manifest</strong> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>— Identity</td>
<td>Предоставляет значения атрибутов элемента <strong>assemblyIdentity</strong> манифеста. Аргументом параметра <strong>-Identity</strong> является строковое значение, содержащее значения атрибутов в полях, разделенных запятыми. Укажите значение атрибута <strong>Name</strong> в первом поле без включения &quot; имени = &quot; подстроки. Все оставшиеся поля задают атрибуты и их значения в виде: <em> <attribute name> </em> = <em> <attribute_value> </em> .<br/> Например, чтобы обновить элемент <strong>assemblyIdentity</strong> манифеста со следующими сведениями:<br/> <assemblyIdentity type=&quot;win32&quot; name=&quot;Microsoft.Windows.SampleAssembly&quot; version=&quot;6.0.0.0&quot; processorArchitecture=&quot;x86&quot; publicKeyToken=&quot;a5aaf5ba15723d5&quot;/> <br/> Включите в командную строку параметр следующего <strong>идентификатора</strong> :<br/> <strong>— Identity:</strong> &quot; Microsoft. Windows. Самплеассембли, processorArchitecture = x86, Version = 6.0.0.0, Type = Win32, publicKeyToken = a5aaf5ba15723d5&quot;<br/></td>
</tr>
<tr class="odd">
<td>-RGS</td>
<td>Указывает имя файла скрипта регистрации (RGS). Параметр <strong>-DLL</strong> требуется для использования параметра <strong>-RGS</strong> .<br/></td>
</tr>
<tr class="even">
<td>-TLB</td>
<td>Задает имя файла библиотеки типов (TLB-файла). Параметр <strong>-DLL</strong> необходим для использования параметра <strong>-tlb</strong> .<br/></td>
</tr>
<tr class="odd">
<td>-DLL</td>
<td>Указывает имя файла библиотеки динамической компоновки (DLL). Параметр <strong>-DLL</strong> является обязательным для <strong>mt.exe</strong> , если используются параметры <strong>-RGS</strong> или <strong>-tlb</strong> . Укажите имя библиотеки DLL, которая будет построена в конечном итоге из файлов. RGS или. tlb.<br/> Например, следующая команда запрашивает операцию, создающую манифест из RGS-и TLB-файлов.<br/> <strong>mt.exe-RGS: testreg1. RGS-tlb: testlib1. tlb -dll:test.dll-Places: представитель. manifest — Identity: &quot; Microsoft. Windows. самплеассембли, processorArchitecture = x86, версия = 6.0.0.0, Type = Win32, PublicKeyToken = a5aaf5ba15723d5 &quot; -out: ргстлб. manifest</strong><br/></td>
</tr>
<tr class="even">
<td>-замены</td>
<td>Указывает файл, содержащий значения для заменяемой строки в RGS файле.<br/></td>
</tr>
<tr class="odd">
<td>-манажедассемблинаме</td>
<td>Создает манифест из указанной управляемой сборки. Используйте с параметром <strong>-undependency</strong> для создания манифеста без элементов зависимостей. Используйте с параметром <strong>-Category</strong> для создания манифеста с тегами категорий. Например, если managed.dll является управляемой сборкой, приведенная ниже Командная строка создает manifest-манифест из managed.dll.<br/> <strong>mt.exe -managedassemblyname:managed.dll: out. manifest</strong> <br/></td>
</tr>
<tr class="even">
<td>-dependency</td>
<td>Указывает операцию, которая создает манифест без элементов зависимостей. Для параметра <strong>-undependency</strong> требуется параметр <strong>-манажедассемблинаме</strong> . Например, если managed.dll является управляемой сборкой, следующая командная строка создает манифест out. manifest из managed.dll без сведений о зависимостях.<br/> <strong>mt.exe -managedassemblyname:managed.dll: out. manifest-undependency</strong><br/></td>
</tr>
<tr class="odd">
<td>— Категория</td>
<td>Указывает операцию, которая создает манифест с тегами категорий. Для параметра <strong>-Category</strong> требуется параметр <strong>-манажедассемблинаме</strong> . Например, если managed.dll является управляемой сборкой, следующая командная строка создает манифест out. manifest из managed.dll с тегами категорий.<br/> <strong>mt.exe -managedassemblyname:managed.dll: out. manifest — Категория</strong><br/></td>
</tr>
<tr class="even">
<td>-nologo</td>
<td>Указывает операцию, выполняемую без отображения стандартных данных об авторских правах Майкрософт. Если <strong>mt.exe</strong> выполняется как часть процесса сборки, этот параметр можно использовать, чтобы предотвратить запись нежелательной информации в файлы журнала. <br/></td>
</tr>
<tr class="odd">
<td>-out</td>
<td>Указывает имя обновленного манифеста. Если это операция с одним манифестом, а параметр <strong>-out</strong> не указан, Исходный манифест изменяется. <br/></td>
</tr>
<tr class="even">
<td>-инпутресаурце</td>
<td>Указывает операцию, выполняемую с манифестом, полученным из ресурса типа RT_MANIFEST. Если параметр <strong>-инпутресаурце</strong> используется без указания идентификатора ресурса, <em> <resource_id> </em> то операция использует значение CREATEPROCESS_MANIFEST_RESOURCE. <br/> Например, следующая команда запрашивает операцию, которая объединяет манифест из библиотеки DLL, dll_with_manifest.dll и файла манифеста man2. manifest. Объединенные манифесты получаются манифестом в файле ресурсов другой библиотеки DLL, dll_with_merged_manifests. <br/> <strong>mt.exe -inputresource:dll_with_manifest.dll; #1-manifest man2. manifest -outputresource:dll_with_merged_manifest.dll; #3</strong><br/> Чтобы извлечь манифест из библиотеки DLL, укажите имя файла DLL. Например, следующая команда извлекает манифест из lib1.dll и man3. manifest получает извлеченный манифест.<br/> <strong>mt.exe -inputresource:lib.dll; #1-out: man3. manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-аутпутресаурце</td>
<td>Указывает операцию, которая создает манифест для получения ресурсом типа RT_MANIFEST. Если параметр <strong>-аутпутресаурце</strong> используется без указания идентификатора ресурса, <em> <resource_id> </em> то операция использует значение CREATEPROCESS_MANIFEST_RESOURCE. <br/></td>
</tr>
<tr class="even">
<td>-—</td>
<td>Указывает операцию, эквивалентную использованию параметров <strong>-инпутресаурце</strong> и <strong>-аутпутресаурце</strong> с идентичными аргументами. Например, следующая команда запрашивает операцию, которая выполняет вычисление хэша файлов по указанному пути, и обновляет манифест ресурса переносимого исполняемого файла (PE).<br/> <strong>mt.exe -updateresource:dll_with_manifest.dll; #1-хашупдате: f: \филес</strong>.<br/></td>
</tr>
<tr class="odd">
<td>-хашупдате</td>
<td>Выполняет вычисление хэш-значения файлов по указанным путям и обновляет значение атрибута <strong>hash</strong> элемента <strong>File</strong> с помощью этого значения. <br/> Например, следующая команда запрашивает операцию, которая объединяет два файла манифеста, man1. manifest и man2. manifest, и обновляет значение атрибута <strong>hash</strong> элемента <strong>File</strong> в манифесте, который получает объединенные сведения, Объединенные. manifest.<br/> <strong>mt.exe-manifest man1. манифест man2. manifest-хашупдате: d: \филерепоситори-out: Merged. manifest</strong><br/> Если пути к файлам не указаны, операция ищет расположение манифеста, указанного для получения обновления. Например, следующая команда запрашивает операцию, которая выполняет вычисление обновленного хэш-значения с помощью файлов, найденных путем поиска в расположении обновленного файла. manifest.<br/> <strong>mt.exe-manifest Йоуркомпонент. manifest-хашупдате: Обновлено. manifest</strong><br/></td>
</tr>
<tr class="even">
<td>— validate_manifest</td>
<td>Задает операцию, которая выполняет проверку синтаксиса соответствия манифеста со схемой манифеста. Например, следующая команда запрашивает проверку соответствия man1. manifest со схемой. <br/> <strong>mt.exe манифест man1. manifest — validate_manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>— validate_file_hashes</td>
<td>Задает операцию, которая проверяет хэш-значения <strong>файловых</strong> элементов манифеста. Например, следующая команда запрашивает операцию, которая проверяет хэш-значения всех элементов <strong>file файла</strong> man1. manifest.<br/> <strong>mt.exe-manifest man1. manifest-validate_file_hashes: &quot; c; \филес&quot;</strong><br/></td>
</tr>
<tr class="even">
<td>-канонизировать</td>
<td>Указывает операцию обновления манифеста до канонической формы. Например, следующая команда обновляет man1. manifest до канонической формы.<br/> <strong>mt.exe манифест man1. manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>— check_for_duplicates</td>
<td>Указывает операцию, которая проверяет манифест на наличие повторяющихся элементов. Например, следующая команда проверяет man1. manifest на наличие повторяющихся элементов.<br/> <strong>mt.exe-man1. manifest — check_for_duplicates</strong><br/></td>
</tr>
<tr class="even">
<td>-макекдфс</td>
<td>Создает файлы. CDF для создания каталогов. Например, следующая команда запрашивает операцию, которая обновляет значение хэша и создает CDF-файл.<br/> <strong>mt.exe-manifest comp1. manifest-хашупдате-макекдфс: updated. manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-verbose</td>
<td>Отображает подробные сведения об отладке.</td>
</tr>
<tr class="even">
<td>-?</td>
<td>При запуске с-?, или без параметров и аргументов Mt.exe выводит текст справки.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Средства разработки параллельных сборок](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

