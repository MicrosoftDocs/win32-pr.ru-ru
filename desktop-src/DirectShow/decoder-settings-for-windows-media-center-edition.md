---
description: Параметры декодера для Windows Media Center Edition
ms.assetid: 019b063f-f215-44d8-a916-3125bee6af93
title: Параметры декодера для Windows Media Center Edition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f66b5107fa0316f6ce2547e1f5f066165ed598
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105656729"
---
# <a name="decoder-settings-for-windows-media-center-edition"></a><span data-ttu-id="97498-103">Параметры декодера для Windows Media Center Edition</span><span class="sxs-lookup"><span data-stu-id="97498-103">Decoder Settings for Windows Media Center Edition</span></span>

<span data-ttu-id="97498-104">В Windows XP Media Center Edition 2005 и более поздних версий используется интерфейс [**икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) для настройки фильтра декодера звука для воспроизведения телепередач и DVD-дисков.</span><span class="sxs-lookup"><span data-stu-id="97498-104">Windows XP Media Center Edition 2005 and later uses the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface to configure the audio decoder filter for television and DVD playback.</span></span> <span data-ttu-id="97498-105">Поддерживаются следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="97498-105">The following properties are supported.</span></span>



| <span data-ttu-id="97498-106">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="97498-106">Property GUID</span></span>                   | <span data-ttu-id="97498-107">Описание</span><span class="sxs-lookup"><span data-stu-id="97498-107">Description</span></span>                                      |
|---------------------------------|--------------------------------------------------|
| <span data-ttu-id="97498-108">\_ \_ Формат выходного звука кодекапи \_</span><span class="sxs-lookup"><span data-stu-id="97498-108">CODECAPI\_AUDIO\_OUTPUT\_FORMAT</span></span> | <span data-ttu-id="97498-109">Настраивает формат выходного звука.</span><span class="sxs-lookup"><span data-stu-id="97498-109">Configures the audio output format.</span></span> <span data-ttu-id="97498-110">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="97498-110">See Remarks.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="97498-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97498-111">Remarks</span></span>

<span data-ttu-id="97498-112">Значение \_ \_ Свойства формат выходного звука кодекапи \_ представляет собой СТРОКОВОЕ представление идентификатора GUID, хранящегося в виде значения **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="97498-112">The value of the CODECAPI\_AUDIO\_OUTPUT\_FORMAT property is a string representation of a GUID, stored as a **BSTR** value.</span></span> <span data-ttu-id="97498-113">Определены следующие идентификаторы GUID.</span><span class="sxs-lookup"><span data-stu-id="97498-113">The following GUIDs are defined.</span></span>



| <span data-ttu-id="97498-114">Идентификатор GUID</span><span class="sxs-lookup"><span data-stu-id="97498-114">GUID</span></span>                                                        | <span data-ttu-id="97498-115">Описание</span><span class="sxs-lookup"><span data-stu-id="97498-115">Description</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97498-116">КОДЕКАПИ \_ Audio \_ выходной \_ Формат \_ PCM \_ стерео \_ матриксенкодед</span><span class="sxs-lookup"><span data-stu-id="97498-116">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_STEREO\_MATRIXENCODED</span></span> | <span data-ttu-id="97498-117">Программа фильтрации звука программного обеспечения должна выполнять декодирование и вывод стерео аудио-потока с многоканальной матрицей, закодированной по двум каналам.</span><span class="sxs-lookup"><span data-stu-id="97498-117">The software audio filter should perform software decoding and output a stereo audio stream, with the multichannel audio matrix encoded to the two channels.</span></span>                                                   |
| <span data-ttu-id="97498-118">\_звуковой \_ Формат выходных данных кодекапи \_ \_ PCM \_ стерео</span><span class="sxs-lookup"><span data-stu-id="97498-118">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_STEREO</span></span>                | <span data-ttu-id="97498-119">Программа фильтрации звука программного обеспечения должна выполнять декодирование и вывод стерео аудио-потока.</span><span class="sxs-lookup"><span data-stu-id="97498-119">The software audio filter should perform software decoding and output a stereo audio stream.</span></span>                                                                                                                   |
| <span data-ttu-id="97498-120">\_ \_ Формат выходного аудио кодекапи \_ \_ SPDIF \_</span><span class="sxs-lookup"><span data-stu-id="97498-120">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_SPDIF\_PCM</span></span>                 | <span data-ttu-id="97498-121">Фильтр программного обеспечения должен выполнять декодирование программного обеспечения, даже если физический вывод компьютера может быть цифровым интерфейсом, например S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="97498-121">The software audio filter should perform software audio decoding, even though the physical output from the PC may be a digital interface, such as S/PDIF.</span></span>                                                      |
| <span data-ttu-id="97498-122">\_ \_ Формат выходного звука кодекапи \_ \_ SPDIF \_ битовый поток</span><span class="sxs-lookup"><span data-stu-id="97498-122">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_SPDIF\_BITSTREAM</span></span>           | <span data-ttu-id="97498-123">Фильтр программного обеспечения не должен выполнять декодирование программного обеспечения, но должен передавать Необработанный цифровой звук битовый поток для внешней обработки устройством, подключенным к цифровому каналу, например S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="97498-123">The software audio filter should not perform software audio decoding, but should pass the raw digital audio bitstream for external processing by a device connected with a digital audio link, such as S/PDIF.</span></span> |
| <span data-ttu-id="97498-124">\_выходной формат кодекапиного звука \_ PCM для \_ \_ \_ наушников</span><span class="sxs-lookup"><span data-stu-id="97498-124">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_HEADPHONES</span></span>            | <span data-ttu-id="97498-125">Фильтр программного обеспечения должен выполнять декодирование аудио программного обеспечения и применять собственную обработку для оптимизации наушников.</span><span class="sxs-lookup"><span data-stu-id="97498-125">The software audio filter should perform software audio decoding and should apply proprietary processing to optimize for headphones.</span></span> <span data-ttu-id="97498-126">Поддержка этого параметра является необязательной.</span><span class="sxs-lookup"><span data-stu-id="97498-126">Support for this setting is optional.</span></span>                                     |



 

> [!Note]  
> <span data-ttu-id="97498-127">Интерфейс **икодекапи** хранит свойства кодека как пары "ключ-значение", где ключ является идентификатором GUID, а значение — типом **Variant** .</span><span class="sxs-lookup"><span data-stu-id="97498-127">The **ICodecAPI** interface stores codec properties as key/value pairs, where the key is a GUID and the value is a **VARIANT** type.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="97498-128">См. также</span><span class="sxs-lookup"><span data-stu-id="97498-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97498-129">Разработка кодировщика и декодера</span><span class="sxs-lookup"><span data-stu-id="97498-129">Encoder and Decoder Development</span></span>](encoder-and-decoder-development.md)
</dt> </dl>

 

 



