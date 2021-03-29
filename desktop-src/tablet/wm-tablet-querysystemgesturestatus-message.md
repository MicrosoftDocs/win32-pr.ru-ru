---
description: Посылается, когда система запрашивает окно, какие системные жесты хотели бы получить.
ms.assetid: 5b747b3c-3b77-4913-932f-182114d1f674
title: Сообщение WM_TABLET_QUERYSYSTEMGESTURESTATUS (Тпкшрд. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395196f963cae9b8d18697276e546f1eba05b245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897253"
---
# <a name="wm_tablet_querysystemgesturestatus-message"></a>\_Сообщение WM планшет \_ куерисистемжестурестатус

Посылается, когда система запрашивает окно, какие системные жесты хотели бы получить.


```C++
#define WM_TABLET_DEFBASE                    0x02C0
#define WM_TABLET_QUERYSYSTEMGESTURESTATUS   (WM_TABLET_DEFBASE + 12)       
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Значение точки, представляющее экранные координаты.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Обрабатывая это сообщение, можно динамически отключить жесты для областей окна.

> [!Note]  
> *LParam* можно преобразовать в координаты x и y с помощью `GET_X_LPARAM` `GET_Y_LPARAM` макросов и.

 

По умолчанию окно будет принимать все события системных жестов. Вы можете выбрать события, которые должны быть получены в окне, и какие события вы хотите отключить, отменив ответ на **сообщение \_ \_ куерисистемжестурестатус WM планшета** в **WndProc**. Сообщение **WM \_ планшет \_ куерисистемжестурестатус** определено в тпкшрд. h. Значения для включения и отключения системных жестов планшета также определяются в тпкшрд. h следующим образом:

``` syntax
#define TABLET_DISABLE_PRESSANDHOLD        0x00000001
#define TABLET_DISABLE_PENTAPFEEDBACK      0x00000008
#define TABLET_DISABLE_PENBARRELFEEDBACK   0x00000010
#define TABLET_DISABLE_TOUCHUIFORCEON      0x00000100
#define TABLET_DISABLE_TOUCHUIFORCEOFF     0x00000200
#define TABLET_DISABLE_TOUCHSWITCH         0x00008000
#define TABLET_DISABLE_FLICKS              0x00010000
#define TABLET_ENABLE_FLICKSONCONTEXT      0x00020000
#define TABLET_ENABLE_FLICKLEARNINGMODE    0x00040000
#define TABLET_DISABLE_SMOOTHSCROLLING     0x00080000
#define TABLET_DISABLE_FLICKFALLBACKKEYS   0x00100000
#define TABLET_ENABLE_MULTITOUCHDATA       0x01000000
```

> [!Note]
>
> Отключение нажатия и удерживания повысит скорость реагирования щелчков мыши, так как эта функция создает время ожидания для различения двух операций.

 

Будьте внимательны при обработке сообщения **WM \_ планшета \_ куерисистемжестурестатус** . **WM \_ Планшет \_ куерисистемжестурестатус** передается с помощью функции [**функции sendmessagetimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) . При вызове методов для COM-интерфейса этот объект должен находиться в одном процессе. В противном случае COM создает исключение.

## <a name="examples"></a>Примеры

В следующем примере показано, как отключить жесты для региона с помощью WM \_ планшета \_ куерисистемжестурестатус.


```C++
#include <windowsx.h>        

(...)        
        
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    case WM_TABLET_QUERYSYSTEMGESTURESTATUS:
        int x = GET_X_LPARAM(lParam);
        int y = GET_Y_LPARAM(lParam);
        if (x < xThreashold && y < yThreshold){
            // no flicks in the region specified by the threashold
            return TABLET_DISABLE_FLICKS;
        }
        // flicks will happen otherwise
        return 0;
}        
        
```



В следующем примере показано, как отключить различные функции жестов для всего окна.


```C++
const DWORD dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
        
void SetTabletpenserviceProperties(HWND hWnd){
    ATOM atom = ::GlobalAddAtom(MICROSOFT_TABLETPENSERVICE_PROPERTY);    
    ::SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
    ::GlobalDeleteAtom(atom);
}        
        
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Тпкшрд. h</dt> </dl> |



 

 
