---
description: Поставщик службы мультимедиа (MSP) позволяет приложению управлять носителями для конкретного транспортного механизма.
ms.assetid: f886380f-d970-4511-bf71-fb1eb767e4f4
title: Поставщики служб мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd78f5ff4a13da4365f99bd2cb539738b6f3fd6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684756"
---
# <a name="media-service-providers"></a><span data-ttu-id="50289-103">Поставщики служб мультимедиа</span><span class="sxs-lookup"><span data-stu-id="50289-103">Media Service Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="50289-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="50289-104">Purpose</span></span>

<span data-ttu-id="50289-105">Поставщик службы мультимедиа (MSP) позволяет приложению управлять носителями для конкретного транспортного механизма.</span><span class="sxs-lookup"><span data-stu-id="50289-105">A media service provider (MSP) enables an application to control media for a particular transport mechanism.</span></span> <span data-ttu-id="50289-106">MSP всегда сопряжен с поставщиком услуг телефонии (TSP).</span><span class="sxs-lookup"><span data-stu-id="50289-106">An MSP is always paired with a Telephony Service Provider (TSP).</span></span>

<span data-ttu-id="50289-107">Интерфейс поставщика службы мультимедиа (МСПИ) — это набор интерфейсов и методов, реализованных MSP, чтобы обеспечить управление приложениями через транспорт носителей во время сеанса связи.</span><span class="sxs-lookup"><span data-stu-id="50289-107">The Media Service Provider Interface (MSPI) is a set of interfaces and methods implemented by an MSP to allow an application control over media transport during a communications session.</span></span> <span data-ttu-id="50289-108">MSP обрабатывает механизмы для конкретных устройств и протоколов, необходимые для внедрения этих элементов управления, и взаимодействует со связанным TSP или приложением с помощью методов, предоставляемых в МСПИ.</span><span class="sxs-lookup"><span data-stu-id="50289-108">An MSP handles the device-specific and protocol-specific mechanisms required to enact these controls, and communicates with its paired TSP or an application through use of the methods provided in the MSPI.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="50289-109">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="50289-109">Developer audience</span></span>

<span data-ttu-id="50289-110">Требуется знание COM.</span><span class="sxs-lookup"><span data-stu-id="50289-110">Familiarity with COM is required.</span></span> <span data-ttu-id="50289-111">Опыт разработки с помощью телекоммуникаций или других приложений телефонии полезен, но не нужен.</span><span class="sxs-lookup"><span data-stu-id="50289-111">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="50289-112">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="50289-112">Run-time requirements</span></span>

<span data-ttu-id="50289-113">МСПИ позволяет разрабатывать поставщики служб мультимедиа для определенных протоколов или устройств, работающих в операционных системах Windows Server 2003, Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="50289-113">MSPI enables development of media service providers for particular protocols or devices running on Windows Server 2003 operating systems, Windows XP, and Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="50289-114">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="50289-114">In this section</span></span>



| <span data-ttu-id="50289-115">Раздел</span><span class="sxs-lookup"><span data-stu-id="50289-115">Topic</span></span>                                                                       | <span data-ttu-id="50289-116">Описание</span><span class="sxs-lookup"><span data-stu-id="50289-116">Description</span></span>                                                           |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="50289-117">Обзор</span><span class="sxs-lookup"><span data-stu-id="50289-117">Overview</span></span>](about-the-media-service-provider-msp-.md)<br/>            | <span data-ttu-id="50289-118">Общие сведения об архитектуре и компонентах MSP.</span><span class="sxs-lookup"><span data-stu-id="50289-118">General information about MSP architecture and components.</span></span><br/> |
| [<span data-ttu-id="50289-119">Ссылки</span><span class="sxs-lookup"><span data-stu-id="50289-119">Reference</span></span>](media-service-provider-interface-mspi-reference.md)<br/> | <span data-ttu-id="50289-120">Документация по интерфейсам МСПИ.</span><span class="sxs-lookup"><span data-stu-id="50289-120">Documentation for the MSPI interfaces.</span></span><br/>                     |



 

## <a name="related-topics"></a><span data-ttu-id="50289-121">См. также</span><span class="sxs-lookup"><span data-stu-id="50289-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50289-122">Обзор телефонии Майкрософт</span><span class="sxs-lookup"><span data-stu-id="50289-122">Microsoft Telephony Overview</span></span>](microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="50289-123">TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="50289-123">TAPI 3.1</span></span>](tapi-3-1-start-page.md)
</dt> <dt>

[<span data-ttu-id="50289-124">Поставщики услуг телефонии</span><span class="sxs-lookup"><span data-stu-id="50289-124">Telephony Service Providers</span></span>](./telephony-service-providers-start-page.md)
</dt> </dl>

 

