---
title: Сообщение TVM_GETBKCOLOR (Коммктрл. h)
description: Возвращает текущий цвет фона элемента управления. Это сообщение можно отправить явно или с помощью \_ макроса Жетбкколор TreeView.
ms.assetid: 1b9eea90-54cd-47b9-befa-ec0128a0230f
keywords:
- Элементы управления Windows для TVM_GETBKCOLOR сообщений
topic_type:
- apiref
api_name:
- TVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8077bc9655c088aceefe239ed019cc45874d38ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654638"
---
# <a name="tvm_getbkcolor-message"></a><span data-ttu-id="3247d-105">\_Сообщение TVM жетбкколор</span><span class="sxs-lookup"><span data-stu-id="3247d-105">TVM\_GETBKCOLOR message</span></span>

<span data-ttu-id="3247d-106">Возвращает текущий цвет фона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="3247d-106">Retrieves the current background color of the control.</span></span> <span data-ttu-id="3247d-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жетбкколор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="3247d-107">You can send this message explicitly or by using the [**TreeView\_GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3247d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3247d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3247d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3247d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3247d-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3247d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3247d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3247d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3247d-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3247d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3247d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3247d-113">Return value</span></span>

<span data-ttu-id="3247d-114">Возвращает значение [**COLORREF**](/windows/desktop/gdi/colorref) , представляющее текущий цвет фона.</span><span class="sxs-lookup"><span data-stu-id="3247d-114">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the current background color.</span></span> <span data-ttu-id="3247d-115">Если это значение равно-1, то элемент управления использует системный цвет для цвета фона.</span><span class="sxs-lookup"><span data-stu-id="3247d-115">If this value is -1, the control is using the system color for the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="3247d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3247d-116">Requirements</span></span>



| <span data-ttu-id="3247d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3247d-117">Requirement</span></span> | <span data-ttu-id="3247d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3247d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3247d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3247d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3247d-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3247d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3247d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3247d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3247d-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3247d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3247d-123">Header</span><span class="sxs-lookup"><span data-stu-id="3247d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3247d-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3247d-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3247d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3247d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3247d-126">**TVM \_ сетбкколор**</span><span class="sxs-lookup"><span data-stu-id="3247d-126">**TVM\_SETBKCOLOR**</span></span>](tvm-setbkcolor.md)
</dt> </dl>

 

