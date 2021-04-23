---
title: Код уведомления LVN_SETDISPINFO (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что оно должно обновлять сведения, которые он поддерживает для элемента. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 1ea51d50-4a57-4662-972e-89e916fa9b16
keywords:
- LVN_SETDISPINFO кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_SETDISPINFO
- LVN_SETDISPINFOA
- LVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659623d892f0f5a556f4890703d4e0dd725536b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989007"
---
# <a name="lvn_setdispinfo-notification-code"></a><span data-ttu-id="38d83-105">\_Код уведомления ЛВН сетдиспинфо</span><span class="sxs-lookup"><span data-stu-id="38d83-105">LVN\_SETDISPINFO notification code</span></span>

<span data-ttu-id="38d83-106">Сообщает родительскому окну элемента управления "представление списка", что оно должно обновлять сведения, которые он поддерживает для элемента.</span><span class="sxs-lookup"><span data-stu-id="38d83-106">Notifies a list-view control's parent window that it must update the information it maintains for an item.</span></span> <span data-ttu-id="38d83-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="38d83-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_SETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a><span data-ttu-id="38d83-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="38d83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38d83-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38d83-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38d83-110">Указатель на структуру [**нмлвдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) , которая задает сведения для измененного элемента.</span><span class="sxs-lookup"><span data-stu-id="38d83-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure that specifies information for the changed item.</span></span> <span data-ttu-id="38d83-111">**Элемент** этой структуры является структурой [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) , содержащей сведения об измененном элементе.</span><span class="sxs-lookup"><span data-stu-id="38d83-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that contains information about the item that was changed.</span></span> <span data-ttu-id="38d83-112">Элемент **псзтекст** **элемента** содержит допустимое значение, независимо от того, \_ установлен ли флаг текста лвиф в элементе **Mask** этой структуры.</span><span class="sxs-lookup"><span data-stu-id="38d83-112">The **pszText** member of **item** contains a valid value, regardless of whether the LVIF\_TEXT flag is set in the **mask** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38d83-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38d83-113">Return value</span></span>

<span data-ttu-id="38d83-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="38d83-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="38d83-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38d83-115">Remarks</span></span>

<span data-ttu-id="38d83-116">Получатель уведомлений выполняет приведение *lParam* для получения структуры [**нмлвдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="38d83-116">The notification receiver casts *lParam* to retrieve the [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="38d83-117">Параметр *wParam* содержит код сообщения.</span><span class="sxs-lookup"><span data-stu-id="38d83-117">The *wParam* parameter contains the message code.</span></span>

## <a name="requirements"></a><span data-ttu-id="38d83-118">Требования</span><span class="sxs-lookup"><span data-stu-id="38d83-118">Requirements</span></span>



| <span data-ttu-id="38d83-119">Требование</span><span class="sxs-lookup"><span data-stu-id="38d83-119">Requirement</span></span> | <span data-ttu-id="38d83-120">Значение</span><span class="sxs-lookup"><span data-stu-id="38d83-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38d83-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38d83-121">Minimum supported client</span></span><br/> | <span data-ttu-id="38d83-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="38d83-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="38d83-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38d83-123">Minimum supported server</span></span><br/> | <span data-ttu-id="38d83-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="38d83-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="38d83-125">Header</span><span class="sxs-lookup"><span data-stu-id="38d83-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="38d83-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="38d83-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="38d83-127">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="38d83-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="38d83-128">**ЛВН \_ СЕТДИСПИНФОВ** (Юникод) и **ЛВН \_ сетдиспинфоа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="38d83-128">**LVN\_SETDISPINFOW** (Unicode) and **LVN\_SETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="38d83-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38d83-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38d83-130">ЛВН \_ жетдиспинфо</span><span class="sxs-lookup"><span data-stu-id="38d83-130">LVN\_GETDISPINFO</span></span>](lvn-getdispinfo.md)
</dt> </dl>

 

 





