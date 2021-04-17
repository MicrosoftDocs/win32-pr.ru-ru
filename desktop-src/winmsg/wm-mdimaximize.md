---
description: Приложение отправляет \_ сообщение WM мдимаксимизе в окно клиента многодокументного интерфейса (MDI) для максимального увеличения дочернего окна MDI.
ms.assetid: 7c5e4157-13f6-40d7-a64a-076bd14aca0d
title: Сообщение WM_MDIMAXIMIZE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8372bcb25f35a52793292de4fd94a4a9dadafe6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710969"
---
# <a name="wm_mdimaximize-message"></a><span data-ttu-id="a0652-103">\_Сообщение МДИМАКСИМИЗЕ WM</span><span class="sxs-lookup"><span data-stu-id="a0652-103">WM\_MDIMAXIMIZE message</span></span>

<span data-ttu-id="a0652-104">Приложение отправляет сообщение **WM \_ мдимаксимизе** в окно клиента многодокументного интерфейса (MDI) для максимального увеличения дочернего окна MDI.</span><span class="sxs-lookup"><span data-stu-id="a0652-104">An application sends the **WM\_MDIMAXIMIZE** message to a multiple-document interface (MDI) client window to maximize an MDI child window.</span></span> <span data-ttu-id="a0652-105">Система изменяет размер дочернего окна, сделав его клиентской областью заполнение клиентского окна.</span><span class="sxs-lookup"><span data-stu-id="a0652-105">The system resizes the child window to make its client area fill the client window.</span></span> <span data-ttu-id="a0652-106">Система помещает значок меню окна дочернего окна в крайнее правое положение строки меню окна фрейма и помещает значок восстановления дочернего окна в крайнюю левую точку.</span><span class="sxs-lookup"><span data-stu-id="a0652-106">The system places the child window's window menu icon in the rightmost position of the frame window's menu bar, and places the child window's restore icon in the leftmost position.</span></span> <span data-ttu-id="a0652-107">Система также добавляет текст заголовка дочернего окна к окну окна фрейма.</span><span class="sxs-lookup"><span data-stu-id="a0652-107">The system also appends the title bar text of the child window to that of the frame window.</span></span>


```C++
#define WM_MDIMAXIMIZE                  0x0225
```



## <a name="parameters"></a><span data-ttu-id="a0652-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0652-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0652-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a0652-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0652-110">Обработчик для развернутого дочернего окна MDI.</span><span class="sxs-lookup"><span data-stu-id="a0652-110">A handle to the MDI child window to be maximized.</span></span>

</dd> <dt>

<span data-ttu-id="a0652-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0652-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0652-112">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="a0652-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0652-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0652-113">Return value</span></span>

<span data-ttu-id="a0652-114">Тип: **ноль**</span><span class="sxs-lookup"><span data-stu-id="a0652-114">Type: **zero**</span></span>

<span data-ttu-id="a0652-115">Возвращаемое значение всегда равно нулю.</span><span class="sxs-lookup"><span data-stu-id="a0652-115">The return value is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0652-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0652-116">Remarks</span></span>

<span data-ttu-id="a0652-117">Если клиентское MDI-окно получает сообщение, которое изменяет активацию своих дочерних окон, пока текущее активное дочернее окно MDI находится в развернутом состоянии, система восстанавливает активное дочернее окно и разворачивает вновь активированное дочернее окно.</span><span class="sxs-lookup"><span data-stu-id="a0652-117">If an MDI client window receives any message that changes the activation of its child windows while the currently active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0652-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a0652-118">Requirements</span></span>



| <span data-ttu-id="a0652-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a0652-119">Requirement</span></span> | <span data-ttu-id="a0652-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a0652-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0652-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0652-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a0652-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a0652-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a0652-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0652-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a0652-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a0652-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a0652-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a0652-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0652-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0652-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0652-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0652-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="a0652-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="a0652-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a0652-129">**WM \_ мдиресторе**</span><span class="sxs-lookup"><span data-stu-id="a0652-129">**WM\_MDIRESTORE**</span></span>](wm-mdirestore.md)
</dt> <dt>

<span data-ttu-id="a0652-130">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="a0652-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a0652-131">Интерфейс с несколькими документами</span><span class="sxs-lookup"><span data-stu-id="a0652-131">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




