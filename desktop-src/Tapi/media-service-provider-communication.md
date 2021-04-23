---
description: Начиная с поставщиков услуг телефонии Windows 2000, которые согласовывают версию 3,0 или более поздней версии, должен иметь соответствующий поставщик службы мультимедиа.
ms.assetid: 9235c631-77bc-42c6-8139-9208c9c254b4
title: Взаимодействие с поставщиком службы мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a50ec6a4fb96a86ceab3a302b138ee72d6c61b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351475"
---
# <a name="media-service-provider-communication"></a><span data-ttu-id="593ed-103">Взаимодействие с поставщиком службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="593ed-103">Media Service Provider Communication</span></span>

<span data-ttu-id="593ed-104">Начиная с поставщиков услуг телефонии Windows 2000, которые согласовывают версию 3,0 или более поздней версии, должен иметь соответствующий поставщик службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="593ed-104">Starting with Windows 2000 telephony service providers that negotiate a version of 3.0 or later must have a matching media service provider.</span></span> <span data-ttu-id="593ed-105">Точное деление эксплуатационных обязанностей зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="593ed-105">The precise division of operational responsibilities is implementation dependent.</span></span> <span data-ttu-id="593ed-106">Например, TSP может использовать соответствующий MSP для определения типа носителя во входящем сеансе.</span><span class="sxs-lookup"><span data-stu-id="593ed-106">For example, a TSP might use the matching MSP to perform media type determination on an incoming session.</span></span> <span data-ttu-id="593ed-107">Однако TSP должен соответствовать ТСПИ, что означает получение этого определения из MSP и составление отчетов на TAPI.</span><span class="sxs-lookup"><span data-stu-id="593ed-107">However, the TSP must conform to the TSPI, which means getting that determination from the MSP and reporting it to TAPI.</span></span>

<span data-ttu-id="593ed-108">ТСПИ предоставляет следующие функции и сообщения для разрешения виртуального подключения между TSP и MSP:</span><span class="sxs-lookup"><span data-stu-id="593ed-108">TSPI provides the following functions and messages to allow a virtual connection between a TSP and an MSP:</span></span>

-   [<span data-ttu-id="593ed-109">**ТСПИ \_ линеклосемспинстанце**</span><span class="sxs-lookup"><span data-stu-id="593ed-109">**TSPI\_lineCloseMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [<span data-ttu-id="593ed-110">**ТСПИ \_ линекреатемспинстанце**</span><span class="sxs-lookup"><span data-stu-id="593ed-110">**TSPI\_lineCreateMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [<span data-ttu-id="593ed-111">**ТСПИ \_ линемспидентифи**</span><span class="sxs-lookup"><span data-stu-id="593ed-111">**TSPI\_lineMSPIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [<span data-ttu-id="593ed-112">**ТСПИ \_ линерецеивемспдата**</span><span class="sxs-lookup"><span data-stu-id="593ed-112">**TSPI\_lineReceiveMSPData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [<span data-ttu-id="593ed-113">**Строка \_ косинфо**</span><span class="sxs-lookup"><span data-stu-id="593ed-113">**LINE\_QOSINFO**</span></span>](line-qosinfo.md)
-   [<span data-ttu-id="593ed-114">**Строка \_ сендмспдата**</span><span class="sxs-lookup"><span data-stu-id="593ed-114">**LINE\_SENDMSPDATA**</span></span>](line-sendmspdata.md)

 

 
