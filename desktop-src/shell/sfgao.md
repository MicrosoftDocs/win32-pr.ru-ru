---
description: Атрибуты, которые могут быть получены для элемента (файла или папки) или набора элементов.
ms.assetid: 4cb85995-cdc8-4474-8c4d-c783ac91c759
title: СФГАО (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f01691c3dbb1e5b76d93739b4893ffaf7c69e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815321"
---
# <a name="sfgao"></a>сфгао

Атрибуты, которые могут быть получены для элемента (файла или папки) или набора элементов.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Константа/значение</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CANCOPY"></span><span id="sfgao_cancopy"></span><dl> <dt><strong>SFGAO_CANCOPY</strong></dt> <dt>0x00000001</dt> </dl></td>
<td style="text-align: left;">Указанные элементы могут быть скопированы.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_CANMOVE"></span><span id="sfgao_canmove"></span><dl> <dt><strong>SFGAO_CANMOVE</strong></dt> <dt>0x00000002</dt> </dl></td>
<td style="text-align: left;">Указанные элементы могут быть перемещены.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CANLINK"></span><span id="sfgao_canlink"></span><dl> <dt><strong>SFGAO_CANLINK</strong></dt> <dt>0x00000004</dt> </dl></td>
<td style="text-align: left;">Для указанных элементов можно создать ярлыки. Этот атрибут имеет то же значение, что и <a href="/windows/desktop/com/dropeffect-constants"><strong>DROPEFFECT_LINK</strong></a>. <br/> Если расширение пространства имен возвращает этот атрибут, в контекстное меню, отображаемое во время операций перетаскивания, добавляется запись <strong>создания ярлыка</strong> с обработчиком по умолчанию. Расширение также может реализовать собственный обработчик для команды <em>Link</em> вместо значения по умолчанию. Если это расширение, оно отвечает за создание ярлыка.<br/> Элемент <strong>создать ярлык</strong> также добавляется в меню <strong>файл</strong> проводника Windows и в обычные контекстные меню.<br/> Если элемент выбран, метод <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>IContextMenu:: инвокекомманд</strong></a> приложения вызывается с элементом <strong>Лпверб</strong> набора структур <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>кминвокекоммандинфо</strong></a> для <em>компоновки</em>. Приложение отвечает за создание ссылки.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_STORAGE"></span><span id="sfgao_storage"></span><dl> <dt><strong>SFGAO_STORAGE</strong></dt> <dt>0x00000008</dt> </dl></td>
<td style="text-align: left;">Указанные элементы могут быть привязаны к объекту <a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>IStorage</strong></a> через <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>Ишеллфолдер:: биндтубжект</strong></a>. Дополнительные сведения о возможностях управления пространствами имен см. в разделе <strong>IStorage</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CANRENAME"></span><span id="sfgao_canrename"></span><dl> <dt><strong>SFGAO_CANRENAME</strong></dt> <dt>0x00000010</dt> </dl></td>
<td style="text-align: left;">Указанные элементы могут быть переименованы. Обратите внимание, что это значение является, по сути, предложением. не все клиенты пространства имен допускают Переименование элементов. Однако они должны иметь этот набор атрибутов.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_CANDELETE"></span><span id="sfgao_candelete"></span><dl> <dt><strong>SFGAO_CANDELETE</strong></dt> <dt>0x00000020</dt> </dl></td>
<td style="text-align: left;">Указанные элементы можно удалить.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_HASPROPSHEET"></span><span id="sfgao_haspropsheet"></span><dl> <dt><strong>SFGAO_HASPROPSHEET</strong></dt> <dt>0x00000040</dt> </dl></td>
<td style="text-align: left;">Указанные элементы имеют вкладки свойств.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_DROPTARGET"></span><span id="sfgao_droptarget"></span><dl> <dt><strong>SFGAO_DROPTARGET</strong></dt> <dt>0x00000100</dt> </dl></td>
<td style="text-align: left;">Указанные элементы являются целевыми объектами для удаления.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CAPABILITYMASK"></span><span id="sfgao_capabilitymask"></span><dl> <dt><strong>SFGAO_CAPABILITYMASK</strong></dt> <dt>0x00000177</dt> </dl></td>
<td style="text-align: left;">Этот флаг является маской для атрибутов возможностей: SFGAO_CANCOPY, SFGAO_CANMOVE, SFGAO_CANLINK, SFGAO_CANRENAME, SFGAO_CANDELETE, SFGAO_HASPROPSHEET и SFGAO_DROPTARGET. Вызывающие объекты обычно не используют это значение.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_SYSTEM"></span><span id="sfgao_system"></span><dl> <dt><strong>SFGAO_SYSTEM</strong></dt> <dt>0x00001000</dt> </dl></td>
<td style="text-align: left;"><strong>Windows 7 и более поздние версии</strong>. Указанные элементы являются системными элементами.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_ENCRYPTED"></span><span id="sfgao_encrypted"></span><dl> <dt><strong>SFGAO_ENCRYPTED</strong></dt> <dt>0x00002000</dt> </dl></td>
<td style="text-align: left;">Указанные элементы шифруются и могут требовать специальной презентации.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_ISSLOW"></span><span id="sfgao_isslow"></span><dl> <dt><strong>SFGAO_ISSLOW</strong></dt> <dt>0x00004000</dt> </dl></td>
<td style="text-align: left;">Доступ к элементу (через <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a> или другие интерфейсы хранения) должен быть очень высокой операцией. Приложения должны избегать доступа к элементам, помеченным SFGAO_ISSLOW. <br/>
<blockquote>
[!Note]<br />
Открытие потока для элемента обычно выполняется очень часто. SFGAO_ISSLOW указывает, что ожидается, что он будет особенно замедляться, например, при использовании высокодоступных сетевых подключений или автономных файлов (FILE_ATTRIBUTE_OFFLINE). Однако запрос SFGAO_ISSLOW сам по себе является очень высокой операцией. Приложения должны запрашивать SFGAO_ISSLOW только в фоновом потоке. Вместо вызова метода, включающего SFGAO_ISSLOW, может использоваться альтернативный метод, например, извлечение свойства <a href="/windows/desktop/properties/props-system-fileattributes"><strong>PKEY_FileAttributes</strong></a> и тестирование FILE_ATTRIBUTE_OFFLINE.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_GHOSTED"></span><span id="sfgao_ghosted"></span><dl> <dt><strong>SFGAO_GHOSTED</strong></dt> <dt>0x00008000</dt> </dl></td>
<td style="text-align: left;">Указанные элементы отображаются как недоступные для пользователя и недоступны пользователю.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_LINK"></span><span id="sfgao_link"></span><dl> <dt><strong>SFGAO_LINK</strong></dt> <dt>0x00010000</dt> </dl></td>
<td style="text-align: left;">Указанные элементы являются ярлыками.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_SHARE"></span><span id="sfgao_share"></span><dl> <dt><strong>SFGAO_SHARE</strong></dt> <dt>0x00020000</dt> </dl></td>
<td style="text-align: left;">Указанные объекты являются общими.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_READONLY"></span><span id="sfgao_readonly"></span><dl> <dt><strong>SFGAO_READONLY</strong></dt> <dt>0x00040000</dt> </dl></td>
<td style="text-align: left;">Указанные элементы доступны только для чтения. В случае папок это означает, что новые элементы не могут быть созданы в этих папках. Это не следует путать с поведением, заданным флагом FILE_ATTRIBUTE_READONLY, полученным с помощью <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>иколумнпровидер:: жетитемдата</strong></a> в структуре <a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>школумндата</strong></a> . FILE_ATTRIBUTE_READONLY не имеет смысла для папок файловой системы Win32.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_HIDDEN"></span><span id="sfgao_hidden"></span><dl> <dt><strong>SFGAO_HIDDEN</strong></dt> <dt>0x00080000</dt> </dl></td>
<td style="text-align: left;">Элемент скрыт и не должен отображаться, если в <strong>параметрах папки</strong>не включен параметр <strong>Показать скрытые файлы и папки</strong> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_DISPLAYATTRMASK"></span><span id="sfgao_displayattrmask"></span><dl> <dt><strong>SFGAO_DISPLAYATTRMASK</strong></dt> <dt>0x000FC000</dt> </dl></td>
<td style="text-align: left;">Не используйте.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_NONENUMERATED"></span><span id="sfgao_nonenumerated"></span><dl> <dt><strong>SFGAO_NONENUMERATED</strong></dt> <dt>0x00100000</dt> </dl></td>
<td style="text-align: left;">Элементы являются неперечислимыми элементами и должны быть скрыты. Они не возвращаются через перечислитель, например созданный методом <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>ишеллфолдер:: енумобжектс</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_NEWCONTENT"></span><span id="sfgao_newcontent"></span><dl> <dt><strong>SFGAO_NEWCONTENT</strong></dt> <dt>0x00200000</dt> </dl></td>
<td style="text-align: left;">Элементы содержат новое содержимое в соответствии с определением конкретного приложения.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CANMONIKER"></span><span id="sfgao_canmoniker"></span><dl> <dt><strong>SFGAO_CANMONIKER</strong></dt> </dl></td>
<td style="text-align: left;">Не поддерживается.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_HASSTORAGE"></span><span id="sfgao_hasstorage"></span><dl> <dt><strong>SFGAO_HASSTORAGE</strong></dt> </dl></td>
<td style="text-align: left;">Не поддерживается.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_STREAM"></span><span id="sfgao_stream"></span><dl> <dt><strong>SFGAO_STREAM</strong></dt> <dt>0x00400000</dt> </dl></td>
<td style="text-align: left;">Указывает, что элемент имеет связанный с ним поток. Доступ к этому потоку можно получить с помощью вызова <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>ишеллфолдер:: биндтубжект</strong></a> или <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>интерфейса IShellItem:: биндтохандлер</strong></a> с IID_IStream в параметре <em>riid</em> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_STORAGEANCESTOR"></span><span id="sfgao_storageancestor"></span><dl> <dt><strong>SFGAO_STORAGEANCESTOR</strong></dt> <dt>0x00800000</dt> </dl></td>
<td style="text-align: left;">Дочерние элементы этого элемента доступны через <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a> или <a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>IStorage</strong></a>. Эти дочерние элементы помечаются SFGAO_STORAGE или SFGAO_STREAM.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_VALIDATE"></span><span id="sfgao_validate"></span><dl> <dt><strong>SFGAO_VALIDATE</strong></dt> <dt>0x01000000</dt> </dl></td>
<td style="text-align: left;">При указании в качестве входных данных SFGAO_VALIDATE указывает, что папка должна проверять наличие элементов, содержащихся в папке или массиве элементов оболочки. Если один или несколько из этих элементов не существуют, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof"><strong>ишеллфолдер:: жетаттрибутесоф</strong></a> и <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes"><strong>Ишеллитемаррай:: OutAttribute</strong></a> возвращают код ошибки. Этот флаг никогда не возвращается как значение [out].<br/> При использовании с папкой файловой системы SFGAO_VALIDATE указывает папке на удаление кэшированных свойств, полученных клиентами <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex"><strong>IShellFolder2:: жетдетаилсекс</strong></a> , которые могли накапливаться для указанных элементов.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_REMOVABLE"></span><span id="sfgao_removable"></span><dl> <dt><strong>SFGAO_REMOVABLE</strong></dt> <dt>0x02000000</dt> </dl></td>
<td style="text-align: left;">Указанные элементы находятся на съемном носителе или сами по себе являются съемными устройствами.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_COMPRESSED"></span><span id="sfgao_compressed"></span><dl> <dt><strong>SFGAO_COMPRESSED</strong></dt> <dt>0x04000000</dt> </dl></td>
<td style="text-align: left;">Указанные элементы сжимаются.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_BROWSABLE"></span><span id="sfgao_browsable"></span><dl> <dt><strong>SFGAO_BROWSABLE</strong></dt> <dt>0x08000000</dt> </dl></td>
<td style="text-align: left;">Указанные элементы могут размещаться внутри веб-браузера или фрейма проводника Windows.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_FILESYSANCESTOR"></span><span id="sfgao_filesysancestor"></span><dl> <dt><strong>SFGAO_FILESYSANCESTOR</strong></dt> <dt>0x10000000</dt> </dl></td>
<td style="text-align: left;">Указанные папки являются папками файловой системы или содержат по крайней мере один потомок (дочерний, внучатый или более поздний), который является папкой файловой системы (SFGAO_FILESYSTEM).<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_FOLDER"></span><span id="sfgao_folder"></span><dl> <dt><strong>SFGAO_FOLDER</strong></dt> <dt>0x20000000</dt> </dl></td>
<td style="text-align: left;">Указанные элементы являются папками. Некоторые элементы можно пометить как SFGAO_STREAM, так и SFGAO_FOLDER, например сжатый файл с расширением ZIP. Некоторые приложения могут включать этот флаг при тестировании для элементов, которые являются файлами и контейнерами.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_FILESYSTEM"></span><span id="sfgao_filesystem"></span><dl> <dt><strong>SFGAO_FILESYSTEM</strong></dt> <dt>0x40000000</dt> </dl></td>
<td style="text-align: left;">Указанные папки или файлы являются частью файловой системы (то есть файлы, каталоги или корневые каталоги). Проанализированные имена элементов могут считаться допустимыми путями файловой системы Win32. Эти пути могут быть в формате UNC или на основе букв диска.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_STORAGECAPMASK"></span><span id="sfgao_storagecapmask"></span><dl> <dt><strong>SFGAO_STORAGECAPMASK</strong></dt> <dt>0x70C50008</dt> </dl></td>
<td style="text-align: left;">Этот флаг является маской для атрибутов возможностей хранения: SFGAO_STORAGE, SFGAO_LINK, SFGAO_READONLY, SFGAO_STREAM, SFGAO_STORAGEANCESTOR, SFGAO_FILESYSANCESTOR, SFGAO_FOLDER и SFGAO_FILESYSTEM. Вызывающие объекты обычно не используют это значение.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_HASSUBFOLDER"></span><span id="sfgao_hassubfolder"></span><dl> <dt><strong>SFGAO_HASSUBFOLDER</strong></dt> <dt>0x80000000</dt> </dl></td>
<td style="text-align: left;">Указанные папки имеют вложенные папки. Атрибут SFGAO_HASSUBFOLDER содержит только рекомендации и может возвращаться реализациями папок оболочки, даже если они не содержат вложенных папок. Однако обратите внимание, что обратное — не возвращает SFGAO_HASSUBFOLDER — точно так же говорится, что объекты папки не имеют вложенных папок.<br/> Возврат SFGAO_HASSUBFOLDER рекомендуется, если требуется значительное количество времени, чтобы определить, существуют ли какие-либо вложенные папки. Например, оболочка всегда возвращает SFGAO_HASSUBFOLDER, если папка находится на сетевом диске.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_CONTENTSMASK"></span><span id="sfgao_contentsmask"></span><dl> <dt><strong>SFGAO_CONTENTSMASK</strong></dt> <dt>0x80000000</dt> </dl></td>
<td style="text-align: left;">Этот флаг является маской для атрибутов содержимого в настоящее время SFGAO_HASSUBFOLDER. Вызывающие объекты обычно не используют это значение.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_PKEYSFGAOMASK"></span><span id="sfgao_pkeysfgaomask"></span><dl> <dt><strong>SFGAO_PKEYSFGAOMASK</strong></dt> <dt>0x81044000</dt> </dl></td>
<td style="text-align: left;">Маска, используемая свойством <a href="/windows/desktop/properties/props-system-sfgaoflags">PKEY_SFGAOFlags</a> для определения атрибутов, которые считаются причиной медленных вычислений или отсутствия контекста: SFGAO_ISSLOW, SFGAO_READONLY, SFGAO_HASSUBFOLDER и SFGAO_VALIDATE. Вызывающие объекты обычно не используют это значение.<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ишеллфолдер:: Жетаттрибутесоф**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof)
</dt> <dt>

[**Ишеллфолдер::P Арседисплайнаме**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname)
</dt> <dt>

[**Ишеллитемаррай:: OutAttribute**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes)
</dt> </dl>

 

 
