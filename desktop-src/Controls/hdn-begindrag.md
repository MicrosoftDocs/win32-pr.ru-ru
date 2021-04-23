---
title: Код уведомления HDN_BEGINDRAG (Коммктрл. h)
description: Посылается элементом управления "заголовок", когда в одном из его элементов началась операция перетаскивания. Этот код уведомления отправляется только элементам управления "заголовок", для которых задан \_ стиль HDS DRAGDROP. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 3dfb7a7c-d783-48e0-ba92-8144104f163a
keywords:
- HDN_BEGINDRAG кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- HDN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6b4af8e662a8a9891e9a81535de987337567f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071556"
---
# <a name="hdn_begindrag-notification-code"></a><span data-ttu-id="a6a67-106">\_Код уведомления ХДН бегиндраг</span><span class="sxs-lookup"><span data-stu-id="a6a67-106">HDN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="a6a67-107">Посылается элементом управления "заголовок", когда в одном из его элементов началась операция перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="a6a67-107">Sent by a header control when a drag operation has begun on one of its items.</span></span> <span data-ttu-id="a6a67-108">Этот код уведомления отправляется только элементам управления "заголовок", для которых задан стиль [**HDS \_ DRAGDROP**](header-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a6a67-108">This notification code is sent only by header controls that are set to the [**HDS\_DRAGDROP**](header-control-styles.md) style.</span></span> <span data-ttu-id="a6a67-109">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a6a67-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_BEGINDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a6a67-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6a67-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6a67-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6a67-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6a67-112">Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , содержащую сведения о перемещенном элементе заголовка.</span><span class="sxs-lookup"><span data-stu-id="a6a67-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure containing information about the header item that is being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6a67-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a6a67-113">Return value</span></span>

<span data-ttu-id="a6a67-114">Чтобы разрешить элементу управления "заголовок" автоматически управлять операциями перетаскивания, возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a6a67-114">To allow the header control to automatically manage drag-and-drop operations, return **FALSE**.</span></span> <span data-ttu-id="a6a67-115">Если владелец элемента управления выполняет изменение порядка перетаскивания вручную, возвращается **значение true**.</span><span class="sxs-lookup"><span data-stu-id="a6a67-115">If the owner of the control is manually performing drag-and-drop reordering, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6a67-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6a67-116">Remarks</span></span>

<span data-ttu-id="a6a67-117">По умолчанию элемент управления "заголовок" автоматически управляет изменением порядка перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="a6a67-117">A header control defaults to automatically managing drag-and-drop reordering.</span></span> <span data-ttu-id="a6a67-118">Возврат значения **true** для указания внешнего (ручного) управления перетаскиванием позволяет владельцу элемента управления предоставлять пользовательские службы в рамках процесса перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="a6a67-118">Returning **TRUE** to indicate external (manual) drag-and-drop management allows the owner of the control to provide custom services as part of the drag-and-drop process.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6a67-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a6a67-119">Requirements</span></span>



| <span data-ttu-id="a6a67-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a6a67-120">Requirement</span></span> | <span data-ttu-id="a6a67-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a6a67-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a67-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a6a67-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a6a67-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a6a67-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6a67-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a6a67-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a6a67-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a6a67-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6a67-126">Header</span><span class="sxs-lookup"><span data-stu-id="a6a67-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6a67-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6a67-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





