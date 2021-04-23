---
description: 'Всдкодежен имеет две функции: создание файлов конфигурации и создание исходного кода для клиентских и хостовых приложений WSDAPI.'
ms.assetid: 75f5071c-040b-4e65-a80e-e1fea63535b0
title: Синтаксис командной строки Всдкодежен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7db3afe9b13286833f8563c0cacb41919d77bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898518"
---
# <a name="wsdcodegen-command-line-syntax"></a><span data-ttu-id="61e20-103">Синтаксис командной строки Всдкодежен</span><span class="sxs-lookup"><span data-stu-id="61e20-103">WsdCodeGen Command Line Syntax</span></span>

<span data-ttu-id="61e20-104">Всдкодежен имеет две функции: создание файлов конфигурации и создание исходного кода для клиентских и хостовых приложений WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="61e20-104">WsdCodeGen has two functions: generating configuration files and generating source code for WSDAPI client and host applications.</span></span> <span data-ttu-id="61e20-105">В этом разделе приводится синтаксис командной строки, используемый для выполнения каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="61e20-105">This topic gives the command line syntax used to perform each task.</span></span>

## <a name="generating-a-configuration-file"></a><span data-ttu-id="61e20-106">Создание файла конфигурации</span><span class="sxs-lookup"><span data-stu-id="61e20-106">Generating a Configuration File</span></span>

### <a name="syntax"></a><span data-ttu-id="61e20-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61e20-107">Syntax</span></span>

<span data-ttu-id="61e20-108">**WSDCODEGEN.EXE** **/женератеконфиг:**{ \| **узел** клиента \| **ALL**} **\[ /аутпутфиле:**_конфигфиленаме_ *_\]_* *всдлфиленамелист*</span><span class="sxs-lookup"><span data-stu-id="61e20-108">**WSDCODEGEN.EXE** **/generateconfig:**{**client**\|**host**\|**all**} **\[/outputfile:**_ConfigFileName_*_\]_* *WSDLFileNameList*</span></span>

### <a name="parameters"></a><span data-ttu-id="61e20-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="61e20-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61e20-110"><span id="_generateconfig__client___host___all_"></span><span id="_GENERATECONFIG__CLIENT___HOST___ALL_"></span>**/женератеконфиг: { \| узел клиента \| все}**</span><span class="sxs-lookup"><span data-stu-id="61e20-110"><span id="_generateconfig__client___host___all_"></span><span id="_GENERATECONFIG__CLIENT___HOST___ALL_"></span>**/generateconfig:{client \| host \| all}**</span></span>
</dt> <dd>

<span data-ttu-id="61e20-111">Тип кода, который будет создан выходным файлом конфигурации.</span><span class="sxs-lookup"><span data-stu-id="61e20-111">The type of code that the output configuration file will generate.</span></span> <span data-ttu-id="61e20-112">**/женератеконфиг: Client** используется для создания файла конфигурации для создания кода клиента, **/женератеконфиг: Host** используется для создания файла конфигурации для создания кода узла, а **/женератеконфиг: ALL** используется для создания файла конфигурации для создания клиента и кода узла.</span><span class="sxs-lookup"><span data-stu-id="61e20-112">**/generateconfig:client** is used to generate a configuration file for generating client code, **/generateconfig:host** is used to generate a configuration file for generating host code, and **/generateconfig:all** is used to generate a configuration file for generating both client and host code.</span></span>

</dd> <dt>

<span data-ttu-id="61e20-113"><span id="_outputfile_ConfigFileName"></span><span id="_outputfile_configfilename"></span><span id="_OUTPUTFILE_CONFIGFILENAME"></span>**/аутпутфиле:**_конфигфиленаме_</span><span class="sxs-lookup"><span data-stu-id="61e20-113"><span id="_outputfile_ConfigFileName"></span><span id="_outputfile_configfilename"></span><span id="_OUTPUTFILE_CONFIGFILENAME"></span>**/outputfile:**_ConfigFileName_</span></span>
</dt> <dd>

