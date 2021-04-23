---
title: Интерполяция кадров
description: Интерполяция кадров
ms.assetid: 74dbe855-361c-42ba-b21b-322ccd1c91d0
keywords:
- Windows Media Format SDK, интерполяция кадров
- кодеки, интерполяция кадров
- Интерполяция кадров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c62f95322920576eec0f10f3e4d61a279fdc4cf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069570"
---
# <a name="frame-interpolation"></a><span data-ttu-id="f56e8-106">Интерполяция кадров</span><span class="sxs-lookup"><span data-stu-id="f56e8-106">Frame Interpolation</span></span>

<span data-ttu-id="f56e8-107">Интерполяция кадров — это процесс создания промежуточных видеокадров на основе данных в двух последовательных кадрах закодированного видео.</span><span class="sxs-lookup"><span data-stu-id="f56e8-107">Frame interpolation is the process of creating intermediate video frames based on the data in two consecutive frames of encoded video.</span></span> <span data-ttu-id="f56e8-108">Фактически интерполяция кадров увеличивает [*частоту кадров*](wmformat-glossary.md) закодированного видео во время декодирования.</span><span class="sxs-lookup"><span data-stu-id="f56e8-108">In effect, frame interpolation increases the [*frame rate*](wmformat-glossary.md) of encoded video at the time of decoding.</span></span> <span data-ttu-id="f56e8-109">Интерполяцию кадров можно использовать для повышения гладкости воспроизведения видеопотоков с низкой частотой кадров.</span><span class="sxs-lookup"><span data-stu-id="f56e8-109">You can use frame interpolation to improve the smoothness of playback for video streams with low frame rates.</span></span>

<span data-ttu-id="f56e8-110">Поскольку это функция декодирования, она не включает специальные параметры кодирования и не требует дополнительной нагрузки на содержимое.</span><span class="sxs-lookup"><span data-stu-id="f56e8-110">Because this is a decoding feature, it does not involve any special encoding options and adds no overhead to the content.</span></span> <span data-ttu-id="f56e8-111">Интерполяция кадров указывается в качестве выходного параметра в объекте Reader.</span><span class="sxs-lookup"><span data-stu-id="f56e8-111">Frame interpolation is specified as an output setting in the reader object.</span></span>

<span data-ttu-id="f56e8-112">Только кодек Windows Media Video 9 поддерживает интерполяцию кадров.</span><span class="sxs-lookup"><span data-stu-id="f56e8-112">Only the Windows Media Video 9 codec supports frame interpolation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f56e8-113">См. также</span><span class="sxs-lookup"><span data-stu-id="f56e8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f56e8-114">**Функции кодеков**</span><span class="sxs-lookup"><span data-stu-id="f56e8-114">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="f56e8-115">**IWMReaderAdvanced2:: Сетаутпутсеттинг**</span><span class="sxs-lookup"><span data-stu-id="f56e8-115">**IWMReaderAdvanced2::SetOutputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[<span data-ttu-id="f56e8-116">**Параметры вывода**</span><span class="sxs-lookup"><span data-stu-id="f56e8-116">**Output Settings**</span></span>](output-settings.md)
</dt> </dl>

 

 




