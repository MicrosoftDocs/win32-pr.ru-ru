---
title: Сообщение UDM_SETPOS32 (Коммктрл. h)
description: Задает расположение элемента управления "вверх-вниз" с 32-разрядной точностью.
ms.assetid: a337f2a1-0e3d-4ff4-a224-57b7f25c4bd0
keywords:
- Элементы управления Windows для UDM_SETPOS32 сообщений
topic_type:
- apiref
api_name:
- UDM_SETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0153305bb535a79dbed59e8d42a7c25157c30cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988978"
---
# <a name="udm_setpos32-message"></a><span data-ttu-id="2abb5-104">\_Сообщение SETPOS32 UDM</span><span class="sxs-lookup"><span data-stu-id="2abb5-104">UDM\_SETPOS32 message</span></span>

<span data-ttu-id="2abb5-105">Задает расположение элемента управления "вверх-вниз" с 32-разрядной точностью.</span><span class="sxs-lookup"><span data-stu-id="2abb5-105">Sets the position of an up-down control with 32-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="2abb5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2abb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2abb5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2abb5-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2abb5-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="2abb5-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2abb5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2abb5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2abb5-110">Переменная целочисленного типа, указывающая новое расположение для элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="2abb5-110">Variable of type integer that specifies the new position for the up-down control.</span></span> <span data-ttu-id="2abb5-111">Если параметр находится за пределами указанного диапазона элемента управления, для *lParam* задается ближайшее допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="2abb5-111">If the parameter is outside the control's specified range, *lParam* is set to the nearest valid value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2abb5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2abb5-112">Return value</span></span>

<span data-ttu-id="2abb5-113">Возвращает предыдущее расположение.</span><span class="sxs-lookup"><span data-stu-id="2abb5-113">Returns the previous position.</span></span>

## <a name="requirements"></a><span data-ttu-id="2abb5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="2abb5-114">Requirements</span></span>



| <span data-ttu-id="2abb5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="2abb5-115">Requirement</span></span> | <span data-ttu-id="2abb5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2abb5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2abb5-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2abb5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2abb5-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2abb5-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2abb5-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2abb5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2abb5-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2abb5-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2abb5-121">Header</span><span class="sxs-lookup"><span data-stu-id="2abb5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2abb5-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2abb5-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2abb5-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2abb5-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="2abb5-124">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="2abb5-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2abb5-125">**\_ЖЕТПОС UDM**</span><span class="sxs-lookup"><span data-stu-id="2abb5-125">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> <dt>

[<span data-ttu-id="2abb5-126">**\_СЕТПОС UDM**</span><span class="sxs-lookup"><span data-stu-id="2abb5-126">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="2abb5-127">**\_GETPOS32 UDM**</span><span class="sxs-lookup"><span data-stu-id="2abb5-127">**UDM\_GETPOS32**</span></span>](udm-getpos32.md)
</dt> </dl>

 

 





