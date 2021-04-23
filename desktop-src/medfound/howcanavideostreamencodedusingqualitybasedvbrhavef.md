---
description: Как поток видео в кодировке на основе качества имеет меньше кадров, чем исходный поток?
ms.assetid: acce9c88-2ee1-4628-9fd5-ccb441f8b43e
title: Как поток видео в кодировке на основе качества имеет меньше кадров, чем исходный поток?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2af2775882155ed7ef2b0cfffdddeb30b2066e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264052"
---
# <a name="how-can-a-video-stream-encoded-using-quality-based-vbr-have-fewer-frames-than-the-original-stream"></a><span data-ttu-id="b983c-103">Как поток видео в кодировке на основе качества имеет меньше кадров, чем исходный поток?</span><span class="sxs-lookup"><span data-stu-id="b983c-103">How can a video stream encoded using quality-based VBR have fewer frames than the original stream?</span></span>

<span data-ttu-id="b983c-104">Число кадров закодированного потока может быть меньше, чем число кадров в оригинале по одной из двух причин: повторяющихся кадров и удаленных кадров.</span><span class="sxs-lookup"><span data-stu-id="b983c-104">The frame count of an encoded stream can be lower than the frame count of the original for one of two reasons: duplicate frames and dropped frames.</span></span>

<span data-ttu-id="b983c-105">Кодировщик обычно не создает кадры, которые являются точными дубликатами предыдущего кадра.</span><span class="sxs-lookup"><span data-stu-id="b983c-105">The encoder does not normally produce frames that are exact duplicates of the previous frame.</span></span> <span data-ttu-id="b983c-106">Если необходимо получить пример для каждого кадра (например, для некоторых контейнеров), можно настроить кодировщик для создания "фиктивных" кадров, задав для свойства [мфпкэй \_ ПРОДУЦЕДУММИФРАМЕС](mfpkey-producedummyframesproperty.md) значение Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="b983c-106">If you need to have a sample for every frame (this is required by some containers, for example), you can configure the encoder to produce "dummy" frames by setting the [MFPKEY\_PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="b983c-107">Кодировщик удаляет кадры, если не удается закодировать все кадры без переполнения буфера.</span><span class="sxs-lookup"><span data-stu-id="b983c-107">The encoder drops frames when it cannot encode all of the frames without overflowing the buffer.</span></span> <span data-ttu-id="b983c-108">Удаленные кадры влияют на качество потока, а дублирование кадров — нет.</span><span class="sxs-lookup"><span data-stu-id="b983c-108">Dropped frames affect the quality of the stream, duplicate frames do not.</span></span>

<span data-ttu-id="b983c-109">Вы можете получить статистику кадров от кодировщика, чтобы определить, были ли удалены кадры.</span><span class="sxs-lookup"><span data-stu-id="b983c-109">You can get frame statistics from the encoder to determine whether frames have been dropped.</span></span> <span data-ttu-id="b983c-110">Дополнительные сведения см. в разделе [Получение статистики кодировки](gettingencodingstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="b983c-110">For more information, see [Getting Encoding Statistics](gettingencodingstatistics.md).</span></span>

<span data-ttu-id="b983c-111">Как правило, потоки с частотой, основанной на уровне качества, будут иметь меньше кадров, чем исходный, если есть дублирующиеся кадры (поскольку скорость потока не ограничена).</span><span class="sxs-lookup"><span data-stu-id="b983c-111">Typically, quality-based VBR streams will only have fewer frames than the original if there are duplicate frames (because the bit rate is not constrained).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b983c-112">См. также</span><span class="sxs-lookup"><span data-stu-id="b983c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b983c-113">Часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="b983c-113">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