<span data-ttu-id="61e20-114">Этот необязательный параметр используется для указания имени выходного файла конфигурации.</span><span class="sxs-lookup"><span data-stu-id="61e20-114">This optional parameter is used to specify the file name of the output configuration file.</span></span> <span data-ttu-id="61e20-115">Если этот параметр исключен, то имя выходного файла конфигурации будет codegen.config.</span><span class="sxs-lookup"><span data-stu-id="61e20-115">If this parameter is excluded, the name of the output configuration file is codegen.config.</span></span>

</dd> <dt>

<span data-ttu-id="61e20-116"><span id="_pnpx"></span><span id="_PNPX"></span>*/пнпкс*</span><span class="sxs-lookup"><span data-stu-id="61e20-116"><span id="_pnpx"></span><span id="_PNPX"></span>*/pnpx*</span></span>
</dt> <dd>

<span data-ttu-id="61e20-117">Включите шаблон PnP-X в файл конфигурации.</span><span class="sxs-lookup"><span data-stu-id="61e20-117">Include a PnP-X template in the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="61e20-118"><span id="WSDLFileNameList"></span><span id="wsdlfilenamelist"></span><span id="WSDLFILENAMELIST"></span>*всдлфиленамелист*</span><span class="sxs-lookup"><span data-stu-id="61e20-118"><span id="WSDLFileNameList"></span><span id="wsdlfilenamelist"></span><span id="WSDLFILENAMELIST"></span>*WSDLFileNameList*</span></span>
</dt> <dd>

<span data-ttu-id="61e20-119">Разделенный пробелами список WSDL-файлов, которые должны быть обработаны Всдкодежен.</span><span class="sxs-lookup"><span data-stu-id="61e20-119">A space-delimited list of the WSDL file(s) to be processed by WsdCodeGen.</span></span>

</dd> </dl>

## <a name="generating-source-code"></a><span data-ttu-id="61e20-120">Создание исходного кода</span><span class="sxs-lookup"><span data-stu-id="61e20-120">Generating Source Code</span></span>

### <a name="syntax"></a><span data-ttu-id="61e20-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61e20-121">Syntax</span></span>

<span data-ttu-id="61e20-122">**WSDCODEGEN.EXE** **/женератекоде** **\[ /download \]** **\[ /ГБК \]** **\[ аутпутрут:**_путь_ *_\]_* **\[ /вритеакцесс:**_Command_ *_\]_* *конфигфиленаме*</span><span class="sxs-lookup"><span data-stu-id="61e20-122">**WSDCODEGEN.EXE** **/generatecode** **\[/download\]** **\[/gbc\]** **\[outputroot:**_path_*_\]_* **\[/writeaccess:**_command_*_\]_* *ConfigFileName*</span></span>

### <a name="parameters"></a><span data-ttu-id="61e20-123">Параметры</span><span class="sxs-lookup"><span data-stu-id="61e20-123">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61e20-124"><span id="_generatecode"></span><span id="_GENERATECODE"></span>**/женератекоде**</span><span class="sxs-lookup"><span data-stu-id="61e20-124"><span id="_generatecode"></span><span id="_GENERATECODE"></span>**/generatecode**</span></span>
</dt> <dd>

<span data-ttu-id="61e20-125">Направляет Всдкодежен для создания исходного кода.</span><span class="sxs-lookup"><span data-stu-id="61e20-125">Directs WsdCodeGen to generate source code.</span></span> <span data-ttu-id="61e20-126">Этот режим используется по умолчанию, если режим не указан.</span><span class="sxs-lookup"><span data-stu-id="61e20-126">This is the default mode if no mode is specified.</span></span>

</dd> <dt>

<span data-ttu-id="61e20-127"><span id="_download"></span><span id="_DOWNLOAD"></span>**/Download**</span><span class="sxs-lookup"><span data-stu-id="61e20-127"><span id="_download"></span><span id="_DOWNLOAD"></span>**/download**</span></span>
</dt> <dd>

