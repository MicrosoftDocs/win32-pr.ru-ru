---
description: Почему видеокодировщик отклоняет выходной формат, который я пытаюсь задать, при извлечении формата из того же объекта?
ms.assetid: f0747450-d224-423a-a9f1-04580df8a17e
title: Почему видеокодировщик отклоняет выходной формат, который я пытаюсь задать, при извлечении формата из того же объекта?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680908ec814fe322585c1ac97d3bb79deddaf034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080565"
---
# <a name="why-does-the-video-encoder-reject-an-output-format-that-i-try-to-set-when-i-retrieved-the-format-from-the-same-object"></a><span data-ttu-id="b33de-103">Почему видеокодировщик отклоняет выходной формат, который я пытаюсь задать, при извлечении формата из того же объекта?</span><span class="sxs-lookup"><span data-stu-id="b33de-103">Why does the video encoder reject an output format that I try to set, when I retrieved the format from the same object?</span></span>

<span data-ttu-id="b33de-104">В отличие от типов вывода звукового кодировщика, Поддерживаемые выходные данные, перечисленные кодировщиками видео, не являются доставленными.</span><span class="sxs-lookup"><span data-stu-id="b33de-104">Unlike audio encoder output types, the supported outputs enumerated by the video encoders are not complete as delivered.</span></span> <span data-ttu-id="b33de-105">Необходимо задать скорость потока в элементе **двбитрате** структуры **видеоинфохеадер** , чтобы она соответствовала значению, заданному для свойства [мфпкэй \_ равг](mfpkey-ravgproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="b33de-105">You must set the bit rate of the stream in the **dwBitrate** member of the **VIDEOINFOHEADER** structure to match the value set for the [MFPKEY\_RAVG](mfpkey-ravgproperty.md) property.</span></span>

<span data-ttu-id="b33de-106">После того как все параметры будут заданы нужным образом, необходимо получить частные данные кодека и добавить их в структуру **видеоинфохеадер** .</span><span class="sxs-lookup"><span data-stu-id="b33de-106">After all of the options are set the way that you want them, you must retrieve the codec private data and append it to the **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="b33de-107">Дополнительные сведения см. [в разделе Использование частных данных видеокодека](usingvideocodecprivatedata.md).</span><span class="sxs-lookup"><span data-stu-id="b33de-107">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b33de-108">См. также</span><span class="sxs-lookup"><span data-stu-id="b33de-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b33de-109">Часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="b33de-109">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



