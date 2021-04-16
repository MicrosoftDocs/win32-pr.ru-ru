---
title: Код уведомления EN_ALIGNRTL (RichEdit. h)
description: Сообщает родительскому окну элемента управления Rich Edit, что направление абзаца изменилось на справа налево. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ командного сообщения WM.
ms.assetid: 2db5fd49-9ecd-49d7-8199-1706648255ca
keywords:
- EN_ALIGNRTL кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_ALIGNRTL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac2adaa629d00ef940f02f1ed69eb778cdc7813
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489987"
---
# <a name="en_alignrtl-notification-code"></a><span data-ttu-id="c385f-105">\_Код уведомления EN алигнртл</span><span class="sxs-lookup"><span data-stu-id="c385f-105">EN\_ALIGNRTL notification code</span></span>

<span data-ttu-id="c385f-106">Сообщает родительскому окну элемента управления Rich Edit, что направление абзаца изменилось на справа налево.</span><span class="sxs-lookup"><span data-stu-id="c385f-106">Notifies a rich edit control's parent window that the paragraph direction changed to right-to-left.</span></span> <span data-ttu-id="c385f-107">Форматированный элемент управления "поле ввода" отправляет этот код уведомления в [**виде \_ командного сообщения WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="c385f-107">A rich edit control sends this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ALIGNRTL

    WPARAM wParam
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="c385f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c385f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c385f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c385f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c385f-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c385f-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the rich edit control.</span></span> <span data-ttu-id="c385f-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="c385f-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="c385f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c385f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c385f-113">Обработчик для элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c385f-113">Handle to the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c385f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c385f-114">Return value</span></span>

<span data-ttu-id="c385f-115">Этот код уведомления не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c385f-115">This notification code does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c385f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c385f-116">Requirements</span></span>



| <span data-ttu-id="c385f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c385f-117">Requirement</span></span> | <span data-ttu-id="c385f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c385f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c385f-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c385f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c385f-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c385f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c385f-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c385f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c385f-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c385f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c385f-123">Header</span><span class="sxs-lookup"><span data-stu-id="c385f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c385f-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c385f-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c385f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c385f-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="c385f-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="c385f-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c385f-127">**EN \_ алигнлтр**</span><span class="sxs-lookup"><span data-stu-id="c385f-127">**EN\_ALIGNLTR**</span></span>](en-alignltr.md)
</dt> <dt>

<span data-ttu-id="c385f-128">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="c385f-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="c385f-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c385f-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="c385f-130">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c385f-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c385f-131">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="c385f-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

