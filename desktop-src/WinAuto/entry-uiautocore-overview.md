---
title: Основы модели автоматизации пользовательского интерфейса
description: В этом разделе объясняются фундаментальные понятия, на основе которых основана модель автоматизации пользовательского интерфейса.
ms.assetid: 109f113f-9ed0-4a57-b3af-90e831e53c42
keywords:
- Модель автоматизации пользовательского интерфейса, Microsoft Win32 API
- Модель автоматизации пользовательского интерфейса, API Win32
- Автоматизация пользовательского интерфейса, поставщики
- Модель автоматизации пользовательского интерфейса, клиентские приложения
- Клиенты, Microsoft UI Automation для Microsoft Win32 API
- Клиенты, модель автоматизации пользовательского интерфейса для Microsoft Win32 API
- API Win32
- Microsoft Win32 API
- Модель автоматизации пользовательского интерфейса для Microsoft Win32 API
- Microsoft UI Automation для Microsoft Win32 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba8147a8dd7f8d03340fad43465c225a174e606
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411166"
---
# <a name="ui-automation-fundamentals"></a><span data-ttu-id="a4cf7-113">Основы модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a4cf7-113">UI Automation Fundamentals</span></span>

<span data-ttu-id="a4cf7-114">Служба автоматизации пользовательского интерфейса Майкрософт предоставляет вспомогательные технологические приложения и автоматизированные средства тестирования для взаимодействия с элементами управления пользовательского интерфейса других приложений.</span><span class="sxs-lookup"><span data-stu-id="a4cf7-114">Microsoft UI Automation enables assistive technology applications and automated testing tools to interact with the UI controls of other applications.</span></span> <span data-ttu-id="a4cf7-115">В этом разделе объясняются фундаментальные понятия, на основе которых основана модель автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a4cf7-115">This section explains the fundamental concepts that UI Automation is based on.</span></span>

<span data-ttu-id="a4cf7-116">API автоматизации пользовательского интерфейса состоит из двух частей.</span><span class="sxs-lookup"><span data-stu-id="a4cf7-116">The UI Automation API is in two parts.</span></span> <span data-ttu-id="a4cf7-117">Одна часть используется приложениями *поставщика автоматизации пользовательского интерфейса* , а другая — *клиентскими приложениями модели автоматизации пользовательского интерфейса* .</span><span class="sxs-lookup"><span data-stu-id="a4cf7-117">One part is used by *UI Automation provider* applications, and the other is used by *UI Automation client* applications.</span></span> <span data-ttu-id="a4cf7-118">API поставщика позволяет разработчикам пользовательского элемента управления Microsoft Win32 и других платформ управления предоставлять эти элементы управления модели автоматизации пользовательского интерфейса и сделать их видимыми для клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="a4cf7-118">The provider API enables developers of Microsoft Win32 custom control and other control frameworks to expose those controls to UI Automation and make them visible to client applications.</span></span> <span data-ttu-id="a4cf7-119">Клиентский API позволяет приложениям взаимодействовать с элементами управления в других приложениях и получать сведения о них.</span><span class="sxs-lookup"><span data-stu-id="a4cf7-119">The client API enables applications to interact with controls in other applications and retrieve information about them.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a4cf7-120">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="a4cf7-120">In this section</span></span>

-   [<span data-ttu-id="a4cf7-121">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a4cf7-121">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
-   [<span data-ttu-id="a4cf7-122">Модель автоматизации пользовательского интерфейса и Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="a4cf7-122">UI Automation and Active Accessibility</span></span>](uiauto-msaa.md)
-   [<span data-ttu-id="a4cf7-123">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a4cf7-123">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
-   [<span data-ttu-id="a4cf7-124">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a4cf7-124">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
-   [<span data-ttu-id="a4cf7-125">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a4cf7-125">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
-   [<span data-ttu-id="a4cf7-126">Общие сведения о свойствах автоматизированного пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a4cf7-126">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
-   [<span data-ttu-id="a4cf7-127">Обзор событий автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a4cf7-127">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
-   [<span data-ttu-id="a4cf7-128">Пользовательские свойства, события и шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="a4cf7-128">Custom Properties, Events, and Control Patterns</span></span>](uiauto-custompropertieseventscontrolpatterns.md)
-   [<span data-ttu-id="a4cf7-129">Поддержка модели автоматизации пользовательского интерфейса для текстового содержимого</span><span class="sxs-lookup"><span data-stu-id="a4cf7-129">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
-   [<span data-ttu-id="a4cf7-130">Поддержка модели автоматизации пользовательского интерфейса для перетаскивания</span><span class="sxs-lookup"><span data-stu-id="a4cf7-130">UI Automation Support for Drag-and-Drop</span></span>](ui-automation-support-for-drag-and-drop.md)
-   [<span data-ttu-id="a4cf7-131">Вопросы безопасности для вспомогательных технологий</span><span class="sxs-lookup"><span data-stu-id="a4cf7-131">Security Considerations for Assistive Technologies</span></span>](uiauto-securityoverview.md)
-   [<span data-ttu-id="a4cf7-132">Рекомендации по использованию безнадежных массивов</span><span class="sxs-lookup"><span data-stu-id="a4cf7-132">Best Practices for Using Safe Arrays</span></span>](uiauto-workingwithsafearrays.md)
-   [<span data-ttu-id="a4cf7-133">Спецификация модели автоматизации пользовательского интерфейса и обязательство сообщества</span><span class="sxs-lookup"><span data-stu-id="a4cf7-133">UI Automation Specification and Community Promise</span></span>](uiauto-specandcommunitypromise.md)

## <a name="related-topics"></a><span data-ttu-id="a4cf7-134">См. также</span><span class="sxs-lookup"><span data-stu-id="a4cf7-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4cf7-135">Модель автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a4cf7-135">UI Automation</span></span>](entry-uiauto-win32.md)
</dt> </dl>

 

 




