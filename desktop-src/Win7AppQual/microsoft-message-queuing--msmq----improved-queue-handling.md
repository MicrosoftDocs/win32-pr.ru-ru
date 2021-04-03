---
description: .
ms.assetid: 49bdfdfa-c77e-4a57-8079-bf4ff6b5010b
title: Очередь сообщений Майкрософт (MSMQ) — Улучшенная обработка очередей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffcc566c4c4ea461fdd9c4634b26ff69f239f03e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998718"
---
# <a name="microsoft-message-queuing-msmq---improved-queue-handling"></a><span data-ttu-id="9cc82-103">Очередь сообщений Майкрософт (MSMQ) — Улучшенная обработка очередей</span><span class="sxs-lookup"><span data-stu-id="9cc82-103">Microsoft Message Queuing (MSMQ) - Improved Queue Handling</span></span>

## <a name="platforms"></a><span data-ttu-id="9cc82-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="9cc82-104">Platforms</span></span>

<span data-ttu-id="9cc82-105">**Клиенты** — Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cc82-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="9cc82-106">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9cc82-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="9cc82-107">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="9cc82-107">Feature Impact</span></span>

 <span data-ttu-id="9cc82-108">**Серьезность** — низкая</span><span class="sxs-lookup"><span data-stu-id="9cc82-108">**Severity** - Low</span></span>  
<span data-ttu-id="9cc82-109">**Частота** -низкая</span><span class="sxs-lookup"><span data-stu-id="9cc82-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="9cc82-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9cc82-110">Description</span></span>

<span data-ttu-id="9cc82-111">Служба MSMQ не ограничивает число очередей, которые могут быть созданы в системе.</span><span class="sxs-lookup"><span data-stu-id="9cc82-111">MSMQ Service does not put a hard limit on the number of queues that can be created on a system.</span></span> <span data-ttu-id="9cc82-112">Однако производительность системы снижается, когда создается большое количество очередей.</span><span class="sxs-lookup"><span data-stu-id="9cc82-112">However, the performance of the system is impacted when a large number of queues is created.</span></span> <span data-ttu-id="9cc82-113">В частности, при наличии более чем нескольких тысяч очередей время запуска службы MSMQ увеличивается экспоненциально, что приводит к заметному влиянию.</span><span class="sxs-lookup"><span data-stu-id="9cc82-113">Specifically, when there are more than a few thousand queues, the start-up time of the MSMQ Service increases exponentially resulting in a visible impact.</span></span>

<span data-ttu-id="9cc82-114">Майкрософт оптимизирует запуск службы MSMQ в Windows 7, чтобы уменьшить издержки на подстановку для загрузки очередей в память.</span><span class="sxs-lookup"><span data-stu-id="9cc82-114">Microsoft has optimized the MSMQ Service start-up in Windows 7 to reduce the lookup overhead for loading the queues into memory.</span></span> <span data-ttu-id="9cc82-115">Эта оптимизация привела к значительному улучшению времени запуска службы MSMQ, даже если в системе создано несколько тысяч очередей.</span><span class="sxs-lookup"><span data-stu-id="9cc82-115">This optimization has led to a dramatic improvement of the start-up time of the MSMQ Service even when several thousand queues are created in the system.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="9cc82-116">Влияние на манифесты</span><span class="sxs-lookup"><span data-stu-id="9cc82-116">Manifestation of Impact</span></span>

<span data-ttu-id="9cc82-117">Это улучшение производительности не влияет на функциональность любого существующего приложения.</span><span class="sxs-lookup"><span data-stu-id="9cc82-117">This performance improvement does not impact the functionality of any existing application.</span></span>

## <a name="leveraging-the-changed-feature"></a><span data-ttu-id="9cc82-118">Использование измененной функции</span><span class="sxs-lookup"><span data-stu-id="9cc82-118">Leveraging the Changed Feature</span></span>

<span data-ttu-id="9cc82-119">Разработчики приложений, использующие MSMQ в Windows 7, теперь могут спроектировать свои решения, не ограничивая число очередей.</span><span class="sxs-lookup"><span data-stu-id="9cc82-119">Application developers using MSMQ on Windows 7 can now architect their solutions without limiting the number of queues.</span></span> <span data-ttu-id="9cc82-120">Обратите внимание, что количество очередей по-прежнему влияет на общую производительность сервера MSMQ, но снижение производительности теперь находится на линейной, а не экспоненциальной шкале.</span><span class="sxs-lookup"><span data-stu-id="9cc82-120">Note that the number of queues still affects overall performance of the MSMQ Server, but the performance impact is now on a linear rather than exponential scale.</span></span>

## <a name="compatibility-performance-reliability-and-usability-tests"></a><span data-ttu-id="9cc82-121">Тесты на совместимость, производительность, надежность и удобство использования</span><span class="sxs-lookup"><span data-stu-id="9cc82-121">Compatibility, Performance, Reliability, and Usability Tests</span></span>

<span data-ttu-id="9cc82-122">Если вы используете большое количество очередей, имитируйте рабочую среду в испытательной среде, отслеживайте производительность и проанализируйте время запуска службы и пропускную способность сообщений с большим количеством очередей и сообщений, имеющихся в тестовой системе.</span><span class="sxs-lookup"><span data-stu-id="9cc82-122">If you use a large number of queues, simulate the production environment on a test bed, monitor performance, and analyze the service start-up time and the message throughput with a large number of queues and messages present in the test system.</span></span>

 

 



