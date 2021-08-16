---
description: 'Набор строковых ключей, которые используются с методом IBindCtx:: Регистеробжектпарам для указания контекста привязки.'
title: Ключи строк контекста привязки (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d89a0ee1-9a4b-48a4-8965-0d92f09743a6
api_name:
- STR_AVOID_DRIVE_RESTRICTION_POLICY
- STR_BIND_DELEGATE_CREATE_OBJECT
- STR_BIND_FOLDER_ENUM_MODE
- STR_BIND_FOLDERS_READ_ONLY
- STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE
- STR_DONT_PARSE_RELATIVE
- STR_DONT_RESOLVE_LINK
- STR_FILE_SYS_FIND_DATA
- STR_FILE_SYS_BIND_DATA_WIN7_FORMAT
- STR_GET_ASYNC_HANDLER
- STR_GPS_BESTEFFORT
- STR_GPS_DELAYCREATION
- STR_GPS_FASTPROPERTIESONLY
- STR_GPS_HANDLERPROPERTIESONLY
- STR_GPS_NO_OPLOCK
- STR_GPS_OPENSLOWITEM
- STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK
- STR_IFILTER_LOAD_DEFINED_FILTER
- STR_INTERNAL_NAVIGATE
- STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE
- STR_ITEM_CACHE_CONTEXT
- STR_NO_VALIDATE_FILENAME_CHARS
- STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS
- STR_PARSE_AND_CREATE_ITEM
- STR_PARSE_DONT_REQUIRE_VALIDATED_URLS
- STR_PARSE_PARTIAL_IDLIST
- STR_PARSE_PREFER_FOLDER_BROWSING
- STR_PARSE_PREFER_WEB_BROWSING
- STR_PARSE_PROPERTYSTORE
- STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS
- STR_PARSE_SHOW_NET_DIAGNOSTICS_UI
- STR_PARSE_SKIP_NET_CACHE
- STR_PARSE_TRANSLATE_ALIASES
- STR_PARSE_WITH_PROPERTIES
- STR_PROPERTYBAG_PARAM
- STR_SKIP_BINDING_CLSID
- STR_TRACK_CLSID
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 78743f18f9dc10b9c20b7e911224f1cd4e53e3f536f23686936a8f021605bf9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452051"
---
# <a name="bind-context-string-keys"></a>Ключи строк контекста привязки

Набор строковых ключей, которые используются с методом [**IBindCtx:: регистеробжектпарам**](/windows/win32/api/objidl/nf-objidl-ibindctx-registerobjectparam) для указания контекста привязки.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Константа</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="STR_AVOID_DRIVE_RESTRICTION_POLICY"></span><span id="str_avoid_drive_restriction_policy"></span><dl> <dt><strong>STR_AVOID_DRIVE_RESTRICTION_POLICY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>введено в Windows XP SP2</strong>. Укажите этот контекст привязки, чтобы разрешить клиентам источника данных переопределять политику скрытых букв диска и предоставлять доступ к объектам представления для источников данных на заблокированных дисках.<br/> Используется с <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>ишеллфолдер:: биндтубжект</strong></a> или <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>интерфейса IShellItem:: биндтохандлер</strong></a>.<br/> система поддерживает политики, управляемые администратором, которые скрывают указанные буквы дисков, чтобы запретить пользователям доступ к этим дискам через обозреватель Windows. Если эта политика активна, в результате объекты представления и другие обработчики, созданные с помощью метода <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject"><strong>ишеллфолдер:: креатевиевобжект</strong></a> , будут завершаться ошибкой при вызове на дисках, заблокированных политикой.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_BIND_DELEGATE_CREATE_OBJECT"></span><span id="str_bind_delegate_create_object"></span><dl> <dt><strong>STR_BIND_DELEGATE_CREATE_OBJECT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows Vista</strong>. Укажите этот контекст привязки, чтобы метод <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>ишеллфолдер:: биндтубжект</strong></a> использовал объект, указанный параметром <em>ПБК</em> , для создания целевого объекта. в этом случае объект, указанный параметром <em>Punk</em> в вызове <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx:: регистеробжектпарам</strong></a> , должен реализовать интерфейс <a href="/windows/desktop/api/Propsys/nn-propsys-icreateobject"><strong>икреатеобжект</strong></a> . <br/> Используется с <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>ишеллфолдер:: биндтубжект</strong></a> или <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>интерфейса IShellItem:: биндтохандлер</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_BIND_FOLDER_ENUM_MODE"></span><span id="str_bind_folder_enum_mode"></span><dl> <dt><strong>STR_BIND_FOLDER_ENUM_MODE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows 7</strong>. Передается в <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>ишеллфолдер::P арседисплайнаме</strong></a> со значением <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folder_enum_mode"><strong>FOLDER_ENUM_MODE</strong></a> для управления режимом перечисления проанализированного элемента. Значение <strong>FOLDER_ENUM_MODE</strong> передается в контексте привязки через объект, реализующий <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithfolderenummode"><strong>иобжектвисфолдеренуммоде</strong></a>. <br/> Элементы с различными режимами перечисления сравниваются по-разному (SHCIDS_CANONICALONLY), так как они перечисляют различные наборы элементов.<br/> Если элемент не поддерживает режим перечисления (поскольку он не является папкой или не предоставляет режим перечисления), то он создается в режиме перечисления по умолчанию.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_BIND_FOLDERS_READ_ONLY"></span><span id="str_bind_folders_read_only"></span><dl> <dt><strong>STR_BIND_FOLDERS_READ_ONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows 7</strong>. Передается в <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>ишеллфолдер::P арседисплайнаме</strong></a> вместе с <strong>STR_FILE_SYS_BIND_DATA</strong>. Это вызывает простой анализ, а также проверяет наличие файлов Desktop.ini по пути, из которого получается локализованная строка имени. Это позволяет избежать поиска папок по пути, который, в случае с папкой, представляющей сервер или общую папку, может занять много времени и ресурсов. Desktop.ini файлы кэшируются в некоторых расположениях, поэтому они будут по крайней мере настолько эффективны, как проверка атрибутов папок, а затем зондирование на Desktop.ini если эта папка должна включать подразделение «только для чтения».<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE"></span><span id="str_bind_force_folder_shortcut_resolve"></span><dl> <dt><strong>STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>введено в Windows XP SP2</strong>. Укажите этот контекст привязки, чтобы принудительно использовать ярлык папки для разрешения ссылки, указывающей на ее целевой объект. <br/> Ярлык папки — это элемент папки, указывающий на другой элемент папки в том же пространстве имен с помощью ссылки (ярлыка) для хранения IDList целевого объекта. Ссылка разрешается для наблюдения за целевым объектом в случае его перемещения или переименования. например, папка Windows XP " <strong>мое сетевое окружение</strong> " и папка <strong>компьютера</strong> Windows Vista могут содержать ярлыки папок, созданные с помощью мастера <strong>добавления сетевого расположения</strong> . Для повышения производительности метод <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>ишеллфолдер:: биндтубжект</strong></a> по умолчанию не разрешает ссылки на сетевую папку.<br/> Используется с <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>ишеллфолдер:: биндтубжект</strong></a> или <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>интерфейса IShellItem:: биндтохандлер</strong></a>. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_DONT_PARSE_RELATIVE"></span><span id="str_dont_parse_relative"></span><dl> <dt><strong>STR_DONT_PARSE_RELATIVE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows XP</strong>. Укажите этот контекст привязки, чтобы запретить вызов метода <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>ишеллфолдер::P арседисплайнаме</strong></a> в папке <strong>настольных систем</strong> от обработки относительных путей относительно рабочего стола. в этом случае синтаксический анализ завершается ошибкой, если указан контекст привязки.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_DONT_RESOLVE_LINK"></span><span id="str_dont_resolve_link"></span><dl> <dt><strong>STR_DONT_RESOLVE_LINK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows Vista</strong>. Укажите этот контекст привязки, чтобы указать <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>интерфейса IShellItem</strong></a> не разрешать целевой объект ссылки, полученный при использовании идентификатора GUID <strong>BHID_LinkTargetItem</strong> в <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>интерфейса IShellItem:: биндтохандлер</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_FILE_SYS_FIND_DATA"></span><span id="str_file_sys_find_data"></span><dl> <dt><strong>STR_FILE_SYS_FIND_DATA</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows XP</strong>. Укажите этот контекст привязки, чтобы предоставить метаданные файла методу <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>ишеллфолдер::P арседисплайнаме</strong></a> , который используется вместо попытки получения фактических метаданных файла. Связанный объект должен реализовывать <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>ифилесистембинддата</strong></a> и при необходимости также реализовывать <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata2"><strong>IFileSystemBindData2</strong></a>. По умолчанию метод <strong>ишеллфолдер::P арседисплайнаме</strong> проверяет, существует ли файл, и использует фактические метаданные файла для заполнения списка идентификаторов.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_FILE_SYS_BIND_DATA_WIN7_FORMAT"></span><span id="str_file_sys_bind_data_win7_format"></span><dl> <dt><strong>STR_FILE_SYS_BIND_DATA_WIN7_FORMAT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Введено в Windows 8.1</strong>. укажите этот контекст привязки, чтобы указать, что данные, предоставленные в контексте привязки <strong>STR_FILE_SYS_FIND_DATA</strong> , должны использоваться для создания списка ItemID в формате Windows 7.&quot;<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GET_ASYNC_HANDLER"></span><span id="str_get_async_handler"></span><dl> <dt><strong>STR_GET_ASYNC_HANDLER</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows 7</strong>. Укажите этот контекст привязки при извлечении обработчика в том же потоке, что и пользовательский интерфейс. Следует избегать любых операций, интенсивно использующих память, таких как связанные с диском или сетевым доступом.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_BESTEFFORT"></span><span id="str_gps_besteffort"></span><dl> <dt><strong>STR_GPS_BESTEFFORT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows Vista</strong>. Укажите этот контекст привязки при запросе обработчика <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> или <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>ипропертисторе</strong></a> . Это значение используется с <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>ишеллфолдер:: биндтубжект</strong></a>. Дополнительные сведения см. в описании флага <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_BESTEFFORT</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_DELAYCREATION"></span><span id="str_gps_delaycreation"></span><dl> <dt><strong>STR_GPS_DELAYCREATION</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows Vista</strong>. Укажите этот контекст привязки при запросе обработчика <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> или <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>ипропертисторе</strong></a> . Это значение используется с <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>ишеллфолдер:: биндтубжект</strong></a>. Дополнительные сведения см. в описании флага <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_DELAYCREATION</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_FASTPROPERTIESONLY"></span><span id="str_gps_fastpropertiesonly"></span><dl> <dt><strong>STR_GPS_FASTPROPERTIESONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows Vista</strong>. Укажите этот контекст привязки при запросе обработчика <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> или <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>ипропертисторе</strong></a> . Это значение используется с <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>ишеллфолдер:: биндтубжект</strong></a>. Дополнительные сведения см. в описании флага <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_FASTPROPERTIESONLY</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_HANDLERPROPERTIESONLY"></span><span id="str_gps_handlerpropertiesonly"></span><dl> <dt><strong>STR_GPS_HANDLERPROPERTIESONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows Vista</strong>. Укажите этот контекст привязки при запросе обработчика <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> или <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>ипропертисторе</strong></a> . Это значение используется с <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>ишеллфолдер:: биндтубжект</strong></a>. Дополнительные сведения см. в описании флага <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_HANDLERPROPERTIESONLY</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_NO_OPLOCK"></span><span id="str_gps_no_oplock"></span><dl> <dt><strong>STR_GPS_NO_OPLOCK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows 7</strong>. Укажите этот контекст привязки при запросе обработчика <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> или <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>ипропертисторе</strong></a> . Это значение используется с <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>ишеллфолдер:: биндтубжект</strong></a>. Дополнительные сведения см. в описании флага <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_NO_OPLOCK</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_OPENSLOWITEM"></span><span id="str_gps_openslowitem"></span><dl> <dt><strong>STR_GPS_OPENSLOWITEM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows Vista</strong>. Укажите этот контекст привязки при запросе обработчика <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> или <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>ипропертисторе</strong></a> . Это значение используется с <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>ишеллфолдер:: биндтубжект</strong></a>. Дополнительные сведения см. в описании флага <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_OPENSLOWITEM</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK"></span><span id="str_ifilter_force_text_filter_fallback"></span><dl> <dt><strong>STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Windows Только Vista.</strong> Укажите этот контекст привязки, чтобы вызвать метод <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>ишеллфолдер:: биндтубжект</strong></a> , который запрашивает интерфейс <a href="/windows/desktop/api/filter/nn-filter-ifilter"><strong>IFilter</strong></a> для объекта файловой системы, чтобы возвратить текстовый фильтр, если другие фильтры недоступны. это значение не определено на Windows 7.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_IFILTER_LOAD_DEFINED_FILTER"></span><span id="str_ifilter_load_defined_filter"></span><dl> <dt><strong>STR_IFILTER_LOAD_DEFINED_FILTER</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Windows Только Vista.</strong> Укажите этот контекст привязки, чтобы вызвать метод <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>ишеллфолдер:: биндтубжект</strong></a> , который запрашивает интерфейс <a href="/windows/desktop/api/filter/nn-filter-ifilter"><strong>IFilter</strong></a> для объекта файловой системы, не возвращая резервный фильтр, если не удалось найти зарегистрированный фильтр.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_INTERNAL_NAVIGATE"></span><span id="str_internal_navigate"></span><dl> <dt><strong>STR_INTERNAL_NAVIGATE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows Vista</strong>. Укажите этот контекст привязки, чтобы включить загрузку журнала из потока для внутренней навигации при вызове метода <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768216(v=vs.85)"><strong>иперсиссистори:: LoadHistory</strong></a> . Внутренняя навигация — это Навигация в одном и том же представлении.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE"></span><span id="str_internetfolder_parse_only_urlmon_bindable"></span><dl> <dt><strong>STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows 7</strong>. Укажите этот контекст привязки с STR_PARSE_PREFER_FOLDER_BROWSING, когда клиент хочет, чтобы обработчики папок оболочки Интернета создавали IDList для любого допустимого URL-адреса, если не удается создать папку DAV-Type для этого URL-адреса. URL-адрес не проверен на существование; проверяется только его синтаксис и зарегистрированный обработчик протокола.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_ITEM_CACHE_CONTEXT"></span><span id="str_item_cache_context"></span><dl> <dt><strong>STR_ITEM_CACHE_CONTEXT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows 7</strong>. Укажите этот контекст привязки, чтобы указать реализации <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>ишеллфолдер::P арседисплайнаме</strong></a> и <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3:: инитиализикс</strong></a> для кэширования вспомогательных объектов, интенсивно использующих память, которые могут существовать во время создания экземпляров элементов оболочки, а не повторно создавать эти объекты при каждом создании элемента оболочки. Связанный объект является другим объектом контекста привязки, изначально пустым. Это должно привести к созданию отдельного объекта контекста привязки, доступ к которому осуществляется через <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam"><strong>IBindCtx:: жетобжектпарам</strong></a> или <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx:: Register. обжектпарам</strong></a>. <br/> Вызывающий объект должен принять это поведение, предоставив этот параметр контекста привязки при вызове <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>шкреатеитемфромпарсингнаме</strong></a>. Это позволяет оптимизировать поведение привязки к нескольким именам синтаксического анализа в случае успеха. Время существования объекта контекста привязки должно охватывать несколько экземпляров элементов оболочки и их отдельные контексты привязки.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_NO_VALIDATE_FILENAME_CHARS"></span><span id="str_no_validate_filename_chars"></span><dl> <dt><strong>STR_NO_VALIDATE_FILENAME_CHARS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows Vista</strong>. Укажите этот контекст привязки, чтобы разрешить отображение недопустимых символов имени файла в именах файлов. По умолчанию вызов метода <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>ишеллфолдер::P арседисплайнаме</strong></a> отклоняет символы, недопустимые в именах файлов. Этот контекст привязки имеет смысл только в сочетании с контекстом привязки STR_FILE_SYS_FIND_DATA.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS"></span><span id="str_parse_allow_internet_shell_folders"></span><dl> <dt><strong>STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows Vista</strong>. Укажите этот контекст привязки, чтобы разрешить вызов метода <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>ишеллфолдер::P арседисплайнаме</strong></a> в папке <strong>Desktop</strong> для анализа URL-адресов. Если указан контекст привязки, он переопределяет <strong><strong>STR_PARSE_PREFER_WEB_BROWSING</strong></strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_AND_CREATE_ITEM"></span><span id="str_parse_and_create_item"></span><dl> <dt><strong>STR_PARSE_AND_CREATE_ITEM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows 7</strong>. Укажите этот контекст привязки, чтобы дать указание реализации <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>ишеллфолдер::P арседисплайнаме</strong></a> , чтобы оптимизировать поведение <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>шкреатеитемфромпарсингнаме</strong></a>. <br/> Как правило, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>шкреатеитемфромпарсингнаме</strong></a> выполняет две операции привязки к имени, которое необходимо проанализировать: один от и один к <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>Ишеллфолдер::P арседисплайнаме</strong></a> и один для создания элемента оболочки. Если контекст привязки <strong>STR_PARSE_AND_CREATE_ITEM</strong> поддерживается, вторую привязку можно избежать, создав элемент оболочки во время <strong>Ишеллфолдер::P арседисплайнаме</strong> привязку и сохранение элемента оболочки через <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iparseandcreateitem-setitem"><strong>ипарсеандкреатеитем:: сетитем</strong></a>. Затем <strong>шкреатеитемфромпарсингнаме</strong> использует сохраненный элемент оболочки вместо того, чтобы создавать его.<br/> Этот параметр применяется к последнему элементу анализируемого имени. Например, в имени &quot;C:\Folder1\File.txt данные применяются к File.txt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_DONT_REQUIRE_VALIDATED_URLS"></span><span id="str_parse_dont_require_validated_urls"></span><dl> <dt><strong>STR_PARSE_DONT_REQUIRE_VALIDATED_URLS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Windows Только Vista.</strong> Указывает, что при синтаксическом анализе URL-адреса этот контекст привязки не должен требовать существования URL-адреса перед созданием для него IDList. Укажите этот контекст привязки вместе с <strong><strong>STR_PARSE_PREFER_FOLDER_BROWSING</strong></strong> , когда клиент хочет, чтобы обработчики папок <strong>Internet Shell</strong> создавали IDList для URL-адреса, если не удается создать папку DAV для данного URL-адреса.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_PARTIAL_IDLIST"></span><span id="str_parse_partial_idlist"></span><dl> <dt><strong>STR_PARSE_PARTIAL_IDLIST</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows Vista</strong>. Укажите этот контекст привязки, чтобы передать исходный элемент, который повторно анализируется, если этот элемент хранится в виде объекта <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>интерфейса IShellItem</strong></a> , который также реализует интерфейс <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>ипарентандитем</strong></a> . до Windows 7 это значение не было определено в файле заголовка. Он может быть определен вызывающим объектом или передан как его строковое значение <strong>L &quot; парсеоригиналитем &quot; </strong>. начиная с Windows 7, значение определяется в шлобж. h. Обратите внимание, что этот заголовок отличается от других констант STR.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_PREFER_FOLDER_BROWSING"></span><span id="str_parse_prefer_folder_browsing"></span><dl> <dt><strong>STR_PARSE_PREFER_FOLDER_BROWSING</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows XP</strong>. Укажите этот контекст привязки, чтобы разрешить вызов метода <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>ишеллфолдер::P арседисплайнаме</strong></a> в папке <strong>Desktop</strong> для анализа URL-адресов, как если бы они были папками. Используйте этот контекст привязки для привязки к серверу WebDAV.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_PREFER_WEB_BROWSING"></span><span id="str_parse_prefer_web_browsing"></span><dl> <dt><strong>STR_PARSE_PREFER_WEB_BROWSING</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows Vista</strong>. Укажите этот контекст привязки, чтобы предотвратить вызов метода <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>ишеллфолдер::P арседисплайнаме</strong></a> в папке " <strong>Рабочий стол</strong> " в форме "URL-адреса для анализа". Этот контекст привязки может быть переопределен <strong><strong>STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS</strong></strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_PROPERTYSTORE"></span><span id="str_parse_propertystore"></span><dl> <dt><strong>STR_PARSE_PROPERTYSTORE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows Vista</strong>. Укажите этот контекст привязки, чтобы переопределить хранилище свойств по умолчанию, используемое методом <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>ишеллфолдер::P арседисплайнаме</strong></a> , и используйте вместо этого хранилище свойств, указанное в качестве параметра привязки. Применяется к папкам делегирования.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS"></span><span id="str_parse_shell_protocol_to_file_objects"></span><dl> <dt><strong>STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>введено в Windows XP SP2</strong>. Укажите этот контекст привязки, чтобы разрешить вызов метода <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>ишеллфолдер::P арседисплайнаме</strong></a> в папке <strong>Desktop</strong> , чтобы использовать &quot; &quot; нотацию оболочки: prefix для доступа к файлам.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_SHOW_NET_DIAGNOSTICS_UI"></span><span id="str_parse_show_net_diagnostics_ui"></span><dl> <dt><strong>STR_PARSE_SHOW_NET_DIAGNOSTICS_UI</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows Vista</strong>. Укажите этот контекст привязки, чтобы вызвать метод <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>ишеллфолдер::P арседисплайнаме</strong></a> для вывода диалогового окна диагностики сети в случае сбоя анализа сетевого пути.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_SKIP_NET_CACHE"></span><span id="str_parse_skip_net_cache"></span><dl> <dt><strong>STR_PARSE_SKIP_NET_CACHE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows Vista</strong>. Укажите этот контекст привязки, чтобы вызвать метод <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>ишеллфолдер::P арседисплайнаме</strong></a> для пропуска проверки кэша общих сетевых ресурсов и непосредственного обращения к сетевому серверу. Сведения о сетевых ресурсах кэшируются для повышения производительности и <strong>ишеллфолдер::P арседисплайнаме</strong> проверяет этот кэш по умолчанию.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_TRANSLATE_ALIASES"></span><span id="str_parse_translate_aliases"></span><dl> <dt><strong>STR_PARSE_TRANSLATE_ALIASES</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows XP</strong>. Укажите этот контекст привязки, чтобы передать проанализированные свойства методу <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>ишеллфолдер::P арседисплайнаме</strong></a> для пространства имен делегата. Пространство имен может использовать переданные свойства вместо того, чтобы пытаться проанализировать само имя.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_WITH_PROPERTIES"></span><span id="str_parse_with_properties"></span><dl> <dt><strong>STR_PARSE_WITH_PROPERTIES</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Windows Только Vista.</strong> Контекст привязки синтаксического анализа, который используется для передачи набора свойств и имени элемента при вызове <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>ишеллфолдер::P арседисплайнаме</strong></a>. Объект в контексте привязки реализует <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>ипропертисторе</strong></a> и извлекается путем вызова <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam"><strong>IBindCtx:: жетобжектпарам</strong></a>.<br/> Дбфолдер — это источник данных оболочки, представляющий элементы в результатах поиска и представлениях, основанных на запросах. дбфолдер извлекает эти элементы, запрашивая систему поиска Windows. Элементы в результатах поиска определяются по схеме протокола, например &quot; File: &quot; или &quot; MAPI: &quot; . Дбфолдер обеспечивает поведение этих элементов, делегируя их источникам данных оболочки, созданным для этих протоколов. Дополнительные сведения см. в разделе <a href="/previous-versions/bb233544(v=msdn.10)">Разработка надстроек для обработчиков протоколов</a> .<br/> когда дбфолдер делегирует свою операцию синтаксического анализа источникам данных оболочки, которые поддерживают протоколы поиска Windows, этот контекст привязки предоставляет доступ к значениям, которые были возвращены в результате запроса для этого элемента. Например:<br/>
<ul>
<li><a href="/windows/desktop/properties/props-system-itemtype">System. ItemType</a> (PKEY_ItemType)</li>
<li><a href="/windows/desktop/properties/props-system-parsingpath">System. парсингпас</a> (PKEY_ParsingPath)</li>
<li><a href="/windows/desktop/properties/props-system-itempathdisplay">System. итемпасдисплай</a> (PKEY_ItemPathDisplay)</li>
<li><a href="/windows/desktop/properties/props-system-itemnamedisplay">System. итемнамедисплай</a> (PKEY_ItemNameDisplay)</li>
</ul>
<br/> Этот контекст привязки также можно использовать для синтаксического анализа элемента Дбфолдер, если у клиента есть набор свойств, определяющих элемент. В этом случае пустое имя должно быть передано в <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>ишеллфолдер::P арседисплайнаме</strong></a>.<br/> до Windows 7 это значение не было определено в файле заголовка. Он может быть определен вызывающим объектом или передан как его строковое значение: <code>L&quot;ParseWithProperties&quot;</code> . начиная с Windows 7, значение определяется в шлобж. h. Обратите внимание, что этот заголовок отличается от того места, где определены другие константы STR.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PROPERTYBAG_PARAM"></span><span id="str_propertybag_param"></span><dl> <dt><strong>STR_PROPERTYBAG_PARAM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Введено в Windows 8</strong>. Укажите этот контекст привязки, чтобы указать, что параметр контекста привязки является контейнером свойств (<a href="/windows/win32/api/oaidl/nn-oaidl-ipropertybag"><strong>ипропертибаг</strong></a>), используемым для передачи значений Variant в контексте привязки. Дополнительные сведения см. в разделе "Примечания".<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_SKIP_BINDING_CLSID"></span><span id="str_skip_binding_clsid"></span><dl> <dt><strong>STR_SKIP_BINDING_CLSID</strong></dt> </dl></td>
<td style="text-align: left;"><strong>появилось в Windows XP</strong>. Укажите этот контекст привязки, чтобы вызвать методы <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>ишеллфолдер::P арседисплайнаме</strong></a> или <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>Ишеллфолдер:: биндтубжект</strong></a> , чтобы игнорировать определенное расширение пространства имен оболочки при синтаксическом анализе или привязке. CLSID игнорируемого пространства имен предоставляется методом <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid"><strong>IPersist::-ClassID</strong></a> параметра BIND. <br/>
<blockquote>
[!Note]<br />
это значение, введенное в Windows 2000 с пакетом обновления 3 (SP3), было определено в шлобж. h до Windows XP, когда оно было перемещено в Shobjidl. h.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_TRACK_CLSID"></span><span id="str_track_clsid"></span><dl> <dt><strong>STR_TRACK_CLSID</strong></dt> </dl></td>
<td style="text-align: left;">Не используется.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Remarks

Контексты привязки используются для передачи необязательных параметров функциям с \* параметром IBindCtx. Эти параметры выражаются в виде COM-объектов и могут реализовывать интерфейсы, используемые для моделирования данных параметров. Некоторые контексты привязки представляют логическое значение, где **true** означает объект, реализующий только [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , и false указывает, что объект отсутствует.

[**Ишеллфолдер::P арседисплайнаме**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname), [**Ишеллфолдер:: биндтубжект**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) и [**интерфейса IShellItem:: биндтохандлер**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) принимают контекст привязки, и вы можете передать их параметры через этот контекст привязки.

Некоторые контексты привязки относятся к определенным реализациям источника данных или типам обработчиков.

Параметры контекста привязки определяются для использования с определенной функцией или методом.

При запросе хранилища свойств через [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)можно указать эквивалент значения [**\_ по умолчанию GPS**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags) , передав параметр [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) null. Также можно указать эквивалент типа \_ ReadWrite, передав режим стгм \_ ReadWrite \| стгм \_ Exclusive в контексте привязки.

Контейнер свойств, указанный в контекстном объекте BIND **\_ \_ параметра str** , содержит дополнительные значения, к которым можно получить доступ с помощью методов [**Ипропертибаг:: Read**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768197(v=vs.85)) и [**ипропертибаг:: Write**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768198(v=vs.85)) .



| Имя свойства                                 | Тип     | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ Флаги элементов перечисления str \_                       | VT \_ UI4  | **Введено в Windows 8**. Указывает значение [**шконтф**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) , которое будет передано в [**Ишеллфолдер:: енумобжектс**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) при вызове [**интерфейса IShellItem:: биндтохандлер**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) с **бхид \_ енумитемс**.                                                                                                                                                                                                                         |
| \_явная ассоциация синтаксического анализа str \_ \_ \_ успешно выполнена | Логическое значение VT \_ | **появилось в Windows 7**. Метод [**ишеллфолдер::P арседисплайнаме**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) задает это свойство, чтобы сообщить вызывающей стороне о том, что возвращенный IDList был привязан к [идентификатору ProgID](fa-progids.md) , указанному с помощью метода **str \_ Parse, \_ с \_ явным \_ идентификатором ProgID** или с **\_ \_ \_ явным \_ ассокапп** для приложения, указанного в параметре str Parse. Когда инструкция **str \_ Parse \_ явное \_ сопоставление \_ успешно** отсутствует, ProgID или приложение не были привязаны к IDList. |
| STR \_ Parse \_ с \_ явно \_ ассокапп          | VT \_ BSTR | **появилось в Windows 7**. Укажите это свойство, чтобы вызвать метод [**ишеллфолдер::P арседисплайнаме**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) , чтобы вернуть IDList, привязанный к обработчику сопоставления типов файлов для приложения.                                                                                                                                                                                                                                          |
| STR \_ Parse \_ с \_ явно указанным \_ ProgID            | VT \_ BSTR | **появилось в Windows 7**. Укажите это свойство, чтобы вызвать метод [**ишеллфолдер::P арседисплайнаме**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) , чтобы вернуть IDList, привязанный к обработчику сопоставления файлов предоставленного [ProgID](fa-progids.md).                                                                                                                                                                                                                          |



 

Пример использования значений контекста привязки см. в разделе [анализ с помощью примера параметров](samples-parsingwithparameters.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 
