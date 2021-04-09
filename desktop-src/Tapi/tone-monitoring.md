---
description: Мониторинг тонового режима отслеживает поток мультимедиа при вызове указанных тонов.
ms.assetid: c3218013-b71f-41cd-9397-ba717c0cf556
title: Мониторинг тона
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9a3275e5207999896792ee04dc1842b01f4ad0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080900"
---
# <a name="tone-monitoring"></a><span data-ttu-id="219b2-103">Мониторинг тона</span><span class="sxs-lookup"><span data-stu-id="219b2-103">Tone Monitoring</span></span>

<span data-ttu-id="219b2-104">Мониторинг тонового режима отслеживает поток мультимедиа при вызове указанных тонов.</span><span class="sxs-lookup"><span data-stu-id="219b2-104">Tone monitoring monitors the media stream of a call for specified tones.</span></span> <span data-ttu-id="219b2-105">Гудок описывается частотой и ритмичностью его компонентов.</span><span class="sxs-lookup"><span data-stu-id="219b2-105">A tone is described by its component frequencies and cadence.</span></span> <span data-ttu-id="219b2-106">Реализация API может обеспечить одновременное отслеживание нескольких различных тонов.</span><span class="sxs-lookup"><span data-stu-id="219b2-106">An implementation of the API may allow several different tones to be monitored simultaneously.</span></span> <span data-ttu-id="219b2-107">Приложение может отметить каждый тон, чтобы отличать различные звуки, для которых он запрашивает обнаружение.</span><span class="sxs-lookup"><span data-stu-id="219b2-107">An application can tag each tone to be able to distinguish the different tones for which it requests detection.</span></span>

<span data-ttu-id="219b2-108">Приложение может включить или отключить мониторинг тонового объекта при указанном вызове с помощью [**линемонитортонес**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones).</span><span class="sxs-lookup"><span data-stu-id="219b2-108">An application can enable or disable tone monitoring on a specified call with [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones).</span></span> <span data-ttu-id="219b2-109">С помощью этой функции приложение указывает, какие звуки должны обнаруживаться при указанном вызове.</span><span class="sxs-lookup"><span data-stu-id="219b2-109">With this function, the application indicates which tones to detect on a specified call.</span></span> <span data-ttu-id="219b2-110">Если включен мониторинг тона, обнаруженные цифры приводят к тому, что приложение будет уведомлено с помощью [**строки \_ монитортоне**](line-monitortone.md) Message.</span><span class="sxs-lookup"><span data-stu-id="219b2-110">When tone monitoring is enabled, detected digits cause the application to be notified with the [**LINE\_MONITORTONE**](line-monitortone.md) message.</span></span> <span data-ttu-id="219b2-111">Это сообщение предоставляет маркер вызова, на котором был обнаружен тон, а также тег приложения для тона.</span><span class="sxs-lookup"><span data-stu-id="219b2-111">This message provides the call handle on which the tone was detected as well as the application's tag for the tone.</span></span>

<span data-ttu-id="219b2-112">Область отслеживания тона связана с временем существования вызова.</span><span class="sxs-lookup"><span data-stu-id="219b2-112">The scope of tone monitoring is bound by the lifetime of the call.</span></span> <span data-ttu-id="219b2-113">Отслеживание тона в вызове завершается, как только вызов *отключается* или переходит в *состояние простоя*.</span><span class="sxs-lookup"><span data-stu-id="219b2-113">Tone monitoring on a call ends as soon the call *disconnects* or goes *idle*.</span></span>

> [!Note]  
> <span data-ttu-id="219b2-114">Мониторинг тонов, цифр или типов мультимедиа часто требует использования ресурсов, для которых поставщик услуг может иметь только ограниченный объем.</span><span class="sxs-lookup"><span data-stu-id="219b2-114">The monitoring of tones, digits, or media types often requires the use of resources of which the service provider can only have a finite amount.</span></span> <span data-ttu-id="219b2-115">Запрос на наблюдение может быть отклонен, если ресурсы недоступны.</span><span class="sxs-lookup"><span data-stu-id="219b2-115">A request for monitoring can be rejected if resources are not available.</span></span> <span data-ttu-id="219b2-116">По той же причине приложение должно отключить все ненужные средства мониторинга.</span><span class="sxs-lookup"><span data-stu-id="219b2-116">For the same reason, an application should disable any unnecessary monitoring.</span></span>

 

 

 



