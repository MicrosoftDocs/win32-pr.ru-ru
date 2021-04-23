---
title: Сообщение TVM_SETTEXTCOLOR (Коммктрл. h)
description: Задает цвет текста элемента управления. Это сообщение можно отправить явно или с помощью \_ макроса Сеттекстколор TreeView.
ms.assetid: eb57dfd5-3e7b-4cda-a659-be9e03470a44
keywords:
- Элементы управления Windows для TVM_SETTEXTCOLOR сообщений
topic_type:
- apiref
api_name:
- TVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0049c2666faccce7879146c78ddecc70825e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802650"
---
# <a name="tvm_settextcolor-message"></a><span data-ttu-id="79676-105">\_Сообщение TVM сеттекстколор</span><span class="sxs-lookup"><span data-stu-id="79676-105">TVM\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="79676-106">Задает цвет текста элемента управления.</span><span class="sxs-lookup"><span data-stu-id="79676-106">Sets the text color of the control.</span></span> <span data-ttu-id="79676-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сеттекстколор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) .</span><span class="sxs-lookup"><span data-stu-id="79676-107">You can send this message explicitly or by using the [**TreeView\_SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="79676-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="79676-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79676-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="79676-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="79676-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="79676-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="79676-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="79676-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79676-112">Значение [**COLORREF**](/windows/desktop/gdi/colorref) , содержащее новый цвет текста.</span><span class="sxs-lookup"><span data-stu-id="79676-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new text color.</span></span> <span data-ttu-id="79676-113">Если этот аргумент равен-1, элемент управления вернется к использованию системного цвета для цвета текста.</span><span class="sxs-lookup"><span data-stu-id="79676-113">If this argument is -1, the control will revert to using the system color for the text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79676-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79676-114">Return value</span></span>

<span data-ttu-id="79676-115">Возвращает значение **COLORREF** , представляющее предыдущий цвет текста.</span><span class="sxs-lookup"><span data-stu-id="79676-115">Returns a **COLORREF** value that represents the previous text color.</span></span> <span data-ttu-id="79676-116">Если это значение равно-1, элемент управления использует системный цвет для цвета текста.</span><span class="sxs-lookup"><span data-stu-id="79676-116">If this value is -1, the control was using the system color for the text color.</span></span>

## <a name="requirements"></a><span data-ttu-id="79676-117">Требования</span><span class="sxs-lookup"><span data-stu-id="79676-117">Requirements</span></span>



| <span data-ttu-id="79676-118">Требование</span><span class="sxs-lookup"><span data-stu-id="79676-118">Requirement</span></span> | <span data-ttu-id="79676-119">Значение</span><span class="sxs-lookup"><span data-stu-id="79676-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79676-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79676-120">Minimum supported client</span></span><br/> | <span data-ttu-id="79676-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="79676-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="79676-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79676-122">Minimum supported server</span></span><br/> | <span data-ttu-id="79676-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="79676-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79676-124">Header</span><span class="sxs-lookup"><span data-stu-id="79676-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="79676-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="79676-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79676-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79676-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79676-127">**TVM \_ жеттекстколор**</span><span class="sxs-lookup"><span data-stu-id="79676-127">**TVM\_GETTEXTCOLOR**</span></span>](tvm-gettextcolor.md)
</dt> </dl>

 

