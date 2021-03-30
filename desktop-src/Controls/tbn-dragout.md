---
title: Код уведомления TBN_DRAGOUT (Коммктрл. h)
description: Посылается элементом управления ToolBar, когда пользователь нажимает кнопку, а затем перемещает курсор за пределы кнопки. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 3566ad60-9744-494f-bb02-d30b41d06351
keywords:
- TBN_DRAGOUT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_DRAGOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54fa61ef183b56b882c6ecdcb9d0d59edbf13e80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071371"
---
# <a name="tbn_dragout-notification-code"></a><span data-ttu-id="49926-105">\_Код уведомления о перетаскивании ТБН</span><span class="sxs-lookup"><span data-stu-id="49926-105">TBN\_DRAGOUT notification code</span></span>

<span data-ttu-id="49926-106">Посылается элементом управления ToolBar, когда пользователь нажимает кнопку, а затем перемещает курсор за пределы кнопки.</span><span class="sxs-lookup"><span data-stu-id="49926-106">Sent by a toolbar control when the user clicks a button and then moves the cursor off the button.</span></span> <span data-ttu-id="49926-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="49926-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DRAGOUT

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="49926-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="49926-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49926-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49926-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49926-110">Указатель на структуру [**нмтулбар**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) , содержащую сведения об этом коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="49926-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about this notification code.</span></span> <span data-ttu-id="49926-111">Для этого кода уведомления допустимы только элементы **HDR** и **Член iItem** этой структуры.</span><span class="sxs-lookup"><span data-stu-id="49926-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span> <span data-ttu-id="49926-112">Элемент **Член iItem** этой структуры содержит идентификатор команды для перетаскивания кнопки.</span><span class="sxs-lookup"><span data-stu-id="49926-112">The **iItem** member of this structure contains the command identifier of the button being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49926-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49926-113">Return value</span></span>

<span data-ttu-id="49926-114">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="49926-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="49926-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49926-115">Remarks</span></span>

<span data-ttu-id="49926-116">Этот код уведомления позволяет приложению реализовать функцию перетаскивания для кнопок панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="49926-116">This notification code allows an application to implement drag-and-drop functionality for toolbar buttons.</span></span> <span data-ttu-id="49926-117">При обработке этого кода уведомления приложение начнет операцию перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="49926-117">When processing this notification code, the application will begin the drag-and-drop operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="49926-118">Требования</span><span class="sxs-lookup"><span data-stu-id="49926-118">Requirements</span></span>



| <span data-ttu-id="49926-119">Требование</span><span class="sxs-lookup"><span data-stu-id="49926-119">Requirement</span></span> | <span data-ttu-id="49926-120">Значение</span><span class="sxs-lookup"><span data-stu-id="49926-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49926-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49926-121">Minimum supported client</span></span><br/> | <span data-ttu-id="49926-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49926-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49926-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49926-123">Minimum supported server</span></span><br/> | <span data-ttu-id="49926-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="49926-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49926-125">Header</span><span class="sxs-lookup"><span data-stu-id="49926-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="49926-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="49926-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





