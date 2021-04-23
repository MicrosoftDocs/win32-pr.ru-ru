---
title: Сообщение WM_INITMENU (Winuser. h)
description: Посылается, когда меню собирается стать активным.
ms.assetid: d0fcc6d8-f57c-4d04-b9e7-4cfab6add173
keywords:
- WM_INITMENU меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_INITMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94626b99a5016efaa9427d1ae8b3b3122e599965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710537"
---
# <a name="wm_initmenu-message"></a><span data-ttu-id="a9daf-104">\_Сообщение ИНИТМЕНУ WM</span><span class="sxs-lookup"><span data-stu-id="a9daf-104">WM\_INITMENU message</span></span>

<span data-ttu-id="a9daf-105">Посылается, когда меню собирается стать активным.</span><span class="sxs-lookup"><span data-stu-id="a9daf-105">Sent when a menu is about to become active.</span></span> <span data-ttu-id="a9daf-106">Это происходит, когда пользователь щелкает элемент в строке меню или нажимает клавишу меню.</span><span class="sxs-lookup"><span data-stu-id="a9daf-106">It occurs when the user clicks an item on the menu bar or presses a menu key.</span></span> <span data-ttu-id="a9daf-107">Это позволяет приложению изменить меню перед его отображением.</span><span class="sxs-lookup"><span data-stu-id="a9daf-107">This allows the application to modify the menu before it is displayed.</span></span>

<span data-ttu-id="a9daf-108">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a9daf-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INITMENU                     0x0116
```



## <a name="parameters"></a><span data-ttu-id="a9daf-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9daf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9daf-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a9daf-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9daf-111">Описатель для инициализации меню.</span><span class="sxs-lookup"><span data-stu-id="a9daf-111">A handle to the menu to be initialized.</span></span>

</dd> <dt>

<span data-ttu-id="a9daf-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9daf-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9daf-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="a9daf-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9daf-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a9daf-114">Return value</span></span>

<span data-ttu-id="a9daf-115">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="a9daf-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9daf-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a9daf-116">Remarks</span></span>

<span data-ttu-id="a9daf-117">Сообщение **WM \_ инитмену** отправляется только при первом обращении к меню. для каждого доступа создается только одно сообщение **\_ инитмену WM** .</span><span class="sxs-lookup"><span data-stu-id="a9daf-117">A **WM\_INITMENU** message is sent only when a menu is first accessed; only one **WM\_INITMENU** message is generated for each access.</span></span> <span data-ttu-id="a9daf-118">Например, перемещение мыши по нескольким пунктам меню, удерживая нажатой кнопку, не создает новые сообщения.</span><span class="sxs-lookup"><span data-stu-id="a9daf-118">For example, moving the mouse across several menu items while holding down the button does not generate new messages.</span></span> <span data-ttu-id="a9daf-119">**WM \_ ИНИТМЕНУ** не предоставляет сведения о пунктах меню.</span><span class="sxs-lookup"><span data-stu-id="a9daf-119">**WM\_INITMENU** does not provide information about menu items.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9daf-120">Требования</span><span class="sxs-lookup"><span data-stu-id="a9daf-120">Requirements</span></span>



| <span data-ttu-id="a9daf-121">Требование</span><span class="sxs-lookup"><span data-stu-id="a9daf-121">Requirement</span></span> | <span data-ttu-id="a9daf-122">Значение</span><span class="sxs-lookup"><span data-stu-id="a9daf-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9daf-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a9daf-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a9daf-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a9daf-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a9daf-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a9daf-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a9daf-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a9daf-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a9daf-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a9daf-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9daf-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9daf-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9daf-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9daf-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="a9daf-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="a9daf-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a9daf-131">**WM \_ инитменупопуп**</span><span class="sxs-lookup"><span data-stu-id="a9daf-131">**WM\_INITMENUPOPUP**</span></span>](wm-initmenupopup.md)
</dt> <dt>

<span data-ttu-id="a9daf-132">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="a9daf-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a9daf-133">Сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="a9daf-133">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

