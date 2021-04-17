---
description: При поступлении нового сеанса связи приложения TAPI, которые регистрировали интерес в адресе и типе носителя, будут отправлять уведомления о событии.
ms.assetid: 6074619c-6aa0-4b03-9208-10268682e704
title: Ответ на сеанс, инициированный в других местах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e25651b58f8841ac4de9bf14f4d139161c1359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674467"
---
# <a name="respond-to-session-initiated-elsewhere"></a><span data-ttu-id="b3af4-103">Ответ на сеанс, инициированный в других местах</span><span class="sxs-lookup"><span data-stu-id="b3af4-103">Respond to Session Initiated Elsewhere</span></span>

<span data-ttu-id="b3af4-104">При поступлении нового сеанса связи приложения TAPI, которые регистрировали интерес в [адресе](address-ovr.md) и [типе носителя](media-type-ovr.md) , будут отправлять [уведомления о событии](event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="b3af4-104">When a new communications session arrives, TAPI applications that registered an interest in the [address](address-ovr.md) and [media type](media-type-ovr.md) will be sent an [event notification](event-notification.md).</span></span> <span data-ttu-id="b3af4-105">Только одно приложение будет предлагать [права](privilege-ovr.md) владения для сеанса.</span><span class="sxs-lookup"><span data-stu-id="b3af4-105">Only one application will be offered ownership [privileges](privilege-ovr.md) over the session.</span></span> <span data-ttu-id="b3af4-106">Это приложение не может отклонять сеанс.</span><span class="sxs-lookup"><span data-stu-id="b3af4-106">This application cannot refuse the session.</span></span>

<span data-ttu-id="b3af4-107">Первоначальное состояние вызова входящего сеанса — предложение.</span><span class="sxs-lookup"><span data-stu-id="b3af4-107">The initial call state of an incoming session is offering.</span></span> <span data-ttu-id="b3af4-108">Пока вызов находится в состоянии предложения, приложение может получить такие сведения, как режим носителя и причина вызова, если поставщики услуг представили эти сведения и доступны.</span><span class="sxs-lookup"><span data-stu-id="b3af4-108">While the call is in the offering state, an application can obtain information such as bearer mode and call reason, if the service providers supplied this information and it is available.</span></span> <span data-ttu-id="b3af4-109">Некоторые сведения о вызовах могут быть недоступны немедленно, например идентификатор вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="b3af4-109">Some call information may not be available immediately, such as caller ID.</span></span>

<span data-ttu-id="b3af4-110">Существует шесть базовых ответов на предлагаемый сеанс: [ответ](answer-ovr.md), [принятие](accept-ovr.md), пересылка, [Удаление](drop-ovr.md), [переадресация](forward-ovr.md)и [Перенаправление](redirect-ovr.md). [](handoffs-ovr.md)</span><span class="sxs-lookup"><span data-stu-id="b3af4-110">There are six basic responses to an offered session: [answer](answer-ovr.md), [accept](accept-ovr.md), [handoff](handoffs-ovr.md), [drop](drop-ovr.md), [forward](forward-ovr.md), and [redirect](redirect-ovr.md).</span></span> <span data-ttu-id="b3af4-111">В зависимости от поставщика услуг, полный набор этих операций может быть недоступен.</span><span class="sxs-lookup"><span data-stu-id="b3af4-111">Depending on the service provider, the full set of these operations may not be available.</span></span>

 

 



