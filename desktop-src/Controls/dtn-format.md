---
title: Код уведомления DTN_FORMAT (Коммктрл. h)
description: Отправляется элементом управления "Выбор даты и времени" (DTP) для запроса текста, отображаемого в поле обратного вызова. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: ce0ee230-638e-425f-9f34-c379342cea93
keywords:
- DTN_FORMAT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- DTN_FORMAT
- DTN_FORMATA
- DTN_FORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fadd11b090777d2226eeed85f32d2062e8340e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491526"
---
# <a name="dtn_format-notification-code"></a><span data-ttu-id="3d789-105">\_Код уведомления формата ДТН</span><span class="sxs-lookup"><span data-stu-id="3d789-105">DTN\_FORMAT notification code</span></span>

<span data-ttu-id="3d789-106">Отправляется элементом управления "Выбор даты и времени" (DTP) для запроса текста, отображаемого в поле обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="3d789-106">Sent by a date and time picker (DTP) control to request text to be displayed in a callback field.</span></span> <span data-ttu-id="3d789-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3d789-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_FORMAT

    lpNMFormat = (LPNMDATETIMEFORMAT) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3d789-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d789-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d789-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d789-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d789-110">Указатель на структуру [**нмдатетимеформат**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata) , содержащую сведения об этом экземпляре кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="3d789-110">A pointer to an [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata) structure containing information regarding this instance of the notification code.</span></span> <span data-ttu-id="3d789-111">Структура содержит подстроку, определяющую поле обратного вызова, и получает форматированную строку, которую будет отображать элемент управления.</span><span class="sxs-lookup"><span data-stu-id="3d789-111">The structure contains the substring that defines the callback field and receives the formatted string that the control will display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d789-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d789-112">Return value</span></span>

<span data-ttu-id="3d789-113">Владелец элемента управления должен возвращать ноль.</span><span class="sxs-lookup"><span data-stu-id="3d789-113">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d789-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d789-114">Remarks</span></span>

<span data-ttu-id="3d789-115">Обработка этого кода уведомления позволяет владельцу элемента управления предоставить пользовательскую строку, которую будет отображать элемент управления.</span><span class="sxs-lookup"><span data-stu-id="3d789-115">Handling this notification code allows the owner of the control to provide a custom string that the control will display.</span></span> <span data-ttu-id="3d789-116">(Дополнительные сведения о полях обратного вызова см. в разделе [поля обратного](date-and-time-picker-controls.md)вызова.)</span><span class="sxs-lookup"><span data-stu-id="3d789-116">(For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="3d789-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3d789-117">Requirements</span></span>



| <span data-ttu-id="3d789-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3d789-118">Requirement</span></span> | <span data-ttu-id="3d789-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3d789-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d789-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d789-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3d789-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3d789-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3d789-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d789-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3d789-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3d789-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3d789-124">Header</span><span class="sxs-lookup"><span data-stu-id="3d789-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d789-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d789-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="3d789-126">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="3d789-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3d789-127">**ДТН \_ ФОРМАТВ** (Юникод) и **\_ Формат ДТН** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3d789-127">**DTN\_FORMATW** (Unicode) and **DTN\_FORMATA** (ANSI)</span></span><br/>                     |



 

 





