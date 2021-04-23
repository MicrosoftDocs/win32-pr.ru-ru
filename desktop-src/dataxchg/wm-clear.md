---
title: Сообщение WM_CLEAR (Winuser. h)
description: Приложение отправляет \_ сообщение с открытым текстом WM в элемент управления или поле со списком, чтобы удалить (Очистить) текущее выделение (если оно имеется) из элемента управления Edit.
ms.assetid: 6730a725-01ec-4821-9ffc-1ea267d665b3
keywords:
- Обмен данными с сообщениями WM_CLEAR
topic_type:
- apiref
api_name:
- WM_CLEAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a8e325704d1e8b953fe59bfaf4e8fcee62cf40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701055"
---
# <a name="wm_clear-message"></a><span data-ttu-id="2b288-104">\_Сообщение об очистке WM</span><span class="sxs-lookup"><span data-stu-id="2b288-104">WM\_CLEAR message</span></span>

<span data-ttu-id="2b288-105">Приложение отправляет сообщение с **\_ открытым текстом WM** в элемент управления или поле со списком, чтобы удалить (Очистить) текущее выделение (если оно имеется) из элемента управления Edit.</span><span class="sxs-lookup"><span data-stu-id="2b288-105">An application sends a **WM\_CLEAR** message to an edit control or combo box to delete (clear) the current selection, if any, from the edit control.</span></span>


```C++
#define WM_CLEAR                        0x0303
```



## <a name="parameters"></a><span data-ttu-id="2b288-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b288-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b288-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b288-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b288-108">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="2b288-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2b288-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b288-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b288-110">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="2b288-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b288-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b288-111">Return value</span></span>

<span data-ttu-id="2b288-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2b288-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b288-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b288-113">Remarks</span></span>

<span data-ttu-id="2b288-114">Удаление, выполняемое сообщением **WM \_ clear** , можно отменить, отправив элемент управления Edit с сообщением об [**\_ отмене EM**](../controls/em-undo.md) .</span><span class="sxs-lookup"><span data-stu-id="2b288-114">The deletion performed by the **WM\_CLEAR** message can be undone by sending the edit control an [**EM\_UNDO**](../controls/em-undo.md) message.</span></span>

<span data-ttu-id="2b288-115">Чтобы удалить текущее выделение и поместить удаленное содержимое в буфер обмена, используйте сообщение [**WM \_ Cut**](wm-cut.md) .</span><span class="sxs-lookup"><span data-stu-id="2b288-115">To delete the current selection and place the deleted content on the clipboard, use the [**WM\_CUT**](wm-cut.md) message.</span></span>

<span data-ttu-id="2b288-116">При отправке в поле со списком сообщение **об \_ очистке WM** обрабатывается его элементом управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="2b288-116">When sent to a combo box, the **WM\_CLEAR** message is handled by its edit control.</span></span> <span data-ttu-id="2b288-117">Это сообщение не действует при отправке в поле со списком со стилем [**\_ DROPDOWNLIST в CBS**](../controls/combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2b288-117">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b288-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2b288-118">Requirements</span></span>



| <span data-ttu-id="2b288-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2b288-119">Requirement</span></span> | <span data-ttu-id="2b288-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2b288-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b288-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b288-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2b288-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2b288-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2b288-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b288-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2b288-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2b288-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2b288-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2b288-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b288-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b288-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b288-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b288-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="2b288-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="2b288-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2b288-129">**\_копия WM**</span><span class="sxs-lookup"><span data-stu-id="2b288-129">**WM\_COPY**</span></span>](wm-copy.md)
</dt> <dt>

[<span data-ttu-id="2b288-130">**Вырезание WM \_**</span><span class="sxs-lookup"><span data-stu-id="2b288-130">**WM\_CUT**</span></span>](wm-cut.md)
</dt> <dt>

[<span data-ttu-id="2b288-131">**\_Вставка WM**</span><span class="sxs-lookup"><span data-stu-id="2b288-131">**WM\_PASTE**</span></span>](wm-paste.md)
</dt> <dt>

[<span data-ttu-id="2b288-132">**\_Отмена изменений WM**</span><span class="sxs-lookup"><span data-stu-id="2b288-132">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="2b288-133">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="2b288-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2b288-134">Буфер обмена</span><span class="sxs-lookup"><span data-stu-id="2b288-134">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

