---
description: Интерфейс программирования Microsoft телефонии (TAPI) версии 2,2 (TAPI/C) позволяет реализовать коммуникационные приложения от основного элемента управления модемом до центров вызовов с несколькими агентами и коммутаторами.
ms.assetid: 02bfe923-9915-439e-ac7c-a570416d054a
title: Интерфейс программирования приложений телефонии, версия 2,2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e0dc158210350979105d765dc939f600f61d8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264809"
---
# <a name="telephony-application-programming-interface-version-22"></a><span data-ttu-id="c1324-103">Интерфейс программирования приложений телефонии, версия 2,2</span><span class="sxs-lookup"><span data-stu-id="c1324-103">Telephony Application Programming Interface Version 2.2</span></span>

## <a name="purpose"></a><span data-ttu-id="c1324-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="c1324-104">Purpose</span></span>

<span data-ttu-id="c1324-105">Интерфейс программирования Microsoft телефонии (TAPI) версии 2,2 (TAPI/C) позволяет реализовать коммуникационные приложения от основного элемента управления модемом до центров вызовов с несколькими агентами и коммутаторами.</span><span class="sxs-lookup"><span data-stu-id="c1324-105">The Microsoft Telephony Application Programming Interface (TAPI) version 2.2 (TAPI/C) enables implementation of communications applications ranging from basic modem control to call centers with multiple agents and switches.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="c1324-106">Где применимо</span><span class="sxs-lookup"><span data-stu-id="c1324-106">Where applicable</span></span>

<span data-ttu-id="c1324-107">Возможные приложения для TAPI 2,2 включают:</span><span class="sxs-lookup"><span data-stu-id="c1324-107">Possible TAPI 2.2 applications include:</span></span>

-   <span data-ttu-id="c1324-108">Базовые вызовы голосовой связи в коммутируемой телефонной сети (PSTN)</span><span class="sxs-lookup"><span data-stu-id="c1324-108">Basic voice calls on the Public Switched Telephone Network (PSTN)</span></span>
-   <span data-ttu-id="c1324-109">Приложения центра обработки вызовов для отслеживания нескольких агентов</span><span class="sxs-lookup"><span data-stu-id="c1324-109">Call center applications for tracking multiple agents</span></span>
-   <span data-ttu-id="c1324-110">Элемент управления модемом</span><span class="sxs-lookup"><span data-stu-id="c1324-110">Modem control</span></span>
-   <span data-ttu-id="c1324-111">Элемент управления УАТС</span><span class="sxs-lookup"><span data-stu-id="c1324-111">PBX control</span></span>
-   <span data-ttu-id="c1324-112">Системы интерактивного речевого ответа (IVR)</span><span class="sxs-lookup"><span data-stu-id="c1324-112">Interactive voice response (IVR) systems</span></span>
-   <span data-ttu-id="c1324-113">Голосовая почта</span><span class="sxs-lookup"><span data-stu-id="c1324-113">Voice mail</span></span>
-   <span data-ttu-id="c1324-114">Подробное управление телефонным устройством</span><span class="sxs-lookup"><span data-stu-id="c1324-114">Detailed phone device control</span></span>

## <a name="developer-audience"></a><span data-ttu-id="c1324-115">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="c1324-115">Developer audience</span></span>

<span data-ttu-id="c1324-116">TAPI/C предназначен для использования программистами C/C++.</span><span class="sxs-lookup"><span data-stu-id="c1324-116">TAPI/C is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="c1324-117">Опыт разработки с помощью телекоммуникаций или других приложений телефонии полезен, но не нужен.</span><span class="sxs-lookup"><span data-stu-id="c1324-117">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c1324-118">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="c1324-118">Run-time requirements</span></span>

<span data-ttu-id="c1324-119">TAPI версии 2,2 позволяет разрабатывать коммуникационные приложения для операционных систем Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98 и Windows 95.</span><span class="sxs-lookup"><span data-stu-id="c1324-119">TAPI version 2.2 enables development of communications applications for the Windows Server 2003 operating systems, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, and Windows 95.</span></span> <span data-ttu-id="c1324-120">Дополнительные сведения о том, какие операционные системы поддерживают определенную функцию, см. в разделе «требования» документации по этой функции.</span><span class="sxs-lookup"><span data-stu-id="c1324-120">For more information about which operating systems support a particular function, see the Requirements section of the documentation for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c1324-121">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="c1324-121">In this section</span></span>



| <span data-ttu-id="c1324-122">Раздел</span><span class="sxs-lookup"><span data-stu-id="c1324-122">Topic</span></span>                                          | <span data-ttu-id="c1324-123">Описание</span><span class="sxs-lookup"><span data-stu-id="c1324-123">Description</span></span>                                                                                                       |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1324-124">Обзор</span><span class="sxs-lookup"><span data-stu-id="c1324-124">Overview</span></span>](tapi-2-2-overview.md)<br/>   | <span data-ttu-id="c1324-125">Общие сведения об архитектуре и компонентах TAPI.</span><span class="sxs-lookup"><span data-stu-id="c1324-125">General information about TAPI architecture and components.</span></span><br/>                                            |
| [<span data-ttu-id="c1324-126">Ссылки</span><span class="sxs-lookup"><span data-stu-id="c1324-126">Reference</span></span>](tapi-2-2-reference.md)<br/> | <span data-ttu-id="c1324-127">Документация по функциям, структурам, сообщениям, константам и классам устройств, доступным в TAPI 2,2.</span><span class="sxs-lookup"><span data-stu-id="c1324-127">Documentation of functions, structures, messages, constants, and device classes available in TAPI 2.2.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="c1324-128">См. также</span><span class="sxs-lookup"><span data-stu-id="c1324-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1324-129">TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="c1324-129">TAPI 3.1</span></span>](./tapi-3-1-start-page.md)
</dt> <dt>

[<span data-ttu-id="c1324-130">Поставщики услуг TAPI</span><span class="sxs-lookup"><span data-stu-id="c1324-130">TAPI Service Providers</span></span>](./tapi-service-providers.md)
</dt> </dl>

 

