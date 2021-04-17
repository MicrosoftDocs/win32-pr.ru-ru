---
title: Сообщение WM_PASTE (Winuser. h)
description: Приложение отправляет \_ сообщение вставки WM в элемент управления или поле со списком, чтобы скопировать текущее содержимое буфера обмена в элемент управления "поле ввода" в текущей позиции курсора. Данные вставляются только в том случае, если буфер обмена содержит данные в \_ текстовом формате CF.
ms.assetid: 6830b511-986f-46ef-a977-7adedffe86ea
keywords:
- Обмен данными с сообщениями WM_PASTE
topic_type:
- apiref
api_name:
- WM_PASTE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86b723830ecdd0f8b7e3faa9da9adcb51161b297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415969"
---
# <a name="wm_paste-message"></a><span data-ttu-id="79cd4-105">\_Сообщение вставки WM</span><span class="sxs-lookup"><span data-stu-id="79cd4-105">WM\_PASTE message</span></span>

<span data-ttu-id="79cd4-106">Приложение отправляет сообщение **\_ вставки WM** в элемент управления или поле со списком, чтобы скопировать текущее содержимое буфера обмена в элемент управления "поле ввода" в текущей позиции курсора.</span><span class="sxs-lookup"><span data-stu-id="79cd4-106">An application sends a **WM\_PASTE** message to an edit control or combo box to copy the current content of the clipboard to the edit control at the current caret position.</span></span> <span data-ttu-id="79cd4-107">Данные вставляются только в том случае, если буфер обмена содержит данные в [**\_ текстовом формате CF**](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="79cd4-107">Data is inserted only if the clipboard contains data in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_PASTE                        0x0302
```



## <a name="parameters"></a><span data-ttu-id="79cd4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="79cd4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79cd4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="79cd4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79cd4-110">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="79cd4-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="79cd4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="79cd4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79cd4-112">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="79cd4-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79cd4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79cd4-113">Return value</span></span>

<span data-ttu-id="79cd4-114">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="79cd4-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79cd4-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79cd4-115">Remarks</span></span>

<span data-ttu-id="79cd4-116">При отправке в поле со списком сообщение **\_ вставки WM** обрабатывается его элементом управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="79cd4-116">When sent to a combo box, the **WM\_PASTE** message is handled by its edit control.</span></span> <span data-ttu-id="79cd4-117">Это сообщение не действует при отправке в поле со списком со стилем [**\_ DROPDOWNLIST в CBS**](../controls/combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="79cd4-117">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="79cd4-118">Требования</span><span class="sxs-lookup"><span data-stu-id="79cd4-118">Requirements</span></span>



| <span data-ttu-id="79cd4-119">Требование</span><span class="sxs-lookup"><span data-stu-id="79cd4-119">Requirement</span></span> | <span data-ttu-id="79cd4-120">Значение</span><span class="sxs-lookup"><span data-stu-id="79cd4-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79cd4-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79cd4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="79cd4-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="79cd4-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="79cd4-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79cd4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="79cd4-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="79cd4-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="79cd4-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="79cd4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="79cd4-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79cd4-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79cd4-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79cd4-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="79cd4-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="79cd4-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="79cd4-129">**WM \_ clear**</span><span class="sxs-lookup"><span data-stu-id="79cd4-129">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="79cd4-130">**\_копия WM**</span><span class="sxs-lookup"><span data-stu-id="79cd4-130">**WM\_COPY**</span></span>](wm-copy.md)
</dt> <dt>

[<span data-ttu-id="79cd4-131">**Вырезание WM \_**</span><span class="sxs-lookup"><span data-stu-id="79cd4-131">**WM\_CUT**</span></span>](wm-cut.md)
</dt> <dt>

[<span data-ttu-id="79cd4-132">**\_Отмена изменений WM**</span><span class="sxs-lookup"><span data-stu-id="79cd4-132">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="79cd4-133">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="79cd4-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="79cd4-134">Буфер обмена</span><span class="sxs-lookup"><span data-stu-id="79cd4-134">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

