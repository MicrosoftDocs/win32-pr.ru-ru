---
title: Сообщение TB_SETCOLORSCHEME (Коммктрл. h)
description: Задает сведения о цветовой схеме для элемента управления ToolBar.
ms.assetid: 96cf6464-b760-46af-910f-984e41dbfca5
keywords:
- Элементы управления Windows для TB_SETCOLORSCHEME сообщений
topic_type:
- apiref
api_name:
- TB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b4ed278ea31dfa156dcc8a64afdb98a2ae3b938
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892617"
---
# <a name="tb_setcolorscheme-message"></a><span data-ttu-id="e897a-104">\_Сообщение СЕТКОЛОРСЧЕМЕ ТБ</span><span class="sxs-lookup"><span data-stu-id="e897a-104">TB\_SETCOLORSCHEME message</span></span>

<span data-ttu-id="e897a-105">Задает сведения о цветовой схеме для элемента управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="e897a-105">Sets the color scheme information for the toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e897a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e897a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e897a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e897a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e897a-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e897a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e897a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e897a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e897a-110">Указатель на структуру [**колорсчеме**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) , содержащую сведения о цветовой схеме.</span><span class="sxs-lookup"><span data-stu-id="e897a-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that contains the color scheme information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e897a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e897a-111">Return value</span></span>

<span data-ttu-id="e897a-112">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="e897a-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e897a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e897a-113">Remarks</span></span>

<span data-ttu-id="e897a-114">Элемент управления ToolBar использует сведения о цветовой схеме при рисовании трехмерных элементов в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="e897a-114">The toolbar control uses the color scheme information when drawing the 3-D elements in the control.</span></span>

<span data-ttu-id="e897a-115">Если стили оформления включены, это сообщение не действует.</span><span class="sxs-lookup"><span data-stu-id="e897a-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="e897a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e897a-116">Requirements</span></span>



| <span data-ttu-id="e897a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e897a-117">Requirement</span></span> | <span data-ttu-id="e897a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e897a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e897a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e897a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e897a-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e897a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e897a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e897a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e897a-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e897a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e897a-123">Header</span><span class="sxs-lookup"><span data-stu-id="e897a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e897a-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e897a-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e897a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e897a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e897a-126">**\_ЖЕТКОЛОРСЧЕМЕ ТБ**</span><span class="sxs-lookup"><span data-stu-id="e897a-126">**TB\_GETCOLORSCHEME**</span></span>](tb-getcolorscheme.md)
</dt> </dl>

 

 





