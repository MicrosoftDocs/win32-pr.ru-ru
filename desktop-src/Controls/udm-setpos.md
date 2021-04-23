---
title: Сообщение UDM_SETPOS (Коммктрл. h)
description: Задает текущую точку для элемента управления "вверх/вниз" с 16-разрядной точностью.
ms.assetid: e7c8b55f-3a4f-47e7-8c7d-e47509f27f1d
keywords:
- Элементы управления Windows для UDM_SETPOS сообщений
topic_type:
- apiref
api_name:
- UDM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b409f9e7468e3add89248b61b7b563ac592f0dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136619"
---
# <a name="udm_setpos-message"></a><span data-ttu-id="8c5bc-104">\_Сообщение СЕТПОС UDM</span><span class="sxs-lookup"><span data-stu-id="8c5bc-104">UDM\_SETPOS message</span></span>

<span data-ttu-id="8c5bc-105">Задает текущую точку для элемента управления "вверх/вниз" с 16-разрядной точностью.</span><span class="sxs-lookup"><span data-stu-id="8c5bc-105">Sets the current position for an up-down control with 16-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c5bc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c5bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c5bc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c5bc-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8c5bc-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8c5bc-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8c5bc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c5bc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c5bc-110">Новое расположение элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="8c5bc-110">New position for the up-down control.</span></span> <span data-ttu-id="8c5bc-111">Если параметр находится за пределами указанного диапазона элемента управления, для свойства *lParam* будет установлено ближайшее допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="8c5bc-111">If the parameter is outside the control's specified range, *lParam* will be set to the nearest valid value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c5bc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c5bc-112">Return value</span></span>

<span data-ttu-id="8c5bc-113">Возвращаемое значение является предыдущей позицией.</span><span class="sxs-lookup"><span data-stu-id="8c5bc-113">The return value is the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c5bc-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c5bc-114">Remarks</span></span>

<span data-ttu-id="8c5bc-115">Это сообщение поддерживает только 16-разрядные позиции.</span><span class="sxs-lookup"><span data-stu-id="8c5bc-115">This message only supports 16-bit positions.</span></span> <span data-ttu-id="8c5bc-116">Если 32-разрядные значения включены для элемента управления "вверх/вниз" [**с \_ SETRANGE32 UDM**](udm-setrange32.md), [**Используйте \_ SETPOS32 UDM**](udm-setpos32.md).</span><span class="sxs-lookup"><span data-stu-id="8c5bc-116">If 32-bit values have been enabled for an up-down control with [**UDM\_SETRANGE32**](udm-setrange32.md), use [**UDM\_SETPOS32**](udm-setpos32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c5bc-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8c5bc-117">Requirements</span></span>



| <span data-ttu-id="8c5bc-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8c5bc-118">Requirement</span></span> | <span data-ttu-id="8c5bc-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8c5bc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c5bc-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c5bc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8c5bc-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c5bc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c5bc-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c5bc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8c5bc-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8c5bc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c5bc-124">Header</span><span class="sxs-lookup"><span data-stu-id="8c5bc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c5bc-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c5bc-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c5bc-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c5bc-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="8c5bc-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="8c5bc-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8c5bc-128">**многомерный \_ диапазон UDM**</span><span class="sxs-lookup"><span data-stu-id="8c5bc-128">**UDM\_GETRANGE**</span></span>](udm-getrange.md)
</dt> <dt>

[<span data-ttu-id="8c5bc-129">**\_ЖЕТПОС UDM**</span><span class="sxs-lookup"><span data-stu-id="8c5bc-129">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> </dl>

 

 





