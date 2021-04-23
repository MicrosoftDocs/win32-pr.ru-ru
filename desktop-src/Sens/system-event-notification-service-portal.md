---
description: Отслеживайте уведомления о системных событиях от программ, выполняемых на мобильных компьютерах, чтобы определить пропускную способность и задержку сетевого подключения. Создавайте оптимизированные приложения для мобильных вычислений и сетей с высокой задержкой.
ms.assetid: a27386c5-1ab3-448a-88d9-8c9a18599e59
title: Служба уведомления о системных событиях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3238441f82c26a33370c37fe09b3e4007639f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999207"
---
# <a name="system-event-notification-service"></a><span data-ttu-id="f5e7b-104">Служба уведомления о системных событиях</span><span class="sxs-lookup"><span data-stu-id="f5e7b-104">System Event Notification Service</span></span>

## <a name="purpose"></a><span data-ttu-id="f5e7b-105">Назначение</span><span class="sxs-lookup"><span data-stu-id="f5e7b-105">Purpose</span></span>

<span data-ttu-id="f5e7b-106">Приложениям, предназначенным для использования мобильными пользователями, требуется уникальный набор функций подключения и уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f5e7b-106">Applications designed for use by mobile users require a unique set of connectivity functions and notifications.</span></span> <span data-ttu-id="f5e7b-107">В прошлом эти отдельные приложения требовались для внутренней реализации этих функций.</span><span class="sxs-lookup"><span data-stu-id="f5e7b-107">In the past these individual applications were required to implement these features internally.</span></span> <span data-ttu-id="f5e7b-108">Служба уведомлений о системных событиях (Сенс) теперь предоставляет эти возможности в операционной системе, создавая единый интерфейс подключения и уведомления для приложений.</span><span class="sxs-lookup"><span data-stu-id="f5e7b-108">The System Event Notification Service (SENS) now provides these capabilities in the operating system, creating a uniform connectivity and notification interface for applications.</span></span> <span data-ttu-id="f5e7b-109">С помощью СЕНСных разработчиков можно определить пропускную способность и сведения о задержке подключения из приложения и оптимизировать работу приложения на основе этих условий.</span><span class="sxs-lookup"><span data-stu-id="f5e7b-109">Using SENS developers can determine connection bandwidth and latency information from within their application and optimize the application's operation based on those conditions.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="f5e7b-110">Где применимо</span><span class="sxs-lookup"><span data-stu-id="f5e7b-110">Where applicable</span></span>

<span data-ttu-id="f5e7b-111">Функции подключения и уведомления Сенс полезны для приложений, написанных для мобильных компьютеров или компьютеров, подключенных к локальным сетям с высокой задержкой.</span><span class="sxs-lookup"><span data-stu-id="f5e7b-111">The connectivity functions and notifications of SENS are useful for applications written for mobile computers or computers connected to high latency local area networks.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="f5e7b-112">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="f5e7b-112">Developer audience</span></span>

<span data-ttu-id="f5e7b-113">Этот документ предназначен для разработчиков программного обеспечения, разрабатывающих приложения для мобильных вычислений и локальных сетей с высокой задержкой.</span><span class="sxs-lookup"><span data-stu-id="f5e7b-113">This document is intended for software developers who develop applications for mobile computing and high latency local area networks.</span></span> <span data-ttu-id="f5e7b-114">Этот документ содержит полный справочник по всем частям службы уведомлений о системных событиях, включая объект Сенс и вспомогательные методы.</span><span class="sxs-lookup"><span data-stu-id="f5e7b-114">This document provides a complete reference of all parts of the System Event Notification Service including the SENS object and supporting methods.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="f5e7b-115">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="f5e7b-115">Run-time requirements</span></span>

<span data-ttu-id="f5e7b-116">Требуется Microsoft Windows XP или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="f5e7b-116">Requires Microsoft Windows XP or later.</span></span> <span data-ttu-id="f5e7b-117">Сведения о том, какие операционные системы требуются для использования определенного интерфейса или функции, см. в разделе "требования" документации.</span><span class="sxs-lookup"><span data-stu-id="f5e7b-117">For information about which operating systems are required to use a particular interface or function, see the Requirements section of the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f5e7b-118">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="f5e7b-118">In this section</span></span>



| <span data-ttu-id="f5e7b-119">Раздел</span><span class="sxs-lookup"><span data-stu-id="f5e7b-119">Topic</span></span>                                                              | <span data-ttu-id="f5e7b-120">Описание</span><span class="sxs-lookup"><span data-stu-id="f5e7b-120">Description</span></span>                                                                           |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5e7b-121">Обзор</span><span class="sxs-lookup"><span data-stu-id="f5e7b-121">Overview</span></span>](about-system-event-notification-service.md)<br/> | <span data-ttu-id="f5e7b-122">Общие сведения о службе уведомлений о системных событиях.</span><span class="sxs-lookup"><span data-stu-id="f5e7b-122">General information about System Event Notification Service.</span></span><br/>               |
| [<span data-ttu-id="f5e7b-123">Ссылки</span><span class="sxs-lookup"><span data-stu-id="f5e7b-123">Reference</span></span>](sens-reference.md)<br/>                         | <span data-ttu-id="f5e7b-124">Документация по методам и интерфейсам службы уведомлений о системных событиях.</span><span class="sxs-lookup"><span data-stu-id="f5e7b-124">Documentation of System Event Notification Service methods and interfaces.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="f5e7b-125">См. также</span><span class="sxs-lookup"><span data-stu-id="f5e7b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5e7b-126">**иевентсубскриптион**</span><span class="sxs-lookup"><span data-stu-id="f5e7b-126">**IEventSubscription**</span></span>](/windows/win32/api/eventsys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 
