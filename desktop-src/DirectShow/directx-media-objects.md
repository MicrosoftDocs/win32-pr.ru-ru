---
description: Объекты мультимедиа DirectX
ms.assetid: e4424740-31b9-4317-8791-6a9aebb0c7e6
title: Объекты мультимедиа DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2119fc8cce602bc1cc085886edd6852320aca180
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105674528"
---
# <a name="directx-media-objects"></a><span data-ttu-id="d1513-103">Объекты мультимедиа DirectX</span><span class="sxs-lookup"><span data-stu-id="d1513-103">DirectX Media Objects</span></span>

> [!Note]  
> <span data-ttu-id="d1513-104">Дмос были заменены [Media Foundation преобразованиями](/windows/desktop/medfound/media-foundation-transforms) (МФТС).</span><span class="sxs-lookup"><span data-stu-id="d1513-104">DMOs have been superseded by [Media Foundation Transforms](/windows/desktop/medfound/media-foundation-transforms) (MFTs).</span></span> <span data-ttu-id="d1513-105">Интерфейсы DMO по-прежнему поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="d1513-105">The DMO interfaces are still supported.</span></span> <span data-ttu-id="d1513-106">Однако при написании пользовательского кодека или подключаемого модуля обработки звука и видео следует рассмотреть возможность его реализации как MFT.</span><span class="sxs-lookup"><span data-stu-id="d1513-106">However, if you are writing a custom codec or audio/video processing plug-in, you should consider implementing it as an MFT.</span></span>

 

<span data-ttu-id="d1513-107">Объекты мультимедиа DirectX (дмос) — это компоненты потоковой передачи данных на основе COM.</span><span class="sxs-lookup"><span data-stu-id="d1513-107">DirectX Media Objects (DMOs) are COM-based data-streaming components.</span></span> <span data-ttu-id="d1513-108">В некоторых отношениях дмос похожи на фильтры Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d1513-108">In some respects, DMOs are similar to Microsoft DirectShow filters.</span></span> <span data-ttu-id="d1513-109">Как и фильтры DirectShow, дмос принимает входные данные и использует их для создания выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d1513-109">Like DirectShow filters, DMOs take input data and use it to produce output data.</span></span> <span data-ttu-id="d1513-110">Однако прикладные программные интерфейсы (API) для дмос гораздо проще, чем соответствующие API-интерфейсы для DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d1513-110">However, the application programming interfaces (APIs) for DMOs are much simpler than the corresponding APIs for DirectShow.</span></span> <span data-ttu-id="d1513-111">В результате дмос проще в создании, тестировании и использовании.</span><span class="sxs-lookup"><span data-stu-id="d1513-111">As a result, DMOs are easier to create, test, and use.</span></span> <span data-ttu-id="d1513-112">Дмос можно использовать во многих сценариях:</span><span class="sxs-lookup"><span data-stu-id="d1513-112">DMOs can be used in many scenarios:</span></span>

-   <span data-ttu-id="d1513-113">Приложения, основанные на DirectShow, могут использовать дмос через фильтр DirectShow, называемый фильтром [оболочки DMO](dmo-wrapper-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="d1513-113">Applications based on DirectShow can use DMOs through a DirectShow filter called the [DMO Wrapper](dmo-wrapper-filter.md) filter.</span></span> <span data-ttu-id="d1513-114">Различие между фильтрами и дмос является прозрачным для приложения.</span><span class="sxs-lookup"><span data-stu-id="d1513-114">The distinction between filters and DMOs is transparent to the application.</span></span> <span data-ttu-id="d1513-115">Приложение не вызывает напрямую интерфейсы API DMO.</span><span class="sxs-lookup"><span data-stu-id="d1513-115">The application does not directly call the DMO APIs.</span></span>
-   <span data-ttu-id="d1513-116">Приложения, основанные на Microsoft DirectSound, могут использовать звуковые эффекты дмос.</span><span class="sxs-lookup"><span data-stu-id="d1513-116">Applications based on Microsoft DirectSound can use audio effect DMOs.</span></span> <span data-ttu-id="d1513-117">Опять же, приложение изолируется от низкоуровневых API DMO с интерфейсами API DirectSound более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="d1513-117">Again, the application is shielded from the low-level DMO APIs by the higher-level DirectSound APIs.</span></span>
-   <span data-ttu-id="d1513-118">Приложения могут использовать дмос напрямую.</span><span class="sxs-lookup"><span data-stu-id="d1513-118">Applications can use DMOs directly.</span></span>

<span data-ttu-id="d1513-119">Таким же путем написания DMO вы создаете компонент, который можно использовать в широком спектре приложений.</span><span class="sxs-lookup"><span data-stu-id="d1513-119">Thus, by writing a DMO, you create a component that can be used in a wide range of applications.</span></span> <span data-ttu-id="d1513-120">Эта документация содержит следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="d1513-120">This documentation contains the following sections:</span></span>

-   [<span data-ttu-id="d1513-121">О дмос</span><span class="sxs-lookup"><span data-stu-id="d1513-121">About DMOs</span></span>](about-dmos.md)
-   [<span data-ttu-id="d1513-122">Использование дмос</span><span class="sxs-lookup"><span data-stu-id="d1513-122">Using DMOs</span></span>](using-dmos.md)
-   [<span data-ttu-id="d1513-123">Написание DMO</span><span class="sxs-lookup"><span data-stu-id="d1513-123">Writing a DMO</span></span>](writing-a-dmo.md)
-   [<span data-ttu-id="d1513-124">Параметры носителя</span><span class="sxs-lookup"><span data-stu-id="d1513-124">Media Parameters</span></span>](media-parameters.md)
-   [<span data-ttu-id="d1513-125">Справочник по DMO</span><span class="sxs-lookup"><span data-stu-id="d1513-125">DMO Reference</span></span>](dmo-reference.md)

## <a name="related-topics"></a><span data-ttu-id="d1513-126">См. также</span><span class="sxs-lookup"><span data-stu-id="d1513-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1513-127">DirectShow</span><span class="sxs-lookup"><span data-stu-id="d1513-127">DirectShow</span></span>](directshow.md)
</dt> </dl>

 

 
