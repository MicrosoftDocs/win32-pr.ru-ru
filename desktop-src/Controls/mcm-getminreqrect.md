---
title: Сообщение MCM_GETMINREQRECT (Коммктрл. h)
description: Возвращает минимальный размер, необходимый для показа полного месяца в элементе управления ' календарь на месяц '. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал жетминрекрект.
ms.assetid: f0378338-4809-48e9-9387-ed8b79356f95
keywords:
- Элементы управления Windows для MCM_GETMINREQRECT сообщений
topic_type:
- apiref
api_name:
- MCM_GETMINREQRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac6b2e2b16a70841836a277ffe55e030a6d6a241
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489963"
---
# <a name="mcm_getminreqrect-message"></a><span data-ttu-id="0f902-105">\_Сообщение MCM жетминрекрект</span><span class="sxs-lookup"><span data-stu-id="0f902-105">MCM\_GETMINREQRECT message</span></span>

<span data-ttu-id="0f902-106">Возвращает минимальный размер, необходимый для показа полного месяца в элементе управления ' календарь на месяц '.</span><span class="sxs-lookup"><span data-stu-id="0f902-106">Retrieves the minimum size required to display a full month in a month calendar control.</span></span> <span data-ttu-id="0f902-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ жетминрекрект**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) .</span><span class="sxs-lookup"><span data-stu-id="0f902-107">You can send this message explicitly or by using the [**MonthCal\_GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0f902-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f902-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f902-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f902-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0f902-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="0f902-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0f902-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f902-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f902-112">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая будет принимать сведения об ограничивающем прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="0f902-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive bounding rectangle information.</span></span> <span data-ttu-id="0f902-113">Этот параметр должен быть допустимым адресом и не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0f902-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f902-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f902-114">Return value</span></span>

<span data-ttu-id="0f902-115">Возвращает ненулевое значение, а *lParam* получает применимые сведения об ограничении в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="0f902-115">Returns nonzero and *lParam* receives the applicable bounding information if successful.</span></span> <span data-ttu-id="0f902-116">В противном случае сообщение возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="0f902-116">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f902-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f902-117">Remarks</span></span>

<span data-ttu-id="0f902-118">Минимальный необходимый размер окна для элемента управления "Календарь на месяц" зависит от текущего выбранного шрифта, стилей элементов управления, системных метрик и региональных параметров.</span><span class="sxs-lookup"><span data-stu-id="0f902-118">The minimum required window size for a month calendar control depends on the currently selected font, control styles, system metrics, and regional settings.</span></span> <span data-ttu-id="0f902-119">Когда приложение изменяет все, что влияет на минимальный размер окна, или обрабатывает сообщение [**WM \_ сеттингчанже**](/windows/desktop/winmsg/wm-settingchange) , оно должно отправить **MCM \_ жетминрекрект** , чтобы определить новый минимальный размер.</span><span class="sxs-lookup"><span data-stu-id="0f902-119">When an application changes anything that affects the minimum window size, or processes a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message, it should send **MCM\_GETMINREQRECT** to determine the new minimum size.</span></span>

> [!Note]  
> <span data-ttu-id="0f902-120">Прямоугольник, возвращаемый функцией **MCM \_ жетминрекрект** , не включает ширину строки "Today", если она существует.</span><span class="sxs-lookup"><span data-stu-id="0f902-120">The rectangle returned by **MCM\_GETMINREQRECT** does not include the width of the "Today" string, if it is present.</span></span> <span data-ttu-id="0f902-121">Если стиль [**MCS \_ Today**](month-calendar-control-styles.md) не задан, приложение также должно извлечь прямоугольник, который определяет ширину строки "сегодня", отправив сообщение [**MCM \_ жетмакстодайвидс**](mcm-getmaxtodaywidth.md) .</span><span class="sxs-lookup"><span data-stu-id="0f902-121">If the [**MCS\_NOTODAY**](month-calendar-control-styles.md) style is not set, your application should also retrieve the rectangle that defines the "Today" string width by sending a [**MCM\_GETMAXTODAYWIDTH**](mcm-getmaxtodaywidth.md) message.</span></span> <span data-ttu-id="0f902-122">Используйте большее из двух прямоугольников, чтобы убедиться, что строка "Today" не обрезана.</span><span class="sxs-lookup"><span data-stu-id="0f902-122">Use the larger of the two rectangles to ensure that the "Today" string is not clipped.</span></span>

 

<span data-ttu-id="0f902-123">**Верхние** и **левые** элементы структуры, на которые указывает *lParam* , всегда будут равны нулю.</span><span class="sxs-lookup"><span data-stu-id="0f902-123">The **top** and **left** members of the structure pointed to by *lParam* will always be zero.</span></span> <span data-ttu-id="0f902-124">**Правый** и **Нижний** элементы представляют минимум *CX* и *CY* , необходимые для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0f902-124">The **right** and **bottom** members represent the minimum *cx* and *cy* required for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f902-125">Требования</span><span class="sxs-lookup"><span data-stu-id="0f902-125">Requirements</span></span>



| <span data-ttu-id="0f902-126">Требование</span><span class="sxs-lookup"><span data-stu-id="0f902-126">Requirement</span></span> | <span data-ttu-id="0f902-127">Значение</span><span class="sxs-lookup"><span data-stu-id="0f902-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f902-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f902-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0f902-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f902-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0f902-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f902-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0f902-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0f902-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0f902-132">Header</span><span class="sxs-lookup"><span data-stu-id="0f902-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f902-133"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f902-133"><dt>Commctrl.h</dt></span></span> </dl> |



 

