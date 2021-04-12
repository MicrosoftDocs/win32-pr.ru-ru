---
title: Элемент управления "заголовок" (Справочник по элементам пользовательского интерфейса MSAA)
description: Элемент управления "заголовок" отображает заголовки в верхней части столбцов данных и позволяет пользователю сортировать информацию, щелкая заголовки. Проводник Windows использует элемент управления "заголовок", когда выбрано подробное представление.
ms.assetid: 669d6bb8-7bc4-4e6f-bf4f-207887f44b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d069770b14ad3ba58022af28ad07fc78cb8c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331440"
---
# <a name="header-control-msaa-ui-element-reference"></a>Элемент управления "заголовок" (Справочник по элементам пользовательского интерфейса MSAA)

> [!Note]  
> В этом разделе описываются объекты **элементов управления заголовков** в целях справочника по элементам ПОЛЬЗОВАТЕЛЬСКОГО интерфейса MSAA. Создание объектов **элементов управления "заголовок** " в различных ПЛАТФОРМАХ пользовательского интерфейса не описывается здесь. См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.

 

Элемент управления "заголовок" отображает заголовки в верхней части столбцов данных и позволяет пользователю сортировать информацию, щелкая заголовки. Проводник Windows использует элемент управления "заголовок", когда выбрано подробное представление.

Имя класса Window для элемента управления "заголовок" — это \_ заголовок WC, который определен как "SysHeader32" в коммктрл. h.

## <a name="iaccessible-methods"></a>Методы IAccessible

Элемент управления "заголовок" поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Метод                                                                    | Комментарии                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Этот метод выполняет действие по умолчанию, щелкнув заголовок. |
| [**акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                 |
| [**акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                 |
| [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                 |
| [**аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                 |



 

## <a name="iaccessible-properties"></a>Свойства IAccessible

Элемент управления "заголовок" поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Свойство                                                                       | Комментарии                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**получить \_ аккчилдкаунт**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | Свойство **ChildCount** равно нулю.                                                                                                                                                                                                   |
| [**получить \_ аккдефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | Свойство **DefaultAction** — "Click".                                                                                                                                                                                             |
| [**получить \_ аккфокус**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 |                                                                                                                                                                                                                                        |
| [**получить \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | Свойство **Name** совпадает с именем заголовка столбца.                                                                                                                                                                    |
| [**получить \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)               | **Родительское** свойство — это окно ( [**\_ \_ список системы ролей**](object-roles.md) ), которое окружает элемент управления и имеет то же имя класса окна, что и элемент управления.                                                      |
| [**получить \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | Свойство **Role** имеет [**роль \_ System \_ колумнхеадер**](object-roles.md).                                                                                                                                  |
| [**получить \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | Значение свойства **State** всегда имеет [**состояние " \_ \_ только для чтения**](object-state-constants.md) ", а также может включать [**систему состояния " \_ \_ невидимая**](object-state-constants.md)". |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейс IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




