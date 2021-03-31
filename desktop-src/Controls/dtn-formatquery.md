---
title: Код уведомления DTN_FORMATQUERY (Коммктрл. h)
description: Отправляется элементом управления "Выбор даты и времени" (DTP) для получения максимально допустимого размера строки, которая будет отображаться в поле обратного вызова. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 0f00086a-0ab8-4f6f-9c3e-6e77008aa088
keywords:
- DTN_FORMATQUERY кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- DTN_FORMATQUERY
- DTN_FORMATQUERYA
- DTN_FORMATQUERYW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69e9653f369f13e0ef4a775265d763e854db4de7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988243"
---
# <a name="dtn_formatquery-notification-code"></a><span data-ttu-id="3a362-105">\_Код уведомления ДТН форматкуери</span><span class="sxs-lookup"><span data-stu-id="3a362-105">DTN\_FORMATQUERY notification code</span></span>

<span data-ttu-id="3a362-106">Отправляется элементом управления "Выбор даты и времени" (DTP) для получения максимально допустимого размера строки, которая будет отображаться в поле обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="3a362-106">Sent by a date and time picker (DTP) control to retrieve the maximum allowable size of the string that will be displayed in a callback field.</span></span> <span data-ttu-id="3a362-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3a362-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_FORMATQUERY

    lpDTFormatQuery = (LPNMDATETIMEFORMATQUERY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3a362-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a362-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a362-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a362-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a362-110">Указатель на структуру [**нмдатетимеформаткуери**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) , содержащую сведения о поле обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="3a362-110">A pointer to an [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) structure containing information about the callback field.</span></span> <span data-ttu-id="3a362-111">Структура содержит подстроку, которая определяет поле обратного вызова и получает максимально допустимый размер строки, которая будет отображаться в поле обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="3a362-111">The structure contains a substring that defines a callback field and receives the maximum allowable size of the string that will be displayed in the callback field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a362-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a362-112">Return value</span></span>

<span data-ttu-id="3a362-113">Владелец элемента управления должен вычислить максимально возможную ширину текста, который будет отображаться в поле обратного вызова, задать элемент **сзмакс** структуры [**нмдатетимеформаткуери**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) и вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="3a362-113">The owner of the control must calculate the maximum possible width of the text that will be displayed in the callback field, set the **szMax** member of the [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) structure, and return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a362-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a362-114">Remarks</span></span>

<span data-ttu-id="3a362-115">Обработка этого кода уведомления подготавливает элемент управления для корректировки максимального размера строки, которая будет отображаться в конкретном поле обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="3a362-115">Handling this notification code prepares the control to adjust for the maximum size of the string that will be displayed in a particular callback field.</span></span> <span data-ttu-id="3a362-116">Это позволяет элементу управления правильно отображать выходные данные в любое время, уменьшая мерцание в отображаемом элементе управления.</span><span class="sxs-lookup"><span data-stu-id="3a362-116">This enables the control to properly display output at all times, reducing flicker within the control's display.</span></span> <span data-ttu-id="3a362-117">(Дополнительные сведения о полях обратного вызова см. в разделе [поля обратного](date-and-time-picker-controls.md)вызова.)</span><span class="sxs-lookup"><span data-stu-id="3a362-117">(For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="3a362-118">Требования</span><span class="sxs-lookup"><span data-stu-id="3a362-118">Requirements</span></span>



| <span data-ttu-id="3a362-119">Требование</span><span class="sxs-lookup"><span data-stu-id="3a362-119">Requirement</span></span> | <span data-ttu-id="3a362-120">Значение</span><span class="sxs-lookup"><span data-stu-id="3a362-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a362-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a362-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3a362-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a362-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a362-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a362-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3a362-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3a362-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a362-125">Header</span><span class="sxs-lookup"><span data-stu-id="3a362-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a362-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a362-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="3a362-127">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="3a362-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3a362-128">**ДТН \_ ФОРМАТКУЕРИВ** (Юникод) и **ДТН \_ форматкуеря** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3a362-128">**DTN\_FORMATQUERYW** (Unicode) and **DTN\_FORMATQUERYA** (ANSI)</span></span><br/>           |



 

 





