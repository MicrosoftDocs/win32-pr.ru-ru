---
description: Компилятор SNMP запускается в режиме командной строки в виде одного исполняемого файла.
ms.assetid: 0e85fe84-dacb-4720-8242-ffa0046780f3
ms.tgt_platform: multiple
title: smi2smir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e1d757293b5ee128f2ce1bc2bd5ec8479d9b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272571"
---
# <a name="smi2smir"></a><span data-ttu-id="a3e40-103">smi2smir</span><span class="sxs-lookup"><span data-stu-id="a3e40-103">smi2smir</span></span>

<span data-ttu-id="a3e40-104">Компилятор SNMP запускается в режиме командной строки в виде одного исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="a3e40-104">The SNMP compiler runs as a single executable file in the command-line mode.</span></span> <span data-ttu-id="a3e40-105">Компилятор принимает один модуль SNMP Information в качестве входных данных и принимает все дополнительные модули, необходимые для разрешения внешних ссылок.</span><span class="sxs-lookup"><span data-stu-id="a3e40-105">The compiler accepts one SNMP information module as input, and accepts any additional modules necessary to resolve external references.</span></span> <span data-ttu-id="a3e40-106">Используйте один из следующих примеров синтаксиса командной строки.</span><span class="sxs-lookup"><span data-stu-id="a3e40-106">Use one of the following command-line syntax examples.</span></span>

