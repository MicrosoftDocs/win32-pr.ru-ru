---
title: Сообщение TVM_GETTEXTCOLOR (Коммктрл. h)
description: Извлекает текущий цвет текста элемента управления. Это сообщение можно отправить явно или с помощью \_ макроса Жеттекстколор TreeView.
ms.assetid: fe1aa2e8-fdf2-48d1-936b-6d6bc8e589f4
keywords:
- Элементы управления Windows для TVM_GETTEXTCOLOR сообщений
topic_type:
- apiref
api_name:
- TVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899fc68847fea937a6f62bff6367eeac5570a5a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071367"
---
# <a name="tvm_gettextcolor-message"></a><span data-ttu-id="3d149-105">\_Сообщение TVM жеттекстколор</span><span class="sxs-lookup"><span data-stu-id="3d149-105">TVM\_GETTEXTCOLOR message</span></span>

<span data-ttu-id="3d149-106">Извлекает текущий цвет текста элемента управления.</span><span class="sxs-lookup"><span data-stu-id="3d149-106">Retrieves the current text color of the control.</span></span> <span data-ttu-id="3d149-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жеттекстколор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) .</span><span class="sxs-lookup"><span data-stu-id="3d149-107">You can send this message explicitly or by using the [**TreeView\_GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3d149-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d149-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d149-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3d149-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3d149-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3d149-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3d149-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d149-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3d149-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3d149-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d149-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d149-113">Return value</span></span>

<span data-ttu-id="3d149-114">Возвращает значение [**COLORREF**](/windows/desktop/gdi/colorref) , представляющее текущий цвет текста.</span><span class="sxs-lookup"><span data-stu-id="3d149-114">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the current text color.</span></span> <span data-ttu-id="3d149-115">Если это значение равно-1, то элемент управления использует системный цвет для цвета текста.</span><span class="sxs-lookup"><span data-stu-id="3d149-115">If this value is -1, the control is using the system color for the text color.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d149-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3d149-116">Requirements</span></span>



| <span data-ttu-id="3d149-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3d149-117">Requirement</span></span> | <span data-ttu-id="3d149-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3d149-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d149-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d149-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3d149-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3d149-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3d149-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d149-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3d149-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3d149-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3d149-123">Header</span><span class="sxs-lookup"><span data-stu-id="3d149-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d149-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d149-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d149-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d149-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d149-126">**TVM \_ сеттекстколор**</span><span class="sxs-lookup"><span data-stu-id="3d149-126">**TVM\_SETTEXTCOLOR**</span></span>](tvm-settextcolor.md)
</dt> </dl>

 

