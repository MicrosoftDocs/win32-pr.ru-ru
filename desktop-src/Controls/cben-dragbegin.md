---
title: Код уведомления CBEN_DRAGBEGIN (Коммктрл. h)
description: Посылается, когда пользователь начинает перетаскивать изображение элемента, отображаемого в области редактирования элемента управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: bdab2700-a605-48af-aee3-bbf573408e3f
keywords:
- CBEN_DRAGBEGIN кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- CBEN_DRAGBEGIN
- CBEN_DRAGBEGINA
- CBEN_DRAGBEGINW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910e6ac494b49f685a55e77b432e96b4fb22bd29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137283"
---
# <a name="cben_dragbegin-notification-code"></a><span data-ttu-id="58008-105">\_Код уведомления кбен драгбегин</span><span class="sxs-lookup"><span data-stu-id="58008-105">CBEN\_DRAGBEGIN notification code</span></span>

<span data-ttu-id="58008-106">Посылается, когда пользователь начинает перетаскивать изображение элемента, отображаемого в области редактирования элемента управления.</span><span class="sxs-lookup"><span data-stu-id="58008-106">Sent when the user begins dragging the image of the item displayed in the edit portion of the control.</span></span> <span data-ttu-id="58008-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="58008-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_DRAGBEGIN

    lpnmdb = (LPNMCBEDRAGBEGIN) lParam;
```



## <a name="parameters"></a><span data-ttu-id="58008-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="58008-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58008-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58008-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58008-110">Указатель на структуру [**нмкбедрагбегин**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="58008-110">A pointer to a [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58008-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="58008-111">Return value</span></span>

<span data-ttu-id="58008-112">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="58008-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="58008-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58008-113">Remarks</span></span>

<span data-ttu-id="58008-114">Если принимающее приложение реализует функцию перетаскивания из элемента управления, приложение начнет операцию перетаскивания в ответ на этот код уведомления.</span><span class="sxs-lookup"><span data-stu-id="58008-114">If the receiving application implements drag-and-drop functionality from the control, the application will begin the drag-and-drop operation in response to this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="58008-115">Требования</span><span class="sxs-lookup"><span data-stu-id="58008-115">Requirements</span></span>



| <span data-ttu-id="58008-116">Требование</span><span class="sxs-lookup"><span data-stu-id="58008-116">Requirement</span></span> | <span data-ttu-id="58008-117">Значение</span><span class="sxs-lookup"><span data-stu-id="58008-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58008-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58008-118">Minimum supported client</span></span><br/> | <span data-ttu-id="58008-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58008-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="58008-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58008-120">Minimum supported server</span></span><br/> | <span data-ttu-id="58008-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="58008-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="58008-122">Header</span><span class="sxs-lookup"><span data-stu-id="58008-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="58008-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="58008-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="58008-124">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="58008-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="58008-125">**Кбен \_ ДРАГБЕГИНВ** (Юникод) и **кбен \_ драгбегина** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="58008-125">**CBEN\_DRAGBEGINW** (Unicode) and **CBEN\_DRAGBEGINA** (ANSI)</span></span><br/>             |



 

 





