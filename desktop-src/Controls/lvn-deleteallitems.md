---
title: Код уведомления LVN_DELETEALLITEMS (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что все элементы в элементе управления будут удалены. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: e4a219cf-4af9-4d02-8810-f576ba658177
keywords:
- LVN_DELETEALLITEMS кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583ad6e2372649ab5f63bd208fb97b93b1591c12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989451"
---
# <a name="lvn_deleteallitems-notification-code"></a><span data-ttu-id="270a6-105">\_Код уведомления ЛВН делетеаллитемс</span><span class="sxs-lookup"><span data-stu-id="270a6-105">LVN\_DELETEALLITEMS notification code</span></span>

<span data-ttu-id="270a6-106">Сообщает родительскому окну элемента управления "представление списка", что все элементы в элементе управления будут удалены.</span><span class="sxs-lookup"><span data-stu-id="270a6-106">Notifies a list-view control's parent window that all items in the control are about to be deleted.</span></span> <span data-ttu-id="270a6-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="270a6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_DELETEALLITEMS

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="270a6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="270a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="270a6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="270a6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="270a6-110">Указатель на структуру [**нмлиствиев**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="270a6-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="270a6-111">Элемент **Член iItem** имеет значение-1, а остальные члены равны нулю.</span><span class="sxs-lookup"><span data-stu-id="270a6-111">The **iItem** member is -1, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="270a6-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="270a6-112">Return value</span></span>

<span data-ttu-id="270a6-113">Чтобы отключить последующие коды уведомлений [ЛВН \_ DELETEITEM](lvn-deleteitem.md) , возвратите **значение true**.</span><span class="sxs-lookup"><span data-stu-id="270a6-113">To suppress subsequent [LVN\_DELETEITEM](lvn-deleteitem.md) notification codes, return **TRUE**.</span></span>

<span data-ttu-id="270a6-114">Чтобы получить последующие коды уведомлений [ЛВН \_ DELETEITEM](lvn-deleteitem.md) , возвратите **значение false**.</span><span class="sxs-lookup"><span data-stu-id="270a6-114">To receive subsequent [LVN\_DELETEITEM](lvn-deleteitem.md) notification codes, return **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="270a6-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="270a6-115">Remarks</span></span>

<span data-ttu-id="270a6-116">Элемент управления "представление списка" отправляет код уведомления [**LVM \_ делетеаллитемс**](lvm-deleteallitems.md) при его уничтожении или при получении сообщения **LVM \_ делетеаллитемс** .</span><span class="sxs-lookup"><span data-stu-id="270a6-116">A list-view control sends the [**LVM\_DELETEALLITEMS**](lvm-deleteallitems.md) notification code when it is destroyed or when it receives the **LVM\_DELETEALLITEMS** message.</span></span> <span data-ttu-id="270a6-117">Если **LVM \_ делетеаллитемс** не возвращает **значение true**, элемент управления также будет передавать код уведомления [ЛВН \_ DELETEITEM](lvn-deleteitem.md) по мере удаления каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="270a6-117">If **LVM\_DELETEALLITEMS** does not return **TRUE**, the control will also send an [LVN\_DELETEITEM](lvn-deleteitem.md) notification code as each item is deleted.</span></span>

<span data-ttu-id="270a6-118">Если обработчик сообщений [**LVM \_ делетеаллитемс**](lvm-deleteallitems.md) находится в процедуре диалогового окна, возвратите значение **true** из процедуры диалогового окна и используйте функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) с DWL мсгресулт, \_ чтобы установить возвращаемое значение сообщения.</span><span class="sxs-lookup"><span data-stu-id="270a6-118">If the [**LVM\_DELETEALLITEMS**](lvm-deleteallitems.md) message handler is in a dialog box procedure, return **TRUE** from the dialog box procedure, and use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT to set the message return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="270a6-119">Требования</span><span class="sxs-lookup"><span data-stu-id="270a6-119">Requirements</span></span>



| <span data-ttu-id="270a6-120">Требование</span><span class="sxs-lookup"><span data-stu-id="270a6-120">Requirement</span></span> | <span data-ttu-id="270a6-121">Значение</span><span class="sxs-lookup"><span data-stu-id="270a6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="270a6-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="270a6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="270a6-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="270a6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="270a6-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="270a6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="270a6-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="270a6-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="270a6-126">Header</span><span class="sxs-lookup"><span data-stu-id="270a6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="270a6-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="270a6-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

