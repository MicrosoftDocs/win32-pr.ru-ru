---
title: Microsoft Active Accessibility
description: Microsoft Active Accessibility — это технология на основе модели COM, которая улучшает способ работы специальных средств с приложениями, работающими в Microsoft Windows.
ms.assetid: f3e31c6f-c49e-4a61-99f1-b695ece2bfc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef277e54c34b64747811c4db40ecfb8fa1fb6bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792727"
---
# <a name="microsoft-active-accessibility"></a><span data-ttu-id="98ac1-103">Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="98ac1-103">Microsoft Active Accessibility</span></span>

## <a name="purpose"></a><span data-ttu-id="98ac1-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="98ac1-104">Purpose</span></span>

<span data-ttu-id="98ac1-105">Microsoft Active Accessibility — это технология на основе модели COM, которая улучшает способ работы специальных средств с приложениями, работающими в Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="98ac1-105">Microsoft Active Accessibility is a Component Object Model (COM)-based technology that improves the way accessibility aids work with applications running on Microsoft Windows.</span></span> <span data-ttu-id="98ac1-106">Он предоставляет библиотеки динамической компоновки, встроенные в операционную систему, а также COM-интерфейс и элементы API, которые предоставляют надежные методы для предоставления сведений об элементах пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="98ac1-106">It provides dynamic-link libraries that are incorporated into the operating system as well as a COM interface and API elements that provide reliable methods for exposing information about UI elements.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="98ac1-107">Где применимо</span><span class="sxs-lookup"><span data-stu-id="98ac1-107">Where applicable</span></span>

<span data-ttu-id="98ac1-108">Используя Active Accessibility Майкрософт и следующие рекомендации по проектированию, разработчики могут сделать приложения, работающие в среде Windows, более доступными для многих людей с зрением, слухом или нарушениями движения.</span><span class="sxs-lookup"><span data-stu-id="98ac1-108">By using Microsoft Active Accessibility and following accessible design practices, developers can make applications running on Windows more accessible to many people with vision, hearing, or motion disabilities.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="98ac1-109">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="98ac1-109">Developer audience</span></span>

<span data-ttu-id="98ac1-110">Microsoft Active Accessibility разработана в основном для разработчиков на C, C++ и Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="98ac1-110">Microsoft Active Accessibility is designed primarily for C, C++, and Microsoft Visual Basic developers.</span></span> <span data-ttu-id="98ac1-111">Как правило, разработчикам нужен умеренный уровень понимания COM-объектов и интерфейсов, а также о Юникоде.</span><span class="sxs-lookup"><span data-stu-id="98ac1-111">In general, developers need a moderate level of understanding about COM objects and interfaces as well as about Unicode.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="98ac1-112">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="98ac1-112">Run-time requirements</span></span>

<span data-ttu-id="98ac1-113">Полная поддержка Microsoft Active Accessibility встроена в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="98ac1-113">Full support for Microsoft Active Accessibility is built into Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="98ac1-114">Microsoft Active Accessibility также поддерживается в Windows NT 4,0 с пакетом обновления 6 (SP6) и более поздних версий и Windows 98.</span><span class="sxs-lookup"><span data-stu-id="98ac1-114">Microsoft Active Accessibility is also supported on Windows NT 4.0 with Service Pack 6 (SP6) and later, and Windows 98.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="98ac1-115">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="98ac1-115">In this section</span></span>



| <span data-ttu-id="98ac1-116">Раздел</span><span class="sxs-lookup"><span data-stu-id="98ac1-116">Topic</span></span>                                                             | <span data-ttu-id="98ac1-117">Описание</span><span class="sxs-lookup"><span data-stu-id="98ac1-117">Description</span></span>                                                                                                                                                                                 |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98ac1-118">Начало работы</span><span class="sxs-lookup"><span data-stu-id="98ac1-118">Getting Started</span></span>](getting-started.md)<br/>                 | <span data-ttu-id="98ac1-119">Общие сведения о компонентах Microsoft Active Accessibility и поддерживаемых платформах, а также кратком сравнении Microsoft Active Accessibility и Microsoft UI Automation.</span><span class="sxs-lookup"><span data-stu-id="98ac1-119">Introduction to the Microsoft Active Accessibility components and the supported platforms, and a brief comparison of Microsoft Active Accessibility and Microsoft UI Automation.</span></span><br/> |
| [<span data-ttu-id="98ac1-120">Технический обзор</span><span class="sxs-lookup"><span data-stu-id="98ac1-120">Technical Overview</span></span>](technical-overview.md)<br/>           | <span data-ttu-id="98ac1-121">Общие сведения о технологии Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="98ac1-121">General information about Microsoft Active Accessibility technology.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="98ac1-122">Рекомендации для разработчиков C/C++</span><span class="sxs-lookup"><span data-stu-id="98ac1-122">C/C++ Developer's Guide</span></span>](c-c---developer-s-guide.md)<br/> | <span data-ttu-id="98ac1-123">Сведения о том, как Microsoft Active Accessibility работает с точки зрения разработчика приложений C или C++.</span><span class="sxs-lookup"><span data-stu-id="98ac1-123">Information about how Microsoft Active Accessibility works from the perspective of a C or C++ application developer.</span></span> <span data-ttu-id="98ac1-124">В нем рассматриваются проблемы, характерные для разработчиков клиентов и серверов.</span><span class="sxs-lookup"><span data-stu-id="98ac1-124">It covers issues specific to client and server developers.</span></span><br/>  |
| [<span data-ttu-id="98ac1-125">Справочник по C/C++</span><span class="sxs-lookup"><span data-stu-id="98ac1-125">C/C++ Reference</span></span>](c-c---reference.md)<br/>                 | <span data-ttu-id="98ac1-126">Справочная документация по Microsoft Active Accessibility API для разработчиков C/C++.</span><span class="sxs-lookup"><span data-stu-id="98ac1-126">Reference documentation about the Microsoft Active Accessibility API for C/C++ developers.</span></span><br/>                                                                                       |
| [<span data-ttu-id="98ac1-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="98ac1-127">Samples</span></span>](samples.md)<br/>                                 | <span data-ttu-id="98ac1-128">Примеры программ, демонстрирующие использование Microsoft Active Accessibility API.</span><span class="sxs-lookup"><span data-stu-id="98ac1-128">Sample programs that demonstrate how to use the Microsoft Active Accessibility API.</span></span><br/>                                                                                              |
| [<span data-ttu-id="98ac1-129">Приложения</span><span class="sxs-lookup"><span data-stu-id="98ac1-129">Appendixes</span></span>](appendixes.md)<br/>                           | <span data-ttu-id="98ac1-130">Дополнительные справочные материалы для разработчиков клиентов и серверов Microsoft Active Accessibility и разработчиков Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="98ac1-130">Additional reference material for Microsoft Active Accessibility client and server developers and Visual Basic developers.</span></span><br/>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="98ac1-131">См. также</span><span class="sxs-lookup"><span data-stu-id="98ac1-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98ac1-132">веб-сайте Microsoft Accessibility.</span><span class="sxs-lookup"><span data-stu-id="98ac1-132">Microsoft Accessibility website</span></span>](https://www.microsoft.com/enable/)
</dt> <dt>

[<span data-ttu-id="98ac1-133">Центр разработчиков специальных возможностей Майкрософт на MSDN</span><span class="sxs-lookup"><span data-stu-id="98ac1-133">Microsoft Accessibility Developer Center on MSDN</span></span>](/windows/apps/accessibility)
</dt> </dl>

 

