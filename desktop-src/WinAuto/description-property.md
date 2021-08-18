---
title: свойство Description (Windows специальные возможности)
description: Свойство Description объекта содержит текстовое описание визуального представления объекта.
ms.assetid: 1fe3221f-e1dd-44b2-b749-d00bee1b6b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c695ae4ed8968620776aa0786358c98372940749be4a1c4335cb89f84b373ba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994234"
---
# <a name="description-property-windows-accessibility-features"></a>свойство Description (Windows специальные возможности)

> [!Note]  
> Свойство **Description** часто используется неправильно и не поддерживается службой автоматизации пользовательского интерфейса Майкрософт. Разработчики Microsoft Active Accessibility Server не должны использовать это свойство. Если для специальных возможностей и сценариев автоматизации требуются дополнительные сведения, используйте свойства, поддерживаемые элементами модели автоматизации пользовательского интерфейса и шаблонами элементов управления.

 

Свойство **Description** объекта содержит текстовое описание визуального представления объекта. Описание в основном используется для предоставления более высокого контекста для пользователей с ослабленным зрением или слепых, но также используется для контекстного поиска или других приложений. Это свойство помогает пользователям понять значок или общий внешний вид.

Свойство **Description** извлекается путем вызова метода [**IAccessible:: Get \_ аккдескриптион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).

## <a name="when-to-support-the-description-property"></a>Когда следует поддерживать свойство Description

Серверы поддерживают свойство **Description** , если описание не очевидно или если оно не избыточно в зависимости от свойств [**имени**](name-property.md), [**роли**](role-property.md), [**состояния**](state-property.md)и [**значения**](value-property.md) объекта. Например, кнопка с надписью "ОК" не потребует дополнительной информации, в то время как кнопку, показывающую рисунок кактуса. Свойства **Name**, **Role** и [**Help**](help-property.md) для такой кнопки описывают ее назначение, но свойство **Description** передает менее материальную информацию. Например, "Эта кнопка показывает рисунок кактуса".

Сервер Microsoft Active Accessibility может добавить поддержку автоматизации пользовательского интерфейса с помощью [прямой заметки](direct-annotation.md), с помощью интерфейса [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) или путем реализации службы Microsoft Active Accessibility и модели автоматизации пользовательского интерфейса параллельно с обеими реализациями, обрабатывающими [**сообщение \_ WM GetObject**](wm-getobject.md) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование прямой аннотации](using-direct-annotation.md)
</dt> <dt>

[Интерфейс IAccessibleEx](iaccessibleex.md)
</dt> </dl>

 

 




