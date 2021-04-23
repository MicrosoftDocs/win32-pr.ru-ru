---
title: Сообщение WM_COPY (Winuser. h)
description: Приложение отправляет \_ сообщение копии WM в элемент управления или поле со списком, чтобы скопировать текущий выделенный фрагмент в буфер обмена в \_ ТЕКСТОВОМ формате CF.
ms.assetid: dcac3ad3-1e70-4b71-accd-261587224e60
keywords:
- Обмен данными с сообщениями WM_COPY
topic_type:
- apiref
api_name:
- WM_COPY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b298248d75b1d25d1bfef8347347fe2f1a6c7916
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "105703480"
---
# <a name="wm_copy-message"></a><span data-ttu-id="985ef-104">\_Сообщение о копировании WM</span><span class="sxs-lookup"><span data-stu-id="985ef-104">WM\_COPY message</span></span>

<span data-ttu-id="985ef-105">Приложение отправляет сообщение **\_ копии WM** в элемент управления или поле со списком, чтобы скопировать текущий выделенный фрагмент в буфер обмена в [**\_ текстовом формате CF**](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="985ef-105">An application sends the **WM\_COPY** message to an edit control or combo box to copy the current selection to the clipboard in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_COPY                         0x0301
```



## <a name="parameters"></a><span data-ttu-id="985ef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="985ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="985ef-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="985ef-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="985ef-108">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="985ef-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="985ef-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="985ef-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="985ef-110">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="985ef-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="985ef-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="985ef-111">Return value</span></span>

<span data-ttu-id="985ef-112">Возвращает ненулевое значение при успешном выполнении, в противном случае — ноль.</span><span class="sxs-lookup"><span data-stu-id="985ef-112">Returns nonzero value on success, else zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="985ef-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="985ef-113">Remarks</span></span>

<span data-ttu-id="985ef-114">При отправке в поле со списком сообщение **о \_ копировании WM** обрабатывается его элементом управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="985ef-114">When sent to a combo box, the **WM\_COPY** message is handled by its edit control.</span></span> <span data-ttu-id="985ef-115">Это сообщение не действует при отправке в поле со списком со стилем [**\_ DROPDOWNLIST в CBS**](../controls/combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="985ef-115">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="985ef-116">Требования</span><span class="sxs-lookup"><span data-stu-id="985ef-116">Requirements</span></span>



| <span data-ttu-id="985ef-117">Требование</span><span class="sxs-lookup"><span data-stu-id="985ef-117">Requirement</span></span> | <span data-ttu-id="985ef-118">Значение</span><span class="sxs-lookup"><span data-stu-id="985ef-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="985ef-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="985ef-119">Minimum supported client</span></span><br/> | <span data-ttu-id="985ef-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="985ef-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="985ef-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="985ef-121">Minimum supported server</span></span><br/> | <span data-ttu-id="985ef-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="985ef-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="985ef-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="985ef-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="985ef-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="985ef-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="985ef-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="985ef-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="985ef-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="985ef-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="985ef-127">**WM \_ clear**</span><span class="sxs-lookup"><span data-stu-id="985ef-127">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="985ef-128">**Вырезание WM \_**</span><span class="sxs-lookup"><span data-stu-id="985ef-128">**WM\_CUT**</span></span>](wm-cut.md)
</dt> <dt>

[<span data-ttu-id="985ef-129">**\_Вставка WM**</span><span class="sxs-lookup"><span data-stu-id="985ef-129">**WM\_PASTE**</span></span>](wm-paste.md)
</dt> <dt>

[<span data-ttu-id="985ef-130">**\_Отмена изменений WM**</span><span class="sxs-lookup"><span data-stu-id="985ef-130">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="985ef-131">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="985ef-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="985ef-132">Буфер обмена</span><span class="sxs-lookup"><span data-stu-id="985ef-132">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

