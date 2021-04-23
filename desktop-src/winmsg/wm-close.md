---
Description: Посылается как сигнал о том, что окно или приложение должно завершиться.
ms.assetid: 19500baf-e0ad-4dfa-804f-6a6e0652cffb
title: Сообщение WM_CLOSE (Winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 2f1403050cfd3c98ddf90df4399547158a583c50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704515"
---
# <a name="wm_close-message"></a><span data-ttu-id="39f66-103">\_Сообщение о закрытии WM</span><span class="sxs-lookup"><span data-stu-id="39f66-103">WM\_CLOSE message</span></span>

<span data-ttu-id="39f66-104">Посылается как сигнал о том, что окно или приложение должно завершиться.</span><span class="sxs-lookup"><span data-stu-id="39f66-104">Sent as a signal that a window or an application should terminate.</span></span>

<span data-ttu-id="39f66-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="39f66-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CLOSE                        0x0010
```



## <a name="parameters"></a><span data-ttu-id="39f66-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="39f66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39f66-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39f66-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39f66-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="39f66-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="39f66-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39f66-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39f66-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="39f66-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39f66-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39f66-111">Return value</span></span>

<span data-ttu-id="39f66-112">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="39f66-112">Type: **LRESULT**</span></span>

<span data-ttu-id="39f66-113">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="39f66-113">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="39f66-114">Пример</span><span class="sxs-lookup"><span data-stu-id="39f66-114">Example</span></span>

```cpp
LRESULT CALLBACK WindowProc(
    __in HWND hWindow,
    __in UINT uMsg,
    __in WPARAM wParam,
    __in LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_CLOSE:
        DestroyWindow(hWindow);
        break;
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWindow, uMsg, wParam, lParam);
    }

    return 0;
}
```
<span data-ttu-id="39f66-115">Пример из [классической выборки Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/RadialController/cpp/RadialController.cpp) на сайте GitHub.</span><span class="sxs-lookup"><span data-stu-id="39f66-115">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/RadialController/cpp/RadialController.cpp) on GitHub.</span></span>


## <a name="remarks"></a><span data-ttu-id="39f66-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39f66-116">Remarks</span></span>

<span data-ttu-id="39f66-117">Приложение может запросить подтверждение перед уничтожением окна, обрабатывая сообщение **\_ закрытия WM** и вызывая функцию [**дестройвиндов**](/windows/win32/api/winuser/nf-winuser-destroywindow) только в том случае, если пользователь подтверждает выбранное значение.</span><span class="sxs-lookup"><span data-stu-id="39f66-117">An application can prompt the user for confirmation, prior to destroying a window, by processing the **WM\_CLOSE** message and calling the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function only if the user confirms the choice.</span></span>

<span data-ttu-id="39f66-118">По умолчанию функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) вызывает функцию [**дестройвиндов**](/windows/win32/api/winuser/nf-winuser-destroywindow) для уничтожения окна.</span><span class="sxs-lookup"><span data-stu-id="39f66-118">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function calls the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function to destroy the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="39f66-119">Требования</span><span class="sxs-lookup"><span data-stu-id="39f66-119">Requirements</span></span>



| <span data-ttu-id="39f66-120">Требование</span><span class="sxs-lookup"><span data-stu-id="39f66-120">Requirement</span></span> | <span data-ttu-id="39f66-121">Значение</span><span class="sxs-lookup"><span data-stu-id="39f66-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39f66-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39f66-122">Minimum supported client</span></span><br/> | <span data-ttu-id="39f66-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="39f66-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="39f66-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39f66-124">Minimum supported server</span></span><br/> | <span data-ttu-id="39f66-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="39f66-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="39f66-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="39f66-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="39f66-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39f66-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39f66-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39f66-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="39f66-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="39f66-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="39f66-130">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="39f66-130">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="39f66-131">**дестройвиндов**</span><span class="sxs-lookup"><span data-stu-id="39f66-131">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

<span data-ttu-id="39f66-132">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="39f66-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="39f66-133">Windows</span><span class="sxs-lookup"><span data-stu-id="39f66-133">Windows</span></span>](windows.md)
</dt> </dl>

 

 
