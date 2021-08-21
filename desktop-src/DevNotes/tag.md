---
description: Определяет запись в базе данных оболочек совместимости.
ms.assetid: c092592d-a4f4-4b2f-9b03-c07951ed214a
title: TAG (Exposeenums2managed. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7e4df727245ead30ecefef0cd941148b8f4c76e2881ab19f41c3388934abd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075798"
---
# <a name="tag"></a>TAG

Определяет запись в базе данных оболочек совместимости.

Следующие записи относятся к типу **\_ \_ списка типов тегов** (0x7000).



| Константа/значение                                                                                                                                                                                                                                                             | Описание                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| <span id="TAG_DATABASE"></span><span id="tag_database"></span><dl> <dt>**Тег \_ БАЗА данных**</dt> <dt>( \| **\_ \_ список типов тегов** 0x1)</dt> </dl>                               | Запись базы данных.<br/>                                                |
| <span id="TAG_LIBRARY"></span><span id="tag_library"></span><dl> <dt>**Тег \_ LIBRARY**</dt> <dt>( \| **\_ \_ список типов тегов** 0x2)</dt> </dl>                                  | Запись в библиотеке.<br/>                                                 |
| <span id="TAG_INEXCLUDE"></span><span id="tag_inexclude"></span><dl> <dt>**Тег \_ ИСКЛЮЧЕНИЕ**</dt> <dt>( \| **\_ \_ список типов тегов** 0x3)</dt> </dl>                            | Включить и исключить запись.<br/>                                     |
| <span id="TAG_SHIM"></span><span id="tag_shim"></span><dl> <dt>**Тег \_ Оболочка совместимости**</dt> <dt>( \| **\_ \_ список типов тегов** 0x4)</dt> </dl>                                           | Запись оболочки совместимости, которая содержит имя и сведения о назначении.<br/>     |
| <span id="TAG_PATCH"></span><span id="tag_patch"></span><dl> <dt>**Тег \_ PATCH**</dt> <dt>( \| **\_ \_ список типов тегов** 0x5)</dt> </dl>                                        | Запись исправления, содержащая сведения об исправлениях в памяти.<br/>  |
| <span id="TAG_APP"></span><span id="tag_app"></span><dl> <dt>**Тег \_ ПРИЛОЖЕНИЕ**</dt> <dt>( \| **\_ \_ список типов тегов** 0x6)</dt> </dl>                                              | Запись приложения.<br/>                                             |
| <span id="TAG_EXE"></span><span id="tag_exe"></span><dl> <dt>**Тег \_ EXE**</dt> <dt>( \| **\_ \_ список типов тегов** 0x7)</dt> </dl>                                              | Исполняемый элемент.<br/>                                              |
| <span id="TAG_MATCHING_FILE"></span><span id="tag_matching_file"></span><dl> <dt>**Тег \_ СООТВЕТСТВУЮЩИЙ \_ файл**</dt> <dt>( \| **\_ \_ список типов тегов** 0x8)</dt> </dl>               | Соответствующая запись файла.<br/>                                           |
| <span id="TAG_SHIM_REF"></span><span id="tag_shim_ref"></span><dl> <dt>**Тег \_ \_Ссылка на оболочку совместимости**</dt> <dt>( \| \_ список типов тегов 0x9 \_ )</dt> </dl>                                   | Запись определения оболочки совместимости.<br/>                                         |
| <span id="TAG_PATCH_REF"></span><span id="tag_patch_ref"></span><dl> <dt>**Тег \_ \_Ссылка на исправление**</dt> <dt>( \| **\_ \_ список типов тегов** 0xA)</dt> </dl>                           | Запись определения исправления.<br/>                                        |
| <span id="TAG_LAYER"></span><span id="tag_layer"></span><dl> <dt>**Тег \_ LAYER**</dt> <dt>( \| **\_ \_ список типов тегов** 0xB)</dt> </dl>                                        | Запись совместимости слоя.<br/>                                              |
| <span id="TAG_FILE"></span><span id="tag_file"></span><dl> <dt>**Тег \_ FILE**</dt> <dt>( \| **\_ \_ список типов тегов** 0xC)</dt> </dl>                                           | Атрибут File, используемый в записи оболочки совместимости.<br/>                           |
| <span id="TAG_APPHELP"></span><span id="tag_apphelp"></span><dl> <dt>**Тег \_ APPHELP**</dt> <dt>( \| **\_ \_ список типов тегов** 0xD)</dt> </dl>                                  | Информационная запись AppHelp.<br/>                                     |
| <span id="TAG_LINK"></span><span id="tag_link"></span><dl> <dt>**Тег \_ LINK**</dt> <dt>( \| **\_ \_ список типов тегов** 0xE)</dt> </dl>                                           | Запись сведений о ссылках в сети AppHelp.<br/>                         |
| <span id="TAG_DATA"></span><span id="tag_data"></span><dl> <dt>**Тег \_ DATA**</dt> <dt>( \| **\_ \_ список типов тегов** 0xF)</dt> </dl>                                           | Запись сопоставления "имя — значение".<br/>                                      |
| <span id="TAG_MSI_TRANSFORM"></span><span id="tag_msi_transform"></span><dl> <dt>**Тег \_ \_Преобразование MSI**</dt> <dt>( \| **\_ \_ список типов тегов** 0x10)</dt> </dl>              | Запись преобразования MSI.<br/>                                      |
| <span id="TAG_MSI_TRANSFORM_REF"></span><span id="tag_msi_transform_ref"></span><dl> <dt>**Тег \_ \_ \_ Ссылка на преобразование MSI**</dt> <dt>( \| **\_ \_ список типов тегов** 0x11)</dt> </dl> | Запись определения преобразования MSI.<br/>                           |
| <span id="TAG_MSI_PACKAGE"></span><span id="tag_msi_package"></span><dl> <dt>**Тег \_ \_Пакет MSI**</dt> <dt>( \| **\_ \_ список типов тегов** 0x12)</dt> </dl>                    | Запись пакета MSI.<br/>                                             |
| <span id="TAG_FLAG"></span><span id="tag_flag"></span><dl> <dt>**Тег \_ FLAG**</dt> <dt>( \| **\_ \_ список типов тегов** 0x13)</dt> </dl>                                          | Запись флага.<br/>                                                    |
| <span id="TAG_MSI_CUSTOM_ACTION"></span><span id="tag_msi_custom_action"></span><dl> <dt>**Тег \_ \_Настраиваемое \_ действие MSI**</dt> <dt>( \| **\_ \_ список типов тегов** 0x14)</dt> </dl> | Запись настраиваемого действия MSI.<br/>                                       |
| <span id="TAG_FLAG_REF"></span><span id="tag_flag_ref"></span><dl> <dt>**Тег \_ ФЛАГ \_ ref**</dt> <dt>( \| **\_ \_ список типов тегов** 0x15)</dt> </dl>                             | Запись определения флага.<br/>                                         |
| <span id="TAG_ACTION"></span><span id="tag_action"></span><dl> <dt>**Тег \_ ACTION**</dt> <dt>( \| **\_ \_ список типов тегов** 0x16)</dt> </dl>                                    | Не используется.<br/>                                                        |
| <span id="TAG_LOOKUP"></span><span id="tag_lookup"></span><dl> <dt>**Тег \_ LOOKUP**</dt> <dt>( \| **\_ \_ список типов тегов** 0x17)</dt> </dl>                                    | Запись поиска, используемая для уточняющего запроса в базе данных драйвера.<br/>             |
| <span id="TAG_STRINGTABLE"></span><span id="tag_stringtable"></span><dl> <dt>**Тег \_ STRINGTABLE**</dt> <dt>( \| **\_ \_ список типов тегов** 0x801)</dt> </dl>                    | Запись в таблице строк.<br/>                                            |
| <span id="TAG_INDEXES"></span><span id="tag_indexes"></span><dl> <dt>**Тег \_ ИНДЕКСы**</dt> <dt>( \| **\_ \_ список типов тегов** 0x802)</dt> </dl>                                | Элемент indexes, определяющий все индексы в базе данных оболочек.<br/> |
| <span id="TAG_INDEX"></span><span id="tag_index"></span><dl> <dt>**Тег \_ INDEX**</dt> <dt>( \| **\_ \_ список типов тегов** 0x803)</dt> </dl>                                      | Элемент индекса, определяющий индекс в базе данных оболочек.<br/>          |



Следующие записи имеют тип **тега \_ \_ стрингреф** (0x6000).



| Константа/значение                                                                                                                                                                                                                                                                     | Описание                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="TAG_NAME"></span><span id="tag_name"></span><dl> <dt>**Тег \_ NAME**</dt> <dt>(0x1 \| **\_ \_ стрингреф тип тега**)</dt> </dl>                                              | Атрибут Name.<br/>                                                                    |
| <span id="TAG_DESCRIPTION"></span><span id="tag_description"></span><dl> <dt>**Тег \_ Описание**</dt> <dt>( \| **тип тега \_ 0x2 \_ стрингреф**)</dt> </dl>                         | Запись описания.<br/>                                                                 |
| <span id="TAG_MODULE"></span><span id="tag_module"></span><dl> <dt>**Тег \_ MODULE**</dt> <dt>( \| **тип тега \_ 0x3 \_ стрингреф**)</dt> </dl>                                        | Атрибут module.<br/>                                                                  |
| <span id="TAG_API"></span><span id="tag_api"></span><dl> <dt>**Тег \_ API**</dt> <dt>( \| **тип тега \_ 0x4 \_ стрингреф**)</dt> </dl>                                                 | Запись API.<br/>                                                                         |
| <span id="TAG_VENDOR"></span><span id="tag_vendor"></span><dl> <dt>**Тег \_ VENDOR**</dt> <dt>( \| **тип тега \_ 0x5 \_ стрингреф**)</dt> </dl>                                        | Атрибут имени поставщика.<br/>                                                             |
| <span id="TAG_APP_NAME"></span><span id="tag_app_name"></span><dl> <dt>**Тег \_ \_Имя приложения**</dt> <dt>( \| **тип тега \_ 0x6 \_ стрингреф**)</dt> </dl>                                 | Атрибут имени приложения, описывающий запись приложения в базе данных оболочек.<br/> |
| <span id="TAG_COMMAND_LINE"></span><span id="tag_command_line"></span><dl> <dt>**Тег \_ КОМАНДная \_ строка**</dt> <dt>( \| **тип тега 0x8 \_ \_ стрингреф**)</dt> </dl>                     | Атрибут командной строки, используемый при передаче аргументов в оболочку совместимости, например.<br/> |
| <span id="TAG_COMPANY_NAME"></span><span id="tag_company_name"></span><dl> <dt>**Тег \_ \_Название организации**</dt> <dt>( \| **тип тега \_ 0x9 \_ стрингреф**)</dt> </dl>                     | Атрибут названия организации.<br/>                                                            |
| <span id="TAG_DLLFILE"></span><span id="tag_dllfile"></span><dl> <dt>**Тег \_ ДЛЛФИЛЕ**</dt> <dt>( \| **тип тега \_ 0xA \_ стрингреф**)</dt> </dl>                                     | Атрибут файла DLL для записи оболочки совместимости.<br/>                                               |
| <span id="TAG_WILDCARD_NAME"></span><span id="tag_wildcard_name"></span><dl> <dt>**Тег \_ ПОДСТАНОВОЧное \_ имя**</dt> <dt>( \| **тип тега 0xB \_ \_ стрингреф**)</dt> </dl>                  | Атрибут имени шаблона для исполняемой записи с подстановочным знаком в качестве имени файла.<br/>  |
| <span id="TAG_PRODUCT_NAME"></span><span id="tag_product_name"></span><dl> <dt>**Тег \_ \_Название продукта**</dt> <dt>( \| **тип тега \_ 0x10 \_ стрингреф**)</dt> </dl>                    | Атрибут имени продукта.<br/>                                                            |
| <span id="TAG_PRODUCT_VERSION"></span><span id="tag_product_version"></span><dl> <dt>**Тег \_ \_Версия продукта**</dt> <dt>( \| **тип тега \_ 0x11 \_ стрингреф**)</dt> </dl>           | Атрибут версии продукта.<br/>                                                         |
| <span id="TAG_FILE_DESCRIPTION"></span><span id="tag_file_description"></span><dl> <dt>**Тег \_ \_Описание файла**</dt> <dt>( \| **тип тега \_ 0x12 \_ стрингреф**)</dt> </dl>        | Атрибут описания файла.<br/>                                                        |
| <span id="TAG_FILE_VERSION"></span><span id="tag_file_version"></span><dl> <dt>**Тег \_ \_Версия файла**</dt> <dt>( \| **тип тега \_ 0x13 \_ стрингреф**)</dt> </dl>                    | Атрибут версии файла.<br/>                                                            |
| <span id="TAG_ORIGINAL_FILENAME"></span><span id="tag_original_filename"></span><dl> <dt>**Тег \_ ИСХОДНОЕ \_ имя файла**</dt> <dt>( \| **тип тега 0x14 \_ \_ стрингреф**)</dt> </dl>     | Исходный атрибут имени файла.<br/>                                                      |
| <span id="TAG_INTERNAL_NAME"></span><span id="tag_internal_name"></span><dl> <dt>**Тег \_ ВНУТРЕННЕЕ \_ имя**</dt> <dt>( \| **тип тега \_ 0x15 \_ стрингреф**)</dt> </dl>                 | Внутренний атрибут имени файла.<br/>                                                      |
| <span id="TAG_LEGAL_COPYRIGHT"></span><span id="tag_legal_copyright"></span><dl> <dt>**Тег \_ Юридическая информация \_ об авторских правах**</dt> <dt>( \| **тип тега 0x16 \_ \_ стрингреф**)</dt> </dl>           | Атрибут Copyright.<br/>                                                               |
| <span id="TAG_16BIT_DESCRIPTION"></span><span id="tag_16bit_description"></span><dl> <dt>**Tag \_ \_ Описание 16-разрядный**</dt> <dt>( \| **тип тега \_ 0x17 \_ стрингреф**)</dt> </dl>     | 16-разрядный атрибут Description.<br/>                                                      |
| <span id="TAG_APPHELP_DETAILS"></span><span id="tag_apphelp_details"></span><dl> <dt>**Тег \_ \_Сведения о APPHELP**</dt> <dt>( \| **тип тега 0x18 \_ \_ стрингреф**)</dt> </dl>           | Атрибут сведений о сообщении AppHelp.<br/>                                     |
| <span id="TAG_LINK_URL"></span><span id="tag_link_url"></span><dl> <dt>**Тег \_ \_URL-адрес ссылки**</dt> <dt>( \| **тип тега 0x19 \_ \_ стрингреф**)</dt> </dl>                                | Атрибут URL-адреса AppHelp Online Link.<br/>                                                 |
| <span id="TAG_LINK_TEXT"></span><span id="tag_link_text"></span><dl> <dt>**Тег \_ \_Текст ссылки**</dt> <dt>( \| **тип тега \_ 0x1a \_ стрингреф**)</dt> </dl>                             | Атрибут текста ссылки AppHelp в сети.<br/>                                                |
| <span id="TAG_APPHELP_TITLE"></span><span id="tag_apphelp_title"></span><dl> <dt>**Тег \_ \_Заголовок APPHELP**</dt> <dt>( \| **тип тега \_ 0x1B \_ стрингреф**)</dt> </dl>                 | Атрибут заголовка AppHelp.<br/>                                                           |
| <span id="TAG_APPHELP_CONTACT"></span><span id="tag_apphelp_contact"></span><dl> <dt>**Тег \_ \_Контакт APPHELP**</dt> <dt>( \| **тип тега \_ 0x1C \_ стрингреф**)</dt> </dl>           | Атрибут контакта AppHelp поставщика.<br/>                                                  |
| <span id="TAG_SXS_MANIFEST"></span><span id="tag_sxs_manifest"></span><dl> <dt>**Тег \_ \_Манифест SxS**</dt> <dt>( \| **тип тега \_ 0x1D \_ стрингреф**)</dt> </dl>                    | Параллельная запись манифеста.<br/>                                                       |
| <span id="TAG_DATA_STRING"></span><span id="tag_data_string"></span><dl> <dt>**Тег \_ \_Строка данных**</dt> <dt>( \| **тип тега \_ 0x1E \_ стрингреф**)</dt> </dl>                       | Строковый атрибут для ввода данных.<br/>                                                 |
| <span id="TAG_MSI_TRANSFORM_FILE"></span><span id="tag_msi_transform_file"></span><dl> <dt>**Тег \_ \_ \_ Файл преобразования MSI**</dt> <dt>( \| **тип тега \_ 0x1F \_ стрингреф**)</dt> </dl> | Атрибут имени файла для записи преобразования MSI.<br/>                                |
| <span id="TAG_16BIT_MODULE_NAME"></span><span id="tag_16bit_module_name"></span><dl> <dt>**Tag \_ 16-разрядный \_ \_ имя модуля**</dt> <dt>( \| **тип тега \_ 0x20 \_ стрингреф**)</dt> </dl>    | 16-разрядный атрибут имени модуля.<br/>                                                      |
| <span id="TAG_LAYER_DISPLAYNAME"></span><span id="tag_layer_displayname"></span><dl> <dt>**Тег \_ \_DisplayName слоя**</dt> <dt>( \| **тип тега \_ 0x21 \_ стрингреф**)</dt> </dl>     | Не используется.<br/>                                                                            |
| <span id="TAG_COMPILER_VERSION"></span><span id="tag_compiler_version"></span><dl> <dt>**Тег \_ \_Версия компилятора**</dt> <dt>( \| **тип тега \_ 0x22 \_ стрингреф**)</dt> </dl>        | Версия компилятора базы данных оболочек.<br/>                                                    |
| <span id="TAG_ACTION_TYPE"></span><span id="tag_action_type"></span><dl> <dt>**Тег \_ \_Тип действия**</dt> <dt>( \| **тип тега \_ 0x23 \_ стрингреф**)</dt> </dl>                       | Не используется.<br/>                                                                            |
| <span id="TAG_EXPORT_NAME"></span><span id="tag_export_name"></span><dl> <dt>**Тег \_ \_Имя экспорта**</dt> <dt>( \| **тип тега \_ 0x24 \_ стрингреф**)</dt> </dl>                       | Атрибут имени файла экспорта.<br/>                                                        |



Следующие записи имеют тип **тега \_ \_ DWORD** (0x4000).



| Константа/значение                                                                                                                                                                                                                                                                    | Описание                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| <span id="TAG_SIZE"></span><span id="tag_size"></span><dl> <dt>**Тег \_ Размер**</dt> <dt>(0x1 \| **\_ тип тега \_ DWORD**)</dt> </dl>                                                 | Атрибут размера файла.<br/>                                                                                  |
| <span id="TAG_OFFSET"></span><span id="tag_offset"></span><dl> <dt>**Тег \_ OFFSET**</dt> <dt>( \| **тип тега \_ 0x2 \_ DWORD**)</dt> </dl>                                           | Не используется.<br/>                                                                                               |
| <span id="TAG_CHECKSUM"></span><span id="tag_checksum"></span><dl> <dt>**Тег \_ CHECKSUM**</dt> <dt>( \| **тип тега \_ 0x3 \_ DWORD**)</dt> </dl>                                     | Атрибут контрольной суммы файла.<br/>                                                                              |
| <span id="TAG_SHIM_TAGID"></span><span id="tag_shim_tagid"></span><dl> <dt>**Тег \_ Оболочка совместимости \_ TAGID**</dt> <dt>( \| **тип тега 0x4 \_ \_ DWORD**)</dt> </dl>                              | Атрибут **TAGID** оболочки.<br/>                                                                             |
| <span id="TAG_PATCH_TAGID"></span><span id="tag_patch_tagid"></span><dl> <dt>**Тег \_ PATCH \_ TAGID**</dt> <dt>( \| **тип тега \_ 0x5 \_ DWORD**)</dt> </dl>                           | Атрибут **TAGID** patch.<br/>                                                                            |
| <span id="TAG_MODULE_TYPE"></span><span id="tag_module_type"></span><dl> <dt>**Тег \_ \_Тип модуля**</dt> <dt>( \| **тип тега \_ 0x6 \_ DWORD**)</dt> </dl>                           | Атрибут типа модуля.<br/>                                                                                |
| <span id="TAG_VERDATEHI"></span><span id="tag_verdatehi"></span><dl> <dt>**Тег \_ ВЕРДАТЕХИ**</dt> <dt>( \| **тип тега \_ 0x7 \_ DWORD**)</dt> </dl>                                  | Старшая часть атрибута даты версии файла.<br/>                                                |
| <span id="TAG_VERDATELO"></span><span id="tag_verdatelo"></span><dl> <dt>**Тег \_ ВЕРДАТЕЛО**</dt> <dt>( \| **тип тега \_ 0x8 \_ DWORD**)</dt> </dl>                                  | Часть атрибута даты версии файла с низким порядковым порядком.<br/>                                                 |
| <span id="TAG_VERFILEOS"></span><span id="tag_verfileos"></span><dl> <dt>**Тег \_ ВЕРФИЛЕОС**</dt> <dt>( \| **тип тега \_ 0x9 \_ DWORD**)</dt> </dl>                                  | Атрибут версии файла операционной системы.<br/>                                                              |
| <span id="TAG_VERFILETYPE"></span><span id="tag_verfiletype"></span><dl> <dt>**Тег \_ ВЕРФИЛЕТИПЕ**</dt> <dt>( \| **тип тега \_ 0xA \_ DWORD**)</dt> </dl>                            | Атрибут типа файла.<br/>                                                                                  |
| <span id="TAG_PE_CHECKSUM"></span><span id="tag_pe_checksum"></span><dl> <dt>**Тег \_ \_Контрольная сумма PE**</dt> <dt>( \| **тип тега 0xB \_ \_ DWORD**)</dt> </dl>                           | Атрибут CHECKSUM файла PE.<br/>                                                                           |
| <span id="TAG_PREVOSMAJORVER"></span><span id="tag_prevosmajorver"></span><dl> <dt>**Тег \_ ПРЕВОСМАЖОРВЕР**</dt> <dt>( \| **тип тега \_ 0xC \_ DWORD**)</dt> </dl>                   | Основной атрибут версии операционной системы.<br/>                                                             |
| <span id="TAG_PREVOSMINORVER"></span><span id="tag_prevosminorver"></span><dl> <dt>**Тег \_ ПРЕВОСМИНОРВЕР**</dt> <dt>( \| **тип тега \_ 0xD \_ DWORD**)</dt> </dl>                   | Дополнительный атрибут версии операционной системы.<br/>                                                             |
| <span id="TAG_PREVOSPLATFORMID"></span><span id="tag_prevosplatformid"></span><dl> <dt>**Тег \_ ПРЕВОСПЛАТФОРМИД**</dt> <dt>( \| **тип тега \_ 0xE \_ DWORD**)</dt> </dl>             | Атрибут идентификатора платформы операционной системы.<br/>                                                       |
| <span id="TAG_PREVOSBUILDNO"></span><span id="tag_prevosbuildno"></span><dl> <dt>**Тег \_ ПРЕВОСБУИЛДНО**</dt> <dt>( \| **тип тега \_ 0xF \_ DWORD**)</dt> </dl>                      | Атрибут номера сборки операционной системы.<br/>                                                              |
| <span id="TAG_PROBLEMSEVERITY"></span><span id="tag_problemseverity"></span><dl> <dt>**Тег \_ ПРОБЛЕМСЕВЕРИТИ**</dt> <dt>( \| **тип тега \_ 0x10 \_ DWORD**)</dt> </dl>               | Атрибут block записи AppHelp. Определяет, является ли приложение жесткой или программно заблокированным.<br/> |
| <span id="TAG_LANGID"></span><span id="tag_langid"></span><dl> <dt>**Тег \_ LANGID**</dt> <dt>( \| **тип тега \_ 0x11 \_ DWORD**)</dt> </dl>                                          | Идентификатор языка записи AppHelp.<br/>                                                              |
| <span id="TAG_VER_LANGUAGE"></span><span id="tag_ver_language"></span><dl> <dt>**Тег \_ VER \_ Language**</dt> <dt>( \| **тип тега \_ 0x12 \_ DWORD**)</dt> </dl>                       | Атрибут языковой версии файла.<br/>                                                                 |
| <span id="TAG_ENGINE"></span><span id="tag_engine"></span><dl> <dt>**Тег \_ ENGINE**</dt> <dt>( \| **тип тега \_ 0x14 \_ DWORD**)</dt> </dl>                                          | Не используется.<br/>                                                                                               |
| <span id="TAG_HTMLHELPID"></span><span id="tag_htmlhelpid"></span><dl> <dt>**Тег \_ ХТМЛХЕЛПИД**</dt> <dt>( \| **тип тега \_ 0x15 \_ DWORD**)</dt> </dl>                              | Атрибут идентификатора справки для записи AppHelp.<br/>                                                       |
| <span id="TAG_INDEX_FLAGS"></span><span id="tag_index_flags"></span><dl> <dt>**Тег \_ \_Флаги индекса**</dt> <dt>( \| **тип тега 0x16 \_ \_ DWORD**)</dt> </dl>                          | Атрибут Flags для записи индекса.<br/>                                                                   |
| <span id="TAG_FLAGS"></span><span id="tag_flags"></span><dl> <dt>**Тег \_ FLAGs**</dt> <dt>( \| **тип тега 0x17 \_ \_ DWORD**)</dt> </dl>                                             | Атрибут Flags для записи AppHelp.<br/>                                                                 |
| <span id="TAG_DATA_VALUETYPE"></span><span id="tag_data_valuetype"></span><dl> <dt>**Тег \_ \_ValueType данных**</dt> <dt>( \| **тип тега \_ 0x18 \_ DWORD**)</dt> </dl>                 | Атрибут типа данных для ввода данных.<br/>                                                                 |
| <span id="TAG_DATA_DWORD"></span><span id="tag_data_dword"></span><dl> <dt>**Тег \_ DATA \_ DWORD**</dt> <dt>( \| **тип тега \_ 0x19 \_ DWORD**)</dt> </dl>                             | Атрибут значения **DWORD** для ввода данных.<br/>                                                           |
| <span id="TAG_LAYER_TAGID"></span><span id="tag_layer_tagid"></span><dl> <dt>**Тег \_ LAYER \_ TAGID**</dt> <dt>( \| **тип тега \_ 0x1a \_ DWORD**)</dt> </dl>                          | Атрибут совместимости слоя **TAGID** .<br/>                                                                       |
| <span id="TAG_MSI_TRANSFORM_TAGID"></span><span id="tag_msi_transform_tagid"></span><dl> <dt>**Тег \_ \_ \_ TAGID преобразования MSI**</dt> <dt>( \| **тип тега \_ 0x1B \_ DWORD**)</dt> </dl> | Атрибут **TAGID** преобразования MSI.<br/>                                                                    |
| <span id="TAG_LINKER_VERSION"></span><span id="tag_linker_version"></span><dl> <dt>**Тег \_ \_Версия компоновщика**</dt> <dt>( \| **тип тега \_ 0x1C \_ DWORD**)</dt> </dl>                 | Атрибут версии компоновщика файла.<br/>                                                                   |
| <span id="TAG_LINK_DATE"></span><span id="tag_link_date"></span><dl> <dt>**Тег \_ \_Дата ссылки**</dt> <dt>( \| **тип тега \_ 0x1D \_ DWORD**)</dt> </dl>                                | Атрибут даты ссылки на файл.<br/>                                                                        |
| <span id="TAG_UPTO_LINK_DATE"></span><span id="tag_upto_link_date"></span><dl> <dt>**Тег \_ До \_ \_ даты связи**</dt> <dt>( \| **тип тега \_ 0x1E \_ DWORD**)</dt> </dl>                | Атрибут даты ссылки на файл. Сопоставление выполняется до и включает эту дату ссылки.<br/>                   |
| <span id="TAG_OS_SERVICE_PACK"></span><span id="tag_os_service_pack"></span><dl> <dt>**Тег \_ \_ \_ Пакет обновления ОС**</dt> <dt>( \| **\_ тип \_ DWORD-тега** 0x1F)</dt> </dl>             | Атрибут пакета обновления операционной системы для исполняемой записи.<br/>                                      |
| <span id="TAG_FLAG_TAGID"></span><span id="tag_flag_tagid"></span><dl> <dt>**Тег \_ FLAG \_ TAGID**</dt> <dt>( \| **тип тега \_ 0x20 \_ DWORD**)</dt> </dl>                             | Помечает атрибут **TAGID** .<br/>                                                                            |
| <span id="TAG_RUNTIME_PLATFORM"></span><span id="tag_runtime_platform"></span><dl> <dt>**Тег \_ \_Платформа среды выполнения**</dt> <dt>( \| **тип тега 0x21 \_ \_ DWORD**)</dt> </dl>           | Атрибут платформы времени выполнения файла.<br/>                                                                |
| <span id="TAG_OS_SKU"></span><span id="tag_os_sku"></span><dl> <dt>**Тег \_ \_SKU ОС**</dt> <dt>( \| **тип тега \_ 0x22 \_ DWORD**)</dt> </dl>                                         | Атрибут SKU операционной системы для исполняемой записи.<br/>                                               |
| <span id="TAG_OS_PLATFORM"></span><span id="tag_os_platform"></span><dl> <dt>**Тег \_ \_Платформа ОС**</dt> <dt>( \| **тип тега \_ 0x23 \_ DWORD**)</dt> </dl>                          | Атрибут платформы операционной системы.<br/>                                                                  |
| <span id="TAG_APP_NAME_RC_ID"></span><span id="tag_app_name_rc_id"></span><dl> <dt>**Тег \_ Имя приложения идентификатор версии- \_ \_ кандидата \_**</dt> <dt>( \| **тип тега 0x24 \_ \_ DWORD**)</dt> </dl>               | Атрибут идентификатора ресурса имени приложения для записей AppHelp.<br/>                                   |
| <span id="TAG_VENDOR_NAME_RC_ID"></span><span id="tag_vendor_name_rc_id"></span><dl> <dt>**Тег \_ Имя поставщика идентификатор версии- \_ \_ кандидата \_**</dt> <dt>( \| **тип тега 0x25 \_ \_ DWORD**)</dt> </dl>      | Атрибут идентификатора ресурса имени поставщика для записей AppHelp.<br/>                                        |
| <span id="TAG_SUMMARY_MSG_RC_ID"></span><span id="tag_summary_msg_rc_id"></span><dl> <dt>**Тег \_ Идентификатор версии- \_ \_ \_ кандидата сводного сообщения**</dt> <dt>( \| **тип тега 0x26 \_ \_ DWORD**)</dt> </dl>      | Атрибут идентификатора ресурса сводного сообщения для записей AppHelp.<br/>                                    |
| <span id="TAG_VISTA_SKU"></span><span id="tag_vista_sku"></span><dl> <dt>**Тег \_ \_SKU Vista**</dt> <dt>( \| **тип тега \_ 0x27 \_ DWORD**)</dt> </dl>                                | Windows Атрибут SKU Vista.<br/>                                                                          |
| <span id="TAG_DESCRIPTION_RC_ID"></span><span id="tag_description_rc_id"></span><dl> <dt>**Тег \_ Описание \_ \_ идентификатора версии-кандидата**</dt> <dt>( \| **тип тега 0x28 \_ \_ DWORD**)</dt> </dl>       | Описание атрибута идентификатора ресурса для записей AppHelp.<br/>                                        |
| <span id="TAG_PARAMETER1_RC_ID"></span><span id="tag_parameter1_rc_id"></span><dl> <dt>**Тег \_ ПАРАМЕТР1 \_ \_ идентификатор версии-кандидата**</dt> <dt>( \| **тип тега 0x29 \_ \_ DWORD**)</dt> </dl>          | Атрибут идентификатора ресурса параметр1 для записей AppHelp.<br/>                                         |
| <span id="TAG_TAGID"></span><span id="tag_tagid"></span><dl> <dt>**Тег \_ TAGID**</dt> <dt>( \| **тип тега \_ 0x801 \_ DWORD**)</dt> </dl>                                            | Атрибут **TAGID** .<br/>                                                                                  |



Следующая запись имеет тип **тега \_ \_ String** (0x8000).



| Константа/значение                                                                                                                                                                                                                                                            | Описание                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------|
| <span id="TAG_STRINGTABLE_ITEM"></span><span id="tag_stringtable_item"></span><dl> <dt>**Тег \_ \_Элемент stringTable**</dt> <dt>( \| **\_ \_ Строка типа тега** 0x801)</dt> </dl> | Запись элемента таблицы строк.<br/> |



Следующие записи имеют тип **тега \_ \_ null** (0x1000).



| Константа/значение                                                                                                                                                                                                                                                                            | Описание                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| <span id="TAG_INCLUDE"></span><span id="tag_include"></span><dl> <dt>**Тег \_ INCLUDE**</dt> <dt>(0x1 — \| **тип тега, \_ \_ null**)</dt> </dl>                                                 | Запись списка включения.<br/>                           |
| <span id="TAG_GENERAL"></span><span id="tag_general"></span><dl> <dt>**Тег \_ Общие**</dt> <dt>( \| **тип тега \_ 0x2 \_ null**)</dt> </dl>                                                 | Запись оболочки общего назначения.<br/>                   |
| <span id="TAG_MATCH_LOGIC_NOT"></span><span id="tag_match_logic_not"></span><dl> <dt>**Тег \_ \_ \_ Без логики соответствия**</dt> <dt>( \| **тип тега 0x3 \_ \_ null**)</dt> </dl>                       | НЕ соответствует записи логики.<br/>                  |
| <span id="TAG_APPLY_ALL_SHIMS"></span><span id="tag_apply_all_shims"></span><dl> <dt>**Тег \_ ПРИМЕНИТЬ \_ все \_ оболочки совместимости**</dt> <dt>( \| **тип тега \_ 0x4 \_ null**)</dt> </dl>                       | Не используется.<br/>                                       |
| <span id="TAG_USE_SERVICE_PACK_FILES"></span><span id="tag_use_service_pack_files"></span><dl> <dt>**Тег \_ ИСПОЛЬЗОВАТЬ \_ \_ \_ файлы пакетов обновления**</dt> <dt>( \| **тип тега \_ 0x5 \_ null**)</dt> </dl> | Сведения о пакете обновления для записей AppHelp.<br/> |
| <span id="TAG_MITIGATION_OS"></span><span id="tag_mitigation_os"></span><dl> <dt>**Тег \_ \_ОС для устранения рисков**</dt> <dt>( \| **тип тега 0x6 \_ \_ null**)</dt> </dl>                              | Устранение рисков при вводе в области операционной системы.<br/>   |
| <span id="TAG_BLOCK_UPGRADE"></span><span id="tag_block_upgrade"></span><dl> <dt>**Тег \_ БЛОКИРОВАТЬ \_ Обновление**</dt> <dt>( \| **тип тега \_ 0x7 \_ null**)</dt> </dl>                              | Запись блока обновления.<br/>                          |
| <span id="TAG_INCLUDEEXCLUDEDLL"></span><span id="tag_includeexcludedll"></span><dl> <dt>**Тег \_ ИНКЛУДИКСКЛУДЕДЛЛ**</dt> <dt>( \| **тип тега \_ 0x8 \_ null**)</dt> </dl>                   | Запись включения или исключения библиотеки DLL.<br/>                    |



Следующие записи имеют тип **тега \_ \_ QWORD** (0x5000).



| Константа/значение                                                                                                                                                                                                                                                                                   | Описание                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TAG_TIME"></span><span id="tag_time"></span><dl> <dt>**Тег \_ ВРЕМЯ**</dt> <dt>(0x1 \| **тип тега, \_ \_ QWORD**)</dt> </dl>                                                                | Атрибут времени.<br/>                                                                                     |
| <span id="TAG_BIN_FILE_VERSION"></span><span id="tag_bin_file_version"></span><dl> <dt>**Тег \_ \_ \_ Версия файла BIN**</dt> <dt>( \| **тип тега 0x2, \_ \_ QWORD**)</dt> </dl>                          | Атрибут версии файла bin для записей файлов.<br/>                                                        |
| <span id="TAG_BIN_PRODUCT_VERSION"></span><span id="tag_bin_product_version"></span><dl> <dt>**Тег \_ \_ \_ Версия продукта bin**</dt> <dt>( \| **тип тега \_ 0x3 \_ QWORD**)</dt> </dl>                 | Атрибут версии bin для записей файлов.<br/>                                                     |
| <span id="TAG_MODTIME"></span><span id="tag_modtime"></span><dl> <dt>**Тег \_ МОДТИМЕ**</dt> <dt>( \| **тип тега 0x4, \_ \_ QWORD**)</dt> </dl>                                                       | Не используется.<br/>                                                                                             |
| <span id="TAG_FLAG_MASK_KERNEL"></span><span id="tag_flag_mask_kernel"></span><dl> <dt>**Тег \_ \_ \_ Ядро флага маски**</dt> <dt>( \| **\_ тип тега \_** 0x5)</dt> </dl>                          | Атрибут маски флага ядра.<br/>                                                                         |
| <span id="TAG_UPTO_BIN_PRODUCT_VERSION"></span><span id="tag_upto_bin_product_version"></span><dl> <dt>**Тег \_ До \_ \_ \_ версии продукта bin**</dt> <dt>( \| **тип тега \_ 0x6 \_ QWORD**)</dt> </dl> | Атрибут версии bin для файла. Сопоставление выполняется до и включает эту версию продукта.<br/> |
| <span id="TAG_DATA_QWORD"></span><span id="tag_data_qword"></span><dl> <dt>**Тег \_ \_QWORD данных**</dt> <dt>( \| **тип тега 0x7, \_ \_ QWORD**)</dt> </dl>                                             | Атрибут значения **улонглонг** для ввода данных.<br/>                                                     |
| <span id="TAG_FLAG_MASK_USER"></span><span id="tag_flag_mask_user"></span><dl> <dt>**Тег \_ ФЛАГ \_ \_ пользователя маски**</dt> <dt>( \| **тип тега 0x8 — \_ \_ QWORD**)</dt> </dl>                                | Атрибут маски флага пользователя.<br/>                                                                           |
| <span id="TAG_FLAGS_NTVDM1"></span><span id="tag_flags_ntvdm1"></span><dl> <dt>**Тег \_ FLAGs \_ NTVDM1**</dt> <dt>( \| **тип тега 0x9, \_ \_ QWORD**)</dt> </dl>                                       | Атрибут маски флага NTVDM1.<br/>                                                                         |
| <span id="TAG_FLAGS_NTVDM2"></span><span id="tag_flags_ntvdm2"></span><dl> <dt>**Тег \_ FLAGs \_ NTVDM2**</dt> <dt>( \| **тип тега 0xA, \_ \_ QWORD**)</dt> </dl>                                       | Атрибут маски флага NTVDM2.<br/>                                                                         |
| <span id="TAG_FLAGS_NTVDM3"></span><span id="tag_flags_ntvdm3"></span><dl> <dt>**Тег \_ FLAGs \_ NTVDM3**</dt> <dt>( \| **тип тега 0xB \_ \_ QWORD**)</dt> </dl>                                       | Атрибут маски флага NTVDM3.<br/>                                                                         |
| <span id="TAG_FLAG_MASK_SHELL"></span><span id="tag_flag_mask_shell"></span><dl> <dt>**Тег \_ Пометка \_ \_ оболочки маски**</dt> <dt>( \| **тип тега 0xC \_ \_ QWORD**)</dt> </dl>                             | Атрибут маски флага оболочки.<br/>                                                                          |
| <span id="TAG_UPTO_BIN_FILE_VERSION"></span><span id="tag_upto_bin_file_version"></span><dl> <dt>**Тег \_ Не \_ более \_ \_ версии файла BIN**</dt> <dt>( \| **тип тега 0xD ( \_ \_ QWORD**))</dt> </dl>          | Атрибут версии файла BIN файла. Сопоставление выполняется до и включает эту версию файла.<br/>       |
| <span id="TAG_FLAG_MASK_FUSION"></span><span id="tag_flag_mask_fusion"></span><dl> <dt>**Тег \_ Пометить \_ \_ Fusion маски**</dt> <dt>( \| **тип тега 0xE \_ \_ QWORD**)</dt> </dl>                          | Атрибут маски флага Fusion.<br/>                                                                         |
| <span id="TAG_FLAG_PROCESSPARAM"></span><span id="tag_flag_processparam"></span><dl> <dt>**Тег \_ FLAG \_ процесспарам**</dt> <dt>( \| **тип тега \_ 0xF \_ QWORD**)</dt> </dl>                        | Атрибут "Process param" флаг.<br/>                                                                       |
| <span id="TAG_FLAG_LUA"></span><span id="tag_flag_lua"></span><dl> <dt>**Тег \_ Пометка \_ Lua**</dt> <dt>( \| **тип тега 0x10, \_ \_ QWORD**)</dt> </dl>                                                  | Атрибут флага LUA.<br/>                                                                                 |
| <span id="TAG_FLAG_INSTALL"></span><span id="tag_flag_install"></span><dl> <dt>**Тег \_ \_Установить флаг установки**</dt> <dt>( \| **тип тега 0x11 \_ \_ QWORD**)</dt> </dl>                                      | Атрибут флага установки.<br/>                                                                             |



Следующие записи имеют тип **тегов \_ \_ binary** (0x9000).



| Константа/значение                                                                                                                                                                                                                                                     | Описание                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span id="TAG_PATCH_BITS"></span><span id="tag_patch_bits"></span><dl> <dt>**Тег \_ \_Биты исправления**</dt> <dt>( \| **\_ \_ двоичный тип тега** 0x2)</dt> </dl>              | Атрибут битов файла исправления.<br/>                          |
| <span id="TAG_FILE_BITS"></span><span id="tag_file_bits"></span><dl> <dt>**Тег \_ \_Биты файлов**</dt> <dt>( \| **тип тега \_ 0x3 \_ binary**)</dt> </dl>                 | Атрибут битов файла.<br/>                                |
| <span id="TAG_EXE_ID"></span><span id="tag_exe_id"></span><dl> <dt>**Тег \_ \_ИД exe**</dt> <dt>- \| **файла ( \_ тип \_ тега** 0x4)</dt> </dl>                          | Атрибут **GUID** исполняемого элемента.<br/>          |
| <span id="TAG_DATA_BITS"></span><span id="tag_data_bits"></span><dl> <dt>**Тег \_ \_Биты данных**</dt> <dt>( \| **\_ \_ двоичный тип тега** 0x5)</dt> </dl>                 | Атрибут битов данных.<br/>                                |
| <span id="TAG_MSI_PACKAGE_ID"></span><span id="tag_msi_package_id"></span><dl> <dt>**Тег \_ \_ \_ Идентификатор пакета MSI**</dt> <dt>( \| **тип тега \_ 0x6 \_ binary**)</dt> </dl> | Атрибут идентификатора пакета MSI пакета MSI.<br/> |
| <span id="TAG_DATABASE_ID"></span><span id="tag_database_id"></span><dl> <dt>**Тег \_ \_Идентификатор базы данных**</dt> <dt>( \| **\_ тип тега \_** 0x7)</dt> </dl>           | Атрибут **GUID** базы данных.<br/>                   |
| <span id="TAG_INDEX_BITS"></span><span id="tag_index_bits"></span><dl> <dt>**Тег \_ \_Биты индекса**</dt> <dt>( \| **\_ \_ двоичный тип тега** 0x801)</dt> </dl>            | Атрибут битов индекса.<br/>                               |



Следующие записи имеют тип **тега \_ \_ Word** (0x3000).



| Константа/значение                                                                                                                                                                                                                                      | Описание                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| <span id="TAG_MATCH_MODE"></span><span id="tag_match_mode"></span><dl> <dt>**Тег \_ \_Режим соответствия**</dt> <dt>(0x1 \| **тип тега, \_ \_ слово**)</dt> </dl> | Атрибут режима соответствия.<br/>                   |
| <span id="TAG_TAG"></span><span id="tag_tag"></span><dl> <dt>**Тег \_ TAG**</dt> <dt>( \| **тип тега \_ 0x801 \_ слово**)</dt> </dl>                     | Запись ТЕГА.<br/>                              |
| <span id="TAG_INDEX_TAG"></span><span id="tag_index_tag"></span><dl> <dt>**Тег \_ \_Тег index**</dt> <dt>( \| **тип тега \_ 0x802 \_ слово**)</dt> </dl>  | Атрибут ТЕГА index для записи индекса.<br/> |
| <span id="TAG_INDEX_KEY"></span><span id="tag_index_key"></span><dl> <dt>**Тег \_ \_Ключ индекса**</dt> <dt>( \| **\_ \_ слово типа тега** 0x803)</dt> </dl>  | Ключевой атрибут индекса для записи индекса.<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Exposeenums2managed. h (включение Аксекстенденумс. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Типы тегов](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> <dt>

[**тагреф**](tagref.md)
</dt> </dl>

 

 




