---
title: Блокнот для сенсорного ввода Windows с помощью примера Real-Timeного пера (C#)
description: Пример использования сенсорного ввода Windows (Мтскратчпадртстилус) демонстрирует использование сообщений Windows Touch для рисования трассировок точек касания в окне.
ms.assetid: 8e80672f-0780-4dec-a9b4-afec0f7782ad
keywords:
- Windows Touch, примеры кода
- Windows Touch, пример кода
- Касание Windows, образцы для ввода пометок
- Образцы для ввода пометок
- Сенсорный экран Windows, объект пера в режиме реального времени (RTS)
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: 4cf9ab2e451dcdcaaee808083ca42c420778f231
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336303"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a>Блокнот для сенсорного ввода Windows с помощью примера Real-Timeного пера (C#)

Пример использования сенсорного ввода Windows ([мтскратчпадртстилус](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) демонстрирует использование сообщений Windows Touch для рисования трассировок точек касания в окне. Трассировка основного пальца, который был размещен на дигитайзере, сначала рисуется черным цветом. Дополнительные пальцы рисуются шестью цветами: красный, зеленый, синий, голубой, пурпурный и желтый. На следующем снимке экрана показано, как приложение может выглядеть при выполнении.

![снимок экрана с примером сенсорного ввода-вывода Windows с помощью пера в режиме реального времени на языке c с черной и красной волнистой линией на экране](images/mtscratchpadrtstyluscs.png)

В этом примере создается объект Real-Time пера (RTS), и включается поддержка нескольких точек контакта. Подключаемый модуль DynamicRenderer добавляется в RTS для отображения содержимого. Подключаемый модуль, Евенсандлерплугин, реализуется для наблюдения за количеством пальцев и изменения цвета, который рисуется динамическим модулем визуализации. При использовании обоих подключаемых модулей в стеке Plug-in RTS приложение Windows Touch помещает основное контактное лицо в черный, а остальные контакты — по различным цветам.

В следующем коде показано, как Евенсандлерплугин увеличивает и уменьшает количество контактов и задает цвет динамического модуля визуализации.

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

В следующем коде показано, как создается RTS с поддержкой нескольких точек контакта.

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

После изменения цвета объекта DynamicRenderer и прорисовки штрихов вызов DynamicRenderer:: Refresh приведет к появлению новых штрихов. В следующем коде показано, как это выполняется в методе Онпаинсандлер.

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

## <a name="related-topics"></a>См. также

[Многосенсорное приложение для ввода пометок (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [многосенсорный Блокнот (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [примеры Windows Touch](windows-touch-samples.md)
