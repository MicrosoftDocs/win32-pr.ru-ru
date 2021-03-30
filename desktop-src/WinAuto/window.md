---
title: Window (Справочник по элементу пользовательского интерфейса MSAA)
description: Microsoft Active Accessibility создает универсальный объект Window в качестве контейнера для другого объекта. Разработчики клиентов не передают информацию от объектов окон конечным пользователям, поскольку эти объекты не содержат полезной информации.
ms.assetid: cc32528f-c454-4522-91b9-06f87cff8bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d87c8601ecd6344dc82bbdb416055c694687e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774807"
---
# <a name="window-msaa-ui-element-reference"></a>Window (Справочник по элементу пользовательского интерфейса MSAA)

> [!Note]  
> В этом разделе описываются объекты **окна** для ссылки на элемент ПОЛЬЗОВАТЕЛЬСКОГО интерфейса MSAA. Создание объектов **Window** в различных ПЛАТФОРМАХ пользовательского интерфейса не описывается здесь. См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.

 

Microsoft Active Accessibility создает универсальный объект Window в качестве контейнера для другого объекта. Разработчики клиентов не передают информацию от объектов окон конечным пользователям, поскольку эти объекты не содержат полезной информации.

Если серверное приложение создает пользовательский элемент управления, то Microsoft Active Accessibility создает объект Window, содержащий пользовательский элемент управления, но сервер создает доступный объект для предоставления сведений о содержимом элемента управления. Система создает события уровня объекта для объекта Window, но сервер должен отправить события для доступного объекта, предоставляющего сведения об элементе управления.

## <a name="iaccessible-methods"></a>Методы IAccessible

Объект Window поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Свойства IAccessible

Объект Window поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Свойство                                                                             | Комментарии                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**получить \_ аккчилд**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Извлекает интерфейс [IDispatch](idispatch-interface.md) указанного дочернего элемента.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**получить \_ аккчилдкаунт**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Свойство **ChildCount** имеет значение 7.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**получить \_ аккдескриптион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | Сам объект окна не имеет свойства **Description** . Свойство **Description** для дочернего объекта можно получить с помощью объекта Window.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**получить \_ аккфокус**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**получить \_ акккэйбоардшорткут**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Сам объект окна не имеет свойства **кэйбоардшорткут** . Свойство **кэйбоардшорткут** для дочернего объекта извлекается через объект Window.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**получить \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Свойство **Name** объекта Window совпадает с дочерним объектом.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**получить \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**получить \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Свойство **Role** является [**\_ системным \_ окном роли**](object-roles.md). **Роль** дочернего объекта извлекается через объект Window.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**получить \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Свойство **State** представляет собой сочетание одного или нескольких из следующих [значений](object-state-constants.md): система состояния " [**\_ \_ невидимая**](object-state-constants.md) система состояния" \| [**\_ \_ недоступна**](object-state-constants.md) система состояний \| [**\_ \_ немалым**](object-state-constants.md) система \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) отслеживания состояния фокус системы система отслеживания состояния<br/> |



 

## <a name="notes"></a>Примечания

Системные объекты [**событий \_ \_ драгдропстарт**](event-constants.md), [**\_ \_ драгдропенд системы**](event-constants.md)событий, [**объектов событий \_ \_ скрыты**](event-constants.md), а [**\_ объекты событий \_ парентчанже**](event-constants.md) не отправляются объектом Window. Это известная проблема, которая решена.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейс IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





