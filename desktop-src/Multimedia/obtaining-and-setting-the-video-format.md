---
title: Получение и установка формата видео
description: Получение и установка формата видео
ms.assetid: 0e6baf24-7a79-45ab-9fc7-69334419956d
keywords:
- макрос Капжетвидеоформат
- макрос Капжетвидеоформатсизе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6890c3a1d653d43d24c5baa0790cc0d26040685b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890609"
---
# <a name="obtaining-and-setting-the-video-format"></a>Получение и установка формата видео

Структура [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) имеет переменную длину для поддержки стандартных и сжатых форматов данных. Так как эта структура имеет переменную длину, приложения всегда должны запрашивать размер структуры и распределять память перед получением текущего видеоформата. В следующем примере используется макрос [**капжетвидеоформатсизе**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) для получения размера буфера, а затем вызывается макрос [**капжетвидеоформат**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) , чтобы получить текущий формат видео.


```C++
LPBITMAPINFO lpbi;
DWORD dwSize;

dwSize = capGetVideoFormatSize(hWndC);
lpbi = GlobalAllocPtr (GHND, dwSize);
capGetVideoFormat(hWndC, lpbi, dwSize); 

// Access the video format and then free the allocated memory.
 
```



Приложения могут использовать макрос [**капсетвидеоформат**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) (или сообщение [**WM \_ Cap \_ Set \_ видеоформат**](wm-cap-set-videoformat.md) ) для отправки структуры заголовка [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) в окно Capture. Так как форматы видео зависят от устройства, приложение должно проверить возвращаемое значение, чтобы определить, был ли формат принят.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование видеозаписи](using-video-capture.md)
</dt> </dl>

 

 