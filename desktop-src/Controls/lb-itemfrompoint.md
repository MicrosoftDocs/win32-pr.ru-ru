---
title: Сообщение LB_ITEMFROMPOINT (Winuser. h)
description: Возвращает отсчитываемый от нуля индекс элемента, ближайшего к заданной точке в списке.
ms.assetid: 5739eccb-e708-4ddb-ac97-d3e6c6120842
keywords:
- Элементы управления Windows для LB_ITEMFROMPOINT сообщений
topic_type:
- apiref
api_name:
- LB_ITEMFROMPOINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c4f06b9de8e6580c81c7faf7ddb8c287a148b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803418"
---
# <a name="lb_itemfrompoint-message"></a><span data-ttu-id="fcacb-104">Сообщение итемфромпоинт балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="fcacb-104">LB\_ITEMFROMPOINT message</span></span>

<span data-ttu-id="fcacb-105">Возвращает отсчитываемый от нуля индекс элемента, ближайшего к заданной точке в списке.</span><span class="sxs-lookup"><span data-stu-id="fcacb-105">Gets the zero-based index of the item nearest the specified point in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="fcacb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fcacb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcacb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fcacb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcacb-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="fcacb-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fcacb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fcacb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcacb-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) задает координату x точки относительно левого верхнего угла клиентской области окна списка.</span><span class="sxs-lookup"><span data-stu-id="fcacb-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the x-coordinate of a point, relative to the upper-left corner of the client area of the list box.</span></span>

<span data-ttu-id="fcacb-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) Указывает координату y точки относительно левого верхнего угла клиентской области окна списка.</span><span class="sxs-lookup"><span data-stu-id="fcacb-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the y-coordinate of a point, relative to the upper-left corner of the client area of the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcacb-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fcacb-112">Return value</span></span>

<span data-ttu-id="fcacb-113">Возвращаемое значение содержит индекс ближайшего элемента в [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fcacb-113">The return value contains the index of the nearest item in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span></span> <span data-ttu-id="fcacb-114">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) равен нулю, если указанная точка находится в клиентской области списка или если она находится за пределами клиентской области.</span><span class="sxs-lookup"><span data-stu-id="fcacb-114">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is zero if the specified point is in the client area of the list box, or one if it is outside the client area.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcacb-115">Требования</span><span class="sxs-lookup"><span data-stu-id="fcacb-115">Requirements</span></span>



| <span data-ttu-id="fcacb-116">Требование</span><span class="sxs-lookup"><span data-stu-id="fcacb-116">Requirement</span></span> | <span data-ttu-id="fcacb-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fcacb-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcacb-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fcacb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fcacb-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fcacb-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fcacb-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fcacb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fcacb-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fcacb-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fcacb-122">Header</span><span class="sxs-lookup"><span data-stu-id="fcacb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcacb-123"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fcacb-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcacb-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fcacb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcacb-125">**макелпарам**</span><span class="sxs-lookup"><span data-stu-id="fcacb-125">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

