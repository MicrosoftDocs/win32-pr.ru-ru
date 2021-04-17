---
title: Перемещение мыши
description: Перемещение мыши
ms.assetid: 54366E9B-470A-4155-8A5F-425BAC8AC1A5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14176310882651cdeb2939d0db55368ff133ea11
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "105684720"
---
# <a name="mouse-movement"></a>Перемещение мыши

При перемещении мыши Windows отправляет сообщение [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) . По умолчанию **WM \_ MOUSEMOVE** перемещается в окно, содержащее курсор. Это поведение можно переопределить, *записывая* мышь, которая описана в следующем разделе.

Сообщение [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) содержит те же параметры, что и сообщения для щелчков мыши. Младшие 16 бит *lParam* содержат координату x, а следующие 16 бит содержат координату y. Используйте макросы [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) и [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) для распаковки координат из *lParam*. Параметр *wParam* содержит побитовое **или** для флагов, указывающих состояние других кнопок мыши, а также клавиши Shift и CTRL. Следующий код получает координаты мыши от *lParam*.


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



Помните, что эти координаты находятся в пикселях, а не в аппаратно-независимых пикселях (DIP). Далее в этом разделе мы рассмотрим код, который выполняет преобразование между двумя единицами.

Окно также может получить сообщение [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) , если положения курсора меняются относительно окна. Например, если курсор находится над окном, а пользователь скрывает окно, окно получает сообщения **WM \_ MOUSEMOVE** , даже если мышь не была перемещена. Одним из последствий такого поведения является то, что координаты мыши могут не меняться между сообщениями **WM \_ MOUSEMOVE** .

## <a name="capturing-mouse-movement-outside-the-window"></a>Захват перемещения мыши за пределами окна

По умолчанию окно прекращает получать сообщения [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) , если мышь перемещается за границей клиентской области. Но для некоторых операций может потребоваться отслеживание позиции мыши за пределами этой точки. Например, программа рисования может позволить пользователю перетаскивать прямоугольник выделения за пределы окна, как показано на следующей схеме.

![Иллюстрация захвата мыши.](images/input01.png)

Чтобы получить сообщения, перемещаемые с помощью мыши, за границей окна, вызовите функцию [**сеткаптуре**](/windows/desktop/api/winuser/nf-winuser-setcapture) . После вызова этой функции окно продолжает принимать сообщения [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) в течение всего времени, когда пользователь удерживает по крайней мере одну кнопку мыши, даже если мышь перемещается за пределы окна. Окно захвата должно быть окном переднего плана, и только одно окно может быть окном захвата за раз. Чтобы освободить захват мыши, вызовите функцию [**релеасекаптуре**](/windows/desktop/api/winuser/nf-winuser-releasecapture) .

Обычно [**сеткаптуре**](/windows/desktop/api/winuser/nf-winuser-setcapture) и [**релеасекаптуре**](/windows/desktop/api/winuser/nf-winuser-releasecapture) используются следующим образом.

1.  Когда пользователь нажимает левую кнопку мыши, вызовите [**сеткаптуре**](/windows/desktop/api/winuser/nf-winuser-setcapture) , чтобы начать захват мыши.
2.  Реагирование на сообщения, перемещаемые мышью.
3.  Когда пользователь отпускает левую кнопку мыши, вызовите [**релеасекаптуре**](/windows/desktop/api/winuser/nf-winuser-releasecapture).

## <a name="example-drawing-circles"></a>Пример: Рисование кругов

Добавим круговую программу из [модуля 3](module-3---windows-graphics.md) , позволяя пользователю рисовать окружность с помощью мыши. Начните с [примера программы Direct2D Circle](direct2d-circle-sample.md) . Мы изменим код в этом примере, чтобы добавить простой рисунок. Сначала добавьте в класс новую переменную-член `MainWindow` .


```C++
    D2D1_POINT_2F           ptMouse;
```



Эта переменная сохраняет указатель мыши в то время, когда пользователь перетаскивает указатель мыши. В `MainWindow` конструкторе Инициализируйте переменные *Ellipse* и *птмаусе* .


```C++
    MainWindow() : pFactory(NULL), pRenderTarget(NULL), pBrush(NULL),
        ellipse(D2D1::Ellipse(D2D1::Point2F(), 0, 0)),
        ptMouse(D2D1::Point2F())
    {
    }
```



Удалите текст `MainWindow::CalculateLayout` метода; он не является обязательным для этого примера.


```C++
    void    CalculateLayout() { }
```



Затем объявите обработчики сообщений для левой кнопки вниз, левой кнопки вверх и переместите сообщения.


```C++
    void    OnLButtonDown(int pixelX, int pixelY, DWORD flags);
    void    OnLButtonUp();
    void    OnMouseMove(int pixelX, int pixelY, DWORD flags);
```



