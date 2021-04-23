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
# <a name="description-property-windows-accessibility-features"></a><span data-ttu-id="5166d-103">Свойство Description (специальные возможности Windows)</span><span class="sxs-lookup"><span data-stu-id="5166d-103">Description Property (Windows Accessibility features)</span></span>

> [!Note]  
> <span data-ttu-id="5166d-104">Свойство **Description** часто используется неправильно и не поддерживается службой автоматизации пользовательского интерфейса Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5166d-104">The **Description** property is often used incorrectly and is not supported by Microsoft UI Automation.</span></span> <span data-ttu-id="5166d-105">Разработчики Microsoft Active Accessibility Server не должны использовать это свойство.</span><span class="sxs-lookup"><span data-stu-id="5166d-105">Microsoft Active Accessibility server developers should not use this property.</span></span> <span data-ttu-id="5166d-106">Если для специальных возможностей и сценариев автоматизации требуются дополнительные сведения, используйте свойства, поддерживаемые элементами модели автоматизации пользовательского интерфейса и шаблонами элементов управления.</span><span class="sxs-lookup"><span data-stu-id="5166d-106">If more information is needed for accessibility and automation scenarios, use the properties supported by UI Automation elements and control patterns.</span></span>

 

<span data-ttu-id="5166d-107">Свойство **Description** объекта содержит текстовое описание визуального представления объекта.</span><span class="sxs-lookup"><span data-stu-id="5166d-107">An object's **Description** property provides a textual description about an object's visual appearance.</span></span> <span data-ttu-id="5166d-108">Описание в основном используется для предоставления более высокого контекста для пользователей с ослабленным зрением или слепых, но также используется для контекстного поиска или других приложений.</span><span class="sxs-lookup"><span data-stu-id="5166d-108">The description is primarily used to provide greater context for low-vision or blind users, but is also used for context searching or other applications.</span></span> <span data-ttu-id="5166d-109">Это свойство помогает пользователям понять значок или общий внешний вид.</span><span class="sxs-lookup"><span data-stu-id="5166d-109">This property can help users understand an icon or the overall visual appearance.</span></span>

<span data-ttu-id="5166d-110">Свойство **Description** извлекается путем вызова метода [**IAccessible:: Get \_ аккдескриптион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).</span><span class="sxs-lookup"><span data-stu-id="5166d-110">The **Description** property is retrieved by calling [**IAccessible::get\_accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).</span></span>

## <a name="when-to-support-the-description-property"></a><span data-ttu-id="5166d-111">Когда следует поддерживать свойство Description</span><span class="sxs-lookup"><span data-stu-id="5166d-111">When to Support the Description Property</span></span>

<span data-ttu-id="5166d-112">Серверы поддерживают свойство **Description** , если описание не очевидно или если оно не избыточно в зависимости от свойств [**имени**](name-property.md), [**роли**](role-property.md), [**состояния**](state-property.md)и [**значения**](value-property.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="5166d-112">Servers support the **Description** property if the description is not obvious, or when it is not redundant based on the object's [**Name**](name-property.md), [**Role**](role-property.md), [**State**](state-property.md), and [**Value**](value-property.md) properties.</span></span> <span data-ttu-id="5166d-113">Например, кнопка с надписью "ОК" не потребует дополнительной информации, в то время как кнопку, показывающую рисунок кактуса.</span><span class="sxs-lookup"><span data-stu-id="5166d-113">For example, a button labeled "OK" would not need additional information, whereas a button that shows a picture of a cactus would.</span></span> <span data-ttu-id="5166d-114">Свойства **Name**, **Role** и [**Help**](help-property.md) для такой кнопки описывают ее назначение, но свойство **Description** передает менее материальную информацию. Например, "Эта кнопка показывает рисунок кактуса".</span><span class="sxs-lookup"><span data-stu-id="5166d-114">The **Name**, **Role**, and [**Help**](help-property.md) properties for such a button describe its purpose, but the **Description** property conveys information that is less tangible; for example, "This button shows a picture of a cactus."</span></span>

<span data-ttu-id="5166d-115">Сервер Microsoft Active Accessibility может добавить поддержку автоматизации пользовательского интерфейса с помощью [прямой заметки](direct-annotation.md), с помощью интерфейса [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) или путем реализации службы Microsoft Active Accessibility и модели автоматизации пользовательского интерфейса параллельно с обеими реализациями, обрабатывающими [**сообщение \_ WM GetObject**](wm-getobject.md) .</span><span class="sxs-lookup"><span data-stu-id="5166d-115">A Microsoft Active Accessibility server can add support for UI Automation by using [Direct Annotation](direct-annotation.md), using the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface, or by implementing Microsoft Active Accessibility and UI Automation side-by-side with both implementations handling the [**WM\_GETOBJECT**](wm-getobject.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5166d-116">См. также</span><span class="sxs-lookup"><span data-stu-id="5166d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5166d-117">Использование прямой аннотации</span><span class="sxs-lookup"><span data-stu-id="5166d-117">Using Direct Annotation</span></span>](using-direct-annotation.md)
</dt> <dt>

[<span data-ttu-id="5166d-118">Интерфейс IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="5166d-118">The IAccessibleEx Interface</span></span>](iaccessibleex.md)
</dt> </dl>

 

 




