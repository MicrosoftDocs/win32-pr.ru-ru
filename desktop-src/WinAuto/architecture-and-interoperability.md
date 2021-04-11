---
title: Архитектура и взаимодействие
description: В этом разделе кратко описывается архитектура Microsoft Active Accessibility и Microsoft UI Automation, а также компоненты, которые позволяют взаимодействовать между приложениями на основе двух различных технологий.
ms.assetid: 7309819c-7c72-4bb3-ab9c-608a27c56d42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f318e46a6a0ad833b7aedb114974240fc4e52c08
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "104133418"
---
# <a name="architecture-and-interoperability"></a><span data-ttu-id="ef578-103">Архитектура и взаимодействие</span><span class="sxs-lookup"><span data-stu-id="ef578-103">Architecture and Interoperability</span></span>

<span data-ttu-id="ef578-104">В этом разделе кратко описывается архитектура Microsoft Active Accessibility и Microsoft UI Automation, а также компоненты, которые позволяют взаимодействовать между приложениями на основе двух различных технологий.</span><span class="sxs-lookup"><span data-stu-id="ef578-104">This topic briefly describes the architecture of Microsoft Active Accessibility and Microsoft UI Automation, and the components that allow interoperability between applications based on the two different technologies.</span></span>

<span data-ttu-id="ef578-105">Дополнительные сведения о взаимодействии Microsoft Active Accessibility и автоматизации пользовательского интерфейса см. в разделе [Общая инфраструктура](common-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="ef578-105">For more information about Microsoft Active Accessibility and UI Automation interoperability, see [Common Infrastructure](common-infrastructure.md).</span></span>

<span data-ttu-id="ef578-106">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="ef578-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ef578-107">Архитектура Active Accessibility Майкрософт</span><span class="sxs-lookup"><span data-stu-id="ef578-107">Microsoft Active Accessibility Architecture</span></span>](#microsoft-active-accessibility-architecture)
-   [<span data-ttu-id="ef578-108">Архитектура модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="ef578-108">UI Automation Architecture</span></span>](#ui-automation-architecture)
-   [<span data-ttu-id="ef578-109">Взаимодействие Microsoft Active Accessibility и автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="ef578-109">Microsoft Active Accessibility and UI Automation Interoperability</span></span>](#microsoft-active-accessibility-and-ui-automation-interoperability)
-   [<span data-ttu-id="ef578-110">Интерфейс IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="ef578-110">The IAccessibleEx Interface</span></span>](#the-iaccessibleex-interface)
-   [<span data-ttu-id="ef578-111">См. также</span><span class="sxs-lookup"><span data-stu-id="ef578-111">Related topics</span></span>](#related-topics)

## <a name="microsoft-active-accessibility-architecture"></a><span data-ttu-id="ef578-112">Архитектура Active Accessibility Майкрософт</span><span class="sxs-lookup"><span data-stu-id="ef578-112">Microsoft Active Accessibility Architecture</span></span>

<span data-ttu-id="ef578-113">Microsoft Active Accessibility предоставляет основные сведения об элементах управления, таких как имя элемента управления, расположение на экране и тип элемента управления, а также сведения о состоянии, такие как видимость и состояние включения или отключения.</span><span class="sxs-lookup"><span data-stu-id="ef578-113">Microsoft Active Accessibility exposes basic information about controls such as control name, location on screen, and type of control, as well as state information such as visibility and enabled/disabled status.</span></span> <span data-ttu-id="ef578-114">Пользовательский интерфейс представлен как иерархия объектов со специальными возможностями; изменения и действия представлены в виде Виневентс.</span><span class="sxs-lookup"><span data-stu-id="ef578-114">The UI is represented as a hierarchy of accessible objects; changes and actions are represented as WinEvents.</span></span>

<span data-ttu-id="ef578-115">Microsoft Active Accessibility состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="ef578-115">Microsoft Active Accessibility consists of the following components:</span></span>

-   <span data-ttu-id="ef578-116">Доступный объект — логический элемент пользовательского интерфейса (например, кнопка), представленный интерфейсом модели компонента [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (com) и целочисленным дочерним идентификатором (чилдид).</span><span class="sxs-lookup"><span data-stu-id="ef578-116">Accessible object—A logical UI element (such as a button) that is represented by an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Component Object Model (COM) interface and an integer child identifier (ChildID).</span></span>
-   <span data-ttu-id="ef578-117">Виневентс — система событий, которая позволяет серверам уведомлять клиентов при изменении объекта со специальными возможностями.</span><span class="sxs-lookup"><span data-stu-id="ef578-117">WinEvents—An event system that enables servers to notify clients when an accessible object changes.</span></span> <span data-ttu-id="ef578-118">Дополнительные сведения см. в разделе [виневентс](winevents-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="ef578-118">For more information, see [WinEvents](winevents-infrastructure.md).</span></span>
-   <span data-ttu-id="ef578-119">OLEACC.dll — библиотека динамических связей среды выполнения, которая предоставляет API Microsoft Active Accessibility и платформу специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="ef578-119">OLEACC.dll—The run-time, dynamic-link library that provides the Microsoft Active Accessibility API and the accessibility system framework.</span></span> <span data-ttu-id="ef578-120">ОЛЕАКК реализует прокси-объекты, предоставляющие сведения о специальных возможностях по умолчанию для стандартных элементов пользовательского интерфейса, включая пользовательские элементы управления, меню пользователей и общие элементы управления.</span><span class="sxs-lookup"><span data-stu-id="ef578-120">OLEACC implements proxy objects that provide default accessibility information for standard UI elements, including USER controls, USER menus, and common controls.</span></span>

<span data-ttu-id="ef578-121">Для Microsoft Active Accessibility системный компонент инфраструктуры специальных возможностей (ОЛЕАКК) помогает организовать взаимодействие между вспомогательными технологиями (средства специальных возможностей) и приложениями, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="ef578-121">For Microsoft Active Accessibility, the system component of the accessibility framework (OLEACC) helps the communication between assistive technologies (accessibility tools) and applications, as the following illustration shows.</span></span>

![Иллюстрация взаимодействия средств специальных возможностей с приложениями](images/msaaarch.gif)

<span data-ttu-id="ef578-123">Приложения (серверы Microsoft Active Accessibility) предоставляют сведения о специальных возможностях в пользовательском интерфейсе для средств (клиентов Microsoft Active Accessibility), взаимодействующих с пользовательским интерфейсом от имени пользователей.</span><span class="sxs-lookup"><span data-stu-id="ef578-123">The applications (Microsoft Active Accessibility servers) provide UI accessibility information to tools (Microsoft Active Accessibility clients), which interact with the UI on behalf of users.</span></span> <span data-ttu-id="ef578-124">Граница кода является программной и границей процесса.</span><span class="sxs-lookup"><span data-stu-id="ef578-124">The code boundary is both a programmatic and a process boundary.</span></span>

## <a name="ui-automation-architecture"></a><span data-ttu-id="ef578-125">Архитектура модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="ef578-125">UI Automation Architecture</span></span>

<span data-ttu-id="ef578-126">При использовании модели автоматизации ПОЛЬЗОВАТЕЛЬСКОГО интерфейса основной компонент модели автоматизации пользовательского интерфейса (UIAutomationCore.dll) загружается в процессы специальных возможностей и приложений.</span><span class="sxs-lookup"><span data-stu-id="ef578-126">With UI Automation, the UI Automation core component (UIAutomationCore.dll) is loaded into both the accessibility tools' and applications' processes.</span></span> <span data-ttu-id="ef578-127">Основной компонент управляет межпроцессным обменом данными, предоставляет службы более высокого уровня, такие как поиск элементов по значениям свойств, и обеспечивает возможность многоуровневой выборки или кэширования свойств, что обеспечивает лучшую производительность по сравнению с реализацией Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="ef578-127">The core component manages cross-process communication, provides higher level services such as searching for elements by property values, and enables bulk fetching or caching of properties, which provides better performance than the Microsoft Active Accessibility implementation.</span></span>

<span data-ttu-id="ef578-128">Модель автоматизации пользовательского интерфейса включает прокси-объекты, предоставляющие сведения о стандартных элементах пользовательского интерфейса, таких как пользовательские элементы управления, меню пользователей и общие элементы управления.</span><span class="sxs-lookup"><span data-stu-id="ef578-128">UI Automation includes proxy objects that provide UI information about standard UI elements such as USER controls, USER menus, and common controls.</span></span> <span data-ttu-id="ef578-129">Он также включает учетные записи-посредники, позволяющие клиентам автоматизации пользовательского интерфейса получать сведения о пользовательском интерфейсе от серверов Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="ef578-129">It also includes proxies that enable UI Automation clients to get UI information from Microsoft Active Accessibility servers.</span></span>

<span data-ttu-id="ef578-130">На следующем рисунке показаны связи между различными компонтентсами автоматизации пользовательского интерфейса, используемыми в средствах специальных возможностей (клиенты) и в приложениях (поставщики).</span><span class="sxs-lookup"><span data-stu-id="ef578-130">The following illustration shows the relationships among the various UI Automation compontents used in accessibility tools (clients) and in applications (providers).</span></span>

![Иллюстрация взаимодействия средств специальных возможностей с компонентами в приложениях](images/uiaarch.gif)

## <a name="microsoft-active-accessibility-and-ui-automation-interoperability"></a><span data-ttu-id="ef578-132">Взаимодействие Microsoft Active Accessibility и автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="ef578-132">Microsoft Active Accessibility and UI Automation Interoperability</span></span>

<span data-ttu-id="ef578-133">Модель автоматизации пользовательского интерфейса для Microsoft Active Accessibility Bridge позволяет клиентам Microsoft Active Accessibility доступ к поставщикам автоматизации ПОЛЬЗОВАТЕЛЬСКОГО интерфейса путем преобразования объектной модели автоматизации пользовательского интерфейса в объектную модель Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="ef578-133">The UI Automation to Microsoft Active Accessibility Bridge enables Microsoft Active Accessibility clients to access UI Automation providers by converting the UI Automation object model to a Microsoft Active Accessibility object model.</span></span> <span data-ttu-id="ef578-134">На следующем рисунке показана роль модели автоматизации пользовательского интерфейса Active Accessibility моста.</span><span class="sxs-lookup"><span data-stu-id="ef578-134">The following illustration shows the role of the UI Automation-to-Microsoft Active Accessibility Bridge.</span></span>

![Иллюстрация работы модели автоматизации пользовательского интерфейса с инструментами и приложениями специальных возможностей](images/uiatomsaabridge.gif)

<span data-ttu-id="ef578-136">Аналогично, прокси-сервер автоматизации Microsoft Active Accessibility в пользовательском интерфейсе преобразует серверные объектные модели на основе Microsoft Active Accessibility для клиентов автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ef578-136">Similarly, the Microsoft Active Accessibility-to-UI Automation Proxy translates Microsoft Active Accessibility-based server object models for UI Automation clients.</span></span> <span data-ttu-id="ef578-137">На следующем рисунке показана роль прокси-сервера автоматизации Microsoft Active Accessibility в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="ef578-137">The following illustration shows the role of the Microsoft Active Accessibility-to-UI Automation Proxy.</span></span>

![Иллюстрация работы прокси-сервера автоматизации пользовательского интерфейса со специальными средствами и приложениями](images/msaatouiaproxy.gif)

## <a name="the-iaccessibleex-interface"></a><span data-ttu-id="ef578-139">Интерфейс IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="ef578-139">The IAccessibleEx Interface</span></span>

<span data-ttu-id="ef578-140">Интерфейс [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) позволяет существующим приложениям или БИБЛИОТЕКАМ пользовательского интерфейса расширить свою модель объектов Microsoft Active Accessibility для поддержки автоматизации пользовательского интерфейса без необходимости перезаписи реализации с нуля.</span><span class="sxs-lookup"><span data-stu-id="ef578-140">The [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface enables existing applications or UI libraries to extend their Microsoft Active Accessibility object model to support UI Automation without rewriting the implementation from scratch.</span></span> <span data-ttu-id="ef578-141">С помощью **IAccessibleEx** можно реализовать только дополнительные свойства автоматизации пользовательского интерфейса и шаблоны элементов управления, необходимые для полного описания пользовательского интерфейса и его функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="ef578-141">With **IAccessibleEx**, you can implement only the additional UI Automation properties and control patterns needed to fully describe the UI and its functionality.</span></span>

<span data-ttu-id="ef578-142">Поскольку прокси-сервер автоматизации Microsoft Active Accessibility в пользовательском интерфейсе преобразует объектные модели серверов Microsoft Active Accessibility с поддержкой [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)в качестве объектных моделей автоматизации пользовательского интерфейса, клиентам автоматизации пользовательского интерфейса не требуется выполнять никаких дополнительных действий.</span><span class="sxs-lookup"><span data-stu-id="ef578-142">Because the Microsoft Active Accessibility-to-UI Automation Proxy translates the object models of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)-enabled Microsoft Active Accessibility servers as UI Automation object models, UI Automation clients do not need to do any extra work.</span></span> <span data-ttu-id="ef578-143">Интерфейс **IAccessibleEx** также может включать внутрипроцессный клиент Microsoft Active Accessibility взаимодействовать непосредственно с поставщиками автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ef578-143">The **IAccessibleEx** interface can also enable in-process Microsoft Active Accessibility clients to interact directly with UI Automation providers.</span></span>

<span data-ttu-id="ef578-144">Дополнительные сведения см. в описании [интерфейса IAccessibleEx](iaccessibleex.md).</span><span class="sxs-lookup"><span data-stu-id="ef578-144">For more information, see [The IAccessibleEx Interface](iaccessibleex.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef578-145">См. также</span><span class="sxs-lookup"><span data-stu-id="ef578-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef578-146">Общие сведения об API автоматизации Windows</span><span class="sxs-lookup"><span data-stu-id="ef578-146">Windows Automation API Overview</span></span>](windows-automation-api-overview.md)
</dt> <dt>

[<span data-ttu-id="ef578-147">Интерфейс IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="ef578-147">The IAccessibleEx Interface</span></span>](iaccessibleex.md)
</dt> <dt>

[<span data-ttu-id="ef578-148">Вопросы безопасности для вспомогательных технологий</span><span class="sxs-lookup"><span data-stu-id="ef578-148">Security Considerations for Assistive Technologies</span></span>](uiauto-securityoverview.md)
</dt> </dl>

 

 




