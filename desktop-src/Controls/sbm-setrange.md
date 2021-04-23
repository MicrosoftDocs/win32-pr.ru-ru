---
title: Сообщение SBM_SETRANGE (Winuser. h)
description: Сообщение СБМ \_ SETRANGE отправляется для установки минимального и максимального значений позиций для элемента управления "полоса прокрутки".
ms.assetid: 9cf84354-3944-4c10-9b59-39427b840868
keywords:
- Элементы управления Windows для SBM_SETRANGE сообщений
topic_type:
- apiref
api_name:
- SBM_SETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7a720531ae58fdb0712b8f23fd1aef88b3e4caa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892545"
---
# <a name="sbm_setrange-message"></a><span data-ttu-id="b6740-104">\_Сообщение SETRANGE СБМ</span><span class="sxs-lookup"><span data-stu-id="b6740-104">SBM\_SETRANGE message</span></span>

<span data-ttu-id="b6740-105">Сообщение **СБМ \_ SETRANGE** отправляется для установки минимального и максимального значений позиций для элемента управления "полоса прокрутки".</span><span class="sxs-lookup"><span data-stu-id="b6740-105">The **SBM\_SETRANGE** message is sent to set the minimum and maximum position values for the scroll bar control.</span></span>

<span data-ttu-id="b6740-106">Приложения не должны отсылать это сообщение напрямую.</span><span class="sxs-lookup"><span data-stu-id="b6740-106">Applications should not send this message directly.</span></span> <span data-ttu-id="b6740-107">Вместо этого они должны использовать функцию [**сетскроллранже**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) .</span><span class="sxs-lookup"><span data-stu-id="b6740-107">Instead, they should use the [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) function.</span></span> <span data-ttu-id="b6740-108">Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b6740-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="b6740-109">Приложения, которые реализуют пользовательский элемент управления "полоса прокрутки", должны отвечать на эти сообщения, чтобы функция **сетскроллранже** работала правильно.</span><span class="sxs-lookup"><span data-stu-id="b6740-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollRange** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6740-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6740-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6740-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6740-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6740-112">Задает минимальную прокрутку.</span><span class="sxs-lookup"><span data-stu-id="b6740-112">Specifies the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="b6740-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6740-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6740-114">Задает максимальную точку прокрутки.</span><span class="sxs-lookup"><span data-stu-id="b6740-114">Specifies the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6740-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6740-115">Return value</span></span>

<span data-ttu-id="b6740-116">**ComCtl32.dll версии 5,0**: Если изменяется расположение ползунка, возвращаемое значение является предыдущим положением поля прокрутки; в противном случае он равен нулю.</span><span class="sxs-lookup"><span data-stu-id="b6740-116">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="b6740-117">**ComCtl32.dll версии 6,0**: текущее расположение поля прокрутки, независимо от того, изменился ли он.</span><span class="sxs-lookup"><span data-stu-id="b6740-117">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6740-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6740-118">Remarks</span></span>

<span data-ttu-id="b6740-119">По умолчанию минимальное и максимальное значения позиций равны нулю.</span><span class="sxs-lookup"><span data-stu-id="b6740-119">The default minimum and maximum position values are zero.</span></span> <span data-ttu-id="b6740-120">Разница между значениями, заданными параметрами *wParam* и *lParam* , не должна превышать макслонг.</span><span class="sxs-lookup"><span data-stu-id="b6740-120">The difference between the values specified by the *wParam* and *lParam* parameters must not be greater than MAXLONG.</span></span>

<span data-ttu-id="b6740-121">Если минимальное и максимальное значения позиционирования равны, элемент управления "полоса прокрутки" скрыт и, по сути, отключен.</span><span class="sxs-lookup"><span data-stu-id="b6740-121">If the minimum and maximum position values are equal, the scroll bar control is hidden and, in effect, disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6740-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b6740-122">Requirements</span></span>



| <span data-ttu-id="b6740-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b6740-123">Requirement</span></span> | <span data-ttu-id="b6740-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b6740-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6740-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6740-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b6740-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6740-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b6740-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6740-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b6740-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b6740-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b6740-129">Header</span><span class="sxs-lookup"><span data-stu-id="b6740-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6740-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6740-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6740-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6740-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="b6740-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="b6740-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b6740-133">**СБМ \_ жетпос**</span><span class="sxs-lookup"><span data-stu-id="b6740-133">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="b6740-134">**СБМ \_**</span><span class="sxs-lookup"><span data-stu-id="b6740-134">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="b6740-135">**СБМ \_ сетпос**</span><span class="sxs-lookup"><span data-stu-id="b6740-135">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="b6740-136">**СБМ \_ сетранжередрав**</span><span class="sxs-lookup"><span data-stu-id="b6740-136">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

