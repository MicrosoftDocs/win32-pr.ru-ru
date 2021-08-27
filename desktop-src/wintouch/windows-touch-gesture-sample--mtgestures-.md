---
title: Windows Пример сенсорного жеста (Мтжестурес)
description: в этом разделе описывается пример сенсорного жеста Windows.
ms.assetid: 04166c9c-5de7-409e-9d5e-dd210a3a3f11
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
ms.openlocfilehash: 656b269eae779cd999680e165ba071d983d18526c2e9b873c5a916d61ccdb9f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110592"
---
# <a name="windows-touch-gesture-sample-mtgestures"></a>Windows Пример сенсорного жеста (Мтжестурес)

в этом разделе описывается пример сенсорного жеста Windows.

в образце Windows касание показано, как использовать сообщения жестов для преобразования, вращения и масштабирования поля, отображаемого интерфейс графических устройств (GDI), обрабатывая сообщение [**WM_GESTURE**](wm-gesture.md) . На следующем снимке экрана показано, как выглядит пример при его выполнении.

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

## <a name="related-topics"></a>Связанные темы

[приложение жестов с несколькими касаниями (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [приложение жестов с несколькими касаниями (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows примеры сенсорного ввода](windows-touch-samples.md)
