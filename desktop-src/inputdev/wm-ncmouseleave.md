---
title: Сообщение WM_NCMOUSELEAVE (Winuser. h)
description: Передается в окно, когда курсор покидает неклиентскую область окна, указанную в предыдущем вызове метода TrackMouseEven.
ms.assetid: b3ada6db-93ce-45d7-b408-d08692328aeb
keywords:
- WM_NCMOUSELEAVE ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_NCMOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf7f9d0931c2623d2e92010abfca96f391107b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691800"
---
# <a name="wm_ncmouseleave-message"></a><span data-ttu-id="ccf26-104">\_Сообщение НКМАУСЕЛЕАВЕ WM</span><span class="sxs-lookup"><span data-stu-id="ccf26-104">WM\_NCMOUSELEAVE message</span></span>

<span data-ttu-id="ccf26-105">Передается в окно, когда курсор покидает неклиентскую область окна, указанную в предыдущем вызове метода [**TrackMouseEven**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span><span class="sxs-lookup"><span data-stu-id="ccf26-105">Posted to a window when the cursor leaves the nonclient area of the window specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="ccf26-106">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ccf26-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMOUSELEAVE                 0x02A2
```



## <a name="parameters"></a><span data-ttu-id="ccf26-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ccf26-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccf26-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ccf26-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccf26-109">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="ccf26-109">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ccf26-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ccf26-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccf26-111">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="ccf26-111">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccf26-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ccf26-112">Return value</span></span>

<span data-ttu-id="ccf26-113">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="ccf26-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccf26-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ccf26-114">Remarks</span></span>

<span data-ttu-id="ccf26-115">При создании этого сообщения все записи, запрошенные [**TrackMouseEven**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) , отменяются.</span><span class="sxs-lookup"><span data-stu-id="ccf26-115">All tracking requested by [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) is canceled when this message is generated.</span></span> <span data-ttu-id="ccf26-116">Приложение должно вызвать **TrackMouseEven** , когда указатель мыши перейдет в окно, если он требует дополнительного отслеживания поведения при наведении указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="ccf26-116">The application must call **TrackMouseEvent** when the mouse reenters its window if it requires further tracking of mouse hover behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccf26-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ccf26-117">Requirements</span></span>



| <span data-ttu-id="ccf26-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ccf26-118">Requirement</span></span> | <span data-ttu-id="ccf26-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ccf26-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf26-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ccf26-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ccf26-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ccf26-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ccf26-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ccf26-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ccf26-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ccf26-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ccf26-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ccf26-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccf26-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ccf26-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccf26-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ccf26-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="ccf26-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="ccf26-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ccf26-128">**TrackMouseEven**</span><span class="sxs-lookup"><span data-stu-id="ccf26-128">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="ccf26-129">**TRACKMOUSEEVEN**</span><span class="sxs-lookup"><span data-stu-id="ccf26-129">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="ccf26-130">**WM \_ сискомманд**</span><span class="sxs-lookup"><span data-stu-id="ccf26-130">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[<span data-ttu-id="ccf26-131">**WM \_ MOUSELEAVE**</span><span class="sxs-lookup"><span data-stu-id="ccf26-131">**WM\_MOUSELEAVE**</span></span>](wm-mouseleave.md)
</dt> <dt>

<span data-ttu-id="ccf26-132">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="ccf26-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ccf26-133">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="ccf26-133">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

