---
description: Internet Explorer 8 — строка агента пользователя
ms.assetid: 1cb0456d-501a-4272-b89d-35e79d29d13a
title: Internet Explorer 8 — строка агента пользователя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94d60930466b7243ad6ecc2b2d8d9c799e0e3da
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088242"
---
# <a name="internet-explorer-8---user-agent-string"></a><span data-ttu-id="e673e-103">Internet Explorer 8 — строка агента пользователя</span><span class="sxs-lookup"><span data-stu-id="e673e-103">Internet Explorer 8 - User Agent String</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="e673e-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="e673e-104">Affected Platforms</span></span>

 <span data-ttu-id="e673e-105">**Клиенты** — Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="e673e-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="e673e-106">**Серверы** — windows Server 2003, windows Server 2008, windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e673e-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="e673e-107">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="e673e-107">Feature Impact</span></span>

<span data-ttu-id="e673e-108">**Серьезность** — средний</span><span class="sxs-lookup"><span data-stu-id="e673e-108">**Severity** - Medium</span></span>  
<span data-ttu-id="e673e-109">**Частота** — высокая</span><span class="sxs-lookup"><span data-stu-id="e673e-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="e673e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e673e-110">Description</span></span>

<span data-ttu-id="e673e-111">Строка агента пользователя — это идентификатор Internet Explorer, предоставляющий данные о версии и других атрибутах для веб-серверов.</span><span class="sxs-lookup"><span data-stu-id="e673e-111">The User Agent String is the Internet Explorer identifier that provides data about its version and other attributes to web servers.</span></span> <span data-ttu-id="e673e-112">Многие веб-приложения основываются на строке агента пользователя IE и проникновения в ней.</span><span class="sxs-lookup"><span data-stu-id="e673e-112">Many web applications rely on, and piggyback on, the IE User Agent String.</span></span> <span data-ttu-id="e673e-113">Будут затронуты те, которые делают это и зависят от более раннего номера версии.</span><span class="sxs-lookup"><span data-stu-id="e673e-113">Those that do so and depend on an earlier version number will be impacted.</span></span> <span data-ttu-id="e673e-114">Строка агента пользователя теперь содержит строку "Trident/4.0", позволяющую различать строку агента пользователя Internet Explorer 7 и строку агента пользователя Internet Explorer 8 при запуске в режиме совместимости Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="e673e-114">The User Agent string now includes the string 'Trident/4.0' in order to allow differentiation between the Internet Explorer 7 User Agent String and the Internet Explorer 8 User Agent string when running in Internet Explorer 7 Compatibility View.</span></span> <span data-ttu-id="e673e-115">Дополнительные сведения см. в разделе Основные сведения о строках агента пользователя.</span><span class="sxs-lookup"><span data-stu-id="e673e-115">See Understanding User Agent Strings for details.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="e673e-116">Влияние на манифесты</span><span class="sxs-lookup"><span data-stu-id="e673e-116">Manifestation of Impact</span></span>

<span data-ttu-id="e673e-117">Есть две затронутые области:</span><span class="sxs-lookup"><span data-stu-id="e673e-117">There are two impacted areas:</span></span>

-   <span data-ttu-id="e673e-118">Веб-страницы, которые явно проверяют строку агента пользователя и не поддерживают строку агента пользователя Internet Explorer 8, могут работать неправильно.</span><span class="sxs-lookup"><span data-stu-id="e673e-118">Webpages that explicitly check the User Agent String and do not support the Internet Explorer 8 User Agent String may not run properly.</span></span> <span data-ttu-id="e673e-119">В большинстве случаев это означает, что страницы будут блокировать пользователей из содержимого, на которое они пытаются получить доступ, или отобразить неверное или неверное содержимое.</span><span class="sxs-lookup"><span data-stu-id="e673e-119">In the majority of cases, this means the pages will be block users from the content they are attempting to access or display incorrect or malformed content.</span></span>
-   <span data-ttu-id="e673e-120">Приложения, размещающие Trident (см. раздел размещение и повторное использование), по умолчанию будут использовать Internet Explorer 7 с помощью веб-дополнительного компонента, но не будут иметь доступа к функциям Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="e673e-120">Applications that host Trident (see Hosting and Reuse) will default to Internet Explorer 7 using the Web Optional Component, but will not have access to Internet Explorer 8 features.</span></span>

