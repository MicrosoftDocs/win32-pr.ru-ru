---
description: Сообщение WM \_ сисколорчанже отправляется во все окна верхнего уровня, когда в параметр системного цвета вносится изменение.
ms.assetid: ffe61768-86d6-4ea8-ae2d-1095a9afa925
title: Сообщение WM_SYSCOLORCHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac3883f0534d91a6d852b0e70fbb4edabdcab56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986056"
---
# <a name="wm_syscolorchange-message"></a><span data-ttu-id="a89fd-103">\_Сообщение СИСКОЛОРЧАНЖЕ WM</span><span class="sxs-lookup"><span data-stu-id="a89fd-103">WM\_SYSCOLORCHANGE message</span></span>

<span data-ttu-id="a89fd-104">Сообщение **WM \_ сисколорчанже** отправляется во все окна верхнего уровня, когда в параметр системного цвета вносится изменение.</span><span class="sxs-lookup"><span data-stu-id="a89fd-104">The **WM\_SYSCOLORCHANGE** message is sent to all top-level windows when a change is made to a system color setting.</span></span>

<span data-ttu-id="a89fd-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a89fd-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="a89fd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a89fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a89fd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a89fd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a89fd-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="a89fd-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a89fd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a89fd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a89fd-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="a89fd-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a89fd-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="a89fd-111">Remarks</span></span>

<span data-ttu-id="a89fd-112">Система отправляет сообщение [**WM \_ Paint**](wm-paint.md) в любое окно, на которое влияет изменение цвета системы.</span><span class="sxs-lookup"><span data-stu-id="a89fd-112">The system sends a [**WM\_PAINT**](wm-paint.md) message to any window that is affected by a system color change.</span></span>

<span data-ttu-id="a89fd-113">Приложения, имеющие кисти, использующие существующие системные цвета, должны удалить эти кисти и создать их повторно с помощью новых системных цветов.</span><span class="sxs-lookup"><span data-stu-id="a89fd-113">Applications that have brushes using the existing system colors should delete those brushes and re-create them using the new system colors.</span></span>

<span data-ttu-id="a89fd-114">Окна верхнего уровня, использующие стандартные элементы управления, должны пересылать сообщение **\_ сисколорчанже WM** элементам управления. в противном случае элементы управления не будут уведомлены об изменении цвета.</span><span class="sxs-lookup"><span data-stu-id="a89fd-114">Top level windows that use common controls must forward the **WM\_SYSCOLORCHANGE** message to the controls; otherwise, the controls will not be notified of the color change.</span></span> <span data-ttu-id="a89fd-115">Это гарантирует, что цвета, используемые общими элементами управления, будут соответствовать значениям, используемым другими объектами пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a89fd-115">This ensures that the colors used by your common controls are consistent with those used by other user interface objects.</span></span> <span data-ttu-id="a89fd-116">Например, элемент управления ToolBar использует цвет "трехмерные объекты" для рисования своих кнопок.</span><span class="sxs-lookup"><span data-stu-id="a89fd-116">For example, a toolbar control uses the "3D Objects" color to draw its buttons.</span></span> <span data-ttu-id="a89fd-117">Если пользователь изменяет цвет 3D-объектов, но сообщение **WM \_ сисколорчанже** не пересылается на панель инструментов, кнопки панели инструментов остаются в исходном цвете, а цвет других кнопок в системе изменится.</span><span class="sxs-lookup"><span data-stu-id="a89fd-117">If the user changes the 3D Objects color but the **WM\_SYSCOLORCHANGE** message is not forwarded to the toolbar, the toolbar buttons will remain in their original color while the color of other buttons in the system changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="a89fd-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a89fd-118">Requirements</span></span>



| <span data-ttu-id="a89fd-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a89fd-119">Requirement</span></span> | <span data-ttu-id="a89fd-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a89fd-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a89fd-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a89fd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a89fd-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a89fd-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a89fd-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a89fd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a89fd-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a89fd-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a89fd-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a89fd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a89fd-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a89fd-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a89fd-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a89fd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a89fd-128">Общие сведения о цветах</span><span class="sxs-lookup"><span data-stu-id="a89fd-128">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="a89fd-129">Цветные сообщения</span><span class="sxs-lookup"><span data-stu-id="a89fd-129">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="a89fd-130">**WM \_ Paint**</span><span class="sxs-lookup"><span data-stu-id="a89fd-130">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 
