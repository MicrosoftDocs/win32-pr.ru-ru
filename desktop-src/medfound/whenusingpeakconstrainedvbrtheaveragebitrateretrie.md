---
description: При использовании пиковой скорости VBR средняя скорость, полученная от объекта кодека, превышает пиковую скорость.
ms.assetid: 5fc344f8-4492-4878-802a-94606c5f33e0
title: При использовании пиковой скорости VBR средняя скорость, полученная от объекта кодека, превышает пиковую скорость. Как это возможно?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2bb2e09f5210baf8817553377fc832b9826b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344842"
---
# <a name="when-i-use-peak-constrained-vbr-the-average-bit-rate-retrieved-from-the-codec-object-is-larger-than-the-peak-bit-rate-how-is-that-possible"></a><span data-ttu-id="eb557-104">При использовании пиковой скорости VBR средняя скорость, полученная от объекта кодека, превышает пиковую скорость.</span><span class="sxs-lookup"><span data-stu-id="eb557-104">When I use peak-constrained VBR, the average bit rate retrieved from the codec object is larger than the peak bit rate.</span></span> <span data-ttu-id="eb557-105">Как это возможно?</span><span class="sxs-lookup"><span data-stu-id="eb557-105">How is that possible?</span></span>

<span data-ttu-id="eb557-106">Связь между средним битом и пиковой скоростью обычно непонятна.</span><span class="sxs-lookup"><span data-stu-id="eb557-106">The relationship between the average bit rate and the peak bit rate is often misunderstood.</span></span> <span data-ttu-id="eb557-107">Пиковая скорость потока описывает ограничение буфера за период времени, заданный пиковым окном буфера.</span><span class="sxs-lookup"><span data-stu-id="eb557-107">The peak bit rate describes a buffer constraint over a period of time specified by the peak buffer window.</span></span> <span data-ttu-id="eb557-108">Средняя скорость для двух проходов (с неограниченным или пиковым ограничением) — это средний бит в секунду в течение файла.</span><span class="sxs-lookup"><span data-stu-id="eb557-108">The average bit rate for two-pass VBR (unconstrained or peak-constrained) is the average bits per second over the duration of the file.</span></span>

<span data-ttu-id="eb557-109">Как описано в [модели буферного контейнера с утечкой](the-leaky-bucket-buffer-model.md), фактическая скорость потока, используемая в течение некоторого периода времени, равная окну буфера, может вдвое подходить к скорости потока.</span><span class="sxs-lookup"><span data-stu-id="eb557-109">As described in [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md), the actual bit rate used over a period of time equal to the buffer window can approach twice the bit rate.</span></span> <span data-ttu-id="eb557-110">Это происходит потому, что буфер, определенный как число бит, равный скорости потока (в секундах), очищается по постоянной ставке.</span><span class="sxs-lookup"><span data-stu-id="eb557-110">This is because the buffer, defined as a number of bits equal to the bit rate times the buffer window (in seconds), is being emptied at a constant rate.</span></span>

<span data-ttu-id="eb557-111">Например, за одну секунду в потоке 56 кбит/с, кодировщик создает примеры общего объема 59 КБ.</span><span class="sxs-lookup"><span data-stu-id="eb557-111">For example, in one second of a 56 Kbps stream, the encoder creates samples totaling 59 Kb.</span></span> <span data-ttu-id="eb557-112">Таким образом, 56 КБ данных удаляется из буфера в этой секунде, в результате чего в буфере удаляются 3 КБ.</span><span class="sxs-lookup"><span data-stu-id="eb557-112">So, 56 Kb of data is removed from the buffer in that second, leaving 3 Kb in the buffer.</span></span> <span data-ttu-id="eb557-113">Если поток содержит окно буфера, равное трем секундам, и, таким образом, общий размер буфера 168 КБ, то заполнение буфера займет почти 40 секунд.</span><span class="sxs-lookup"><span data-stu-id="eb557-113">If the stream has a buffer window of three seconds, and thus a total buffer size of 168 Kb, it would take almost 40 seconds to fill the buffer.</span></span> <span data-ttu-id="eb557-114">Средняя скорость потока (если его длительность меньше, чем время, необходимое для заполнения буфера), составляет 59 кбит/с, несмотря на то, что скорость передачи данных равна 56 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="eb557-114">The average bit rate for the stream (if its duration is less than the time it takes to fill the buffer) is 59 Kbps, even though the bit rate is set to 56 Kbps.</span></span>

<span data-ttu-id="eb557-115">То же самое происходит с ограничениями пиковой скорости.</span><span class="sxs-lookup"><span data-stu-id="eb557-115">The same phenomenon applies to peak bit rate constraints.</span></span> <span data-ttu-id="eb557-116">Для короткого содержимого средняя скорость потока, вычисленная объектом кодека после завершения кодирования, может превышать пиковую скорость.</span><span class="sxs-lookup"><span data-stu-id="eb557-116">For short content, the average bit rate computed by the codec object after encoding is completed can be greater than the peak bit rate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb557-117">См. также</span><span class="sxs-lookup"><span data-stu-id="eb557-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb557-118">Часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="eb557-118">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



