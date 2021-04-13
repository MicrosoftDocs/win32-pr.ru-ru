---
description: Используется для определения частных сообщений, обычно из формы WM \_ app + x, где x — это целочисленное значение.
ms.assetid: fdb549df-426f-4af5-9c17-6e8730e4abc0
title: WM_APP (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4998f8240b08d248a75b375bb813ba02cd02344e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265442"
---
# <a name="wm_app"></a><span data-ttu-id="52266-103">\_приложение WM</span><span class="sxs-lookup"><span data-stu-id="52266-103">WM\_APP</span></span>

<span data-ttu-id="52266-104">Используется для определения частных сообщений, обычно в виде **\_ приложения WM** + *x*, где *x* — это целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="52266-104">Used to define private messages, usually of the form **WM\_APP**+*x*, where *x* is an integer value.</span></span>

``` syntax
#define WM_APP                          0x8000
```

## <a name="remarks"></a><span data-ttu-id="52266-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52266-105">Remarks</span></span>

<span data-ttu-id="52266-106">Константа **\_ приложения WM** используется для различения значений сообщений, зарезервированных для использования системой, и значений, которые могут использоваться приложением для отправки сообщений в закрытом классе окна.</span><span class="sxs-lookup"><span data-stu-id="52266-106">The **WM\_APP** constant is used to distinguish between message values that are reserved for use by the system and values that can be used by an application to send messages within a private window class.</span></span> <span data-ttu-id="52266-107">Ниже приведены диапазоны доступных номеров сообщений.</span><span class="sxs-lookup"><span data-stu-id="52266-107">The following are the ranges of message numbers available.</span></span>



| <span data-ttu-id="52266-108">Диапазон</span><span class="sxs-lookup"><span data-stu-id="52266-108">Range</span></span>                                                 | <span data-ttu-id="52266-109">Значение</span><span class="sxs-lookup"><span data-stu-id="52266-109">Meaning</span></span>                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="52266-110">от 0 до [**WM \_ User**](wm-user.md) – 1</span><span class="sxs-lookup"><span data-stu-id="52266-110">0 through [**WM\_USER**](wm-user.md) –1</span></span><br/>   | <span data-ttu-id="52266-111">Сообщения, зарезервированные для использования системой.</span><span class="sxs-lookup"><span data-stu-id="52266-111">Messages reserved for use by the system.</span></span><br/>            |
| <span data-ttu-id="52266-112">[**WM \_ ПОЛЬЗОВАТЕЛЬ**](wm-user.md) с помощью 0x7FFF</span><span class="sxs-lookup"><span data-stu-id="52266-112">[**WM\_USER**](wm-user.md) through 0x7FFF</span></span><br/> | <span data-ttu-id="52266-113">Целочисленные сообщения для использования классами закрытых окон.</span><span class="sxs-lookup"><span data-stu-id="52266-113">Integer messages for use by private window classes.</span></span><br/> |
| <span data-ttu-id="52266-114">**WM \_ ПРИЛОЖЕНИЕ** через 0xBFFF</span><span class="sxs-lookup"><span data-stu-id="52266-114">**WM\_APP** through 0xBFFF</span></span><br/>                 | <span data-ttu-id="52266-115">Сообщения, доступные для использования приложениями.</span><span class="sxs-lookup"><span data-stu-id="52266-115">Messages available for use by applications.</span></span><br/>         |
| <span data-ttu-id="52266-116">0xC000 до 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="52266-116">0xC000 through 0xFFFF</span></span><br/>                      | <span data-ttu-id="52266-117">Строковые сообщения для использования приложениями.</span><span class="sxs-lookup"><span data-stu-id="52266-117">String messages for use by applications.</span></span><br/>            |
| <span data-ttu-id="52266-118">Больше 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="52266-118">Greater than 0xFFFF</span></span><br/>                        | <span data-ttu-id="52266-119">Зарезервировано системой.</span><span class="sxs-lookup"><span data-stu-id="52266-119">Reserved by the system.</span></span><br/>                             |



 

<span data-ttu-id="52266-120">Номера сообщений в первом диапазоне (от 0 до [**WM \_ User**](wm-user.md) -1) определяются системой.</span><span class="sxs-lookup"><span data-stu-id="52266-120">Message numbers in the first range (0 through [**WM\_USER**](wm-user.md) –1) are defined by the system.</span></span> <span data-ttu-id="52266-121">Значения в этом диапазоне, которые не определены явно, зарезервированы системой.</span><span class="sxs-lookup"><span data-stu-id="52266-121">Values in this range that are not explicitly defined are reserved by the system.</span></span>

<span data-ttu-id="52266-122">Номера сообщений во втором диапазоне ([**\_ пользователь WM**](wm-user.md) с помощью 0x7FFF) можно определить и использовать в приложении для отправки сообщений в закрытом классе окна.</span><span class="sxs-lookup"><span data-stu-id="52266-122">Message numbers in the second range ([**WM\_USER**](wm-user.md) through 0x7FFF) can be defined and used by an application to send messages within a private window class.</span></span> <span data-ttu-id="52266-123">Эти значения нельзя использовать для определения сообщений, которые являются значимыми для приложения, поскольку некоторые предопределенные классы окон уже определяют значения в этом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="52266-123">These values cannot be used to define messages that are meaningful throughout an application because some predefined window classes already define values in this range.</span></span> <span data-ttu-id="52266-124">Например, эти значения могут использоваться в стандартных классах элементов управления, таких как **кнопка**, **Правка**, **ListBox** и **поле со списком** .</span><span class="sxs-lookup"><span data-stu-id="52266-124">For example, predefined control classes such as **BUTTON**, **EDIT**, **LISTBOX**, and **COMBOBOX** may use these values.</span></span> <span data-ttu-id="52266-125">Сообщения в этом диапазоне не должны отправляться другим приложениям, если только приложения не предназначены для обмена сообщениями и для прикрепления одного и того же значения к номерам сообщений.</span><span class="sxs-lookup"><span data-stu-id="52266-125">Messages in this range should not be sent to other applications unless the applications have been designed to exchange messages and to attach the same meaning to the message numbers.</span></span>

<span data-ttu-id="52266-126">Номера сообщений в третьем диапазоне (от 0x8000 до 0xBFFF) доступны для использования приложениями в качестве частных сообщений.</span><span class="sxs-lookup"><span data-stu-id="52266-126">Message numbers in the third range (0x8000 through 0xBFFF) are available for applications to use as private messages.</span></span> <span data-ttu-id="52266-127">Сообщения в этом диапазоне не конфликтуют с системными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="52266-127">Messages in this range do not conflict with system messages.</span></span>

<span data-ttu-id="52266-128">Номера сообщений в четвертом диапазоне (0xC000 до 0xFFFF) определяются во время выполнения, когда приложение вызывает функцию [**регистервиндовмессаже**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) для получения номера сообщения для строки.</span><span class="sxs-lookup"><span data-stu-id="52266-128">Message numbers in the fourth range (0xC000 through 0xFFFF) are defined at run time when an application calls the [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) function to retrieve a message number for a string.</span></span> <span data-ttu-id="52266-129">Все приложения, которые регистрируют одну и ту же строку, могут использовать соответствующий номер сообщения для обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="52266-129">All applications that register the same string can use the associated message number for exchanging messages.</span></span> <span data-ttu-id="52266-130">Однако фактический номер сообщения не является константой и не может быть одинаковым в разных сеансах.</span><span class="sxs-lookup"><span data-stu-id="52266-130">The actual message number, however, is not a constant and cannot be assumed to be the same between different sessions.</span></span>

<span data-ttu-id="52266-131">Номера сообщений в пятом диапазоне (больше 0xFFFF) зарезервированы системой.</span><span class="sxs-lookup"><span data-stu-id="52266-131">Message numbers in the fifth range (greater than 0xFFFF) are reserved by the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="52266-132">Требования</span><span class="sxs-lookup"><span data-stu-id="52266-132">Requirements</span></span>



| <span data-ttu-id="52266-133">Требование</span><span class="sxs-lookup"><span data-stu-id="52266-133">Requirement</span></span> | <span data-ttu-id="52266-134">Значение</span><span class="sxs-lookup"><span data-stu-id="52266-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52266-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52266-135">Minimum supported client</span></span><br/> | <span data-ttu-id="52266-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="52266-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="52266-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52266-137">Minimum supported server</span></span><br/> | <span data-ttu-id="52266-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="52266-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="52266-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="52266-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="52266-140"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52266-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52266-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52266-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="52266-142">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="52266-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="52266-143">**регистервиндовмессаже**</span><span class="sxs-lookup"><span data-stu-id="52266-143">**RegisterWindowMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="52266-144">**\_пользователь WM**</span><span class="sxs-lookup"><span data-stu-id="52266-144">**WM\_USER**</span></span>](wm-user.md)
</dt> <dt>

<span data-ttu-id="52266-145">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="52266-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="52266-146">Сообщения и очереди сообщений</span><span class="sxs-lookup"><span data-stu-id="52266-146">Messages and Message Queues</span></span>](messages-and-message-queues.md)
</dt> </dl>

 

 
