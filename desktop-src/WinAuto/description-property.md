---
title: Свойство Description (специальные возможности Windows)
description: Свойство Description объекта содержит текстовое описание визуального представления объекта.
ms.assetid: 1fe3221f-e1dd-44b2-b749-d00bee1b6b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34320b2959899d049d959037c0f24299780b54b0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488871"
---
# <a name="description-property-windows-accessibility-features"></a>Свойство Description (специальные возможности Windows)

> [!Note]  
> Свойство **Description** часто используется неправильно и не поддерживается службой автоматизации пользовательского интерфейса Майкрософт. Разработчики Microsoft Active Accessibility Server не должны использовать это свойство. Если для специальных возможностей и сценариев автоматизации требуются дополнительные сведения, используйте свойства, поддерживаемые элементами модели автоматизации пользовательского интерфейса и шаблонами элементов управления.

 

Свойство **Description** объекта содержит текстовое описание визуального представления объекта. Описание в основном используется для предоставления более высокого контекста для пользователей с ослабленным зрением или слепых, но также используется для контекстного поиска или других приложений. Это свойство помогает пользователям понять значок или общий внешний вид.

Свойство **Description** извлекается путем вызова метода [**IAccessible:: Get \_ аккдескриптион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).

## <a name="when-to-support-the-description-property"></a>Когда следует поддерживать свойство Description

Серверы поддерживают свойство **Description** , если описание не очевидно или если оно не избыточно в зависимости от свойств [**имени**](name-property.md), [**роли**](role-property.md), [**состояния**](state-property.md)и [**значения**](value-property.md) объекта. Например, кнопка с надписью "ОК" не потребует дополнительной информации, в то время как кнопку, показывающую рисунок кактуса. Свойства **Name**, **Role** и [**Help**](help-property.md) для такой кнопки описывают ее назначение, но свойство **Description** передает менее материальную информацию. Например, "Эта кнопка показывает рисунок кактуса".

Сервер Microsoft Active Accessibility может добавить поддержку автоматизации пользовательского интерфейса с помощью [прямой заметки](direct-annotation.md), с помощью интерфейса [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) или путем реализации службы Microsoft Active Accessibility и модели автоматизации пользовательского интерфейса параллельно с обеими реализациями, обрабатывающими [**сообщение \_ WM GetObject**](wm-getobject.md) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование прямой аннотации](using-direct-annotation.md)
</dt> <dt>

[Интерфейс IAccessibleEx](iaccessibleex.md)
</dt> </dl>

 

 




