---
description: Связывает новый большой или маленький значок с окном. Система отображает крупный значок в диалоговом окне ALT + TAB, а маленький значок в заголовке окна.
ms.assetid: c86620f2-893b-46f8-8254-1d7c4c142f37
title: Сообщение WM_SETICON (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88bec7fc653123ba0a950c96bc1f54ebf436b0d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264519"
---
# <a name="wm_seticon-message"></a><span data-ttu-id="a9218-104">\_Сообщение СЕТИКОН WM</span><span class="sxs-lookup"><span data-stu-id="a9218-104">WM\_SETICON message</span></span>

<span data-ttu-id="a9218-105">Связывает новый большой или маленький значок с окном.</span><span class="sxs-lookup"><span data-stu-id="a9218-105">Associates a new large or small icon with a window.</span></span> <span data-ttu-id="a9218-106">Система отображает крупный значок в диалоговом окне ALT + TAB, а маленький значок в заголовке окна.</span><span class="sxs-lookup"><span data-stu-id="a9218-106">The system displays the large icon in the ALT+TAB dialog box, and the small icon in the window caption.</span></span>


```C++
#define WM_SETICON                      0x0080
```



## <a name="parameters"></a><span data-ttu-id="a9218-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9218-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9218-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a9218-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9218-109">Тип устанавливаемого значка.</span><span class="sxs-lookup"><span data-stu-id="a9218-109">The type of icon to be set.</span></span> <span data-ttu-id="a9218-110">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="a9218-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a9218-111">Значение</span><span class="sxs-lookup"><span data-stu-id="a9218-111">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="a9218-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a9218-112">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <span data-ttu-id="a9218-113"><dt>**Значок \_ БОЛЬШОЙ**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a9218-113"><dt>**ICON\_BIG**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="a9218-114">Задайте крупный значок для окна.</span><span class="sxs-lookup"><span data-stu-id="a9218-114">Set the large icon for the window.</span></span><br/> |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <span data-ttu-id="a9218-115"><dt>**Значок \_ Малый**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a9218-115"><dt>**ICON\_SMALL**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="a9218-116">Задайте маленький значок для окна.</span><span class="sxs-lookup"><span data-stu-id="a9218-116">Set the small icon for the window.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a9218-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9218-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9218-118">Маркер нового большого или маленького значка.</span><span class="sxs-lookup"><span data-stu-id="a9218-118">A handle to the new large or small icon.</span></span> <span data-ttu-id="a9218-119">Если этот параметр имеет **значение NULL**, значок, указанный параметром *wParam*, удаляется.</span><span class="sxs-lookup"><span data-stu-id="a9218-119">If this parameter is **NULL**, the icon indicated by *wParam* is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9218-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a9218-120">Return value</span></span>

<span data-ttu-id="a9218-121">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="a9218-121">Type: **LRESULT**</span></span>

<span data-ttu-id="a9218-122">Возвращаемое значение — это обработчик предыдущего большого или маленького значка в зависимости от значения *wParam*.</span><span class="sxs-lookup"><span data-stu-id="a9218-122">The return value is a handle to the previous large or small icon, depending on the value of *wParam*.</span></span> <span data-ttu-id="a9218-123">Имеет **значение NULL** , если в окне ранее не было значка типа, указанного параметром *wParam*.</span><span class="sxs-lookup"><span data-stu-id="a9218-123">It is **NULL** if the window previously had no icon of the type indicated by *wParam*.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9218-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a9218-124">Remarks</span></span>

<span data-ttu-id="a9218-125">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) возвращает маркер предыдущего большого или маленького значка, связанного с окном, в зависимости от значения *wParam*.</span><span class="sxs-lookup"><span data-stu-id="a9218-125">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns a handle to the previous large or small icon associated with the window, depending on the value of *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9218-126">Требования</span><span class="sxs-lookup"><span data-stu-id="a9218-126">Requirements</span></span>



| <span data-ttu-id="a9218-127">Требование</span><span class="sxs-lookup"><span data-stu-id="a9218-127">Requirement</span></span> | <span data-ttu-id="a9218-128">Значение</span><span class="sxs-lookup"><span data-stu-id="a9218-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9218-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a9218-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a9218-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a9218-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a9218-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a9218-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a9218-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a9218-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a9218-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a9218-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9218-134"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9218-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9218-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9218-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="a9218-136">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="a9218-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a9218-137">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="a9218-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="a9218-138">**\_значок WM**</span><span class="sxs-lookup"><span data-stu-id="a9218-138">**WM\_GETICON**</span></span>](wm-geticon.md)
</dt> <dt>

<span data-ttu-id="a9218-139">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="a9218-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a9218-140">Windows</span><span class="sxs-lookup"><span data-stu-id="a9218-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 
