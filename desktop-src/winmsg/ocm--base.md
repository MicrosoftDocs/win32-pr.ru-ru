---
description: Используется для определения частных сообщений для использования закрытыми классами окон, обычно в виде OCM \_ \_ base + x, где x — это целочисленное значение.
ms.assetid: b1a9c0ca-349d-49d2-9b8b-ae7d3bf94c10
title: OCM__BASE (Олектл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa3713d8a7b7447430e914e2582089244a417b1c
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2021
ms.locfileid: "112588054"
---
# <a name="ocm__base"></a><span data-ttu-id="163f5-103">\_ \_ базовый OCM</span><span class="sxs-lookup"><span data-stu-id="163f5-103">OCM\_\_BASE</span></span>

<span data-ttu-id="163f5-104">Используется для определения частных сообщений для использования закрытыми классами окон, обычно в виде **OCM \_ \_ base** + *x*, где *x* — это целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="163f5-104">Used to define private messages for use by private window classes, usually of the form **OCM\_\_BASE**+*x*, where *x* is an integer value.</span></span>

``` syntax
#define WM_USER                   0x0400
#define OCM__BASE                (WM_USER+0x1c00)
```

## <a name="remarks"></a><span data-ttu-id="163f5-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="163f5-105">Remarks</span></span>

<span data-ttu-id="163f5-106">Ниже приведены диапазоны номеров сообщений.</span><span class="sxs-lookup"><span data-stu-id="163f5-106">The following are the ranges of message numbers.</span></span>



| <span data-ttu-id="163f5-107">Диапазон</span><span class="sxs-lookup"><span data-stu-id="163f5-107">Range</span></span>                                                 | <span data-ttu-id="163f5-108">Значение</span><span class="sxs-lookup"><span data-stu-id="163f5-108">Meaning</span></span>                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="163f5-109">от 0 до [**WM \_ User**](wm-user.md)-1</span><span class="sxs-lookup"><span data-stu-id="163f5-109">0 through [**WM\_USER**](wm-user.md)-1</span></span><br/>   | <span data-ttu-id="163f5-110">Сообщения, зарезервированные для использования системой.</span><span class="sxs-lookup"><span data-stu-id="163f5-110">Messages reserved for use by the system.</span></span><br/>            |
| <span data-ttu-id="163f5-111">[**WM \_ ПОЛЬЗОВАТЕЛЬ**](wm-user.md) с помощью 0x7FFF</span><span class="sxs-lookup"><span data-stu-id="163f5-111">[**WM\_USER**](wm-user.md) through 0x7FFF</span></span><br/> | <span data-ttu-id="163f5-112">Целочисленные сообщения для использования классами закрытых окон.</span><span class="sxs-lookup"><span data-stu-id="163f5-112">Integer messages for use by private window classes.</span></span><br/> |
| <span data-ttu-id="163f5-113">[**WM \_ ПРИЛОЖЕНИЕ**](wm-app.md) через 0xBFFF</span><span class="sxs-lookup"><span data-stu-id="163f5-113">[**WM\_APP**](wm-app.md) through 0xBFFF</span></span><br/>   | <span data-ttu-id="163f5-114">Сообщения, доступные для использования приложениями.</span><span class="sxs-lookup"><span data-stu-id="163f5-114">Messages available for use by applications.</span></span><br/>         |
| <span data-ttu-id="163f5-115">0xC000 до 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="163f5-115">0xC000 through 0xFFFF</span></span><br/>                      | <span data-ttu-id="163f5-116">Строковые сообщения для использования приложениями.</span><span class="sxs-lookup"><span data-stu-id="163f5-116">String messages for use by applications.</span></span><br/>            |
| <span data-ttu-id="163f5-117">Больше 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="163f5-117">Greater than 0xFFFF</span></span><br/>                        | <span data-ttu-id="163f5-118">Зарезервировано системой.</span><span class="sxs-lookup"><span data-stu-id="163f5-118">Reserved by the system.</span></span><br/>                             |



 

<span data-ttu-id="163f5-119">Номера сообщений в первом диапазоне (от 0 до [**WM \_ User**](wm-user.md)  1) определяются системой.</span><span class="sxs-lookup"><span data-stu-id="163f5-119">Message numbers in the first range (0 through [**WM\_USER**](wm-user.md)  1) are defined by the system.</span></span> <span data-ttu-id="163f5-120">Значения в этом диапазоне, которые не определены явно, зарезервированы системой.</span><span class="sxs-lookup"><span data-stu-id="163f5-120">Values in this range that are not explicitly defined are reserved by the system.</span></span>

<span data-ttu-id="163f5-121">Номера сообщений во втором диапазоне ([**\_ пользователь WM**](wm-user.md) с помощью 0x7FFF) можно определить и использовать в приложении для отправки сообщений в закрытом классе окна.</span><span class="sxs-lookup"><span data-stu-id="163f5-121">Message numbers in the second range ([**WM\_USER**](wm-user.md) through 0x7FFF) can be defined and used by an application to send messages within a private window class.</span></span> <span data-ttu-id="163f5-122">Эти значения нельзя использовать для определения сообщений, которые являются значимыми для приложения, поскольку некоторые предопределенные классы окон уже определяют значения в этом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="163f5-122">These values cannot be used to define messages that are meaningful throughout an application because some predefined window classes already define values in this range.</span></span> <span data-ttu-id="163f5-123">Например, эти значения могут использоваться в стандартных классах элементов управления, таких как **кнопка**, **Правка**, **ListBox** и **поле со списком** .</span><span class="sxs-lookup"><span data-stu-id="163f5-123">For example, predefined control classes such as **BUTTON**, **EDIT**, **LISTBOX**, and **COMBOBOX** may use these values.</span></span> <span data-ttu-id="163f5-124">Сообщения в этом диапазоне не должны отправляться другим приложениям, если только приложения не предназначены для обмена сообщениями и для прикрепления одного и того же значения к номерам сообщений.</span><span class="sxs-lookup"><span data-stu-id="163f5-124">Messages in this range should not be sent to other applications unless the applications have been designed to exchange messages and to attach the same meaning to the message numbers.</span></span>

<span data-ttu-id="163f5-125">Номера сообщений в третьем диапазоне (от 0x8000 до 0xBFFF) доступны для использования приложениями в качестве частных сообщений.</span><span class="sxs-lookup"><span data-stu-id="163f5-125">Message numbers in the third range (0x8000 through 0xBFFF) are available for applications to use as private messages.</span></span> <span data-ttu-id="163f5-126">Сообщения в этом диапазоне не конфликтуют с системными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="163f5-126">Messages in this range do not conflict with system messages.</span></span>

<span data-ttu-id="163f5-127">Номера сообщений в четвертом диапазоне (0xC000 до 0xFFFF) определяются во время выполнения, когда приложение вызывает функцию [**регистервиндовмессаже**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) для получения номера сообщения для строки.</span><span class="sxs-lookup"><span data-stu-id="163f5-127">Message numbers in the fourth range (0xC000 through 0xFFFF) are defined at run time when an application calls the [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) function to retrieve a message number for a string.</span></span> <span data-ttu-id="163f5-128">Все приложения, которые регистрируют одну и ту же строку, могут использовать соответствующий номер сообщения для обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="163f5-128">All applications that register the same string can use the associated message number for exchanging messages.</span></span> <span data-ttu-id="163f5-129">Однако фактический номер сообщения не является константой и не может быть одинаковым в разных сеансах.</span><span class="sxs-lookup"><span data-stu-id="163f5-129">The actual message number, however, is not a constant and cannot be assumed to be the same between different sessions.</span></span>

<span data-ttu-id="163f5-130">Номера сообщений в пятом диапазоне (больше 0xFFFF) зарезервированы системой.</span><span class="sxs-lookup"><span data-stu-id="163f5-130">Message numbers in the fifth range (greater than 0xFFFF) are reserved by the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="163f5-131">Требования</span><span class="sxs-lookup"><span data-stu-id="163f5-131">Requirements</span></span>



| <span data-ttu-id="163f5-132">Требование</span><span class="sxs-lookup"><span data-stu-id="163f5-132">Requirement</span></span> | <span data-ttu-id="163f5-133">Значение</span><span class="sxs-lookup"><span data-stu-id="163f5-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="163f5-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="163f5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="163f5-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="163f5-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="163f5-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="163f5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="163f5-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="163f5-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="163f5-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="163f5-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="163f5-139"><dt>Олектл. h</dt></span><span class="sxs-lookup"><span data-stu-id="163f5-139"><dt>Olectl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="163f5-140">См. также</span><span class="sxs-lookup"><span data-stu-id="163f5-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="163f5-141">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="163f5-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="163f5-142">**регистервиндовмессаже**</span><span class="sxs-lookup"><span data-stu-id="163f5-142">**RegisterWindowMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="163f5-143">**\_приложение WM**</span><span class="sxs-lookup"><span data-stu-id="163f5-143">**WM\_APP**</span></span>](wm-app.md)
</dt> <dt>

<span data-ttu-id="163f5-144">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="163f5-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="163f5-145">Сообщения и очереди сообщений</span><span class="sxs-lookup"><span data-stu-id="163f5-145">Messages and Message Queues</span></span>](messages-and-message-queues.md)
</dt> </dl>

 

