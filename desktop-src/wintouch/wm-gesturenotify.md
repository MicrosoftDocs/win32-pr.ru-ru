---
title: Сообщение WM_GESTURENOTIFY (Winuser. h)
description: Дает возможность задать конфигурацию жестов.
ms.assetid: 83c23928-86ce-421d-bb84-5c41a770bf60
keywords:
- WM_GESTURENOTIFY сообщений Windows Touch
topic_type:
- apiref
api_name:
- WM_GESTURENOTIFY
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e900e4b607760df16938080a49f97a3ab0cf2ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136466"
---
# <a name="wm_gesturenotify-message"></a>\_Сообщение ЖЕСТУРЕНОТИФИ WM

Дает возможность задать конфигурацию жестов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на [**жестуренотифиструкт**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Значение должно возвращаться из [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Комментарии

Когда получено сообщение **WM \_ жестуренотифи** , приложение может использовать [**сетжестуреконфиг**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) для указания получаемых жестов. Это сообщение всегда должно быть собрано с помощью функции [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca) .

> [!Note]  
> Обработка сообщения **WM \_ жестуренотифи** изменит конфигурацию жестов на время существования окна, а не только на следующий жест.

 

## <a name="examples"></a>Примеры

В следующем примере показано, как включить все жесты. Дополнительные примеры см. в разделе [**сетжестуреконфиг**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig).


```C++
    switch (message)
    {
    case WM_GESTURENOTIFY:
        GESTURECONFIG gc = {0,GC_ALLGESTURES,0};
        BOOL bResult = SetGestureConfig(hWnd,0,1,&gc,sizeof(GESTURECONFIG));
            
        if(!bResult)
        {
            // an error
        }
        return DefWindowProc(hWnd, WM_GESTURENOTIFY, wParam, lParam);
    }
      
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                               |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Уведомления](notifications.md)
</dt> <dt>

[Инструкции по программированию жестов сенсорного ввода Windows](guide-multi-touch-gestures.md)
</dt> <dt>

[**жестуренотифиструкт**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)
</dt> <dt>

[**сетжестуреконфиг**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)
</dt> </dl>

 

