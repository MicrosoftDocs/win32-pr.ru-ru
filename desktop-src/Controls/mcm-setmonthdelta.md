---
title: Сообщение MCM_SETMONTHDELTA (Коммктрл. h)
description: Задает скорость прокрутки для элемента управления "месячный календарь". Скорость прокрутки — это число месяцев, в течение которых элемент управления перемещает свое отображение, когда пользователь нажимает кнопку прокрутки. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал сетмонсделта.
ms.assetid: 2d01b95f-3be8-4548-80b5-ac01d3e49e9f
keywords:
- Элементы управления Windows для MCM_SETMONTHDELTA сообщений
topic_type:
- apiref
api_name:
- MCM_SETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 123eddb55a7ee8ddf8e3f6d8136e9ee57dfc8681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654687"
---
# <a name="mcm_setmonthdelta-message"></a><span data-ttu-id="8ee8d-106">\_Сообщение MCM сетмонсделта</span><span class="sxs-lookup"><span data-stu-id="8ee8d-106">MCM\_SETMONTHDELTA message</span></span>

<span data-ttu-id="8ee8d-107">Задает скорость прокрутки для элемента управления "месячный календарь".</span><span class="sxs-lookup"><span data-stu-id="8ee8d-107">Sets the scroll rate for a month calendar control.</span></span> <span data-ttu-id="8ee8d-108">Скорость прокрутки — это число месяцев, в течение которых элемент управления перемещает свое отображение, когда пользователь нажимает кнопку прокрутки.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-108">The scroll rate is the number of months that the control moves its display when the user clicks a scroll button.</span></span> <span data-ttu-id="8ee8d-109">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ сетмонсделта**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) .</span><span class="sxs-lookup"><span data-stu-id="8ee8d-109">You can send this message explicitly or by using the [**MonthCal\_SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8ee8d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ee8d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ee8d-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8ee8d-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ee8d-112">Значение, представляющее число месяцев, которое должно быть задано в качестве скорости прокрутки элемента управления.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-112">Value representing the number of months to be set as the control's scroll rate.</span></span> <span data-ttu-id="8ee8d-113">Если это значение равно нулю, то дельта по месяцам сбрасывается до значения по умолчанию, которое равно количеству месяцев, отображаемых в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-113">If this value is zero, the month delta is reset to the default, which is the number of months displayed in the control.</span></span>

</dd> <dt>

<span data-ttu-id="8ee8d-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ee8d-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8ee8d-115">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ee8d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ee8d-116">Return value</span></span>

<span data-ttu-id="8ee8d-117">Возвращает значение типа INT, представляющее предыдущую скорость прокрутки.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-117">Returns an INT value that represents the previous scroll rate.</span></span> <span data-ttu-id="8ee8d-118">Если скорость прокрутки не была задана ранее, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-118">If the scroll rate was not previously set, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ee8d-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ee8d-119">Remarks</span></span>

<span data-ttu-id="8ee8d-120">Клавиши PAGE UP и PAGE DOWN, VK \_ предыдущие и VK \_ Next, изменяют выбранный месяц на один, независимо от числа отображаемых месяцев или значения, установленного **MCM \_ сетмонсделта**.</span><span class="sxs-lookup"><span data-stu-id="8ee8d-120">The PAGE UP and PAGE DOWN keys, VK\_PRIOR and VK\_NEXT, change the selected month by one, regardless of the number of months displayed or the value set by **MCM\_SETMONTHDELTA**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ee8d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="8ee8d-121">Requirements</span></span>



| <span data-ttu-id="8ee8d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="8ee8d-122">Requirement</span></span> | <span data-ttu-id="8ee8d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="8ee8d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee8d-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ee8d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8ee8d-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8ee8d-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8ee8d-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ee8d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8ee8d-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8ee8d-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8ee8d-128">Header</span><span class="sxs-lookup"><span data-stu-id="8ee8d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ee8d-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ee8d-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





