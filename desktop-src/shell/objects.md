---
description: в этом разделе описываются объекты Windows, реализованные оболочкой.
title: Объекты оболочки для сценариев и Microsoft Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.assetid: eee58404-808b-451c-8325-8dcd9537fd11
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bd2c924d9b66194c8f016fc8b1c16bed8a7e3c62f82e3673837e0e31c8563fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858803"
---
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a>Объекты оболочки для сценариев и Microsoft Visual Basic

в этом разделе описываются объекты Windows, реализованные оболочкой.

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
<td><a href="didiskquotauser-object.md"><strong>дидисккуотаусер</strong></a><br/></td>
<td>Позволяет клиенту управлять параметрами дисковой квоты на глобальные тома NTFS. этот объект делает необходимые функции интерфейса <a href="didiskquotauser-object.md"><strong>дидисккуотаусер</strong></a> доступными для создания сценариев и приложений на основе Microsoft Visual Basic.<br/></td>
</tr>
<tr class="even">
<td><a href="diskquotacontrol-object.md"><strong>дисккуотаконтрол</strong></a><br/></td>
<td>Позволяет администратору управлять свойствами дисковой квоты тома. Файловая система NTFS позволяет администратору управлять использованием дискового пространства на общем томе, выделяя заданный объем места на диске или <em>предельную квоту</em>для каждого пользователя. Этот объект можно использовать для задания предельной квоты по умолчанию, которая будет автоматически назначена всем новым пользователям.<br/></td>
</tr>
<tr class="odd">
<td><a href="dshellwindowsevents.md"><strong>дшеллвиндовсевентс</strong></a><br/></td>
<td>Получает события регистрации окна <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>ишеллвиндовс</strong></a> . <br/></td>
</tr>
<tr class="even">
<td><a href="folder.md"><strong>Папка</strong></a><br/></td>
<td>Представляет папку оболочки. Этот объект содержит свойства и методы, позволяющие получить сведения о папке.<br/></td>
</tr>
<tr class="odd">
<td><a href="folder2-object.md"><strong>Folder2</strong></a><br/></td>
<td>Расширяет объект <a href="folder.md"><strong>Folder</strong></a> для поддержки автономных папок.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitem.md"><strong>FolderItem</strong></a><br/></td>
<td>Представляет элемент в папке оболочки. Этот объект содержит свойства и методы, позволяющие получить сведения об элементе.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitems.md"><strong>фолдеритемс</strong></a><br/></td>
<td>Представляет коллекцию элементов в папке оболочки. Этот объект содержит свойства и методы, позволяющие получить сведения о коллекции.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitems2-object.md"><strong>FolderItems2</strong></a><br/></td>
<td>Расширяет объект <a href="folderitems.md"><strong>фолдеритемс</strong></a> . Он поддерживает один дополнительный метод.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitems3-object.md"><strong>FolderItems3</strong></a><br/></td>
<td>Расширяет объект <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> . Этот объект поддерживает дополнительный метод и свойство.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitemverb.md"><strong>фолдеритемверб</strong></a><br/></td>
<td>Представляет единственную команду, доступную для элемента. Этот объект содержит свойства и методы, позволяющие получить сведения о команде.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitemverbs.md"><strong>фолдеритемвербс</strong></a><br/></td>
<td>Представляет коллекцию команд для элемента в папке оболочки. Этот объект содержит свойства и методы, позволяющие получить сведения о коллекции.<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch.md"><strong>ишеллдиспатч</strong></a><br/></td>
<td>Представляет объект в оболочке. Предоставляются методы для управления оболочкой и выполнения команд в оболочке. Существуют также методы для получения других объектов, связанных с оболочкой. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch.md"><strong>Ишеллдиспатч</strong></a> реализован и доступен через объект <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a><br/></td>
<td>Расширяет объект <a href="ishelldispatch.md"><strong>ишеллдиспатч</strong></a> с помощью ряда новых функциональных возможностей. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> реализован и доступен через объект <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a><br/></td>
<td>Расширяет объект <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> . <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> поддерживает один новый метод в дополнение к свойствам и методам, поддерживаемым <strong>IShellDispatch2</strong>. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> реализован и доступен через объект <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a><br/></td>
<td>Расширяет объект <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> . В дополнение к свойствам и методам, поддерживаемым <strong>IShellDispatch3</strong>, <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> поддерживает четыре дополнительных метода. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> реализован и доступен через объект <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a><br/></td>
<td>Расширяет объект <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> . В дополнение к свойствам и методам, поддерживаемым <strong>IShellDispatch4</strong>, <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> добавляет метод, который отображает открытые окна в трехмерном стеке. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> реализован и доступен через объект <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a><br/></td>
<td>Расширяет объект <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> . В дополнение к свойствам и методам, поддерживаемым <strong>IShellDispatch5</strong>, <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> добавляет метод, отображающий панель поиска приложений. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> реализован и доступен через объект <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a><br/></td>
<td>Расширяет объект <a href="shelllinkobject-object.md"><strong>шелллинкобжект</strong></a> и поддерживает одно дополнительное свойство.<br/></td>
</tr>
<tr class="odd">
<td><a href="newwdevents.md"><strong>неввдевентс</strong></a><br/></td>
<td>Расширяет объект <a href="webwizardhost.md"><strong>вебвизардхост</strong></a> , позволяя страницам на стороне сервера, размещенным в мастере, проверять, что пользователь прошел проверку подлинности с помощью учетная запись Майкрософт.<br/></td>
</tr>
<tr class="even">
<td><a href="shell.md"><strong>Shell</strong></a><br/></td>
<td>Представляет объекты в оболочке. Предоставляются методы для управления оболочкой и выполнения команд в оболочке. Существуют также методы для получения других объектов, связанных с оболочкой.<br/></td>
</tr>
<tr class="odd">
<td><a href="shellfolderitem-object.md"><strong>шеллфолдеритем</strong></a><br/></td>
<td>Расширяет объект <a href="folderitem.md"><strong>FolderItem</strong></a> . В дополнение к свойствам и методам, поддерживаемым <strong>FolderItem</strong>, <a href="shellfolderitem-object.md"><strong>шеллфолдеритем</strong></a> имеет два дополнительных метода.<br/></td>
</tr>
<tr class="even">
<td><a href="shellfolderview.md"><strong>шеллфолдервиев</strong></a><br/></td>
<td>Представляет объекты в представлении и предоставляет свойства и методы, используемые для получения сведений о содержимом представления.<br/></td>
</tr>
<tr class="odd">
<td><a href="shellfolderviewoc-object.md"><strong>шеллфолдервиевок</strong></a><br/></td>
<td>Перенаправляет события, инициируемые указанным объектом <a href="shellfolderview.md"><strong>шеллфолдервиев</strong></a> , в соответствующие обработчики событий <a href="shellfolderviewoc-object.md"><strong>шеллфолдервиевок</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="shelllinkobject-object.md"><strong>шелллинкобжект</strong></a><br/></td>
<td>Управляет связями оболочки. Этот объект делает большую часть функциональных возможностей интерфейса <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>ишелллинк</strong></a> , доступного для сценариев приложений. <br/></td>
</tr>
<tr class="odd">
<td><a href="shelluihelper.md"><strong>шеллуихелпер</strong></a><br/></td>
<td>реализовано оболочкой, чтобы помочь скриптам и Visual Basic разработчикам использовать некоторые функции, доступные в оболочке. Объект <a href="shelluihelper.md"><strong>шеллуихелпер</strong></a> не имеет свойств или событий. Для добавления элементов в оболочку предоставляются методы.<br/></td>
</tr>
<tr class="even">
<td><a href="shellwindows.md"><strong>шеллвиндовс</strong></a><br/></td>
<td>Представляет коллекцию открытых окон, принадлежащих оболочке. Методы, связанные с этими объектами, могут управлять и выполнять команды в оболочке и получать другие объекты, связанные с оболочкой.<br/></td>
</tr>
<tr class="odd">
<td><a href="webwizardhost.md"><strong>вебвизардхост</strong></a><br/></td>
<td>Предоставляет методы, позволяющие HTML-страницам, размещенным в расширении мастера, взаимодействовать с мастером.<br/></td>
</tr>
</tbody>
</table>



 

 

 




