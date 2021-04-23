---
title: Сообщение WM_CUT (Winuser. h)
description: Приложение отправляет \_ сообщение WM Cut в элемент управления или поле со списком, чтобы удалить (вырезать) текущий выделенный фрагмент (если таковой имеется) в элементе управления "поле ввода" и скопировать удаленный текст в буфер обмена в \_ ТЕКСТОВОМ формате CF.
ms.assetid: 6ac45589-3e34-491c-9562-e072ddc478f9
keywords:
- Обмен данными с сообщениями WM_CUT
topic_type:
- apiref
api_name:
- WM_CUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a63dfe85fb637636fbabbce5fa139699fd09a65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672627"
---
# <a name="wm_cut-message"></a><span data-ttu-id="6b7ba-104">\_Вырезание сообщения WM</span><span class="sxs-lookup"><span data-stu-id="6b7ba-104">WM\_CUT message</span></span>

<span data-ttu-id="6b7ba-105">Приложение отправляет сообщение **WM \_ Cut** в элемент управления или поле со списком, чтобы удалить (вырезать) текущий выделенный фрагмент (если таковой имеется) в элементе управления "поле ввода" и скопировать удаленный текст в буфер обмена в [**\_ текстовом формате CF**](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="6b7ba-105">An application sends a **WM\_CUT** message to an edit control or combo box to delete (cut) the current selection, if any, in the edit control and copy the deleted text to the clipboard in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_CUT                          0x0300
```



## <a name="parameters"></a><span data-ttu-id="6b7ba-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b7ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b7ba-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b7ba-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b7ba-108">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="6b7ba-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6b7ba-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b7ba-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b7ba-110">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="6b7ba-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b7ba-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b7ba-111">Return value</span></span>

<span data-ttu-id="6b7ba-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6b7ba-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b7ba-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b7ba-113">Remarks</span></span>

<span data-ttu-id="6b7ba-114">Удаление, выполняемое сообщением команды **WM \_ Cut** , можно отменить, отправив элемент управления Edit с сообщением об [**\_ отмене EM**](../controls/em-undo.md) .</span><span class="sxs-lookup"><span data-stu-id="6b7ba-114">The deletion performed by the **WM\_CUT** message can be undone by sending the edit control an [**EM\_UNDO**](../controls/em-undo.md) message.</span></span>

<span data-ttu-id="6b7ba-115">Чтобы удалить текущее выделение без помещения удаленного текста в буфер обмена, используйте сообщение об [**\_ очистке WM**](wm-clear.md) .</span><span class="sxs-lookup"><span data-stu-id="6b7ba-115">To delete the current selection without placing the deleted text on the clipboard, use the [**WM\_CLEAR**](wm-clear.md) message.</span></span>

<span data-ttu-id="6b7ba-116">При отправке в поле со списком сообщение **\_ вырезания WM** обрабатывается его элементом управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="6b7ba-116">When sent to a combo box, the **WM\_CUT** message is handled by its edit control.</span></span> <span data-ttu-id="6b7ba-117">Это сообщение не действует при отправке в поле со списком со стилем [**\_ DROPDOWNLIST в CBS**](../controls/combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6b7ba-117">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b7ba-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6b7ba-118">Requirements</span></span>



| <span data-ttu-id="6b7ba-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6b7ba-119">Requirement</span></span> | <span data-ttu-id="6b7ba-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6b7ba-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b7ba-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b7ba-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6b7ba-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6b7ba-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6b7ba-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b7ba-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6b7ba-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6b7ba-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6b7ba-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6b7ba-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b7ba-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b7ba-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b7ba-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b7ba-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="6b7ba-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="6b7ba-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6b7ba-129">**WM \_ clear**</span><span class="sxs-lookup"><span data-stu-id="6b7ba-129">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="6b7ba-130">**\_копия WM**</span><span class="sxs-lookup"><span data-stu-id="6b7ba-130">**WM\_COPY**</span></span>](wm-copy.md)
</dt> <dt>

[<span data-ttu-id="6b7ba-131">**\_Вставка WM**</span><span class="sxs-lookup"><span data-stu-id="6b7ba-131">**WM\_PASTE**</span></span>](wm-paste.md)
</dt> <dt>

[<span data-ttu-id="6b7ba-132">**\_Отмена изменений WM**</span><span class="sxs-lookup"><span data-stu-id="6b7ba-132">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="6b7ba-133">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="6b7ba-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6b7ba-134">Буфер обмена</span><span class="sxs-lookup"><span data-stu-id="6b7ba-134">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="6b7ba-135">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="6b7ba-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="6b7ba-136">**\_Отмена EM**</span><span class="sxs-lookup"><span data-stu-id="6b7ba-136">**EM\_UNDO**</span></span>](../controls/em-undo.md)
</dt> </dl>

 

