---
title: Нерекомендуемые функции node
description: Нерекомендуемые функции node
ms.assetid: 72833757-a356-4727-8fc8-77a60e26aa99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7273ffd6c704c9db6408165d1eba3a293f3d1cf
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "103987955"
---
# <a name="deprecated-node-functions"></a>Нерекомендуемые функции node

> [!Note]  
> Функции шаблона элемента управления, описанные в этом разделе, являются устаревшими. Клиентские приложения должны использовать интерфейсы модели COM, описанные в следующих разделах:
>
> -   [Интерфейсы элементов модели автоматизации пользовательского интерфейса для клиентов](uiauto-entry-uiautoclientinterfaces.md)
> -   [Интерфейс условий свойств для клиентов](uiauto-client-propconditioninterfaces.md)
> -   [Интерфейсы шаблонов элементов управления для клиентов](uiauto-client-controlpatterninterfaces.md)
> -   [Интерфейсы обработки событий для клиентов](uiauto-client-eventhandlinginterfaces.md)
> -   [Интерфейсы фабрики прокси-серверов для клиентов](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a>Содержание раздела



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Функция</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>уиааддевент</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать COM-интерфейсы модели автоматизации пользовательского интерфейса Майкрософт.
</blockquote>
<br/> Добавляет прослушиватель для событий на узле в дереве модели автоматизации пользовательского интерфейса.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>уиаевентаддвиндов</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Добавляет окно в прослушиватель событий.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>уиаевенткаллбакк</em></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Реализованная клиентом функция, вызываемая автоматизацией пользовательского интерфейса при возникновении события, на которое подписан клиент.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>уиаевентремовевиндов</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Удаляет окно из прослушивателя событий.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>уиафинд</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Извлекает один или несколько узлов автоматизации пользовательского интерфейса, соответствующих условиям поиска.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>уиажетеррордескриптион</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Возвращает строку ошибки, чтобы ее можно было передать клиенту. Этот метод не используется клиентами напрямую.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>уиажетпаттернпровидер</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Извлекает <em>шаблон элемента управления</em>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>уиажетпропертивалуе</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Извлекает значение свойства модели автоматизации пользовательского интерфейса.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>уиажетрутноде</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Извлекает корневой узел автоматизации пользовательского интерфейса.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>уиажетрунтимеид</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Получает идентификатор среды выполнения узла модели автоматизации пользовательского интерфейса.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>уиажетупдатедкаче</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Обновляет кэш значений свойств и шаблонов элементов управления.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>уиахпаттернобжектфромвариант</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Возвращает объект шаблона элемента управления из типа <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>уиахтекстранжефромвариант</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Возвращает текстовый диапазон из типа <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>уиахуианодефромвариант</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Возвращает ХУИАНОДЕ из типа <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>уиалукупид</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Возвращает целочисленный идентификатор, который может использоваться в методах, требующих PROPERTYID, ПАТТЕРНИД, КОНТРОЛТИПЕИД, ТЕКСТАТТРИБУТЕИД или EVENTID.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>уианавигате</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Переходит в дерево модели автоматизации пользовательского интерфейса, при необходимости получая кэшированные данные.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>уианодефромфокус</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Извлекает узел модели автоматизации пользовательского интерфейса для элемента пользовательского интерфейса, который в данный момент имеет фокус ввода.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>уианодефромхандле</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Извлекает узел автоматизации пользовательского интерфейса, связанный с окном.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>уианодефромпоинт</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Извлекает узел модели автоматизации пользовательского интерфейса для элемента в указанной точке.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>уианодефромпровидер</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Извлекает узел модели автоматизации пользовательского интерфейса для поставщика необработанных элементов.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>уианодерелеасе</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Удаляет узел из памяти.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>уиапаттернрелеасе</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Удаляет выделенный объект шаблона из памяти.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>уиапровидеркаллбакк</em></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Определяемая приложением функция, которая вызывается автоматизацией пользовательского интерфейса для получения поставщика на стороне клиента для элемента.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>уиаректисемпти</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Возвращает логическое значение, указывающее, имеет ли прямоугольник все его координаты, равные 0.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>уиаректсетемпти</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Устанавливает элементы структуры <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>уиарект</strong></a> в значение 0.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>уиарегистерпровидеркаллбакк</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Регистрирует определенный приложением метод, который вызывается автоматизацией пользовательского интерфейса для получения поставщика для элемента.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>уиаремовивент</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Удаляет прослушиватель для событий на узле в дереве модели автоматизации пользовательского интерфейса.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>уиасетфокус</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Устанавливает фокус ввода на указанный элемент в пользовательском интерфейсе.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>уиатекстранжерелеасе</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.
</blockquote>
<br/> Удаляет выделенный объект текстового диапазона из памяти.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Клиенты автоматизации пользовательского интерфейса](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

