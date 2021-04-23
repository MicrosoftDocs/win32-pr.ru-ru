---
title: Код уведомления LVN_ITEMACTIVATE (Коммктрл. h)
description: Отправляется элементом управления "представление списка", когда пользователь активирует элемент. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 475c8e6a-8e2e-4182-8ccc-a4bc6fc891a8
keywords:
- LVN_ITEMACTIVATE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_ITEMACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9f139559b03fd82ac655381972803a288f00db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137890"
---
# <a name="lvn_itemactivate-notification-code"></a><span data-ttu-id="1b9b9-105">\_Код уведомления ЛВН итемактивате</span><span class="sxs-lookup"><span data-stu-id="1b9b9-105">LVN\_ITEMACTIVATE notification code</span></span>

<span data-ttu-id="1b9b9-106">Отправляется элементом управления "представление списка", когда пользователь активирует элемент.</span><span class="sxs-lookup"><span data-stu-id="1b9b9-106">Sent by a list-view control when the user activates an item.</span></span> <span data-ttu-id="1b9b9-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1b9b9-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMACTIVATE

#if (_WIN32_IE >= 0x0400)
    lpnmia = (LPNMITEMACTIVATE)lParam;
#else
    lpnm = (LPNMHDR)lParam;
#endif
```



## <a name="parameters"></a><span data-ttu-id="1b9b9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b9b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b9b9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b9b9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b9b9-110">[Версия 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="1b9b9-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="1b9b9-111">Указатель на структуру [**нмитемактивате**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) , содержащую сведения об этом коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="1b9b9-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains information about this notification code.</span></span>

<span data-ttu-id="1b9b9-112">[Версия 4,70](common-control-versions.md) и более ранние версии.</span><span class="sxs-lookup"><span data-stu-id="1b9b9-112">[Version 4.70](common-control-versions.md) and earlier.</span></span> <span data-ttu-id="1b9b9-113">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую сведения об этом коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="1b9b9-113">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b9b9-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b9b9-114">Return value</span></span>

<span data-ttu-id="1b9b9-115">Приложение, получающее этот код уведомления, должно возвращать ноль.</span><span class="sxs-lookup"><span data-stu-id="1b9b9-115">The application receiving this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b9b9-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b9b9-116">Remarks</span></span>

<span data-ttu-id="1b9b9-117">Чтобы получить активируемые элементы, принимающее приложение должно использовать сообщение [**LVM \_ жетселектедкаунт**](lvm-getselectedcount.md) , чтобы получить количество выбранных элементов, а затем отправить сообщение [**LVM \_ жетнекститем**](lvm-getnextitem.md) с **лвни \_ Selected** , пока не будут получены все элементы.</span><span class="sxs-lookup"><span data-stu-id="1b9b9-117">To obtain the items being activated, the receiving application should use the [**LVM\_GETSELECTEDCOUNT**](lvm-getselectedcount.md) message to retrieve the number of items that are selected and then send the [**LVM\_GETNEXTITEM**](lvm-getnextitem.md) message with **LVNI\_SELECTED** until all of the items have been retrieved.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b9b9-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1b9b9-118">Requirements</span></span>



| <span data-ttu-id="1b9b9-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1b9b9-119">Requirement</span></span> | <span data-ttu-id="1b9b9-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1b9b9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b9b9-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b9b9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1b9b9-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b9b9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b9b9-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b9b9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1b9b9-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1b9b9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b9b9-125">Header</span><span class="sxs-lookup"><span data-stu-id="1b9b9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b9b9-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b9b9-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





