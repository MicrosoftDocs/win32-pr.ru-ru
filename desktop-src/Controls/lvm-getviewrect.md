---
title: Сообщение LVM_GETVIEWRECT (Коммктрл. h)
description: Извлекает ограничивающий прямоугольник всех элементов в элементе управления "представление списка". Представление списка должно быть в виде значка или маленького значка. Это сообщение можно отправить явно или с помощью \_ макроса Жетвиеврект ListView.
ms.assetid: 69b96f86-8b7e-42c1-ad73-f9b2732ab9f9
keywords:
- Элементы управления Windows для LVM_GETVIEWRECT сообщений
topic_type:
- apiref
api_name:
- LVM_GETVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d4c4fdf0e8466d3fb0b2ad164241c3f6a541570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071902"
---
# <a name="lvm_getviewrect-message"></a><span data-ttu-id="529f9-106">\_Сообщение LVM жетвиеврект</span><span class="sxs-lookup"><span data-stu-id="529f9-106">LVM\_GETVIEWRECT message</span></span>

<span data-ttu-id="529f9-107">Извлекает ограничивающий прямоугольник всех элементов в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="529f9-107">Retrieves the bounding rectangle of all items in the list-view control.</span></span> <span data-ttu-id="529f9-108">Представление списка должно быть в виде значка или маленького значка.</span><span class="sxs-lookup"><span data-stu-id="529f9-108">The list view must be in icon or small icon view.</span></span> <span data-ttu-id="529f9-109">Это сообщение можно отправить явно или с помощью макроса [**\_ жетвиеврект ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect) .</span><span class="sxs-lookup"><span data-stu-id="529f9-109">You can send this message explicitly or by using the [**ListView\_GetViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="529f9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="529f9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="529f9-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="529f9-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="529f9-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="529f9-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="529f9-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="529f9-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="529f9-114">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая получает ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="529f9-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span> <span data-ttu-id="529f9-115">Все координаты задаются относительно видимой области элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="529f9-115">All coordinates are relative to the visible area of the list-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="529f9-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="529f9-116">Return value</span></span>

<span data-ttu-id="529f9-117">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="529f9-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="529f9-118">Требования</span><span class="sxs-lookup"><span data-stu-id="529f9-118">Requirements</span></span>



| <span data-ttu-id="529f9-119">Требование</span><span class="sxs-lookup"><span data-stu-id="529f9-119">Requirement</span></span> | <span data-ttu-id="529f9-120">Значение</span><span class="sxs-lookup"><span data-stu-id="529f9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="529f9-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="529f9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="529f9-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="529f9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="529f9-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="529f9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="529f9-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="529f9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="529f9-125">Header</span><span class="sxs-lookup"><span data-stu-id="529f9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="529f9-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="529f9-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

