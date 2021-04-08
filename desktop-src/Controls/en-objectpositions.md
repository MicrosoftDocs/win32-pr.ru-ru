---
title: Код уведомления EN_OBJECTPOSITIONS (RichEdit. h)
description: Сообщает родительскому окну элемента управления Rich Edit, когда элемент управления считывает объекты. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: 1965185f-8a13-4989-8574-af8b9b30f6b0
keywords:
- EN_OBJECTPOSITIONS кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_OBJECTPOSITIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35681f6734457eb6b6ebcac1bcb67227cbd3b9e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892030"
---
# <a name="en_objectpositions-notification-code"></a><span data-ttu-id="a0b78-105">\_Код уведомления EN обжектпоситионс</span><span class="sxs-lookup"><span data-stu-id="a0b78-105">EN\_OBJECTPOSITIONS notification code</span></span>

<span data-ttu-id="a0b78-106">Сообщает родительскому окну элемента управления Rich Edit, когда элемент управления считывает объекты.</span><span class="sxs-lookup"><span data-stu-id="a0b78-106">Notifies a rich edit control's parent window when the control reads in objects.</span></span> <span data-ttu-id="a0b78-107">Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a0b78-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_OBJECTPOSITIONS

    pOjectPositions = (OBJECTPOSITIONS *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a0b78-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0b78-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0b78-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0b78-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0b78-110">Структура [**обжектпоситионс**](/windows/desktop/api/Richedit/ns-richedit-objectpositions) .</span><span class="sxs-lookup"><span data-stu-id="a0b78-110">An [**OBJECTPOSITIONS**](/windows/desktop/api/Richedit/ns-richedit-objectpositions) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0b78-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0b78-111">Return value</span></span>

<span data-ttu-id="a0b78-112">Возвращает ноль, чтобы продолжить операцию **чтения** .</span><span class="sxs-lookup"><span data-stu-id="a0b78-112">Return zero to continue the **Read** operation.</span></span>

<span data-ttu-id="a0b78-113">Для завершения операции **чтения** возвращается ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="a0b78-113">Return a nonzero value to stop the **Read** operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0b78-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0b78-114">Remarks</span></span>

<span data-ttu-id="a0b78-115">Чтобы получить \_ код уведомления EN обжектпоситионс, укажите флаг [**енм \_ обжектпоситионс**](rich-edit-control-event-mask-flags.md) в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="a0b78-115">To receive an EN\_OBJECTPOSITIONS notification code, specify the [**ENM\_OBJECTPOSITIONS**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0b78-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a0b78-116">Requirements</span></span>



| <span data-ttu-id="a0b78-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a0b78-117">Requirement</span></span> | <span data-ttu-id="a0b78-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a0b78-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0b78-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0b78-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a0b78-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a0b78-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a0b78-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0b78-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a0b78-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a0b78-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0b78-123">Header</span><span class="sxs-lookup"><span data-stu-id="a0b78-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0b78-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0b78-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0b78-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0b78-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="a0b78-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="a0b78-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a0b78-127">**EM \_ SETEVENTMASK**</span><span class="sxs-lookup"><span data-stu-id="a0b78-127">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> <dt>

[<span data-ttu-id="a0b78-128">**обжектпоситионс**</span><span class="sxs-lookup"><span data-stu-id="a0b78-128">**OBJECTPOSITIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-objectpositions)
</dt> <dt>

[<span data-ttu-id="a0b78-129">**\_уведомление WM**</span><span class="sxs-lookup"><span data-stu-id="a0b78-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> <dt>

<span data-ttu-id="a0b78-130">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="a0b78-130">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="a0b78-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0b78-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="a0b78-132">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0b78-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

