---
title: Средство тестирования, готовое для платформы Майкрософт
description: Средство тестирования, готовое для платформы Майкрософт
ms.assetid: C41FBE70-E392-4FD0-954B-6C24168CB93E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6286e7ed64f013a8ea002ea392ba0d3bcac67296
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "103794196"
---
# <a name="microsoft-platform-ready-test-tool"></a><span data-ttu-id="94a69-103">Средство тестирования, готовое для платформы Майкрософт</span><span class="sxs-lookup"><span data-stu-id="94a69-103">Microsoft Platform Ready Test Tool</span></span>

## <a name="platform"></a><span data-ttu-id="94a69-104">Платформа</span><span class="sxs-lookup"><span data-stu-id="94a69-104">Platform</span></span>

 <span data-ttu-id="94a69-105">**Серверы** — windows Server 2012 \| Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="94a69-105">**Servers** – Windows Server 2012 \| Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="94a69-106">Описание</span><span class="sxs-lookup"><span data-stu-id="94a69-106">Description</span></span>

<span data-ttu-id="94a69-107">Средство тестирования готовности платформы Майкрософт (MPR) используется для обеспечения готовности приложений платформы и проверки соответствия требованиям сертификации для приложений Windows Server 2012 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="94a69-107">The Microsoft Platform Ready (MPR) Test Tool is used for platform application readiness and to validate compliance with certification requirements for Windows Server 2012 and Windows Server 2012 R2 applications.</span></span>

<span data-ttu-id="94a69-108">Корпорация Майкрософт настоятельно рекомендует включать средство тестирования многопротокольного управления в процессы сборки и тестирования программного обеспечения, обеспечивая готовность платформы до выпуска приложений на рынке.</span><span class="sxs-lookup"><span data-stu-id="94a69-108">Microsoft strongly encourages incorporating the MPR Test Tool into the software build and test processes, thereby ensuring platform readiness before applications are released to market.</span></span> <span data-ttu-id="94a69-109">Средство тестирования многопротокольного алгоритма также является рекомендуемым средством для тестирования бизнес-приложений и оценки серверных продуктов на совместимость с платформой перед принятием решений о приобретении.</span><span class="sxs-lookup"><span data-stu-id="94a69-109">The MPR Test Tool is also a recommended tool to test line of business applications and for evaluating server products for their platform compatibility before making purchasing decisions.</span></span>

## <a name="requirements"></a><span data-ttu-id="94a69-110">Требования</span><span class="sxs-lookup"><span data-stu-id="94a69-110">Requirements</span></span>

<span data-ttu-id="94a69-111">Средство тестирования многопротокольного управления включает автоматические тесты для:</span><span class="sxs-lookup"><span data-stu-id="94a69-111">The MPR Test Tool includes automated tests for:</span></span>

-   <span data-ttu-id="94a69-112">Установщик Windows</span><span class="sxs-lookup"><span data-stu-id="94a69-112">Windows Installer</span></span>
-   <span data-ttu-id="94a69-113">Установка и основная функциональность</span><span class="sxs-lookup"><span data-stu-id="94a69-113">Setup and Primary Functionality</span></span>
-   <span data-ttu-id="94a69-114">Драйверы и безопасность</span><span class="sxs-lookup"><span data-stu-id="94a69-114">Drivers and Security</span></span>
-   <span data-ttu-id="94a69-115">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="94a69-115">Best Practices</span></span>

<span data-ttu-id="94a69-116">Самостоятельное тестирование и отправка результатов для большинства серверных приложений займет не более 2 часов; более сложные приложения могут занять около 4 часов.</span><span class="sxs-lookup"><span data-stu-id="94a69-116">Self-testing and submission of results for most Server apps should take 2 hours or less; more complex apps can take around 4 hours.</span></span>

<span data-ttu-id="94a69-117">Все драйверы должны отдельно проходить тестирование сертификации оборудования Windows и быть подписаны корпорацией Майкрософт для Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="94a69-117">All drivers must separately pass Windows Hardware Certification testing and be signed by Microsoft for Windows Server 2012.</span></span>

## <a name="usage"></a><span data-ttu-id="94a69-118">Использование</span><span class="sxs-lookup"><span data-stu-id="94a69-118">Usage</span></span>

<span data-ttu-id="94a69-119">Чтобы протестировать приложения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="94a69-119">To test your apps:</span></span>

1.  <span data-ttu-id="94a69-120">Установите последнюю конфигурацию Windows Server 2012 (с полным ГРАФИЧЕСКИм интерфейсом сервера, минимального интерфейса сервера или Server Core) в соответствии с требованиями приложения.</span><span class="sxs-lookup"><span data-stu-id="94a69-120">Install the latest Windows Server 2012 minimum configuration (Full Server GUI, Minimal Server Interface, or Server Core) as required for your app.</span></span>
2.  <span data-ttu-id="94a69-121">Ознакомьтесь с требованиями к сертификации.</span><span class="sxs-lookup"><span data-stu-id="94a69-121">Review the certification requirements.</span></span>
3.  <span data-ttu-id="94a69-122">В чистой системе запустите средство тестирования многопротокольного режима в режиме полного пользовательского интерфейса или в режиме командной строки.</span><span class="sxs-lookup"><span data-stu-id="94a69-122">On a clean system, run the MPR Test Tool in either full UI mode or command line mode.</span></span>
4.  <span data-ttu-id="94a69-123">Завершите процесс самостоятельного тестирования.</span><span class="sxs-lookup"><span data-stu-id="94a69-123">Complete the self-guided testing process.</span></span>
5.  <span data-ttu-id="94a69-124">Проверьте результаты и при необходимости исправьте приложение.</span><span class="sxs-lookup"><span data-stu-id="94a69-124">Review results and fix your app as required.</span></span>
6.  <span data-ttu-id="94a69-125">Войдите в систему и отправьте результаты на портал готовности платформы Майкрософт для перечисления в каталоге Windows Server и использовании логотипа.</span><span class="sxs-lookup"><span data-stu-id="94a69-125">Sign-in and upload successful results to Microsoft Platform Ready portal for listing in Windows Server Catalog and usage of the logo.</span></span>

## <a name="resources"></a><span data-ttu-id="94a69-126">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="94a69-126">Resources</span></span>

-   [<span data-ttu-id="94a69-127">Требования к программе сертификации приложений Windows Server</span><span class="sxs-lookup"><span data-stu-id="94a69-127">Requirements for Windows Server App Certification Program</span></span>](../win_cert/certification-requirements-for-windows-desktop-apps.md)
-   [<span data-ttu-id="94a69-128">Средство тестирования, готовое для платформы Майкрософт (MPR)</span><span class="sxs-lookup"><span data-stu-id="94a69-128">Microsoft Platform Ready (MPR) Test Tool</span></span>](https://www.microsoft.com/download/details.aspx?id=37143)
-   [<span data-ttu-id="94a69-129">Программа сертификации приложений для Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="94a69-129">Windows Server 2012 Application Certification Program</span></span>](https://azure.microsoft.com/overview/commercial-marketplace/)
-   [<span data-ttu-id="94a69-130">Отзывы о логотипах Windows Server</span><span class="sxs-lookup"><span data-stu-id="94a69-130">Windows Server Logo Feedback</span></span>](mailto:WSLogoFB@microsoft.com)

 

 