Координаты мыши задаются в физических пикселях, но Direct2D — аппаратно-независимые пиксели (DIP). Чтобы правильно обрабатывались параметры с высоким разрешением, необходимо преобразовать координаты пикселя в DIP. Дополнительные сведения о DPI см. в разделе [dpi и Device-Independent пикселей](dpi-and-device-independent-pixels.md). В следующем коде показан вспомогательный класс, который преобразует пиксели в DIP.


```C++
class DPIScale
{
    static float scaleX;
    static float scaleY;

public:
    static void Initialize(ID2D1Factory *pFactory)
    {
        FLOAT dpiX, dpiY;
        pFactory->GetDesktopDpi(&dpiX, &dpiY);
        scaleX = dpiX/96.0f;
        scaleY = dpiY/96.0f;
    }

    template <typename T>
    static D2D1_POINT_2F PixelsToDips(T x, T y)
    {
        return D2D1::Point2F(static_cast<float>(x) / scaleX, static_cast<float>(y) / scaleY);
    }
};

float DPIScale::scaleX = 1.0f;
float DPIScale::scaleY = 1.0f;
```



`DPIScale::Initialize`После создания объекта фабрики Direct2D вызовите в обработчике [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) .


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        DPIScale::Initialize(pFactory);
        return 0;
```



Чтобы получить координаты мыши в DIP из сообщений мыши, выполните следующие действия.

1.  Используйте макросы [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) и [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) для получения координат пикселя. Эти макросы определяются в Виндовскс. h, поэтому не забудьте включить этот заголовок в проект.
2.  Вызовите метод `DPIScale::PixelsToDipsX` и `DPIScale::PixelsToDipsY` , чтобы преобразовать Пиксели в DIP.

Теперь добавьте обработчики сообщений в процедуру окна.


```C++
    case WM_LBUTTONDOWN: 
        OnLButtonDown(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;

    case WM_LBUTTONUP: 
        OnLButtonUp();
        return 0;

    case WM_MOUSEMOVE: 
        OnMouseMove(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;
```



Наконец, реализуйте сами обработчики сообщений.

### <a name="left-button-down"></a>Левая кнопка вниз

Для сообщения, расположенного слева, выполните следующие действия.

1.  Вызовите [**сеткаптуре**](/windows/desktop/api/winuser/nf-winuser-setcapture) , чтобы начать захват мыши.
2.  Сохраните расположение щелчка мыши в переменной *птмаусе* . Это расположение определяет верхний левый угол ограничивающего прямоугольника для эллипса.
3.  Сброс структуры эллипса.
4.  Вызовите [**инвалидатерект**](/windows/desktop/api/winuser/nf-winuser-invalidaterect). Эта функция заставляет окно перерисовываться.


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    SetCapture(m_hwnd);
    ellipse.point = ptMouse = DPIScale::PixelsToDips(pixelX, pixelY);
    ellipse.radiusX = ellipse.radiusY = 1.0f; 
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



### <a name="mouse-move"></a>Перемещение мыши

Для сообщения о перемещении мыши проверьте, не отключена ли левая кнопка мыши. Если это так, повторно Вычислите эллипс и перерисовывает окно. В Direct2D Эллипс определяется центральной точкой и осями x и y. Нам нужно нарисовать эллипс, соответствующий ограничивающему прямоугольнику, определенному точкой (*птмаусе*) и текущей позицией курсора (*x*, *y*), поэтому для поиска ширины, высоты и положения эллипса требуется несколько арифметических действий.

Следующий код повторно вычисляет эллипс, а затем вызывает [**инвалидатерект**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) для перерисовки окна.

![Схема, на которой показан эллипс с радиусами x и y.](images/input02.png)


```C++
void MainWindow::OnMouseMove(int pixelX, int pixelY, DWORD flags)
{
    if (flags & MK_LBUTTON) 
    { 
        const D2D1_POINT_2F dips = DPIScale::PixelsToDips(pixelX, pixelY);

        const float width = (dips.x - ptMouse.x) / 2;
        const float height = (dips.y - ptMouse.y) / 2;
        const float x1 = ptMouse.x + width;
        const float y1 = ptMouse.y + height;

        ellipse = D2D1::Ellipse(D2D1::Point2F(x1, y1), width, height);

        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



### <a name="left-button-up"></a>Кнопка "влево"

Для сообщения с левой кнопкой мыши просто вызовите [**релеасекаптуре**](/windows/desktop/api/winuser/nf-winuser-releasecapture) , чтобы освободить мышь.


```C++
void MainWindow::OnLButtonUp()
{
    ReleaseCapture(); 
}
```



## <a name="next"></a>Следующая

[Другие операции с мышью](other-mouse-operations.md)

 

 