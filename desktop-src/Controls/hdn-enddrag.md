---
title: Код уведомления HDN_ENDDRAG (Коммктрл. h)
description: Посылается элементом управления "заголовок" при завершении операции перетаскивания для одного из ее элементов. Этот код уведомления отправляется в виде \_ сообщения WM notify. Этот код уведомления можно отправить только элементам управления "заголовок", для которых задан \_ стиль HDS DRAGDROP.
ms.assetid: a28df985-73f1-4fc7-a1db-81a86a131c06
keywords:
- HDN_ENDDRAG кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- HDN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eef628dd8ff748829542ace76642e20ad97786f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493341"
---
# <a name="hdn_enddrag-notification-code"></a><span data-ttu-id="4365b-106">\_Код уведомления ХДН енддраг</span><span class="sxs-lookup"><span data-stu-id="4365b-106">HDN\_ENDDRAG notification code</span></span>

<span data-ttu-id="4365b-107">Посылается элементом управления "заголовок" при завершении операции перетаскивания для одного из ее элементов.</span><span class="sxs-lookup"><span data-stu-id="4365b-107">Sent by a header control when a drag operation has ended on one of its items.</span></span> <span data-ttu-id="4365b-108">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4365b-108">This notification code is sent as a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="4365b-109">Этот код уведомления можно отправить только элементам управления "заголовок", для которых задан стиль [**HDS \_ DRAGDROP**](header-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="4365b-109">Only header controls that are set to the [**HDS\_DRAGDROP**](header-control-styles.md) style send this notification code.</span></span>


```C++
HDN_ENDDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="4365b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4365b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4365b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4365b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4365b-112">Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , содержащую сведения о перемещенном элементе заголовка.</span><span class="sxs-lookup"><span data-stu-id="4365b-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure containing information about the header item that was being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4365b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4365b-113">Return value</span></span>

<span data-ttu-id="4365b-114">Чтобы разрешить элементу управления автоматически размещать и упорядочивать элемент, возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="4365b-114">To allow the control to automatically place and reorder the item, return **FALSE**.</span></span> <span data-ttu-id="4365b-115">Чтобы предотвратить размещение элемента, возвратите **значение true**.</span><span class="sxs-lookup"><span data-stu-id="4365b-115">To prevent the item from being placed, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4365b-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4365b-116">Remarks</span></span>

<span data-ttu-id="4365b-117">Если владелец выполняет внешнее (ручное) Управление перетаскиванием, оно должно возвращать **значение false**.</span><span class="sxs-lookup"><span data-stu-id="4365b-117">If the owner is performing external (manual) drag-and-drop management, it must return **FALSE**.</span></span> <span data-ttu-id="4365b-118">Затем владелец должен вручную изменить порядок элементов заголовка, отправив [**HDM \_ Сетитем**](hdm-setitem.md) или [**HDM \_ сетордераррай**](hdm-setorderarray.md).</span><span class="sxs-lookup"><span data-stu-id="4365b-118">The owner then must reorder header items manually by sending [**HDM\_SETITEM**](hdm-setitem.md) or [**HDM\_SETORDERARRAY**](hdm-setorderarray.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4365b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4365b-119">Requirements</span></span>



| <span data-ttu-id="4365b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4365b-120">Requirement</span></span> | <span data-ttu-id="4365b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4365b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4365b-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4365b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4365b-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4365b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4365b-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4365b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4365b-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4365b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4365b-126">Header</span><span class="sxs-lookup"><span data-stu-id="4365b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4365b-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4365b-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





