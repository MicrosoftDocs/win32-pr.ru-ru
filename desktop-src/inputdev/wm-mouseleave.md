---
title: Сообщение WM_MOUSELEAVE (Winuser. h)
description: Отправляется в окно, когда курсор покидает клиентскую область окна, указанное в предыдущем вызове метода TrackMouseEven.
ms.assetid: b23d24ff-531a-4b6d-8848-f82ac5568995
keywords:
- WM_MOUSELEAVE ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_MOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc96022e94df7f518b21b1c9a46895fc9204b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490035"
---
# <a name="wm_mouseleave-message"></a><span data-ttu-id="db52c-104">\_Сообщение WM MOUSELEAVE</span><span class="sxs-lookup"><span data-stu-id="db52c-104">WM\_MOUSELEAVE message</span></span>

<span data-ttu-id="db52c-105">Отправляется в окно, когда курсор покидает клиентскую область окна, указанное в предыдущем вызове метода [**TrackMouseEven**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span><span class="sxs-lookup"><span data-stu-id="db52c-105">Posted to a window when the cursor leaves the client area of the window specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="db52c-106">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="db52c-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSELEAVE                   0x02A3
```



## <a name="parameters"></a><span data-ttu-id="db52c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="db52c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db52c-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="db52c-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db52c-109">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="db52c-109">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="db52c-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db52c-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db52c-111">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="db52c-111">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db52c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db52c-112">Return value</span></span>

<span data-ttu-id="db52c-113">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="db52c-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="db52c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db52c-114">Remarks</span></span>

<span data-ttu-id="db52c-115">При создании этого сообщения все записи, запрошенные [**TrackMouseEven**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) , отменяются.</span><span class="sxs-lookup"><span data-stu-id="db52c-115">All tracking requested by [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) is canceled when this message is generated.</span></span> <span data-ttu-id="db52c-116">Приложение должно вызвать **TrackMouseEven** , когда указатель мыши перейдет в окно, если он требует дополнительного отслеживания поведения при наведении указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="db52c-116">The application must call **TrackMouseEvent** when the mouse reenters its window if it requires further tracking of mouse hover behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="db52c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="db52c-117">Requirements</span></span>



| <span data-ttu-id="db52c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="db52c-118">Requirement</span></span> | <span data-ttu-id="db52c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="db52c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db52c-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db52c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="db52c-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="db52c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="db52c-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db52c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="db52c-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="db52c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="db52c-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="db52c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="db52c-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db52c-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db52c-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db52c-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="db52c-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="db52c-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="db52c-128">**Захват**</span><span class="sxs-lookup"><span data-stu-id="db52c-128">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="db52c-129">**сеткаптуре**</span><span class="sxs-lookup"><span data-stu-id="db52c-129">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="db52c-130">**TrackMouseEven**</span><span class="sxs-lookup"><span data-stu-id="db52c-130">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="db52c-131">**TRACKMOUSEEVEN**</span><span class="sxs-lookup"><span data-stu-id="db52c-131">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="db52c-132">**WM \_ нкмауселеаве**</span><span class="sxs-lookup"><span data-stu-id="db52c-132">**WM\_NCMOUSELEAVE**</span></span>](wm-ncmouseleave.md)
</dt> <dt>

<span data-ttu-id="db52c-133">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="db52c-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="db52c-134">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="db52c-134">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

