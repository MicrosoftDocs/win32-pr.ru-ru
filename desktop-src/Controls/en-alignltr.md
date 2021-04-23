---
title: Код уведомления EN_ALIGNLTR (RichEdit. h)
description: Сообщает родительскому окну элемента управления Rich Edit, что направление абзаца изменилось на слева направо. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ командного сообщения WM.
ms.assetid: 754ac2b5-bcec-487b-a1ab-b653f673830a
keywords:
- EN_ALIGNLTR кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_ALIGNLTR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55c20a9ae4efb3ba5758ed0740b20b8b57f3877
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071462"
---
# <a name="en_alignltr-notification-code"></a><span data-ttu-id="d3010-105">\_Код уведомления EN алигнлтр</span><span class="sxs-lookup"><span data-stu-id="d3010-105">EN\_ALIGNLTR notification code</span></span>

<span data-ttu-id="d3010-106">Сообщает родительскому окну элемента управления Rich Edit, что направление абзаца изменилось на слева направо.</span><span class="sxs-lookup"><span data-stu-id="d3010-106">Notifies a rich edit control's parent window that the paragraph direction has changed to left-to-right.</span></span> <span data-ttu-id="d3010-107">Форматированный элемент управления "поле ввода" отправляет этот код уведомления в [**виде \_ командного сообщения WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="d3010-107">A rich edit control sends this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ALIGNLTR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d3010-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3010-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3010-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3010-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3010-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d3010-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the rich edit control.</span></span> <span data-ttu-id="d3010-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="d3010-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d3010-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3010-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3010-113">Обработчик для элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d3010-113">Handle to the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3010-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3010-114">Return value</span></span>

<span data-ttu-id="d3010-115">Этот код уведомления не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d3010-115">This notification code does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3010-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d3010-116">Requirements</span></span>



| <span data-ttu-id="d3010-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d3010-117">Requirement</span></span> | <span data-ttu-id="d3010-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d3010-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3010-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3010-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d3010-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3010-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d3010-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3010-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d3010-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d3010-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d3010-123">Header</span><span class="sxs-lookup"><span data-stu-id="d3010-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3010-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3010-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3010-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3010-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="d3010-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="d3010-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d3010-127">**EN \_ алигнртл**</span><span class="sxs-lookup"><span data-stu-id="d3010-127">**EN\_ALIGNRTL**</span></span>](en-alignrtl.md)
</dt> <dt>

<span data-ttu-id="d3010-128">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="d3010-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d3010-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3010-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d3010-130">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3010-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d3010-131">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="d3010-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

