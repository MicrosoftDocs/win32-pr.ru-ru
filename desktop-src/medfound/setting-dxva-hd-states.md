---
description: .
ms.assetid: 7f339ee8-01e6-4bbb-8563-020ff0e02499
title: Настройка состояний ДКСВА-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e539796aa5d3997b35739e75c80b438a7b5da50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711396"
---
# <a name="setting-dxva-hd-states"></a>Настройка состояний ДКСВА-HD

Во время обработки видео устройство Microsoft DirectX Video ускорение High Definition (ДКСВА-HD) поддерживает постоянное состояние от одного кадра до следующего. Каждое состояние имеет задокументированное значение по умолчанию. После настройки устройства задайте все состояния, которые вы хотите изменить, по умолчанию. Перед обработкой каждого кадра обновите все состояния, которые должны быть изменены.

> [!Note]  
> Этот проект отличается от ДКСВА-президента. В ДКСВА-президент приложение должно указать все параметры каждого из этих кадров.

 

Состояния устройств делятся на две категории:

-   Состояния *потоков* применяют каждый входной поток отдельно. К каждому потоку можно применить разные параметры.
-   Состояния *Блит* применяются глобально ко всей Блит обработки видео.

Определены следующие состояния потока.



| Состояние потока                                   | Описание                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| **ДКСВАХД \_ \_ состояния потока \_ D3DFORMAT**           | Входной формат видео.                                                                                             |
| **\_ \_ \_ Формат кадра состояния потока \_ дксвахд**       | Чередование.                                                                                                    |
| **\_ \_ \_ \_ цветовое пространство ввода состояния потока дксвахд \_** | Цветное пространство ввода. Это состояние задает диапазон цветов RGB и матрицу передачи Икбкр для входного потока. |
| **\_ \_ \_ частота вывода состояния потока \_ дксвахд**        | Частота выходных кадров. Это состояние управляет преобразованием частоты кадров.                                                   |
| **\_ \_ \_ исходный \_ прямоугольник состояния потока дксвахд**        | Исходный прямоугольник.                                                                                               |
| **\_ \_ \_ целевой \_ прямоугольник состояния потока дксвахд**   | Прямоугольник назначения.                                                                                          |
| **ДКСВАХД \_ потоковое \_ состояние \_ Alpha**               | Плоская альфа-версия.                                                                                                   |
| **\_ \_ Палитра состояния потока дксвахд \_**             | Цветовая палитра. Это состояние применяется только к входным форматам палеттизед.                                             |
| **\_ \_ \_ ключ яркости состояния потока \_ дксвахд**           | Ключ яркости.                                                                                                       |
| **пропорции \_ состояния потока дксвахд \_ \_ \_**       | Пропорция в пикселях.                                                                                             |
| **\_ \_ Фильтр состояния потока \_ дксвахд \_ XXXX**        | Параметры фильтра изображений. Драйвер может поддерживать яркость, контрастность и другие фильтры изображений.                    |



 

Определены следующие состояния Блит:



| Состояние Блит                                   | Описание                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| **\_ \_ \_ целевой \_ прямоугольник состояния БЛТ дксвахд**         | Целевой прямоугольник.                                                            |
| **\_ \_ \_ цвет фона состояния дксвахд \_ БЛТ**    | Цвет фона.                                                            |
| **\_ \_ \_ \_ цветовая область вывода состояния БЛТ дксвахд \_** | Цветовое пространство вывода.                                                          |
| **\_ \_ \_ Заливка альфа-дксвахд состояния БЛТ \_**          | Режим заливки альфа-канала.                                                             |
| **ДКСВАХД \_ БЛТ \_ состояния \_**         | Ограничением. Это состояние определяет, довнсамплес ли устройство к выходным данным. |



 

Чтобы задать состояние потока, вызовите метод [**идксвахд \_ видеопроцессор:: сетвидеопроцессстреамстате**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) . Чтобы задать состояние Блит, вызовите метод [**идксвахд \_ видеопроцессор:: сетвидеопроцессблтстате**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) . В обоих методах значение перечисления указывает заданное состояние. Данные о состоянии задаются с помощью структуры данных, зависящей от состояния, которую приложение приводит к **типу \* void** .

В следующем примере кода задается входной формат и прямоугольник назначения для потока 0 и устанавливается черный цвет фона.


```C++
HRESULT SetDXVAHDStates(HWND hwnd, D3DFORMAT inputFormat)
{
    // Set the initial stream states.

    // Set the format of the input stream

    DXVAHD_STREAM_STATE_D3DFORMAT_DATA d3dformat = { inputFormat };

    HRESULT hr = g_pDXVAVP->SetVideoProcessStreamState(
        0,  // Stream index
        DXVAHD_STREAM_STATE_D3DFORMAT,
        sizeof(d3dformat),
        &d3dformat
        );

    if (SUCCEEDED(hr))
    { 
        // For this example, the input stream contains progressive frames.

        DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA frame_format = { DXVAHD_FRAME_FORMAT_PROGRESSIVE };
        
        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index
            DXVAHD_STREAM_STATE_FRAME_FORMAT,
            sizeof(frame_format),
            &frame_format
            );
    }

    if (SUCCEEDED(hr))
    { 
        // Compute the letterbox area.

        RECT rcDest;
        GetClientRect(hwnd, &rcDest);

        RECT rcSrc;
        SetRect(&rcSrc, 0, 0, VIDEO_WIDTH, VIDEO_HEIGHT);

        rcDest = LetterBoxRect(rcSrc, rcDest);

        // Set the destination rectangle, so the frame is displayed within the 
        // letterbox area. Otherwise, the frame is stretched to cover the 
        // entire surface.

        DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA DstRect = { TRUE, rcDest };

        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index 
            DXVAHD_STREAM_STATE_DESTINATION_RECT,
            sizeof(DstRect),
            &DstRect
            );
    }

    if (SUCCEEDED(hr))
    { 
        DXVAHD_COLOR_RGBA rgbBackground = { 0.0f, 0.0f, 0.0f, 1.0f };  // RGBA

        DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA background = { FALSE, rgbBackground };

        hr = g_pDXVAVP->SetVideoProcessBltState(
            DXVAHD_BLT_STATE_BACKGROUND_COLOR,
            sizeof (background),
            &background
            );
    }

    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[ДКСВА-HD](dxva-hd.md)
</dt> </dl>

 

 



