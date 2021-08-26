---
title: Строка меню (Справочник по элементам пользовательского интерфейса MSAA)
description: Строка меню — это область окна, расположенная сразу под строкой заголовка, в которой содержатся пункты меню, такие как файл, Правка, окно и Справка.
ms.assetid: 63b496c7-ae3b-49b5-8c22-41fc9a8f3981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1212ba3c56673ab638e5aeedcc0ce20aea68dda2ad55e0904906d9f809c234ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998414"
---
# <a name="menu-bar-msaa-ui-element-reference"></a>Строка меню (Справочник по элементам пользовательского интерфейса MSAA)

> [!Note]  
> В этом разделе описываются объекты **строки меню** для ссылки на элемент ПОЛЬЗОВАТЕЛЬСКОГО интерфейса MSAA. Создание объектов **строки меню** в различных ПЛАТФОРМАХ пользовательского интерфейса не описывается здесь. См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.

 

Строка меню — это область окна, расположенная сразу под строкой заголовка, в которой содержатся пункты меню, такие как **файл**, **Правка**, **окно** и **Справка**. Microsoft Active Accessibility также создает объект строки меню для системного меню, которое представляет собой меню в левом верхнем углу строки заголовка и содержит пункты меню **восстановить**, **переместить**, **Размер**, **Minimize** и **максимизировать**.

> [!Note]  
> Поскольку элементы управления "строка меню" не получают фокус, методы [**аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) и [**Get \_ аккфокус**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus) не поддерживаются для этого элемента управления.

 

## <a name="iaccessible-methods"></a>Методы IAccessible

Элементы управления "строка меню" поддерживают следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Свойства IAccessible

Элементы управления "строка меню" поддерживают следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Свойство                                                                             | Примечания                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**получить \_ аккчилд**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Извлекает [**IDispatch**](idispatch-interface.md) для указанного элемента меню. Идентификаторы дочерних элементов меню нумеруются последовательно слева направо, начиная с единицы.                                                                                                                                                                                             |
| [**получить \_ аккчилдкаунт**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Свойство **ChildCount** — это число пунктов меню в строке меню. Свойство **ChildCount** для системного меню — это одно из свойств.                                                                                                                                                                                                                                                   |
| [**получить \_ аккдескриптион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | Свойство **Description** строки меню "содержит команды для управления текущим представлением или документом". Свойство **Description** для системного меню — содержит команды для управления окном.                                                                                                                                                                   |
| [**получить \_ аккдефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**получить \_ аккфокус**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**получить \_ акчелп**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**получить \_ акчелптопик**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**получить \_ акккэйбоардшорткут**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Свойство **кэйбоардшорткут** строки меню под заголовком заголовка — "Alt". Свойство **кэйбоардшорткут** для системного меню — "ALT + пробел".                                                                                                                                                                                                                             |
| [**получить \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Свойство **Name** строки меню под заголовком окна "приложение". Свойством " **имя** " для системного меню является "System".                                                                                                                                                                                                                                                |
| [**получить \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**получить \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Свойство **Role** — [**\_ \_ строка подсистемы роли**](object-roles.md).                                                                                                                                                                                                                                                                                      |
| [**получить \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Свойство **State** представляет собой сочетание одного или нескольких из следующих [значений](object-state-constants.md): Системное состояние [**\_ \_ невидимая**](object-state-constants.md) система состояния, \| [**\_ \_ сфокусированная**](object-state-constants.md) на \| [**\_ \_ системе состояния**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Примечания

Система запускает более одного события [**системы событий \_ \_ менустарт**](event-constants.md) , которое не всегда имеет соответствующее событие [**\_ системы событий \_ менуенд**](event-constants.md) . Кроме того, система не вызывает согласованность [**\_ системных событий \_ менупопупстарт**](event-constants.md) и [**событий \_ System \_ менупопупенд**](event-constants.md) . Это известная проблема, которая решена.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Интерфейс IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Пункт меню**](menu-item.md)
</dt> <dt>

[**Всплывающее меню**](pop-up-menu.md)
</dt> </dl>

 

 





