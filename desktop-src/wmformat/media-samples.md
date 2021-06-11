---
title: Примеры носителей (пакет SDK для Windows Media Format 11)
description: Узнайте о примерах мультимедиа в пакете SDK для Windows Media Format 11. Пример носителя — это объект, содержащий упорядоченный список из нуля или более буферов.
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- Windows Media Format SDK, примеры мультимедиа
- Windows Media Format SDK, примеры
- Расширенный формат систем (ASF), примеры мультимедиа
- ASF (Расширенный системный формат), примеры мультимедиа
- Расширенный формат систем (ASF), примеры
- ASF (Расширенный системный формат), примеры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b8d264aa23e80f1e692f28789c2f2e631ef3ed8
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989079"
---
# <a name="media-samples-windows-media-format-11-sdk"></a><span data-ttu-id="5d620-110">Примеры носителей (пакет SDK для Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="5d620-110">Media Samples (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="5d620-111">Пример носителя, или пример, представляет собой блок цифровых медиа-данных.</span><span class="sxs-lookup"><span data-stu-id="5d620-111">A media sample, or sample, is a block of digital media data.</span></span> <span data-ttu-id="5d620-112">Примером является базовый блок, который управляется чтением и записью объектов пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="5d620-112">A sample is the basic unit that is manipulated by the reading and writing objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="5d620-113">Содержимое отдельного образца определяется типом носителя, связанным с образцом.</span><span class="sxs-lookup"><span data-stu-id="5d620-113">The contents of an individual sample are dictated by the media type associated with the sample.</span></span> <span data-ttu-id="5d620-114">Для видео каждый пример представляет один кадр.</span><span class="sxs-lookup"><span data-stu-id="5d620-114">For video, each sample represents a single frame.</span></span> <span data-ttu-id="5d620-115">Для звука объем данных в отдельном примере задается в профиле, который используется для создания ASF-файла.</span><span class="sxs-lookup"><span data-stu-id="5d620-115">For audio, the amount of data in an individual sample is set in the profile used to create the ASF file.</span></span>

<span data-ttu-id="5d620-116">Примеры могут содержать несжатые данные или могут содержать сжатые данные. в этом случае они называются *примерами потока*.</span><span class="sxs-lookup"><span data-stu-id="5d620-116">Samples can contain uncompressed data, or they can contain compressed data, in which case they are called *stream samples*.</span></span> <span data-ttu-id="5d620-117">При создании файла ASF образцы передаются в модуль записи.</span><span class="sxs-lookup"><span data-stu-id="5d620-117">When creating an ASF file, you pass samples to the writer.</span></span> <span data-ttu-id="5d620-118">Модуль записи координирует сжатие образцов с помощью соответствующего кодека и упорядочивает сжатые данные в разделе данных файла ASF.</span><span class="sxs-lookup"><span data-stu-id="5d620-118">The writer coordinates compression of the samples with the appropriate codec and arranges the compressed data in the data section of the ASF file.</span></span> <span data-ttu-id="5d620-119">При воспроизведении средство чтения считывает сжатые данные, распаковывает их и предоставляет воссозданные несжатые данные в виде выходных образцов.</span><span class="sxs-lookup"><span data-stu-id="5d620-119">On playback, the reader reads the compressed data, decompresses it, and provides the reconstructed uncompressed data as output samples.</span></span>

<span data-ttu-id="5d620-120">Все примеры, используемые пакетом SDK для Windows Media Format, инкапсулированы в буферный объект, память которого автоматически выделяется компонентами времени выполнения пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="5d620-120">All samples used by the Windows Media Format SDK are encapsulated in buffer object whose memory is allocated automatically by the SDK run-time components.</span></span> <span data-ttu-id="5d620-121">При необходимости можно также выделить собственные буферы, используя расширенные возможности модуля записи и читателя.</span><span class="sxs-lookup"><span data-stu-id="5d620-121">You can also allocate your own buffers if you need to, using advanced features of the writer and reader.</span></span>

<span data-ttu-id="5d620-122">**Примечание** . Термин пример используется в этом пакете SDK для ссылки на пример носителя, а не аудио.</span><span class="sxs-lookup"><span data-stu-id="5d620-122">**Note** The term sample is used in this SDK to refer to a media sample, not an audio sample.</span></span> <span data-ttu-id="5d620-123">В примере кодирования звука образец ссылается на одно закодированное звуковое значение.</span><span class="sxs-lookup"><span data-stu-id="5d620-123">In audio encoding, a sample refers to a single encoded audio value.</span></span> <span data-ttu-id="5d620-124">Как правило, качество закодированного звука определяется числом выборок в секунду.</span><span class="sxs-lookup"><span data-stu-id="5d620-124">Typically, the quality of encoded audio is specified by a number of samples per second.</span></span> <span data-ttu-id="5d620-125">Например, звук с качеством CD записывается в 44 100 выборок в секунду.</span><span class="sxs-lookup"><span data-stu-id="5d620-125">For example, CD quality sound is recorded at 44,100 samples per second.</span></span> <span data-ttu-id="5d620-126">Это значение обычно сокращается с помощью нотации Гц, поэтому 44 100 выборок в секунду будет составлять 44 100 Гц или 44,1 кГц.</span><span class="sxs-lookup"><span data-stu-id="5d620-126">This value is commonly abbreviated with the Hz notation, so 44,100 samples per second would be 44,100 Hz or 44.1 kHz.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d620-127">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="5d620-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d620-128">**Основные понятия**</span><span class="sxs-lookup"><span data-stu-id="5d620-128">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="5d620-129">**Интерфейс Инссбуффер**</span><span class="sxs-lookup"><span data-stu-id="5d620-129">**INSSBuffer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[<span data-ttu-id="5d620-130">**Входы, потоки и выходные данные**</span><span class="sxs-lookup"><span data-stu-id="5d620-130">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




