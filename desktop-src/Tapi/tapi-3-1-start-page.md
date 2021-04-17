---
description: Интерфейс программирования Microsoft телефонии (TAPI) 3,1 — это интерфейс API на основе модели COM, который выполняет слияние классической и IP-телефонии.
ms.assetid: 79c4d2c9-953e-4e68-98b7-6a0dd9a04e0b
title: Интерфейс программирования приложений телефонии, версия 3,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d302f6ffe67094d436caf94cc8cf109e1e3c9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674108"
---
# <a name="telephony-application-programming-interface-version-31"></a><span data-ttu-id="c84c9-103">Интерфейс программирования приложений телефонии, версия 3,1</span><span class="sxs-lookup"><span data-stu-id="c84c9-103">Telephony Application Programming Interface Version 3.1</span></span>

## <a name="purpose"></a><span data-ttu-id="c84c9-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="c84c9-104">Purpose</span></span>

<span data-ttu-id="c84c9-105">Интерфейс программирования Microsoft телефонии (TAPI) 3,1 — это интерфейс API на основе модели COM, который выполняет слияние классической и IP-телефонии.</span><span class="sxs-lookup"><span data-stu-id="c84c9-105">The Microsoft Telephony Application Programming Interface (TAPI) version 3.1 is a Component Object Model (COM)-based API that merges classic and IP telephony.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="c84c9-106">Где применимо</span><span class="sxs-lookup"><span data-stu-id="c84c9-106">Where applicable</span></span>

<span data-ttu-id="c84c9-107">Возможные приложения TAPI включают:</span><span class="sxs-lookup"><span data-stu-id="c84c9-107">Possible TAPI applications include:</span></span>

-   <span data-ttu-id="c84c9-108">Многоадресные IP-конференции мультимедиа с качеством обслуживания (QOS)</span><span class="sxs-lookup"><span data-stu-id="c84c9-108">Multicast multimedia IP conferencing with quality of service (QOS)</span></span>
-   <span data-ttu-id="c84c9-109">Голосовой вызов через Интернет с помощью протокола H. 323</span><span class="sxs-lookup"><span data-stu-id="c84c9-109">Voice calls over the Internet using the H.323 protocol</span></span>
-   <span data-ttu-id="c84c9-110">Приложения центра обработки вызовов, способные отслеживать несколько агентов</span><span class="sxs-lookup"><span data-stu-id="c84c9-110">Call center applications capable of tracking multiple agents</span></span>
-   <span data-ttu-id="c84c9-111">Базовые вызовы голосовой связи в коммутируемой телефонной сети (PSTN)</span><span class="sxs-lookup"><span data-stu-id="c84c9-111">Basic voice calls on the Public Switched Telephone Network (PSTN)</span></span>
-   <span data-ttu-id="c84c9-112">Элемент управления УАТС</span><span class="sxs-lookup"><span data-stu-id="c84c9-112">PBX control</span></span>
-   <span data-ttu-id="c84c9-113">Системы интерактивного речевого ответа (IVR)</span><span class="sxs-lookup"><span data-stu-id="c84c9-113">Interactive voice response (IVR) systems</span></span>
-   <span data-ttu-id="c84c9-114">Голосовая почта</span><span class="sxs-lookup"><span data-stu-id="c84c9-114">Voice mail</span></span>

## <a name="developer-audience"></a><span data-ttu-id="c84c9-115">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="c84c9-115">Developer audience</span></span>

<span data-ttu-id="c84c9-116">Приложения с поддержкой TAPI можно писать на многих языках, включая Java, Visual Basic и C/C++.</span><span class="sxs-lookup"><span data-stu-id="c84c9-116">You can write TAPI-enabled applications in many languages, including Java, Visual Basic, and C/C++.</span></span> <span data-ttu-id="c84c9-117">Требуется знание COM.</span><span class="sxs-lookup"><span data-stu-id="c84c9-117">Familiarity with COM is required.</span></span> <span data-ttu-id="c84c9-118">Опыт разработки с помощью телекоммуникаций или других приложений телефонии полезен, но не нужен.</span><span class="sxs-lookup"><span data-stu-id="c84c9-118">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c84c9-119">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="c84c9-119">Run-time requirements</span></span>

<span data-ttu-id="c84c9-120">TAPI версии 3,1 позволяет разрабатывать коммуникационные приложения для операционных систем Windows Server 2003, Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c84c9-120">TAPI version 3.1 enables development of communications applications for Windows Server 2003 operating systems, Windows XP, and Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c84c9-121">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="c84c9-121">In this section</span></span>



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="c84c9-122">Раздел</span><span class="sxs-lookup"><span data-stu-id="c84c9-122">Topic</span></span></th><th><span data-ttu-id="c84c9-123">Описание</span><span class="sxs-lookup"><span data-stu-id="c84c9-123">Description</span></span></th></tr></thead><tbody><tr class="odd"><td><span data-ttu-id="c84c9-124"><a href="tapi-3-1-overview.md">Обзор</a></span><span class="sxs-lookup"><span data-stu-id="c84c9-124"><a href="tapi-3-1-overview.md">Overview</a></span></span><br/></td><td><span data-ttu-id="c84c9-125">Общие сведения об архитектуре и компонентах TAPI.</span><span class="sxs-lookup"><span data-stu-id="c84c9-125">General information about TAPI architecture and components.</span></span><br/></td></tr><tr class="even"><td><span data-ttu-id="c84c9-126">Справочник</span><span class="sxs-lookup"><span data-stu-id="c84c9-126">Reference</span></span><br/></td><td><span data-ttu-id="c84c9-127">Документация по:</span><span class="sxs-lookup"><span data-stu-id="c84c9-127">Documentation for:</span></span><br/><ul><li><span data-ttu-id="c84c9-128"><a href="call-and-media-controls-reference.md">Справочник по вызовам и элементам управления мультимедиа</a></span><span class="sxs-lookup"><span data-stu-id="c84c9-128"><a href="call-and-media-controls-reference.md">Call and Media Controls Reference</a></span></span></li><li><span data-ttu-id="c84c9-129"><a href="call-center-controls-reference.md">Справочник по элементам управления центра обработки вызовов</a></span><span class="sxs-lookup"><span data-stu-id="c84c9-129"><a href="call-center-controls-reference.md">Call Center Controls Reference</a></span></span></li><li><span data-ttu-id="c84c9-130"><a href="rendezvous-ip-telephony-conferencing-reference.md">Встречная ссылка</a></span><span class="sxs-lookup"><span data-stu-id="c84c9-130"><a href="rendezvous-ip-telephony-conferencing-reference.md">Rendezvous Reference</a></span></span></li></ul></td></tr></tbody></table>



 

## <a name="related-topics"></a><span data-ttu-id="c84c9-131">См. также</span><span class="sxs-lookup"><span data-stu-id="c84c9-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c84c9-132">Обзор телефонии Майкрософт</span><span class="sxs-lookup"><span data-stu-id="c84c9-132">Microsoft Telephony Overview</span></span>](microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="c84c9-133">TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="c84c9-133">TAPI 2.2</span></span>](./tapi-2-2-start-page.md)
</dt> <dt>

[<span data-ttu-id="c84c9-134">Поставщики услуг TAPI</span><span class="sxs-lookup"><span data-stu-id="c84c9-134">TAPI Service Providers</span></span>](./tapi-service-providers.md)
</dt> </dl>

 

