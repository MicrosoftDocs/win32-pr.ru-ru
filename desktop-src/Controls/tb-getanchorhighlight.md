---
title: Сообщение TB_GETANCHORHIGHLIGHT (Коммктрл. h)
description: Получает параметр выделения закреплений для панели инструментов.
ms.assetid: 167d481c-8684-40eb-9323-cfa238be3643
keywords:
- Элементы управления Windows для TB_GETANCHORHIGHLIGHT сообщений
topic_type:
- apiref
api_name:
- TB_GETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bfff5ef1853bbf5657604c673dcc6a9be43af83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892801"
---
# <a name="tb_getanchorhighlight-message"></a><span data-ttu-id="33175-104">\_Сообщение ЖЕТАНЧОРХИГХЛИГХТ ТБ</span><span class="sxs-lookup"><span data-stu-id="33175-104">TB\_GETANCHORHIGHLIGHT message</span></span>

<span data-ttu-id="33175-105">Получает параметр выделения закреплений для панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="33175-105">Retrieves the anchor highlight setting for a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="33175-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="33175-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33175-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33175-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="33175-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="33175-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="33175-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33175-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="33175-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="33175-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33175-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="33175-111">Return value</span></span>

<span data-ttu-id="33175-112">Возвращает логическое значение, указывающее, задано ли выделение закреплений.</span><span class="sxs-lookup"><span data-stu-id="33175-112">Returns a Boolean value that indicates if anchor highlighting is set.</span></span> <span data-ttu-id="33175-113">Если это значение не равно нулю, выделение закреплений включено.</span><span class="sxs-lookup"><span data-stu-id="33175-113">If this value is nonzero, anchor highlighting is enabled.</span></span> <span data-ttu-id="33175-114">Если это значение равно нулю, то оно отключено.</span><span class="sxs-lookup"><span data-stu-id="33175-114">If this value is zero, it is disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="33175-115">Требования</span><span class="sxs-lookup"><span data-stu-id="33175-115">Requirements</span></span>



| <span data-ttu-id="33175-116">Требование</span><span class="sxs-lookup"><span data-stu-id="33175-116">Requirement</span></span> | <span data-ttu-id="33175-117">Значение</span><span class="sxs-lookup"><span data-stu-id="33175-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33175-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33175-118">Minimum supported client</span></span><br/> | <span data-ttu-id="33175-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="33175-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="33175-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33175-120">Minimum supported server</span></span><br/> | <span data-ttu-id="33175-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="33175-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="33175-122">Header</span><span class="sxs-lookup"><span data-stu-id="33175-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="33175-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="33175-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33175-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33175-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33175-125">**\_СЕТАНЧОРХИГХЛИГХТ ТБ**</span><span class="sxs-lookup"><span data-stu-id="33175-125">**TB\_SETANCHORHIGHLIGHT**</span></span>](tb-setanchorhighlight.md)
</dt> </dl>

 

 





