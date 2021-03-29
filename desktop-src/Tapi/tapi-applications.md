---
description: В следующем материале приводятся рекомендации по использованию TAPI для написания приложений для обмена данными с конечным пользователем или сервером. Эти сведения также очень важны для программистов поставщиков услуг.
ms.assetid: fb97aff7-910e-451f-b183-36324a459423
title: Приложения TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6836f33af120171016b080693ae7a8315f9b9d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674263"
---
# <a name="tapi-applications"></a><span data-ttu-id="e61ed-104">Приложения TAPI</span><span class="sxs-lookup"><span data-stu-id="e61ed-104">TAPI Applications</span></span>

<span data-ttu-id="e61ed-105">В следующем материале приводятся рекомендации по использованию TAPI для написания приложений для обмена данными с конечным пользователем или сервером.</span><span class="sxs-lookup"><span data-stu-id="e61ed-105">The following material provides guidelines on using TAPI to write end-user or server communications applications.</span></span> <span data-ttu-id="e61ed-106">Эти сведения также очень важны для программистов поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="e61ed-106">This information is also highly relevant to service provider programmers.</span></span>

<span data-ttu-id="e61ed-107">Первым решением, которое программисту нужно сделать с помощью TAPI, является требуемый уровень обслуживания.</span><span class="sxs-lookup"><span data-stu-id="e61ed-107">The first decision a programmer needs to make in using TAPI is the level of service required.</span></span> <span data-ttu-id="e61ed-108">Например, если приложению требуется выбрать пункт меню, который может набрать номер телефона, то, скорее всего, не потребуется полноценное приложение TAPI.</span><span class="sxs-lookup"><span data-stu-id="e61ed-108">For example, if an application requires a menu selection that can dial a phone number, a full TAPI application is probably not required.</span></span> <span data-ttu-id="e61ed-109">Служба поддержки телефонии может быстро и просто включить этот параметр.</span><span class="sxs-lookup"><span data-stu-id="e61ed-109">Assisted Telephony can enable this option quickly and simply.</span></span> <span data-ttu-id="e61ed-110">Дополнительные сведения о различии между полными приложениями TAPI и поддержкой телефонии см. в разделе [уровни обслуживания TAPI](tapi-levels-of-service.md) .</span><span class="sxs-lookup"><span data-stu-id="e61ed-110">Please see [TAPI Levels of Service](tapi-levels-of-service.md) for more information on the distinction between full TAPI applications and Assisted Telephony.</span></span>

<span data-ttu-id="e61ed-111">Второе важное решение — использовать TAPI 2. x, API на основе C или TAPI 3. x, основанный на COM.</span><span class="sxs-lookup"><span data-stu-id="e61ed-111">The second important decision is whether to use TAPI 2.x, the C-based API, or TAPI 3.x, which is based on COM.</span></span> <span data-ttu-id="e61ed-112">См. раздел [TAPI 3. x и TAPI 2. x](tapi-3-x-versus-tapi-2-x.md) , в котором рассматриваются важные моменты, касающиеся выбора того, какой из них следует использовать.</span><span class="sxs-lookup"><span data-stu-id="e61ed-112">Please see [TAPI 3.x vs. TAPI 2.x](tapi-3-x-versus-tapi-2-x.md) for a discussion of important considerations in deciding which one to use.</span></span>

<span data-ttu-id="e61ed-113">На следующей схеме показаны основные стандартные блоки полного приложения TAPI.</span><span class="sxs-lookup"><span data-stu-id="e61ed-113">The following diagram illustrates the basic building blocks of a full TAPI application.</span></span> <span data-ttu-id="e61ed-114">TAPI 2. x и TAPI 3. x разрешаются в этих разделах.</span><span class="sxs-lookup"><span data-stu-id="e61ed-114">TAPI 2.x and TAPI 3.x are both addressed in these sections.</span></span> <span data-ttu-id="e61ed-115">В обзорных разделах для TAPI 2. x или TAPI 3. x используется специальный материал.</span><span class="sxs-lookup"><span data-stu-id="e61ed-115">Material that is highly specific to one is addressed in the overview sections for TAPI 2.x or TAPI 3.x.</span></span>

![стандартные блоки приложения TAPI](images/tapior3.png)

<span data-ttu-id="e61ed-117">По следующим ссылкам можно получить содержимое, соответствующее рисункам на изображении выше:</span><span class="sxs-lookup"><span data-stu-id="e61ed-117">The following links provide content that corresponds to the figures in the above image:</span></span>

| <span data-ttu-id="e61ed-118">Замкнут</span><span class="sxs-lookup"><span data-stu-id="e61ed-118">Figure</span></span> | <span data-ttu-id="e61ed-119">Документация</span><span class="sxs-lookup"><span data-stu-id="e61ed-119">Documentation</span></span>                                                                    |
|--------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e61ed-120">1</span><span class="sxs-lookup"><span data-stu-id="e61ed-120">1</span></span>      | [<span data-ttu-id="e61ed-121">Инициализация TAPI</span><span class="sxs-lookup"><span data-stu-id="e61ed-121">TAPI Initialization</span></span>](tapi-initialization.md)                                   |
| <span data-ttu-id="e61ed-122">2</span><span class="sxs-lookup"><span data-stu-id="e61ed-122">2</span></span>      | [<span data-ttu-id="e61ed-123">Управление сеансом</span><span class="sxs-lookup"><span data-stu-id="e61ed-123">Session Control</span></span>](session-control.md)                                           |
| <span data-ttu-id="e61ed-124">3</span><span class="sxs-lookup"><span data-stu-id="e61ed-124">3</span></span>      | [<span data-ttu-id="e61ed-125">Управление устройством</span><span class="sxs-lookup"><span data-stu-id="e61ed-125">Device Control</span></span>](device-control.md)                                             |
| <span data-ttu-id="e61ed-126">4</span><span class="sxs-lookup"><span data-stu-id="e61ed-126">4</span></span>      | [<span data-ttu-id="e61ed-127">Элемент управления мультимедиа</span><span class="sxs-lookup"><span data-stu-id="e61ed-127">Media Control</span></span>](media-control.md)                                               |
| <span data-ttu-id="e61ed-128">5</span><span class="sxs-lookup"><span data-stu-id="e61ed-128">5</span></span>      | [<span data-ttu-id="e61ed-129">Сведения об элементах управления центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="e61ed-129">About Call Center Controls</span></span>](about-call-center-controls.md)                     |
| <span data-ttu-id="e61ed-130">6</span><span class="sxs-lookup"><span data-stu-id="e61ed-130">6</span></span>      | [<span data-ttu-id="e61ed-131">Встречные конференции с IP-телефонией</span><span class="sxs-lookup"><span data-stu-id="e61ed-131">Rendezvous IP Telephony Conferencing</span></span>](rendezvous-ip-telephony-conferencing.md) |
| <span data-ttu-id="e61ed-132">7</span><span class="sxs-lookup"><span data-stu-id="e61ed-132">7</span></span>      | [<span data-ttu-id="e61ed-133">Завершение работы TAPI</span><span class="sxs-lookup"><span data-stu-id="e61ed-133">TAPI Shutdown</span></span>](tapi-shutdown.md)                                               |



 

 

 



