---
title: Сообщение HDM_ORDERTOINDEX (Коммктрл. h)
description: Извлекает значение индекса для элемента на основе его порядка в элементе управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса ордертоиндекс.
ms.assetid: vs|controls|~\controls\header\messages\hdm_ordertoindex.htm
keywords:
- Элементы управления Windows для HDM_ORDERTOINDEX сообщений
topic_type:
- apiref
api_name:
- HDM_ORDERTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b65d10fb27c9a07639ebbd5770a53d72cbf0aba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071560"
---
# <a name="hdm_ordertoindex-message"></a><span data-ttu-id="7caf1-105">\_Сообщение ОРДЕРТОИНДЕКС HDM</span><span class="sxs-lookup"><span data-stu-id="7caf1-105">HDM\_ORDERTOINDEX message</span></span>

<span data-ttu-id="7caf1-106">Извлекает значение индекса для элемента на основе его порядка в элементе управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="7caf1-106">Retrieves an index value for an item based on its order in the header control.</span></span> <span data-ttu-id="7caf1-107">Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ ордертоиндекс**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) .</span><span class="sxs-lookup"><span data-stu-id="7caf1-107">You can send this message explicitly or use the [**Header\_OrderToIndex**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7caf1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7caf1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7caf1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7caf1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7caf1-110">Порядок, в котором элемент отображается внутри элемента управления "заголовок" слева направо.</span><span class="sxs-lookup"><span data-stu-id="7caf1-110">The order in which the item appears within the header control, from left to right.</span></span> <span data-ttu-id="7caf1-111">Например, значение индекса элемента в дальнем левом столбце должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="7caf1-111">For example, the index value of the item in the far left column would be 0.</span></span> <span data-ttu-id="7caf1-112">Для следующего элемента справа будет использоваться значение 1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="7caf1-112">The value for the next item to the right would be 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="7caf1-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7caf1-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7caf1-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="7caf1-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7caf1-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7caf1-115">Return value</span></span>

<span data-ttu-id="7caf1-116">Возвращает значение типа INT, указывающее индекс элемента.</span><span class="sxs-lookup"><span data-stu-id="7caf1-116">Returns INT that indicates the item index.</span></span> <span data-ttu-id="7caf1-117">Если параметр *wParam* является недопустимым (отрицательный или слишком большой), то возвращаемое значение равно *wParam*.</span><span class="sxs-lookup"><span data-stu-id="7caf1-117">If *wParam* is invalid (negative or too large), the return equals *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="7caf1-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7caf1-118">Requirements</span></span>



| <span data-ttu-id="7caf1-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7caf1-119">Requirement</span></span> | <span data-ttu-id="7caf1-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7caf1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7caf1-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7caf1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7caf1-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7caf1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7caf1-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7caf1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7caf1-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7caf1-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7caf1-125">Header</span><span class="sxs-lookup"><span data-stu-id="7caf1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7caf1-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7caf1-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





