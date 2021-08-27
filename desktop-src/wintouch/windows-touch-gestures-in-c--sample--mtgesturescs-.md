---
title: Windows Сенсорные жесты в образце C (Мтжестурескс)
description: в этом разделе описан пример Windows сенсорных жестов в C \.
ms.assetid: 4b2d70bb-47e4-4448-97e2-6f6e29d1dfdf
keywords:
- Windows Сенсорный ввод, примеры кода
- Windows Сенсорный ввод, пример кода
- Windows Касание, жесты
- Windows Сенсорный ввод, примеры жестов
- Примеры жестов
- жесты, пример кода
- жесты, примеры кода
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: ac3a7c0772ad7329d14d9909b55f8a60ef6e7d7473a06fcba921297117a00b6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089912"
---
# <a name="windows-touch-gestures-in-c-sample-mtgesturescs"></a>Windows Сенсорные жесты в C# — пример (Мтжестурескс)

в этом разделе описывается пример сенсорных жестов Windows в C#.

в этом Windows примере сенсорных жестов показано, как использовать сообщения жестов для преобразования, вращения и масштабирования поля, отображаемого интерфейс графических устройств (GDI), обрабатывая сообщение [**WM_GESTURE**](wm-gesture.md) . На следующем снимке экрана показано, как выглядит пример при его выполнении.

![снимок экрана, в котором показаны жесты касания Windows на языке c, когда он выполняется, со черно-белым прямоугольником, выровненным по центру экрана](images/mtgesturescs.png)

В этом примере сообщения жестов передаются в подсистему жеста, которая затем вызывает методы для рисования, вращения и масштабирования объекта, содержащего методы для обработки этих команд. Чтобы сделать это возможным в C#, создается специальная форма Таучаблеформ для управления сообщениями жестов. затем эта форма использует сообщения для внесения изменений в объект drawing, дравингобжект, чтобы изменить способ отрисовки объекта в методе Paint.

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

## <a name="related-topics"></a>Связанные темы

[приложение жестов с несколькими касаниями (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [приложение жестов с несколькими касаниями (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows примеры сенсорного ввода](windows-touch-samples.md)
