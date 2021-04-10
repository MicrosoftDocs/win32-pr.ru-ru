---
description: В этом обзоре представлено несколько методов XAudio2, которые можно вызывать как часть набора операций.
ms.assetid: 5bfd747d-af65-f619-e549-be8130748261
title: Наборы операций XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90955fc0557f3f84840436c121f768caff4af81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272817"
---
# <a name="xaudio2-operation-sets"></a><span data-ttu-id="a1f2e-103">Наборы операций XAudio2</span><span class="sxs-lookup"><span data-stu-id="a1f2e-103">XAudio2 Operation Sets</span></span>

<span data-ttu-id="a1f2e-104">В этом обзоре представлено несколько методов XAudio2, которые можно вызывать как часть набора операций.</span><span class="sxs-lookup"><span data-stu-id="a1f2e-104">This overview introduces several XAudio2 methods that you can call as part of an operation set.</span></span>

<span data-ttu-id="a1f2e-105">Несколько методов XAudio2 принимают аргумент *Operation* , который позволяет вызывать их как часть отложенной группы.</span><span class="sxs-lookup"><span data-stu-id="a1f2e-105">Several XAudio2 methods take the *OperationSet* argument, which allows them to be called as part of a deferred group.</span></span> <span data-ttu-id="a1f2e-106">В определенное время можно одновременно применить весь набор изменений, вызвав функцию [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) с идентификатором набора *операций* для этой группы.</span><span class="sxs-lookup"><span data-stu-id="a1f2e-106">At a specific time, you can apply an entire set of changes simultaneously by calling the function [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with the *OperationSet* identifier for that group.</span></span> <span data-ttu-id="a1f2e-107">Идентификатор является произвольным числом.</span><span class="sxs-lookup"><span data-stu-id="a1f2e-107">The identifier is an arbitrary number.</span></span> <span data-ttu-id="a1f2e-108">Таким образом, он позволяет отдельным частям кода клиента применять отдельные атомарные изменения к графу без каких либо конфликтов.</span><span class="sxs-lookup"><span data-stu-id="a1f2e-108">Thus, it allows separate parts of the client code to apply separate atomic changes to the graph without any conflict.</span></span> <span data-ttu-id="a1f2e-109">Рекомендуется, чтобы клиент увеличивал глобальный счетчик всякий раз, когда ему *нужно создать уникальный новый идентификатор.*</span><span class="sxs-lookup"><span data-stu-id="a1f2e-109">The recommended practice is for the client to increment a global counter whenever it needs to generate a unique, new *OperationSet* identifier.</span></span> <span data-ttu-id="a1f2e-110">Набор изменений, примененных к диаграмме, применяется атомарно, гарантируется точность выборки.</span><span class="sxs-lookup"><span data-stu-id="a1f2e-110">A set of changes to the graph, applied atomically, is guaranteed to be sample-accurate.</span></span> <span data-ttu-id="a1f2e-111">Например, голосов начнет синхронизироваться.</span><span class="sxs-lookup"><span data-stu-id="a1f2e-111">For example, voices will start in sync.</span></span>

<span data-ttu-id="a1f2e-112">Если для параметра *Operation* задано значение XAUDIO2 \_ commit \_ Now, это изменение применяется немедленно.</span><span class="sxs-lookup"><span data-stu-id="a1f2e-112">If you set *OperationSet* to XAUDIO2\_COMMIT\_NOW, the change applies immediately.</span></span> <span data-ttu-id="a1f2e-113">Он вступает в силу на первом проходе обработки звука после вызова метода.</span><span class="sxs-lookup"><span data-stu-id="a1f2e-113">It takes effect in the first audio processing pass after the method call.</span></span> <span data-ttu-id="a1f2e-114">При вызове [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) с \_ фиксацией XAUDIO2 \_ все незавершенные наборы операций выполняются, независимо от идентификатора их набора операций  .</span><span class="sxs-lookup"><span data-stu-id="a1f2e-114">If you call [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with XAUDIO2\_COMMIT\_ALL, changes to all pending operations sets are performed, regardless of their *OperationSet* identifier.</span></span>

<span data-ttu-id="a1f2e-115">Некоторые методы вступают в силу немедленно, если они вызываются из обратного вызова XAudio2 с набором *операций* XAudio2 \_ commit \_ Now.</span><span class="sxs-lookup"><span data-stu-id="a1f2e-115">Certain methods take effect immediately when they are called from an XAudio2 callback with an *OperationSet* of XAUDIO2\_COMMIT\_NOW.</span></span> <span data-ttu-id="a1f2e-116">Все другие методы, принимающие аргумент *операции* , вступают в силу только при следующем проходе обработки после вызова метода (при вызове с параметром XAUDIO2 \_ commit \_ Now) или после вызова [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) с тем же именем *операции*.</span><span class="sxs-lookup"><span data-stu-id="a1f2e-116">All other methods that take an *OperationSet* argument only take effect on the next processing pass after the method is called (if called with XAUDIO2\_COMMIT\_NOW), or after [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) is called with the same *OperationSet*.</span></span> <span data-ttu-id="a1f2e-117">По этой причине некоторые вызовы методов могут не всегда происходить в том же порядке, в котором они были вызваны.</span><span class="sxs-lookup"><span data-stu-id="a1f2e-117">Because of this, certain method calls may not always happen in the same order in which they were called.</span></span>

<span data-ttu-id="a1f2e-118">Все ожидающие операции фиксируются атомарно при вызове [**IXAudio2:: стопенгине**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) .</span><span class="sxs-lookup"><span data-stu-id="a1f2e-118">All pending operations are committed atomically when [**IXAudio2::StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) is called.</span></span> <span data-ttu-id="a1f2e-119">Все методы, вызываемые при остановке обработчика, вступают в силу немедленно, независимо от предоставленного значения набора *операций* .</span><span class="sxs-lookup"><span data-stu-id="a1f2e-119">Any methods that are called while the engine is stopped take effect immediately, regardless of the *OperationSet* value provided.</span></span> <span data-ttu-id="a1f2e-120">При перезапуске подсистемы XAudio2 возвращается в асинхронный режим.</span><span class="sxs-lookup"><span data-stu-id="a1f2e-120">When you restart the engine, XAudio2 returns to asynchronous mode.</span></span>

<span data-ttu-id="a1f2e-121">Простые сценарии, в которых наборы операций полезны, включают в себя следующие примеры.</span><span class="sxs-lookup"><span data-stu-id="a1f2e-121">Simple scenarios in which operation sets are useful include the following examples.</span></span>

-   <span data-ttu-id="a1f2e-122">Одновременное запуск нескольких голосов.</span><span class="sxs-lookup"><span data-stu-id="a1f2e-122">Starting multiple voices simultaneously.</span></span>
-   <span data-ttu-id="a1f2e-123">Одновременное отправление буфера в речь, установка параметров голоса и запуск голоса.</span><span class="sxs-lookup"><span data-stu-id="a1f2e-123">Simultaneously submitting a buffer to a voice, setting the voice parameters, and starting the voice.</span></span>
-   <span data-ttu-id="a1f2e-124">Внесение крупномасштабных изменений в граф, например подключение всех исходных голосов к новому субмикс Voice.</span><span class="sxs-lookup"><span data-stu-id="a1f2e-124">Making a large-scale change to the graph, such as connecting all source voices to a new submix voice.</span></span>

<span data-ttu-id="a1f2e-125">См. раздел [инструкции. Группирование звуковых методов в качестве набора операций](how-to--group-audio-methods-as-an-operation-set.md) для примера использования набора операций.</span><span class="sxs-lookup"><span data-stu-id="a1f2e-125">See [How to: Group Audio Methods as an Operation Set](how-to--group-audio-methods-as-an-operation-set.md) for an example of using an operation set.</span></span>

## <a name="operation-set-methods"></a><span data-ttu-id="a1f2e-126">Методы набора операций</span><span class="sxs-lookup"><span data-stu-id="a1f2e-126">Operation Set Methods</span></span>

<span data-ttu-id="a1f2e-127">В состав набора операций можно вызывать следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a1f2e-127">You can call the following methods as part of an operation set.</span></span>

-   [<span data-ttu-id="a1f2e-128">**IXAudio2SourceVoice:: Екситлуп**</span><span class="sxs-lookup"><span data-stu-id="a1f2e-128">**IXAudio2SourceVoice::ExitLoop**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-exitloop)
-   [<span data-ttu-id="a1f2e-129">**IXAudio2Voice:: Сетфилтерпараметерс**</span><span class="sxs-lookup"><span data-stu-id="a1f2e-129">**IXAudio2Voice::SetFilterParameters**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)
-   [<span data-ttu-id="a1f2e-130">**IXAudio2SourceVoice:: Сетфрекуенциратио**</span><span class="sxs-lookup"><span data-stu-id="a1f2e-130">**IXAudio2SourceVoice::SetFrequencyRatio**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio)
-   [<span data-ttu-id="a1f2e-131">**IXAudio2Voice::D Исаблиффект**</span><span class="sxs-lookup"><span data-stu-id="a1f2e-131">**IXAudio2Voice::DisableEffect**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect)
-   [<span data-ttu-id="a1f2e-132">**IXAudio2Voice:: Енаблиффект**</span><span class="sxs-lookup"><span data-stu-id="a1f2e-132">**IXAudio2Voice::EnableEffect**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)
-   [<span data-ttu-id="a1f2e-133">**IXAudio2Voice:: Сетчаннелволумес**</span><span class="sxs-lookup"><span data-stu-id="a1f2e-133">**IXAudio2Voice::SetChannelVolumes**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes)
-   [<span data-ttu-id="a1f2e-134">**IXAudio2Voice:: Сетеффектпараметерс**</span><span class="sxs-lookup"><span data-stu-id="a1f2e-134">**IXAudio2Voice::SetEffectParameters**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)
-   [<span data-ttu-id="a1f2e-135">**IXAudio2Voice:: Сетаутпутматрикс**</span><span class="sxs-lookup"><span data-stu-id="a1f2e-135">**IXAudio2Voice::SetOutputMatrix**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)
-   [<span data-ttu-id="a1f2e-136">**IXAudio2Voice:: Сетволуме**</span><span class="sxs-lookup"><span data-stu-id="a1f2e-136">**IXAudio2Voice::SetVolume**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)
-   [<span data-ttu-id="a1f2e-137">**IXAudio2SourceVoice:: Start**</span><span class="sxs-lookup"><span data-stu-id="a1f2e-137">**IXAudio2SourceVoice::Start**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)
-   [<span data-ttu-id="a1f2e-138">**IXAudio2SourceVoice:: останавливаться**</span><span class="sxs-lookup"><span data-stu-id="a1f2e-138">**IXAudio2SourceVoice::Stop**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop)

<span data-ttu-id="a1f2e-139">Как было сказано выше, клиентский код должен в конечном итоге вызвать функцию [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) для выполнения отложенных изменений.</span><span class="sxs-lookup"><span data-stu-id="a1f2e-139">As described previously, client code must ultimately call the function [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) to execute the deferred changes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1f2e-140">См. также</span><span class="sxs-lookup"><span data-stu-id="a1f2e-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1f2e-141">Наборы операций</span><span class="sxs-lookup"><span data-stu-id="a1f2e-141">Operation Sets</span></span>](operation-sets.md)
</dt> <dt>

[<span data-ttu-id="a1f2e-142">Руководство по программированию для XAudio2</span><span class="sxs-lookup"><span data-stu-id="a1f2e-142">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="a1f2e-143">Руководство: группировка звуковых методов как набора операций</span><span class="sxs-lookup"><span data-stu-id="a1f2e-143">How to: Group Audio Methods as an Operation Set</span></span>](how-to--group-audio-methods-as-an-operation-set.md)
</dt> </dl>

 

 
