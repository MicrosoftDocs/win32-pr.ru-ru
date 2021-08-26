---
title: Windows Сенсорный Блокнот с помощью примера Real-Timeного пера (C#)
description: ознакомьтесь с примером Windows сенсорного блокнота C# (мтскратчпадртстилус), в котором показано, как использовать Windows сенсорные сообщения для рисования трассировок точек касания в окне.
ms.assetid: 8e80672f-0780-4dec-a9b4-afec0f7782ad
keywords:
- Windows Сенсорный ввод, примеры кода
- Windows Сенсорный ввод, пример кода
- Windows Сенсорный ввод, образцы для ввода пометок
- Образцы для ввода пометок
- Windows Сенсорный ввод, объект пера в режиме реального времени (RTS)
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: a76f7a66f8bc26b7e1cad8f1fa71d9703f0c0da1ad1452a078b374a0f1603238
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055853"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a>Windows Сенсорный Блокнот с помощью примера Real-Timeного пера (C#)

в Windows примере с сенсорным блокнотом ([мтскратчпадртстилус](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) показано, как использовать Windows сенсорные сообщения для рисования трассировок точек касания в окне. Трассировка основного пальца, который был размещен на дигитайзере, сначала рисуется черным цветом. Дополнительные пальцы рисуются шестью цветами: красный, зеленый, синий, голубой, пурпурный и желтый. На следующем снимке экрана показано, как приложение может выглядеть при выполнении.

![снимок экрана с примером сенсорного ввода-вывода Windows с помощью пера в режиме реального времени на языке c с черной и красной волнистой линией на экране](images/mtscratchpadrtstyluscs.png)

В этом примере создается объект Real-Time пера (RTS), и включается поддержка нескольких точек контакта. Подключаемый модуль DynamicRenderer добавляется в RTS для отображения содержимого. Подключаемый модуль, Евенсандлерплугин, реализуется для наблюдения за количеством пальцев и изменения цвета, который рисуется динамическим модулем визуализации. при использовании обоих подключаемых модулей в стеке plug-in RTS приложение Windows Touch блокнот будет отображать основной контакт в черном, а остальные — в различных цветах.

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

## <a name="related-topics"></a>Связанные темы

многофункциональное [приложение для ввода пометок (rts/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [многосенсорный блокнот (rts/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [Windows примеры сенсорного ввода](windows-touch-samples.md)
