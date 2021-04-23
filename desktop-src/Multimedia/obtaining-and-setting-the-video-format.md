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
# <a name="obtaining-and-setting-the-video-format"></a><span data-ttu-id="78343-105">Получение и установка формата видео</span><span class="sxs-lookup"><span data-stu-id="78343-105">Obtaining and Setting the Video Format</span></span>

<span data-ttu-id="78343-106">Структура [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) имеет переменную длину для поддержки стандартных и сжатых форматов данных.</span><span class="sxs-lookup"><span data-stu-id="78343-106">The [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure is of variable length to accommodate standard and compressed data formats.</span></span> <span data-ttu-id="78343-107">Так как эта структура имеет переменную длину, приложения всегда должны запрашивать размер структуры и распределять память перед получением текущего видеоформата.</span><span class="sxs-lookup"><span data-stu-id="78343-107">Because this structure is of variable length, applications must always query the size of the structure and allocate memory before retrieving the current video format.</span></span> <span data-ttu-id="78343-108">В следующем примере используется макрос [**капжетвидеоформатсизе**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) для получения размера буфера, а затем вызывается макрос [**капжетвидеоформат**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) , чтобы получить текущий формат видео.</span><span class="sxs-lookup"><span data-stu-id="78343-108">The following example uses the [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) macro to retrieve the buffer size and then calls the [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) macro to retrieve the current video format.</span></span>


```C++
LPBITMAPINFO lpbi;
DWORD dwSize;

dwSize = capGetVideoFormatSize(hWndC);
lpbi = GlobalAllocPtr (GHND, dwSize);
capGetVideoFormat(hWndC, lpbi, dwSize); 

// Access the video format and then free the allocated memory.
 
```



<span data-ttu-id="78343-109">Приложения могут использовать макрос [**капсетвидеоформат**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) (или сообщение [**WM \_ Cap \_ Set \_ видеоформат**](wm-cap-set-videoformat.md) ) для отправки структуры заголовка [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) в окно Capture.</span><span class="sxs-lookup"><span data-stu-id="78343-109">Applications can use the [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) macro (or the [**WM\_CAP\_SET\_VIDEOFORMAT**](wm-cap-set-videoformat.md) message) to send a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) header structure to the capture window.</span></span> <span data-ttu-id="78343-110">Так как форматы видео зависят от устройства, приложение должно проверить возвращаемое значение, чтобы определить, был ли формат принят.</span><span class="sxs-lookup"><span data-stu-id="78343-110">Because video formats are device specific, your application should check the return value to determine if the format was accepted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78343-111">См. также</span><span class="sxs-lookup"><span data-stu-id="78343-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78343-112">Использование видеозаписи</span><span class="sxs-lookup"><span data-stu-id="78343-112">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 