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
# <a name="general-information-messages"></a>Общие информационные сообщения

В следующих информационных сообщениях описывается операция компилятора.

<dl> <dt>

<span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**smi2smir: версии <версии \#> определений MIB, скомпилированные из <file name>**
</dt> <dd>

Это сообщение появляется в начале каждой компиляции файла. Это означает, что файл мог быть явно указан пользователем в командной строке или был извлечен компилятором из каталогов include, а также из каталогов include, указанных в командной строке.

</dd> <dt>

<span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: ошибка при проверке синтаксиса <file name>**
</dt> <dd>

Конкретные сообщения об ошибках, предшествующие этому сообщению, дают характер синтаксических ошибок.

</dd> <dt>

<span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: сбой семантической проверки <file name>**
</dt> <dd>

Конкретные сообщения об ошибках, предшествующие этому сообщению, дают природу семантических ошибок.

</dd> <dt>

<span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**smi2smir: не удалось загрузить <file name> в Смир**
</dt> <dd>

Сбой при проверке синтаксиса или семантической проверки модуля, или СМИРное взаимодействие не было завершено.

</dd> <dt>

<span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: Проверка синтаксиса выполнена успешно <file name>**
</dt> <dd></dd> <dt>

<span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: успешная семантическая проверка <file name>**
</dt> <dd></dd> <dt>

<span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**smi2smir: <file name> успешно загружен в Смир**
</dt> <dd></dd> <dt>

<span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**smi2smir: не удалось разрешить один или несколько символов в <module name>**
</dt> <dd>

Модули, соответствующие одному или нескольким импортированным символам в указанном модуле, не найдены или не могут быть скомпилированы.

</dd> <dt>

<span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**smi2smir: не удалось подключиться к Смир**
</dt> <dd>

Убедитесь, что Smir.dll существует, была зарегистрирована с помощью команды regsvr32 и что сервер инструментарий управления Windows (WMI) (WMI) работает.

</dd> <dt>

<span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**smi2smir: модули в Смир: <список модулей, 1 в каждой строке>**
</dt> <dd>

Это выходные данные параметра **/l** .

</dd> <dt>

<span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**smi2smir не удалось перечислить модули в Смир**
</dt> <dd>

Это указывает на сбой параметра **/l** из-за отсутствия подключения Смир.

</dd> <dt>

<span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**smi2smir: модуль <module name> успешно удален**
</dt> <dd>

Параметр **/d** прошел.

</dd> <dt>

<span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**smi2smir: не удалось удалить модуль <module name>**
</dt> <dd>

Это указывает на сбой параметра **/d** из-за отсутствия подключения Смир.

</dd> <dt>

<span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: удалены все модули в Смир**
</dt> <dd>

Параметр **/p** прошел.

</dd> <dt>

<span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: не удалось удалить все модули в Смир**
</dt> <dd>

Сбой параметра **/p** из-за отсутствия подключения Смир.

</dd> <dt>

<span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**smi2smir: модуль <module name> не существует в Смир**
</dt> <dd>

Не удалось выполнить параметр **/d** , так как указанный модуль не находится в Смир.

</dd> <dt>

<span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**smi2smir: успешно создан MOF**
</dt> <dd>

Параметр **/g** или **/GC** успешно сработал.

</dd> <dt>

<span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**smi2smir: не удалось создать MOF**
</dt> <dd>

Параметр **/g** или **/GC** не был успешно выполнен из-за отсутствия подключения Смир.

</dd> <dt>

<span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**smi2smir: имя модуля: <module name>**
</dt> <dd>

Это успешный вывод параметра **/n** .

</dd> <dt>

<span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**smi2smir: не удалось успешно выполнить синтаксический анализ <file name>**
</dt> <dd>

Это указывает на сбой параметра **/n** или **/ни** , так как указанный файл не является допустимым файлом MIB.

</dd> <dt>

<span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**smi2smir: успешно обработанные <number> файлы**
</dt> <dd>

Указывает количество файлов, успешно проанализированных при использовании параметра **/r** или **/АУТО** .

</dd> <dt>

<span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**smi2smir: повторяющиеся файлы во входных данных для модуля <module name> . <file name> Будет скомпилирован только файл**
</dt> <dd>

Пользователь явно указал более одного файла в командной строке, и два или более из этих файлов имеют один и тот же модуль MIB.

</dd> <dt>

<span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: <directory name> в реестр добавлен каталог**
</dt> <dd>

Успешное выполнение параметра **/ПА** .

</dd> <dt>

<span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: не удалось добавить каталог <directory name> в реестр**
</dt> <dd>

Сбой параметра **/ПА** , который происходит только в случае сбоя API реестра.

</dd> <dt>

<span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: удален каталог <directory name> из реестра.**
</dt> <dd>

Успешное выполнение параметра **/ПД** .

</dd> <dt>

<span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: не удалось удалить <directory name> из реестра**
</dt> <dd>

Сбой параметра **/ПД** . Указанный каталог не существует в списке каталогов в реестре.

</dd> <dt>

<span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**smi2smir: <file name> не является допустимым файлом MIB**
</dt> <dd>

В командной строке указано более одного файла, один из которых не является допустимым файлом MIB.

</dd> </dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md)
</dt> </dl>

 

 



