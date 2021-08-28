---
Description: Посылается окну после изменения его размера.
ms.assetid: e3e14dcd-9236-48bd-a692-6985d8146f81
title: Сообщение WM_SIZE (Winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 473e4e63523c7b97968e54349e5882b7e589fc7238d717ccf96563b5ce93388e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548224"
---
# <a name="wm_size-message"></a>\_Сообщение о размере WM

Посылается окну после изменения его размера.

Окно получает это сообщение через функцию [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) .


```C++
#define WM_SIZE                         0x0005
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Тип запрошенного изменения размера. Этот параметр может принимать одно из указанных ниже значений.



| Значение                                                                                                                                                                                                                   | Значение                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="SIZE_MAXHIDE"></span><span id="size_maxhide"></span><dl> <dt>**Размер \_ МАКСХИДЕ**</dt> <dt>4</dt> </dl>       | Сообщение отправляется во все всплывающие окна, когда какое-либо другое окно развернуто.<br/>                              |
| <span id="SIZE_MAXIMIZED"></span><span id="size_maximized"></span><dl> <dt>**Размер \_ РАЗВЕРНУТО**</dt> <dt>2</dt> </dl> | Окно развернуто.<br/>                                                                          |
| <span id="SIZE_MAXSHOW"></span><span id="size_maxshow"></span><dl> <dt>**Размер \_ МАКСШОВ**</dt> <dt>3</dt> </dl>       | Сообщение отправляется во все всплывающие окна при восстановлении какого-либо другого окна до своего прежнего размера.<br/>      |
| <span id="SIZE_MINIMIZED"></span><span id="size_minimized"></span><dl> <dt>**Размер \_ СВЕДЕНная**</dt> <dt>1</dt> </dl> | Окно было сведено к минимальному.<br/>                                                                          |
| <span id="SIZE_RESTORED"></span><span id="size_restored"></span><dl> <dt>**Размер \_ ВОССТАНОВЛЕНо**</dt> <dt>0</dt> </dl>    | Размер окна был изменен, но не применяется ни **\_ уменьшенный размер** , ни **\_ развернутое значение размера** .<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Слово *lParam* в низком порядке задает новую ширину клиентской области.

Слово *lParam* в высоком порядке задает новую высоту клиентской области.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **lResult**

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="example"></a>Пример

```cpp
/******************************************************************
*                                                                 *
*  SimpleText::OnResize                                           *
*                                                                 *
*  If the application receives a WM_SIZE message, this method     *
*  resize the render target appropriately.                        *
*                                                                 *
******************************************************************/

void SimpleText::OnResize(UINT width, UINT height)
{
    if (pRT_)
    {
        D2D1_SIZE_U size;
        size.width = width;
        size.height = height;
        pRT_->Resize(size);
    }
}

LRESULT CALLBACK SimpleText::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
   
    SimpleText *pSimpleText = reinterpret_cast<SimpleText *>(
                ::GetWindowLongPtr(hwnd, GWLP_USERDATA));

    if (pSimpleText)
    {
        switch(message)
        {
        case WM_SIZE:
            {
                UINT width = LOWORD(lParam);
                UINT height = HIWORD(lParam);
                pSimpleText->OnResize(width, height);
            }
            return 0;

// ...

```

пример из [Windows классических примеров](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) на GitHub.

## <a name="remarks"></a>Remarks

Если функция [**сетскроллпос**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) или [**мовевиндов**](/windows/win32/api/winuser/nf-winuser-movewindow) вызывается для дочернего окна в результате сообщения **\_ размера WM** , параметр *бредрав* или *брепаинт* должен быть ненулевым, чтобы перерисовать окно.

Хотя ширина и высота окна представляют собой 32-битные значения, параметр *lParam* содержит только 16 младших разрядов каждого из них.

Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) отправляет сообщения **WM \_ size** и **WM \_ Move** при обработке сообщения [**WM \_ виндовпосчанжед**](wm-windowposchanged.md) .
Сообщения **WM \_ size** и **WM \_ Move** не отправляются, если приложение обрабатывает сообщение **WM \_ виндовпосчанжед** без вызова **дефвиндовпрок**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**мовевиндов**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**WM \_ виндовпосчанжед**](wm-windowposchanged.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**сетскроллпос**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)
</dt> </dl>

 

 
