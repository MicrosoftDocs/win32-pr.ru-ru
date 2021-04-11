---
description: Настройка кодирования звука
ms.assetid: 40004f07-0b8c-49cd-9e17-1f6ad7604fbb
title: Настройка кодирования звука (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e47595f440d10ad0d3c5695f117204f357035d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262813"
---
# <a name="configuring-audio-encoding-microsoft-media-foundation"></a><span data-ttu-id="80d3e-103">Настройка кодирования звука (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="80d3e-103">Configuring Audio Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="80d3e-104">Кодировщик Windows Media Audio выполняет перечисление всех поддерживаемых типов вывода в своей полной форме.</span><span class="sxs-lookup"><span data-stu-id="80d3e-104">The Windows Media Audio encoder enumerates all of its supported output types in their complete form.</span></span> <span data-ttu-id="80d3e-105">Получите требуемый тип, вызвав **имедиаобжект:: жетаутпуттипе** или **Имфтрансформ:: жетаваилаблеаутпуттипе**, а затем установите извлеченный тип без изменений в качестве выходного типа, вызвав **Имедиаобжект:: Сетаутпуттипе** или **IMFTransform:: SetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="80d3e-105">Retrieve the type that you want by calling **IMediaObject::GetOutputType** or **IMFTransform::GetAvailableOutputType**, and then set the retrieved type, unaltered, as the output type by calling **IMediaObject::SetOutputType** or **IMFTransform::SetOutputType**.</span></span>

<span data-ttu-id="80d3e-106">Настраиваются типы выходных данных, поддерживаемые изменением аудио кодировщика в качестве свойств кодировщика.</span><span class="sxs-lookup"><span data-stu-id="80d3e-106">The output media types supported by the audio encoder change as encoder properties are configured.</span></span> <span data-ttu-id="80d3e-107">Перед перечислением типа выходных данных необходимо настроить все свойства кодировщика, которые вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="80d3e-107">You must configure all of the encoder properties you want to use before you enumerate the output type.</span></span>

<span data-ttu-id="80d3e-108">Звуковые кодировщики поддерживают режимы с двумя проходами и VBR, но настроены иначе, чем для видео.</span><span class="sxs-lookup"><span data-stu-id="80d3e-108">Two-pass and VBR modes are supported by the audio encoders, but are configured differently than for video.</span></span> <span data-ttu-id="80d3e-109">Дополнительные сведения см. в разделе [Перечисление типов аудио для конкретных режимов кодирования](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="80d3e-109">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="80d3e-110">Входные типы, поддерживаемые кодировщиком аудио, недоступны до тех пор, пока не будет задан тип выходных данных.</span><span class="sxs-lookup"><span data-stu-id="80d3e-110">The input types supported by the audio encoder are not available until you set the output type.</span></span> <span data-ttu-id="80d3e-111">При вызове **имедиаобжект:: жетинпуттипе** или **Имфтрансформ:: жетинпуттипе** перед настройкой выходного типа метод возвращает DMO \_ е \_ больше \_ \_ элементов или MFT \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="80d3e-111">If you call **IMediaObject::GetInputType** or **IMFTransform::GetInputType** before setting an output type, the method returns DMO\_E\_NO\_MORE\_ITEMS or MFT\_E\_NO\_MORE\_TYPES respectively.</span></span> <span data-ttu-id="80d3e-112">После установки типа выходных данных кодировщик перечисляет поддерживаемые типы входных данных для выбранного типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="80d3e-112">After the output type is set, the encoder enumerates the input types that it supports for the selected output type.</span></span>

<span data-ttu-id="80d3e-113">Не выполняется перевыборка звука с помощью кодировщика Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="80d3e-113">No audio resampling is performed by the Windows Media Audio encoder.</span></span> <span data-ttu-id="80d3e-114">Это означает, что тип выходных данных кодировщика и тип входных данных кодировщика должны иметь одинаковое количество каналов, бит на выборку и частоту выборки.</span><span class="sxs-lookup"><span data-stu-id="80d3e-114">This means that the encoder output type and the encoder input type must have the same number of channels, bits per sample, and sample rate.</span></span> <span data-ttu-id="80d3e-115">Дополнительные сведения см. в разделе [Поиск типов вывода звукового кодировщика](findingaudioencoderoutputtypes.md).</span><span class="sxs-lookup"><span data-stu-id="80d3e-115">For more information, see [Finding Audio Encoder Output Types](findingaudioencoderoutputtypes.md).</span></span>

> [!Note]  
>    <span data-ttu-id="80d3e-116">Каждый тип выходных данных, перечисленный кодировщиком аудио, содержит структуру **вавеформатекс** (на которую указывает **AM \_ Media \_ Type. пбформат**) с добавленными расширенными данными.</span><span class="sxs-lookup"><span data-stu-id="80d3e-116">Each output type enumerated by the audio encoder contains a **WAVEFORMATEX** structure (pointed to by **AM\_MEDIA\_TYPE.pbFormat**) with extended data appended to it.</span></span> <span data-ttu-id="80d3e-117">Размер расширенных данных задается параметром **вавеформатекс. кбсизе**.</span><span class="sxs-lookup"><span data-stu-id="80d3e-117">The size of the extended data is specified by **WAVEFORMATEX.cbSize**.</span></span> <span data-ttu-id="80d3e-118">Эти данные должны храниться в закодированном содержимом, чтобы их можно было доставить декодеру.</span><span class="sxs-lookup"><span data-stu-id="80d3e-118">This data must be kept with the encoded content so that it can be delivered to the decoder.</span></span> <span data-ttu-id="80d3e-119">Содержимое не может быть распаковано без данных расширенного формата.</span><span class="sxs-lookup"><span data-stu-id="80d3e-119">The content cannot be decompressed without the extended format data.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="80d3e-120">См. также</span><span class="sxs-lookup"><span data-stu-id="80d3e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80d3e-121">Работа с аудио</span><span class="sxs-lookup"><span data-stu-id="80d3e-121">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



