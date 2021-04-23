---
title: Сообщение DTM_GETMCSTYLE (Коммктрл. h)
description: Возвращает стиль элемента управления "Выбор даты и времени" (DTP). Отправляйте это сообщение явным образом или с помощью \_ макроса DateTime жетмонскалстиле.
ms.assetid: 8983898f-e23a-4247-838c-56364f695429
keywords:
- Элементы управления Windows для DTM_GETMCSTYLE сообщений
topic_type:
- apiref
api_name:
- DTM_GETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cae82d271d0e9aece54046527dfa3bedcef657f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989019"
---
# <a name="dtm_getmcstyle-message"></a><span data-ttu-id="4be29-105">\_Сообщение DTM жетмкстиле</span><span class="sxs-lookup"><span data-stu-id="4be29-105">DTM\_GETMCSTYLE message</span></span>

<span data-ttu-id="4be29-106">Возвращает стиль элемента управления "Выбор даты и времени" (DTP).</span><span class="sxs-lookup"><span data-stu-id="4be29-106">Gets the style of a date and time picker (DTP) control.</span></span> <span data-ttu-id="4be29-107">Отправляйте это сообщение явным образом или с помощью макроса [**DateTime \_ жетмонскалстиле**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) .</span><span class="sxs-lookup"><span data-stu-id="4be29-107">Send this message explicitly or by using the [**DateTime\_GetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4be29-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4be29-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4be29-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4be29-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4be29-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4be29-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4be29-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4be29-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4be29-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4be29-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4be29-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4be29-113">Return value</span></span>

<span data-ttu-id="4be29-114">Возвращает значение стиля элемента управления.</span><span class="sxs-lookup"><span data-stu-id="4be29-114">Returns the style value of the control.</span></span> <span data-ttu-id="4be29-115">Дополнительные сведения см. в разделе [стили элементов управления календарем месяца](month-calendar-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="4be29-115">For more information see [Month Calendar Control Styles](month-calendar-control-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4be29-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4be29-116">Requirements</span></span>



| <span data-ttu-id="4be29-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4be29-117">Requirement</span></span> | <span data-ttu-id="4be29-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4be29-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4be29-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4be29-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4be29-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4be29-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4be29-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4be29-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4be29-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4be29-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4be29-123">Header</span><span class="sxs-lookup"><span data-stu-id="4be29-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4be29-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4be29-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





