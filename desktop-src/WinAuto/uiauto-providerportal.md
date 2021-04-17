---
title: Рекомендации программиста поставщика модели автоматизации пользовательского интерфейса
description: В этом разделе содержатся сведения о создании поставщиков автоматизации пользовательского интерфейса Майкрософт.
ms.assetid: dd9996ec-f70f-4d5b-a029-ad4102b92a14
keywords:
- Модель автоматизации пользовательского интерфейса, создание поставщиков
- Автоматизация пользовательского интерфейса, создание поставщика
- создание поставщиков
- поставщики, создание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da09b5bcef605dd4979a15433c708e04e49534d
ms.sourcegitcommit: 305298a7727a428310fa138b45a933bcd7ef2532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/25/2020
ms.locfileid: "105691470"
---
# <a name="ui-automation-provider-programmers-guide"></a><span data-ttu-id="66cc0-107">Рекомендации программиста поставщика модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="66cc0-107">UI Automation Provider Programmer's Guide</span></span>

<span data-ttu-id="66cc0-108">В этом разделе содержатся сведения о создании поставщиков автоматизации пользовательского интерфейса Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="66cc0-108">This section contains information about creating Microsoft UI Automation providers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="66cc0-109">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="66cc0-109">In this section</span></span>

-   [<span data-ttu-id="66cc0-110">Общие сведения о поставщиках автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="66cc0-110">UI Automation Providers Overview</span></span>](uiauto-providersoverview.md)
-   [<span data-ttu-id="66cc0-111">Реализация поставщика автоматизации пользовательского интерфейса Server-Side</span><span class="sxs-lookup"><span data-stu-id="66cc0-111">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
-   [<span data-ttu-id="66cc0-112">Реализация поставщика автоматизации пользовательского интерфейса Client-Side (прокси)</span><span class="sxs-lookup"><span data-stu-id="66cc0-112">Implementing a Client-Side (Proxy) UI Automation Provider</span></span>](uiauto-clientsideprovider.md)
-   [<span data-ttu-id="66cc0-113">Добавление функций автоматизации пользовательского интерфейса на серверы Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="66cc0-113">Adding UI Automation Functionality to Active Accessibility Servers</span></span>](uiauto-usingiaccessibleex.md)
-   [<span data-ttu-id="66cc0-114">Реализация шаблонов элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="66cc0-114">Implementing UI Automation Control Patterns</span></span>](uiauto-implementinguiautocontrolpatterns.md)
-   [<span data-ttu-id="66cc0-115">Поддержка типов элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="66cc0-115">Supporting UI Automation Control Types</span></span>](uiauto-supportinguiautocontroltypes.md)
-   [<span data-ttu-id="66cc0-116">Разделы руководства для поставщиков автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="66cc0-116">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)

## <a name="related-topics"></a><span data-ttu-id="66cc0-117">См. также</span><span class="sxs-lookup"><span data-stu-id="66cc0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66cc0-118">Модель автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="66cc0-118">UI Automation</span></span>](entry-uiauto-win32.md)
</dt> <dt>

[<span data-ttu-id="66cc0-119">Пример простого поставщика модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="66cc0-119">UI Automation Simple Provider Sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/UI%20Automation%20simple%20provider%20sample)
</dt> <dt>

[<span data-ttu-id="66cc0-120">Пример поставщика основного окна модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="66cc0-120">UI Automation Core Window Provider Sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/UI%20Automation%20core%20window%20provider%20sample)
</dt> <dt>

[<span data-ttu-id="66cc0-121">Пример поставщика фрагментов модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="66cc0-121">UI Automation Fragment Provider Sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/UI%20Automation%20fragment%20provider%20sample)
</dt> <dt>

[<span data-ttu-id="66cc0-122">Пример поставщика содержимого документов модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="66cc0-122">UI Automation Document Content Provider Sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/UI%20Automation%20document%20content%20provider%20sample)
</dt> </dl>

 

 