<span data-ttu-id="a3e40-107">Дополнительные сведения о том, когда используется этот компилятор, см. [в разделе Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="a3e40-107">For more information about when this compiler is used, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

``` syntax
smi2smir [<DiagnosticArgs>] [<VersionArgs>]
     <CommandArgs> <MIB file> [<Import Files>]

smi2smir [<DiagnosticArgs>] <RegistryArgs> [<Directory>]

smi2smir <ModuleInfoArgs> <MIB file>

smi2smir <HelpArgs>
```

## <a name="switches"></a><span data-ttu-id="a3e40-108">коммутаторы;</span><span class="sxs-lookup"><span data-stu-id="a3e40-108">Switches</span></span>

<dl> <span data-ttu-id="a3e40-109"><dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*диагностикаргс*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="a3e40-109"><dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*DiagnosticArgs*>
</dt> </span></span><dd>

<span data-ttu-id="a3e40-110">Компилятор принимает следующие аргументы диагностики.</span><span class="sxs-lookup"><span data-stu-id="a3e40-110">The compiler accepts the following diagnostic arguments.</span></span>

<dl> <dt>

<span data-ttu-id="a3e40-111"><span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<** _уровень диагностики_*_>_*</span><span class="sxs-lookup"><span data-stu-id="a3e40-111"><span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<**_diagnostic-level_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-112">Тип отображаемой диагностики.</span><span class="sxs-lookup"><span data-stu-id="a3e40-112">Type of diagnostics to display.</span></span> <span data-ttu-id="a3e40-113">Значение по умолчанию — 2</span><span class="sxs-lookup"><span data-stu-id="a3e40-113">The default is 2.</span></span>

<span data-ttu-id="a3e40-114">Ниже приведен список значений уровня диагностики, которые можно задать.</span><span class="sxs-lookup"><span data-stu-id="a3e40-114">The following is a list of the diagnostic level values that can be set:</span></span>

-   <span data-ttu-id="a3e40-115">0 = автоматический режим</span><span class="sxs-lookup"><span data-stu-id="a3e40-115">0 = Silent</span></span>
-   <span data-ttu-id="a3e40-116">1 = Неустранимая ошибка</span><span class="sxs-lookup"><span data-stu-id="a3e40-116">1 = Fatal</span></span>
-   <span data-ttu-id="a3e40-117">2 = неустранимое и предупреждение</span><span class="sxs-lookup"><span data-stu-id="a3e40-117">2 = Fatal and warning</span></span>
-   <span data-ttu-id="a3e40-118">3 = неустранимые, предупреждения и информационные сообщения</span><span class="sxs-lookup"><span data-stu-id="a3e40-118">3 = Fatal, warning, and information messages</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-119"><span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<** _количество_*_>_*</span><span class="sxs-lookup"><span data-stu-id="a3e40-119"><span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<**_count_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-120">Максимальное число отображаемых неустранимых и предупреждающих сообщений; *Count* должно быть положительным десятичным целым числом.</span><span class="sxs-lookup"><span data-stu-id="a3e40-120">Maximum number of fatal and warning messages to display; *count* must be a positive decimal integer.</span></span> <span data-ttu-id="a3e40-121">Если параметр **/c** не указан, количество ошибок, которые могут быть переданы, не ограничено.</span><span class="sxs-lookup"><span data-stu-id="a3e40-121">If **/c** is not specified, there is no limit to the number of errors that can be reported.</span></span>

<span data-ttu-id="a3e40-122"></dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*версионаргс*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="a3e40-122"></dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*VersionArgs*>
</dt> </span></span><dd>

<span data-ttu-id="a3e40-123">Компилятор принимает следующие аргументы версии.</span><span class="sxs-lookup"><span data-stu-id="a3e40-123">The compiler accepts the following version arguments.</span></span>

<dl> <dt>

<span data-ttu-id="a3e40-124"><span id="_v1"></span><span id="_V1"></span>**/v1**</span><span class="sxs-lookup"><span data-stu-id="a3e40-124"><span id="_v1"></span><span id="_V1"></span>**/v1**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-125">Указывает в качестве более тщательного соответствия SMI.</span><span class="sxs-lookup"><span data-stu-id="a3e40-125">Specifies strict conformance to the SNMPv1 SMI.</span></span> <span data-ttu-id="a3e40-126">Компилятор сообщает об ошибке, если обнаруживает инструкции, не относящиеся к стандарту.</span><span class="sxs-lookup"><span data-stu-id="a3e40-126">The compiler reports an error if it detects non-SNMPv1 statements.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-127"><span id="_v2c"></span><span id="_V2C"></span>**/v2c**</span><span class="sxs-lookup"><span data-stu-id="a3e40-127"><span id="_v2c"></span><span id="_V2C"></span>**/v2c**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-128">Указывает на нестандартное соответствие SMI SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="a3e40-128">Specifies strict conformance to the SNMPv2 SMI.</span></span> <span data-ttu-id="a3e40-129">Компилятор сообщает об ошибке, если обнаруживает инструкции, не относящиеся к SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="a3e40-129">The compiler reports an error if it detects non-SNMPv2 statements.</span></span>

<span data-ttu-id="a3e40-130"></dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*CommandArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="a3e40-130"></dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*CommandArgs*>
</dt> </span></span><dd>

<span data-ttu-id="a3e40-131">Компилятор принимает следующие аргументы команды.</span><span class="sxs-lookup"><span data-stu-id="a3e40-131">The compiler accepts the following command arguments.</span></span>

<dl> <dt>

<span data-ttu-id="a3e40-132"><span id="_d"></span><span id="_D"></span>**/d**</span><span class="sxs-lookup"><span data-stu-id="a3e40-132"><span id="_d"></span><span id="_D"></span>**/d**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-133">Удаляет указанный модуль из Смир.</span><span class="sxs-lookup"><span data-stu-id="a3e40-133">Deletes the specified module from the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-134"><span id="_p"></span><span id="_P"></span>**/p**</span><span class="sxs-lookup"><span data-stu-id="a3e40-134"><span id="_p"></span><span id="_P"></span>**/p**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-135">Удаляет все модули в Смир.</span><span class="sxs-lookup"><span data-stu-id="a3e40-135">Deletes all modules in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-136"><span id="_l"></span><span id="_L"></span>**/l**</span><span class="sxs-lookup"><span data-stu-id="a3e40-136"><span id="_l"></span><span id="_L"></span>**/l**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-137">Список всех модулей в Смир.</span><span class="sxs-lookup"><span data-stu-id="a3e40-137">Lists all modules in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-138"><span id="_lc"></span><span id="_LC"></span>**/лк**</span><span class="sxs-lookup"><span data-stu-id="a3e40-138"><span id="_lc"></span><span id="_LC"></span>**/lc**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-139">Выполняет локальную проверку синтаксиса модуля.</span><span class="sxs-lookup"><span data-stu-id="a3e40-139">Performs a local syntax check on the module.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-140"><span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/ЕК** **\[<** _Коммандмодифиер_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="a3e40-140"><span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/ec** **\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-141">Выполняет локальные и внешние проверки модуля.</span><span class="sxs-lookup"><span data-stu-id="a3e40-141">Performs local and external checks on the module.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-142"><span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**\[ /a <** _Коммандмодифиер_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="a3e40-142"><span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**/a\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-143">Выполняет локальные и внешние проверки и загружает модуль в Смир.</span><span class="sxs-lookup"><span data-stu-id="a3e40-143">Performs local and external checks and loads the module into the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-144"><span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**\[ /SA <** _Коммандмодифиер_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="a3e40-144"><span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**/sa\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-145">То же, что и **/a**, но работает автоматически.</span><span class="sxs-lookup"><span data-stu-id="a3e40-145">Same as **/a**, but works silently.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-146"><span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**\[ /g <** _Коммандмодифиер_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="a3e40-146"><span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**/g\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-147">Создает файл Смир. mof, который позже можно загрузить в WMI с помощью компилятора MOF.</span><span class="sxs-lookup"><span data-stu-id="a3e40-147">Generates a SMIR .mof file that you can later load into WMI using the MOF compiler.</span></span> <span data-ttu-id="a3e40-148">Используется поставщиком классов SNMP для динамического предоставления классов одному или нескольким пространствам имен.</span><span class="sxs-lookup"><span data-stu-id="a3e40-148">Used by the SNMP class provider to provide classes dynamically to one or more namespaces.</span></span> <span data-ttu-id="a3e40-149">Используйте этот параметр, если неизвестно, какие MIB поддерживаются управляемыми SNMP-устройствами.</span><span class="sxs-lookup"><span data-stu-id="a3e40-149">Use this option when you do not know which MIBs are supported by the SNMP devices being managed.</span></span> <span data-ttu-id="a3e40-150">Поставщик классов SNMP проверяет устройство во время выполнения на наличие этой MIB и динамически предоставляет классы пространству имен.</span><span class="sxs-lookup"><span data-stu-id="a3e40-150">The SNMP class provider checks the device at runtime for the presence of this MIB and supplies the classes dynamically to the namespace.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-151"><span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**\[ /GC <** _Коммандмодифиер_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="a3e40-151"><span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**/gc\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-152">Создает статический MOF-файл, который позже можно загрузить в WMI как статические классы для определенного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="a3e40-152">Generates a static .mof file that can be loaded later into WMI as static classes for a particular namespace.</span></span> <span data-ttu-id="a3e40-153">Используйте этот параметр, если известно, какие MIB поддерживаются управляемыми SNMP-устройствами.</span><span class="sxs-lookup"><span data-stu-id="a3e40-153">Use this option when you know which MIBs are supported by the SNMP devices being managed.</span></span> <span data-ttu-id="a3e40-154">Вы можете определить создаваемый MOF-файл путем направления выходных данных команды в указанный файл.</span><span class="sxs-lookup"><span data-stu-id="a3e40-154">You can define the .mof file to be generated by directing the output of your command to a specified file.</span></span> <span data-ttu-id="a3e40-155">Не используйте WITH **/екст/о**.</span><span class="sxs-lookup"><span data-stu-id="a3e40-155">Do not use with **/ext/o**.</span></span>

<span data-ttu-id="a3e40-156"></dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*коммандмодифиерс*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="a3e40-156"></dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*CommandModifiers*>
</dt> </span></span><dd>

<span data-ttu-id="a3e40-157">Компилятор принимает следующие модификаторы команды.</span><span class="sxs-lookup"><span data-stu-id="a3e40-157">The compiler accepts the following command modifiers.</span></span>

<dl> <dt>

<span data-ttu-id="a3e40-158"><span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**/i<** _Каталог_*_>_*</span><span class="sxs-lookup"><span data-stu-id="a3e40-158"><span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**/i<**_directory_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-159">Указывает каталог для поиска зависимых модулей MIB.</span><span class="sxs-lookup"><span data-stu-id="a3e40-159">Specifies a directory to be searched for dependent MIB modules.</span></span> <span data-ttu-id="a3e40-160">Используйте с **/a**, **/ЕК**, **/g**, **/GC** и **/SA**.</span><span class="sxs-lookup"><span data-stu-id="a3e40-160">Use with **/a**, **/ec**, **/g**, **/gc**, and **/sa**.</span></span> <span data-ttu-id="a3e40-161">Параметр **/i** может встречаться в команде несколько раз; Поиск в каталогах выполняется в порядке, указанном в команде.</span><span class="sxs-lookup"><span data-stu-id="a3e40-161">The **/i** option can appear multiple times in the command; directories are searched in the order specified in the command.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-162"><span id="_ch"></span><span id="_CH"></span>**/ч**</span><span class="sxs-lookup"><span data-stu-id="a3e40-162"><span id="_ch"></span><span id="_CH"></span>**/ch**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-163">Создает контекстные сведения, например дату, время, узел или пользователя, в заголовке MOF-файла.</span><span class="sxs-lookup"><span data-stu-id="a3e40-163">Generates context information, such as the date, time, host, or user, in the MOF file header.</span></span> <span data-ttu-id="a3e40-164">Используйте с параметром **/g** и **/GC**.</span><span class="sxs-lookup"><span data-stu-id="a3e40-164">Use with **/g** and **/gc**.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-165"><span id="_t"></span><span id="_T"></span>**/t**</span><span class="sxs-lookup"><span data-stu-id="a3e40-165"><span id="_t"></span><span id="_T"></span>**/t**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-166">Создает классы [снмпнотификатион](snmpnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="a3e40-166">Generates [SnmpNotification](snmpnotification.md) classes.</span></span> <span data-ttu-id="a3e40-167">Используйте WITH **/a**, **/g** и **/SA**.</span><span class="sxs-lookup"><span data-stu-id="a3e40-167">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-168"><span id="_ext"></span><span id="_EXT"></span>**/екст**</span><span class="sxs-lookup"><span data-stu-id="a3e40-168"><span id="_ext"></span><span id="_EXT"></span>**/ext**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-169">Создает классы [снмпекстендеднотификатион](snmpextendednotification.md) .</span><span class="sxs-lookup"><span data-stu-id="a3e40-169">Generates [SnmpExtendedNotification](snmpextendednotification.md) classes.</span></span> <span data-ttu-id="a3e40-170">Используйте WITH **/a**, **/g** и **/SA**.</span><span class="sxs-lookup"><span data-stu-id="a3e40-170">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-171"><span id="_t_o"></span><span id="_T_O"></span>**/т/о**</span><span class="sxs-lookup"><span data-stu-id="a3e40-171"><span id="_t_o"></span><span id="_T_O"></span>**/t/o**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-172">Создает только классы [снмпнотификатион](snmpnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="a3e40-172">Generates only [SnmpNotification](snmpnotification.md) classes.</span></span> <span data-ttu-id="a3e40-173">Используйте WITH **/a**, **/g** и **/SA**.</span><span class="sxs-lookup"><span data-stu-id="a3e40-173">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-174"><span id="_ext_o"></span><span id="_EXT_O"></span>**/екст/о**</span><span class="sxs-lookup"><span data-stu-id="a3e40-174"><span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-175">Создает только классы [снмпекстендеднотификатион](snmpextendednotification.md) .</span><span class="sxs-lookup"><span data-stu-id="a3e40-175">Generates only [SnmpExtendedNotification](snmpextendednotification.md) classes.</span></span> <span data-ttu-id="a3e40-176">Используйте WITH **/a**, **/g** и **/SA**.</span><span class="sxs-lookup"><span data-stu-id="a3e40-176">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-177"><span id="_s"></span><span id="_S"></span>**ключ**</span><span class="sxs-lookup"><span data-stu-id="a3e40-177"><span id="_s"></span><span id="_S"></span>**/s**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-178">Не сопоставляет текст предложения DESCRIPTION.</span><span class="sxs-lookup"><span data-stu-id="a3e40-178">Does not map the text of the DESCRIPTION clause.</span></span> <span data-ttu-id="a3e40-179">Используйте WITH **/a**, **/g**, **/GC** и **/SA**.</span><span class="sxs-lookup"><span data-stu-id="a3e40-179">Use with **/a**, **/g**, **/gc**, and **/sa**.</span></span> <span data-ttu-id="a3e40-180">Используйте этот параметр, если необходимо ограничить требования к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="a3e40-180">Use this option when you want to minimize storage requirements.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-181"><span id="_auto"></span><span id="_AUTO"></span>**/ауто**</span><span class="sxs-lookup"><span data-stu-id="a3e40-181"><span id="_auto"></span><span id="_AUTO"></span>**/auto**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-182">Перестраивает таблицу подстановки MIB перед выполнением параметра <*коммандарг*>.</span><span class="sxs-lookup"><span data-stu-id="a3e40-182">Rebuilds the MIB lookup table before completing the <*CommandArg*> switch.</span></span> <span data-ttu-id="a3e40-183">Используйте с **/a**, **/ЕК**, **/g** и **/GC**.</span><span class="sxs-lookup"><span data-stu-id="a3e40-183">Use with **/a**, **/ec**, **/g**, and **/gc**.</span></span>

<span data-ttu-id="a3e40-184"></dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*регистряргс*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="a3e40-184"></dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*RegistryArgs*>
</dt> </span></span><dd>

<span data-ttu-id="a3e40-185">Компилятор принимает следующие аргументы реестра.</span><span class="sxs-lookup"><span data-stu-id="a3e40-185">The compiler accepts the following registry arguments.</span></span>

<dl> <dt>

<span data-ttu-id="a3e40-186"><span id="_pa"></span><span id="_PA"></span>**/па**</span><span class="sxs-lookup"><span data-stu-id="a3e40-186"><span id="_pa"></span><span id="_PA"></span>**/pa**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-187">Добавляет указанный каталог в реестр.</span><span class="sxs-lookup"><span data-stu-id="a3e40-187">Adds the specified directory to the registry.</span></span> <span data-ttu-id="a3e40-188">Значением по умолчанию является текущий каталог.</span><span class="sxs-lookup"><span data-stu-id="a3e40-188">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-189"><span id="_pd"></span><span id="_PD"></span>**/пд**</span><span class="sxs-lookup"><span data-stu-id="a3e40-189"><span id="_pd"></span><span id="_PD"></span>**/pd**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-190">Удаляет указанный каталог из реестра.</span><span class="sxs-lookup"><span data-stu-id="a3e40-190">Deletes the specified directory from the registry.</span></span> <span data-ttu-id="a3e40-191">Значением по умолчанию является текущий каталог.</span><span class="sxs-lookup"><span data-stu-id="a3e40-191">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-192"><span id="_pl"></span><span id="_PL"></span>**ключом/pl**</span><span class="sxs-lookup"><span data-stu-id="a3e40-192"><span id="_pl"></span><span id="_PL"></span>**/pl**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-193">Список каталогов подстановки MIB в реестре.</span><span class="sxs-lookup"><span data-stu-id="a3e40-193">Lists the MIB lookup directories in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-194"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="a3e40-194"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-195">Перестраивает всю таблицу подстановки MIB.</span><span class="sxs-lookup"><span data-stu-id="a3e40-195">Rebuilds the entire MIB lookup table.</span></span>

<span data-ttu-id="a3e40-196"></dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*модулеинфоаргс*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="a3e40-196"></dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*ModuleInfoArgs*>
</dt> </span></span><dd>

<span data-ttu-id="a3e40-197">Компилятор принимает следующие аргументы сведений о модуле.</span><span class="sxs-lookup"><span data-stu-id="a3e40-197">The compiler accepts the following module information arguments.</span></span>

<dl> <dt>

<span data-ttu-id="a3e40-198"><span id="_n"></span><span id="_N"></span>**параметра**</span><span class="sxs-lookup"><span data-stu-id="a3e40-198"><span id="_n"></span><span id="_N"></span>**/n**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-199">Возвращает имя ASN. 1 указанного модуля.</span><span class="sxs-lookup"><span data-stu-id="a3e40-199">Returns the ASN.1 name of the specified module.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-200"><span id="_ni"></span><span id="_NI"></span>**/ни**</span><span class="sxs-lookup"><span data-stu-id="a3e40-200"><span id="_ni"></span><span id="_NI"></span>**/ni**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-201">Возвращает имена ASN. 1 всех модулей импорта, на которые ссылается входной модуль.</span><span class="sxs-lookup"><span data-stu-id="a3e40-201">Returns the ASN.1 names of all import modules referred to by the input module.</span></span>

<span data-ttu-id="a3e40-202"></dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*хелпаргс*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="a3e40-202"></dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*HelpArgs*>
</dt> </span></span><dd>

<span data-ttu-id="a3e40-203">Компилятор принимает следующие аргументы справки.</span><span class="sxs-lookup"><span data-stu-id="a3e40-203">The compiler accepts the following help arguments.</span></span>

<dl> <dt>

<span data-ttu-id="a3e40-204"><span id="_h"></span><span id="_H"></span>**/h**</span><span class="sxs-lookup"><span data-stu-id="a3e40-204"><span id="_h"></span><span id="_H"></span>**/h**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-205">Отображает справку по синтаксису компилятора SNMP.</span><span class="sxs-lookup"><span data-stu-id="a3e40-205">Displays help on the SNMP compiler syntax.</span></span>

</dd> <dt>

<span data-ttu-id="a3e40-206"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="a3e40-206"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="a3e40-207">Отображает справку по синтаксису компилятора SNMP.</span><span class="sxs-lookup"><span data-stu-id="a3e40-207">Displays help on the SNMP compiler syntax.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3e40-208">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3e40-208">Remarks</span></span>

<span data-ttu-id="a3e40-209">Модули сведений SNMP записываются в подмножестве абстрактного синтаксиса One (ASN. 1). компилятор выполняет следующие функции:</span><span class="sxs-lookup"><span data-stu-id="a3e40-209">SNMP information modules are written in a subset of the Abstract Syntax Notation One (ASN.1) The compiler performs the following functions:</span></span>

-   <span data-ttu-id="a3e40-210">Загружает данные из модуля SNMP-данных.</span><span class="sxs-lookup"><span data-stu-id="a3e40-210">Loads the data from the SNMP information module.</span></span>
-   <span data-ttu-id="a3e40-211">Выполнение операций проверки в модуле данных.</span><span class="sxs-lookup"><span data-stu-id="a3e40-211">Performs checking operations on the information module.</span></span> <span data-ttu-id="a3e40-212">Например, он проверяет локальный синтаксис и проверяет внешние ссылки на сведения в дочерних модулях.</span><span class="sxs-lookup"><span data-stu-id="a3e40-212">For example, it checks the local syntax and it checks external references against information in the subsidiary modules.</span></span>
-   <span data-ttu-id="a3e40-213">Удаление всех загруженных из SMIR данных или удаление данных, загруженных из модуля данных.</span><span class="sxs-lookup"><span data-stu-id="a3e40-213">Removes all previously loaded data from the SMIR, or removes data loaded from one information module.</span></span>
-   <span data-ttu-id="a3e40-214">Возвращает имя модуля ASN. 1 указанного файла или возвращает имена модулей ASN. 1 всех импортированных модулей в указанном файле.</span><span class="sxs-lookup"><span data-stu-id="a3e40-214">Returns the ASN.1 module name of a specified file or returns the ASN.1 module names of all imported modules in a specified file.</span></span>
-   <span data-ttu-id="a3e40-215">Возвращение имен модулей ASN.1 для всех модулей данных SNMP, которые в настоящий момент загружены в SMIR.</span><span class="sxs-lookup"><span data-stu-id="a3e40-215">Returns the ASN.1 module names of all SNMP information modules currently loaded in the SMIR.</span></span>
-   <span data-ttu-id="a3e40-216">Выполняет автоматическое разрешение импортированных модулей, не требуя от пользователей указывать необходимые модули вручную.</span><span class="sxs-lookup"><span data-stu-id="a3e40-216">Performs automatic resolution of imported modules rather than requiring users to specify the required modules manually.</span></span>
-   <span data-ttu-id="a3e40-217">Выполняет режим автоматической загрузки для операции, которая не создает никаких выходных данных, но может использоваться для загрузки данных в Смир во время операции установки.</span><span class="sxs-lookup"><span data-stu-id="a3e40-217">Performs a silent-loading mode of operation that does not generate any output, but can be used to load data into the SMIR during an installation operation.</span></span>
-   <span data-ttu-id="a3e40-218">Выводит данные из модуля SNMP-данных в Смир.</span><span class="sxs-lookup"><span data-stu-id="a3e40-218">Outputs the data from the SNMP information module into the SMIR.</span></span>
-   <span data-ttu-id="a3e40-219">При необходимости создает статический или Смир MOF-файл, содержащий выходные данные из информационного модуля.</span><span class="sxs-lookup"><span data-stu-id="a3e40-219">Optionally creates a static or SMIR MOF file containing the output from the information module.</span></span>

    <span data-ttu-id="a3e40-220">При необходимости можно загрузить статический MOF-файл в пространство имен WMI.</span><span class="sxs-lookup"><span data-stu-id="a3e40-220">If necessary, you can load the static .mof file into a WMI namespace.</span></span> <span data-ttu-id="a3e40-221">Файл Смир. mof содержит имя пространства имен SNMP, в котором должны располагаться классы.</span><span class="sxs-lookup"><span data-stu-id="a3e40-221">A SMIR .mof file contains the name of the SNMP namespace in which the classes should reside.</span></span>

## <a name="examples"></a><span data-ttu-id="a3e40-222">Примеры</span><span class="sxs-lookup"><span data-stu-id="a3e40-222">Examples</span></span>

<span data-ttu-id="a3e40-223">В следующем примере определяется файл одного. mof, который будет выходным файлом одного. MIB.</span><span class="sxs-lookup"><span data-stu-id="a3e40-223">The following example defines the pra.mof file to be the output from the pra.mib file.</span></span>

``` syntax
smi2smir /m 3 /v1 /gc /pra.mib > pra.mof
```

## <a name="requirements"></a><span data-ttu-id="a3e40-224">Требования</span><span class="sxs-lookup"><span data-stu-id="a3e40-224">Requirements</span></span>



| <span data-ttu-id="a3e40-225">Требование</span><span class="sxs-lookup"><span data-stu-id="a3e40-225">Requirement</span></span> | <span data-ttu-id="a3e40-226">Значение</span><span class="sxs-lookup"><span data-stu-id="a3e40-226">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a3e40-227">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3e40-227">Minimum supported client</span></span><br/> | <span data-ttu-id="a3e40-228">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3e40-228">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a3e40-229">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3e40-229">Minimum supported server</span></span><br/> | <span data-ttu-id="a3e40-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3e40-230">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a3e40-231">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3e40-231">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3e40-232">Сообщения об ошибках компилятора SNMP</span><span class="sxs-lookup"><span data-stu-id="a3e40-232">SNMP Compiler Error Messages</span></span>](snmp-compiler-error-messages.md)
</dt> <dt>

[<span data-ttu-id="a3e40-233">Настройка среды SNMP WMI</span><span class="sxs-lookup"><span data-stu-id="a3e40-233">Setting up the WMI SNMP Environment</span></span>](setting-up-the-wmi-snmp-environment.md)
</dt> <dt>

[<span data-ttu-id="a3e40-234">Доступ к SNMP-устройствам</span><span class="sxs-lookup"><span data-stu-id="a3e40-234">Accessing SNMP Devices</span></span>](accessing-snmp-devices.md)
</dt> </dl>

 

 




