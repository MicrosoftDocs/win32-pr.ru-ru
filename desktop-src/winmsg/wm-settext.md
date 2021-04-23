---
description: Задает текст окна.
ms.assetid: 1b48c309-6903-4139-bf42-e8526963e681
title: Сообщение WM_SETTEXT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3284855d817d5207b0d7572a41774e961c0113f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817681"
---
# <a name="wm_settext-message"></a><span data-ttu-id="875af-103">\_Сообщение SETTEXT WM</span><span class="sxs-lookup"><span data-stu-id="875af-103">WM\_SETTEXT message</span></span>

<span data-ttu-id="875af-104">Задает текст окна.</span><span class="sxs-lookup"><span data-stu-id="875af-104">Sets the text of a window.</span></span>


```C++
#define WM_SETTEXT                      0x000C
```



## <a name="parameters"></a><span data-ttu-id="875af-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="875af-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="875af-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="875af-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="875af-107">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="875af-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="875af-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="875af-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="875af-109">Указатель на строку, завершающуюся нулем, которая является текстом окна.</span><span class="sxs-lookup"><span data-stu-id="875af-109">A pointer to a null-terminated string that is the window text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="875af-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="875af-110">Return value</span></span>

<span data-ttu-id="875af-111">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="875af-111">Type: **LRESULT**</span></span>

<span data-ttu-id="875af-112">Если текст задан, возвращается значение **true** .</span><span class="sxs-lookup"><span data-stu-id="875af-112">The return value is **TRUE** if the text is set.</span></span> <span data-ttu-id="875af-113">**Значение false** (для элемента управления "поле ввода"), **Балансировка нагрузки \_ еррспаце** (для списка) или **CB \_ еррспаце** (для поля со списком), если недостаточно места для установки текста в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="875af-113">It is **FALSE** (for an edit control), **LB\_ERRSPACE** (for a list box), or **CB\_ERRSPACE** (for a combo box) if insufficient space is available to set the text in the edit control.</span></span> <span data-ttu-id="875af-114">Значение **CB \_ Err** , если это сообщение отправляется в поле со списком без элемента управления Edit.</span><span class="sxs-lookup"><span data-stu-id="875af-114">It is **CB\_ERR** if this message is sent to a combo box without an edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="875af-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="875af-115">Remarks</span></span>

<span data-ttu-id="875af-116">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) задает и отображает текст окна.</span><span class="sxs-lookup"><span data-stu-id="875af-116">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets and displays the window text.</span></span> <span data-ttu-id="875af-117">Для элемента управления "поле ввода" текст является содержимым элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="875af-117">For an edit control, the text is the contents of the edit control.</span></span> <span data-ttu-id="875af-118">Для поля со списком текст представляет собой содержимое элемента управления "поле ввода" поля со списком.</span><span class="sxs-lookup"><span data-stu-id="875af-118">For a combo box, the text is the contents of the edit-control portion of the combo box.</span></span> <span data-ttu-id="875af-119">Для кнопки текст — это имя кнопки.</span><span class="sxs-lookup"><span data-stu-id="875af-119">For a button, the text is the button name.</span></span> <span data-ttu-id="875af-120">Для других окон текст — это заголовок окна.</span><span class="sxs-lookup"><span data-stu-id="875af-120">For other windows, the text is the window title.</span></span>

<span data-ttu-id="875af-121">Это сообщение не изменяет текущий выбор в списке поля со списком.</span><span class="sxs-lookup"><span data-stu-id="875af-121">This message does not change the current selection in the list box of a combo box.</span></span> <span data-ttu-id="875af-122">Приложение должно использовать сообщение [**\_ селектстринг CB**](../controls/cb-selectstring.md) для выбора элемента в списке, совпадающего с текстом в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="875af-122">An application should use the [**CB\_SELECTSTRING**](../controls/cb-selectstring.md) message to select the item in a list box that matches the text in the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="875af-123">Требования</span><span class="sxs-lookup"><span data-stu-id="875af-123">Requirements</span></span>



| <span data-ttu-id="875af-124">Требование</span><span class="sxs-lookup"><span data-stu-id="875af-124">Requirement</span></span> | <span data-ttu-id="875af-125">Значение</span><span class="sxs-lookup"><span data-stu-id="875af-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="875af-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="875af-126">Minimum supported client</span></span><br/> | <span data-ttu-id="875af-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="875af-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="875af-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="875af-128">Minimum supported server</span></span><br/> | <span data-ttu-id="875af-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="875af-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="875af-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="875af-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="875af-131"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="875af-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="875af-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="875af-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="875af-133">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="875af-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="875af-134">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="875af-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="875af-135">**WM \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="875af-135">**WM\_GETTEXT**</span></span>](wm-gettext.md)
</dt> <dt>

<span data-ttu-id="875af-136">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="875af-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="875af-137">Windows</span><span class="sxs-lookup"><span data-stu-id="875af-137">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="875af-138">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="875af-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="875af-139">**\_СЕЛЕКТСТРИНГ CB**</span><span class="sxs-lookup"><span data-stu-id="875af-139">**CB\_SELECTSTRING**</span></span>](../controls/cb-selectstring.md)
</dt> </dl>

 

 
