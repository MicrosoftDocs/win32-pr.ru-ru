---
description: Посылается окну, когда окно будет скрыто или показано.
ms.assetid: dea7c9aa-eba7-4b93-a4c5-9b2d36999780
title: Сообщение WM_SHOWWINDOW (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbca6cbb4c73ff1cad31754b1b581e0c892970e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345572"
---
# <a name="wm_showwindow-message"></a><span data-ttu-id="2d53b-103">\_Сообщение об ошибке WM SHOWWINDOW</span><span class="sxs-lookup"><span data-stu-id="2d53b-103">WM\_SHOWWINDOW message</span></span>

<span data-ttu-id="2d53b-104">Посылается окну, когда окно будет скрыто или показано.</span><span class="sxs-lookup"><span data-stu-id="2d53b-104">Sent to a window when the window is about to be hidden or shown.</span></span>

<span data-ttu-id="2d53b-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2d53b-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SHOWWINDOW                   0x0018
```



## <a name="parameters"></a><span data-ttu-id="2d53b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d53b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d53b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2d53b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d53b-108">Указывает, отображается ли окно.</span><span class="sxs-lookup"><span data-stu-id="2d53b-108">Indicates whether a window is being shown.</span></span> <span data-ttu-id="2d53b-109">Если параметр *wParam* имеет **значение true**, окно отображается.</span><span class="sxs-lookup"><span data-stu-id="2d53b-109">If *wParam* is **TRUE**, the window is being shown.</span></span> <span data-ttu-id="2d53b-110">Если параметр *wParam* имеет **значение false**, окно скрывается.</span><span class="sxs-lookup"><span data-stu-id="2d53b-110">If *wParam* is **FALSE**, the window is being hidden.</span></span>

</dd> <dt>

<span data-ttu-id="2d53b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2d53b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d53b-112">Состояние отображаемого окна.</span><span class="sxs-lookup"><span data-stu-id="2d53b-112">The status of the window being shown.</span></span> <span data-ttu-id="2d53b-113">Если параметр *lParam* равен нулю, сообщение было отправлено из-за вызова функции [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) ; в противном случае *lParam* имеет одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="2d53b-113">If *lParam* is zero, the message was sent because of a call to the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function; otherwise, *lParam* is one of the following values.</span></span>



| <span data-ttu-id="2d53b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="2d53b-114">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="2d53b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2d53b-115">Meaning</span></span>                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="SW_OTHERUNZOOM"></span><span id="sw_otherunzoom"></span><dl> <span data-ttu-id="2d53b-116"><dt>**SW \_ ОСЕРУНЗУМ**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2d53b-116"><dt>**SW\_OTHERUNZOOM**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="2d53b-117">Выполняется обнаружение окна, так как окно развертывания было восстановлено или уменьшено.</span><span class="sxs-lookup"><span data-stu-id="2d53b-117">The window is being uncovered because a maximize window was restored or minimized.</span></span><br/> |
| <span id="SW_OTHERZOOM"></span><span id="sw_otherzoom"></span><dl> <span data-ttu-id="2d53b-118"><dt>**SW \_ ОСЕРЗУМ**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2d53b-118"><dt>**SW\_OTHERZOOM**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="2d53b-119">Окно охватывается другим окном, которое было развернуто.</span><span class="sxs-lookup"><span data-stu-id="2d53b-119">The window is being covered by another window that has been maximized.</span></span><br/>             |
| <span id="SW_PARENTCLOSING"></span><span id="sw_parentclosing"></span><dl> <span data-ttu-id="2d53b-120"><dt>**SW \_ ПАРЕНТКЛОСИНГ**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2d53b-120"><dt>**SW\_PARENTCLOSING**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="2d53b-121">Окно-владелец окна свернется.</span><span class="sxs-lookup"><span data-stu-id="2d53b-121">The window's owner window is being minimized.</span></span><br/>                                      |
| <span id="SW_PARENTOPENING"></span><span id="sw_parentopening"></span><dl> <span data-ttu-id="2d53b-122"><dt>**SW \_ ПАРЕНТОПЕНИНГ**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2d53b-122"><dt>**SW\_PARENTOPENING**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="2d53b-123">Окно-владелец окна восстанавливается.</span><span class="sxs-lookup"><span data-stu-id="2d53b-123">The window's owner window is being restored.</span></span><br/>                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d53b-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d53b-124">Return value</span></span>

<span data-ttu-id="2d53b-125">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="2d53b-125">Type: **LRESULT**</span></span>

<span data-ttu-id="2d53b-126">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="2d53b-126">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d53b-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2d53b-127">Remarks</span></span>

<span data-ttu-id="2d53b-128">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) скрывает или отображает окно, как указано в сообщении.</span><span class="sxs-lookup"><span data-stu-id="2d53b-128">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function hides or shows the window, as specified by the message.</span></span> <span data-ttu-id="2d53b-129">Если окно имеет стиль " [**WS \_ Visible**](window-styles.md) " при его создании, окно получает это сообщение после его создания, но до его отображения.</span><span class="sxs-lookup"><span data-stu-id="2d53b-129">If a window has the [**WS\_VISIBLE**](window-styles.md) style when it is created, the window receives this message after it is created, but before it is displayed.</span></span> <span data-ttu-id="2d53b-130">Окно также получает это сообщение, когда состояние видимости изменяется функцией [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) или [**шововнедпопупс**](/windows/win32/api/winuser/nf-winuser-showownedpopups) .</span><span class="sxs-lookup"><span data-stu-id="2d53b-130">A window also receives this message when its visibility state is changed by the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) or [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) function.</span></span>

<span data-ttu-id="2d53b-131">Сообщение об ошибке **WM \_ SHOWWINDOW** не отправляется в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="2d53b-131">The **WM\_SHOWWINDOW** message is not sent under the following circumstances:</span></span>

-   <span data-ttu-id="2d53b-132">При создании перекрывающегося окна верхнего уровня с помощью стиля [**WS \_ Maximize**](window-styles.md) или **WS \_ Minimize** .</span><span class="sxs-lookup"><span data-stu-id="2d53b-132">When a top-level, overlapped window is created with the [**WS\_MAXIMIZE**](window-styles.md) or **WS\_MINIMIZE** style.</span></span>
-   <span data-ttu-id="2d53b-133">При указании флага **SW \_ шовнормал** в вызове функции [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="2d53b-133">When the **SW\_SHOWNORMAL** flag is specified in the call to the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d53b-134">Требования</span><span class="sxs-lookup"><span data-stu-id="2d53b-134">Requirements</span></span>



| <span data-ttu-id="2d53b-135">Требование</span><span class="sxs-lookup"><span data-stu-id="2d53b-135">Requirement</span></span> | <span data-ttu-id="2d53b-136">Значение</span><span class="sxs-lookup"><span data-stu-id="2d53b-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d53b-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d53b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2d53b-138">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2d53b-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2d53b-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d53b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2d53b-140">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2d53b-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2d53b-141">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2d53b-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d53b-142"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d53b-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d53b-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d53b-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="2d53b-144">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="2d53b-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2d53b-145">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="2d53b-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="2d53b-146">**шововнедпопупс**</span><span class="sxs-lookup"><span data-stu-id="2d53b-146">**ShowOwnedPopups**</span></span>](/windows/win32/api/winuser/nf-winuser-showownedpopups)
</dt> <dt>

[<span data-ttu-id="2d53b-147">**ShowWindow**</span><span class="sxs-lookup"><span data-stu-id="2d53b-147">**ShowWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-showwindow)
</dt> <dt>

<span data-ttu-id="2d53b-148">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="2d53b-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2d53b-149">Windows</span><span class="sxs-lookup"><span data-stu-id="2d53b-149">Windows</span></span>](windows.md)
</dt> </dl>

 

 
