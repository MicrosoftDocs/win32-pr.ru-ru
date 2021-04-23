---
description: Непосредственное размещение DMO
ms.assetid: 10fb99cf-78d9-4519-9aec-23b0daeca9e2
title: Непосредственное размещение DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3c933cf4eb946abb9ffefd5186159595480887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806893"
---
# <a name="directly-hosting-a-dmo"></a><span data-ttu-id="a4363-103">Непосредственное размещение DMO</span><span class="sxs-lookup"><span data-stu-id="a4363-103">Directly Hosting a DMO</span></span>

<span data-ttu-id="a4363-104">В этом разделе описывается, как приложение может работать в качестве непосредственного клиента DMO.</span><span class="sxs-lookup"><span data-stu-id="a4363-104">This section describes how an application can act as the direct client of a DMO.</span></span> <span data-ttu-id="a4363-105">Приложение предоставляет входные данные для DMO, объекты DMO создают выходные данные, а приложение использует выходные данные для отрисовки, дальнейшей обработки или что-либо еще.</span><span class="sxs-lookup"><span data-stu-id="a4363-105">The application delivers input to the DMO, the DMO creates output, and the application uses the output for rendering, further processing, or anything else.</span></span> <span data-ttu-id="a4363-106">Приложение отвечает за такие проблемы, как выделение памяти, время и синхронизация, а также многопоточность.</span><span class="sxs-lookup"><span data-stu-id="a4363-106">The application is responsible for issues such as memory allocation, timing and synchronization, and threading.</span></span> <span data-ttu-id="a4363-107">Эти требования будут зависеть от природы приложения.</span><span class="sxs-lookup"><span data-stu-id="a4363-107">These requirements will depend on the nature of the application.</span></span>

<span data-ttu-id="a4363-108">Сведения в этом разделе также применяются при написании компонента, который выступает в качестве слоя между приложением и DMO (например, с элементом управления ActiveX, в котором размещен объект DMO).</span><span class="sxs-lookup"><span data-stu-id="a4363-108">The information in this section also applies if you are writing a component that acts as a layer between an application and a DMO (for example, an ActiveX Control that hosts a DMO).</span></span> <span data-ttu-id="a4363-109">Кроме того, следует прочесть этот раздел, если вы пишете DMO, так как он описывает функциональные возможности, которые должен реализовать ваш объект DMO.</span><span class="sxs-lookup"><span data-stu-id="a4363-109">In addition, you should read this section if you are writing a DMO, because it describes the functionality that your DMO must implement.</span></span>

<span data-ttu-id="a4363-110">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="a4363-110">This section contains the following topics:</span></span>

-   [<span data-ttu-id="a4363-111">Настройка типов мультимедиа для DMO</span><span class="sxs-lookup"><span data-stu-id="a4363-111">Setting Media Types on a DMO</span></span>](setting-media-types-on-a-dmo.md)
-   [<span data-ttu-id="a4363-112">Обработка данных в DMO</span><span class="sxs-lookup"><span data-stu-id="a4363-112">Processing Data in a DMO</span></span>](processing-data-in-a-dmo.md)
-   [<span data-ttu-id="a4363-113">Обработка на месте</span><span class="sxs-lookup"><span data-stu-id="a4363-113">In-Place Processing</span></span>](in-place-processing.md)
-   [<span data-ttu-id="a4363-114">Необязательные потоки</span><span class="sxs-lookup"><span data-stu-id="a4363-114">Optional Streams</span></span>](optional-streams.md)
-   [<span data-ttu-id="a4363-115">Реализация Имедиабуффер</span><span class="sxs-lookup"><span data-stu-id="a4363-115">Implementing IMediaBuffer</span></span>](implementing-imediabuffer.md)

## <a name="related-topics"></a><span data-ttu-id="a4363-116">См. также</span><span class="sxs-lookup"><span data-stu-id="a4363-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4363-117">Использование дмос</span><span class="sxs-lookup"><span data-stu-id="a4363-117">Using DMOs</span></span>](using-dmos.md)
</dt> </dl>

 

 



