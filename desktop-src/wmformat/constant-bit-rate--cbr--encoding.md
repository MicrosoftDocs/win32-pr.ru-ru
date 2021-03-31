---
title: Кодирование с постоянной скоростью (CBR)
description: Кодирование с постоянной скоростью (CBR)
ms.assetid: f87277a5-55f1-46c7-a6a4-5824f3904d60
keywords:
- Windows Media Format SDK, кодирование CBR
- Windows Media Format SDK, постоянная скорость потока (CBR)
- кодеки, кодировка CBR
- кодеки, постоянная скорость битов (CBR)
- Постоянная скорость (CBR)
- CBR (Постоянная скорость)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3ded3709e2e7a3e5b567b91a127ad3486a0b66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411299"
---
# <a name="constant-bit-rate-cbr-encoding"></a><span data-ttu-id="27ae8-109">Кодирование с постоянной скоростью (CBR)</span><span class="sxs-lookup"><span data-stu-id="27ae8-109">Constant Bit Rate (CBR) Encoding</span></span>

<span data-ttu-id="27ae8-110">Кодирование с постоянной скоростью (CBR) — это метод кодирования по умолчанию для пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="27ae8-110">Constant bit rate (CBR) encoding is the default method of encoding with the Windows Media Format SDK.</span></span> <span data-ttu-id="27ae8-111">При использовании кодировки CBR вы указываете целевую скорость потока, и кодек использует любой объем сжатия, необходимый для его достижения.</span><span class="sxs-lookup"><span data-stu-id="27ae8-111">When using CBR encoding, you specify the target bit rate for a stream, and the codec uses whatever amount of compression is necessary to achieve it.</span></span>

<span data-ttu-id="27ae8-112">С CBR кодированием скорость и размер закодированного потока известны до кодирования.</span><span class="sxs-lookup"><span data-stu-id="27ae8-112">With CBR encoding the bit rate and size of the encoded stream are known prior to encoding.</span></span> <span data-ttu-id="27ae8-113">Например, при кодировании песни за три минуты в 32 000 бит/с вы узнаете, что размер файла будет примерно 704 КБ (32 000 бит/с x 180 секунды/8 бит на байт/1 024).</span><span class="sxs-lookup"><span data-stu-id="27ae8-113">For example, if you are encoding a three minute song at 32,000 bits per second, you know that the file size will be about 704 kilobytes (32,000 bps x 180 seconds / 8 bits per byte / 1,024).</span></span> <span data-ttu-id="27ae8-114">Кроме того, вы узнали, что пропускная способность, необходимая для потоковой передачи закодированного содержимого, составляет примерно 32 000 бит в секунду.</span><span class="sxs-lookup"><span data-stu-id="27ae8-114">You also know that the bandwidth required to stream the encoded content is about 32,000 bits per second.</span></span>

<span data-ttu-id="27ae8-115">Одновременная скорость кодирования с переменным битом (описанная в следующем разделе) позволяет также получить сведения о скорости потока до кодирования, но так как частота является переменной, полученный файл нельзя передать в потоке так эффективно, как файл, закодированный в режиме CBR.</span><span class="sxs-lookup"><span data-stu-id="27ae8-115">Constrained variable bit rate encoding (described in the following section) also enables you to know the bit rate prior to encoding, but since the rate is variable, the resulting file cannot be streamed as efficiently as a file encoded in CBR mode.</span></span> <span data-ttu-id="27ae8-116">При использовании CBR скорость потока с течением времени всегда остается близкой к среднему или целевому темпу, а также может быть задан объем вариации.</span><span class="sxs-lookup"><span data-stu-id="27ae8-116">With CBR, the bit rate over time always remains close to the average or target bit rate, and the amount of variation can be specified.</span></span>

<span data-ttu-id="27ae8-117">Недостаток кодировки CBR заключается в том, что качество закодированного содержимого не будет постоянным.</span><span class="sxs-lookup"><span data-stu-id="27ae8-117">The disadvantage of CBR encoding is that the quality of the encoded content will not be constant.</span></span> <span data-ttu-id="27ae8-118">Поскольку часть содержимого сложнее сжимать, части потока CBR будут иметь более низкую качество, чем другие.</span><span class="sxs-lookup"><span data-stu-id="27ae8-118">Because some content is more difficult to compress, parts of a CBR stream will be of lower quality than others.</span></span> <span data-ttu-id="27ae8-119">Например, типичный фильм содержит несколько сцен, которые довольно статичны, и некоторые сцены, которые являются полными действиями.</span><span class="sxs-lookup"><span data-stu-id="27ae8-119">For example, a typical movie has some scenes that are fairly static and some scenes that are full of action.</span></span> <span data-ttu-id="27ae8-120">Если вы кодируете фильм с помощью CBR, статичные сцены и, таким образом, легко кодируются эффективно, имеют более высокое качество, чем сцены действий, что намного сложнее кодировать.</span><span class="sxs-lookup"><span data-stu-id="27ae8-120">If you encode a movie using CBR, the scenes that are static, and therefore easy to encode efficiently, will be of higher quality than the action scenes, which are much more difficult to encode efficiently.</span></span>

<span data-ttu-id="27ae8-121">Кодировка CBR также может привести к нестабильному качеству одного файла в другой.</span><span class="sxs-lookup"><span data-stu-id="27ae8-121">CBR encoding can also result in inconsistent quality from one file to another.</span></span> <span data-ttu-id="27ae8-122">Если вы используете CBR для кодирования нескольких композиций различных жанров с одинаковой скоростью, вы можете заметить некоторые различия между ними.</span><span class="sxs-lookup"><span data-stu-id="27ae8-122">If you use CBR to encode several songs of different genres at the same bit rate, you may notice some difference in quality between them.</span></span>

<span data-ttu-id="27ae8-123">Как правило, вариации в качестве файла CBR более производятся с более низкими скоростями.</span><span class="sxs-lookup"><span data-stu-id="27ae8-123">In general, variations in the quality of a CBR file are more pronounced at lower bit rates.</span></span> <span data-ttu-id="27ae8-124">При более высоких скоростях качество файла с CBR по-прежнему будет отличаться, но проблемы с качеством будут менее заметны для пользователя.</span><span class="sxs-lookup"><span data-stu-id="27ae8-124">At higher bit rates, the quality of a CBR-encoded file will still vary, but the quality issues will be less noticeable to the user.</span></span> <span data-ttu-id="27ae8-125">При использовании кодировки CBR следует задать высокую пропускную способность так, как это разрешено в сценарии доставки.</span><span class="sxs-lookup"><span data-stu-id="27ae8-125">When using CBR encoding, you should set the bandwidth as high as your delivery scenario allows.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27ae8-126">См. также</span><span class="sxs-lookup"><span data-stu-id="27ae8-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27ae8-127">**Выбор метода кодирования**</span><span class="sxs-lookup"><span data-stu-id="27ae8-127">**Choosing an Encoding Method**</span></span>](choosing-an-encoding-method.md)
</dt> <dt>

[<span data-ttu-id="27ae8-128">**Функции кодеков**</span><span class="sxs-lookup"><span data-stu-id="27ae8-128">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="27ae8-129">**Кодирование переменной скорости (VBR)**</span><span class="sxs-lookup"><span data-stu-id="27ae8-129">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




