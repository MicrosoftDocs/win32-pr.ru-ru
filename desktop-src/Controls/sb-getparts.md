---
title: Сообщение SB_GETPARTS (Коммктрл. h)
description: Извлекает количество частей в окне состояния. Сообщение также получает координату правого края указанного числа частей.
ms.assetid: 2535f490-4d6b-468a-b13c-096941e61bf4
keywords:
- Элементы управления Windows для SB_GETPARTS сообщений
topic_type:
- apiref
api_name:
- SB_GETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee0f33331c579490cf66a38b9ce6655215ae673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534832"
---
# <a name="sb_getparts-message"></a><span data-ttu-id="2a17a-105">\_Сообщение SB</span><span class="sxs-lookup"><span data-stu-id="2a17a-105">SB\_GETPARTS message</span></span>

<span data-ttu-id="2a17a-106">Извлекает количество частей в окне состояния.</span><span class="sxs-lookup"><span data-stu-id="2a17a-106">Retrieves a count of the parts in a status window.</span></span> <span data-ttu-id="2a17a-107">Сообщение также получает координату правого края указанного числа частей.</span><span class="sxs-lookup"><span data-stu-id="2a17a-107">The message also retrieves the coordinate of the right edge of the specified number of parts.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a17a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a17a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a17a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a17a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a17a-110">Число частей, для которых необходимо получить координаты.</span><span class="sxs-lookup"><span data-stu-id="2a17a-110">Number of parts for which to retrieve coordinates.</span></span> <span data-ttu-id="2a17a-111">Если этот параметр больше числа частей в окне, сообщение получает координаты только для существующих частей.</span><span class="sxs-lookup"><span data-stu-id="2a17a-111">If this parameter is greater than the number of parts in the window, the message retrieves coordinates for existing parts only.</span></span>

</dd> <dt>

<span data-ttu-id="2a17a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a17a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a17a-113">Указатель на целочисленный массив с тем же количеством элементов, что и части, заданные параметром *wParam*.</span><span class="sxs-lookup"><span data-stu-id="2a17a-113">Pointer to an integer array that has the same number of elements as parts specified by *wParam*.</span></span> <span data-ttu-id="2a17a-114">Каждый элемент массива получает клиентскую координату правого края соответствующей части.</span><span class="sxs-lookup"><span data-stu-id="2a17a-114">Each element in the array receives the client coordinate of the right edge of the corresponding part.</span></span> <span data-ttu-id="2a17a-115">Если элемент имеет значение-1, то расположение правого края для этой части расширяется до правого края окна.</span><span class="sxs-lookup"><span data-stu-id="2a17a-115">If an element is set to -1, the position of the right edge for that part extends to the right edge of the window.</span></span> <span data-ttu-id="2a17a-116">Чтобы получить текущее количество частей, присвойте этому параметру значение 0.</span><span class="sxs-lookup"><span data-stu-id="2a17a-116">To retrieve the current number of parts, set this parameter to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a17a-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a17a-117">Return value</span></span>

<span data-ttu-id="2a17a-118">Возвращает количество частей в окне.</span><span class="sxs-lookup"><span data-stu-id="2a17a-118">Returns the number of parts in the window.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a17a-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a17a-119">Remarks</span></span>

<span data-ttu-id="2a17a-120">Это сообщение всегда возвращает количество частей в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="2a17a-120">This message always returns the number of parts in the status bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a17a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2a17a-121">Requirements</span></span>



| <span data-ttu-id="2a17a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2a17a-122">Requirement</span></span> | <span data-ttu-id="2a17a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2a17a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a17a-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a17a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2a17a-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a17a-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2a17a-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a17a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2a17a-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2a17a-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2a17a-128">Header</span><span class="sxs-lookup"><span data-stu-id="2a17a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a17a-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a17a-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





