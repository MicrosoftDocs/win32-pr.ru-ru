---
title: Код уведомления TVN_SINGLEEXPAND (Коммктрл. h)
description: Посылается элементом управления "дерево" с помощью стиля "ТЕЛЕВИЗОРы сингликспанд", \_ когда пользователь открывает или закрывает элемент дерева одним щелчком мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: ae738237-172a-400b-b9fe-33832224e299
keywords:
- TVN_SINGLEEXPAND кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TVN_SINGLEEXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c0e8acfee1f024e4ee7f88d9f745e4029ec82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489636"
---
# <a name="tvn_singleexpand-notification-code"></a><span data-ttu-id="ea6b8-105">\_Код уведомления ТВН сингликспанд</span><span class="sxs-lookup"><span data-stu-id="ea6b8-105">TVN\_SINGLEEXPAND notification code</span></span>

<span data-ttu-id="ea6b8-106">Посылается элементом управления "дерево" с помощью стиля " [**телевизоры \_ сингликспанд**](tree-view-control-window-styles.md) ", когда пользователь открывает или закрывает элемент дерева одним щелчком мыши.</span><span class="sxs-lookup"><span data-stu-id="ea6b8-106">Sent by a tree-view control with the [**TVS\_SINGLEEXPAND**](tree-view-control-window-styles.md) style when the user opens or closes a tree item using a single click of the mouse.</span></span> <span data-ttu-id="ea6b8-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ea6b8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SINGLEEXPAND

    lpnmtv = (LPNMTREEVIEW)lParam;
```



## <a name="parameters"></a><span data-ttu-id="ea6b8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea6b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea6b8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea6b8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea6b8-110">Указатель на структуру [**нмтривиев**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) , содержащую сведения об этом коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="ea6b8-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea6b8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea6b8-111">Return value</span></span>

<span data-ttu-id="ea6b8-112">Возвращает ТВНРЕТ \_ по умолчанию, чтобы разрешить выполнение поведения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ea6b8-112">Return TVNRET\_DEFAULT to allow the default behavior to occur.</span></span> <span data-ttu-id="ea6b8-113">Чтобы изменить поведение по умолчанию, возвратите:</span><span class="sxs-lookup"><span data-stu-id="ea6b8-113">To modify the default behavior, return:</span></span>



| <span data-ttu-id="ea6b8-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ea6b8-114">Return code</span></span>                                                                                    | <span data-ttu-id="ea6b8-115">Описание</span><span class="sxs-lookup"><span data-stu-id="ea6b8-115">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="ea6b8-116"><dt>**ТВНРЕТ \_ скиполд**</dt></span><span class="sxs-lookup"><span data-stu-id="ea6b8-116"><dt>**TVNRET\_SKIPOLD**</dt></span></span> </dl> | <span data-ttu-id="ea6b8-117">Пропустить обработку по умолчанию для элемента, для которого выполняется отмена выбора.</span><span class="sxs-lookup"><span data-stu-id="ea6b8-117">Skip default processing of the item being unselected.</span></span><br/> |
| <dl> <span data-ttu-id="ea6b8-118"><dt>**ТВНРЕТ \_ скипнев**</dt></span><span class="sxs-lookup"><span data-stu-id="ea6b8-118"><dt>**TVNRET\_SKIPNEW**</dt></span></span> </dl> | <span data-ttu-id="ea6b8-119">Пропустить обработку выбранного элемента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ea6b8-119">Skip default processing of the item being selected.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="ea6b8-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea6b8-120">Remarks</span></span>

<span data-ttu-id="ea6b8-121">Чтобы пропустить обработку выбранных и невыбранных элементов по умолчанию, возвратите ТВНРЕТ \_ скиполд и твнрет \_ скипнев, объединив их с логическим или.</span><span class="sxs-lookup"><span data-stu-id="ea6b8-121">To skip default processing of selected and unselected items, return both TVNRET\_SKIPOLD and TVNRET\_SKIPNEW by combining them with a logical OR.</span></span>

<span data-ttu-id="ea6b8-122">Этот код уведомления отправляется только элементами управления "дерево", которые имеют [**стиль \_ Сингликспанд "телевизоры**](tree-view-control-window-styles.md) ".</span><span class="sxs-lookup"><span data-stu-id="ea6b8-122">This notification code is only sent by tree-view controls that have the [**TVS\_SINGLEEXPAND**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea6b8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ea6b8-123">Requirements</span></span>



| <span data-ttu-id="ea6b8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ea6b8-124">Requirement</span></span> | <span data-ttu-id="ea6b8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ea6b8-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea6b8-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea6b8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ea6b8-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea6b8-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea6b8-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea6b8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ea6b8-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ea6b8-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea6b8-130">Header</span><span class="sxs-lookup"><span data-stu-id="ea6b8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea6b8-131"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea6b8-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





