---
description: В этом разделе описываются константы, перечисления и флаги оболочки Windows.
title: Константы, перечисления и флаги оболочки
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 638beaa7-a065-4ab3-8eb5-286a306a8f24
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2070ef1acc37262a526186862f46afa002c47343
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "104273169"
---
# <a name="shell-constants-enumerations-and-flags"></a>Константы, перечисления и флаги оболочки

В этом разделе описываются константы, перечисления и флаги оболочки Windows.

## <a name="in-this-section"></a>В этом разделе



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Раздел</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_svgio"><strong>_SVGIO</strong></a><br/></td>
<td>Используется с методами <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-items"><strong>ифолдервиев:: Items</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-itemcount"><strong>Ифолдервиев:: ItemCount</strong></a>и <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getitemobject"><strong>ишеллвиев:: жетитемобжект</strong></a> для ограничения или управления элементами в коллекциях.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_svsif"><strong>_SVSIF</strong></a><br/></td>
<td>Указывает флаги, используемые <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview"><strong>ифолдервиев</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2"><strong>IFolderView2</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>ишеллвиев</strong></a> и <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2"><strong>IShellView2</strong></a> , чтобы указать тип выбора для применения.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shappmgr/ne-shappmgr-appactionflags"><strong>аппактионфлагс</strong></a><br/></td>
<td>Указывает действия по управлению приложениями, поддерживаемые издателем приложения. Эти флаги являются битовыми масками, передаваемыми <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-ishellapp-getpossibleactions"><strong>ишеллапп:: жетпоссиблеактионс</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shappmgr/ne-shappmgr-appinfodataflags"><strong>аппинфодатафлагс</strong></a><br/></td>
<td>Указывает сведения о приложении, возвращаемые из <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-ishellapp-getappinfo"><strong>ишеллапп:: жетаппинфо</strong></a>. Эти флаги являются битовыми масками, используемыми в элементе <a href="/windows/desktop/api/Shappmgr/ns-shappmgr-appinfodata"><strong>двмаск</strong></a> структуры <strong>аппинфодата</strong> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ne-shobjidl_core-application_view_orientation"><strong>APPLICATION_VIEW_ORIENTATION</strong></a><br/></td>
<td>Определяет набор режимов ориентации экрана для окна (представление приложения). Используется <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings2-getapplicationvieworientation"><strong>IApplicationDesignModeSettings2:: жетаппликатионвиевориентатион</strong></a> и <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings2-setapplicationvieworientation"><strong>IApplicationDesignModeSettings2:: сетаппликатионвиевориентатион</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ne-shobjidl_core-application_view_size_preference"><strong>APPLICATION_VIEW_SIZE_PREFERENCE</strong></a><br/></td>
<td>Определяет набор возможных параметров размера окна общих окон (представление приложения). Используется <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ilaunchsourceviewsizepreference-getsourceviewsizepreference"><strong>илаунчсаурцевиевсизепреференце:: жетсаурцевиевсизепреференце</strong></a> и <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ilaunchtargetviewsizepreference-gettargetviewsizepreference"><strong>Илаунчтаржетвиевсизепреференце:: GetTargetViewSizePreference</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-application_view_state"><strong>APPLICATION_VIEW_STATE</strong></a><br/></td>
<td>Указывает текущее состояние представления для приложения Магазина Windows. Используется <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-setapplicationviewstate"><strong>иаппликатиондесигнмодесеттингс:: сетаппликатионвиевстате</strong></a> и <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-isapplicationviewstatesupported"><strong>Иаппликатиондесигнмодесеттингс:: IsApplicationViewStateSupported</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-assocdata"><strong>ассокдата</strong></a><br/></td>
<td>Используется <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getdata"><strong>икуеряссоЦиатионс:: GetData</strong></a> для определения типа возвращаемых данных.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/shell/assocf_str"><strong>ассокф</strong></a><br/></td>
<td>Предоставляет сведения для методов интерфейса <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>икуеряссоЦиатионс</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel"><strong>ассоЦиатионлевел</strong></a><br/></td>
<td>Указывает источник связи по умолчанию для расширения имени файла. Используется методами интерфейса <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>иаппликатионассоЦиатионрегистратион</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype"><strong>ASSOCIATIONTYPE</strong></a><br/></td>
<td>Указывает тип связи для приложения. Используется методами интерфейса <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>иаппликатионассоЦиатионрегистратион</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-assockey"><strong>ассоккэй</strong></a><br/></td>
<td>Указывает тип ключа, возвращаемого <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getkey"><strong>икуеряссоЦиатионс:: GetKey</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr"><strong>ассокстр</strong></a><br/></td>
<td>Используется методом <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getstring"><strong>икуеряссоЦиатионс:: GetString</strong></a> для определения типа возвращаемой строки.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-attachment_action"><strong>ATTACHMENT_ACTION</strong></a><br/></td>
<td>Предоставляет набор флагов для использования с <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-prompt"><strong>иаттачментексекуте::P ллекцию</strong></a> , чтобы указать действие, выполняемое при подтверждении пользователя.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-attachment_prompt"><strong>ATTACHMENT_PROMPT</strong></a><br/></td>
<td>Предоставляет набор флагов для использования с <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-prompt"><strong>иаттачментексекуте::P ллекцию</strong></a> для указания типа отображаемого интерфейса Prompt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ne-shlobj_core-autocompletelistoptions"><strong>аутокомплетелистоптионс</strong></a><br/></td>
<td>Указывает, какие объекты перечисляются для списков автозавершения.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shldisp/ne-shldisp-autocompleteoptions"><strong>аутокомплетеоптионс</strong></a><br/></td>
<td>Указывает значения, используемые параметрами <a href="/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-getoptions"><strong>IAutoComplete2::</strong></a> IAutoComplete2 и <a href="/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions"><strong>:: сетоптионс</strong></a> для параметров, окружающих Автозаполнение.<br/></td>
</tr>
<tr class="even">
<td><a href="str-constants.md"><strong>Ключи строк контекста привязки</strong></a><br/></td>
<td>Набор строковых ключей, которые используются с методом <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx:: регистеробжектпарам</strong></a> для указания контекста привязки.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shdeprecated/ne-shdeprecated-bnstate"><strong>бнстате</strong></a><br/></td>
<td>Не рекомендуется. Используется <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice-setnavigatestate"><strong>ибровсерсервице:: сетнавигатестате</strong></a> и <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice-getnavigatestate"><strong>Ибровсерсервице:: жетнавигатестате</strong></a> для указания состояний навигации.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ne-shobjidl_core-_browserframeoptions"><strong>бровсерфрамеоптионс</strong></a><br/></td>
<td>Используется с методом <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibrowserframeoptions-getframeoptions"><strong>ибровсерфрамеоптионс:: жетфрамеоптионс</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-categoryinfo_flags"><strong>CATEGORYINFO_FLAGS</strong></a><br/></td>
<td>Предоставляет набор флагов для использования со структурой <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-category_info"><strong>CATEGORY_INFO</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-catsort_flags"><strong>CATSORT_FLAGS</strong></a><br/></td>
<td>Указывает методы для сортировки данных категории.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb762483(v=vs.85)"><strong>кдконтролстате</strong></a><br/></td>
<td>Задает значения, указывающие, является ли элемент управления видимым и включенным. Используется членами интерфейса <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize"><strong>ифиледиалогкустомизе</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_enum_flags"><strong>CM_ENUM_FLAGS</strong></a><br/></td>
<td>Используется членами интерфейса <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>иколумнманажер</strong></a> для указания того, какой набор столбцов запрашивается: все или только видимые в данный момент.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_mask"><strong>CM_MASK</strong></a><br/></td>
<td>Указывает, какие значения в структуре <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a> должны быть установлены во время вызовов <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icolumnmanager-setcolumninfo"><strong>Иколумнманажер:: сетколумнинфо</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_set_width_value"><strong>CM_SET_WIDTH_VALUE</strong></a><br/></td>
<td>Задает значения ширины в пикселях и включает специальную поддержку по умолчанию и Автоподбор размеров. Используется членами интерфейса <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>иколумнманажер</strong></a> через структуру <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_state"><strong>CM_STATE</strong></a><br/></td>
<td>Указывает значения состояния столбца. Используется членами интерфейса <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>иколумнманажер</strong></a> через структуру <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/CredentialProvider/ne-credentialprovider-credential_provider_account_options"><strong>CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS</strong></a><br/></td>
<td>Указывает тип учетных данных, которые поставщик учетных данных должен вернуть для связи с &quot; &quot; плиткой другого пользователя. Используется <a href="/windows/desktop/api/CredentialProvider/nf-credentialprovider-icredentialprovideruserarray-getaccountoptions"><strong>ICredentialProviderUserArray_GetAccountOptions</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/ne-credentialprovider-credential_provider_credential_field_options"><strong>CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS</strong></a><br/></td>
<td>Предоставляет параметры настройки для одного поля в пользовательском интерфейсе входа или учетных данных.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_field_interactive_state"><strong>CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE</strong></a><br/></td>
<td>Описывает состояние поля и то, как оно может взаимодействовать с ним пользователь. Поставщики учетных данных могут отображать поля в различных интерактивных состояниях.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_field_state"><strong>CREDENTIAL_PROVIDER_FIELD_STATE</strong></a><br/></td>
<td>Задает состояние одного поля в пользовательском интерфейсе учетных данных.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_field_type"><strong>CREDENTIAL_PROVIDER_FIELD_TYPE</strong></a><br/></td>
<td>Указывает тип поля учетных данных. Используется <a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_field_descriptor"><strong>CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_get_serialization_response"><strong>CREDENTIAL_PROVIDER_GET_SERIALIZATION_RESPONSE</strong></a><br/></td>
<td>Описывает ответ, когда поставщик учетных данных пытается сериализовать учетные данные.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_status_icon"><strong>CREDENTIAL_PROVIDER_STATUS_ICON</strong></a><br/></td>
<td>Указывает, какой значок состояния должен отображаться.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_usage_scenario"><strong>CREDENTIAL_PROVIDER_USAGE_SCENARIO</strong></a><br/></td>
<td>Объявляет сценарии, в которых поддерживается поставщик учетных данных. Сценарий использования поставщика учетных данных (ЦП) позволяет поставщику учетных данных предоставлять отдельное поведение перечисления и настройку полей пользовательского интерфейса в разных сценариях.<br/></td>
</tr>
<tr class="even">
<td><a href="csidl.md"><strong>CSID</strong></a><br/></td>
<td><blockquote>
<p><b>Примечание. </b> Начиная с Windows Vista, эти значения были заменены на значения <a href="knownfolderid.md"><strong>кновнфолдерид</strong></a> . Список новых констант и соответствующих значений CSID см. в этом разделе. Для удобства соответствующие значения <strong>кновнфолдерид</strong> также указаны здесь для каждого значения CSid.</p>
<p>Система с CSID поддерживается в Windows Vista в целях совместимости. Однако новая разработка должна использовать значения <a href="knownfolderid.md"><strong>кновнфолдерид</strong></a> , а не значения CSid.<br/></p>
</blockquote>
<br/> Значения "CSID" (Специальный список ИДЕНТИФИКАТОРов элементов) обеспечивают уникальный независимый от системы способ идентификации специальных папок, часто используемых приложениями, но которые могут не иметь одинакового имени или расположения в любой заданной системе. Например, системная папка может быть &quot; C:\Windows &quot; на одной системе и &quot; C:\Winnt &quot; на другом. Эти константы определены в Шлобж. h.<br/></td>
</tr>
<tr class="odd">
<td><a href="ctf.md"><strong>Флаги КТФ</strong></a><br/></td>
<td>Флаги, управляющие поведением вызывающей функции. Используется <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread"><strong>шкреатесреад</strong></a> и <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadwithhandle"><strong>шкреатесреадвисхандле</strong></a>. В этих функциях эти значения определяются как тип SHCT_FLAGS.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-dataobj_get_item_flags"><strong>DATAOBJ_GET_ITEM_FLAGS</strong></a><br/></td>
<td>Значения, используемые функцией <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromdataobject"><strong>шжетитемфромдатаобжект</strong></a> для указания параметров, касающихся обработки исходного объекта.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-tagdeskbandcid"><strong>Флаги команды DBID</strong></a><br/></td>
<td>Эти идентификаторы команд можно отправить в контейнер объекта полосы с помощью <a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-exec"><strong>IOleCommandTarget:: Exec</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-def_share_id"><strong>DEF_SHARE_ID</strong></a><br/></td>
<td>Значения, указывающие на обрабатываемую папку с помощью методов интерфейса <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isharingconfigurationmanager"><strong>ишарингконфигуратионманажер</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype"><strong>дефаултсавефолдертипе</strong></a><br/></td>
<td>Указывает расположение для сохранения по умолчанию.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-default_folder_menu_restrictions"><strong>DEFAULT_FOLDER_MENU_RESTRICTIONS</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-desktop_wallpaper_position"><strong>DESKTOP_WALLPAPER_POSITION</strong></a><br/></td>
<td>Указывает, как должен отображаться фоновый рисунок рабочего стола.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shtypes/ne-shtypes-device_scale_factor"><strong>DEVICE_SCALE_FACTOR</strong></a><br/></td>
<td>Указывает на поддельный коэффициент масштабирования устройства в процентах. Используется <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-setapplicationviewstate"><strong>иаппликатиондесигнмодесеттингс:: сетаппликатионвиевстате</strong></a> и <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-isapplicationviewstatesupported"><strong>Иаппликатиондесигнмодесеттингс:: IsApplicationViewStateSupported</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/ne-shellscalingapi-display_device_type"><strong>DISPLAY_DEVICE_TYPE</strong></a><br/></td>
<td>Указывает, является ли устройство основным или иммерсивного типом дисплея.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype"><strong>дропимажетипе</strong></a><br/></td>
<td>Значения, используемые с структурой <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription"><strong>дропдескриптион</strong></a> для указания изображения перетаскивания.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_expcmdstate"><strong>експкмдстате</strong></a><br/></td>
<td>Значения <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_expcmdstate"><strong>експкмдстате</strong></a> представляют состояние команды для элемента оболочки.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_fill_flags"><strong>EXPLORER_BROWSER_FILL_FLAGS</strong></a><br/></td>
<td>Эти флаги используются с <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-fillfromobject"><strong>иексплорербровсер:: филлфромобжект</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_options"><strong>EXPLORER_BROWSER_OPTIONS</strong></a><br/></td>
<td>Эти флаги используются с параметрами <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-getoptions"><strong>иексплорербровсер::</strong></a> Иексплорербровсер и <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-setoptions"><strong>:: сетоптионс</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_explorerpanestate"><strong>експлорерпанестате</strong></a><br/></td>
<td>Укажите флаги, используемые <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate"><strong>иексплорерпаневисибилити:: жетпанестате</strong></a> , чтобы получить текущее состояние данной панели проводника Windows.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fdap"><strong>фдап</strong></a><br/></td>
<td>Указывает размещение списка.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fde_overwrite_response"><strong>FDE_OVERWRITE_RESPONSE</strong></a><br/></td>
<td>Задает значения, используемые методом <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onoverwrite"><strong>ифиледиаложевентс:: оноверврите</strong></a> для указания ответа приложения на запрос перезаписи во время операции сохранения с помощью общего диалогового окна файла.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fde_shareviolation_response"><strong>FDE_SHAREVIOLATION_RESPONSE</strong></a><br/></td>
<td>Задает значения, используемые методом <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onshareviolation"><strong>ифиледиаложевентс:: оншаревиолатион</strong></a> для указания ответа приложения на нарушение совместного доступа, возникающее при открытии или сохранении файла.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fffp_mode"><strong>FFFP_MODE</strong></a><br/></td>
<td>Описывает критерии соответствия. Используется методами интерфейса <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager"><strong>икновнфолдерманажер</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-file_usage_type"><strong>FILE_USAGE_TYPE</strong></a><br/></td>
<td>Константы, используемые <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileisinuse-getusage"><strong>ифилеисинусе:: Usage</strong></a> для указания способа использования файла.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_fileopendialogoptions"><strong>филеопендиалогоптионс</strong></a><br/></td>
<td>Определяет набор параметров, доступных для диалогового окна открытия или сохранения.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>филетипеаттрибутефлагс</strong></a><br/></td>
<td>Указывает константы <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>филетипеаттрибутефлагс</strong></a> , которые используются в значении едитфлагс раздела реестра <a href="fa-progids.md">ProgID</a> сопоставления файлов.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folder_enum_mode"><strong>FOLDER_ENUM_MODE</strong></a><br/></td>
<td>Используется методами <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithfolderenummode-getmode"><strong>иобжектвисфолдеренуммоде:: onmode</strong></a> и <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithfolderenummode-setmode"><strong>Иобжектвисфолдеренуммоде:: SetMode</strong></a> для получения и задания режимов просмотра папок.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderflags"><strong>фолдерфлагс</strong></a><br/></td>
<td>Набор флагов, определяющих параметры представления папки. Флаги не зависят друг от друга и могут использоваться в любом сочетании.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderlogicalviewmode"><strong>фолдерлогикалвиевмоде</strong></a><br/></td>
<td>Используется <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderviewsettings-getviewmode"><strong>ифолдервиевсеттингс:: жетвиевмоде</strong></a> и <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-setfolderlogicalviewmode"><strong>Исеарчфолдеритемфактори:: сетфолдерлогикалвиевмоде</strong></a> для описания режима представления.<br/></td>
</tr>
<tr class="odd">
<td><a href="foldertypeid.md"><strong>фолдертипеид</strong></a><br/></td>
<td>Значения <a href="foldertypeid.md"><strong>фолдертипеид</strong></a> представляют шаблон представления, применяемый к папке, обычно основанный на предполагаемом использовании и содержимом.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode"><strong>фолдервиевмоде</strong></a><br/></td>
<td>Указывает тип представления папок.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-folderviewoptions"><strong>фолдервиевоптионс</strong></a><br/></td>
<td>Используется методами интерфейса <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderviewoptions"><strong>ифолдервиевоптионс</strong></a> для активации параметров Windows Vista, не поддерживаемых по умолчанию в Windows 7 и более поздних системах, а также для деактивации новых параметров Windows 7.<br/></td>
</tr>
<tr class="even">
<td><a href="iactivedesktop-flags.md"><strong>Флаги Иактиведесктоп</strong></a><br/></td>
<td>В этом разделе описываются флаги, используемые методами интерфейса <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop"><strong>иактиведесктоп</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ne-shlobj_core-ieshortcutflags"><strong>иешорткутфлагс</strong></a><br/></td>
<td>Указывает способ обработки ярлыка браузером.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category"><strong>KF_CATEGORY</strong></a><br/></td>
<td>Значение, представляющее категорию, с которой можно классифицировать папку, зарегистрированную в системе с известными папками.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_kf_definition_flags"><strong>KF_DEFINITION_FLAGS</strong></a><br/></td>
<td>Флаги, указывающие определенные поведения известных папок. Используется со структурой <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition"><strong>KNOWNFOLDER_DEFINITION</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_kf_redirect_flags"><strong>KF_REDIRECT_FLAGS</strong></a><br/></td>
<td>Флаги, используемые <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-redirect"><strong>икновнфолдерманажер:: redirect</strong></a> для указания сведений о перенаправлении известных папок, таких как разрешения и владение для перенаправленной папки.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_kf_redirection_capabilities"><strong>KF_REDIRECTION_CAPABILITIES</strong></a><br/></td>
<td>Флаги, указывающие текущие возможности перенаправления известной папки. Используется <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getredirectioncapabilities"><strong>икновнфолдер:: жетредиректионкапабилитиес</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag"><strong>KNOWN_FOLDER_FLAG</strong></a><br/></td>
<td>Укажите специальные параметры извлечения для известных папок. Эти значения заменяют значения <a href="csidl.md"><strong>CSid</strong></a> , которые имеют параллельное значение.<br/></td>
</tr>
<tr class="odd">
<td><a href="knownfolderid.md"><strong>кновнфолдерид</strong></a><br/></td>
<td>Константы <a href="knownfolderid.md"><strong>кновнфолдерид</strong></a> представляют идентификаторы GUID, которые определяют стандартные папки, зарегистрированные в системе как <a href="known-folders.md">известные папки</a>. Эти папки устанавливаются вместе с Windows Vista и более поздними операционными системами, и на компьютере будут находиться только папки, соответствующие установленной версии. Описания этих папок см. в разделе <a href="csidl.md"><strong>CSid</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryfolderfilter"><strong>либрарифолдерфилтер</strong></a><br/></td>
<td>Определяет параметры для фильтрации элементов папки. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarymanagedialogoptions"><strong>либрариманажедиалогоптионс</strong></a><br/></td>
<td>Используется <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shshowmanagelibraryui"><strong>шшовманажелибрарюи</strong></a> для определения параметров обработки конфликтов имен при сохранении библиотеки.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryoptionflags"><strong>либрарйоптионфлагс</strong></a><br/></td>
<td>Задает параметры библиотеки.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarysaveflags"><strong>либрарисавефлагс</strong></a><br/></td>
<td>Задает параметры для обработки конфликтов имен при сохранении библиотеки. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-mimeassociationdialog_in_flags"><strong>MIMEASSOCIATIONDIALOG_IN_FLAGS</strong></a><br/></td>
<td>Используется с функцией <a href="/windows/desktop/api/Intshcut/nf-intshcut-mimeassociationdialoga"><strong>мимеассоЦиатиондиалог</strong></a> для определения способа ее выполнения.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-monitor_app_visibility"><strong>MONITOR_APP_VISIBILITY</strong></a><br/></td>
<td>Указывает, отображаются ли на дисплее окна рабочего стола вместо приложений для Магазина Windows.<br/></td>
</tr>
<tr class="even">
<td><a href="mp-popupflags.md"><strong>Константы MP_POPUPFLAGS</strong></a><br/></td>
<td>Представляет параметры, доступные при отображении всплывающего меню.<br/></td>
</tr>
<tr class="odd">
<td><a href="net-string.md"><strong>NET_STRING</strong></a><br/></td>
<td>Представляет типы сетевых адресов. Используйте одну или несколько (как побитовое сочетание) следующих констант, чтобы создать маску сетевого адреса для использования с макросом <a href="/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype"><strong>NetAddr_SetAllowType</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-nstcfoldercapabilities"><strong>нсткфолдеркапабилитиес</strong></a><br/></td>
<td>Задает состояние элемента дерева. Эти значения используются методами интерфейса <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrolfoldercapabilities"><strong>инамеспацетриконтролфолдеркапабилитиес</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_nstcitemstate"><strong>нстЦитемстате</strong></a><br/></td>
<td>Задает состояние элемента дерева. Эти значения используются методами интерфейса <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>инамеспацетриконтрол</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_nstcstyle"><strong>нсткстиле</strong></a><br/></td>
<td>Описывает характеристики данного элемента управления деревом пространства имен.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-nstcstyle2"><strong>NSTCSTYLE2</strong></a><br/></td>
<td>Используется методами <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrol2"><strong>INameSpaceTreeControl2</strong></a> для указания расширенных стилей экрана в пространстве имен оболочки TreeView.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-nwmf"><strong>нвмф</strong></a><br/></td>
<td>Флаги, используемые <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inewwindowmanager-evaluatenewwindow"><strong>иневвиндовманажер:: евалуатеневвиндов</strong></a>. Эти значения являются факторами при принятии решения о том, следует ли отображать всплывающее окно.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-package_execution_state"><strong>PACKAGE_EXECUTION_STATE</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/win32/api/shtypes/ne-shtypes-perceived"><strong>УХУДШИТ</strong></a><br/></td>
<td>Указывает воспринимаемый тип файла. Этот набор констант используется в функции <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype"><strong>ассокжетперцеиведтипе</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shappmgr/ne-shappmgr-pubappinfoflags"><strong>пубаппинфофлагс</strong></a><br/></td>
<td>Указывает, какие члены структуры <a href="/windows/desktop/api/Shappmgr/ns-shappmgr-pubappinfo"><strong>пубаппинфо</strong></a> являются допустимыми. Эти флаги являются битовыми масками, заданными в элементе <strong>двмаск</strong> и передаваемыми <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-ipublishedapp-getpublishedappinfo"><strong>Ипублишедапп:: жетпублишедаппинфо</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ne-shellapi-query_user_notification_state"><strong>QUERY_USER_NOTIFICATION_STATE</strong></a><br/></td>
<td>Указывает состояние компьютера для текущего пользователя по отношению к отправке уведомления. Используется <a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate"><strong>шкуерюсернотификатионстате</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="hkey-type.md"><strong>Типы данных реестра</strong></a><br/></td>
<td>Эти типы данных можно использовать для указания типа значения реестра.<br/></td>
</tr>
<tr class="even">
<td><a href="regsam.md"><strong>регсам</strong></a><br/></td>
<td>Тип данных, используемый для указания атрибутов доступа безопасности в реестре.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions"><strong>ОГРАНИЧЕНИЯ</strong></a><br/></td>
<td>Эти флаги используются с функцией <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shrestricted"><strong>шрестриктед</strong></a> . <strong>Шрестриктед</strong> используется для определения того, действует ли указанная политика администратора. Во многих случаях приложениям необходимо изменить определенные режимы работы, чтобы обеспечить соответствие политикам, используемым системными администраторами.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/ne-shellscalingapi-scale_change_flags"><strong>SCALE_CHANGE_FLAGS</strong></a><br/></td>
<td>Флаги, которые используются для указания того, что произошло изменение масштабирования.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-scnrt_status"><strong>SCNRT_STATUS</strong></a><br/></td>
<td>Указывает, следует ли включить или отключить асинхронную регистрацию и отменить регистрацию для <a href="/windows/desktop/api/Shlobj/nf-shlobj-shchangenotifyregisterthread"><strong>шчанженотифирегистерсреад</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-tagsfbs_flags"><strong>SFBS_FLAGS</strong></a><br/></td>
<td>Указывает, как функция <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>стрформатбитесизикс</strong></a> должна выполнять округление неотображаемых цифр.<br/></td>
</tr>
<tr class="odd">
<td><a href="sfgao.md"><strong>сфгао</strong></a><br/></td>
<td>Атрибуты, которые могут быть получены для элемента (файла или папки) или набора элементов.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-shard"><strong>СЕГМЕНТА</strong></a><br/></td>
<td>Обозначает интерпретацию данных, передаваемых методом <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>шаддторецентдокс</strong></a> в параметре <em>ПС</em> , для обозначения элемента, статистику использования которого отслеживается.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-share_role"><strong>SHARE_ROLE</strong></a><br/></td>
<td>Указывает разрешения на доступ, назначенные <strong>пользователям</strong> или <strong>общей</strong> папке. Используется в <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isharingconfigurationmanager-createshare"><strong>креатешаре</strong></a> и <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isharingconfigurationmanager-getsharepermissions"><strong>жетшарепермиссионс</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shtypes/ne-shtypes-shcolstate"><strong>школстате</strong></a><br/></td>
<td>Описывает, как должно обрабатываться свойство. Эти значения определены в Штипес. h.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_shcontf"><strong>шконтф</strong></a><br/></td>
<td>Определяет типы элементов, включаемых в перечисление. Эти значения используются с методом <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>ишеллфолдер:: енумобжектс</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-shell_link_data_flags"><strong>SHELL_LINK_DATA_FLAGS</strong></a><br/></td>
<td>Задает настройки параметров. Используется с <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinkdatalist-getflags"><strong>флагами ишелллинкдаталист::</strong></a> Ишелллинкдаталист и <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinkdatalist-setflags"><strong>:: сетфлагс</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-shell_ui_component"><strong>SHELL_UI_COMPONENT</strong></a><br/></td>
<td>Определяет тип компонента пользовательского интерфейса, который требуется в оболочке.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/ne-shldisp-shellfolderviewoptions"><strong>шеллфолдервиевоптионс</strong></a><br/></td>
<td>Задает параметры представления, возвращаемые свойством <a href="shellfolderview-viewoptions.md"><strong>виевоптионс</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants"><strong>шеллспеЦиалфолдерконстантс</strong></a><br/></td>
<td>Задает уникальные, независимые от системы значения, которые определяют специальные папки. Эти папки часто используются приложениями, но они могут не иметь одинакового имени или расположения в любой заданной системе. Например, системная папка может быть &quot; C:\Windows &quot; в одной системе и &quot; C:\Winnt &quot; на другом.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ExDisp/ne-exdisp-shellwindowfindwindowoptions"><strong>шеллвиндовфиндвиндовоптионс</strong></a><br/></td>
<td>Задает параметры для поиска окна в коллекции окон оболочки. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Exdisp/ne-exdisp-shellwindowtypeconstants"><strong>шеллвиндовтипеконстантс</strong></a><br/></td>
<td>Задает типы окон оболочки.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_shgdnf"><strong>шгднф</strong></a><br/></td>
<td>Определяет значения, используемые с методами <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>ишеллфолдер:: жетдисплайнамеоф</strong></a> и <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-setnameof"><strong>Ишеллфолдер:: сетнамеоф</strong></a> для указания типа имен файлов или папок, используемых этими методами. <br/>
<blockquote>
<b>Примечание</b>.<br />
До Windows 7 эти значения были упакованы как перечисление ШГНО.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-shglobalcounter"><strong>шглобалкаунтер</strong></a><br/></td>
<td>Идентификаторы для различных глобальных счетчиков или общих переменных. Каждый глобальный счетчик можно увеличить или уменьшить с помощью <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shglobalcounterincrement"><strong>шглобалкаунтеринкремент</strong></a> и <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shglobalcounterdecrement"><strong>шглобалкаунтердекремент</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-shregdel_flags"><strong>SHREGDEL_FLAGS</strong></a><br/></td>
<td>Предоставляет набор значений, указывающий, из какого базового ключа будет удален элемент.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-shregenum_flags"><strong>SHREGENUM_FLAGS</strong></a><br/></td>
<td>Предоставляет набор значений, указывающий базовый ключ, который будет использоваться для перечисления.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ne-shellapi-shstockiconid"><strong>шстоккиконид</strong></a><br/></td>
<td>Используется <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>шжетстоккиконинфо</strong></a> для определения извлекаемого значка акции.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_sichintf"><strong>сичинтф</strong></a><br/></td>
<td>Используется для определения способа сравнения двух элементов оболочки. <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-compare"><strong>Интерфейса IShellItem:: Compare</strong></a> использует этот перечислимый тип.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sigdn"><strong>сигдн</strong></a><br/></td>
<td>Запрашивает форму отображаемого имени элемента для извлечения с помощью <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname"><strong>интерфейса IShellItem::</strong></a> lt и <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetnamefromidlist"><strong>шжетнамефромидлист</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-spaction"><strong>ДЕЙСТВИЕ</strong></a><br/></td>
<td>Описывает выполняемое действие, которое требует отображения хода выполнения для пользователя с помощью интерфейса <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress"><strong>иактионпрогресс</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_spbeginf"><strong>спбегинф</strong></a><br/></td>
<td>Эти константы, используемые <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iactionprogress-begin"><strong>иактионпрогресс:: Begin</strong></a>, указывают определенные операции пользовательского интерфейса, которые должны быть включены или отключены.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sptext"><strong>ТЕКСТ</strong></a><br/></td>
<td>Задает тип описательного текста, предоставляемого интерфейсу <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress"><strong>иактионпрогресс</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="srrf.md"><strong>сррф</strong></a><br/></td>
<td>Флаги, ограничивающие установленные или возвращаемые данные.<br/></td>
</tr>
<tr class="odd">
<td><a href="ssf-constants.md"><strong>Константы ССФ</strong></a><br/></td>
<td>Используется функцией <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings"><strong>шжетсетсеттингс</strong></a> для указания того, какие члены структуры <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellstatea"><strong>шеллстате</strong></a> должны быть установлены или массивах.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-stpflag"><strong>стпфлаг</strong></a><br/></td>
<td>Используется методом <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist4-settabproperties"><strong>ITaskbarList4:: сеттабпропертиес</strong></a> для указания свойств вкладки.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-svuia_status"><strong>SVUIA_STATUS</strong></a><br/></td>
<td>Используется с методом <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-_uiactivateview"><strong>IBrowserService2:: _UIActivateView</strong></a> для задания состояния представления браузера.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_cancel_request"><strong>SYNCMGR_CANCEL_REQUEST</strong></a><br/></td>
<td>Описывает запрос от пользователя на отмену синхронизации.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_conflict_item_type"><strong>SYNCMGR_CONFLICT_ITEM_TYPE</strong></a><br/></td>
<td>Описывает тип конфликтующего элемента.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_control_flags"><strong>SYNCMGR_CONTROL_FLAGS</strong></a><br/></td>
<td>Указывает способ выполнения операции, запрашиваемой определенными методами <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrcontrol"><strong>исинкмгрконтрол</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_event_flags"><strong>SYNCMGR_EVENT_FLAGS</strong></a><br/></td>
<td>Задает флаги для события синхронизации.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_event_level"><strong>SYNCMGR_EVENT_LEVEL</strong></a><br/></td>
<td>Указывает тип события, сообщаемого в центр синхронизации.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_handler_capabilities"><strong>SYNCMGR_HANDLER_CAPABILITIES</strong></a><br/></td>
<td>Указывает возможности обработчика относительно действий, которые могут быть выполнены с ним.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_handler_policies"><strong>SYNCMGR_HANDLER_POLICIES</strong></a><br/></td>
<td>Перечисляет политики, заданные обработчиком синхронизации, который отличается от политики по умолчанию.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_handler_type"><strong>SYNCMGR_HANDLER_TYPE</strong></a><br/></td>
<td>Указывает тип обработчика. Используется <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrhandlerinfo-gettype"><strong>исинкмгрхандлеринфо:: GetType</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_item_capabilities"><strong>SYNCMGR_ITEM_CAPABILITIES</strong></a><br/></td>
<td>Указывает действия, которые могут быть выполнены с элементом.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_item_policies"><strong>SYNCMGR_ITEM_POLICIES</strong></a><br/></td>
<td>Задает политики элемента для управления включением или отключением групповых политик.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_presenter_choice"><strong>SYNCMGR_PRESENTER_CHOICE</strong></a><br/></td>
<td>Описывает, какой вариант пользователь выполняет при разрешении конфликтов диспетчера синхронизации. Используется <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictpresenter"><strong>исинкмгрконфликтпресентер</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_presenter_next_step"><strong>SYNCMGR_PRESENTER_NEXT_STEP</strong></a><br/></td>
<td>Описание следующего шага, выполняемого при разрешении конфликтов диспетчера синхронизации. Используется <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictpresenter"><strong>исинкмгрконфликтпресентер</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_progress_status"><strong>SYNCMGR_PROGRESS_STATUS</strong></a><br/></td>
<td>Указывает текущее состояние выполнения процесса синхронизации. Используется <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsynccallback-reportprogress"><strong>исинкмгрсинккаллбакк:: репортпрогресс</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_resolution_abilities"><strong>SYNCMGR_RESOLUTION_ABILITIES</strong></a><br/></td>
<td>Указывает возможности и действие по устранению конфликтов. Используется с <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrresolutionhandler-queryabilities"><strong>исинкмгрресолутионхандлер:: куерябилитиес</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_resolution_feedback"><strong>SYNCMGR_RESOLUTION_FEEDBACK</strong></a><br/></td>
<td>Содержит описание диспетчер синхронизации отзывов о разрешении. Используется <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrresolutionhandler"><strong>исинкмгрресолутионхандлер</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_sync_control_flags"><strong>SYNCMGR_SYNC_CONTROL_FLAGS</strong></a><br/></td>
<td>Указывает флаги, используемые <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-starthandlersync"><strong>исинкмгрконтрол:: старсандлерсинк</strong></a> и <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-startitemsync"><strong>Исинкмгрконтрол:: стартитемсинк</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrflag"><strong>синкмгрфлаг</strong></a><br/></td>
<td>Значения перечисления <a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrflag"><strong>синкмгрфлаг</strong></a> используются в методе <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-initialize"><strong>Исинкмгрсинчронизе:: Initialize</strong></a> для указания способа инициирования события синхронизации.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrhandlerflags"><strong>синкмгрхандлерфлагс</strong></a><br/></td>
<td>Используется в структуре <a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrhandlerinfo"><strong>синкмгрхандлеринфо</strong></a> в качестве флагов, применяемых к текущему обработчику.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrinvokeflags"><strong>синкмгринвокефлагс</strong></a><br/></td>
<td>Значение перечисления <a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrinvokeflags"><strong>синкмгринвокефлагс</strong></a> указывает, как будет вызываться диспетчер синхронизации в методе <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizeinvoke-updateitems"><strong>Исинкмгрсинчронизеинвоке:: упдатеитемс</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgritemflags"><strong>синкмгритемфлагс</strong></a><br/></td>
<td>Задает сведения для текущего элемента в структуре <a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>синкмгритем</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrloglevel"><strong>синкмгрлоглевел</strong></a><br/></td>
<td>Значения перечисления <a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrloglevel"><strong>синкмгрлоглевел</strong></a> указывают уровень ошибок для использования в методе <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror"><strong>Исинкмгрсинчронизекаллбакк:: LogError</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrregisterflags"><strong>синкмгррегистерфлагс</strong></a><br/></td>
<td>Значения перечисления <a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrregisterflags"><strong>синкмгррегистерфлагс</strong></a> используются в методах интерфейса <a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrregister"><strong>исинкмгррегистер</strong></a> для указания событий, для которых обработчик регистрируется для уведомления.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrstatus"><strong>синкмгрстатус</strong></a><br/></td>
<td>Используется в методе <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-setitemstatus"><strong>исинкмгрсинчронизе:: сетитемстатус</strong></a> для указания обновленного состояния элемента.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-thumbbuttonflags"><strong>сумббуттонфлагс</strong></a><br/></td>
<td>Используется <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>сумббуттон</strong></a> для управления конкретными состояниями и поведением кнопки.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-thumbbuttonmask"><strong>сумббуттонмаск</strong></a><br/></td>
<td>Используется структурой <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>сумббуттон</strong></a> для указания, какие члены этой структуры содержат допустимые данные.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/thumbnailstreamcache/ne-thumbnailstreamcache-thumbnailstreamcacheoptions"><strong>сумбнаилстреамкачеоптионс</strong></a><br/></td>
<td>Определяет параметры кэша, используемые интерфейсом <a href="/windows/desktop/api/thumbnailstreamcache/nn-thumbnailstreamcache-ithumbnailstreamcache"><strong>исумбнаилстреамкаче</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags"><strong>TRANSFER_SOURCE_FLAGS</strong></a><br/></td>
<td>Используется методами интерфейсов <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource"><strong>итрансферсаурце</strong></a> и <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination"><strong>итрансфердестинатион</strong></a> для управления операциями с файлами.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-translateurl_in_flags"><strong>TRANSLATEURL_IN_FLAGS</strong></a><br/></td>
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-translateurl_in_flags"><strong>TRANSLATEURL_IN_FLAGS</strong></a> перечислимые значения используются с функцией <a href="/windows/desktop/api/Intshcut/nf-intshcut-translateurla"><strong>транслатеурл</strong></a> , чтобы определить, как она будет выполняться.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-undock_reason"><strong>UNDOCK_REASON</strong></a><br/></td>
<td>Значения, указывающие причину, по которой закрепленное окно приложения специальных возможностей было отброшено. Используется <a href="/windows/desktop/api/shobjidl/nf-shobjidl-iaccessibilitydockingservicecallback-undocked"><strong>иакцессибилитидоккингсервицекаллбакк:: undockd</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-url_scheme"><strong>URL_SCHEME</strong></a><br/></td>
<td>Используется для указания схем URL-адресов.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-urlassociationdialog_in_flags"><strong>URLASSOCIATIONDIALOG_IN_FLAGS</strong></a><br/></td>
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-urlassociationdialog_in_flags"><strong>URLASSOCIATIONDIALOG_IN_FLAGS</strong></a> перечислимые значения используются с <a href="/windows/desktop/api/Intshcut/nf-intshcut-urlassociationdialoga"><strong>урлассоЦиатиондиалог</strong></a> для определения их выполнения.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-vpcolorflags"><strong>впколорфлагс</strong></a><br/></td>
<td>Задает использование цвета. Используется методами <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ivisualproperties"><strong>ивисуалпропертиес</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-vpwatermarkflags"><strong>впватермаркфлагс</strong></a><br/></td>
<td>Задает флаги водяного знака. Используется <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-ivisualproperties-setwatermark"><strong>ивисуалпропертиес:: сетватермарк</strong></a>.<br/></td>
</tr>
</tbody>
</table>



 

 

 
