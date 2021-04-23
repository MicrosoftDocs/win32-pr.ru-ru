---
title: Сообщение PGM_GETBORDER (Коммктрл. h)
description: Возвращает текущий размер границы для элемента управления страничного навигатора. Это сообщение можно отправить явным образом или воспользоваться макросом страничного навигатора \_ .
ms.assetid: 5d2f49ad-d940-4a0b-b5a0-05d742151b1c
keywords:
- Элементы управления Windows для PGM_GETBORDER сообщений
topic_type:
- apiref
api_name:
- PGM_GETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be510af44c9cf53000420531843a79e9856c40dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654574"
---
# <a name="pgm_getborder-message"></a><span data-ttu-id="42a15-105">\_Сообщение о ВЫГРАНИЦЕ PGM</span><span class="sxs-lookup"><span data-stu-id="42a15-105">PGM\_GETBORDER message</span></span>

<span data-ttu-id="42a15-106">Возвращает текущий размер границы для элемента управления страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="42a15-106">Retrieves the current border size for the pager control.</span></span> <span data-ttu-id="42a15-107">Это сообщение можно отправить явным образом или воспользоваться макросом [**страничного навигатора \_**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) .</span><span class="sxs-lookup"><span data-stu-id="42a15-107">You can send this message explicitly or use the [**Pager\_GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="42a15-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="42a15-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42a15-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42a15-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="42a15-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="42a15-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="42a15-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42a15-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="42a15-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="42a15-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42a15-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42a15-113">Return value</span></span>

<span data-ttu-id="42a15-114">Возвращает значение типа INT, которое содержит текущий размер границы (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="42a15-114">Returns an INT value that contains the current border size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="42a15-115">Требования</span><span class="sxs-lookup"><span data-stu-id="42a15-115">Requirements</span></span>



| <span data-ttu-id="42a15-116">Требование</span><span class="sxs-lookup"><span data-stu-id="42a15-116">Requirement</span></span> | <span data-ttu-id="42a15-117">Значение</span><span class="sxs-lookup"><span data-stu-id="42a15-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42a15-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42a15-118">Minimum supported client</span></span><br/> | <span data-ttu-id="42a15-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="42a15-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42a15-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42a15-120">Minimum supported server</span></span><br/> | <span data-ttu-id="42a15-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="42a15-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="42a15-122">Header</span><span class="sxs-lookup"><span data-stu-id="42a15-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="42a15-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="42a15-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42a15-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42a15-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a15-125">**\_СЕТБОРДЕР PGM**</span><span class="sxs-lookup"><span data-stu-id="42a15-125">**PGM\_SETBORDER**</span></span>](pgm-setborder.md)
</dt> </dl>

 

 





