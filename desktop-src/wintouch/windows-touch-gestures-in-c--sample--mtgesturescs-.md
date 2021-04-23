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
# <a name="windows-touch-gestures-in-c-sample-mtgesturescs"></a><span data-ttu-id="2e5ca-110">Жесты касания Windows в C# — пример (Мтжестурескс)</span><span class="sxs-lookup"><span data-stu-id="2e5ca-110">Windows Touch Gestures in C# Sample (MTGesturesCS)</span></span>

<span data-ttu-id="2e5ca-111">В этом разделе описывается пример использования сенсорных жестов Windows в C#.</span><span class="sxs-lookup"><span data-stu-id="2e5ca-111">This section describes the Windows Touch Gestures sample in C#.</span></span>

<span data-ttu-id="2e5ca-112">В этом образце сенсорных жестов Windows показано, как использовать сообщения жестов для преобразования, вращения и масштабирования поля, отображаемого интерфейс графических устройств (GDI), обрабатывая сообщение [**WM_GESTURE**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="2e5ca-112">This Windows Touch Gestures sample demonstrates how to use gesture messages to translate, rotate, and scale a box rendered by the Graphics Device Interface (GDI) by handling the [**WM_GESTURE**](wm-gesture.md) message.</span></span> <span data-ttu-id="2e5ca-113">На следующем снимке экрана показано, как выглядит пример при его выполнении.</span><span class="sxs-lookup"><span data-stu-id="2e5ca-113">The following screen shot shows how the sample looks when it is running.</span></span>

![снимок экрана, в котором показаны жесты касания Windows на языке c, когда он выполняется, со черно-белым прямоугольником, выровненным по центру экрана](images/mtgesturescs.png)

<span data-ttu-id="2e5ca-115">В этом примере сообщения жестов передаются в подсистему жеста, которая затем вызывает методы для рисования, вращения и масштабирования объекта, содержащего методы для обработки этих команд.</span><span class="sxs-lookup"><span data-stu-id="2e5ca-115">For this sample, gesture messages are passed to a gesture engine which then calls methods on drawing objects to translate, rotate, and scale an object that has methods for handling these commands.</span></span> <span data-ttu-id="2e5ca-116">Чтобы сделать это возможным в C#, создается специальная форма Таучаблеформ для управления сообщениями жестов.</span><span class="sxs-lookup"><span data-stu-id="2e5ca-116">To make this possible in C#, a special form, TouchableForm, is created to handle gesture messages.</span></span> <span data-ttu-id="2e5ca-117">Затем эта форма использует сообщения для внесения изменений в объект Drawing, Дравингобжект, для изменения способа отрисовки объекта в методе Paint.</span><span class="sxs-lookup"><span data-stu-id="2e5ca-117">This form then uses the messages to make changes on a drawing object, DrawingObject, to change how the object renders in the Paint method.</span></span>

<span data-ttu-id="2e5ca-118">Чтобы продемонстрировать работу образца, ознакомьтесь с инструкциями по использованию команды Pan для перевода подготовленного к просмотру поля.</span><span class="sxs-lookup"><span data-stu-id="2e5ca-118">To help show how the sample works, consider the steps for using the pan command to translate the rendered box.</span></span> <span data-ttu-id="2e5ca-119">Пользователь выполняет жест панорамирования, который создает [**WM_GESTURE**](wm-gesture.md) сообщение с идентификатором жеста GID_PAN.</span><span class="sxs-lookup"><span data-stu-id="2e5ca-119">A user performs the pan gesture which generates a [**WM_GESTURE**](wm-gesture.md) message with the gesture identifier GID_PAN.</span></span> <span data-ttu-id="2e5ca-120">Таучаблеформ обрабатывает эти сообщения и обновляет расположение объекта Drawing, а объект преобразуется в преобразованный.</span><span class="sxs-lookup"><span data-stu-id="2e5ca-120">The TouchableForm handles this messages and updates the position of the drawing object, and the object will then render itself translated.</span></span>

<span data-ttu-id="2e5ca-121">В следующем коде показано, как обработчик жестов извлекает параметры из [**WM_GESTURE**](wm-gesture.md) сообщения, а затем выполняет перевод для отрисованного окна с помощью вызова метода Move объекта Drawing.</span><span class="sxs-lookup"><span data-stu-id="2e5ca-121">The following code shows how the gesture handler retrieves parameters from the [**WM_GESTURE**](wm-gesture.md) message and then performs translation on the rendered box through a call to the drawing object's move method.</span></span>

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

<span data-ttu-id="2e5ca-122">В следующем коде показано, как метод Move объекта Drawing обновляет внутренние переменные положения.</span><span class="sxs-lookup"><span data-stu-id="2e5ca-122">The following code shows how the drawing object's move method updates internal position variables.</span></span>

```CSharp
        public void Move(int deltaX,int deltaY)
        {
            _ptCenter.X += deltaX;
            _ptCenter.Y += deltaY;
        }
```

<span data-ttu-id="2e5ca-123">В следующем коде показано, как используется значение в методе Paint объекта Drawing.</span><span class="sxs-lookup"><span data-stu-id="2e5ca-123">The following code shows how the position is used in the drawing object's paint method.</span></span>

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

<span data-ttu-id="2e5ca-124">Жесты панорамирования приводят к тому, что отображаемое поле будет отображаться в преобразованном виде.</span><span class="sxs-lookup"><span data-stu-id="2e5ca-124">Pan gestures will cause the drawn box to be rendered translated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e5ca-125">См. также</span><span class="sxs-lookup"><span data-stu-id="2e5ca-125">Related topics</span></span>

<span data-ttu-id="2e5ca-126">[Приложение жестов с несколькими касаниями (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [приложение жестов с несколькими касаниями (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [примеры для Windows Touch](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="2e5ca-126">[Multi-touch Gestures Application (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [Multi-touch Gestures Application (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
