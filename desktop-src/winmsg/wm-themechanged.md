---
description: Вещание в каждом окне после события изменения темы. Примерами событий изменения темы являются активация темы, деактивация темы или переход от одной темы к другой.
ms.assetid: 1a4051ac-cc6e-4520-ab66-d0a41a8a4c73
title: Сообщение WM_THEMECHANGED (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc15ab64126ff8972b858ef43ddd4d92cd62f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809550"
---
# <a name="wm_themechanged-message"></a><span data-ttu-id="ba477-104">\_Сообщение СЕМЕЧАНЖЕД WM</span><span class="sxs-lookup"><span data-stu-id="ba477-104">WM\_THEMECHANGED message</span></span>

<span data-ttu-id="ba477-105">Вещание в каждом окне после события изменения темы.</span><span class="sxs-lookup"><span data-stu-id="ba477-105">Broadcast to every window following a theme change event.</span></span> <span data-ttu-id="ba477-106">Примерами событий изменения темы являются активация темы, деактивация темы или переход от одной темы к другой.</span><span class="sxs-lookup"><span data-stu-id="ba477-106">Examples of theme change events are the activation of a theme, the deactivation of a theme, or a transition from one theme to another.</span></span>


```C++
#define WM_THEMECHANGED                 0x031A
```



## <a name="parameters"></a><span data-ttu-id="ba477-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba477-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba477-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ba477-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba477-109">Этот параметр зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="ba477-109">This parameter is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ba477-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba477-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba477-111">Этот параметр зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="ba477-111">This parameter is reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba477-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba477-112">Return value</span></span>

<span data-ttu-id="ba477-113">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="ba477-113">Type: **LRESULT**</span></span>

<span data-ttu-id="ba477-114">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="ba477-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba477-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba477-115">Remarks</span></span>

<span data-ttu-id="ba477-116">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ba477-116">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="ba477-117">Это сообщение отправляется операционной системой.</span><span class="sxs-lookup"><span data-stu-id="ba477-117">This message is posted by the operating system.</span></span> <span data-ttu-id="ba477-118">Обычно приложения не отправляют это сообщение.</span><span class="sxs-lookup"><span data-stu-id="ba477-118">Applications typically do not send this message.</span></span>

 

<span data-ttu-id="ba477-119">Темы — это спецификации для внешнего вида элементов управления, чтобы визуальный элемент элемента управления обрабатывался отдельно от его функциональности.</span><span class="sxs-lookup"><span data-stu-id="ba477-119">Themes are specifications for the appearance of controls, so that the visual element of a control is treated separately from its functionality.</span></span>

<span data-ttu-id="ba477-120">Чтобы освободить существующий маркер темы, вызовите [**клосесемедата**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata).</span><span class="sxs-lookup"><span data-stu-id="ba477-120">To release an existing theme handle, call [**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata).</span></span> <span data-ttu-id="ba477-121">Чтобы получить новый маркер темы, используйте [**опенсемедата**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata).</span><span class="sxs-lookup"><span data-stu-id="ba477-121">To acquire a new theme handle, use [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata).</span></span>

<span data-ttu-id="ba477-122">После вещания **WM \_ семечанжед** все существующие дескрипторы тем недопустимы.</span><span class="sxs-lookup"><span data-stu-id="ba477-122">Following the **WM\_THEMECHANGED** broadcast, any existing theme handles are invalid.</span></span> <span data-ttu-id="ba477-123">При получении сообщения **WM \_ семечанжед** окно, поддерживающее темы, должно освободить и повторно открыть любые существующие дескрипторы темы.</span><span class="sxs-lookup"><span data-stu-id="ba477-123">A theme-aware window should release and reopen any of its pre-existing theme handles when it receives the **WM\_THEMECHANGED** message.</span></span> <span data-ttu-id="ba477-124">Если функция [**опенсемедата**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) возвращает **значение NULL**, окно не должно рисоваться.</span><span class="sxs-lookup"><span data-stu-id="ba477-124">If the [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) function returns **NULL**, the window should paint unthemed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba477-125">Требования</span><span class="sxs-lookup"><span data-stu-id="ba477-125">Requirements</span></span>



| <span data-ttu-id="ba477-126">Требование</span><span class="sxs-lookup"><span data-stu-id="ba477-126">Requirement</span></span> | <span data-ttu-id="ba477-127">Значение</span><span class="sxs-lookup"><span data-stu-id="ba477-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba477-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba477-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ba477-129">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ba477-129">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ba477-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba477-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ba477-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ba477-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ba477-132">Header</span><span class="sxs-lookup"><span data-stu-id="ba477-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba477-133"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba477-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba477-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba477-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="ba477-135">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="ba477-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="ba477-136">**клосесемедата**</span><span class="sxs-lookup"><span data-stu-id="ba477-136">**CloseThemeData**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata)
</dt> <dt>

[<span data-ttu-id="ba477-137">**иссемеактиве**</span><span class="sxs-lookup"><span data-stu-id="ba477-137">**IsThemeActive**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-isthemeactive)
</dt> <dt>

[<span data-ttu-id="ba477-138">**опенсемедата**</span><span class="sxs-lookup"><span data-stu-id="ba477-138">**OpenThemeData**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata)
</dt> </dl>

 

 
