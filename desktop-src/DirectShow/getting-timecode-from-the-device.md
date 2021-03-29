---
description: Получение времени работы с устройства
ms.assetid: e3d06e0c-a595-4bc3-be62-168bd5122397
title: Получение времени работы с устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5787cf328214c1a266b7f129e4e517716b1d04f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105650420"
---
# <a name="getting-timecode-from-the-device"></a><span data-ttu-id="2d9ca-103">Получение времени работы с устройства</span><span class="sxs-lookup"><span data-stu-id="2d9ca-103">Getting Timecode from the Device</span></span>

<span data-ttu-id="2d9ca-104">Пока лента DV воспроизводится или находится в режиме паузы записей, вы можете получить код времени SMPTE или номер абсолютной записи.</span><span class="sxs-lookup"><span data-stu-id="2d9ca-104">While a DV tape is playing or is in record-pause mode, you can retrieve the SMPTE timecode or the absolute track number.</span></span> <span data-ttu-id="2d9ca-105">Для этого вызовите метод [**иамтимекодереадер:: жеттимекоде**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) .</span><span class="sxs-lookup"><span data-stu-id="2d9ca-105">To do this, call the [**IAMTimecodeReader::GetTimecode**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) method.</span></span> <span data-ttu-id="2d9ca-106">Этот метод принимает указатель на структуру [**\_ образца**](/windows/win32/api/strmif/ns-strmif-timecode_sample) времени, описывающую код времени.</span><span class="sxs-lookup"><span data-stu-id="2d9ca-106">This method takes a pointer to a [**TIMECODE\_SAMPLE**](/windows/win32/api/strmif/ns-strmif-timecode_sample) structure, which describes the timecode.</span></span> <span data-ttu-id="2d9ca-107">Перед вызовом метода инициализируйте элемент **dwFlags** структуры.</span><span class="sxs-lookup"><span data-stu-id="2d9ca-107">Before calling the method, initialize the **dwFlags** member of the structure.</span></span> <span data-ttu-id="2d9ca-108">Для получения кода времени \_ или значения ED девкап АТН Read используйте значение времени в виде ED девкап, чтобы \_ \_ \_ \_ \_ получить абсолютный номер записи.</span><span class="sxs-lookup"><span data-stu-id="2d9ca-108">Use the value ED\_DEVCAP\_TIMECODE\_READ to retrieve the timecode or the value ED\_DEVCAP\_ATN\_READ to retrieve the absolute track number.</span></span>

<span data-ttu-id="2d9ca-109">Элемент **времени в** **\_ образце временной** структуры имеет структуру времени.</span><span class="sxs-lookup"><span data-stu-id="2d9ca-109">The **timecode** member of the **TIMECODE\_SAMPLE** structure is a TIMECODE structure.</span></span> <span data-ttu-id="2d9ca-110">Когда метод возвращает значение, элемент **двфрамес** структуры кода времени содержит код времени или номер записи.</span><span class="sxs-lookup"><span data-stu-id="2d9ca-110">When the method returns, the **dwFrames** member of the TIMECODE structure contains the timecode or track number.</span></span> <span data-ttu-id="2d9ca-111">Для кода времени часы, минуты, секунды и кадры упаковываются в DWORD в виде двоичных значений Decimal (BCD) с форматом *ххммссфф*.</span><span class="sxs-lookup"><span data-stu-id="2d9ca-111">For timecode, the hours, minutes, seconds, and frames are packed into a DWORD as binary coded decimal (BCD) values, with the format *hhmmssff*.</span></span> <span data-ttu-id="2d9ca-112">Используйте битовые маски для извлечения отдельных значений.</span><span class="sxs-lookup"><span data-stu-id="2d9ca-112">Use bitmasks to extract the individual values.</span></span>

<span data-ttu-id="2d9ca-113">В следующем примере извлекается код времени и номер записи.</span><span class="sxs-lookup"><span data-stu-id="2d9ca-113">The following example retrieves the timecode and track number.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2d9ca-114">См. также</span><span class="sxs-lookup"><span data-stu-id="2d9ca-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d9ca-115">Управление видеокамерой</span><span class="sxs-lookup"><span data-stu-id="2d9ca-115">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 
