---
title: Код уведомления MCN_GETDAYSTATE (Коммктрл. h)
description: Посылается элементом управления "месячный календарь" для запроса сведений о том, как должны отображаться отдельные дни. Этот код уведомления отправляется только элементам управления "месячный календарь", использующим \_ стиль MCS дайстате, и отправляется в виде \_ сообщения уведомления WM.
ms.assetid: dc2608e0-c598-4b26-9195-208f09cd84b7
keywords:
- MCN_GETDAYSTATE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- MCN_GETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff81b9f171884f39063c517cb17299a55b4053b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802417"
---
# <a name="mcn_getdaystate-notification-code"></a><span data-ttu-id="fd3f3-105">\_Код уведомления МКН жетдайстате</span><span class="sxs-lookup"><span data-stu-id="fd3f3-105">MCN\_GETDAYSTATE notification code</span></span>

<span data-ttu-id="fd3f3-106">Посылается элементом управления "месячный календарь" для запроса сведений о том, как должны отображаться отдельные дни.</span><span class="sxs-lookup"><span data-stu-id="fd3f3-106">Sent by a month calendar control to request information about how individual days should be displayed.</span></span> <span data-ttu-id="fd3f3-107">Этот код уведомления отправляется только элементам управления "месячный календарь", использующим стиль [**MCS \_ дайстате**](month-calendar-control-styles.md) , и отправляется в виде сообщения [**\_ уведомления WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fd3f3-107">This notification code is sent only by month calendar controls that use the [**MCS\_DAYSTATE**](month-calendar-control-styles.md) style, and it is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_GETDAYSTATE

    lpNMDayState = (LPNMDAYSTATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="fd3f3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd3f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd3f3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fd3f3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd3f3-110">Указатель на структуру [**нмдайстате**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) .</span><span class="sxs-lookup"><span data-stu-id="fd3f3-110">Pointer to an [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) structure.</span></span> <span data-ttu-id="fd3f3-111">Структура содержит сведения о кадре времени, для которого элемент управления нуждается в сведениях, и получает адрес массива, предоставляющего эти данные.</span><span class="sxs-lookup"><span data-stu-id="fd3f3-111">The structure contains information about the time frame for which the control needs information, and it receives the address of an array that provides this data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd3f3-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd3f3-112">Return value</span></span>

<span data-ttu-id="fd3f3-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="fd3f3-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd3f3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd3f3-114">Remarks</span></span>

<span data-ttu-id="fd3f3-115">Обработка этого кода уведомления позволяет приложению настраивать его отображение, указывая, что определенные дни отображаются полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="fd3f3-115">Handling this notification code allows your application to customize its display by specifying that certain days be displayed in bold.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd3f3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fd3f3-116">Requirements</span></span>



| <span data-ttu-id="fd3f3-117">Требование</span><span class="sxs-lookup"><span data-stu-id="fd3f3-117">Requirement</span></span> | <span data-ttu-id="fd3f3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fd3f3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd3f3-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd3f3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fd3f3-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd3f3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd3f3-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd3f3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fd3f3-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fd3f3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fd3f3-123">Header</span><span class="sxs-lookup"><span data-stu-id="fd3f3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd3f3-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd3f3-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





