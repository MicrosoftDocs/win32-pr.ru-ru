---
title: Сообщение WM_TOUCH (Winuser. h)
description: Уведомляет окно, когда одна или несколько сенсорных точек, таких как палец или перо, касаются сенсорной поверхности дигитайзера.
ms.assetid: 5dee8bab-34fa-4dd9-a65b-35883757ec80
keywords:
- сообщение WM_TOUCH Windows TOUCH
topic_type:
- apiref
api_name:
- WM_TOUCH
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1034a229dbb1f3895726fcb3c1551e2dd0f390be0fd7bc2eb81d8331e582eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810104"
---
# <a name="wm_touch-message"></a>\_Сообщение касания WM

Уведомляет окно, когда одна или несколько сенсорных точек, таких как палец или перо, касаются сенсорной поверхности дигитайзера.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Слово нижнего порядка содержит количество сенсорных точек, связанных с этим сообщением. Слово высокого порядка зарезервировано для будущего использования.

</dd> <dt>

*lParam* 
</dt> <dd>

Содержит входной маркер касания, который можно использовать в вызове [**жеттаучинпутинфо**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) для получения подробных сведений о сенсорных точках, связанных с этим сообщением.

Этот обработчик действителен только в пределах текущего процесса и не должен передаваться между процессами, за исключением случаев, когда **lParam** используется в вызовах **SendMessage** или @ **Message** .

Если приложению больше не требуется этот обработчик, приложение должно вызвать **клосетаучинпусандле** , чтобы освободить память процесса, связанную с этим маркером. Если этого не сделать, это может привести к утечке памяти приложения.

Обратите внимание, что маркер сенсорного ввода в этом параметре больше не действителен после передачи сообщения в [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca). [Дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca) закроет и сделает этот маркер недействительным.

Обратите внимание, что маркер сенсорного ввода в этом параметре больше не действителен после пересылки сообщения с помощью [**сообщения**](sendmessage--postmessage--and-related-functions.md), **SendMessage** или одного из вариантов. Эти функции закрывают и не проверяют этот обработчик.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

Если приложение не обрабатывает сообщение, оно должно вызвать [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca). Это приводит к утечке памяти в приложении, поскольку дескриптор сенсорного ввода не закрыт, а связанная память процесса не освобождается.

## <a name="remarks"></a>Remarks

**WM \_ СЕНСОРные** сообщения не учитывают **хттранспарент** области Windows. Если окно возвращает **хттранспарент** в ответ на сообщение **\_ нчиттест WM** , сообщения мыши переходят к родительскому элементу, а сообщения **WM \_ Touch** переходят непосредственно в окно.

## <a name="examples"></a>Примеры

В следующем коде приведен пример того, как получить подробные данные сенсорного ввода, связанные с этим сообщением.


```C++
UINT cInputs = LOWORD(wParam);
PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
if (NULL != pInputs)
{
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
                          cInputs,
                          pInputs,
                          sizeof(TOUCHINPUT)))
    {
        // process pInputs
        if (!CloseTouchInputHandle((HTOUCHINPUT)lParam))
        {
            // error handling
        }
    }
    else
    {
        // GetLastError() and error handling
    }
    delete [] pInputs;
}
else
{
    // error handling, presumably out of memory
}
return DefWindowProc(hWnd, message, wParam, lParam);
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                               |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                                  |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Сообщения](messages.md)
</dt> <dt>

[Инструкции по программированию и обработке инерции](manipulation-and-inertia.md)
</dt> <dt>

[Windows Руководств по программированию для сенсорного ввода](guide-multi-touch-input.md)
</dt> </dl>

 