<span data-ttu-id="61e20-128">Скачивает импортированные документы, на которые ссылается файл конфигурации.</span><span class="sxs-lookup"><span data-stu-id="61e20-128">Downloads imported documents referenced by the configuration file.</span></span> <span data-ttu-id="61e20-129">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="61e20-129">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="61e20-130"><span id="_gbc"></span><span id="_GBC"></span>**/гбк**</span><span class="sxs-lookup"><span data-stu-id="61e20-130"><span id="_gbc"></span><span id="_GBC"></span>**/gbc**</span></span>
</dt> <dd>

<span data-ttu-id="61e20-131">Добавляет комментарии в исходный код, который указывает на созданный код.</span><span class="sxs-lookup"><span data-stu-id="61e20-131">Adds comments to the source code that indicates the code was generated.</span></span> <span data-ttu-id="61e20-132">Эти комментарии начинаются с фразы "создано".</span><span class="sxs-lookup"><span data-stu-id="61e20-132">These comments are prefixed with the phrase "Generated by".</span></span> <span data-ttu-id="61e20-133">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="61e20-133">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="61e20-134"><span id="_outputroot_path"></span><span id="_OUTPUTROOT_PATH"></span>**/аутпутрут:**_путь_</span><span class="sxs-lookup"><span data-stu-id="61e20-134"><span id="_outputroot_path"></span><span id="_OUTPUTROOT_PATH"></span>**/outputroot:**_path_</span></span>
</dt> <dd>

<span data-ttu-id="61e20-135">Расположение выходных данных для созданных файлов.</span><span class="sxs-lookup"><span data-stu-id="61e20-135">The output location for generated files.</span></span> <span data-ttu-id="61e20-136">*путь* может быть абсолютным или относительным путем.</span><span class="sxs-lookup"><span data-stu-id="61e20-136">*path* can be an absolute or relative path.</span></span> <span data-ttu-id="61e20-137">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="61e20-137">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="61e20-138"><span id="_writeaccess_command"></span><span id="_WRITEACCESS_COMMAND"></span>**/вритеакцесс:**_Command_</span><span class="sxs-lookup"><span data-stu-id="61e20-138"><span id="_writeaccess_command"></span><span id="_WRITEACCESS_COMMAND"></span>**/writeaccess:**_command_</span></span>
</dt> <dd>

<span data-ttu-id="61e20-139">Направляет Всдкодежен для выполнения указанной команды перед изменением существующих файлов на диске.</span><span class="sxs-lookup"><span data-stu-id="61e20-139">Directs WsdCodeGen to execute the specified command before it modifies any existing files on disk.</span></span> <span data-ttu-id="61e20-140">Выходные файлы, идентичные параметрам на диске, не будут получать эту команду и не будут записываться в.</span><span class="sxs-lookup"><span data-stu-id="61e20-140">Output files that are identical to those on disk will not receive this command, nor will they be written to.</span></span> <span data-ttu-id="61e20-141">Если команда содержит последовательность " {0} ", эта последовательность будет заменена именем изменяемого файла.</span><span class="sxs-lookup"><span data-stu-id="61e20-141">If the command contains the sequence "{0}", this sequence will be replaced with the filename of the file to be modified.</span></span> <span data-ttu-id="61e20-142">В противном случае имя файла будет добавлено к команде.</span><span class="sxs-lookup"><span data-stu-id="61e20-142">If not, the filename will be appended to the command.</span></span>

<span data-ttu-id="61e20-143">Примеры:</span><span class="sxs-lookup"><span data-stu-id="61e20-143">Examples:</span></span>

<span data-ttu-id="61e20-144">**/вритеакцесс: "attrib-r"**</span><span class="sxs-lookup"><span data-stu-id="61e20-144">**/writeaccess:"attrib -r"**</span></span>

<span data-ttu-id="61e20-145">**/вритеакцесс: "attrib-r {0} "**</span><span class="sxs-lookup"><span data-stu-id="61e20-145">**/writeaccess:"attrib -r {0}"**</span></span>

<span data-ttu-id="61e20-146">**/вритеакцесс: "Copy {0} .. \\ Резервное копирование \\ »**</span><span class="sxs-lookup"><span data-stu-id="61e20-146">**/writeaccess:"copy {0} ..\\backup\\"**</span></span>

</dd> <dt>

