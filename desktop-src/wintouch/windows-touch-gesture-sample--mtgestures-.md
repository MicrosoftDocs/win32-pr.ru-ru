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
# <a name="windows-touch-gesture-sample-mtgestures"></a>Пример сенсорного жеста Windows (Мтжестурес)

В этом разделе описывается пример сенсорного жеста Windows.

В образце Windows Touch жестов показано, как использовать сообщения жестов для преобразования, вращения и масштабирования поля, отображаемого интерфейс графических устройств (GDI), обрабатывая сообщение [**WM_GESTURE**](wm-gesture.md) . На следующем снимке экрана показано, как выглядит пример при его выполнении.

![снимок экрана с образцом жеста касания Windows при его выполнении с повернутым, черно-белым прямоугольником на экране](images/mtgestures.png)

В этом примере сообщения жестов передаются в подсистему жестов, которая затем вызывает методы для рисования, вращения и масштабирования объекта, содержащего методы для обработки этих команд. Чтобы продемонстрировать, как работает пример, рассмотрите шаги по использованию команды касания с двумя пальцами для включения или отключения диагональных линий в подготовленном для просмотра окне. Пользователь выполняет жест касания с двумя пальцами, который создает сообщение, обрабатываемое программой. Когда сообщение обрабатывается, оно переключает логическое значение для отрисовки по диагонали в объекте-изображении, а объект затем отображает диагональные линии.

В следующем коде показано, как сообщения жестов передаются подсистеме жестов из метода WndProc.

```C++
    case WM_GESTURE:
        // The gesture-processing code is implemented in the CGestureEngine
        // class.
        return g_cGestureEngine.WndProc(hWnd,wParam,lParam);
        break;
```

В следующем коде показано, как подсистема жестов обрабатывает команду касания с двумя пальцами.

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

В следующем коде показано, как объект Drawing переключает свои диагональные линии.

```C++
void ToggleDrawDiagonals(void){_bDrawDiagonals = !_bDrawDiagonals;}
```

В следующем коде показано, как объект визуализирует диагональные линии в своем методе Draw.

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

## <a name="related-topics"></a>См. также

[Приложение жестов с несколькими касаниями (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [приложение жестов с несколькими касаниями (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [примеры для Windows Touch](windows-touch-samples.md)
