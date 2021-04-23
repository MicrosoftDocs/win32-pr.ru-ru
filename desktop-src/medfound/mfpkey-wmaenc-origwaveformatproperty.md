---
description: Указывает структуру ВАВЕФОРМАТЕКС, описывающую входное звуковое содержимое.
ms.assetid: d424f243-5ad6-46f2-b99b-9bb780715e8a
title: Свойство MFPKEY_WMAENC_ORIGWAVEFORMAT (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3475e5578124b8f0a762beddf713f701a5695110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263900"
---
# <a name="mfpkey_wmaenc_origwaveformat-property"></a><span data-ttu-id="1062b-103">МФПКЭЙ \_ вмаенк \_ Оригвавеформат, свойство</span><span class="sxs-lookup"><span data-stu-id="1062b-103">MFPKEY\_WMAENC\_ORIGWAVEFORMAT Property</span></span>

<span data-ttu-id="1062b-104">Указывает структуру [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) , описывающую входное звуковое содержимое.</span><span class="sxs-lookup"><span data-stu-id="1062b-104">Specifies the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure describing the input audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1062b-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="1062b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1062b-106">g \_ всзвмакоригиналвавеформат</span><span class="sxs-lookup"><span data-stu-id="1062b-106">g\_wszWMACOriginalWaveFormat</span></span>

## <a name="data-type"></a><span data-ttu-id="1062b-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1062b-107">Data Type</span></span>

<span data-ttu-id="1062b-108">VT \_ array \| VT \_ UI1 ([**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) в виде массива байтов)</span><span class="sxs-lookup"><span data-stu-id="1062b-108">VT\_ARRAY \| VT\_UI1 ([**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) as an array of bytes)</span></span>

## <a name="remarks"></a><span data-ttu-id="1062b-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1062b-109">Remarks</span></span>

<span data-ttu-id="1062b-110">При перекодировании содержимого Windows Media Audio на более низкую скорость можно передать структуру [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) содержимого кодеку, чтобы кодек мог оптимизировать свои алгоритмы.</span><span class="sxs-lookup"><span data-stu-id="1062b-110">When transcoding Windows Media Audio-based content to a lower bit rate, you can pass the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure of the content to the codec to enable the codec to optimize its algorithms.</span></span> <span data-ttu-id="1062b-111">Эта функция, называемая интеллектуальным повторным сжатием, обеспечивает лучшие результаты, чем распаковка содержимого, и последующее перестроение восстановленных примеров PCM обратно через кодек.</span><span class="sxs-lookup"><span data-stu-id="1062b-111">This feature, called smart recompression, provides better results than decompressing the content and then feeding the reconstructed PCM samples back through the codec.</span></span>

<span data-ttu-id="1062b-112">При передаче структуры [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) включите все дополнительные байты в конце структуры, указанной параметром **вавеформатекс. кбсизе**.</span><span class="sxs-lookup"><span data-stu-id="1062b-112">When passing the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure, include any extra bytes at the end of the structure specified by **WAVEFORMATEX.cbSize**.</span></span>

<span data-ttu-id="1062b-113">Кодировщик звука принимает только входы и выходы, для которых количество каналов, бит на выборку и частота выборки идентичны.</span><span class="sxs-lookup"><span data-stu-id="1062b-113">The audio encoder accepts only inputs and outputs for which the number of channels, bits per sample, and sample rate are identical.</span></span> <span data-ttu-id="1062b-114">Вы можете перекодировать содержимое только на более низкую скорость в пределах этих параметров.</span><span class="sxs-lookup"><span data-stu-id="1062b-114">You can transcode content only to a lower bit rate within those parameters.</span></span> <span data-ttu-id="1062b-115">В любом случае необходимо декодировать содержимое и передать несжатые примеры в качестве входных данных кодировщику.</span><span class="sxs-lookup"><span data-stu-id="1062b-115">In any case, you must decode the content and pass the uncompressed samples as input to the encoder.</span></span> <span data-ttu-id="1062b-116">Задание этого свойства дает кодировщику некоторую информацию об обработке, уже выполненной над содержимым.</span><span class="sxs-lookup"><span data-stu-id="1062b-116">Setting this property gives the encoder some information about the processing that has already been performed on the content.</span></span>

## <a name="requirements"></a><span data-ttu-id="1062b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1062b-117">Requirements</span></span>



| <span data-ttu-id="1062b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1062b-118">Requirement</span></span> | <span data-ttu-id="1062b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1062b-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1062b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1062b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1062b-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1062b-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1062b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1062b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1062b-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1062b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1062b-124">Header</span><span class="sxs-lookup"><span data-stu-id="1062b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1062b-125"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="1062b-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1062b-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1062b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1062b-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1062b-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