<span data-ttu-id="61e20-147"><span id="ConfigFileName"></span><span id="configfilename"></span><span id="CONFIGFILENAME"></span>*конфигфиленаме*</span><span class="sxs-lookup"><span data-stu-id="61e20-147"><span id="ConfigFileName"></span><span id="configfilename"></span><span id="CONFIGFILENAME"></span>*ConfigFileName*</span></span>
</dt> <dd>

<span data-ttu-id="61e20-148">Имя файла конфигурации для обработки перед созданием кода.</span><span class="sxs-lookup"><span data-stu-id="61e20-148">The name of the configuration file to process before generating code.</span></span>

</dd> </dl>

## <a name="formatting-legend"></a><span data-ttu-id="61e20-149">Условные обозначения форматирования</span><span class="sxs-lookup"><span data-stu-id="61e20-149">Formatting Legend</span></span>



| <span data-ttu-id="61e20-150">Формат</span><span class="sxs-lookup"><span data-stu-id="61e20-150">Format</span></span>                                                                    | <span data-ttu-id="61e20-151">Значение</span><span class="sxs-lookup"><span data-stu-id="61e20-151">Meaning</span></span>                                                 |
|---------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="61e20-152">*Наклонный*</span><span class="sxs-lookup"><span data-stu-id="61e20-152">*Italic*</span></span>                                                                  | <span data-ttu-id="61e20-153">Сведения, которые должен предоставить пользователь</span><span class="sxs-lookup"><span data-stu-id="61e20-153">Information that the user must provide</span></span>                  |
| <span data-ttu-id="61e20-154">**Полужирный**</span><span class="sxs-lookup"><span data-stu-id="61e20-154">**Bold**</span></span>                                                                  | <span data-ttu-id="61e20-155">Элементы, которые пользователь должен ввести в точности так, как показано</span><span class="sxs-lookup"><span data-stu-id="61e20-155">Elements that the user must type exactly as shown</span></span>       |
| <span data-ttu-id="61e20-156">Между скобками ( \[ \] )</span><span class="sxs-lookup"><span data-stu-id="61e20-156">Between brackets (\[\])</span></span>                                                   | <span data-ttu-id="61e20-157">Необязательные элементы</span><span class="sxs-lookup"><span data-stu-id="61e20-157">Optional items</span></span>                                          |
| <span data-ttu-id="61e20-158">Между фигурными скобками ( {} ); варианты, разделенные вертикальной чертой ( \| ).</span><span class="sxs-lookup"><span data-stu-id="61e20-158">Between braces ({}); choices separated by pipe (\|).</span></span> <span data-ttu-id="61e20-159">Пример: {четных и \| нечетных}</span><span class="sxs-lookup"><span data-stu-id="61e20-159">Example: {even\|odd}</span></span> | <span data-ttu-id="61e20-160">Набор вариантов, из которых пользователь должен выбрать только один</span><span class="sxs-lookup"><span data-stu-id="61e20-160">Set of choices from which the user must choose only one</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="61e20-161">Требования</span><span class="sxs-lookup"><span data-stu-id="61e20-161">Requirements</span></span>



| <span data-ttu-id="61e20-162">Требование</span><span class="sxs-lookup"><span data-stu-id="61e20-162">Requirement</span></span> | <span data-ttu-id="61e20-163">Значение</span><span class="sxs-lookup"><span data-stu-id="61e20-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="61e20-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61e20-164">Minimum supported client</span></span><br/> | <span data-ttu-id="61e20-165">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="61e20-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="61e20-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61e20-166">Minimum supported server</span></span><br/> | <span data-ttu-id="61e20-167">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="61e20-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="61e20-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61e20-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61e20-169">Файл конфигурации Всдкодежен</span><span class="sxs-lookup"><span data-stu-id="61e20-169">WsdCodeGen Configuration File</span></span>](wsdcodegen-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="61e20-170">Использование Всдкодежен</span><span class="sxs-lookup"><span data-stu-id="61e20-170">Using WsdCodeGen</span></span>](using-wsdcodegen.md)
</dt> </dl>

 

 




