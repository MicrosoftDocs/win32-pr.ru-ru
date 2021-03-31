---
title: Руководством программиста клиента автоматизации пользовательского интерфейса
description: В этом разделе содержатся сведения о создании приложений, использующих автоматизацию пользовательского интерфейса Майкрософт для взаимодействия с пользовательским интерфейсом других приложений и рабочего стола.
ms.assetid: d3616e1f-7b38-4a3e-ac96-72ec70cc13fc
keywords:
- Создание клиентских приложений модели автоматизации пользовательского интерфейса
- Создание клиентских приложений
- Клиенты, создание приложений автоматизации пользовательского интерфейса
- Клиенты, создание приложений модели автоматизации пользовательского интерфейса
- Модель автоматизации пользовательского интерфейса, создание клиентских приложений
- Автоматизация пользовательского интерфейса, создание клиентского приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f353243c8c194e2d732efd1d68bc2894ca930285
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791940"
---
# <a name="ui-automation-client-programmers-guide"></a><span data-ttu-id="5c16a-109">Руководством программиста клиента автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="5c16a-109">UI Automation Client Programmer's Guide</span></span>

<span data-ttu-id="5c16a-110">В этом разделе содержатся сведения о создании приложений, использующих автоматизацию пользовательского интерфейса Майкрософт для взаимодействия с пользовательским интерфейсом других приложений и рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="5c16a-110">This section contains information about creating applications that use Microsoft UI Automation to interact with the UI of other applications and the desktop.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5c16a-111">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="5c16a-111">In this section</span></span>

-   [<span data-ttu-id="5c16a-112">Общие сведения о клиентах автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="5c16a-112">UI Automation Clients Overview</span></span>](/windows/desktop/WinAuto/uiauto-clientsoverview)
-   [<span data-ttu-id="5c16a-113">Создание объекта Куиаутоматион</span><span class="sxs-lookup"><span data-stu-id="5c16a-113">Creating the CUIAutomation Object</span></span>](uiauto-creatingcuiautomation.md)
-   [<span data-ttu-id="5c16a-114">Получение элементов автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="5c16a-114">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
-   [<span data-ttu-id="5c16a-115">Получение свойств элементов модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="5c16a-115">Retrieving Properties from UI Automation Elements</span></span>](uiauto-propertiesforclients.md)
-   [<span data-ttu-id="5c16a-116">Кэширование свойств и шаблонов элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="5c16a-116">Caching UI Automation Properties and Control Patterns</span></span>](uiauto-cachingforclients.md)
-   [<span data-ttu-id="5c16a-117">Подписка на события модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="5c16a-117">Subscribing to UI Automation Events</span></span>](uiauto-eventsforclients.md)
-   [<span data-ttu-id="5c16a-118">Работа с элементами управления на основе текста</span><span class="sxs-lookup"><span data-stu-id="5c16a-118">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
-   [<span data-ttu-id="5c16a-119">Работа с виртуализированными элементами</span><span class="sxs-lookup"><span data-stu-id="5c16a-119">Working with Virtualized Items</span></span>](uiauto-workingwithvirtualizeditems.md)
-   [<span data-ttu-id="5c16a-120">Доступ к серверам Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="5c16a-120">Accessing Microsoft Active Accessibility Servers</span></span>](uiauto-accessingmsaaservers.md)
-   [<span data-ttu-id="5c16a-121">Использование Автоматизации Пользовательского Интерфейса для автоматизированного тестирования</span><span class="sxs-lookup"><span data-stu-id="5c16a-121">Using UI Automation for Automated Testing</span></span>](uiauto-usefortesting.md)
-   [<span data-ttu-id="5c16a-122">Основные сведения о проблемах масштабирования экрана</span><span class="sxs-lookup"><span data-stu-id="5c16a-122">Understanding Screen Scaling Issues</span></span>](uiauto-screenscaling.md)
-   [<span data-ttu-id="5c16a-123">Основные сведения о проблемах с потоками</span><span class="sxs-lookup"><span data-stu-id="5c16a-123">Understanding Threading Issues</span></span>](uiauto-threading.md)
-   [<span data-ttu-id="5c16a-124">Разделы руководства по клиентам автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="5c16a-124">How-To Topics for UI Automation Clients</span></span>](uiauto-howto-topics-for-uiautomation-clients.md)

## <a name="related-topics"></a><span data-ttu-id="5c16a-125">См. также</span><span class="sxs-lookup"><span data-stu-id="5c16a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c16a-126">Регистрация с простотой доступа</span><span class="sxs-lookup"><span data-stu-id="5c16a-126">Registering with Ease of Access</span></span>](/windows/desktop/WinAuto/ease-of-access---assistive-technology-registration)
</dt> <dt>

[<span data-ttu-id="5c16a-127">Вопросы безопасности для вспомогательных технологий</span><span class="sxs-lookup"><span data-stu-id="5c16a-127">Security Considerations for Assistive Technologies</span></span>](uiauto-securityoverview.md)
</dt> <dt>

[<span data-ttu-id="5c16a-128">Модель автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="5c16a-128">UI Automation</span></span>](entry-uiauto-win32.md)
</dt> </dl>

 

 