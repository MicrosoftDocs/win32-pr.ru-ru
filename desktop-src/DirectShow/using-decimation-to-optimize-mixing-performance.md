---
description: Использование децимации для оптимизации смешанной производительности
ms.assetid: 94d4ce86-9d60-4fd4-ab01-851dc073680b
title: Использование децимации для оптимизации смешанной производительности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e9e4ddfe3bbba3eb5eeab91b7cf0e8b9cbfa03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911076"
---
# <a name="using-decimation-to-optimize-mixing-performance"></a><span data-ttu-id="06726-103">Использование децимации для оптимизации смешанной производительности</span><span class="sxs-lookup"><span data-stu-id="06726-103">Using Decimation to Optimize Mixing Performance</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06726-104">Оптимизация, описанная в этом разделе, сильно зависит от базового оборудования.</span><span class="sxs-lookup"><span data-stu-id="06726-104">The optimization described in this section is highly dependent on the underlying hardware.</span></span> <span data-ttu-id="06726-105">Если вы не можете гарантировать, какой тип графического оборудования будет использоваться для приложения, это может серьезно понизить внешний вид видеоизображения.</span><span class="sxs-lookup"><span data-stu-id="06726-105">Unless you can guarantee what type of graphics hardware will be used with the application, it may seriously degrade the appearance of the video image.</span></span>

 

<span data-ttu-id="06726-106">ТВВЧ требует большого объема вычислительной мощности, что в более новых системах предоставляется в основном графической картой.</span><span class="sxs-lookup"><span data-stu-id="06726-106">HDTV requires a lot of processing power, which on newer systems is provided mostly by the graphics card.</span></span> <span data-ttu-id="06726-107">Но даже если графическая карта и декодер поддерживают разрешение 1920 x 1080, у пользователя может не всегда быть установлен для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="06726-107">But even if the graphics card and the decoder can support resolutions of 1920x1080, the user may not always have their monitor set to this resolution.</span></span> <span data-ttu-id="06726-108">В этом случае графическая микросхема требуется для создания изображения 1920 x 1080, а затем уменьшите разрешение перед отправкой в буфер кадров.</span><span class="sxs-lookup"><span data-stu-id="06726-108">In this case, the graphics chip is required to create a 1920 x 1080 image, and then reduce the resolution before sending it to the frame buffer.</span></span>

<span data-ttu-id="06726-109">Так как это потеря вычислительной мощности, VMR предоставляет способ децимации (уменьшить) изображение на момент подготовки к просмотру на поверхности DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="06726-109">Since this is a waste of processing power, the VMR provides a way to decimate (reduce) the image at the time it is being rendered onto the DirectDraw surface.</span></span> <span data-ttu-id="06726-110">Это исключает необходимость копирования дополнительной памяти, если необходимо изменить размер изображения после его подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="06726-110">This eliminates the extra memory copy required if the image has to be resized after it has been rendered.</span></span>

<span data-ttu-id="06726-111">**VMR-7:** Чтобы включить децимации, вызовите [**ивмрмиксерконтрол:: сетмиксингпрефс**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) с \_ флагом миксерпреф деЦиматеаутпут.</span><span class="sxs-lookup"><span data-stu-id="06726-111">**VMR-7:** To enable decimation, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) with the MixerPref\_DecimateOutput flag.</span></span>

<span data-ttu-id="06726-112">**VMR-9:** Чтобы включить децимации, вызовите [**IVMRMixerControl9:: сетмиксингпрефс**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) с \_ флагом MixerPref9 деЦиматеаутпут.</span><span class="sxs-lookup"><span data-stu-id="06726-112">**VMR-9:** To enable decimation, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_DecimateOutput flag.</span></span>

<span data-ttu-id="06726-113">Перед подключением VMR необходимо вызвать метод **сетмиксингпрефс** .</span><span class="sxs-lookup"><span data-stu-id="06726-113">The **SetMixingPrefs** method must be called before the VMR is connected.</span></span> <span data-ttu-id="06726-114">Флаги предпочтений смешивание нельзя изменить после выполнения графа.</span><span class="sxs-lookup"><span data-stu-id="06726-114">The mixing preference flags cannot be changed once the graph is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06726-115">См. также</span><span class="sxs-lookup"><span data-stu-id="06726-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06726-116">Использование режима смешения VMR</span><span class="sxs-lookup"><span data-stu-id="06726-116">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



