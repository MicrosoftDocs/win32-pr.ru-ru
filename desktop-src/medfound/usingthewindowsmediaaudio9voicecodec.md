---
description: Использование кодека Windows Media Audio Voice
ms.assetid: 771acb04-33a4-4ea3-8f50-e5e3dbdf9495
title: Использование кодека Windows Media Audio Voice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d636bd97b76e23acc6b68da87c8a206b17dea60a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547314"
---
# <a name="using-the-windows-media-audio-voice-codec"></a><span data-ttu-id="ef0f3-103">Использование кодека Windows Media Audio Voice</span><span class="sxs-lookup"><span data-stu-id="ef0f3-103">Using the Windows Media Audio Voice Codec</span></span>

<span data-ttu-id="ef0f3-104">Кодек Windows Media Audio Voice обеспечивает небольшое сжатие с низкой скоростью, оптимизированное для звука, содержащего речь.</span><span class="sxs-lookup"><span data-stu-id="ef0f3-104">The Windows Media Audio Voice codec provides low bit-rate compression optimized for audio containing speech.</span></span> <span data-ttu-id="ef0f3-105">Создание таких небольших образцов с помощью кодека обусловлено ограниченной частотой звучания звука человеческого голоса.</span><span class="sxs-lookup"><span data-stu-id="ef0f3-105">The ability of the codec to produce such small samples is due to the limited frequency range of the sounds of the human voice.</span></span> <span data-ttu-id="ef0f3-106">Такая оптимизация означает, что выделенный речевой кодировщик создает плохое качество вывода содержимого, содержащего более сложные звуки, например музыку.</span><span class="sxs-lookup"><span data-stu-id="ef0f3-106">This optimization means that a dedicated voice encoder creates poor-quality output for content that contains more complicated sounds, like music.</span></span> <span data-ttu-id="ef0f3-107">Однако кодек Windows Media Audio Voice компенсирует возможные проблемы с качеством, предоставляя отдельные режимы для голосовой связи, музыки и смешанного содержимого.</span><span class="sxs-lookup"><span data-stu-id="ef0f3-107">However, the Windows Media Audio Voice codec compensates for this potential quality issue by providing separate modes for voice, music, and mixed content.</span></span> <span data-ttu-id="ef0f3-108">Кодек анализирует смешанное содержимое, чтобы определить, какой режим следует использовать для каждой части файла.</span><span class="sxs-lookup"><span data-stu-id="ef0f3-108">The codec analyzes mixed content to determine which mode to use for each portion of the file.</span></span>

<span data-ttu-id="ef0f3-109">Кодек Windows Media Audio Voice реализован в объекте кодировщика, определяемом идентификатором класса CLSID \_ CWMSPEncMediaObject2, и в объекте декодера, определяемом идентификатором класса CLSID \_ квмспдекмедиаобжект.</span><span class="sxs-lookup"><span data-stu-id="ef0f3-109">The Windows Media Audio Voice codec is implemented in the encoder object identified by the class identifier CLSID\_CWMSPEncMediaObject2, and in the decoder object identified by the class identifier CLSID\_CWMSPDecMediaObject.</span></span> <span data-ttu-id="ef0f3-110">Тег Format типов мультимедиа, использующих этот кодек, — 0x00.</span><span class="sxs-lookup"><span data-stu-id="ef0f3-110">The format tag of media types using this codec is 0x00A.</span></span>

## <a name="configuring-the-encoder"></a><span data-ttu-id="ef0f3-111">Настройка кодировщика</span><span class="sxs-lookup"><span data-stu-id="ef0f3-111">Configuring the Encoder</span></span>

