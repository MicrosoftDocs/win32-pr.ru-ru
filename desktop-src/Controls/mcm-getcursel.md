---
title: Сообщение MCM_GETCURSEL (Коммктрл. h)
description: Извлекает текущую выбранную дату. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал.
ms.assetid: d4edc9ed-7c92-4ec8-bfa1-8ae597826b3f
keywords:
- Элементы управления Windows для MCM_GETCURSEL сообщений
topic_type:
- apiref
api_name:
- MCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dece95c65e900119c7043c0d5eda22bf473e6c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491448"
---
# <a name="mcm_getcursel-message"></a><span data-ttu-id="132f0-105">MCM \_ сообщение</span><span class="sxs-lookup"><span data-stu-id="132f0-105">MCM\_GETCURSEL message</span></span>

<span data-ttu-id="132f0-106">Извлекает текущую выбранную дату.</span><span class="sxs-lookup"><span data-stu-id="132f0-106">Retrieves the currently selected date.</span></span> <span data-ttu-id="132f0-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) .</span><span class="sxs-lookup"><span data-stu-id="132f0-107">You can send this message explicitly or by using the [**MonthCal\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="132f0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="132f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="132f0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="132f0-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="132f0-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="132f0-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="132f0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="132f0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="132f0-112">Указатель на структуру [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , которая будет принимать текущую выбранную информацию о дате.</span><span class="sxs-lookup"><span data-stu-id="132f0-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that will receive the currently selected date information.</span></span> <span data-ttu-id="132f0-113">Этот параметр должен быть допустимым адресом и не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="132f0-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="132f0-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="132f0-114">Return value</span></span>

<span data-ttu-id="132f0-115">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="132f0-115">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="132f0-116">Это сообщение всегда будет завершаться ошибкой при применении к элементам управления "Календарь на месяц", для которых задан стиль "Многоэлементный [**\_ Выбор MCS**](month-calendar-control-styles.md) ".</span><span class="sxs-lookup"><span data-stu-id="132f0-116">This message will always fail when applied to month calendar controls set to the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="132f0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="132f0-117">Requirements</span></span>



| <span data-ttu-id="132f0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="132f0-118">Requirement</span></span> | <span data-ttu-id="132f0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="132f0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="132f0-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="132f0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="132f0-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="132f0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="132f0-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="132f0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="132f0-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="132f0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="132f0-124">Header</span><span class="sxs-lookup"><span data-stu-id="132f0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="132f0-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="132f0-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="132f0-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="132f0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="132f0-127">Время в элементе управления ' календарь на месяц '</span><span class="sxs-lookup"><span data-stu-id="132f0-127">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

