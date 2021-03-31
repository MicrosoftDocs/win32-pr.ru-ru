---
title: Кодировка Two-Pass
description: Кодировка Two-Pass
ms.assetid: 354cd0a5-9a64-4171-9604-694e60b382ad
keywords:
- Windows Media Format SDK, многопроходная кодировка
- Windows Media Format SDK, 2 — передача кодирования
- кодеки, два прохода кодирования
- кодеки, 2-передача кодировки
- 2-проходная кодировка, о
- 2. Передача кодирования, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6764f80857447e122c97c69683243a65da7e83b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067734"
---
# <a name="two-pass-encoding"></a><span data-ttu-id="c9bb6-109">Кодировка Two-Pass</span><span class="sxs-lookup"><span data-stu-id="c9bb6-109">Two-Pass Encoding</span></span>

<span data-ttu-id="c9bb6-110">Двусторонняя кодировка — это метод кодирования, доступный в некоторых кодеках, таких как кодек Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="c9bb6-110">Two-pass encoding is an encoding method available with some codecs, like the Windows Media Video 9 codec.</span></span> <span data-ttu-id="c9bb6-111">При использовании двусторонней кодировки кодек обрабатывает все примеры для потока дважды.</span><span class="sxs-lookup"><span data-stu-id="c9bb6-111">When you use two-pass encoding, the codec processes all of the samples for the stream twice.</span></span> <span data-ttu-id="c9bb6-112">При первом прохождении кодек собирает сведения о содержимом потока.</span><span class="sxs-lookup"><span data-stu-id="c9bb6-112">On the first pass, the codec gathers information about the content of the stream.</span></span> <span data-ttu-id="c9bb6-113">На втором этапе кодек использует информацию, собранную на первом этапе, для оптимизации процесса кодирования потока.</span><span class="sxs-lookup"><span data-stu-id="c9bb6-113">On the second pass, the codec uses the information gathered on the first pass to optimize the encoding process for the stream.</span></span>

<span data-ttu-id="c9bb6-114">В режиме кодирования постоянной скорости потока файлы, закодированные в двух проходах, обычно более эффективны, чем файлы, закодированные за один проход.</span><span class="sxs-lookup"><span data-stu-id="c9bb6-114">In the Constant Bit Rate encoding mode, files that are encoded in two passes are generally more efficient than files encoded in a single pass.</span></span> <span data-ttu-id="c9bb6-115">Качество VBR, основанное на одном проходе, обеспечивает более устойчивое качество, чем скорость с частотой передачи данных на скорости, которая представляет собой два этапа.</span><span class="sxs-lookup"><span data-stu-id="c9bb6-115">Quality-based VBR, which is one pass, produces more consistent quality than bit-rate-based VBR, which is two-pass.</span></span>

<span data-ttu-id="c9bb6-116">Нельзя использовать двустороннюю кодировку для потоков в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="c9bb6-116">You cannot use two-pass encoding on live streams.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9bb6-117">См. также</span><span class="sxs-lookup"><span data-stu-id="c9bb6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9bb6-118">**Функции кодеков**</span><span class="sxs-lookup"><span data-stu-id="c9bb6-118">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="c9bb6-119">**Использование кодировки Two-Pass**</span><span class="sxs-lookup"><span data-stu-id="c9bb6-119">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> </dl>

 

 




