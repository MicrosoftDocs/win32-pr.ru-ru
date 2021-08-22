---
description: Получение времени работы с устройства
ms.assetid: e3d06e0c-a595-4bc3-be62-168bd5122397
title: Получение времени работы с устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265769300c0134ec9f3b3635ada3e595205e8452ced262d4062f9fb6cdaaadc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564734"
---
# <a name="getting-timecode-from-the-device"></a>Получение времени работы с устройства

Пока лента DV воспроизводится или находится в режиме паузы записей, вы можете получить код времени SMPTE или номер абсолютной записи. Для этого вызовите метод [**иамтимекодереадер:: жеттимекоде**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) . Этот метод принимает указатель на структуру [**\_ образца**](/windows/win32/api/strmif/ns-strmif-timecode_sample) времени, описывающую код времени. Перед вызовом метода инициализируйте элемент **dwFlags** структуры. Для получения кода времени \_ или значения ED девкап АТН Read используйте значение времени в виде ED девкап, чтобы \_ \_ \_ \_ \_ получить абсолютный номер записи.

Элемент **времени в** **\_ образце временной** структуры имеет структуру времени. Когда метод возвращает значение, элемент **двфрамес** структуры кода времени содержит код времени или номер записи. Для кода времени часы, минуты, секунды и кадры упаковываются в DWORD в виде двоичных значений Decimal (BCD) с форматом *ххммссфф*. Используйте битовые маски для извлечения отдельных значений.

В следующем примере извлекается код времени и номер записи.


```C++
if (MyDevCap.bHasTimecode)
{
    TIMECODE_SAMPLE TimecodeSample;
    TimecodeSample.timecode.dwFrames = 0;
    char szBuf[32];

    TimecodeSample.dwFlags = ED_DEVCAP_TIMECODE_READ;
    if (hr = MyDevCap.pTimecode->GetTimecode(&TimecodeSample),  SUCCEEDED(hr)) 
    {
        DWORD dwTime = TimecodeSample.timecode.dwFrames; // Packed BCD value.
        int hour  = ((dwTime & 0x0F000000) >> 24) + 
                    (10 * ((dwTime & 0xF0000000) >> 28));
        int min   = ((dwTime & 0x0F0000) >> 16) + 
                    (10 * ((dwTime & 0xF00000) >> 20));
        int sec   = ((dwTime & 0x0F00) >> 8) + 
                    (10 * ((dwTime & 0xF000) >> 12));
        int frame = (dwTime & 0x0F) + 
                    (10 * ((dwTime & 0xF0) >> 4));
    }

    TimecodeSample.dwFlags = ED_DEVCAP_ATN_READ;
    if (hr = MyDevCap.pTimecode->GetTimecode(&TimecodeSample), SUCCEEDED(hr)) 
    {
        DWORD dwTrackNumber = TimecodeSample.timecode.dwFrames;
    }
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Управление видеокамерой](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 
