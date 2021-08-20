---
description: Содержит данные набора анимации.
ms.assetid: 8d29b9fe-cc6e-48e3-b754-f00f17e4c80a
title: компресседаниматионсет
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0666a7aa62eda365eceba1f016af14c3f84c47c39257d42e287ced470bff7f5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118097092"
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

## <a name="see-also"></a>См. также

<dl> <dt>

[Шаблоны](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[**ксфилекомпресседаниматионсет**](xfilecompressedanimationset.md)
</dt> </dl>

 

 
