---
title: Копирование компакт-диска
description: Копирование компакт-диска
ms.assetid: f5c1b5bf-d616-48cb-8690-e0237c56e402
keywords:
- Проигрыватель Windows Media, копирование компакт-дисков
- Объектная модель проигрывателя Windows Media, копирование компакт-дисков
- Объектная модель, копирование компакт-дисков
- Элемент управления ActiveX проигрывателя Windows Media, копирование компакт-дисков
- Элемент управления ActiveX, копирование компакт-дисков
- Мобильный элемент управления ActiveX проигрывателя Windows Media, копирование компакт-дисков
- Проигрыватель Windows Media Mobile, копирование компакт-дисков
- Копирование компакт-дисков, сведения
- Копирование компакт-дисков, о программе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 767734b3449fd0a64b31c8f351406bbf9f6c805b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888808"
---
# <a name="ripping-a-cd"></a><span data-ttu-id="524e5-112">Копирование компакт-диска</span><span class="sxs-lookup"><span data-stu-id="524e5-112">Ripping a CD</span></span>

<span data-ttu-id="524e5-113">Существует два способа копирования компакт-диска с помощью элемента управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="524e5-113">There are two ways to rip a CD by using the Windows Media Player control.</span></span> <span data-ttu-id="524e5-114">Проигрыватель Windows Media 9 может копировать компакт-диски с помощью **ивмпплайерсервицес:: сеттаскпане**.</span><span class="sxs-lookup"><span data-stu-id="524e5-114">Windows Media Player 9 can rip CDs by using **IWMPPlayerServices::setTaskPane**.</span></span> <span data-ttu-id="524e5-115">В проигрывателе Windows Media 11 появился интерфейс **ивмпкдромрип** для копирования компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="524e5-115">Windows Media Player 11 introduces the **IWMPCdromRip** interface for ripping CDs.</span></span> <span data-ttu-id="524e5-116">Этот интерфейс предоставляет больше функций, чем **ивмпплайерсервицес:: сеттаскпане**, и рекомендуется использовать **ивмпкдромрип** , если он доступен.</span><span class="sxs-lookup"><span data-stu-id="524e5-116">This interface provides more functionality than **IWMPPlayerServices::setTaskPane**, and it is recommended that you use **IWMPCdromRip** if it is available.</span></span>

<span data-ttu-id="524e5-117">В следующих разделах описывается копирование компакт-диска с помощью проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="524e5-117">The following sections describe how to rip a CD by using Windows Media Player.</span></span>

-   [<span data-ttu-id="524e5-118">Копирование с помощью интерфейса Ивмпкдромрип</span><span class="sxs-lookup"><span data-stu-id="524e5-118">Ripping by Using the IWMPCdromRip Interface</span></span>](ripping-by-using-the-iwmpcdromrip-interface.md)
-   [<span data-ttu-id="524e5-119">Копирование с помощью Ивмпплайерсервицес:: Сеттаскпане</span><span class="sxs-lookup"><span data-stu-id="524e5-119">Ripping by Using IWMPPlayerServices::setTaskPane</span></span>](ripping-by-using-iwmpplayerservices--settaskpane.md)

## <a name="related-topics"></a><span data-ttu-id="524e5-120">См. также</span><span class="sxs-lookup"><span data-stu-id="524e5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="524e5-121">**Управление проигрывателем**</span><span class="sxs-lookup"><span data-stu-id="524e5-121">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




