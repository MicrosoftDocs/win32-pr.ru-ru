---
title: Сообщение TVM_SETBKCOLOR (Коммктрл. h)
description: Задает цвет фона элемента управления. Это сообщение можно отправить явно или с помощью \_ макроса Сетбкколор TreeView.
ms.assetid: 087f5e0b-ac73-4db4-b82e-15c7641b681c
keywords:
- Элементы управления Windows для TVM_SETBKCOLOR сообщений
topic_type:
- apiref
api_name:
- TVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 151aef7aa61e7c66d436d0c90f2481fada017059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892134"
---
# <a name="tvm_setbkcolor-message"></a><span data-ttu-id="755d7-105">\_Сообщение TVM сетбкколор</span><span class="sxs-lookup"><span data-stu-id="755d7-105">TVM\_SETBKCOLOR message</span></span>

<span data-ttu-id="755d7-106">Задает цвет фона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="755d7-106">Sets the background color of the control.</span></span> <span data-ttu-id="755d7-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сетбкколор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="755d7-107">You can send this message explicitly or by using the [**TreeView\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="755d7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="755d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="755d7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="755d7-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="755d7-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="755d7-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="755d7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="755d7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="755d7-112">Значение [**COLORREF**](/windows/desktop/gdi/colorref) , содержащее новый цвет фона.</span><span class="sxs-lookup"><span data-stu-id="755d7-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new background color.</span></span> <span data-ttu-id="755d7-113">Если это значение равно-1, то элемент управления вернется к использованию системного цвета для цвета фона.</span><span class="sxs-lookup"><span data-stu-id="755d7-113">If this value is -1, the control will revert to using the system color for the background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="755d7-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="755d7-114">Return value</span></span>

<span data-ttu-id="755d7-115">Возвращает значение [**COLORREF**](/windows/desktop/gdi/colorref) , представляющее предыдущий цвет фона.</span><span class="sxs-lookup"><span data-stu-id="755d7-115">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous background color.</span></span> <span data-ttu-id="755d7-116">Если это значение равно-1, то элемент управления использовал системный цвет для цвета фона.</span><span class="sxs-lookup"><span data-stu-id="755d7-116">If this value is -1, the control was using the system color for the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="755d7-117">Требования</span><span class="sxs-lookup"><span data-stu-id="755d7-117">Requirements</span></span>



| <span data-ttu-id="755d7-118">Требование</span><span class="sxs-lookup"><span data-stu-id="755d7-118">Requirement</span></span> | <span data-ttu-id="755d7-119">Значение</span><span class="sxs-lookup"><span data-stu-id="755d7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="755d7-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="755d7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="755d7-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="755d7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="755d7-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="755d7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="755d7-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="755d7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="755d7-124">Header</span><span class="sxs-lookup"><span data-stu-id="755d7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="755d7-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="755d7-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="755d7-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="755d7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="755d7-127">**TVM \_ жетбкколор**</span><span class="sxs-lookup"><span data-stu-id="755d7-127">**TVM\_GETBKCOLOR**</span></span>](tvm-getbkcolor.md)
</dt> </dl>

 

