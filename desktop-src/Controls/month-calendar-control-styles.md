---
title: Стили управления календарем месяца (Коммктрл. h)
description: При создании элементов управления "месячный календарь" используются следующие константы стиля.
ms.assetid: 8d9b2239-fd13-4579-81a2-0385fd318e83
topic_type:
- apiref
api_name:
- MCS_DAYSTATE
- MCS_MULTISELECT
- MCS_WEEKNUMBERS
- MCS_NOTODAYCIRCLE
- MCS_NOTODAY
- MCS_NOTRAILINGDATES
- MCS_SHORTDAYSOFWEEK
- MCS_NOSELCHANGEONNAV
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45ccef4a3cc8e16851c0676b8b0dce8c53cfdd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648629"
---
# <a name="month-calendar-control-styles"></a><span data-ttu-id="83358-103">Стили элемента управления "календарь месяца"</span><span class="sxs-lookup"><span data-stu-id="83358-103">Month Calendar Control Styles</span></span>

<span data-ttu-id="83358-104">При создании элементов управления "месячный календарь" используются следующие константы стиля.</span><span class="sxs-lookup"><span data-stu-id="83358-104">The following style constants are used when creating month calendar controls.</span></span>



| <span data-ttu-id="83358-105">Константа</span><span class="sxs-lookup"><span data-stu-id="83358-105">Constant</span></span>                                                                                                                                                                           | <span data-ttu-id="83358-106">Описание</span><span class="sxs-lookup"><span data-stu-id="83358-106">Description</span></span>                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_DAYSTATE"></span><span id="mcs_daystate"></span><dl> <span data-ttu-id="83358-107"><dt>**\_ДАЙСТАТЕ MCS**</dt></span><span class="sxs-lookup"><span data-stu-id="83358-107"><dt>**MCS\_DAYSTATE**</dt></span></span> </dl>                         | <span data-ttu-id="83358-108">[Версия 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="83358-108">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="83358-109">Месячный календарь отправляет уведомления [МКН \_ жетдайстате](mcn-getdaystate.md) , чтобы запросить сведения о том, какие дни должны отображаться полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="83358-109">The month calendar sends [MCN\_GETDAYSTATE](mcn-getdaystate.md) notifications to request information about which days should be displayed in bold.</span></span><br/>                                                                                                          |
| <span id="MCS_MULTISELECT"></span><span id="mcs_multiselect"></span><dl> <span data-ttu-id="83358-110"><dt>**\_МНОГОвариантный выбор MCS**</dt></span><span class="sxs-lookup"><span data-stu-id="83358-110"><dt>**MCS\_MULTISELECT**</dt></span></span> </dl>                | <span data-ttu-id="83358-111">[Версия 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="83358-111">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="83358-112">Месячный календарь позволяет пользователю выбрать диапазон дат в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="83358-112">The month calendar enables the user to select a range of dates within the control.</span></span> <span data-ttu-id="83358-113">По умолчанию максимальный диапазон составляет одну неделю.</span><span class="sxs-lookup"><span data-stu-id="83358-113">By default, the maximum range is one week.</span></span> <span data-ttu-id="83358-114">Вы можете изменить максимальный диапазон, который можно выбрать, с помощью сообщения [**MCM \_ сетмаксселкаунт**](mcm-setmaxselcount.md) .</span><span class="sxs-lookup"><span data-stu-id="83358-114">You can change the maximum range that can be selected by using the [**MCM\_SETMAXSELCOUNT**](mcm-setmaxselcount.md) message.</span></span> <br/> |
| <span id="MCS_WEEKNUMBERS"></span><span id="mcs_weeknumbers"></span><dl> <span data-ttu-id="83358-115"><dt>**\_ВИКНУМБЕРС MCS**</dt></span><span class="sxs-lookup"><span data-stu-id="83358-115"><dt>**MCS\_WEEKNUMBERS**</dt></span></span> </dl>                | <span data-ttu-id="83358-116">[Версия 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="83358-116">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="83358-117">Элемент управления "календарь месяца" отображает номера недель (1-52) слева от каждой строки дней.</span><span class="sxs-lookup"><span data-stu-id="83358-117">The month calendar control displays week numbers (1-52) to the left of each row of days.</span></span> <span data-ttu-id="83358-118">Неделя 1 определена как первая неделя, которая содержит не менее четырех дней.</span><span class="sxs-lookup"><span data-stu-id="83358-118">Week 1 is defined as the first week that contains at least four days.</span></span> <br/>                                                                                              |
| <span id="MCS_NOTODAYCIRCLE"></span><span id="mcs_notodaycircle"></span><dl> <span data-ttu-id="83358-119"><dt>**\_НОТОДАЙЦИРКЛЕ MCS**</dt></span><span class="sxs-lookup"><span data-stu-id="83358-119"><dt>**MCS\_NOTODAYCIRCLE**</dt></span></span> </dl>          | <span data-ttu-id="83358-120">[Версия 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="83358-120">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="83358-121">Элемент управления "календарь месяца" не обработает дату "сегодня".</span><span class="sxs-lookup"><span data-stu-id="83358-121">The month calendar control does not circle the "today" date.</span></span> <br/>                                                                                                                                                                                                |
| <span id="MCS_NOTODAY"></span><span id="mcs_notoday"></span><dl> <span data-ttu-id="83358-122"><dt>**\_сейчас MCS**</dt></span><span class="sxs-lookup"><span data-stu-id="83358-122"><dt>**MCS\_NOTODAY**</dt></span></span> </dl>                            | <span data-ttu-id="83358-123">[Версия 4,70](common-control-versions.md). В элементе управления "календарь месяца" не отображается дата "сегодня" в нижней части элемента управления.</span><span class="sxs-lookup"><span data-stu-id="83358-123">[Version 4.70](common-control-versions.md).The month calendar control does not display the "today" date at the bottom of the control.</span></span> <br/>                                                                                                                                                                   |
| <span id="MCS_NOTRAILINGDATES"></span><span id="mcs_notrailingdates"></span><dl> <span data-ttu-id="83358-124"><dt>**\_НОТРАИЛИНГДАТЕС MCS**</dt></span><span class="sxs-lookup"><span data-stu-id="83358-124"><dt>**MCS\_NOTRAILINGDATES**</dt></span></span> </dl>    | <span data-ttu-id="83358-125">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="83358-125">**Windows Vista.**</span></span> <span data-ttu-id="83358-126">Даты из предыдущего и следующего месяцев не отображаются в календаре текущего месяца.</span><span class="sxs-lookup"><span data-stu-id="83358-126">Dates from the previous and next months are not displayed in the current month's calendar.</span></span><br/>                                                                                                                                                                                              |
| <span id="MCS_SHORTDAYSOFWEEK"></span><span id="mcs_shortdaysofweek"></span><dl> <span data-ttu-id="83358-127"><dt>**\_ШОРТДАЙСОФВИК MCS**</dt></span><span class="sxs-lookup"><span data-stu-id="83358-127"><dt>**MCS\_SHORTDAYSOFWEEK**</dt></span></span> </dl>    | <span data-ttu-id="83358-128">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="83358-128">**Windows Vista.**</span></span> <span data-ttu-id="83358-129">Короткие названия дней отображаются в заголовке.</span><span class="sxs-lookup"><span data-stu-id="83358-129">Short day names are displayed in the header.</span></span><br/>                                                                                                                                                                                                                                            |
| <span id="MCS_NOSELCHANGEONNAV"></span><span id="mcs_noselchangeonnav"></span><dl> <span data-ttu-id="83358-130"><dt>**\_НОСЕЛЧАНЖЕОННАВ MCS**</dt></span><span class="sxs-lookup"><span data-stu-id="83358-130"><dt>**MCS\_NOSELCHANGEONNAV**</dt></span></span> </dl> | <span data-ttu-id="83358-131">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="83358-131">**Windows Vista.**</span></span> <span data-ttu-id="83358-132">Выбор не изменяется, когда пользователь переходит к следующему или предыдущему элементу в календаре.</span><span class="sxs-lookup"><span data-stu-id="83358-132">The selection is not changed when the user navigates next or previous in the calendar.</span></span> <span data-ttu-id="83358-133">Это позволяет пользователю выбрать диапазон больше, чем видимый.</span><span class="sxs-lookup"><span data-stu-id="83358-133">This allows the user to select a range larger than is visible.</span></span><br/>                                                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="83358-134">Требования</span><span class="sxs-lookup"><span data-stu-id="83358-134">Requirements</span></span>



| <span data-ttu-id="83358-135">Требование</span><span class="sxs-lookup"><span data-stu-id="83358-135">Requirement</span></span> | <span data-ttu-id="83358-136">Значение</span><span class="sxs-lookup"><span data-stu-id="83358-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83358-137">Header</span><span class="sxs-lookup"><span data-stu-id="83358-137">Header</span></span><br/> | <dl> <span data-ttu-id="83358-138"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="83358-138"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





