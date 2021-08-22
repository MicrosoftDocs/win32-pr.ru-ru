---
title: Рисование с использованием Direct2D
description: После создания графических ресурсов можно приступать к рисованию.
ms.assetid: a73f7043-dffc-4688-adfc-16ed9a9e12d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d8a346300b32fe1c716e51efe6bfb8fdbf6220fb2ff17df6de617de27ba1a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535083"
---
# <a name="drawing-with-direct2d"></a>Рисование с использованием Direct2D

После создания графических ресурсов можно приступать к рисованию.

## <a name="drawing-an-ellipse"></a>Рисование эллипса

Программа [Circle](your-first-direct2d-program.md) выполняет очень простую логику рисования:

1.  Заполните фон сплошным цветом.
2.  Рисование заполненного круга.

![снимок экрана программы круга.](images/graphics08.png)

Так как целевой объект прорисовки является окном (а не точечным рисунком или другой заданной областью), рисование выполняется в ответ на сообщения [**\_ рисования WM**](/windows/desktop/gdi/wm-paint) . В следующем коде показана процедура окна для круговой программы.


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        case WM_PAINT:
            OnPaint();
            return 0;

         // Other messages not shown...
    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```

Вот код, который рисует окружность.

```C++
void MainWindow::OnPaint()
{
    HRESULT hr = CreateGraphicsResources();
    if (SUCCEEDED(hr))
    {
        PAINTSTRUCT ps;
        BeginPaint(m_hwnd, &ps);
     
        pRenderTarget->BeginDraw();

        pRenderTarget->Clear( D2D1::ColorF(D2D1::ColorF::SkyBlue) );
        pRenderTarget->FillEllipse(ellipse, pBrush);

        hr = pRenderTarget->EndDraw();
        if (FAILED(hr) || hr == D2DERR_RECREATE_TARGET)
        {
            DiscardGraphicsResources();
        }
        EndPaint(m_hwnd, &ps);
    }
}
```



Интерфейс [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) используется для всех операций рисования. `OnPaint`Метод программы выполняет следующие действия:

1.  Метод [**ID2D1RenderTarget:: бегиндрав**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) сигнализирует о начале рисования.
2.  Метод [**ID2D1RenderTarget:: Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) заполняет весь целевой объект отрисовки сплошным цветом. Цвет задается в виде структуры [**D2D1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) . Для инициализации структуры можно использовать класс [**D2D1:: колорф**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) . Дополнительные сведения см. [в разделе Использование цвета в Direct2D](using-color-in-direct2d.md).
3.  Метод [**ID2D1RenderTarget:: филлеллипсе**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) Рисует закрашенный эллипс, используя указанную кисть для заливки. Эллипс задается центральной точкой и осями x и y. Если оси x и y одинаковы, результатом будет окружность.
4.  Метод [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) сигнализирует о завершении рисования для этого кадра. Все операции рисования должны размещаться между вызовами [**бегиндрав**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) и **EndDraw**.

Методы [**бегиндрав**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw), [**clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear)и [**филлеллипсе**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) имеют тип возвращаемого значения **void** . Если во время выполнения любого из этих методов возникает ошибка, то эта ошибка сообщается через возвращаемое значение метода [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . `CreateGraphicsResources`Метод показан в разделе [Создание ресурсов Direct2D](render-targets--devices--and-resources.md). Этот метод создает целевой объект отрисовки и Кисть сплошного цвета.

Устройство может буферизовать команды рисования и откладывать их выполнение до тех пор, пока не будет вызван [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Можно заставить устройство выполнять любые ожидающие команды рисования, вызывая [**ID2D1RenderTarget:: Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush). Однако при сбросе может снизиться производительность.

## <a name="handling-device-loss"></a>Обработка потери устройства

Во время выполнения программы используемое графическое устройство может стать недоступным. Например, устройство может быть потеряно при изменении разрешения экрана или при удалении пользователем видеоадаптера. Если устройство потеряно, то целевой объект рендеринга также становится недействительным, наряду с ресурсами, зависящими от устройства, которые были связаны с устройством. Direct2D передает потерянное устройство, возвращая код ошибки **D2DERR \_ Повторное создание \_ целевого объекта** из метода [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Если вы получаете этот код ошибки, необходимо повторно создать целевой объект рендеринга и все ресурсы, зависящие от устройства.

Чтобы отменить ресурс, просто освободите интерфейс для этого ресурса.


```C++
void MainWindow::DiscardGraphicsResources()
{
    SafeRelease(&pRenderTarget);
    SafeRelease(&pBrush);
}
```



Создание ресурса может быть дорогостоящей операцией, поэтому не следует повторно создавать ресурсы для каждого сообщения [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) . Создайте ресурс один раз и кэшировать указатель ресурса, пока ресурс не станет недопустимым из-за потери устройства или пока не будет нужен ресурс.

## <a name="the-direct2d-render-loop"></a>Цикл рендеринга Direct2D

Независимо от того, что вы рисуете, программа должна выполнить цикл, аналогичный приведенному ниже.

1.  Создание ресурсов, независимых от устройства.
2.  Отрисовка сцены.
    1.  Проверьте, существует ли допустимый целевой объект рендеринга. В противном случае создайте целевой объект рендеринга и ресурсы, зависящие от устройства.
    2.  Вызовите [**ID2D1RenderTarget:: бегиндрав**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).
    3.  Выдача команд рисования.
    4.  Вызовите [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).
    5.  Если [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) возвращает **\_ \_ целевой объект D2DERR recreate**, удалите целевой объект рендеринга и ресурсы, зависящие от устройства.
3.  Повторите шаг 2 при необходимости обновить или перерисовать сцену.

Если целевой объект прорисовки является окном, шаг 2 возникает каждый раз, когда окно получает сообщение [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) .

Приведенный здесь цикл обрабатывает потери устройства, удаляя ресурсы, зависящие от устройства, и повторно создавая их в начале следующего цикла (шаг 2A).

## <a name="next"></a>Следующая

[DPI и Device-Independent пикселей](dpi-and-device-independent-pixels.md)

 

 