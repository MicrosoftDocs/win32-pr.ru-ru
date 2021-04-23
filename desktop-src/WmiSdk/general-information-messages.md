---
description: В следующих информационных сообщениях описывается операция компилятора.
ms.assetid: 838e598d-871d-4015-a372-4d94cacf8048
ms.tgt_platform: multiple
title: Общие информационные сообщения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0997fad497299c7598fc1130edace49c20d7bb76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344912"
---
# <a name="general-information-messages"></a><span data-ttu-id="f4b3b-103">Общие информационные сообщения</span><span class="sxs-lookup"><span data-stu-id="f4b3b-103">General Information Messages</span></span>

<span data-ttu-id="f4b3b-104">В следующих информационных сообщениях описывается операция компилятора.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-104">The following information messages describe the compiler operation.</span></span>

<dl> <dt>

<span data-ttu-id="f4b3b-105"><span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**smi2smir: версии <версии \#> определений MIB, скомпилированные из <file name>**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-105"><span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**smi2smir: Version <version \#> MIB definitions compiled from <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-106">Это сообщение появляется в начале каждой компиляции файла.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-106">This message appears at the beginning of every file compilation.</span></span> <span data-ttu-id="f4b3b-107">Это означает, что файл мог быть явно указан пользователем в командной строке или был извлечен компилятором из каталогов include, а также из каталогов include, указанных в командной строке.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-107">It means the file may have been explicitly specified on the command line by the user, or it may have been pulled in by the compiler from the registry include directories or the include directories mentioned on the command line.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-108"><span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: ошибка при проверке синтаксиса <file name>**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-108"><span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: Syntax check failed on <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-109">Конкретные сообщения об ошибках, предшествующие этому сообщению, дают характер синтаксических ошибок.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-109">The specific error messages that precede this message give the nature of the syntax errors.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-110"><span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: сбой семантической проверки <file name>**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-110"><span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: Semantic check failed on <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-111">Конкретные сообщения об ошибках, предшествующие этому сообщению, дают природу семантических ошибок.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-111">The specific error messages that precede this message give the nature of the semantic errors.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-112"><span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**smi2smir: не удалось загрузить <file name> в Смир**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-112"><span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**smi2smir: Could not load <file name> into the smir**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-113">Сбой при проверке синтаксиса или семантической проверки модуля, или СМИРное взаимодействие не было завершено.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-113">Syntax or semantic check failed on the module, or SMIR interaction was not complete.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-114"><span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: Проверка синтаксиса выполнена успешно <file name>**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-114"><span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: Syntax check successful on <file name>**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f4b3b-115"><span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: успешная семантическая проверка <file name>**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-115"><span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: Semantic check successful on <file name>**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f4b3b-116"><span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**smi2smir: <file name> успешно загружен в Смир**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-116"><span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**smi2smir: Loaded <file name> successfully into the smir**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f4b3b-117"><span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**smi2smir: не удалось разрешить один или несколько символов в <module name>**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-117"><span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**smi2smir: Could not resolve one or more symbols in <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-118">Модули, соответствующие одному или нескольким импортированным символам в указанном модуле, не найдены или не могут быть скомпилированы.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-118">The modules corresponding to one or more of the imported symbols in the specified module were not found or could not be compiled.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-119"><span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**smi2smir: не удалось подключиться к Смир**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-119"><span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**smi2smir: Could not connect to the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-120">Убедитесь, что Smir.dll существует, была зарегистрирована с помощью команды regsvr32 и что сервер инструментарий управления Windows (WMI) (WMI) работает.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-120">Ensure that Smir.dll exists, has been registered using the regsvr32 command, and that the Windows Management Instrumentation (WMI) server is up and running.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-121"><span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**smi2smir: модули в Смир: <список модулей, 1 в каждой строке>**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-121"><span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**smi2smir: Modules in the SMIR: <list of modules, 1 on each line>**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-122">Это выходные данные параметра **/l** .</span><span class="sxs-lookup"><span data-stu-id="f4b3b-122">This is the output of the **/l** switch.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-123"><span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**smi2smir не удалось перечислить модули в Смир**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-123"><span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**smi2smir Could not list the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-124">Это указывает на сбой параметра **/l** из-за отсутствия подключения Смир.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-124">This indicates a failure of the **/l** switch due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-125"><span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**smi2smir: модуль <module name> успешно удален**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-125"><span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**smi2smir: Deleted module <module name> successfully**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-126">Параметр **/d** прошел.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-126">The **/d** switch succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-127"><span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**smi2smir: не удалось удалить модуль <module name>**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-127"><span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**smi2smir: Could not delete module <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-128">Это указывает на сбой параметра **/d** из-за отсутствия подключения Смир.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-128">This indicates a failure of the **/d** switch due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-129"><span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: удалены все модули в Смир**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-129"><span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: Deleted all the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-130">Параметр **/p** прошел.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-130">The **/p** switch succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-131"><span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: не удалось удалить все модули в Смир**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-131"><span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: Could not delete all the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-132">Сбой параметра **/p** из-за отсутствия подключения Смир.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-132">The **/p** switch failed because there is no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-133"><span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**smi2smir: модуль <module name> не существует в Смир**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-133"><span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**smi2smir: Module <module name> does not exist in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-134">Не удалось выполнить параметр **/d** , так как указанный модуль не находится в Смир.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-134">The **/d** switch failed because the specified module is not in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-135"><span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**smi2smir: успешно создан MOF**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-135"><span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**smi2smir: Generated MOF successfully**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-136">Параметр **/g** или **/GC** успешно сработал.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-136">The **/g** or **/gc** switch worked successfully.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-137"><span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**smi2smir: не удалось создать MOF**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-137"><span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**smi2smir: Could not generate MOF**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-138">Параметр **/g** или **/GC** не был успешно выполнен из-за отсутствия подключения Смир.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-138">The **/g** or **/gc** switch did not work successfully due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-139"><span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**smi2smir: имя модуля: <module name>**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-139"><span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**smi2smir: Name of the module: <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-140">Это успешный вывод параметра **/n** .</span><span class="sxs-lookup"><span data-stu-id="f4b3b-140">This is the successful output of the **/n** switch.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-141"><span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**smi2smir: не удалось успешно выполнить синтаксический анализ <file name>**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-141"><span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**smi2smir: Could not parse <file name> successfully**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-142">Это указывает на сбой параметра **/n** или **/ни** , так как указанный файл не является допустимым файлом MIB.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-142">This indicates failure of the **/n** or **/ni** switch because the specified file is not a valid MIB file.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-143"><span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**smi2smir: успешно обработанные <number> файлы**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-143"><span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**smi2smir: Processed <number> files successfully**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-144">Указывает количество файлов, успешно проанализированных при использовании параметра **/r** или **/АУТО** .</span><span class="sxs-lookup"><span data-stu-id="f4b3b-144">This specifies the number of files that were successfully parsed when the **/r** or the **/auto** switch were used.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-145"><span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**smi2smir: повторяющиеся файлы во входных данных для модуля <module name> . <file name> Будет скомпилирован только файл**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-145"><span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**smi2smir: Repeated files in the input for module <module name>. Only the file <file name> will be compiled**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-146">Пользователь явно указал более одного файла в командной строке, и два или более из этих файлов имеют один и тот же модуль MIB.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-146">The user has explicitly specified more than one file on the command line, and two or more of these files have the same MIB module.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-147"><span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: <directory name> в реестр добавлен каталог**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-147"><span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: Added directory <directory name> to the registry**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-148">Успешное выполнение параметра **/ПА** .</span><span class="sxs-lookup"><span data-stu-id="f4b3b-148">Success of the **/pa** switch.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-149"><span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: не удалось добавить каталог <directory name> в реестр**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-149"><span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: Could not add directory <directory name> to the registry**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-150">Сбой параметра **/ПА** , который происходит только в случае сбоя API реестра.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-150">Failure of the **/pa** switch, which happens only if the registry API fails.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-151"><span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: удален каталог <directory name> из реестра.**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-151"><span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: Deleted directory <directory name> from the registry**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-152">Успешное выполнение параметра **/ПД** .</span><span class="sxs-lookup"><span data-stu-id="f4b3b-152">Success of the **/pd** switch.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-153"><span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: не удалось удалить <directory name> из реестра**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-153"><span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: Could not delete <directory name> from the registry**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-154">Сбой параметра **/ПД** .</span><span class="sxs-lookup"><span data-stu-id="f4b3b-154">Failure of the **/pd** switch.</span></span> <span data-ttu-id="f4b3b-155">Указанный каталог не существует в списке каталогов в реестре.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-155">The specified directory does not exist in the list of directories in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="f4b3b-156"><span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**smi2smir: <file name> не является допустимым файлом MIB**</span><span class="sxs-lookup"><span data-stu-id="f4b3b-156"><span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**smi2smir: <file name> is not a valid mib file**</span></span>
</dt> <dd>

<span data-ttu-id="f4b3b-157">В командной строке указано более одного файла, один из которых не является допустимым файлом MIB.</span><span class="sxs-lookup"><span data-stu-id="f4b3b-157">More than one file has been specified on the command line, one of which is not a valid MIB file.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="f4b3b-158">См. также</span><span class="sxs-lookup"><span data-stu-id="f4b3b-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4b3b-159">Настройка среды SNMP WMI</span><span class="sxs-lookup"><span data-stu-id="f4b3b-159">Setting up the WMI SNMP Environment</span></span>](setting-up-the-wmi-snmp-environment.md)
</dt> </dl>

 

 



