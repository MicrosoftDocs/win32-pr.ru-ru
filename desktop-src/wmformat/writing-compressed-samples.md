---
title: Написание сжатых образцов
description: Написание сжатых образцов
ms.assetid: f85ca719-1b9d-404f-b2b1-c9e3524e4bc6
keywords:
- Расширенный формат систем (ASF), написание сжатых образцов
- ASF (Расширенный системный формат), написание сжатых образцов
- Расширенный формат систем (ASF), Передача сжатых образцов
- ASF (Расширенный системный формат), Передача сжатых образцов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c43fed30aa89e83c157479257e78fbab4acd98
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104487288"
---
# <a name="writing-compressed-samples"></a><span data-ttu-id="09351-107">Написание сжатых образцов</span><span class="sxs-lookup"><span data-stu-id="09351-107">Writing Compressed Samples</span></span>

<span data-ttu-id="09351-108">Для некоторых звуковых или видеопотоков может потребоваться передача уже сжатых образцов вместо передачи необработанных данных.</span><span class="sxs-lookup"><span data-stu-id="09351-108">For some audio or video streams, you may want to pass samples that are already compressed instead of passing raw data.</span></span> <span data-ttu-id="09351-109">Эта функция используется для копирования существующего потока или для записи образцов, сжатых с помощью стороннего кодека.</span><span class="sxs-lookup"><span data-stu-id="09351-109">This feature is used to copy an existing stream or to write samples compressed with a third-party codec.</span></span> <span data-ttu-id="09351-110">Процесс написания сжатого примера аналогичен написанию несжатого образца, за исключением того, что вместо [**ивмвритер:: вритесампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)используется [**Ивмвритерадванцед:: вритестреамсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) .</span><span class="sxs-lookup"><span data-stu-id="09351-110">The process of writing a compressed sample is identical to writing an uncompressed sample, except that you use [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) instead of [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span></span> <span data-ttu-id="09351-111">Дополнительные сведения о написании несжатых образцов см. [в разделе Создание образцов](to-write-samples.md).</span><span class="sxs-lookup"><span data-stu-id="09351-111">For more information about writing uncompressed samples, see [To Write Samples](to-write-samples.md).</span></span>

<span data-ttu-id="09351-112">При написании сжатых образцов для профилей CBR модуль записи удаляет некоторые примеры, если это необходимо, для сохранения содержимого в заданной скорости потока и в значениях окна буфера.</span><span class="sxs-lookup"><span data-stu-id="09351-112">When you write compressed samples, for CBR profiles, the writer will drop some samples, if necessary, to keep the content within the specified bit rate and buffer window values.</span></span> <span data-ttu-id="09351-113">Для VBR модуль записи не будет удалять образцы, но не существует способа убедиться, что скорость потока и значения окна буфера будут правильными.</span><span class="sxs-lookup"><span data-stu-id="09351-113">For VBR, the writer will not drop samples, but there is no way to be sure that the bit rate and buffer window values will be correct.</span></span>

<span data-ttu-id="09351-114">При копировании потока из одного файла в другой следует всегда копировать объект конфигурации потока из профиля исходного файла в профиль нового файла.</span><span class="sxs-lookup"><span data-stu-id="09351-114">If you are copying a stream from one file to another, you should always copy the stream configuration object from the profile of the original file to the profile of the new file.</span></span> <span data-ttu-id="09351-115">Это обеспечит правильную скорость потока и данные окна буфера.</span><span class="sxs-lookup"><span data-stu-id="09351-115">This ensures that you have the correct bit rate and buffer window information.</span></span> <span data-ttu-id="09351-116">При копировании сжатого потока в поток, в котором установлен меньший набор окон буфера, примеры будут удалены во время записи файла.</span><span class="sxs-lookup"><span data-stu-id="09351-116">If you copy a compressed stream to a stream that has a lower buffer window set, samples will be dropped during file writing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09351-117">См. также</span><span class="sxs-lookup"><span data-stu-id="09351-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09351-118">**Запись файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="09351-118">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




