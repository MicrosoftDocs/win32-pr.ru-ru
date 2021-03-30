---
title: Сообщение LB_GETTOPINDEX (Winuser. h)
description: Возвращает индекс первого видимого элемента в поле со списком.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_gettopindex.htm
keywords:
- Элементы управления Windows для LB_GETTOPINDEX сообщений
topic_type:
- apiref
api_name:
- LB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdeca8e3f40ab3105bb9703db9355d09a214f5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988692"
---
# <a name="lb_gettopindex-message"></a><span data-ttu-id="7da82-104">Сообщение жеттопиндекс балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="7da82-104">LB\_GETTOPINDEX message</span></span>

<span data-ttu-id="7da82-105">Возвращает индекс первого видимого элемента в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="7da82-105">Gets the index of the first visible item in a list box.</span></span> <span data-ttu-id="7da82-106">Изначально элемент с индексом 0 находится в верхней части окна списка, но если содержимое списка было прокручено, то в верхней части может находиться другой элемент.</span><span class="sxs-lookup"><span data-stu-id="7da82-106">Initially the item with index 0 is at the top of the list box, but if the list box contents have been scrolled another item may be at the top.</span></span> <span data-ttu-id="7da82-107">Первый видимый элемент в списке с несколькими столбцами является верхним левым элементом.</span><span class="sxs-lookup"><span data-stu-id="7da82-107">The first visible item in a multiple-column list box is the top-left item.</span></span>

## <a name="parameters"></a><span data-ttu-id="7da82-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7da82-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7da82-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7da82-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7da82-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="7da82-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7da82-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7da82-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7da82-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="7da82-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7da82-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7da82-113">Return value</span></span>

<span data-ttu-id="7da82-114">Возвращаемое значение — это индекс первого видимого элемента в списке.</span><span class="sxs-lookup"><span data-stu-id="7da82-114">The return value is the index of the first visible item in the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="7da82-115">Требования</span><span class="sxs-lookup"><span data-stu-id="7da82-115">Requirements</span></span>



| <span data-ttu-id="7da82-116">Требование</span><span class="sxs-lookup"><span data-stu-id="7da82-116">Requirement</span></span> | <span data-ttu-id="7da82-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7da82-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7da82-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7da82-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7da82-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7da82-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7da82-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7da82-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7da82-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7da82-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7da82-122">Header</span><span class="sxs-lookup"><span data-stu-id="7da82-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7da82-123"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7da82-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7da82-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7da82-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7da82-125">**сеттопиндекс балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="7da82-125">**LB\_SETTOPINDEX**</span></span>](lb-settopindex.md)
</dt> </dl>

 

 





