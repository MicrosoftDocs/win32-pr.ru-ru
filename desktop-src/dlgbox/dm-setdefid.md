---
title: Сообщение DM_SETDEFID (Winuser. h)
description: Изменяет идентификатор кнопки отправки по умолчанию для диалогового окна.
ms.assetid: 30720fa1-48cb-42d4-8370-87bdbaa34600
keywords:
- DM_SETDEFID диалоговых окон сообщений
topic_type:
- apiref
api_name:
- DM_SETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ceda9ac9e8fd399604e9c55431b8fcd74646f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535264"
---
# <a name="dm_setdefid-message"></a><span data-ttu-id="91eb3-104">\_Сообщение СЕТДЕФИД DM</span><span class="sxs-lookup"><span data-stu-id="91eb3-104">DM\_SETDEFID message</span></span>

<span data-ttu-id="91eb3-105">Изменяет идентификатор кнопки отправки по умолчанию для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="91eb3-105">Changes the identifier of the default push button for a dialog box.</span></span>


```C++
#define WM_USER              0x0400
#define DM_SETDEFID         (WM_USER+1)
```



## <a name="parameters"></a><span data-ttu-id="91eb3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="91eb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91eb3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91eb3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91eb3-108">Идентификатор элемента управления "Кнопка", который станет значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91eb3-108">The identifier of a push button control that will become the default.</span></span>

</dd> <dt>

<span data-ttu-id="91eb3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91eb3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91eb3-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="91eb3-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91eb3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91eb3-111">Return value</span></span>

<span data-ttu-id="91eb3-112">Возвращаемое значение всегда равно **true**.</span><span class="sxs-lookup"><span data-stu-id="91eb3-112">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="91eb3-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91eb3-113">Remarks</span></span>

<span data-ttu-id="91eb3-114">Это сообщение обрабатывается функцией [**дефдлгпрок**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) .</span><span class="sxs-lookup"><span data-stu-id="91eb3-114">This message is processed by the [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) function.</span></span> <span data-ttu-id="91eb3-115">Чтобы задать кнопку по умолчанию, функция может отправлять сообщения [**WM \_ Жетдлгкоде**](wm-getdlgcode.md) и [**BM \_ SETSTYLE**](../controls/bm-setstyle.md) в указанный элемент управления и текущую кнопку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91eb3-115">To set the default push button, the function can send [**WM\_GETDLGCODE**](wm-getdlgcode.md) and [**BM\_SETSTYLE**](../controls/bm-setstyle.md) messages to the specified control and the current default push button.</span></span>

<span data-ttu-id="91eb3-116">Использование сообщения **DM \_ сетдефид** может привести к тому, что несколько кнопок будут иметь состояние кнопки отправки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91eb3-116">Using the **DM\_SETDEFID** message can result in more than one button appearing to have the default push button state.</span></span> <span data-ttu-id="91eb3-117">Когда система открывает диалоговое окно, она рисует первую кнопку отправки в шаблоне диалогового окна с границей состояния по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91eb3-117">When the system brings up a dialog, it draws the first push button in the dialog template with the default state border.</span></span> <span data-ttu-id="91eb3-118">Отправка сообщения **\_ сетдефид DM** для изменения кнопки по умолчанию не всегда приведет к удалению границы состояния по умолчанию из первой кнопки отправки.</span><span class="sxs-lookup"><span data-stu-id="91eb3-118">Sending a **DM\_SETDEFID** message to change the default button will not always remove the default state border from the first push button.</span></span> <span data-ttu-id="91eb3-119">В таких случаях приложение должно отправить сообщение [**BM \_ SETSTYLE**](../controls/bm-setstyle.md) , чтобы изменить стиль границы первой кнопки.</span><span class="sxs-lookup"><span data-stu-id="91eb3-119">In these cases, the application should send a [**BM\_SETSTYLE**](../controls/bm-setstyle.md) message to change the first push button border style.</span></span>

## <a name="requirements"></a><span data-ttu-id="91eb3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="91eb3-120">Requirements</span></span>



| <span data-ttu-id="91eb3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="91eb3-121">Requirement</span></span> | <span data-ttu-id="91eb3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="91eb3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91eb3-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91eb3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="91eb3-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="91eb3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="91eb3-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91eb3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="91eb3-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="91eb3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="91eb3-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="91eb3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="91eb3-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91eb3-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91eb3-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91eb3-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="91eb3-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="91eb3-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="91eb3-131">**дефдлгпрок**</span><span class="sxs-lookup"><span data-stu-id="91eb3-131">**DefDlgProc**</span></span>](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="91eb3-132">**\_ЖЕТДЕФИД DM**</span><span class="sxs-lookup"><span data-stu-id="91eb3-132">**DM\_GETDEFID**</span></span>](dm-getdefid.md)
</dt> <dt>

[<span data-ttu-id="91eb3-133">**WM \_ жетдлгкоде**</span><span class="sxs-lookup"><span data-stu-id="91eb3-133">**WM\_GETDLGCODE**</span></span>](wm-getdlgcode.md)
</dt> <dt>

<span data-ttu-id="91eb3-134">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="91eb3-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="91eb3-135">Диалоговые окна</span><span class="sxs-lookup"><span data-stu-id="91eb3-135">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="91eb3-136">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="91eb3-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="91eb3-137">**BM \_ SETSTYLE**</span><span class="sxs-lookup"><span data-stu-id="91eb3-137">**BM\_SETSTYLE**</span></span>](../controls/bm-setstyle.md)
</dt> <dt>

[<span data-ttu-id="91eb3-138">**EM \_ сетлимиттекст**</span><span class="sxs-lookup"><span data-stu-id="91eb3-138">**EM\_SETLIMITTEXT**</span></span>](../controls/em-setlimittext.md)
</dt> </dl>

 

