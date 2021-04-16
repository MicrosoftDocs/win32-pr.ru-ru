---
title: Сообщение WM_NCXBUTTONDOWN (Winuser. h)
description: Посылается, когда пользователь нажимает первую или вторую кнопку X, пока курсор находится в неклиентской области окна. Это сообщение отправляется в окно, содержащее курсор. Если окно захвачено мышью, это сообщение не отправляется.
ms.assetid: 72744c98-1898-4548-bd10-61ad53eeab15
keywords:
- WM_NCXBUTTONDOWN ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_NCXBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd615b1e30e013f23097cdc7a8ca7c22c338684a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710491"
---
# <a name="wm_ncxbuttondown-message"></a>\_Сообщение НККСБУТТОНДОВН WM

Посылается, когда пользователь нажимает первую или вторую кнопку X, пока курсор находится в неклиентской области окна. Это сообщение отправляется в окно, содержащее курсор. Если окно захвачено мышью, это сообщение *не* отправляется.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCXBUTTONDOWN                0x00AB
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Слово нижнего порядка указывает значение проверки попадания, возвращаемое функцией [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , из обработки сообщения [**WM \_ нчиттест**](wm-nchittest.md) . Список значений проверки попадания см. в разделе **WM \_ нчиттест**. Слово в высоком порядке указывает на нажатую кнопку. Может быть одним из указанных далее.



| Значение                                                                                                                                                                                                     | Значение                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**XBUTTON1**</dt> <dt>0x0001</dt> </dl> | Была нажата первая кнопка X.<br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XBUTTON2**</dt> <dt>0x0002</dt> </dl> | Нажата вторая кнопка X.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**точек**](/previous-versions//dd162808(v=vs.85)) , которая содержит координаты x и y курсора. Координаты задаются относительно левого верхнего угла экрана.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно возвращать **значение true**. Дополнительные сведения об обработке возвращаемого значения см. в разделе "Примечания".

## <a name="remarks"></a>Комментарии

Используйте следующий код, чтобы получить сведения в параметре *wParam* .


```
nHittest = GET_NCHITTEST_WPARAM(wParam); 
fwButton = GET_XBUTTON_WPARAM(wParam); 
```



Для получения координат x и y из *lParam* можно также использовать следующий код:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> Не используйте макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) или [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) для извлечения координат x и y позиции курсора, так как эти макросы возвращают неверные результаты в системах с несколькими мониторами. Системы с несколькими мониторами могут иметь отрицательные координаты x и y, а **ловорд** и **HIWORD** обрабатывают координаты как неподписанные количества.

 

По умолчанию функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) проверяет указанную точку на получение позиции курсора и выполняет соответствующее действие. При необходимости оно отправляет сообщение [**WM \_ сискомманд**](/windows/desktop/menurc/wm-syscommand) в окно.

В отличие от [**сообщений \_ WM нклбуттондовн**](wm-nclbuttondown.md), [**WM \_ нкмбуттондовн**](wm-ncmbuttondown.md)и [**WM \_ нкрбуттондовн**](wm-ncrbuttondown.md) , приложение должно вернуть **значение true** из этого сообщения, если оно обрабатывает его. Это позволит программному обеспечению имитировать это сообщение в системах Windows более ранних, чем Windows 2000, чтобы определить, обрабатывало ли это сообщение процедура окна или вызываемая [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) для его обработки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Виндовскс. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**ПОЛУЧИТЬ \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**ПОЛУЧИТЬ \_ lParam для Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**WM \_ нчиттест**](wm-nchittest.md)
</dt> <dt>

[**WM \_ нкксбуттондблклк**](wm-ncxbuttondblclk.md)
</dt> <dt>

[**WM \_ нкксбуттонуп**](wm-ncxbuttonup.md)
</dt> <dt>

[**WM \_ сискомманд**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Зрения**
</dt> <dt>

[Ввод с помощью мыши](mouse-input.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**макепоинтс**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**ТОЧКИ**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

