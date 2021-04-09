---
title: Сообщение MCM_GETMONTHDELTA (Коммктрл. h)
description: Возвращает скорость прокрутки для элемента управления "месячный календарь". Скорость прокрутки — это число месяцев, в течение которых элемент управления перемещает свое отображение, когда пользователь нажимает кнопку прокрутки. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал жетмонсделта.
ms.assetid: 6db02993-b22c-430f-8928-8bd5768b2151
keywords:
- Элементы управления Windows для MCM_GETMONTHDELTA сообщений
topic_type:
- apiref
api_name:
- MCM_GETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01eaa40b930e6317cc2be6b674f0cea58115ae40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137886"
---
# <a name="mcm_getmonthdelta-message"></a><span data-ttu-id="81068-106">\_Сообщение MCM жетмонсделта</span><span class="sxs-lookup"><span data-stu-id="81068-106">MCM\_GETMONTHDELTA message</span></span>

<span data-ttu-id="81068-107">Возвращает скорость прокрутки для элемента управления "месячный календарь".</span><span class="sxs-lookup"><span data-stu-id="81068-107">Retrieves the scroll rate for a month calendar control.</span></span> <span data-ttu-id="81068-108">Скорость прокрутки — это число месяцев, в течение которых элемент управления перемещает свое отображение, когда пользователь нажимает кнопку прокрутки.</span><span class="sxs-lookup"><span data-stu-id="81068-108">The scroll rate is the number of months that the control moves its display when the user clicks a scroll button.</span></span> <span data-ttu-id="81068-109">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ жетмонсделта**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) .</span><span class="sxs-lookup"><span data-stu-id="81068-109">You can send this message explicitly or by using the [**MonthCal\_GetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="81068-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="81068-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81068-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81068-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="81068-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="81068-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="81068-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81068-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="81068-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="81068-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81068-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81068-115">Return value</span></span>

<span data-ttu-id="81068-116">Если дельта за месяц была ранее задана с помощью сообщения [**MCM \_ сетмонсделта**](mcm-setmonthdelta.md) , возвращает значение типа int, представляющее текущую скорость прокрутки месячного календаря.</span><span class="sxs-lookup"><span data-stu-id="81068-116">If the month delta was previously set using the [**MCM\_SETMONTHDELTA**](mcm-setmonthdelta.md) message, returns an INT value that represents the month calendar's current scroll rate.</span></span> <span data-ttu-id="81068-117">Если дельта за месяц не была ранее задана с помощью сообщения **MCM \_ сетмонсделта** , или значение по умолчанию для параметра month было восстановлено до значения, возвращается значение типа int, представляющее текущее число отображаемых месяцев.</span><span class="sxs-lookup"><span data-stu-id="81068-117">If the month delta was not previously set using the **MCM\_SETMONTHDELTA** message, or the month delta was reset to the default, returns an INT value that represents the current number of months visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="81068-118">Требования</span><span class="sxs-lookup"><span data-stu-id="81068-118">Requirements</span></span>



| <span data-ttu-id="81068-119">Требование</span><span class="sxs-lookup"><span data-stu-id="81068-119">Requirement</span></span> | <span data-ttu-id="81068-120">Значение</span><span class="sxs-lookup"><span data-stu-id="81068-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81068-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81068-121">Minimum supported client</span></span><br/> | <span data-ttu-id="81068-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81068-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="81068-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81068-123">Minimum supported server</span></span><br/> | <span data-ttu-id="81068-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="81068-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="81068-125">Header</span><span class="sxs-lookup"><span data-stu-id="81068-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="81068-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="81068-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





