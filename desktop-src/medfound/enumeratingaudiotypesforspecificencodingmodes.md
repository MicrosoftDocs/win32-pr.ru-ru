---
description: Перечисление типов аудио для конкретных режимов кодирования
ms.assetid: d44960eb-da5e-4379-ba9d-cb804559dc53
title: Перечисление типов аудио для конкретных режимов кодирования (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16a8b97afdd48cb1d7828f80778aa9fcf8dc1ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423537"
---
# <a name="enumerating-audio-types-for-specific-encoding-modes-microsoft-media-foundation"></a><span data-ttu-id="371f4-103">Перечисление типов аудио для конкретных режимов кодирования (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="371f4-103">Enumerating Audio Types for Specific Encoding Modes (Microsoft Media Foundation)</span></span>

<span data-ttu-id="371f4-104">Типы входных и выходных носителей, принимаемые звуковым кодировщиком, очень структурированы.</span><span class="sxs-lookup"><span data-stu-id="371f4-104">The input and output media types accepted by the audio encoder are very structured.</span></span> <span data-ttu-id="371f4-105">Для получения поддерживаемых типов выходных данных необходимо вызвать метод **имедиаобжект:: жетаутпуттипе** или **Имфтрансформ:: жетаутпуттипе**.</span><span class="sxs-lookup"><span data-stu-id="371f4-105">You must obtain supported output types by calling **IMediaObject::GetOutputType** method or **IMFTransform::GetOutputType**.</span></span> <span data-ttu-id="371f4-106">После получения типа выходных данных его не следует изменять.</span><span class="sxs-lookup"><span data-stu-id="371f4-106">After you get an output type, you must not alter it.</span></span>

<span data-ttu-id="371f4-107">Если вы хотите использовать режим кодирования, отличный от однопроходного CBR, необходимо установить режим, а затем перечислить типы выходных данных для этого режима. кодировщик изменяет Поддерживаемые типы выходных данных в зависимости от набора режимов.</span><span class="sxs-lookup"><span data-stu-id="371f4-107">If you want to use an encoding mode other than one-pass CBR, you must set the mode and then enumerate the output types for that mode; the encoder changes the supported output types depending upon the mode set.</span></span> <span data-ttu-id="371f4-108">Свойства, управляющие режимом кодирования, — это [**мфпкэй \_ Вбренаблед**](mfpkey-vbrenabledproperty.md) и [**мфпкэй \_ пассесусед**](mfpkey-passesusedproperty.md).</span><span class="sxs-lookup"><span data-stu-id="371f4-108">The properties that control the encoding mode are [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) and [**MFPKEY\_PASSESUSED**](mfpkey-passesusedproperty.md).</span></span> <span data-ttu-id="371f4-109">Если режим задан в кодировщике, необходимо перечислить и выбрать тип выходных данных, используя его без изменения, как и в случае с CBR.</span><span class="sxs-lookup"><span data-stu-id="371f4-109">When the mode is set in the encoder, you must enumerate and select an output type, using it without alteration, just as with CBR.</span></span>

## <a name="identifying-quality-based-vbr-types"></a><span data-ttu-id="371f4-110">Определение типов VBR с учетом качества</span><span class="sxs-lookup"><span data-stu-id="371f4-110">Identifying Quality Based VBR Types</span></span>

<span data-ttu-id="371f4-111">Процедура идентификации типов VBR с учетом качества зависит от того, выступает ли кодировщик в качестве объекта мультимедиа DirectX (DMO) или выступает в качестве Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="371f4-111">The procedure for identifying quality based VBR types depends on whether the encoder is acting as a DirectX Media Object (DMO) or acting as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="371f4-112">Сведения о том, когда кодировщик выступает в качестве DMO или MFT, см. на страницах справочника по отдельным кодекам в разделе [объекты кодека](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="371f4-112">For information on when an encoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="371f4-113">Если звуковый кодировщик выступает в роли DMO и вы настраиваете кодировщик для использования однопроходных VBR, он перечисляет все поддерживаемые типы вывода.</span><span class="sxs-lookup"><span data-stu-id="371f4-113">When an audio encoder is acting as a DMO and you configure the encoder to use one-pass VBR, it enumerates all of the supported output types.</span></span> <span data-ttu-id="371f4-114">Тем не менее, как правило, необходимо выбрать один тип VBR на основе параметра Quality.</span><span class="sxs-lookup"><span data-stu-id="371f4-114">However, you will typically want to select a one-pass VBR type based on the quality parameter.</span></span> <span data-ttu-id="371f4-115">Кодировщик помещает значение качества для однопроходных выходных типов VBR в элемент **навгбитесперсек** структуры **вавеформатекс** , на который указывает **\_ тип носителя DMO \_ . пбформат**.</span><span class="sxs-lookup"><span data-stu-id="371f4-115">The encoder puts the quality value for one-pass VBR output types in the **nAvgBytesPerSec** member of the **WAVEFORMATEX** structure pointed to by **DMO\_MEDIA\_TYPE.pbFormat**.</span></span>

<span data-ttu-id="371f4-116">Это значение хранится в следующем формате: 0x7FFFFFXX, где XX — это значение качества (от 0 до 100).</span><span class="sxs-lookup"><span data-stu-id="371f4-116">This value is stored in the following format: 0x7FFFFFXX, where XX is the quality value (from 0 to 100).</span></span> <span data-ttu-id="371f4-117">Например, значение **навгбитесперсек** в 0x7FFFFF62 указывает уровень качества 98 (0x62 = 98).</span><span class="sxs-lookup"><span data-stu-id="371f4-117">For example, the **nAvgBytesPerSec** value of 0x7FFFFF62 specifies quality level 98 (0x62 = 98).</span></span>

<span data-ttu-id="371f4-118">В следующем примере показано, как проверить уровень качества в формате, когда кодировщик выступает в роли DMO.</span><span class="sxs-lookup"><span data-stu-id="371f4-118">The following example shows how to check the quality level of a format when the encoder is acting as a DMO.</span></span>


```
void ShowQuality(WAVEFORMATEX* pWave)
{
    // Store the average bytes per second in a local variable
    // with a more manageable name.
    DWORD dwBps = pWave->nAvgBytesPerSec;

    // Verify that the value is a VBR quality level by using 
    // a bitmask to check for the bit pattern 0x7FFFFFXX. 
    if(dwBps & 0x7FFFFF00 == 0x7FFFFF00)
        printf("VBR Quality: %d%%\n",(dwBps & 0x000000FF));
    else // Not a valid VBR quality value.
        printf("Not a valid one-pass VBR audio format.\n");
}
```



<span data-ttu-id="371f4-119">Когда кодировщик выступает в качестве MFT и перечисляет тип выходных данных при вызове **жетаваилаблеаутпуттипе**, можно запросить таблицу MFT для **мфпкэй \_ последнего \_ \_ перечисленного свойства \_ вбркуалити** .</span><span class="sxs-lookup"><span data-stu-id="371f4-119">When the encoder is acting as an MFT and it enumerates an output type on a call to **GetAvailableOutputType**, you can query the MFT for the **MFPKEY\_MOST\_RECENTLY\_ENUMERATED\_VBRQUALITY** property.</span></span> <span data-ttu-id="371f4-120">Возвращаемое значение указывает качество VBR последнего возвращенного типа выходного носителя.</span><span class="sxs-lookup"><span data-stu-id="371f4-120">The value returned indicates the VBR quality of the most recently returned output media type.</span></span> <span data-ttu-id="371f4-121">Затем это значение можно использовать для задания свойства [**мфпкэй \_ требуемого \_ вбркуалити**](mfpkey-desired-vbrqualityproperty.md) кодировщика.</span><span class="sxs-lookup"><span data-stu-id="371f4-121">Then you can use that value to set the [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) property of the encoder.</span></span>

## <a name="setting-peak-constraints"></a><span data-ttu-id="371f4-122">Настройка ограничений пиковой нагрузки</span><span class="sxs-lookup"><span data-stu-id="371f4-122">Setting Peak Constraints</span></span>

<span data-ttu-id="371f4-123">Для уровня с VBR (однопроходный) и с неограниченными двумя проходами VBR дополнительные параметры не требуются после получения выходного типа.</span><span class="sxs-lookup"><span data-stu-id="371f4-123">For quality based VBR (one-pass) and unconstrained two-pass VBR, no additional settings are required after retrieving the output type.</span></span> <span data-ttu-id="371f4-124">Чтобы использовать пиковую нагрузку, извлеките выходной тип с поддержкой VBR и двумя наборами проходов.</span><span class="sxs-lookup"><span data-stu-id="371f4-124">To use peak-constrained VBR, retrieve an output type with VBR enabled and two passes set.</span></span> <span data-ttu-id="371f4-125">Этот тип, без изменения, описывает параметры с неограниченными VBR.</span><span class="sxs-lookup"><span data-stu-id="371f4-125">This type, without alteration, describes unconstrained VBR settings.</span></span> <span data-ttu-id="371f4-126">Чтобы задать ограничения пиковой нагрузки, задайте свойства [мфпкэй \_ Рмакс](mfpkey-rmaxproperty.md) и [мфпкэй \_ бмакс](mfpkey-bmaxproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="371f4-126">To set peak constraints, set the [MFPKEY\_RMAX](mfpkey-rmaxproperty.md) and [MFPKEY\_BMAX](mfpkey-bmaxproperty.md) properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="371f4-127">См. также</span><span class="sxs-lookup"><span data-stu-id="371f4-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="371f4-128">Настройка кодирования звука</span><span class="sxs-lookup"><span data-stu-id="371f4-128">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> <dt>

[<span data-ttu-id="371f4-129">Поиск типов вывода звукового кодировщика</span><span class="sxs-lookup"><span data-stu-id="371f4-129">Finding Audio Encoder Output Types</span></span>](findingaudioencoderoutputtypes.md)
</dt> <dt>

[<span data-ttu-id="371f4-130">Использование кодировки Two-Pass</span><span class="sxs-lookup"><span data-stu-id="371f4-130">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
</dt> <dt>

[<span data-ttu-id="371f4-131">Использование кодирования VBR</span><span class="sxs-lookup"><span data-stu-id="371f4-131">Using VBR Encoding</span></span>](usingvbrencoding.md)
</dt> </dl>

 

 



