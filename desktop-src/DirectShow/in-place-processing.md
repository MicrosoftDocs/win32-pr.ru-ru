---
description: Обработка In-Place
ms.assetid: 61e5c12c-e42a-42d8-ac5b-e60afaceda82
title: Обработка In-Place
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba0aa5c50fc000eadadc0f121db6f954a57c338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673067"
---
# <a name="in-place-processing"></a><span data-ttu-id="365b9-103">Обработка In-Place</span><span class="sxs-lookup"><span data-stu-id="365b9-103">In-Place Processing</span></span>

<span data-ttu-id="365b9-104">Некоторые преобразования данных могут быть выполнены путем непосредственного изменения данных.</span><span class="sxs-lookup"><span data-stu-id="365b9-104">Certain data transformations can be accomplished by directly modifying the data.</span></span> <span data-ttu-id="365b9-105">Это называется обработкой *на месте* .</span><span class="sxs-lookup"><span data-stu-id="365b9-105">This is called *in-place* processing.</span></span> <span data-ttu-id="365b9-106">Таким образом можно выполнять многие видеоэффекты и аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="365b9-106">Many audio and video effects can be done in this manner.</span></span> <span data-ttu-id="365b9-107">Если объект DMO поддерживает обработку на месте, он предоставляет интерфейс [**имедиаобжектинплаце**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) .</span><span class="sxs-lookup"><span data-stu-id="365b9-107">If a DMO supports in-place processing, it exposes the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) interface.</span></span> <span data-ttu-id="365b9-108">Обработка на месте, как правило, более эффективна, чем использование отдельных буферов для выходных данных.</span><span class="sxs-lookup"><span data-stu-id="365b9-108">In-place processing is generally more efficient than using separate buffers for the output.</span></span> <span data-ttu-id="365b9-109">(Одно главное исключение — когда буфер находится в видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="365b9-109">(One major exception is when the buffer resides in video memory.</span></span> <span data-ttu-id="365b9-110">В этом случае операции чтения выполняются намного медленнее, чем операции записи, поэтому обработка на месте не рекомендуется.)</span><span class="sxs-lookup"><span data-stu-id="365b9-110">In that situation, read operations are much slower than write operations, so in-place processing is not recommended.)</span></span>

<span data-ttu-id="365b9-111">Для обработки данных на месте клиент выполняет один вызов метода [**имедиаобжектинплаце::P шаблоны**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) , а не отдельные вызовы **ProcessInput** и **ProcessOutput**.</span><span class="sxs-lookup"><span data-stu-id="365b9-111">To process data in place, the client makes a single call to the [**IMediaObjectInPlace::Process**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) method, rather than separate calls to **ProcessInput** and **ProcessOutput**.</span></span> <span data-ttu-id="365b9-112">Метод **процесса** является синхронным; Вся обработка выполняется внутри вызова.</span><span class="sxs-lookup"><span data-stu-id="365b9-112">The **Process** method is synchronous; all processing occurs inside the call.</span></span> <span data-ttu-id="365b9-113">Кроме того, обработка на месте не использует объекты **имедиабуффер** .</span><span class="sxs-lookup"><span data-stu-id="365b9-113">Also, in-place processing does not use **IMediaBuffer** objects.</span></span> <span data-ttu-id="365b9-114">Метод **Process** принимает указатель непосредственно на буфер памяти.</span><span class="sxs-lookup"><span data-stu-id="365b9-114">The **Process** method takes a pointer directly to the memory buffer.</span></span>

<span data-ttu-id="365b9-115">DMO, поддерживающий обработку на месте, по-прежнему должен реализовывать интерфейс **имедиаобжект** , включая методы **ProcessInput** и **ProcessOutput** .</span><span class="sxs-lookup"><span data-stu-id="365b9-115">A DMO that supports in-place processing still must implement the **IMediaObject** interface, including the **ProcessInput** and **ProcessOutput** methods.</span></span> <span data-ttu-id="365b9-116">Клиент может выбрать, использовать ли обработку на месте или использовать отдельные буферы.</span><span class="sxs-lookup"><span data-stu-id="365b9-116">The client can choose whether to use in-place processing or use separate buffers.</span></span> <span data-ttu-id="365b9-117">Однако не следует смешивать два типа обработки.</span><span class="sxs-lookup"><span data-stu-id="365b9-117">However, do not mix the two types of processing.</span></span> <span data-ttu-id="365b9-118">При вызове **процесса** не вызывайте **ProcessInput** или **ProcessOutput** и наоборот.</span><span class="sxs-lookup"><span data-stu-id="365b9-118">If you call **Process**, do not call **ProcessInput** or **ProcessOutput**, and vice-versa.</span></span>

<span data-ttu-id="365b9-119">**Хвосты эффектов**</span><span class="sxs-lookup"><span data-stu-id="365b9-119">**Effect Tails**</span></span>

<span data-ttu-id="365b9-120">Встроенные объекты DMO могут создавать дополнительные выходные данные после остановки ввода.</span><span class="sxs-lookup"><span data-stu-id="365b9-120">An in-place DMO might create some additional output after the input stops.</span></span> <span data-ttu-id="365b9-121">Это называется *хвостовиком Effect*.</span><span class="sxs-lookup"><span data-stu-id="365b9-121">This is called an *effect tail*.</span></span> <span data-ttu-id="365b9-122">Например, переглагол будет продолжаться после того, как входные данные вступят в действие тишины.</span><span class="sxs-lookup"><span data-stu-id="365b9-122">For example, a reverb effect continues after the input reaches silence.</span></span> <span data-ttu-id="365b9-123">Если присутствует хвостовый элемент, метод **Process** возвращает \_ значение false.</span><span class="sxs-lookup"><span data-stu-id="365b9-123">If there is an effect tail, the **Process** method returns S\_FALSE.</span></span> <span data-ttu-id="365b9-124">После того как приложение обработало все свои данные, оно может создать заключительный фрагмент, отправив пустые буферы в метод **Process** .</span><span class="sxs-lookup"><span data-stu-id="365b9-124">Once the application has processed all of its data, it can generate the effect tail by sending empty buffers to the **Process** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="365b9-125">См. также</span><span class="sxs-lookup"><span data-stu-id="365b9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="365b9-126">Непосредственное размещение DMO</span><span class="sxs-lookup"><span data-stu-id="365b9-126">Directly Hosting a DMO</span></span>](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



