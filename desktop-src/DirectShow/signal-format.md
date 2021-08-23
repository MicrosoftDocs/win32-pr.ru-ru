---
description: Формат сигнала
ms.assetid: 8684972c-3233-49bf-8c34-ca644aca432a
title: Формат сигнала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66add7467f2f497985094c603aaea83b55967f6b2c07eba4cacde080503ef2e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583184"
---
# <a name="signal-format"></a>Формат сигнала

Формат сигнала для видеокамеры — NTSC или PAL, Standard или Long-Play.

**Драйвер МСДВ**

Чтобы получить формат входных сигналов из драйвера МСДВ, вызовите метод [**иамексттранспорт:: жеттранспортбасикпараметерс**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) и передайте флаг "ED \_ \_ input Signal" \_ . Метод возвращает определенную константу, указывающую формат.

Следующий код проверяет формат сигнала и использует это значение для вычисления среднего времени каждого кадра. Режим переменной получает константу формата сигнала.


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



Чтобы получить формат выходного сигнала, вызовите тот же метод с \_ \_ флагом "ED Output SignalR" \_ .

**Драйвер УВК**

Чтобы получить формат входного или выходного сигнала из драйвера УВК, вызовите [**иамстреамконфиг::**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) в ПИН-коде и изучите блок формата видео. (Для устройств УВК код, показанный в предыдущем примере, обычно возвращает ED \_ . ОСНОВНОЙ \_ сигнал \_ неизвестен, поэтому он не является надежным.)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Управление видеокамерой](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