<span data-ttu-id="ef0f3-112">Голосовый кодировщик поддерживает три режима: речь, музыка и смешанные.</span><span class="sxs-lookup"><span data-stu-id="ef0f3-112">The voice encoder supports three modes: speech, music, and mixed.</span></span> <span data-ttu-id="ef0f3-113">Каждый режим оптимизирован для получения наилучших результатов для этого типа содержимого.</span><span class="sxs-lookup"><span data-stu-id="ef0f3-113">Each mode is optimized to get the best results for that type of content.</span></span> <span data-ttu-id="ef0f3-114">Вы можете настроить режим работы речевого кодировщика с помощью методов **ипропертисторе** , чтобы задать свойство [мфпкэй \_ вмавоице \_ ENC \_ мусикспичклассмоде](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="ef0f3-114">You can configure the mode of the voice encoder by using the methods of **IPropertyStore** to set the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property.</span></span>

<span data-ttu-id="ef0f3-115">При настройке смешанного содержимого кодек Windows Media Audio Voice будет автоматически обнаруживать фрагменты музыки в содержимом.</span><span class="sxs-lookup"><span data-stu-id="ef0f3-115">When configured for mixed content, the Windows Media Audio Voice codec will automatically detect passages of music in the content.</span></span> <span data-ttu-id="ef0f3-116">Если результаты не удовлетворены, можно указать расположение музыки в содержимом с помощью списка решений для редактирования (ЕДЛ).</span><span class="sxs-lookup"><span data-stu-id="ef0f3-116">If you are not satisfied with the results, you can specify the location of music in the content using an editing decision list (EDL).</span></span> <span data-ttu-id="ef0f3-117">Дополнительные сведения см. в разделе [Использование списка решений для изменения кодировки голоса](usingavoiceeditingdecisionlist.md).</span><span class="sxs-lookup"><span data-stu-id="ef0f3-117">For more information, see [Using an Editing Decision List for Encoding Voice](usingavoiceeditingdecisionlist.md).</span></span>

<span data-ttu-id="ef0f3-118">В отличие от других звуковых кодировщиков, можно задать значение окна буфера для голосового содержимого с помощью свойства [мфпкэй \_ вмавоице \_ ENC \_ буффервиндов](mfpkey-wmavoice-enc-bufferwindowproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="ef0f3-118">Unlike the other audio encoders, you can set the buffer window value for voice content by using the [MFPKEY\_WMAVOICE\_ENC\_BufferWindow](mfpkey-wmavoice-enc-bufferwindowproperty.md) property.</span></span> <span data-ttu-id="ef0f3-119">Однако в большинстве случаев значения по умолчанию должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="ef0f3-119">However, the default values should work fine in most cases.</span></span>

> [!Note]  
>    <span data-ttu-id="ef0f3-120">При настройке речевого кодировщика очень важно задать тип выходных данных перед установкой входного типа.</span><span class="sxs-lookup"><span data-stu-id="ef0f3-120">When configuring the voice encoder, it is very important that you set the output type before you set the input type.</span></span> <span data-ttu-id="ef0f3-121">Это рекомендуемый порядок операций для всех аудиокодеков, но голосовый кодировщик может сообщать ошибочные типы вывода, если входные данные задаются при вызове **имедиаобжект:: жетаутпуттипе** или **Имфтрансформ:: жетаутпуттипе**.</span><span class="sxs-lookup"><span data-stu-id="ef0f3-121">This is the recommended order of operations for all of the audio codecs, but the voice encoder can report erroneous output types if an input is set when you call **IMediaObject::GetOutputType** or **IMFTransform::GetOutputType**.</span></span>

 

## <a name="decoding"></a><span data-ttu-id="ef0f3-122">Декодирование</span><span class="sxs-lookup"><span data-stu-id="ef0f3-122">Decoding</span></span>

<span data-ttu-id="ef0f3-123">Специальные требования для декодирования голосовых аудио отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="ef0f3-123">There are no special requirements for decoding voice audio.</span></span> <span data-ttu-id="ef0f3-124">Дополнительные сведения см. в разделе [Настройка декодирования звука](configuringaudiodecoding.md).</span><span class="sxs-lookup"><span data-stu-id="ef0f3-124">Form more information, see [Configuring Audio Decoding](configuringaudiodecoding.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef0f3-125">См. также</span><span class="sxs-lookup"><span data-stu-id="ef0f3-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef0f3-126">Работа с аудио</span><span class="sxs-lookup"><span data-stu-id="ef0f3-126">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



