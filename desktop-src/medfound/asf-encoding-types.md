---
description: Типы кодирования ASF
ms.assetid: ffa99c6b-3b62-4068-96d5-ad57c340d088
title: Типы кодирования ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6187f4bbf49eafaf50a46a8af92b71b4e72885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143288"
---
# <a name="asf-encoding-types"></a><span data-ttu-id="41576-103">Типы кодирования ASF</span><span class="sxs-lookup"><span data-stu-id="41576-103">ASF Encoding Types</span></span>

<span data-ttu-id="41576-104">Все методы кодирования сосредоточены на буфере, используемом кодировщиком для управления несжатыми входными данными.</span><span class="sxs-lookup"><span data-stu-id="41576-104">The encoding methods all focus on the buffer used by the encoder to manage uncompressed input data.</span></span> <span data-ttu-id="41576-105">Этот буфер определяется скоростью потока в битах в секунду и окном буфера в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="41576-105">This buffer is defined by the bit rate of the stream, in bits per second, and the buffer window, in milliseconds.</span></span> <span data-ttu-id="41576-106">При кодировании в файлы ASF кодировщики Windows Media придерживается ограничений буфера.</span><span class="sxs-lookup"><span data-stu-id="41576-106">When encoding to ASF files, the Windows Media encoders abide by the constraints of the buffer.</span></span> <span data-ttu-id="41576-107">Дополнительные сведения о окне буфера см. в разделе [модель буфера контейнера с утечкой](the-leaky-bucket-buffer-model.md)данных.</span><span class="sxs-lookup"><span data-stu-id="41576-107">For more information about the buffer window, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span> <span data-ttu-id="41576-108">Знание того, как и когда следует использовать каждый из методов, может помочь в создании высококачественного сжатого содержимого.</span><span class="sxs-lookup"><span data-stu-id="41576-108">Knowing how and when to use each method can help you create high-quality compressed content.</span></span> <span data-ttu-id="41576-109">В следующей таблице содержатся ссылки на разделы, посвященные каждому из доступных методов кодирования, которые приложение может использовать для кодирования данных мультимедиа в ASF.</span><span class="sxs-lookup"><span data-stu-id="41576-109">The following table contains links to topics about each of the available encoding methods that an application can use to encode media data to ASF.</span></span>



| <span data-ttu-id="41576-110">Метод Encoding</span><span class="sxs-lookup"><span data-stu-id="41576-110">Encoding method</span></span>                                                                                      | <span data-ttu-id="41576-111">Описание</span><span class="sxs-lookup"><span data-stu-id="41576-111">Description</span></span>                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41576-112">Кодирование постоянной скорости потока</span><span class="sxs-lookup"><span data-stu-id="41576-112">Constant Bit Rate Encoding</span></span>](constant-bit-rate-encoding.md)                                         | <span data-ttu-id="41576-113">Кодировщик сжимает данные до указанной скорости.</span><span class="sxs-lookup"><span data-stu-id="41576-113">The encoder compresses data to a specified bit rate.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="41576-114">Кодирование скорости переменной с учетом качества</span><span class="sxs-lookup"><span data-stu-id="41576-114">Quality-Based Variable Bit Rate Encoding</span></span>](quality-based-variable-bit-rate--vbr--encoding.md)       | <span data-ttu-id="41576-115">Кодировщик сжимает данные до определенного значения качества, чтобы качество закодированного носителя было согласованным в течение всего времени, независимо от требований к буферу результирующего потока.</span><span class="sxs-lookup"><span data-stu-id="41576-115">The encoder compresses data to a particular quality value so that the quality of the encoded media is consistent throughout its duration, regardless of the buffer requirements of the resulting stream.</span></span> |
| [<span data-ttu-id="41576-116">Кодирование переменной скорости с неограниченным битом</span><span class="sxs-lookup"><span data-stu-id="41576-116">Unconstrained Variable Bit Rate Encoding</span></span>](unconstrained-variable-bit-rate--vbr--encoding.md)       | <span data-ttu-id="41576-117">Кодировщик сжимает данные до максимально возможного качества, сохраняя при этом заданную скорость.</span><span class="sxs-lookup"><span data-stu-id="41576-117">The encoder compresses data to the highest possible quality while maintaining a specified bit rate.</span></span> <span data-ttu-id="41576-118">Этот режим также называется 2-проходным кодированием с переменной скоростью (VBR).</span><span class="sxs-lookup"><span data-stu-id="41576-118">This mode is also called 2-pass variable bit rate (VBR) encoding.</span></span>                                    |
| [<span data-ttu-id="41576-119">Пиковое кодирование с переменным ограничением скорости</span><span class="sxs-lookup"><span data-stu-id="41576-119">Peak-Constrained Variable Bit Rate Encoding</span></span>](peak-constrained-variable-bit-rate--vbr--encoding.md) | <span data-ttu-id="41576-120">Кодировщик сжимает данные до указанной скорости, сохраняя значения буфера в указанном максимальном окне буфера и скорости.</span><span class="sxs-lookup"><span data-stu-id="41576-120">The encoder compresses data to a specified bit rate while keeping the buffer values under the specified maximum buffer window and bit rate.</span></span> <span data-ttu-id="41576-121">Этот режим также называется 2-проходным пиковым числом VBR.</span><span class="sxs-lookup"><span data-stu-id="41576-121">This mode is also called 2-pass peak VBR.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="41576-122">См. также</span><span class="sxs-lookup"><span data-stu-id="41576-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41576-123">Поддержка ASF в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="41576-123">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="41576-124">Кодировщики Windows Media</span><span class="sxs-lookup"><span data-stu-id="41576-124">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



