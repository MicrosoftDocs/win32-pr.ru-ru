---
title: Копирование потоков с использованием распакованных образцов
description: Копирование потоков с использованием распакованных образцов
ms.assetid: 03ad8415-1dff-4362-94b4-7ec69c3e7888
keywords:
- Windows Media Format SDK, копирование потоков
- Расширенный системный формат (ASF), копирование потоков
- ASF (Расширенный системный формат), копирование потоков
- потоки, копирование с использованием распакованных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c5c0f98b02090d98814983ad518ee3cd7e5d8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700679"
---
# <a name="copying-streams-using-decompressed-samples"></a><span data-ttu-id="bdc18-107">Копирование потоков с использованием распакованных образцов</span><span class="sxs-lookup"><span data-stu-id="bdc18-107">Copying Streams Using Decompressed Samples</span></span>

<span data-ttu-id="bdc18-108">Настоятельно рекомендуется не копировать потоки из одного файла в другой с помощью распакованных образцов.</span><span class="sxs-lookup"><span data-stu-id="bdc18-108">It is strongly recommended that you not copy streams from one file to another using decompressed samples.</span></span> <span data-ttu-id="bdc18-109">Процесс распаковки и повторного сжатия образцов приведет к снижению качества выходных данных.</span><span class="sxs-lookup"><span data-stu-id="bdc18-109">The process of decompressing and recompressing samples will degrade the quality of the output.</span></span> <span data-ttu-id="bdc18-110">Если вам нужно распаковать примеры и скопировать их в другой поток, может возникнуть какая-то трудность с закодированными потоками с переменной скоростью с переменным качеством (VBR).</span><span class="sxs-lookup"><span data-stu-id="bdc18-110">If you do need to decompress your samples and then copy them to another stream, you may encounter some difficulty with quality-based variable bit rate (VBR) encoded streams.</span></span>

<span data-ttu-id="bdc18-111">Когда кодек заканчивает сжатие потока VBR на основе качества, он записывает скорость и окно буфера полученного содержимого.</span><span class="sxs-lookup"><span data-stu-id="bdc18-111">When the codec finishes compressing a quality-based VBR stream, it records the bit rate and buffer window of the resulting content.</span></span> <span data-ttu-id="bdc18-112">При чтении файла, содержащего поток, закодированный с частотой VBR, профиль, полученный от средства чтения, будет заметок о скорости и окне буфера, а также в окне максимального числа битов и максимального буфера.</span><span class="sxs-lookup"><span data-stu-id="bdc18-112">When you read a file containing a stream encoded with quality-based VBR, the profile obtained from the reader will note the bit rate and buffer window as well as the maximum bit rate and maximum buffer window.</span></span> <span data-ttu-id="bdc18-113">Эта конфигурация в профиле обычно означает потоковую переменную с ограниченным числом переменных с ограничением по битам.</span><span class="sxs-lookup"><span data-stu-id="bdc18-113">This configuration in the profile normally signifies a bit-rate constrained variable bit rate stream.</span></span> <span data-ttu-id="bdc18-114">В результате, когда профиль задается в средстве записи, он ожидает передачи данных для потока, так как для потоков с ограниченным числом VBR требуется использовать двустороннюю кодировку.</span><span class="sxs-lookup"><span data-stu-id="bdc18-114">As a result, when you set the profile on the writer, it will expect a preprocessing pass for the stream, because bit-rate constrained VBR streams require two-pass encoding.</span></span> <span data-ttu-id="bdc18-115">Поток должен обрабатываться так, будто он был потоком с ограничением скорости потока и доставлять образцы для предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="bdc18-115">You should treat the stream as if it were a bit-rate constrained VBR stream and deliver the samples for preprocessing.</span></span> <span data-ttu-id="bdc18-116">Поскольку используются значения, возвращаемые после кодирования содержимого на определенном уровне качества, эти значения представляют нужный уровень качества.</span><span class="sxs-lookup"><span data-stu-id="bdc18-116">Because you are using the values returned after encoding the content at a particular quality level, those values represent the desired quality level.</span></span> <span data-ttu-id="bdc18-117">Конечно, качество повторно закодированных выходных данных будет в любом случае снижать производительность в результате повторной кодировки.</span><span class="sxs-lookup"><span data-stu-id="bdc18-117">Of course, the quality of the re-encoded output will be somewhat degraded anyway, as a result of the re-encoding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdc18-118">См. также</span><span class="sxs-lookup"><span data-stu-id="bdc18-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdc18-119">**Копирование данных из одного файла в другой**</span><span class="sxs-lookup"><span data-stu-id="bdc18-119">**Copying Data from One File to Another**</span></span>](copying-data-from-one-file-to-another.md)
</dt> <dt>

[<span data-ttu-id="bdc18-120">**Копирование потоков без распаковки данных**</span><span class="sxs-lookup"><span data-stu-id="bdc18-120">**Copying Streams Without Decompressing the Data**</span></span>](copying-streams-without-decompressing-the-data.md)
</dt> </dl>

 

 




