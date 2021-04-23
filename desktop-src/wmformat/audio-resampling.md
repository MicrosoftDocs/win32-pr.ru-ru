---
title: Ресамплинг звука
description: Ресамплинг звука
ms.assetid: ec6ad6b2-1d35-4ac4-9a1e-3fc9c053000c
keywords:
- Windows Media Format SDK, ресамплинг звука
- Windows Media Format SDK, ресамплинг аудио
- Расширенный формат систем (ASF), ресамплинг звука
- ASF (Расширенный системный формат), ресамплинг звука
- Расширенный формат систем (ASF), ресамплинг звука
- ASF (Расширенный системный формат), ресамплинг звука
- Ресамплинг звука
- Ресамплинг звука, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608272a7e531d7380991a705d391e6226a6758d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329891"
---
# <a name="audio-resampling"></a><span data-ttu-id="bea00-111">Ресамплинг звука</span><span class="sxs-lookup"><span data-stu-id="bea00-111">Audio Resampling</span></span>

<span data-ttu-id="bea00-112">Каждый сжатый формат аудиокодека имеет определенную частоту выборки и размер выборки.</span><span class="sxs-lookup"><span data-stu-id="bea00-112">Every compressed format of an audio codec has a specific sample rate and sample size.</span></span> <span data-ttu-id="bea00-113">Они не должны соответствовать параметрам формата входных данных или выходного формата.</span><span class="sxs-lookup"><span data-stu-id="bea00-113">These do not need to match the settings of the input format or output format.</span></span> <span data-ttu-id="bea00-114">Если формат входных данных отличается от параметров сжатого формата, описанного в профиле, модуль записи выполнит повторную выборку звука в процессе кодирования, чтобы соответствовать сжатому формату.</span><span class="sxs-lookup"><span data-stu-id="bea00-114">If an input format has different settings than the compressed format described in the profile, the writer will resample the audio, during the encoding process, to match the compressed format.</span></span> <span data-ttu-id="bea00-115">Только определенные форматы принимаются модулем записи в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="bea00-115">Only certain formats are accepted by the writer as input.</span></span> <span data-ttu-id="bea00-116">При перечислении входных форматов для сжатого аудиопотока все полученные форматы можно повторно вычислить в соответствии с форматом в профиле.</span><span class="sxs-lookup"><span data-stu-id="bea00-116">When you enumerate the input formats for a compressed audio stream, all of the formats retrieved can be resampled to match the format in the profile.</span></span>

<span data-ttu-id="bea00-117">При чтении сжатого звука средство чтения повторно выполнит выборку содержимого в соответствии с форматом выходных данных.</span><span class="sxs-lookup"><span data-stu-id="bea00-117">When reading compressed audio, the reader will resample the content to match the output format.</span></span> <span data-ttu-id="bea00-118">Необходимо использовать один из выходных форматов, перечисленных модулем чтения, поэтому вы гарантируете, что звук можно будет перевыборить в параметры формата вывода.</span><span class="sxs-lookup"><span data-stu-id="bea00-118">You must use one of the output formats enumerated by the reader, so you are guaranteed that the audio can be resampled to the output format settings.</span></span>

<span data-ttu-id="bea00-119">Каждая перевыборка может влиять на качество звука.</span><span class="sxs-lookup"><span data-stu-id="bea00-119">Each resampling potentially affects the quality of the audio.</span></span> <span data-ttu-id="bea00-120">По возможности следует использовать форматы входных и выходных данных с параметрами, соответствующими сжатому формату.</span><span class="sxs-lookup"><span data-stu-id="bea00-120">When possible, you should use input and output formats with settings that match the compressed format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bea00-121">См. также</span><span class="sxs-lookup"><span data-stu-id="bea00-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bea00-122">**Функции записи файлов**</span><span class="sxs-lookup"><span data-stu-id="bea00-122">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="bea00-123">**Работа с входными данными**</span><span class="sxs-lookup"><span data-stu-id="bea00-123">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="bea00-124">**Работа с выходами**</span><span class="sxs-lookup"><span data-stu-id="bea00-124">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




