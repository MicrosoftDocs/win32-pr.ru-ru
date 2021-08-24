---
description: Отправляется при уничтожении окна. Он отправляется в окно процедуры, которое уничтожается после удаления окна с экрана.
ms.assetid: 089c0645-199b-4a90-9cbc-740f0cf3267d
title: Сообщение WM_DESTROY (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7acff03f01e9bf0c8021f8324411f646341a29a5b3b6dc1f9b3493ec89010c1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587454"
---
# <a name="wm_destroy-message"></a>\_Сообщение об уничтожении WM

Отправляется при уничтожении окна. Он отправляется в окно процедуры, которое уничтожается после удаления окна с экрана.

Это сообщение отправляется первым в удаляемое окно, а затем в дочерние окна (если они есть) при их уничтожении. Во время обработки сообщения можно предположить, что все остальные дочерние окна все еще существуют.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_DESTROY                      0x0002
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **lResult**

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Remarks

Если удаляемое окно является частью цепочки окна просмотра буфера обмена (задается вызовом функции [**сетклипбоардвиевер**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) ), окно должно удалить себя из цепочки, обрабатывая функцию [**чанжеклипбоардчаин**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) перед возвратом из сообщения **WM \_ destroy** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**чанжеклипбоардчаин**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain)
</dt> <dt>

[**дестройвиндов**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**посткуитмессаже**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[**сетклипбоардвиевер**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[**\_Закрыть WM**](wm-close.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
