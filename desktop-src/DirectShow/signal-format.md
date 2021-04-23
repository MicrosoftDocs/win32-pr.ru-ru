---
description: Формат сигнала
ms.assetid: 8684972c-3233-49bf-8c34-ca644aca432a
title: Формат сигнала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6983328729e0dc72d93c0e00a74e7e65a7f237
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894765"
---
# <a name="signal-format"></a><span data-ttu-id="78382-103">Формат сигнала</span><span class="sxs-lookup"><span data-stu-id="78382-103">Signal Format</span></span>

<span data-ttu-id="78382-104">Формат сигнала для видеокамеры — NTSC или PAL, Standard или Long-Play.</span><span class="sxs-lookup"><span data-stu-id="78382-104">A DV camcorder's signal format can be NTSC or PAL, standard or long-play.</span></span>

<span data-ttu-id="78382-105">**Драйвер МСДВ**</span><span class="sxs-lookup"><span data-stu-id="78382-105">**MSDV Driver**</span></span>

<span data-ttu-id="78382-106">Чтобы получить формат входных сигналов из драйвера МСДВ, вызовите метод [**иамексттранспорт:: жеттранспортбасикпараметерс**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) и передайте флаг "ED \_ \_ input Signal" \_ .</span><span class="sxs-lookup"><span data-stu-id="78382-106">To get the input signal format from the MSDV driver, call the [**IAMExtTransport::GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) method and pass in the ED\_TRANSBASIC\_INPUT\_SIGNAL flag.</span></span> <span data-ttu-id="78382-107">Метод возвращает определенную константу, указывающую формат.</span><span class="sxs-lookup"><span data-stu-id="78382-107">The method returns a defined constant, indicating the format.</span></span>

<span data-ttu-id="78382-108">Следующий код проверяет формат сигнала и использует это значение для вычисления среднего времени каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="78382-108">The following code checks the signal format, and uses this value to calculates the average time per frame.</span></span> <span data-ttu-id="78382-109">Режим переменной получает константу формата сигнала.</span><span class="sxs-lookup"><span data-stu-id="78382-109">The variable Mode receives the signal-format constant.</span></span>


```C++
LONG Mode, AvgTimePerFrame;
hr = MyDevCap.pTransport->GetTransportBasicParameters(
        ED_TRANSBASIC_INPUT_SIGNAL, &Mode, NULL);
if (SUCCEEDED(hr))
{
    switch (Mode)
    {
    case ED_TRANSBASIC_SIGNAL_525_60_SD: // NTSC SD
        AvgTimePerFrame = 33;  // 33 msec (29.97 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_525_60_SDL: // NTSC SDL
        AvgTimePerFrame = 33;  
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SD: // PAL SD
        AvgTimePerFrame = 40;  // 40 msec (25 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SDL: // PAL SDL
        AvgTimePerFrame = 40;  
        break;
    default: 
        // Unknown type
        AvgTimePerFrame = 33; // Default
        break;
    }
}
```



<span data-ttu-id="78382-110">Чтобы получить формат выходного сигнала, вызовите тот же метод с \_ \_ флагом "ED Output SignalR" \_ .</span><span class="sxs-lookup"><span data-stu-id="78382-110">To get the output signal format, call the same method with the ED\_TRANSBASIC\_OUTPUT\_SIGNAL flag.</span></span>

<span data-ttu-id="78382-111">**Драйвер УВК**</span><span class="sxs-lookup"><span data-stu-id="78382-111">**UVC Driver**</span></span>

<span data-ttu-id="78382-112">Чтобы получить формат входного или выходного сигнала из драйвера УВК, вызовите [**иамстреамконфиг::**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) в ПИН-коде и изучите блок формата видео.</span><span class="sxs-lookup"><span data-stu-id="78382-112">To get the input or output signal format from the UVC driver, call [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) on the pin and examine the video format block.</span></span> <span data-ttu-id="78382-113">(Для устройств УВК код, показанный в предыдущем примере, обычно возвращает ED \_ . ОСНОВНОЙ \_ сигнал \_ неизвестен, поэтому он не является надежным.)</span><span class="sxs-lookup"><span data-stu-id="78382-113">(For UVC devices, the code shown in the previous example usually returns ED\_TRANSBASIC\_SIGNAL\_UNKNOWN, so it is not reliable.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="78382-114">См. также</span><span class="sxs-lookup"><span data-stu-id="78382-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78382-115">Управление видеокамерой</span><span class="sxs-lookup"><span data-stu-id="78382-115">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



