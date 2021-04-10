---
title: Пример с сенсорным блокнотом Windows (C++)
description: В примере с сенсорным вводом в Windows показано, как использовать сообщения касания Windows для рисования трассировок точек касания в окне.
ms.assetid: 6c4b4595-1e95-499c-b045-b5ae01aa5a6e
keywords:
- Windows Touch, примеры кода
- Windows Touch, пример кода
- Касание Windows, образцы для ввода пометок
- Образцы для ввода пометок
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: afdd39e886d97671942b4ff67a74c0da75924fbb
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104070822"
---
# <a name="windows-touch-scratchpad-sample-c"></a><span data-ttu-id="ae907-107">Пример с сенсорным блокнотом Windows (C++)</span><span class="sxs-lookup"><span data-stu-id="ae907-107">Windows Touch Scratchpad Sample (C++)</span></span>

<span data-ttu-id="ae907-108">В [примере с сенсорным вводом в Windows](https://github.com/MicrosoftDocs/win32-pr/blob/master/desktop-src/wintouch/windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md) показано, как использовать сообщения касания Windows для рисования трассировок точек касания в окне.</span><span class="sxs-lookup"><span data-stu-id="ae907-108">The [Windows Touch Scratchpad sample](https://github.com/MicrosoftDocs/win32-pr/blob/master/desktop-src/wintouch/windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md) shows how to use Windows Touch messages to draw traces of the touch points to a window.</span></span> <span data-ttu-id="ae907-109">Трассировка основного пальца, который был размещен на дигитайзере, сначала рисуется черным цветом.</span><span class="sxs-lookup"><span data-stu-id="ae907-109">The trace of the primary finger, the one that was put on the digitizer first, is drawn in black.</span></span> <span data-ttu-id="ae907-110">Дополнительные пальцы рисуются шестью цветами: красный, зеленый, синий, голубой, пурпурный и желтый.</span><span class="sxs-lookup"><span data-stu-id="ae907-110">Secondary fingers are drawn in six other colors: red, green, blue, cyan, magenta, and yellow.</span></span> <span data-ttu-id="ae907-111">На следующем рисунке показано, как приложение может выглядеть при выполнении.</span><span class="sxs-lookup"><span data-stu-id="ae907-111">The following image shows how the application could look while running.</span></span>

![снимок экрана с сенсорным блокнотом Windows с красной и черной волнистой линией на экране](images/mtscratchpadwmtouch.png)

<span data-ttu-id="ae907-113">Для этого приложения окно регистрируется в качестве сенсорного окна, сообщения сенсорного ввода обрабатываются для добавления точек касания к объектам Stroke, а рукописные штрихи отображаются на экране в обработчике сообщений **WM_PAINT** .</span><span class="sxs-lookup"><span data-stu-id="ae907-113">For this application, the window is registered as a touch window, touch messages are interpreted to add touch points to stroke objects, and ink strokes are rendered to the screen in the **WM_PAINT** message handler.</span></span>

<span data-ttu-id="ae907-114">В следующем коде показано, как окно регистрируется в качестве сенсорного окна.</span><span class="sxs-lookup"><span data-stu-id="ae907-114">The following code shows how the window is registered as a touch window.</span></span>

```C++
    // Register application window for receiving multitouch input. Use default settings.
    if(!RegisterTouchWindow(hWnd, 0))
    {
        MessageBox(hWnd, L"Cannot register application window for multitouch input", L"Error", MB_OK);
        return FALSE;
    }
```

<span data-ttu-id="ae907-115">В следующем коде показано, как сенсорные сообщения используются для добавления точек касания к рукописным штрихам.</span><span class="sxs-lookup"><span data-stu-id="ae907-115">The following code shows how touch messages are used to add touch points to ink strokes.</span></span>

```C++
        // WM_TOUCH message handlers
        case WM_TOUCH:
            {
                // WM_TOUCH message can contain several messages from different contacts
                // packed together.
                // Message parameters need to be decoded:
                unsigned int numInputs = (unsigned int) wParam; // Number of actual per-contact messages
                TOUCHINPUT* ti = new TOUCHINPUT[numInputs]; // Allocate the storage for the parameters of the per-contact messages
                if(ti == NULL)
                {
                    break;
                }
                // Unpack message parameters into the array of TOUCHINPUT structures, each
                // representing a message for one single contact.
                if(GetTouchInputInfo((HTOUCHINPUT)lParam, numInputs, ti, sizeof(TOUCHINPUT)))
                {
                    // For each contact, dispatch the message to the appropriate message
                    // handler.
                    for(unsigned int i=0; i<numInputs; ++i)
                    {
                        if(ti[i].dwFlags & TOUCHEVENTF_DOWN)
                        {
                            OnTouchDownHandler(hWnd, ti[i]);
                        }
                        else if(ti[i].dwFlags & TOUCHEVENTF_MOVE)
                        {
                            OnTouchMoveHandler(hWnd, ti[i]);
                        }
                        else if(ti[i].dwFlags & TOUCHEVENTF_UP)
                        {
                            OnTouchUpHandler(hWnd, ti[i]);
                        }
                    }
                }
                CloseTouchInputHandle((HTOUCHINPUT)lParam);
                delete [] ti;
            }
            break;
```

<span data-ttu-id="ae907-116">В следующем коде показано, как рукописные штрихи отображаются на экране в обработчике сообщений **WM_PAINT** .</span><span class="sxs-lookup"><span data-stu-id="ae907-116">The following code shows how the ink strokes are drawn to the screen in the **WM_PAINT** message handler.</span></span>

```C++
        case WM_PAINT:
            hdc = BeginPaint(hWnd, &ps);
            // Full redraw: draw complete collection of finished strokes and
            // also all the strokes that are currently in drawing.
            g_StrkColFinished.Draw(hdc);
            g_StrkColDrawing.Draw(hdc);
            EndPaint(hWnd, &ps);
            break;
```

<span data-ttu-id="ae907-117">В следующем коде показано, как объект Stroke отображает штрихи на экране.</span><span class="sxs-lookup"><span data-stu-id="ae907-117">The following code shows how the stroke object renders strokes to the screen.</span></span>

```C++
void CStroke::Draw(HDC hDC) const
{
    if(m_nCount < 2)
    {
        return;
    }

    HPEN hPen = CreatePen(PS_SOLID, 3, m_clr);
    HGDIOBJ hOldPen = SelectObject(hDC, hPen);
    Polyline(hDC, m_arrData, m_nCount);
    SelectObject(hDC, hOldPen);
    DeleteObject(hPen);
}
```

## <a name="related-topics"></a><span data-ttu-id="ae907-118">См. также</span><span class="sxs-lookup"><span data-stu-id="ae907-118">Related topics</span></span>

<span data-ttu-id="ae907-119">[Пример сенсорного ввода Windows (C#)](windows-touch-scratchpad-sample-in-c---mtscratchpadwmtouchcs-.md), многофункциональное [многосенсорное приложение (WM_TOUCH/c #)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [многосенсорный Блокнот (WM_TOUCH/C + +)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), [примеры Windows Touch](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="ae907-119">[Windows Touch Scratchpad Sample (C#)](windows-touch-scratchpad-sample-in-c---mtscratchpadwmtouchcs-.md), [Multi-touch Scratchpad Application (WM_TOUCH/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [Multi-touch Scratchpad Application (WM_TOUCH/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