## <a name="solution"></a><span data-ttu-id="e673e-121">Решение</span><span class="sxs-lookup"><span data-stu-id="e673e-121">Solution</span></span>

<span data-ttu-id="e673e-122">Убедитесь, что ваши приложения должным образом обрабатывали новую версию "MSIE 8,0" в строке агента пользователя.</span><span class="sxs-lookup"><span data-stu-id="e673e-122">Ensure that your applications properly handle the new 'MSIE 8.0' version in the User Agent String.</span></span> <span data-ttu-id="e673e-123">Вы также можете выбрать представление совместимости Internet Explorer 7 для этих приложений на основе Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="e673e-123">You may also opt in to the Internet Explorer 7 Compatibility View for those applications based on Internet Explorer 7.</span></span> <span data-ttu-id="e673e-124">Это можно сделать с помощью meta tags.</span><span class="sxs-lookup"><span data-stu-id="e673e-124">This can be done with meta tags.</span></span> <span data-ttu-id="e673e-125">Дополнительные сведения см. в обсуждении о строках агента пользователя.</span><span class="sxs-lookup"><span data-stu-id="e673e-125">See the discussion in Understanding User Agent Strings for details.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="e673e-126">Совместимость, производительность, надежность и тестирование на удобство использования</span><span class="sxs-lookup"><span data-stu-id="e673e-126">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="e673e-127">Запустите приложения и веб-страницы в среде Internet Explorer 8 в Windows Vista или Windows XP, чтобы убедиться, что они ведут себя нужным образом.</span><span class="sxs-lookup"><span data-stu-id="e673e-127">Run your applications and webpages in an Internet Explorer 8 environment on Windows Vista or Windows XP to ensure that they behave in the desired manner.</span></span>
-   <span data-ttu-id="e673e-128">Кроме того, можно запустить средство тестирования совместимости Internet Explorer (ИЕКТТ), предоставляемое вместе с набором средств для обеспечения совместимости приложений (ACT), для выявления потенциальных проблем, связанных с обновлениями функций безопасности.</span><span class="sxs-lookup"><span data-stu-id="e673e-128">Alternatively, you can run the Internet Explorer Compatibility Test Tool (IECTT) provided with the Application Compatibility Toolkit (ACT) to locate any potential issues due to security feature updates.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="e673e-129">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="e673e-129">Links to Other Resources</span></span>

-   <span data-ttu-id="e673e-130">[Основные сведения о строках агента пользователя](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e673e-130">[Understanding User Agent Strings](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))</span></span>
-   [<span data-ttu-id="e673e-131">Строка User-Agent Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="e673e-131">Internet Explorer 8 User-Agent String</span></span>](/archive/blogs/ie/)
-   [<span data-ttu-id="e673e-132">Строка и вектор версии агента пользователя</span><span class="sxs-lookup"><span data-stu-id="e673e-132">User-Agent String and Version Vector</span></span>](https://archive.msdn.microsoft.com/ie8whitepapers)
-   <span data-ttu-id="e673e-133">[Размещение и повторное использование](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e673e-133">[Hosting and Reuse](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))</span></span>
-   [<span data-ttu-id="e673e-134">Загрузка набора средств для обеспечения совместимости приложений</span><span class="sxs-lookup"><span data-stu-id="e673e-134">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="e673e-135">[Известные проблемы с функциями безопасности в Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="e673e-135">[Known Internet Explorer Security Feature Issues](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span></span>

 

 
