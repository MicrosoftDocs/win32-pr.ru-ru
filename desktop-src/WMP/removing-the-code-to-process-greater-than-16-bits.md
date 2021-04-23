---
title: Удаление кода для обработки более чем 16 бит
description: Удаление кода для обработки более чем 16 бит
ms.assetid: 90c165e1-bc77-42a5-878d-056762c62991
keywords:
- Подключаемые модули проигрывателя Windows Media, метод Echo Sample Допроцессаутпут
- подключаемые модули, метод Echo Sample Допроцессаутпут
- подключаемые модули обработки цифровых сигналов, метод Echo Sample Допроцессаутпут
- Подключаемые модули DSP, метод Echo Sample Допроцессаутпут
- Пример подключаемого модуля Echo DSP, метод Допроцессаутпут
- Пример подключаемого модуля Echo DSP с обработкой более 16 бит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec33332ee332d0ca7b615844ba8ad5cd7b00eb2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888419"
---
# <a name="removing-the-code-to-process-greater-than-16-bits"></a><span data-ttu-id="0f568-109">Удаление кода для обработки более чем 16 бит</span><span class="sxs-lookup"><span data-stu-id="0f568-109">Removing the Code to Process Greater than 16 Bits</span></span>

<span data-ttu-id="0f568-110">Поскольку в этом примере обрабатывается только 8-разрядный или 16-разрядный звук, необходимо изменить код в **цечо:: валидатемедиатипе** , чтобы вернуть \_ тип DMO E \_ \_ не \_ принято для типов мультимедиа, превышающих 16 бит.</span><span class="sxs-lookup"><span data-stu-id="0f568-110">Because this sample only processes 8-bit or 16-bit audio, you need to modify the code in **CEcho::ValidateMediaType** to return DMO\_E\_TYPE\_NOT\_ACCEPTED for media types greater than 16 bits.</span></span> <span data-ttu-id="0f568-111">Для этого необходимо изменить код в блоке switch, который проверяет форматы типа "волна" в \_ \_ расширяемом формате.</span><span class="sxs-lookup"><span data-stu-id="0f568-111">To accomplish this, you must change the code in the switch block that tests formats of type WAVE\_FORMAT\_EXTENSIBLE.</span></span> <span data-ttu-id="0f568-112">Замените код мастера следующим кодом:</span><span class="sxs-lookup"><span data-stu-id="0f568-112">Replace the wizard code with the following example code:</span></span>


```C++
case WAVE_FORMAT_EXTENSIBLE:
    {
         // Sample size is greater than 16-bit or is multichannel.
        WAVEFORMATEXTENSIBLE *pWaveXT = (WAVEFORMATEXTENSIBLE *) pWave;

        if (KSDATAFORMAT_SUBTYPE_PCM != pWaveXT->SubFormat)
        {
            return DMO_E_TYPE_NOT_ACCEPTED;
        }
    }
    break;

```



<span data-ttu-id="0f568-113">Затем удалите или закомментируйте разделы кода в **допроцессаутпут** , которые обрабатывали аудио с высоким битом разрешения.</span><span class="sxs-lookup"><span data-stu-id="0f568-113">Next, delete or comment out the sections of code in **DoProcessOutput** that handle high bit resolution audio.</span></span> <span data-ttu-id="0f568-114">Ниже приведены разделы, которые начинаются с варианта 24 и регистра 32.</span><span class="sxs-lookup"><span data-stu-id="0f568-114">These are the sections that begin with case 24 and case 32.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f568-115">См. также</span><span class="sxs-lookup"><span data-stu-id="0f568-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f568-116">**Реализация Цечо::D Опроцессаутпут**</span><span class="sxs-lookup"><span data-stu-id="0f568-116">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




