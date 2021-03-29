---
description: О устройствах видеозаписи
ms.assetid: 1bf6e64f-c3cf-45a4-9f87-1b8cf503d98b
title: О устройствах видеозаписи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ab9797c11b5c22f6196a5b4e781e50ce34edec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805932"
---
# <a name="about-video-capture-devices"></a><span data-ttu-id="ba447-103">О устройствах видеозаписи</span><span class="sxs-lookup"><span data-stu-id="ba447-103">About Video Capture Devices</span></span>

<span data-ttu-id="ba447-104">Большинство новых устройств записи видео используют драйверы WDM (WDM).</span><span class="sxs-lookup"><span data-stu-id="ba447-104">Most new video capture devices use Windows Driver Model (WDM) drivers.</span></span> <span data-ttu-id="ba447-105">В архитектуре WDM Корпорация Майкрософт предоставляет набор аппаратно независимых драйверов, называемых драйверами классов, и поставщик оборудования предоставляет аппаратные минидриверс.</span><span class="sxs-lookup"><span data-stu-id="ba447-105">In the WDM architecture, Microsoft supplies a set of hardware-independent drivers, called class drivers, and the hardware vendor provides hardware-specific minidrivers.</span></span> <span data-ttu-id="ba447-106">Минидривер реализует все функции, характерные для устройства. для большинства функций минидривер вызывает драйвер класса Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="ba447-106">A minidriver implements any functions that are specific to the device; for most functions, the minidriver calls the Microsoft class driver.</span></span>

<span data-ttu-id="ba447-107">В графе фильтра DirectShow любое устройство записи WDM отображается как фильтр [записи видео WDM](wdm-video-capture-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="ba447-107">In a DirectShow filter graph, any WDM capture device appears as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="ba447-108">Фильтр записи видео WDM настраивается на основе характеристик драйвера.</span><span class="sxs-lookup"><span data-stu-id="ba447-108">The WDM Video Capture filter configures itself based on the characteristics of the driver.</span></span> <span data-ttu-id="ba447-109">Он отображается под именем, предоставленным драйвером, поэтому фильтр с названием «фильтр видеозаписи WDM» в любом месте графа не будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="ba447-109">It appears under a name provided by the driver — you will not see a filter called "WDM Video Capture Filter" anywhere in the graph.</span></span>

<span data-ttu-id="ba447-110">Некоторые устаревшие устройства записи по-прежнему используют драйверы Video для Windows (VFW).</span><span class="sxs-lookup"><span data-stu-id="ba447-110">Some older capture devices still use Video for Windows (VFW) drivers.</span></span> <span data-ttu-id="ba447-111">Несмотря на то что эти драйверы устарели, они поддерживаются в DirectShow с помощью фильтра [записи VFW](vfw-capture-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="ba447-111">Although these drivers are now obsolete, they are supported in DirectShow through the [VFW Capture](vfw-capture-filter.md) filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba447-112">См. также</span><span class="sxs-lookup"><span data-stu-id="ba447-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba447-113">Сведения о записи видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="ba447-113">About Video Capture in DirectShow</span></span>](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



