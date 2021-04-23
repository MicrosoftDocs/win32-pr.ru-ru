---
title: Пример сенсорного жеста Windows (Мтжестурес)
description: В этом разделе описывается пример сенсорного жеста Windows.
ms.assetid: 04166c9c-5de7-409e-9d5e-dd210a3a3f11
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
ms.openlocfilehash: 0e01d97e844af37caeb5c33f3cb780601da4629d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788724"
---
# <a name="windows-touch-gesture-sample-mtgestures"></a><span data-ttu-id="604d0-110">Пример сенсорного жеста Windows (Мтжестурес)</span><span class="sxs-lookup"><span data-stu-id="604d0-110">Windows Touch Gesture Sample (MTGestures)</span></span>

<span data-ttu-id="604d0-111">В этом разделе описывается пример сенсорного жеста Windows.</span><span class="sxs-lookup"><span data-stu-id="604d0-111">This section describes the Windows Touch Gesture sample.</span></span>

<span data-ttu-id="604d0-112">В образце Windows Touch жестов показано, как использовать сообщения жестов для преобразования, вращения и масштабирования поля, отображаемого интерфейс графических устройств (GDI), обрабатывая сообщение [**WM_GESTURE**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="604d0-112">The Windows Touch Gesture sample demonstrates how to use gesture messages to translate, rotate, and scale a box rendered by the Graphics Device Interface (GDI) by handling the [**WM_GESTURE**](wm-gesture.md) message.</span></span> <span data-ttu-id="604d0-113">На следующем снимке экрана показано, как выглядит пример при его выполнении.</span><span class="sxs-lookup"><span data-stu-id="604d0-113">The following screen shot shows how the sample looks when it is running.</span></span>

![снимок экрана с образцом жеста касания Windows при его выполнении с повернутым, черно-белым прямоугольником на экране](images/mtgestures.png)

<span data-ttu-id="604d0-115">В этом примере сообщения жестов передаются в подсистему жестов, которая затем вызывает методы для рисования, вращения и масштабирования объекта, содержащего методы для обработки этих команд.</span><span class="sxs-lookup"><span data-stu-id="604d0-115">For this sample, gesture messages are passed to a gesture engine, which then calls methods on drawing objects to translate, rotate, and scale an object that has methods for handling these commands.</span></span> <span data-ttu-id="604d0-116">Чтобы продемонстрировать, как работает пример, рассмотрите шаги по использованию команды касания с двумя пальцами для включения или отключения диагональных линий в подготовленном для просмотра окне.</span><span class="sxs-lookup"><span data-stu-id="604d0-116">To help show how the sample works, consider the steps for using the two-finger tap command to enable or disable diagonal lines in the rendered box.</span></span> <span data-ttu-id="604d0-117">Пользователь выполняет жест касания с двумя пальцами, который создает сообщение, обрабатываемое программой.</span><span class="sxs-lookup"><span data-stu-id="604d0-117">A user performs the two-finger tap gesture, which generates a message that is handled by the program.</span></span> <span data-ttu-id="604d0-118">Когда сообщение обрабатывается, оно переключает логическое значение для отрисовки по диагонали в объекте-изображении, а объект затем отображает диагональные линии.</span><span class="sxs-lookup"><span data-stu-id="604d0-118">When the message is handled, it will toggle a Boolean for rendering diagonals on the drawing object, and the object will then render the diagonal lines.</span></span>

<span data-ttu-id="604d0-119">В следующем коде показано, как сообщения жестов передаются подсистеме жестов из метода WndProc.</span><span class="sxs-lookup"><span data-stu-id="604d0-119">The following code shows how gesture messages are passed to the gesture engine from the WndProc method.</span></span>

```C++
    case WM_GESTURE:
        // The gesture-processing code is implemented in the CGestureEngine
        // class.
        return g_cGestureEngine.WndProc(hWnd,wParam,lParam);
        break;
```

<span data-ttu-id="604d0-120">В следующем коде показано, как подсистема жестов обрабатывает команду касания с двумя пальцами.</span><span class="sxs-lookup"><span data-stu-id="604d0-120">The following code shows how the gesture engine handles the two-finger tap command.</span></span>

```C++
// Two-finger tap command
void CMyGestureEngine::ProcessTwoFingerTap(void)
{
    if(_pcRect)
    {
        _pcRect->ToggleDrawDiagonals();
    }
}
```

<span data-ttu-id="604d0-121">В следующем коде показано, как объект Drawing переключает свои диагональные линии.</span><span class="sxs-lookup"><span data-stu-id="604d0-121">The following code shows how the drawing object toggles its diagonals.</span></span>

```C++
void ToggleDrawDiagonals(void){_bDrawDiagonals = !_bDrawDiagonals;}
```

<span data-ttu-id="604d0-122">В следующем коде показано, как объект визуализирует диагональные линии в своем методе Draw.</span><span class="sxs-lookup"><span data-stu-id="604d0-122">The following code shows how the object renders diagonal lines in its draw method.</span></span>

```C++
    if(_bDrawDiagonals)
    {
        // draw diagonals
        MoveToEx(hdc,ptRect[0].x,ptRect[0].y,NULL);
        LineTo(hdc,ptRect[2].x,ptRect[2].y);
        MoveToEx(hdc,ptRect[1].x,ptRect[1].y,NULL);
        LineTo(hdc,ptRect[3].x,ptRect[3].y);
    }
```

## <a name="related-topics"></a><span data-ttu-id="604d0-123">См. также</span><span class="sxs-lookup"><span data-stu-id="604d0-123">Related topics</span></span>

<span data-ttu-id="604d0-124">[Приложение жестов с несколькими касаниями (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [приложение жестов с несколькими касаниями (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [примеры для Windows Touch](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="604d0-124">[Multi-touch Gestures Application (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [Multi-touch Gestures Application (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
