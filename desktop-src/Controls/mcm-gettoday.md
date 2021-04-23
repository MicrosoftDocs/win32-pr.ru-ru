---
title: Сообщение MCM_GETTODAY (Коммктрл. h)
description: Извлекает сведения о дате для даты, указанной как \ 0034; сегодня \ 0034; для элемента управления "месячный календарь". Это сообщение можно отправить явно или с помощью \_ макроса монскал ontoday.
ms.assetid: a79feb57-6aa3-4c96-95f3-7018b6b8327f
keywords:
- Элементы управления Windows для MCM_GETTODAY сообщений
topic_type:
- apiref
api_name:
- MCM_GETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21538af3c573b3d972b7f16bfe024e0d36211644
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988726"
---
# <a name="mcm_gettoday-message"></a><span data-ttu-id="efce4-105">\_Сообщение MCM</span><span class="sxs-lookup"><span data-stu-id="efce4-105">MCM\_GETTODAY message</span></span>

<span data-ttu-id="efce4-106">Извлекает сведения о дате для даты, указанной в поле "сегодня", для элемента управления "месячный календарь".</span><span class="sxs-lookup"><span data-stu-id="efce4-106">Retrieves the date information for the date specified as "today" for a month calendar control.</span></span> <span data-ttu-id="efce4-107">Это сообщение можно отправить явно или с помощью макроса [**монскал \_ ontoday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) .</span><span class="sxs-lookup"><span data-stu-id="efce4-107">You can send this message explicitly or by using the [**MonthCal\_GetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="efce4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="efce4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efce4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="efce4-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="efce4-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="efce4-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="efce4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="efce4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="efce4-112">Указатель на структуру [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , которая получит сведения о дате.</span><span class="sxs-lookup"><span data-stu-id="efce4-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that will receive the date information.</span></span> <span data-ttu-id="efce4-113">Этот параметр должен быть допустимым адресом и не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="efce4-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efce4-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="efce4-114">Return value</span></span>

<span data-ttu-id="efce4-115">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="efce4-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="efce4-116">Требования</span><span class="sxs-lookup"><span data-stu-id="efce4-116">Requirements</span></span>



| <span data-ttu-id="efce4-117">Требование</span><span class="sxs-lookup"><span data-stu-id="efce4-117">Requirement</span></span> | <span data-ttu-id="efce4-118">Значение</span><span class="sxs-lookup"><span data-stu-id="efce4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="efce4-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="efce4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="efce4-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="efce4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="efce4-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="efce4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="efce4-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="efce4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="efce4-123">Header</span><span class="sxs-lookup"><span data-stu-id="efce4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="efce4-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="efce4-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efce4-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="efce4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efce4-126">Время в элементе управления ' календарь на месяц '</span><span class="sxs-lookup"><span data-stu-id="efce4-126">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

