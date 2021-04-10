---
title: Код уведомления DTN_WMKEYDOWN (Коммктрл. h)
description: Отправляется элементом управления "Выбор даты и времени" (DTP), когда пользователь вводит в поле обратного вызова. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: e67e222d-28a1-4d30-ae64-8ec9a62fa321
keywords:
- DTN_WMKEYDOWN кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- DTN_WMKEYDOWN
- DTN_WMKEYDOWNA
- DTN_WMKEYDOWNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce2e7d0761308805746278d2f542f5e9458b56d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135295"
---
# <a name="dtn_wmkeydown-notification-code"></a><span data-ttu-id="8cc93-105">\_Код уведомления ДТН вмкэйдовн</span><span class="sxs-lookup"><span data-stu-id="8cc93-105">DTN\_WMKEYDOWN notification code</span></span>

<span data-ttu-id="8cc93-106">Отправляется элементом управления "Выбор даты и времени" (DTP), когда пользователь вводит в поле обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="8cc93-106">Sent by a date and time picker (DTP) control when the user types in a callback field.</span></span> <span data-ttu-id="8cc93-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8cc93-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_WMKEYDOWN

    lpDTKeystroke = (LPNMDATETIMEWMKEYDOWN)lParam;
```



## <a name="parameters"></a><span data-ttu-id="8cc93-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8cc93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cc93-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8cc93-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8cc93-110">Указатель на структуру [**нмдатетимевмкэйдовн**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) , содержащую сведения об этом экземпляре кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="8cc93-110">A pointer to an [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) structure containing information about this instance of the notification code.</span></span> <span data-ttu-id="8cc93-111">Структура включает сведения о ключе, введенном пользователем, подстроке, определяющей поле обратного вызова, а также о текущей системной дате и времени.</span><span class="sxs-lookup"><span data-stu-id="8cc93-111">The structure includes information about the key that the user typed, the substring that defines the callback field, and the current system date and time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cc93-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8cc93-112">Return value</span></span>

<span data-ttu-id="8cc93-113">Владелец элемента управления должен возвращать ноль.</span><span class="sxs-lookup"><span data-stu-id="8cc93-113">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cc93-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8cc93-114">Remarks</span></span>

<span data-ttu-id="8cc93-115">Обработка этого кода уведомления позволяет владельцу элемента управления предоставлять определенные ответы на нажатия клавиш в полях обратного вызова элемента управления.</span><span class="sxs-lookup"><span data-stu-id="8cc93-115">Handling this notification code allows the owner of the control to provide specific responses to keystrokes within the callback fields of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cc93-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8cc93-116">Requirements</span></span>



| <span data-ttu-id="8cc93-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8cc93-117">Requirement</span></span> | <span data-ttu-id="8cc93-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8cc93-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8cc93-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8cc93-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8cc93-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8cc93-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8cc93-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8cc93-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8cc93-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8cc93-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8cc93-123">Header</span><span class="sxs-lookup"><span data-stu-id="8cc93-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cc93-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cc93-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="8cc93-125">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="8cc93-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8cc93-126">**ДТН \_ ВМКЭЙДОВНВ** (Юникод) и **ДТН \_ вмкэйдовна** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8cc93-126">**DTN\_WMKEYDOWNW** (Unicode) and **DTN\_WMKEYDOWNA** (ANSI)</span></span><br/>               |



 

 





