---
title: Реализация Цечо Допроцессаутпут
description: Реализация Цечо Допроцессаутпут
ms.assetid: afd91022-4e2d-46a2-a0f4-cd2b558536d6
keywords:
- Подключаемые модули проигрывателя Windows Media, метод Echo Sample Допроцессаутпут
- подключаемые модули, метод Echo Sample Допроцессаутпут
- подключаемые модули обработки цифровых сигналов, метод Echo Sample Допроцессаутпут
- Подключаемые модули DSP, метод Echo Sample Допроцессаутпут
- Пример подключаемого модуля Echo DSP, метод Допроцессаутпут
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ff40246a6a0ccda2b3f17b12924c44cb79fa4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068608"
---
# <a name="implementing-cechodoprocessoutput"></a><span data-ttu-id="ac32e-108">Реализация Цечо::D Опроцессаутпут</span><span class="sxs-lookup"><span data-stu-id="ac32e-108">Implementing CEcho::DoProcessOutput</span></span>

<span data-ttu-id="ac32e-109">Метод **допроцессаутпут** выполняет обработку цифровых сигналов.</span><span class="sxs-lookup"><span data-stu-id="ac32e-109">The **DoProcessOutput** method performs the digital signal processing.</span></span> <span data-ttu-id="ac32e-110">Это метод, который вносит изменения в данные, предоставляемые проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ac32e-110">This is the method that makes the changes to the data provided by Windows Media Player.</span></span> <span data-ttu-id="ac32e-111">Это результаты этого метода, которые будут слышаться в виде эхо-эффекта при завершении подключаемого модуля Echo Sample.</span><span class="sxs-lookup"><span data-stu-id="ac32e-111">It is the results of this method that you will hear as an echo effect when your Echo sample plug-in is complete.</span></span>

<span data-ttu-id="ac32e-112">В этом примере подключаемый модуль будет обрабатывать только 8-разрядный или 16-разрядный звук.</span><span class="sxs-lookup"><span data-stu-id="ac32e-112">For this sample, the plug-in will only process 8-bit or 16-bit audio.</span></span> <span data-ttu-id="ac32e-113">Необходимо внести некоторые изменения в образец кода мастера подключаемых модулей, чтобы удалить разделы, которые обрабатывают звуковые файлы более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="ac32e-113">You will need to make some changes to the plug-in wizard sample code to remove the sections that process higher bit depth audio.</span></span> <span data-ttu-id="ac32e-114">Однако стоит изучить эти разделы, так как вы можете добавить собственную реализацию эха для этих форматов.</span><span class="sxs-lookup"><span data-stu-id="ac32e-114">It is worthwhile to study these sections, however, because you may decide to add your own echo implementation for those formats.</span></span>

<span data-ttu-id="ac32e-115">В следующих разделах подробно описаны изменения, которые необходимо внести в код.</span><span class="sxs-lookup"><span data-stu-id="ac32e-115">The following sections detail the changes you need to make to the code:</span></span>

-   [<span data-ttu-id="ac32e-116">Удаление кода для обработки более чем 16 бит</span><span class="sxs-lookup"><span data-stu-id="ac32e-116">Removing the Code to Process Greater than 16 Bits</span></span>](removing-the-code-to-process-greater-than-16-bits.md)
-   [<span data-ttu-id="ac32e-117">Обработка звуковых данных</span><span class="sxs-lookup"><span data-stu-id="ac32e-117">Processing the Audio Data</span></span>](processing-the-audio-data.md)
-   [<span data-ttu-id="ac32e-118">Переменные для выполнения обработки</span><span class="sxs-lookup"><span data-stu-id="ac32e-118">Variables to Perform Processing</span></span>](variables-to-perform-processing.md)
-   [<span data-ttu-id="ac32e-119">Создание эффекта эха</span><span class="sxs-lookup"><span data-stu-id="ac32e-119">Creating the Echo Effect</span></span>](creating-the-echo-effect.md)

## <a name="related-topics"></a><span data-ttu-id="ac32e-120">См. также</span><span class="sxs-lookup"><span data-stu-id="ac32e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac32e-121">**Пример эха**</span><span class="sxs-lookup"><span data-stu-id="ac32e-121">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




