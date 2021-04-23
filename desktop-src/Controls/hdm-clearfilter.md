---
title: Сообщение HDM_CLEARFILTER (Коммктрл. h)
description: Очищает фильтр для данного элемента управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса клеарфилтер.
ms.assetid: 74c0265e-68d1-4414-8fd9-20f5f041d4b4
keywords:
- Элементы управления Windows для HDM_CLEARFILTER сообщений
topic_type:
- apiref
api_name:
- HDM_CLEARFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b1184432517761a567cd76bdd488e4593b1e999
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136439"
---
# <a name="hdm_clearfilter-message"></a><span data-ttu-id="41519-105">\_Сообщение КЛЕАРФИЛТЕР HDM</span><span class="sxs-lookup"><span data-stu-id="41519-105">HDM\_CLEARFILTER message</span></span>

<span data-ttu-id="41519-106">Очищает фильтр для данного элемента управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="41519-106">Clears the filter for a given header control.</span></span> <span data-ttu-id="41519-107">Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ клеарфилтер**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) .</span><span class="sxs-lookup"><span data-stu-id="41519-107">You can send this message explicitly or use the [**Header\_ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="41519-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="41519-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41519-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41519-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41519-110">Значение столбца, указывающее, какой фильтр следует очистить.</span><span class="sxs-lookup"><span data-stu-id="41519-110">A column value indicating which filter to clear.</span></span>

</dd> <dt>

<span data-ttu-id="41519-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41519-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="41519-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="41519-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41519-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41519-113">Return value</span></span>

<span data-ttu-id="41519-114">Возвращает целое число.</span><span class="sxs-lookup"><span data-stu-id="41519-114">Returns an integer.</span></span> <span data-ttu-id="41519-115">**LResult** преобразуется в целое число, которое указывает **true**(1) или **false**(0).</span><span class="sxs-lookup"><span data-stu-id="41519-115">The **LRESULT** is cast to an integer that indicates **TRUE**(1) or **FALSE**(0).</span></span>

## <a name="remarks"></a><span data-ttu-id="41519-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41519-116">Remarks</span></span>

<span data-ttu-id="41519-117">Если значение столбца указано как-1, удаляются все фильтры, а уведомление [ХДН \_ филтерчанже](hdn-filterchange.md) отправляется только один раз.</span><span class="sxs-lookup"><span data-stu-id="41519-117">If the column value is specified as -1, all the filters are cleared, and the [HDN\_FILTERCHANGE](hdn-filterchange.md) notification is sent only once.</span></span>

## <a name="requirements"></a><span data-ttu-id="41519-118">Требования</span><span class="sxs-lookup"><span data-stu-id="41519-118">Requirements</span></span>



| <span data-ttu-id="41519-119">Требование</span><span class="sxs-lookup"><span data-stu-id="41519-119">Requirement</span></span> | <span data-ttu-id="41519-120">Значение</span><span class="sxs-lookup"><span data-stu-id="41519-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41519-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41519-121">Minimum supported client</span></span><br/> | <span data-ttu-id="41519-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41519-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="41519-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41519-123">Minimum supported server</span></span><br/> | <span data-ttu-id="41519-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="41519-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41519-125">Header</span><span class="sxs-lookup"><span data-stu-id="41519-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="41519-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="41519-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41519-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41519-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41519-128">**\_Клеараллфилтерс заголовка**</span><span class="sxs-lookup"><span data-stu-id="41519-128">**Header\_ClearAllFilters**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)
</dt> </dl>

 

 





