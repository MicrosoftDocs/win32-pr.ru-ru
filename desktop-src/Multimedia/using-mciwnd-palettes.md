---
title: Использование палитр МЦивнд
description: Использование палитр МЦивнд
ms.assetid: 2b99ca57-f321-4286-8ebf-ae3344d8d2c9
keywords:
- Макрос МЦивнджетпалетте
- Макрос МЦивндсетпалетте
- Макрос МЦивндреализе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970e0e33c9dd03c7f1133576f371b713f7174df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987478"
---
# <a name="using-mciwnd-palettes"></a><span data-ttu-id="ecfb0-106">Использование палитр МЦивнд</span><span class="sxs-lookup"><span data-stu-id="ecfb0-106">Using MCIWnd Palettes</span></span>

<span data-ttu-id="ecfb0-107">Для воспроизведения видеороликов с 8-разрядной глубиной цвета (256-цветовая емкость) требуется палитра для определения используемых цветов.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-107">Playing video clips with 8-bit color depth (256-color capacity) requires a palette to define the colors being used.</span></span> <span data-ttu-id="ecfb0-108">Иногда палитра, включенная в видеоролик, не является наиболее подходящей палитрой для использования во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-108">Sometimes, the palette included with a video clip is not the most appropriate palette to use during playback.</span></span> <span data-ttu-id="ecfb0-109">В этом случае МЦивнд предоставляет три способа управления палитрами для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-109">In this case, MCIWnd provides three ways to manage palettes for playback:</span></span>

-   <span data-ttu-id="ecfb0-110">Получите маркер для палитры, связанной с окном МЦивнд, с помощью макроса [**мЦивнджетпалетте**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) .</span><span class="sxs-lookup"><span data-stu-id="ecfb0-110">Retrieve a handle to the palette associated with an MCIWnd window by using the [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) macro.</span></span> <span data-ttu-id="ecfb0-111">Палитра не обязательно связана исключительно с окном МЦивнд.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-111">The palette is not necessarily associated exclusively with the MCIWnd window.</span></span> <span data-ttu-id="ecfb0-112">Другие приложения могут получить доступ к палитре и даже сделать недействительными.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-112">Other applications can access, and even invalidate, the palette handle.</span></span> <span data-ttu-id="ecfb0-113">Следовательно, приложение должно предвидеть глобальное использование палитры и, по завершении работы с палитрой, не должно освобождать ее.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-113">Consequently, your application should anticipate the global use of the palette and, when finished with the palette, should not free it.</span></span>
-   <span data-ttu-id="ecfb0-114">Укажите новую палитру для использования с видеороликом, связанным с окном МЦивнд, с помощью макроса [**мЦивндсетпалетте**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) .</span><span class="sxs-lookup"><span data-stu-id="ecfb0-114">Specify a new palette to use with the video clip associated with an MCIWnd window by using the [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) macro.</span></span>
-   <span data-ttu-id="ecfb0-115">Реализуйте палитру, связанную с окном МЦивнд, с системной палитрой с помощью макроса [**мЦивндреализе**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) .</span><span class="sxs-lookup"><span data-stu-id="ecfb0-115">Realize the palette associated with an MCIWnd window to the system palette by using the [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) macro.</span></span> <span data-ttu-id="ecfb0-116">Этот макрос вызывает функцию [**реализепалетте**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) с палитрой, связанной с окном мЦивнд.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-116">This macro calls the [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) function with the palette associated with the MCIWnd window.</span></span> <span data-ttu-id="ecfb0-117">Если обработчики сообщений приложения для [**WM \_ Палеттечанжед**](/windows/desktop/gdi/wm-palettechanged) и [**WM \_ Куериневпалетте**](/windows/desktop/gdi/wm-querynewpalette) вызывают только **реализепалетте** или **МЦивндреализе**, необходимо перенаправить эти сообщения в мЦивнд, если вы не обрабатываете их самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-117">If your application message handlers for [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) call only **RealizePalette** or **MCIWndRealize**, you must forward these messages to MCIWnd if you do not handle them yourself.</span></span>

> [!Note]  
> <span data-ttu-id="ecfb0-118">Когда видеоролик с 8-разрядной глубиной цвета загружается в окно МЦивнд, палитра, включенная в этот клип, заменяет палитру, связанную с окном МЦивнд.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-118">When a video clip with 8-bit color depth is loaded into the MCIWnd window, the palette included with that clip replaces the palette associated with the MCIWnd window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ecfb0-119">См. также</span><span class="sxs-lookup"><span data-stu-id="ecfb0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecfb0-120">Усовершенствования воспроизведения</span><span class="sxs-lookup"><span data-stu-id="ecfb0-120">Playback Enhancements</span></span>](playback-enhancements.md)
</dt> </dl>

 

 