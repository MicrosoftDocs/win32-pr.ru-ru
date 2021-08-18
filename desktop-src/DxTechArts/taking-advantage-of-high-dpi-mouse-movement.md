---
title: Использование преимуществ High-Definition перемещения мыши
description: Эта статья посвящена наилучшему способу оптимизации производительности ввода с помощью мыши высокого определения в игре, например кораблей первого человека.
ms.assetid: 0138a248-e8e0-a392-564e-7a9229b94b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d7a6efe6916ad8605e3cdc056ffd716ac5113b66c022b0a95fd8a78b1a62e30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042394"
---
# <a name="taking-advantage-of-high-definition-mouse-movement"></a>Использование преимуществ High-Definition перемещения мыши

Стандартная мышь компьютера возвращает данные с 400 точек на дюйм (DPI), в то время как мышь с высокой степенью определения создает данные с разрешением 800 DPI или выше. Это делает входные данные от мыши с высокой степенью точности более точными, чем с помощью стандартной мыши. Однако данные высокой четкости не могут быть получены через стандартные \_ сообщения WM MOUSEMOVE. Как правило, игры получают преимущества от высококачественных мышей, но игры, получающие данные мыши с помощью только WM \_ MOUSEMOVE, не смогут получить доступ к полному, нефильтрованному разрешению мыши.

Ряд компаний — это высококачественные устройства мыши с высоким уровнем четкости, такие как Microsoft и Logitech. Благодаря повышению популярности устройств мыши с высоким разрешением, важно, чтобы разработчики понимали, как оптимально использовать информацию, создаваемую этими устройствами. Эта статья посвящена наилучшему способу оптимизации производительности ввода с помощью мыши высокого определения в игре, например кораблей первого человека.

## <a name="retrieving-mouse-movement-data"></a>Получение данных о перемещении мыши

Ниже приведены три основных метода получения данных мыши:

