---
title: Код уведомления UDN_DELTAPOS (Коммктрл. h)
description: Отправляется операционной системой в родительское окно элемента управления "вверх/вниз", когда изменяется расположение элемента управления.
ms.assetid: 66262566-d35a-4b2a-8157-d1e789a21016
keywords:
- UDN_DELTAPOS кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- UDN_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec8f0ec2200d1f18e48c068b581b42868db197b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802411"
---
# <a name="udn_deltapos-notification-code"></a><span data-ttu-id="463eb-104">\_Код уведомления УДН делтапос</span><span class="sxs-lookup"><span data-stu-id="463eb-104">UDN\_DELTAPOS notification code</span></span>

<span data-ttu-id="463eb-105">Отправляется операционной системой в родительское окно элемента управления "вверх/вниз", когда изменяется расположение элемента управления.</span><span class="sxs-lookup"><span data-stu-id="463eb-105">Sent by the operating system to the parent window of an up-down control when the position of the control is about to change.</span></span> <span data-ttu-id="463eb-106">Это происходит, когда пользователь запрашивает изменение значения, нажимая клавишу со стрелкой вверх или вниз элемента управления.</span><span class="sxs-lookup"><span data-stu-id="463eb-106">This happens when the user requests a change in the value by pressing the control's up or down arrow.</span></span> <span data-ttu-id="463eb-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="463eb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
UDN_DELTAPOS 

    lpnmud = (LPNMUPDOWN) lParam;
```



## <a name="parameters"></a><span data-ttu-id="463eb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="463eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="463eb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="463eb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="463eb-110">Указатель на структуру [**нмупдовн**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) , содержащую сведения об изменении позиции.</span><span class="sxs-lookup"><span data-stu-id="463eb-110">Pointer to an [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) structure that contains information about the position change.</span></span> <span data-ttu-id="463eb-111">Элемент **ИПОС** этой структуры содержит текущую точку элемента управления.</span><span class="sxs-lookup"><span data-stu-id="463eb-111">The **iPos** member of this structure contains the current position of the control.</span></span> <span data-ttu-id="463eb-112">Элемент **класса idelta** структуры представляет собой целое число со знаком, содержащее предлагаемое изменение в положении.</span><span class="sxs-lookup"><span data-stu-id="463eb-112">The **iDelta** member of the structure is a signed integer that contains the proposed change in position.</span></span> <span data-ttu-id="463eb-113">Если пользователь щелкнул кнопку Up (вверх), это положительное значение.</span><span class="sxs-lookup"><span data-stu-id="463eb-113">If the user has clicked the up button, this is a positive value.</span></span> <span data-ttu-id="463eb-114">Если пользователь щелкнул кнопку вниз, это отрицательное значение.</span><span class="sxs-lookup"><span data-stu-id="463eb-114">If the user has clicked the down button, this is a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="463eb-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="463eb-115">Return value</span></span>

<span data-ttu-id="463eb-116">Возвращает ненулевое значение, чтобы предотвратить изменение в положении элемента управления, или нуль, чтобы разрешить изменение.</span><span class="sxs-lookup"><span data-stu-id="463eb-116">Return nonzero to prevent the change in the control's position, or zero to allow the change.</span></span>

## <a name="remarks"></a><span data-ttu-id="463eb-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="463eb-117">Remarks</span></span>

<span data-ttu-id="463eb-118">\_Код уведомления УДН делтапос отправляется перед сообщением [**WM \_ VSCROLL**](wm-vscroll.md) или [**WM \_ HSCROLL**](wm-hscroll.md) , которое фактически изменяет расположение элемента управления.</span><span class="sxs-lookup"><span data-stu-id="463eb-118">The UDN\_DELTAPOS notification code is sent before the [**WM\_VSCROLL**](wm-vscroll.md) or [**WM\_HSCROLL**](wm-hscroll.md) message, which actually changes the control's position.</span></span> <span data-ttu-id="463eb-119">Это позволяет проверять, разрешать, изменять или запрещать изменение.</span><span class="sxs-lookup"><span data-stu-id="463eb-119">This lets you examine, allow, modify, or disallow the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="463eb-120">Требования</span><span class="sxs-lookup"><span data-stu-id="463eb-120">Requirements</span></span>



| <span data-ttu-id="463eb-121">Требование</span><span class="sxs-lookup"><span data-stu-id="463eb-121">Requirement</span></span> | <span data-ttu-id="463eb-122">Значение</span><span class="sxs-lookup"><span data-stu-id="463eb-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="463eb-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="463eb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="463eb-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="463eb-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="463eb-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="463eb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="463eb-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="463eb-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="463eb-127">Header</span><span class="sxs-lookup"><span data-stu-id="463eb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="463eb-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="463eb-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="463eb-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="463eb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="463eb-130">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="463eb-130">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

