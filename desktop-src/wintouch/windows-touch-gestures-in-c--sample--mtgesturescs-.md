---
title: Жесты касания Windows в образце C (Мтжестурескс)
description: В этом разделе описывается пример использования сенсорных жестов Windows в C.
ms.assetid: 4b2d70bb-47e4-4448-97e2-6f6e29d1dfdf
keywords:
- Windows Touch, примеры кода
- Windows Touch, пример кода
- Касание Windows, жесты
- Сенсорные примеры для Windows, жесты
- Примеры жестов
- жесты, пример кода
- жесты, примеры кода
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: e6ffc0e8caf63807d4df80a1b96229f2fa7b5ff9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412501"
---
# <a name="windows-touch-gestures-in-c-sample-mtgesturescs"></a>Жесты касания Windows в C# — пример (Мтжестурескс)

В этом разделе описывается пример использования сенсорных жестов Windows в C#.

В этом образце сенсорных жестов Windows показано, как использовать сообщения жестов для преобразования, вращения и масштабирования поля, отображаемого интерфейс графических устройств (GDI), обрабатывая сообщение [**WM_GESTURE**](wm-gesture.md) . На следующем снимке экрана показано, как выглядит пример при его выполнении.

![снимок экрана, в котором показаны жесты касания Windows на языке c, когда он выполняется, со черно-белым прямоугольником, выровненным по центру экрана](images/mtgesturescs.png)

В этом примере сообщения жестов передаются в подсистему жеста, которая затем вызывает методы для рисования, вращения и масштабирования объекта, содержащего методы для обработки этих команд. Чтобы сделать это возможным в C#, создается специальная форма Таучаблеформ для управления сообщениями жестов. Затем эта форма использует сообщения для внесения изменений в объект Drawing, Дравингобжект, для изменения способа отрисовки объекта в методе Paint.

Чтобы продемонстрировать работу образца, ознакомьтесь с инструкциями по использованию команды Pan для перевода подготовленного к просмотру поля. Пользователь выполняет жест панорамирования, который создает [**WM_GESTURE**](wm-gesture.md) сообщение с идентификатором жеста GID_PAN. Таучаблеформ обрабатывает эти сообщения и обновляет расположение объекта Drawing, а объект преобразуется в преобразованный.

В следующем коде показано, как обработчик жестов извлекает параметры из [**WM_GESTURE**](wm-gesture.md) сообщения, а затем выполняет перевод для отрисованного окна с помощью вызова метода Move объекта Drawing.

```CSharp
            switch (gi.dwID)
            {
                case GID_BEGIN:
                case GID_END:
                    break;
               (...)
                case GID_PAN:
                    switch (gi.dwFlags)
                    {
                        case GF_BEGIN:
                            _ptFirst.X = gi.ptsLocation.x;
                            _ptFirst.Y = gi.ptsLocation.y;
                            _ptFirst = PointToClient(_ptFirst);
                            break;

                        default:
                            // We read the second point of this gesture. It is a
                            // middle point between fingers in this new position
                            _ptSecond.X = gi.ptsLocation.x;
                            _ptSecond.Y = gi.ptsLocation.y;
                            _ptSecond = PointToClient(_ptSecond);

                            // We apply move operation of the object
                            _dwo.Move(_ptSecond.X - _ptFirst.X, _ptSecond.Y - _ptFirst.Y);

                            Invalidate();

                            // We have to copy second point into first one to
                            // prepare for the next step of this gesture.
                            _ptFirst = _ptSecond;
                            break;
                    }
                    break;
```

В следующем коде показано, как метод Move объекта Drawing обновляет внутренние переменные положения.

```CSharp
        public void Move(int deltaX,int deltaY)
        {
            _ptCenter.X += deltaX;
            _ptCenter.Y += deltaY;
        }
```

В следующем коде показано, как используется значение в методе Paint объекта Drawing.

```CSharp
public void Paint(Graphics graphics)
        {
(...)
            for (int j = 0; j < 5; j++)
            {
                int idx = arrPts[j].X;
                int idy = arrPts[j].Y;

                // rotation
                arrPts[j].X = (int)(idx * dCos + idy * dSin);
                arrPts[j].Y = (int)(idy * dCos - idx * dSin);

                // translation
                arrPts[j].X += _ptCenter.X;
                arrPts[j].Y += _ptCenter.Y;
            }
(...)
        }
```

Жесты панорамирования приводят к тому, что отображаемое поле будет отображаться в преобразованном виде.

## <a name="related-topics"></a>См. также

[Приложение жестов с несколькими касаниями (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [приложение жестов с несколькими касаниями (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [примеры для Windows Touch](windows-touch-samples.md)
