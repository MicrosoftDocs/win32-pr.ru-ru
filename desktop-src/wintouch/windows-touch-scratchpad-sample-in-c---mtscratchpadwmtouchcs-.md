---
title: Пример сенсорного ввода Windows в C (Мтскратчпадвмтаучкс)
description: Пример использования сенсорного ввода Windows в C# демонстрирует использование сообщений Windows Touch для рисования трассировок точек касания в окне.
ms.assetid: 652124be-01a8-4df4-b590-e5c2ca3f012c
keywords:
- Windows Touch, примеры кода
- Windows Touch, пример кода
- Касание Windows, образцы для ввода пометок
- Образцы для ввода пометок
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: 2d91c08c55f0d5b29a170a3a01c6ee882fad765f
ms.sourcegitcommit: c7fa8fc137714433c8d18b1bf71e9cf0b5bf5e80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/25/2020
ms.locfileid: "104070739"
---
# <a name="windows-touch-scratchpad-sample-c"></a>Пример сенсорного ввода Windows (C#)

[Пример использования сенсорного ввода Windows в C#](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS) демонстрирует использование сообщений Windows Touch для рисования трассировок точек касания в окне. Трассировка основного пальца, который был размещен на дигитайзере, сначала рисуется черным цветом. Дополнительные пальцы рисуются шестью цветами: красный, зеленый, синий, голубой, пурпурный и желтый. На следующем рисунке показано, как приложение может выглядеть при его запуске.

![снимок экрана, в котором на экране показан пример сенсорного ввода Windows на языке c, с черным, зеленым, синим и красным волнистым экраном](images/mtscratchpadwmtouchcs.png)

В этом примере создается сенсорная форма для обработки [**WM_TOUCH**](wm-touchdown.md) сообщений. Эта форма наследуется, чтобы включить Windows Touch в приложении для создания блокнота. Когда **WM_TOUCH** сообщения поступают в форму, они обрабатываются в точках и добавляются в коллекцию штрихов. Коллекция штрихов отображается в графическом объекте. В следующем коде показано, как сенсорная форма регистрируется для обработки **WM_TOUCH** сообщений и как она обрабатывает сообщения **WM_TOUCH** .

```CSharp
        private void OnLoadHandler(Object sender, EventArgs e)
        {
            try
            {
                // Registering the window for multi-touch, using the default settings.
                // p/invoking into user32.dll
                if (!RegisterTouchWindow(this.Handle, 0))
                {
                    Debug.Print("ERROR: Could not register window for multi-touch");
                }
            }
            catch (Exception exception)
            {
                Debug.Print("ERROR: RegisterTouchWindow API not available");
                Debug.Print(exception.ToString());
                MessageBox.Show("RegisterTouchWindow API not available", "MTScratchpadWMTouch ERROR",
                    MessageBoxButtons.OK, MessageBoxIcon.Error, MessageBoxDefaultButton.Button1, 0);
            }
        }
(...)
        [PermissionSet(SecurityAction.Demand, Name = "FullTrust")]
        protected override void WndProc(ref Message m)
        {
            // Decode and handle WM_TOUCH message.
            bool handled;
            switch (m.Msg)
            {
                case WM_TOUCH:
                    handled = DecodeTouch(ref m);
                    break;
                default:
                    handled = false;
                    break;
            }

            // Call parent WndProc for default message processing.
            base.WndProc(ref m);

            if (handled)
            {
                // Acknowledge event if handled.
                m.Result = new System.IntPtr(1);
            }
        }
```

В следующем коде показано, как интерпретируется сообщение касания Windows и добавляются данные в коллекции штрихов.

```CSharp
        private bool DecodeTouch(ref Message m)
        {
            // More than one touchinput may be associated with a touch message,
            // so an array is needed to get all event information.
            int inputCount = LoWord(m.WParam.ToInt32()); // Number of touch inputs, actual per-contact messages

            TOUCHINPUT[] inputs; // Array of TOUCHINPUT structures
            inputs = new TOUCHINPUT[inputCount]; // Allocate the storage for the parameters of the per-contact messages

            // Unpack message parameters into the array of TOUCHINPUT structures, each
            // representing a message for one single contact.
            if (!GetTouchInputInfo(m.LParam, inputCount, inputs, touchInputSize))
            {
                // Get touch info failed.
                return false;
            }

            // For each contact, dispatch the message to the appropriate message
            // handler.
            bool handled = false; // Boolean, is message handled
            for (int i = 0; i < inputCount; i++)
            {
                TOUCHINPUT ti = inputs[i];

                // Assign a handler to this message.
                EventHandler<WMTouchEventArgs> handler = null;     // Touch event handler
                if ((ti.dwFlags & TOUCHEVENTF_DOWN) != 0)
                {
                    handler = Touchdown;
                }
                else if ((ti.dwFlags & TOUCHEVENTF_UP) != 0)
                {
                    handler = Touchup;
                }
                else if ((ti.dwFlags & TOUCHEVENTF_MOVE) != 0)
                {
                    handler = TouchMove;
                }

                // Convert message parameters into touch event arguments and handle the event.
                if (handler != null)
                {
                    // Convert the raw touchinput message into a touchevent.
                    WMTouchEventArgs te = new WMTouchEventArgs(); // Touch event arguments

                    // TOUCHINFO point coordinates and contact size is in 1/100 of a pixel; convert it to pixels.
                    // Also convert screen to client coordinates.
                    te.ContactY = ti.cyContact/100;
                    te.ContactX = ti.cxContact/100;
                    te.Id = ti.dwID;
                    {
                        Point pt = PointToClient(new Point(ti.x/100, ti.y/100));
                        te.LocationX = pt.X;
                        te.LocationY = pt.Y;
                    }
                    te.Time = ti.dwTime;
                    te.Mask = ti.dwMask;
                    te.Flags = ti.dwFlags;

                    // Invoke the event handler.
                    handler(this, te);

                    // Mark this event as handled.
                    handled = true;
                }
            }

            CloseTouchInputHandle(m.LParam);

            return handled;
        }
    }
```

В следующем коде показано, как отображается коллекция штрихов.

```CSharp
        public void Draw(Graphics graphics)
        {
            if ((points.Count < 2) || (graphics == null))
            {
                return;
            }

            Pen pen = new Pen(color, penWidth);
            graphics.DrawLines(pen, (Point[]) points.ToArray(typeof(Point)));
        }
```

В следующем коде показано, как отдельные объекты Stroke отображаются с графическим объектом.

```CSharp
        public void Draw(Graphics graphics)
        {
            if(points.Count < 2 || graphics == null)
            {
                return;
            }

            Pen pen = new Pen(color, penWidth);
            graphics.DrawLines(pen, (Point[]) points.ToArray(typeof(Point)));
        }
```

## <a name="related-topics"></a>См. также

[Пример сенсорного ввода Windows (C++)](windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md), многофункциональное многофункциональное [приложение (WM_TOUCH/c #)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [многосенсорный Блокнот (WM_TOUCH/C + +)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), [примеры Windows Touch](windows-touch-samples.md)