-   [WM \_ MOUSEMOVE](/windows)
-   [\_входные данные WM](/windows)
-   [DirectInput](#directinput)

У каждого метода есть свои преимущества и недостатки в зависимости от того, как будут использоваться эти данные.

### <a name="wm_mousemove"></a>WM \_ MOUSEMOVE

Самый простой способ чтения данных перемещения мыши — это сообщения WM \_ MOUSEMOVE. Ниже приведен пример того, как можно считать данные перемещения мыши из \_ сообщения WM MOUSEMOVE:

```cpp
case WM_MOUSEMOVE:
{
    int xPosAbsolute = GET_X_PARAM(lParam); 
    int yPosAbsolute = GET_Y_PARAM(lParam);
    // ...
    break;
}
```

Основным недостатком данных из WM \_ MOUSEMOVE является то, что оно ограничено разрешением экрана. Это означает, что если переместить мышь немного, но недостаточно, чтобы указатель переместится на следующий пиксель, то \_ сообщение WM MOUSEMOVE не создается. Таким образом, использование этого метода для чтения движения мыши отменяет преимущества входных данных высокой четкости.

\_тем не менее, преимущество WM MOUSEMOVE заключается в том, что Windows применяет ускорение указателя (также известный как баллистикс) к необработанным данным мыши, что заставляет указатель мыши вести себя по мере ожидания клиентов. Это делает WM \_ MOUSEMOVE предпочтительным вариантом для элемента управления "указатель" (над \_ входными данными WM или директинпут), так как он приводит к более естественному поведению для пользователей. Несмотря на то, что WM \_ MOUSEMOVE идеально подходит для перемещения указателей мыши, это не так удобно для перемещения камеры первого пользователя, так как точность высокой четкости будет потеряна.

Дополнительные сведения о WM \_ MouseMove см. в разделе [**WM \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove).

### <a name="wm_input"></a>\_входные данные WM

Второй способ получения данных мыши — чтение \_ входных сообщений WM. Обработка \_ входных сообщений WM сложнее, чем обработка \_ сообщений WM MOUSEMOVE, но \_ входные сообщения WM считываются непосредственно из стека устройство HID (HID) и отображают результаты высокой четкости.

Для чтения данных перемещения мыши из \_ входного сообщения WM необходимо сначала зарегистрировать устройство. пример кода приведен ниже.

```cpp
// you can #include <hidusage.h> for these defines
#ifndef HID_USAGE_PAGE_GENERIC
#define HID_USAGE_PAGE_GENERIC         ((USHORT) 0x01)
#endif
#ifndef HID_USAGE_GENERIC_MOUSE
#define HID_USAGE_GENERIC_MOUSE        ((USHORT) 0x02)
#endif

RAWINPUTDEVICE Rid[1];
Rid[0].usUsagePage = HID_USAGE_PAGE_GENERIC; 
Rid[0].usUsage = HID_USAGE_GENERIC_MOUSE; 
Rid[0].dwFlags = RIDEV_INPUTSINK;   
Rid[0].hwndTarget = hWnd;
RegisterRawInputDevices(Rid, 1, sizeof(Rid[0]));
```

Следующий код обрабатывает \_ входные сообщения WM в обработчике винпрока приложения:

```cpp
case WM_INPUT: 
{
    UINT dwSize = sizeof(RAWINPUT);
    static BYTE lpb[sizeof(RAWINPUT)];

    GetRawInputData((HRAWINPUT)lParam, RID_INPUT, lpb, &dwSize, sizeof(RAWINPUTHEADER));

    RAWINPUT* raw = (RAWINPUT*)lpb;

    if (raw->header.dwType == RIM_TYPEMOUSE) 
    {
        int xPosRelative = raw->data.mouse.lLastX;
        int yPosRelative = raw->data.mouse.lLastY;
    } 
    break;
}
```

Преимущество использования \_ входных данных WM заключается в том, что игра получает необработанные данные от мыши на самом низком уровне.

Недостаток заключается в том, что \_ Вход WM не имеет баллистикс к данным, поэтому, если вы хотите поместить курсор с этими данными, потребуется выполнить дополнительные усилия, чтобы поведение курсора было таким, как в Windows. дополнительные сведения о применении указателя баллистикс см. в разделе [указатель баллистикс для Windows XP](https://www.microsoft.com/whdc/archive/pointer-bal.mspx).

Дополнительные сведения о \_ входных данных WM см. в разделе [о необработанных входных данных](/windows/desktop/inputdev/about-raw-input).

### <a name="directinput"></a>DirectInput

[Директинпут](/windows-hardware/drivers/hid/directinput) — это набор вызовов API, который абстрагирует устройства ввода в системе. На внутреннем уровне Директинпут создает второй поток для чтения \_ входных данных WM, а использование интерфейсов API директинпут приведет к дополнительным издержкам, чем простое чтение \_ входов WM. Директинпут удобно использовать только для чтения данных из Директинпут джойстиков. однако, если требуется поддержка только контроллера Xbox 360 для Windows, используйте вместо него [ксинпут](/windows/desktop/xinput/xinput-game-controller-apis-portal) . В целом использование Директинпут не дает никаких преимуществ при чтении данных с устройств мыши или клавиатуры, и использование Директинпут в этих сценариях не рекомендуется.

Сравните сложность использования [директинпут](/windows-hardware/drivers/hid/directinput), показанную в следующем коде, с методами, описанными выше. Для создания Директинпут мыши требуется следующий набор вызовов:

```cpp
LPDIRECTINPUT8 pDI;
LPDIRECTINPUTDEVICE8 pMouse;

hr = DirectInput8Create(GetModuleHandle(NULL), DIRECTINPUT_VERSION, IID_IDirectInput8, (VOID**)&pDI, NULL);
if(FAILED(hr))
    return hr;

hr = pDI->CreateDevice(GUID_SysMouse, &pMouse, NULL);
if(FAILED(hr))
    return hr;

hr = pMouse->SetDataFormat(&c_dfDIMouse2);
if(FAILED(hr))
    return hr;

hr = pMouse->SetCooperativeLevel(hWnd, DISCL_NONEXCLUSIVE | DISCL_FOREGROUND);
if(FAILED(hr))
    return hr;

if(!bImmediate)
{
    DIPROPDWORD dipdw;
    dipdw.diph.dwSize       = sizeof(DIPROPDWORD);
    dipdw.diph.dwHeaderSize = sizeof(DIPROPHEADER);
    dipdw.diph.dwObj        = 0;
    dipdw.diph.dwHow        = DIPH_DEVICE;
    dipdw.dwData            = 16; // Arbitrary buffer size

    if(FAILED(hr = pMouse->SetProperty(DIPROP_BUFFERSIZE, &dipdw.diph)))
        return hr;
}

pMouse->Acquire();
```

После этого устройство мыши Директинпут может читать каждый кадр:

```cpp
DIMOUSESTATE2 dims2; 
ZeroMemory(&dims2, sizeof(dims2));

hr = pMouse->GetDeviceState(sizeof(DIMOUSESTATE2), &dims2);
if(FAILED(hr)) 
{
    hr = pMouse->Acquire();
    while(hr == DIERR_INPUTLOST) 
        hr = pMouse->Acquire();

    return S_OK; 
}

int xPosRelative = dims2.lX;
int yPosRelative = dims2.lY;
```

## <a name="summary"></a>Сводка

В целом, лучшим методом получения данных о перемещении мыши с высоким определением являются \_ входные данные WM. Если пользователи просто перемещают указатель мыши, рассмотрите возможность использования WM \_ MOUSEMOVE, чтобы избежать необходимости выполнять баллистикс указателя. Оба эти сообщения окна будут работать хорошо, даже если мышь не является указателем высокой четкости. благодаря поддержке высокого определения Windows игры могут обеспечить более точное управление пользователями.