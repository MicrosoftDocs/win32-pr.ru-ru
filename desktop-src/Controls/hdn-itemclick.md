---
title: Код уведомления HDN_ITEMCLICK (Коммктрл. h)
description: Сообщает родительскому окну элемента управления заголовка, что пользователь щелкнул элемент управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 25ed0070-5891-4f36-9ae0-fc04e064401f
keywords:
- HDN_ITEMCLICK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- HDN_ITEMCLICK
- HDN_ITEMCLICKA
- HDN_ITEMCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca49cd4fd77425f202c5d8ee06cb0b3d7712e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892474"
---
# <a name="hdn_itemclick-notification-code"></a><span data-ttu-id="59ecc-105">\_Код уведомления ХДН итемкликк</span><span class="sxs-lookup"><span data-stu-id="59ecc-105">HDN\_ITEMCLICK notification code</span></span>

<span data-ttu-id="59ecc-106">Сообщает родительскому окну элемента управления заголовка, что пользователь щелкнул элемент управления.</span><span class="sxs-lookup"><span data-stu-id="59ecc-106">Notifies a header control's parent window that the user clicked the control.</span></span> <span data-ttu-id="59ecc-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="59ecc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="59ecc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="59ecc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59ecc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59ecc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59ecc-110">Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , которая идентифицирует элемент управления "заголовок" и задает индекс элемента заголовка, который был нажат, и кнопку мыши, которая использовалась для щелчка элемента.</span><span class="sxs-lookup"><span data-stu-id="59ecc-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that identifies the header control and specifies the index of the header item that was clicked and the mouse button used to click the item.</span></span> <span data-ttu-id="59ecc-111">Элемент **питем** имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="59ecc-111">The **pItem** member is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59ecc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59ecc-112">Return value</span></span>

<span data-ttu-id="59ecc-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="59ecc-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59ecc-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59ecc-114">Remarks</span></span>

<span data-ttu-id="59ecc-115">Элемент управления "заголовок" отправляет этот код уведомления после того, как пользователь отпускает левую кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="59ecc-115">A header control sends this notification code after the user releases the left mouse button.</span></span>

## <a name="requirements"></a><span data-ttu-id="59ecc-116">Требования</span><span class="sxs-lookup"><span data-stu-id="59ecc-116">Requirements</span></span>



| <span data-ttu-id="59ecc-117">Требование</span><span class="sxs-lookup"><span data-stu-id="59ecc-117">Requirement</span></span> | <span data-ttu-id="59ecc-118">Значение</span><span class="sxs-lookup"><span data-stu-id="59ecc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59ecc-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59ecc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="59ecc-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59ecc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59ecc-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59ecc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="59ecc-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="59ecc-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59ecc-123">Header</span><span class="sxs-lookup"><span data-stu-id="59ecc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="59ecc-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="59ecc-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="59ecc-125">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="59ecc-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="59ecc-126">**ХДН \_ ИТЕМКЛИККВ** (Юникод) и **ХДН \_ итемкликка** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="59ecc-126">**HDN\_ITEMCLICKW** (Unicode) and **HDN\_ITEMCLICKA** (ANSI)</span></span><br/>               |



 

 





