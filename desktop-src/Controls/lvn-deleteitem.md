---
title: Код уведомления LVN_DELETEITEM (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что элемент собирается удалиться. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 6e3d1955-ee35-488b-8b96-3d6ebbe5ceb5
keywords:
- LVN_DELETEITEM кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 009d39e78aa93d5c5230e9c1b06b84d2854a0d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137894"
---
# <a name="lvn_deleteitem-notification-code"></a><span data-ttu-id="a7a98-105">\_Код уведомления ЛВН DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="a7a98-105">LVN\_DELETEITEM notification code</span></span>

<span data-ttu-id="a7a98-106">Сообщает родительскому окну элемента управления "представление списка", что элемент собирается удалиться.</span><span class="sxs-lookup"><span data-stu-id="a7a98-106">Notifies a list-view control's parent window that an item is about to be deleted.</span></span> <span data-ttu-id="a7a98-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a7a98-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_DELETEITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a7a98-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7a98-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7a98-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a7a98-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7a98-110">Указатель на структуру [**нмлиствиев**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="a7a98-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="a7a98-111">Член **Член iItem** определяет удаляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="a7a98-111">The **iItem** member identifies the item being deleted.</span></span> <span data-ttu-id="a7a98-112">Если у элемента управления нет стиля **LVS \_ овнердата** , то параметр *lParam* является определяемыми приложением данными, связанными с элементом.</span><span class="sxs-lookup"><span data-stu-id="a7a98-112">If the control does not have the **LVS\_OWNERDATA** style, then the *lParam* is the application-defined data associated with the item.</span></span> <span data-ttu-id="a7a98-113">Все остальные члены этой структуры равны нулю.</span><span class="sxs-lookup"><span data-stu-id="a7a98-113">All other members of this structure are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7a98-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7a98-114">Return value</span></span>

<span data-ttu-id="a7a98-115">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="a7a98-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7a98-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7a98-116">Remarks</span></span>

<span data-ttu-id="a7a98-117">Не добавляйте, удаляйте и не Переупорядочивайте элементы в представлении списка при обработке этого кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="a7a98-117">Do not add, delete, or rearrange items in the list view while processing this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7a98-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a7a98-118">Requirements</span></span>



| <span data-ttu-id="a7a98-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a7a98-119">Requirement</span></span> | <span data-ttu-id="a7a98-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a7a98-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a7a98-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7a98-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a7a98-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a7a98-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a7a98-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7a98-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a7a98-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a7a98-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a7a98-125">Header</span><span class="sxs-lookup"><span data-stu-id="a7a98-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7a98-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7a98-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





