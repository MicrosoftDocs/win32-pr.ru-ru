---
title: Сообщение MCM_GETCALENDARCOUNT (Коммктрл. h)
description: Возвращает число календарей, отображаемых в данный момент в элементе управления Calendar. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал жеткалендаркаунт.
ms.assetid: b9463f02-d37b-49b0-8387-0938020c23ee
keywords:
- Элементы управления Windows для MCM_GETCALENDARCOUNT сообщений
topic_type:
- apiref
api_name:
- MCM_GETCALENDARCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a3be9e9bcc5db8c1aab32cacbcc2ded82727af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136650"
---
# <a name="mcm_getcalendarcount-message"></a><span data-ttu-id="e99fb-105">\_Сообщение MCM жеткалендаркаунт</span><span class="sxs-lookup"><span data-stu-id="e99fb-105">MCM\_GETCALENDARCOUNT message</span></span>

<span data-ttu-id="e99fb-106">Возвращает число календарей, отображаемых в данный момент в элементе управления Calendar.</span><span class="sxs-lookup"><span data-stu-id="e99fb-106">Gets the number of calendars currently displayed in the calendar control.</span></span> <span data-ttu-id="e99fb-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ жеткалендаркаунт**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) .</span><span class="sxs-lookup"><span data-stu-id="e99fb-107">You can send this message explicitly or by using the [**MonthCal\_GetCalendarCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e99fb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e99fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e99fb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e99fb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e99fb-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e99fb-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e99fb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e99fb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e99fb-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e99fb-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e99fb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e99fb-113">Return value</span></span>

<span data-ttu-id="e99fb-114">Число календарей, отображаемых в данный момент в элементе управления Calendar.</span><span class="sxs-lookup"><span data-stu-id="e99fb-114">Number of calendars currently displayed in the calendar control.</span></span> <span data-ttu-id="e99fb-115">Максимальное число разрешенных календарей — 12.</span><span class="sxs-lookup"><span data-stu-id="e99fb-115">The maximum number of allowed calendars is 12.</span></span>

## <a name="requirements"></a><span data-ttu-id="e99fb-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e99fb-116">Requirements</span></span>



| <span data-ttu-id="e99fb-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e99fb-117">Requirement</span></span> | <span data-ttu-id="e99fb-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e99fb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e99fb-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e99fb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e99fb-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e99fb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e99fb-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e99fb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e99fb-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e99fb-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e99fb-123">Header</span><span class="sxs-lookup"><span data-stu-id="e99fb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e99fb-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e99fb-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





