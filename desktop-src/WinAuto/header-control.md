---
title: Элемент управления "заголовок" (Справочник по элементам пользовательского интерфейса MSAA)
description: Элемент управления "заголовок" отображает заголовки в верхней части столбцов данных и позволяет пользователю сортировать информацию, щелкая заголовки. Windows Обозреватель использует элемент управления "заголовок", когда выбрано подробное представление.
ms.assetid: 669d6bb8-7bc4-4e6f-bf4f-207887f44b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c378bb0244e94f4cb95c8b2ba90512d2b17542bdef7428197ee58479dbfde1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994184"
---
# <a name="header-control-msaa-ui-element-reference"></a>Элемент управления "заголовок" (Справочник по элементам пользовательского интерфейса MSAA)

> [!Note]  
> В этом разделе описываются объекты **элементов управления заголовков** в целях справочника по элементам ПОЛЬЗОВАТЕЛЬСКОГО интерфейса MSAA. Создание объектов **элементов управления "заголовок** " в различных ПЛАТФОРМАХ пользовательского интерфейса не описывается здесь. См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.

 

Элемент управления "заголовок" отображает заголовки в верхней части столбцов данных и позволяет пользователю сортировать информацию, щелкая заголовки. Windows Обозреватель использует элемент управления "заголовок", когда выбрано подробное представление.

Имя класса Window для элемента управления "заголовок" — это \_ заголовок WC, который определен как "SysHeader32" в коммктрл. h.

## <a name="iaccessible-methods"></a>Методы IAccessible

Элемент управления "заголовок" поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Метод                                                                    | Примечания                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Этот метод выполняет действие по умолчанию, щелкнув заголовок. |
| [**акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                 |
| [**акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                 |
| [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                 |
| [**аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                 |



 

## <a name="iaccessible-properties"></a>Свойства IAccessible

Элемент управления "заголовок" поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Свойство                                                                       | Примечания                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**получить \_ аккчилдкаунт**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | Свойство **ChildCount** равно нулю.                                                                                                                                                                                                   |
| [**получить \_ аккдефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | Свойство **DefaultAction** — "Click".                                                                                                                                                                                             |
| [**получить \_ аккфокус**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 |                                                                                                                                                                                                                                        |
| [**получить \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | Свойство **Name** совпадает с именем заголовка столбца.                                                                                                                                                                    |
| [**получить \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)               | **Родительское** свойство — это окно ( [**\_ \_ список системы ролей**](object-roles.md) ), которое окружает элемент управления и имеет то же имя класса окна, что и элемент управления.                                                      |
| [**получить \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | Свойство **Role** имеет [**роль \_ System \_ колумнхеадер**](object-roles.md).                                                                                                                                  |
| [**получить \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | Значение свойства **State** всегда имеет [**состояние " \_ \_ только для чтения**](object-state-constants.md) ", а также может включать [**систему состояния " \_ \_ невидимая**](object-state-constants.md)". |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Интерфейс IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




