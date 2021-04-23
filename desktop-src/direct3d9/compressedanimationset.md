---
description: Содержит данные набора анимации.
ms.assetid: 8d29b9fe-cc6e-48e3-b754-f00f17e4c80a
title: компресседаниматионсет
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6cdf8fde552583884604fa66ec1167183918ed5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072512"
---
# <a name="compressedanimationset"></a><span data-ttu-id="32fb9-103">компресседаниматионсет</span><span class="sxs-lookup"><span data-stu-id="32fb9-103">CompressedAnimationSet</span></span>

<span data-ttu-id="32fb9-104">Содержит данные набора анимации.</span><span class="sxs-lookup"><span data-stu-id="32fb9-104">Contains animation set data.</span></span>

``` syntax
template CompressedAnimationSet
{
    <7F9B00B3-F125-4890-876E-1C42BF697C4D>
    DWORD CompressedBlockSize;
    FLOAT TicksPerSec;
    DWORD PlaybackType;
    DWORD BufferLength;
    array DWORD CompressedData[BufferLength];
}
```

<span data-ttu-id="32fb9-105">Где:</span><span class="sxs-lookup"><span data-stu-id="32fb9-105">Where:</span></span>

-   <span data-ttu-id="32fb9-106">Компресседблокксизе — общий размер (в байтах) сжатых данных в буфере данных анимации сжатого опорного кадра.</span><span class="sxs-lookup"><span data-stu-id="32fb9-106">CompressedBlockSize - Total size, in bytes, of the compressed data in the compressed key frame animation data buffer.</span></span>
-   <span data-ttu-id="32fb9-107">Тикксперсек — число тактов кадров ключа анимации, которые находятся в секунду.</span><span class="sxs-lookup"><span data-stu-id="32fb9-107">TicksPerSec - Number of animation key frame ticks that occur per second.</span></span>
-   <span data-ttu-id="32fb9-108">Плайбакктипе — тип цикла воспроизведения набора анимации.</span><span class="sxs-lookup"><span data-stu-id="32fb9-108">PlaybackType - Type of the animation set playback loop.</span></span> <span data-ttu-id="32fb9-109">См. раздел [**\_ тип D3DXPLAYBACK**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="32fb9-109">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>
-   <span data-ttu-id="32fb9-110">BufferLength — минимальный размер буфера (в байтах), необходимый для хранения данных анимации с сжатым ключевым кадром.</span><span class="sxs-lookup"><span data-stu-id="32fb9-110">BufferLength - Minimum buffer size, in bytes, required to hold compressed key frame animation data.</span></span> <span data-ttu-id="32fb9-111">Значение равно ((Компресседблокксизе + 3)/4).</span><span class="sxs-lookup"><span data-stu-id="32fb9-111">Value is equal to ( ( CompressedBlockSize + 3 ) / 4 ).</span></span>
-   <span data-ttu-id="32fb9-112">Компресседдата \[ BufferLength \] — массив значений сжатых данных.</span><span class="sxs-lookup"><span data-stu-id="32fb9-112">CompressedData\[BufferLength\] - An array of compressed data values.</span></span>

## <a name="see-also"></a><span data-ttu-id="32fb9-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32fb9-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32fb9-114">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="32fb9-114">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[<span data-ttu-id="32fb9-115">**ксфилекомпресседаниматионсет**</span><span class="sxs-lookup"><span data-stu-id="32fb9-115">**XFILECOMPRESSEDANIMATIONSET**</span></span>](xfilecompressedanimationset.md)
</dt> </dl>

 

 
