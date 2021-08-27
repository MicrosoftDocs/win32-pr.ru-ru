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
ms.openlocfilehash: 8e4d367b836516259a4c0f73cea9da20e7e13326
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465031"
---
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a>Объекты оболочки для сценариев и Microsoft Visual Basic

в этом разделе описываются объекты Windows, реализованные оболочкой.

## <a name="in-this-section"></a>В этом разделе




| Раздел | Описание | 
|-------|-------------|
| <a href="didiskquotauser-object.md"><strong>дидисккуотаусер</strong></a><br /> | Позволяет клиенту управлять параметрами дисковой квоты на глобальные тома NTFS. этот объект делает необходимые функции интерфейса <a href="didiskquotauser-object.md"><strong>дидисккуотаусер</strong></a> доступными для создания сценариев и приложений на основе Microsoft Visual Basic.<br /> | 
| <a href="diskquotacontrol-object.md"><strong>дисккуотаконтрол</strong></a><br /> | Позволяет администратору управлять свойствами дисковой квоты тома. Файловая система NTFS позволяет администратору управлять использованием дискового пространства на общем томе, выделяя заданный объем места на диске или <em>предельную квоту</em>для каждого пользователя. Этот объект можно использовать для задания предельной квоты по умолчанию, которая будет автоматически назначена всем новым пользователям.<br /> | 
| <a href="dshellwindowsevents.md"><strong>дшеллвиндовсевентс</strong></a><br /> | Получает события регистрации окна <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>ишеллвиндовс</strong></a> . <br /> | 
| <a href="folder.md"><strong>Папка</strong></a><br /> | Представляет папку оболочки. Этот объект содержит свойства и методы, позволяющие получить сведения о папке.<br /> | 
| <a href="folder2-object.md"><strong>Folder2</strong></a><br /> | Расширяет объект <a href="folder.md"><strong>Folder</strong></a> для поддержки автономных папок.<br /> | 
| <a href="folderitem.md"><strong>FolderItem</strong></a><br /> | Представляет элемент в папке оболочки. Этот объект содержит свойства и методы, позволяющие получить сведения об элементе.<br /> | 
| <a href="folderitems.md"><strong>фолдеритемс</strong></a><br /> | Представляет коллекцию элементов в папке оболочки. Этот объект содержит свойства и методы, позволяющие получить сведения о коллекции.<br /> | 
| <a href="folderitems2-object.md"><strong>FolderItems2</strong></a><br /> | Расширяет объект <a href="folderitems.md"><strong>фолдеритемс</strong></a> . Он поддерживает один дополнительный метод.<br /> | 
| <a href="folderitems3-object.md"><strong>FolderItems3</strong></a><br /> | Расширяет объект <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> . Этот объект поддерживает дополнительный метод и свойство.<br /> | 
| <a href="folderitemverb.md"><strong>фолдеритемверб</strong></a><br /> | Представляет единственную команду, доступную для элемента. Этот объект содержит свойства и методы, позволяющие получить сведения о команде.<br /> | 
| <a href="folderitemverbs.md"><strong>фолдеритемвербс</strong></a><br /> | Представляет коллекцию команд для элемента в папке оболочки. Этот объект содержит свойства и методы, позволяющие получить сведения о коллекции.<br /> | 
| <a href="ishelldispatch.md"><strong>ишеллдиспатч</strong></a><br /> | Представляет объект в оболочке. Предоставляются методы для управления оболочкой и выполнения команд в оболочке. Существуют также методы для получения других объектов, связанных с оболочкой. <br /><blockquote>[!Note]<br /><a href="ishelldispatch.md"><strong>Ишеллдиспатч</strong></a> реализован и доступен через объект <a href="shell.md"><strong>Shell</strong></a> .</blockquote><br /> | 
| <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a><br /> | Расширяет объект <a href="ishelldispatch.md"><strong>ишеллдиспатч</strong></a> с помощью ряда новых функциональных возможностей. <br /><blockquote>[!Note]<br /><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> реализован и доступен через объект <a href="shell.md"><strong>Shell</strong></a> .</blockquote><br /> | 
| <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a><br /> | Расширяет объект <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> . <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> поддерживает один новый метод в дополнение к свойствам и методам, поддерживаемым <strong>IShellDispatch2</strong>. <br /><blockquote>[!Note]<br /><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> реализован и доступен через объект <a href="shell.md"><strong>Shell</strong></a> .</blockquote><br /> | 
| <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a><br /> | Расширяет объект <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> . В дополнение к свойствам и методам, поддерживаемым <strong>IShellDispatch3</strong>, <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> поддерживает четыре дополнительных метода. <br /><blockquote>[!Note]<br /><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> реализован и доступен через объект <a href="shell.md"><strong>Shell</strong></a> .</blockquote><br /> | 
| <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a><br /> | Расширяет объект <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> . В дополнение к свойствам и методам, поддерживаемым <strong>IShellDispatch4</strong>, <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> добавляет метод, который отображает открытые окна в трехмерном стеке. <br /><blockquote>[!Note]<br /><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> реализован и доступен через объект <a href="shell.md"><strong>Shell</strong></a> .</blockquote><br /> | 
| <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a><br /> | Расширяет объект <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> . В дополнение к свойствам и методам, поддерживаемым <strong>IShellDispatch5</strong>, <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> добавляет метод, отображающий панель поиска приложений. <br /><blockquote>[!Note]<br /><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> реализован и доступен через объект <a href="shell.md"><strong>Shell</strong></a> .</blockquote><br /> | 
| <a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a><br /> | Расширяет объект <a href="shelllinkobject-object.md"><strong>шелллинкобжект</strong></a> и поддерживает одно дополнительное свойство.<br /> | 
| <a href="newwdevents.md"><strong>неввдевентс</strong></a><br /> | Расширяет объект <a href="webwizardhost.md"><strong>вебвизардхост</strong></a> , позволяя страницам на стороне сервера, размещенным в мастере, проверять, что пользователь прошел проверку подлинности с помощью учетная запись Майкрософт.<br /> | 
| <a href="shell.md"><strong>Shell</strong></a><br /> | Представляет объекты в оболочке. Предоставляются методы для управления оболочкой и выполнения команд в оболочке. Существуют также методы для получения других объектов, связанных с оболочкой.<br /> | 
| <a href="shellfolderitem-object.md"><strong>шеллфолдеритем</strong></a><br /> | Расширяет объект <a href="folderitem.md"><strong>FolderItem</strong></a> . В дополнение к свойствам и методам, поддерживаемым <strong>FolderItem</strong>, <a href="shellfolderitem-object.md"><strong>шеллфолдеритем</strong></a> имеет два дополнительных метода.<br /> | 
| <a href="shellfolderview.md"><strong>шеллфолдервиев</strong></a><br /> | Представляет объекты в представлении и предоставляет свойства и методы, используемые для получения сведений о содержимом представления.<br /> | 
| <a href="shellfolderviewoc-object.md"><strong>шеллфолдервиевок</strong></a><br /> | Перенаправляет события, инициируемые указанным объектом <a href="shellfolderview.md"><strong>шеллфолдервиев</strong></a> , в соответствующие обработчики событий <a href="shellfolderviewoc-object.md"><strong>шеллфолдервиевок</strong></a> .<br /> | 
| <a href="shelllinkobject-object.md"><strong>шелллинкобжект</strong></a><br /> | Управляет связями оболочки. Этот объект делает большую часть функциональных возможностей интерфейса <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>ишелллинк</strong></a> , доступного для сценариев приложений. <br /> | 
| <a href="shelluihelper.md"><strong>шеллуихелпер</strong></a><br /> | реализовано оболочкой, чтобы помочь скриптам и Visual Basic разработчикам использовать некоторые функции, доступные в оболочке. Объект <a href="shelluihelper.md"><strong>шеллуихелпер</strong></a> не имеет свойств или событий. Для добавления элементов в оболочку предоставляются методы.<br /> | 
| <a href="shellwindows.md"><strong>шеллвиндовс</strong></a><br /> | Представляет коллекцию открытых окон, принадлежащих оболочке. Методы, связанные с этими объектами, могут управлять и выполнять команды в оболочке и получать другие объекты, связанные с оболочкой.<br /> | 
| <a href="webwizardhost.md"><strong>вебвизардхост</strong></a><br /> | Предоставляет методы, позволяющие HTML-страницам, размещенным в расширении мастера, взаимодействовать с мастером.<br /> | 




 

 

 




