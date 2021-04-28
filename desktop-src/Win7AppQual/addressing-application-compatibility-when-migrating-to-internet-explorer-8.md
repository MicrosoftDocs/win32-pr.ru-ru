---
description: Устранение совместимости приложений при переходе на Internet Explorer 8
ms.assetid: 3F79CF5F-416D-4C06-AAAE-D935F36CD2E2
title: Устранение совместимости приложений при переходе на Internet Explorer 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24fb4b0cbfb946f2385ddbd13ddc697987e659d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088772"
---
# <a name="addressing-application-compatibility-when-migrating-to-internet-explorer-8"></a><span data-ttu-id="2769f-103">Устранение совместимости приложений при переходе на Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="2769f-103">Addressing Application Compatibility When Migrating to Internet Explorer 8</span></span>

<span data-ttu-id="2769f-104">В этом разделе приводятся общие сведения о тестировании проблем совместимости приложений и устранении этих проблем в веб-приложениях для Windows Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="2769f-104">This section provides an overview of testing for application compatibility issues and fixing those issues in web applications for Windows Internet Explorer 8.</span></span> <span data-ttu-id="2769f-105">В следующих разделах описываются изменения в Internet Explorer 8, а также средства и технологии для обеспечения совместимости приложения.</span><span class="sxs-lookup"><span data-stu-id="2769f-105">The following topics describe the changes in Internet Explorer 8 and the tools and technologies to ensure compatibility for your application.</span></span>



| <span data-ttu-id="2769f-106">Section</span><span class="sxs-lookup"><span data-stu-id="2769f-106">Section</span></span>                                                                                                                                              | <span data-ttu-id="2769f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="2769f-107">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2769f-108">Введение</span><span class="sxs-lookup"><span data-stu-id="2769f-108">Introduction</span></span>](introduction.md)                                                                                                                     | <span data-ttu-id="2769f-109">Содержит общие сведения о вопросах совместимости Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="2769f-109">Provides an overview of Internet Explorer 8 compatibility considerations.</span></span>                 |
| [<span data-ttu-id="2769f-110">Основные сведения о вызове совместимости приложений</span><span class="sxs-lookup"><span data-stu-id="2769f-110">Understanding the Application Compatibility Challenge</span></span>](understanding-the-application-compatibility-challenge.md)                                   | <span data-ttu-id="2769f-111">Общие сведения о совместимости Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="2769f-111">Provides background about Internet Explorer 8 compatibility.</span></span>                              |
| [<span data-ttu-id="2769f-112">Веб-стандарты и совместимость приложений</span><span class="sxs-lookup"><span data-stu-id="2769f-112">Web Standards and Application Compatibility</span></span>](web-standards-and-application-compatibility.md)                                                       | <span data-ttu-id="2769f-113">Содержит фундаментальные сведения о том, почему веб-стандарты важны.</span><span class="sxs-lookup"><span data-stu-id="2769f-113">Provides background about why web standards are important.</span></span>                                |
| [<span data-ttu-id="2769f-114">Разработка обновлений, влияющих на совместимость браузеров</span><span class="sxs-lookup"><span data-stu-id="2769f-114">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)                           | <span data-ttu-id="2769f-115">Содержит тематическую информацию об обновлениях проекта, влияющих на совместимость.</span><span class="sxs-lookup"><span data-stu-id="2769f-115">Provides topical information about design updates that impact compatibility.</span></span>              |
| [<span data-ttu-id="2769f-116">Устранение проблем совместимости в веб-приложениях и надстройках</span><span class="sxs-lookup"><span data-stu-id="2769f-116">Fixing Compatibility Issues in Web Applications and Add-Ons</span></span>](remediating-web-applications-and-add-ons.md)                                          | <span data-ttu-id="2769f-117">Предлагает предложения по устранению проблем совместимости с веб-приложениями и надстройками.</span><span class="sxs-lookup"><span data-stu-id="2769f-117">Offers suggestions for addressing compatibility issues with web applications and add-ons.</span></span> |
| [<span data-ttu-id="2769f-118">Средства для отладки веб-приложений и дополнительных компонентов</span><span class="sxs-lookup"><span data-stu-id="2769f-118">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)                                             | <span data-ttu-id="2769f-119">Содержит список средств, доступных для отладки веб-приложений и дополнительных компонентов.</span><span class="sxs-lookup"><span data-stu-id="2769f-119">Lists tools that are available for debugging web applications and add-ons.</span></span>                |
| [<span data-ttu-id="2769f-120">Приложение 1. изменения браузера Internet Explorer 6 для Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="2769f-120">Appendix 1: Internet Explorer 6 to Internet Explorer 8 browser changes</span></span>](appendix-1--internet-explorer-6-to-internet-explorer-8-browser-changes.md) | <span data-ttu-id="2769f-121">Перечисление изменений из Microsoft Internet Explorer 6 в Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="2769f-121">Lists changes from Microsoft Internet Explorer 6 to Internet Explorer 8.</span></span>                  |
| [<span data-ttu-id="2769f-122">Приложение 2. сценарии тестовых сценариев</span><span class="sxs-lookup"><span data-stu-id="2769f-122">Appendix 2: Test Script Scenarios</span></span>](appendix-2--test-script-scenarios.md)                                                                           | <span data-ttu-id="2769f-123">Список рекомендуемых сценариев для проверки совместимости сайтов.</span><span class="sxs-lookup"><span data-stu-id="2769f-123">Lists recommended scenarios for testing sites for compatibility.</span></span>                          |



 

 

 



