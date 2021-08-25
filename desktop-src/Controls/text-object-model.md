---
title: Объектная модель текста
description: В этом разделе содержатся сведения об элементах программирования, используемых с моделью текстовых объектов (TOM).
ms.assetid: vs|controls|~\controls\richedit\textobjectmodel.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be3b6ce6e91ac2eaca1fdf7636a5a4d0f2ba14eb6791e083d1ab6f37ed49279e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875673"
---
# <a name="text-object-model"></a>Объектная модель текста

В этом разделе содержатся сведения об элементах программирования, используемых с моделью текстовых объектов (TOM).

TOM определяет значительный набор интерфейсов обработки текста. текстовые решения, такие как Microsoft Word и элементы с богатыми возможностями редактирования, поддерживают набор возможностей TOM. на том было сильно влияло на WordBasic (язык программирования, используемый для Word), и его легко использовать в Microsoft Visual Basic для приложений (VBA). Эта совместимость имеет несколько преимуществ.

-   Код может легко переноситься из одного решения в другое.
-   Один язык можно использовать для обмена текстовыми данными между различными текстовыми обработчиками.
-   Это снижает потребность в документации и коде по сравнению с отдельными интерфейсами модели COM и VBA.

Однако это может быть менее эффективным для целей C/C++, чем использование более общих COM-интерфейсов нижнего уровня.

TOM — это простой набор интерфейсов для реализации в основных текстовых решениях, Word и форматированных элементах редактирования. Однако для приложений, которые размещают небольшое внимание на текст, лучше предоставить объект TOM, передавая текст в элемент управления Edit, который поддерживает TOM. Так как широкие возможности управления редактированием поставляются с операционными системами Майкрософт, они являются стандартными средствами для получения функции TOM.

### <a name="overviews"></a>Разделы общих сведений



| Раздел                                                          | Содержимое                                                                                                                                                                                                         |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [О модели текстовых объектов](about-text-object-model.md)         | Объект модели текстовых объектов верхнего уровня (TOM) определяется интерфейсом [**итекстдокумент**](/windows/desktop/api/Tom/nn-tom-itextdocument) , который имеет методы для создания и извлечения объектов в иерархии объектов ниже.<br/> |
| [Использование объектной модели текста](using-the-text-object-model.md) | Примеры кода в этом документе показывают различные аспекты использования объектной модели текста (TOM).<br/>                                                                                                          |



 

### <a name="interfaces"></a>Интерфейсы



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Раздел</th>
<th>Содержимое</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>итекстдокумент</strong></a></td>
<td>Интерфейс <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>итекстдокумент</strong></a> — это интерфейс верхнего уровня Tom, который получает активные объекты выделения и диапазона для любой истории в документе независимо от того, активна или нет. Он позволяет приложению выполнять следующие задачи:
<ul>
<li>Открытие и сохранение документов.</li>
<li>Управление поведением отмены и обновлением экрана.</li>
<li>Поиск диапазона по положению экрана.</li>
<li>Получение перечислителя истории <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>итекстсториранжес</strong></a> .</li>
</ul>
<br/> <strong>Когда следует реализовывать</strong><br/> Обычно приложения не реализуют интерфейс <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>итекстдокумент</strong></a> . Microsoft Text Solutions, например элементы управления Rich Editing, реализуют <strong>итекстдокумент</strong> как часть своей реализации Tom. <br/> <strong>Когда следует использовать</strong><br/> Приложения могут извлекать указатель <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>итекстдокумент</strong></a> из элемента управления Rich Edit. Для этого отправьте <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> сообщение, чтобы получить объект <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>иричедитоле</strong></a> из элемента управления Rich Edit. Затем вызовите метод <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown:: QueryInterface</strong></a> объекта, чтобы получить указатель <strong>итекстдокумент</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>итекстфонт</strong></a></td>
<td>Доступ к атрибутам диапазона форматированного текста осуществляется через пару сдвоенных интерфейсов, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>итекстфонт</strong></a> и <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>итекстпара</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>итекстпара</strong></a></td>
<td>Доступ к атрибутам диапазона форматированного текста осуществляется через пару сдвоенных интерфейсов, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>итекстфонт</strong></a> и <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>итекстпара</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>итекстранже</strong></a></td>
<td>Объекты <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>итекстранже</strong></a> — это мощные средства редактирования и привязки данных, позволяющие программе выбирать текст в истории, а затем проверять или изменять этот текст.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>итекстселектион</strong></a></td>
<td>Выделение текста — это текстовый диапазон с выделением выделения.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>итекстсториранжес</strong></a></td>
<td>Целью интерфейса <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>итекстсториранжес</strong></a> является перечисление историй в <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>итекстдокумент</strong></a>.<br/></td>
</tr>
</tbody>
</table>



 

 

