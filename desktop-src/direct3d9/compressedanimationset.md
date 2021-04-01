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
# <a name="compressedanimationset"></a>компресседаниматионсет

Содержит данные набора анимации.

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

Где:

-   Компресседблокксизе — общий размер (в байтах) сжатых данных в буфере данных анимации сжатого опорного кадра.
-   Тикксперсек — число тактов кадров ключа анимации, которые находятся в секунду.
-   Плайбакктипе — тип цикла воспроизведения набора анимации. См. раздел [**\_ тип D3DXPLAYBACK**](./d3dxplayback-type.md).
-   BufferLength — минимальный размер буфера (в байтах), необходимый для хранения данных анимации с сжатым ключевым кадром. Значение равно ((Компресседблокксизе + 3)/4).
-   Компресседдата \[ BufferLength \] — массив значений сжатых данных.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Шаблоны](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[**ксфилекомпресседаниматионсет**](xfilecompressedanimationset.md)
</dt> </dl>

 

 
