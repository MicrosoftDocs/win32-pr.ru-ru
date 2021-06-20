---
title: Блокнот для сенсорного ввода Windows с помощью примера Real-Timeного пера (C#)
description: Ознакомьтесь с примером примера C# для сенсорного ввода в Windows (Мтскратчпадртстилус), который показывает, как использовать сообщения Windows Touch для рисования трассировок точек касания в окне.
ms.assetid: 8e80672f-0780-4dec-a9b4-afec0f7782ad
keywords:
- Windows Touch, примеры кода
- Windows Touch, пример кода
- Касание Windows, образцы для ввода пометок
- Образцы для ввода пометок
- Сенсорный экран Windows, объект пера в режиме реального времени (RTS)
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: 3c30d3543024a48394ddd7b9b2b06a05b61f5025
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406317"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a><span data-ttu-id="0ff4a-108">Блокнот для сенсорного ввода Windows с помощью примера Real-Timeного пера (C#)</span><span class="sxs-lookup"><span data-stu-id="0ff4a-108">Windows Touch Scratchpad using the Real-Time Stylus Sample (C#)</span></span>

<span data-ttu-id="0ff4a-109">Пример использования сенсорного ввода Windows ([мтскратчпадртстилус](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) демонстрирует использование сообщений Windows Touch для рисования трассировок точек касания в окне.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-109">The Windows Touch Scratchpad sample ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) shows how to use Windows Touch messages to draw traces of the touch points to a window.</span></span> <span data-ttu-id="0ff4a-110">Трассировка основного пальца, который был размещен на дигитайзере, сначала рисуется черным цветом.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-110">The trace of the primary finger, the one that was put on the digitizer first, is drawn in black.</span></span> <span data-ttu-id="0ff4a-111">Дополнительные пальцы рисуются шестью цветами: красный, зеленый, синий, голубой, пурпурный и желтый.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-111">Secondary fingers are drawn in six other colors: red, green, blue, cyan, magenta and yellow.</span></span> <span data-ttu-id="0ff4a-112">На следующем снимке экрана показано, как приложение может выглядеть при выполнении.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-112">The following screen shot shows how the application could look while running.</span></span>

![снимок экрана с примером сенсорного ввода-вывода Windows с помощью пера в режиме реального времени на языке c с черной и красной волнистой линией на экране](images/mtscratchpadrtstyluscs.png)

<span data-ttu-id="0ff4a-114">В этом примере создается объект Real-Time пера (RTS), и включается поддержка нескольких точек контакта.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-114">For this sample, the Real-Time Stylus (RTS) object is created and support for multiple contact points is enabled.</span></span> <span data-ttu-id="0ff4a-115">Подключаемый модуль DynamicRenderer добавляется в RTS для отображения содержимого.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-115">A DynamicRenderer plug-in is added to the RTS to render content.</span></span> <span data-ttu-id="0ff4a-116">Подключаемый модуль, Евенсандлерплугин, реализуется для наблюдения за количеством пальцев и изменения цвета, который рисуется динамическим модулем визуализации.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-116">A plug-in, EventHandlerPlugIn, is implemented to track down the number of fingers and to change the color that the dynamic renderer is drawing.</span></span> <span data-ttu-id="0ff4a-117">При использовании обоих подключаемых модулей в стеке Plug-in RTS приложение Windows Touch помещает основное контактное лицо в черный, а остальные контакты — по различным цветам.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-117">With both plug-ins in the RTS plug-in stack, the Windows Touch Scratchpad application will render the primary contact in black and the rest of the contacts in the various colors.</span></span>

<span data-ttu-id="0ff4a-118">В следующем коде показано, как Евенсандлерплугин увеличивает и уменьшает количество контактов и задает цвет динамического модуля визуализации.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-118">The following code shows how the EventHandlerPlugIn increments and decrements a count of the number of contacts and sets the color of the dynamic renderer.</span></span>

```CSharp
        public void StylusDown(RealTimeStylus sender, StylusDownData data)
        {
            // Set new stroke color to the DrawingAttributes of the DynamicRenderer
            // If there are no fingers down, this is a primary contact
            dynamicRenderer.DrawingAttributes.Color = touchColor.GetColor(cntContacts == 0);

            ++cntContacts;  // Increment finger-down counter
        }

        public void StylusUp(RealTimeStylus sender, StylusUpData data)
        {
            --cntContacts;  // Decrement finger-down counter
        }
```

<span data-ttu-id="0ff4a-119">В следующем коде показано, как создается RTS с поддержкой нескольких точек контакта.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-119">The following code shows how the RTS is created with multiple contact point support.</span></span>

```CSharp
        private void OnLoadHandler(Object sender, EventArgs e)
        {
            // Create RealTimeStylus object and enable it for multi-touch
            realTimeStylus = new RealTimeStylus(this);
            realTimeStylus.MultiTouchEnabled = true;

            // Create DynamicRenderer and event handler, and add them to the RTS object as synchronous plugins
            dynamicRenderer = new DynamicRenderer(this);
            eventHandler = new EventHandlerPlugIn(this.CreateGraphics(), dynamicRenderer);
            realTimeStylus.SyncPluginCollection.Add(eventHandler);
            realTimeStylus.SyncPluginCollection.Add(dynamicRenderer);

            // Enable RTS and DynamicRenderer object, and enable auto-redraw of the DynamicRenderer
            realTimeStylus.Enabled = true;
            dynamicRenderer.Enabled = true;
            dynamicRenderer.EnableDataCache = true;
        }
```

<span data-ttu-id="0ff4a-120">После изменения цвета объекта DynamicRenderer и прорисовки штрихов вызов DynamicRenderer:: Refresh приведет к появлению новых штрихов.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-120">After the DynamicRenderer object's color has changed and strokes have been drawn, a call to DynamicRenderer::Refresh will cause the new strokes to appear.</span></span> <span data-ttu-id="0ff4a-121">В следующем коде показано, как это выполняется в методе Онпаинсандлер.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-121">The following code shows how this is performed in the OnPaintHandler method.</span></span>

```CSharp
        private void OnPaintHandler(object sender, PaintEventArgs e)
        {
            // Erase the background
            Brush brush = new SolidBrush(SystemColors.Window);
            e.Graphics.FillRectangle(brush, ClientRectangle);

            // Ask DynamicRenderer to redraw itself
            dynamicRenderer.Refresh();
        }
```

## <a name="related-topics"></a><span data-ttu-id="0ff4a-122">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="0ff4a-122">Related topics</span></span>

<span data-ttu-id="0ff4a-123">[Многосенсорное приложение для ввода пометок (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [многосенсорный Блокнот (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [примеры Windows Touch](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="0ff4a-123">[Multi-touch Scratchpad Application (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [Multi-touch Scratchpad Application (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
