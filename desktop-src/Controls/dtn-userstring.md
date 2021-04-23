---
title: Код уведомления DTN_USERSTRING (Коммктрл. h)
description: Отправляется элементом управления "Выбор даты и времени" (DTP), когда пользователь заканчивает редактирование строки в элементе управления.
ms.assetid: a5b13582-323b-4804-912c-a988d902547d
keywords:
- DTN_USERSTRING кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- DTN_USERSTRING
- DTN_USERSTRINGA
- DTN_USERSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4878875d23a0a5fce95aa4cc9ebfedfbdf24cb93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891561"
---
# <a name="dtn_userstring-notification-code"></a><span data-ttu-id="780a5-104">\_Код уведомления ДТН усерстринг</span><span class="sxs-lookup"><span data-stu-id="780a5-104">DTN\_USERSTRING notification code</span></span>

<span data-ttu-id="780a5-105">Отправляется элементом управления "Выбор даты и времени" (DTP), когда пользователь заканчивает редактирование строки в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="780a5-105">Sent by a date and time picker (DTP) control when a user finishes editing a string in the control.</span></span> <span data-ttu-id="780a5-106">Этот код уведомления отправляется только элементами управления DTP, для которых задан стиль [**\_ Аппканпарсе служб DTS**](date-and-time-picker-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="780a5-106">This notification code is only sent by DTP controls that are set to the [**DTS\_APPCANPARSE**](date-and-time-picker-control-styles.md) style.</span></span> <span data-ttu-id="780a5-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="780a5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_USERSTRING

    lpDTstring = (LPNMDATETIMESTRING) lParam;
```



## <a name="parameters"></a><span data-ttu-id="780a5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="780a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="780a5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="780a5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="780a5-110">Указатель на структуру [**нмдатетиместринг**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) , содержащую сведения об экземпляре кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="780a5-110">A pointer to an [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) structure that contains information about the instance of the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="780a5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="780a5-111">Return value</span></span>

<span data-ttu-id="780a5-112">Владелец элемента управления должен возвращать ноль.</span><span class="sxs-lookup"><span data-stu-id="780a5-112">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="780a5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="780a5-113">Remarks</span></span>

<span data-ttu-id="780a5-114">Обработка этого кода уведомления позволяет владельцу предоставлять пользовательские ответы на строки, которые пользователь вводит в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="780a5-114">Handling this notification code allows the owner to provide custom responses to strings entered into the control by the user.</span></span> <span data-ttu-id="780a5-115">Владелец должен быть подготовлен для анализа входной строки и при необходимости предпринимать необходимые действия.</span><span class="sxs-lookup"><span data-stu-id="780a5-115">The owner must be prepared to parse the input string and take action if necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="780a5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="780a5-116">Requirements</span></span>



| <span data-ttu-id="780a5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="780a5-117">Requirement</span></span> | <span data-ttu-id="780a5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="780a5-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="780a5-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="780a5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="780a5-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="780a5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="780a5-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="780a5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="780a5-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="780a5-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="780a5-123">Header</span><span class="sxs-lookup"><span data-stu-id="780a5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="780a5-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="780a5-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="780a5-125">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="780a5-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="780a5-126">**ДТН \_ УСЕРСТРИНГВ** (Юникод) и **ДТН \_ усерстринга** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="780a5-126">**DTN\_USERSTRINGW** (Unicode) and **DTN\_USERSTRINGA** (ANSI)</span></span><br/>             |



 

 





