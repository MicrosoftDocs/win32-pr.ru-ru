---
title: Сообщение DTM_GETRANGE (Коммктрл. h)
description: Возвращает текущее минимальное и максимальное допустимое системное время для элемента управления "Выбор даты и времени" (DTP). Это сообщение можно отправить явным образом или использовать макрос DateTime \_ .
ms.assetid: 190cada6-49ee-483f-a464-d3d789127159
keywords:
- Элементы управления Windows для DTM_GETRANGE сообщений
topic_type:
- apiref
api_name:
- DTM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a50a2ae9fe4ca77198f9e63548f709e0f571fdb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491826"
---
# <a name="dtm_getrange-message"></a><span data-ttu-id="6c1a8-105">Сообщение DTMного \_ диапазона</span><span class="sxs-lookup"><span data-stu-id="6c1a8-105">DTM\_GETRANGE message</span></span>

<span data-ttu-id="6c1a8-106">Возвращает текущее минимальное и максимальное допустимое системное время для элемента управления "Выбор даты и времени" (DTP).</span><span class="sxs-lookup"><span data-stu-id="6c1a8-106">Gets the current minimum and maximum allowable system times for a date and time picker (DTP) control.</span></span> <span data-ttu-id="6c1a8-107">Это сообщение можно отправить явным образом или использовать макрос [**DateTime \_**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) .</span><span class="sxs-lookup"><span data-stu-id="6c1a8-107">You can send this message explicitly or use the [**DateTime\_GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c1a8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c1a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c1a8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c1a8-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6c1a8-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="6c1a8-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6c1a8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c1a8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c1a8-112">Указатель на массив структур [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) с двумя элементами.</span><span class="sxs-lookup"><span data-stu-id="6c1a8-112">A pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c1a8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c1a8-113">Return value</span></span>

<span data-ttu-id="6c1a8-114">Возвращает значение **типа DWORD** , которое представляет собой сочетание гдтр \_ min или гдтр \_ Max.</span><span class="sxs-lookup"><span data-stu-id="6c1a8-114">Returns a **DWORD** value that is a combination of GDTR\_MIN or GDTR\_MAX.</span></span> <span data-ttu-id="6c1a8-115">Первый элемент массива [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) содержит минимальное допустимое время, если \_ задано значение гдтр min.</span><span class="sxs-lookup"><span data-stu-id="6c1a8-115">The first element of the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) array contains the minimum allowable time if GDTR\_MIN is set.</span></span> <span data-ttu-id="6c1a8-116">Второй элемент массива **SYSTEMTIME** содержит максимально допустимое время, если \_ задано значение гдтр Max.</span><span class="sxs-lookup"><span data-stu-id="6c1a8-116">The second element of the **SYSTEMTIME** array contains the maximum allowable time if GDTR\_MAX is set.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c1a8-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c1a8-117">Remarks</span></span>

<span data-ttu-id="6c1a8-118">Средство выбора даты и времени отображает только даты и время, которые находятся в пределах указанного диапазона, запрещая пользователю выбирать дату и время, находящиеся за пределами диапазона.</span><span class="sxs-lookup"><span data-stu-id="6c1a8-118">The date and time picker displays only dates/times that fall within the specified range, preventing the user from selecting a date and time that falls outside the range.</span></span> <span data-ttu-id="6c1a8-119">Если сообщение [**DTM \_ сетсистемтиме**](dtm-setsystemtime.md) указывает дату и время, которые выходят за пределы диапазона, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="6c1a8-119">If the [**DTM\_SETSYSTEMTIME**](dtm-setsystemtime.md) message specifies a date and time that falls outside the range, it will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c1a8-120">Требования</span><span class="sxs-lookup"><span data-stu-id="6c1a8-120">Requirements</span></span>



| <span data-ttu-id="6c1a8-121">Требование</span><span class="sxs-lookup"><span data-stu-id="6c1a8-121">Requirement</span></span> | <span data-ttu-id="6c1a8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6c1a8-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c1a8-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c1a8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6c1a8-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c1a8-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c1a8-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c1a8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6c1a8-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6c1a8-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c1a8-127">Header</span><span class="sxs-lookup"><span data-stu-id="6c1a8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c1a8-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c1a8-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

