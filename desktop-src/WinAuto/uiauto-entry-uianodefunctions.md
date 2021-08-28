---
title: Нерекомендуемые функции node
description: Нерекомендуемые функции node
ms.assetid: 72833757-a356-4727-8fc8-77a60e26aa99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d700c506ee0bb0baf41cdd2facb85b0e7153d57
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476170"
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




| Компонент | Описание | 
|----------|-------------|
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>уиааддевент</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать COM-интерфейсы модели автоматизации пользовательского интерфейса Майкрософт.</blockquote><br /> Добавляет прослушиватель для событий на узле в дереве модели автоматизации пользовательского интерфейса.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>уиаевентаддвиндов</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Добавляет окно в прослушиватель событий.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>уиаевенткаллбакк</em></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Реализованная клиентом функция, вызываемая автоматизацией пользовательского интерфейса при возникновении события, на которое подписан клиент.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>уиаевентремовевиндов</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Удаляет окно из прослушивателя событий.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>уиафинд</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Извлекает один или несколько узлов автоматизации пользовательского интерфейса, соответствующих условиям поиска.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>уиажетеррордескриптион</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Возвращает строку ошибки, чтобы ее можно было передать клиенту. Этот метод не используется клиентами напрямую.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>уиажетпаттернпровидер</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Извлекает <em>шаблон элемента управления</em>.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>уиажетпропертивалуе</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Извлекает значение свойства модели автоматизации пользовательского интерфейса.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>уиажетрутноде</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Извлекает корневой узел автоматизации пользовательского интерфейса.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>уиажетрунтимеид</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Получает идентификатор среды выполнения узла модели автоматизации пользовательского интерфейса.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>уиажетупдатедкаче</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Обновляет кэш значений свойств и шаблонов элементов управления.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>уиахпаттернобжектфромвариант</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Возвращает объект шаблона элемента управления из типа <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>уиахтекстранжефромвариант</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Возвращает текстовый диапазон из типа <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>уиахуианодефромвариант</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Возвращает ХУИАНОДЕ из типа <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>уиалукупид</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Возвращает целочисленный идентификатор, который может использоваться в методах, требующих PROPERTYID, ПАТТЕРНИД, КОНТРОЛТИПЕИД, ТЕКСТАТТРИБУТЕИД или EVENTID.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>уианавигате</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Переходит в дерево модели автоматизации пользовательского интерфейса, при необходимости получая кэшированные данные.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>уианодефромфокус</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Извлекает узел модели автоматизации пользовательского интерфейса для элемента пользовательского интерфейса, который в данный момент имеет фокус ввода.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>уианодефромхандле</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Извлекает узел автоматизации пользовательского интерфейса, связанный с окном.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>уианодефромпоинт</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Извлекает узел модели автоматизации пользовательского интерфейса для элемента в указанной точке.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>уианодефромпровидер</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Извлекает узел модели автоматизации пользовательского интерфейса для поставщика необработанных элементов.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>уианодерелеасе</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Удаляет узел из памяти.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>уиапаттернрелеасе</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Удаляет выделенный объект шаблона из памяти.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>уиапровидеркаллбакк</em></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Определяемая приложением функция, которая вызывается автоматизацией пользовательского интерфейса для получения поставщика на стороне клиента для элемента.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>уиаректисемпти</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Возвращает логическое значение, указывающее, имеет ли прямоугольник все его координаты, равные 0.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>уиаректсетемпти</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Устанавливает элементы структуры <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>уиарект</strong></a> в значение 0.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>уиарегистерпровидеркаллбакк</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Регистрирует определенный приложением метод, который вызывается автоматизацией пользовательского интерфейса для получения поставщика для элемента.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>уиаремовивент</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Удаляет прослушиватель для событий на узле в дереве модели автоматизации пользовательского интерфейса.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>уиасетфокус</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Устанавливает фокус ввода на указанный элемент в пользовательском интерфейсе.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>уиатекстранжерелеасе</strong></a><br /> | <blockquote>[!Note]<br />Эта функция является устаревшей. Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</blockquote><br /> Удаляет выделенный объект текстового диапазона из памяти.<br /> | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Клиенты автоматизации пользовательского интерфейса](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

