---
title: Сведения об элементах управления IP-адресов
description: Элемент управления IP-адреса позволяет пользователю ввести IP-адрес в удобном для понимания формате.
ms.assetid: cf6a59fc-661c-420a-a67f-a42619946357
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6859bd31250d30bcf26d0c5fde37afeca8cc81bd
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424234"
---
# <a name="about-ip-address-controls"></a><span data-ttu-id="6f1cf-103">Сведения об элементах управления IP-адресов</span><span class="sxs-lookup"><span data-stu-id="6f1cf-103">About IP Address Controls</span></span>

<span data-ttu-id="6f1cf-104">Элемент управления IP-адреса позволяет пользователю ввести IP-адрес в удобном для понимания формате.</span><span class="sxs-lookup"><span data-stu-id="6f1cf-104">An Internet Protocol (IP) address control allows the user to enter an IP address in an easily understood format.</span></span> <span data-ttu-id="6f1cf-105">Этот элемент управления также позволяет приложению получить адрес в виде цифровой формы, а не в виде текста.</span><span class="sxs-lookup"><span data-stu-id="6f1cf-105">This control also allows the application to obtain the address in numeric form rather than in text form.</span></span>

-   [<span data-ttu-id="6f1cf-106">Сведения об элементах управления IP-адресов</span><span class="sxs-lookup"><span data-stu-id="6f1cf-106">About IP Address Controls</span></span>](#about-ip-address-controls)
-   [<span data-ttu-id="6f1cf-107">Создание элемента управления IP-адреса</span><span class="sxs-lookup"><span data-stu-id="6f1cf-107">Creating an IP Address Control</span></span>](#creating-an-ip-address-control)
-   [<span data-ttu-id="6f1cf-108">Является ли IP-адрес элементом управления "поле ввода"?</span><span class="sxs-lookup"><span data-stu-id="6f1cf-108">Is an IP Address Control an Edit Control?</span></span>](#is-an-ip-address-control-an-edit-control)

## <a name="about-ip-address-controls"></a><span data-ttu-id="6f1cf-109">Сведения об элементах управления IP-адресов</span><span class="sxs-lookup"><span data-stu-id="6f1cf-109">About IP Address Controls</span></span>

<span data-ttu-id="6f1cf-110">В Windows Internet Explorer версии 4,0 появился элемент управления "IP-адрес", новый элемент управления, аналогичный элементу управления "поле ввода", который позволяет пользователю вводить числовой адрес в формате протокола Интернета (IP).</span><span class="sxs-lookup"><span data-stu-id="6f1cf-110">Windows Internet Explorer Version 4.0 introduces the IP address control, a new control similar to an edit control that allows the user to enter a numeric address in Internet protocol (IP) format.</span></span> <span data-ttu-id="6f1cf-111">Этот формат состоит из 4 3-разрядных полей.</span><span class="sxs-lookup"><span data-stu-id="6f1cf-111">This format consists of four three-digit fields.</span></span> <span data-ttu-id="6f1cf-112">Каждое поле обрабатывается по отдельности. Номера полей отсчитываются от нуля и продолжаются слева направо, как показано на рисунке.</span><span class="sxs-lookup"><span data-stu-id="6f1cf-112">Each field is treated individually; the field numbers are zero-based and proceed from left to right as shown in this figure.</span></span>

![Диаграмма, показывающая значения в каждом из четырех полей элемента управления IP-адреса](images/ipa-scrn.png)

<span data-ttu-id="6f1cf-114">Элемент управления позволяет указать в каждом из полей только числовой текст.</span><span class="sxs-lookup"><span data-stu-id="6f1cf-114">The control allows only numeric text to be entered in each of the fields.</span></span> <span data-ttu-id="6f1cf-115">После ввода трех цифр в заданное поле фокус клавиатуры автоматически перемещается в следующее поле.</span><span class="sxs-lookup"><span data-stu-id="6f1cf-115">Once three digits have been entered in a given field, keyboard focus is automatically moved to the next field.</span></span> <span data-ttu-id="6f1cf-116">Если заполнение всего поля не требуется приложению, пользователь может ввести меньше трех цифр.</span><span class="sxs-lookup"><span data-stu-id="6f1cf-116">If filling the entire field is not required by the application, the user can enter fewer than three digits.</span></span> <span data-ttu-id="6f1cf-117">Например, если поле должно содержать только цифру двадцать 1, введя «21» и нажав клавишу, пользователь перейдет к следующему полю.</span><span class="sxs-lookup"><span data-stu-id="6f1cf-117">For example, if the field should only contain the number twenty-one, typing "21" and pressing the key will take the user to the next field.</span></span>

<span data-ttu-id="6f1cf-118">По умолчанию для каждого поля используется диапазон от 0 до 255, но приложение может задать диапазону любые значения между этими ограничениями с помощью сообщения [**IPM \_ SETRANGE**](ipm-setrange.md) .</span><span class="sxs-lookup"><span data-stu-id="6f1cf-118">The default range for each field is 0 to 255, but the application can set the range to any values between those limits with the [**IPM\_SETRANGE**](ipm-setrange.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="6f1cf-119">Элемент управления IP-адресов реализован в версии 4,71 и более поздних Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="6f1cf-119">The IP address control is implemented in version 4.71 and later of Comctl32.dll.</span></span>

 

## <a name="creating-an-ip-address-control"></a><span data-ttu-id="6f1cf-120">Создание элемента управления IP-адреса</span><span class="sxs-lookup"><span data-stu-id="6f1cf-120">Creating an IP Address Control</span></span>

<span data-ttu-id="6f1cf-121">Перед созданием элемента управления IP-адресами вызовите [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) с флагом **ICC- \_ \_ классов** , установленным в члене **двикк** структуры [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) .</span><span class="sxs-lookup"><span data-stu-id="6f1cf-121">Before creating an IP address control, call [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) with the **ICC\_INTERNET\_CLASSES** flag set in the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

<span data-ttu-id="6f1cf-122">Для создания элемента управления IP-адреса используйте функцию [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) или [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="6f1cf-122">Use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create an IP address control.</span></span> <span data-ttu-id="6f1cf-123">Имя класса для элемента управления — это [**WC \_ IPAddress**](common-control-window-classes.md), который определен в коммктрл. h.</span><span class="sxs-lookup"><span data-stu-id="6f1cf-123">The class name for the control is [**WC\_IPADDRESS**](common-control-window-classes.md), which is defined in Commctrl.h.</span></span> <span data-ttu-id="6f1cf-124">Стили, относящиеся к контролю IP-адресов, не существуют; Однако, поскольку это дочерний элемент управления, используйте в качестве минимума стиль [**\_ дочернего элемента WS**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="6f1cf-124">No IP address control-specific styles exist; however, because this is a child control, use the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style as a minimum.</span></span>

## <a name="is-an-ip-address-control-an-edit-control"></a><span data-ttu-id="6f1cf-125">Является ли IP-адрес элементом управления "поле ввода"?</span><span class="sxs-lookup"><span data-stu-id="6f1cf-125">Is an IP Address Control an Edit Control?</span></span>

<span data-ttu-id="6f1cf-126">Элемент управления "IP-адрес" не является элементом управления редактированием и не реагирует на \_ сообщения EM.</span><span class="sxs-lookup"><span data-stu-id="6f1cf-126">An IP address control is not an edit control and it will not respond to EM\_ messages.</span></span> <span data-ttu-id="6f1cf-127">Однако окно "владелец" будет отправлять следующие уведомления об изменении элементов управления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="6f1cf-127">It will, however, send the owner window the following edit control notifications through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="6f1cf-128">Обратите внимание, что элемент управления IP-адресов также будет отправлять уведомления частного ИПН \_ через сообщение [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6f1cf-128">Note that the IP address control will also send private IPN\_ notifications through the [**WM\_NOTIFY**](wm-notify.md) message.</span></span>



|     <span data-ttu-id="6f1cf-129">Уведомление</span><span class="sxs-lookup"><span data-stu-id="6f1cf-129">Notification</span></span>                              |     <span data-ttu-id="6f1cf-130">Причина уведомления</span><span class="sxs-lookup"><span data-stu-id="6f1cf-130">Reason for notification</span></span>                                                                                                                                                                                                    |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f1cf-131">" \_ en"</span><span class="sxs-lookup"><span data-stu-id="6f1cf-131">EN\_SETFOCUS</span></span>](en-setfocus.md)   | <span data-ttu-id="6f1cf-132">Посылается, когда элемент управления "IP-адрес" получает фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="6f1cf-132">Sent when the IP address control gains the keyboard focus.</span></span>                                                                                                                                              |
| [<span data-ttu-id="6f1cf-133">EN \_ киллфокус</span><span class="sxs-lookup"><span data-stu-id="6f1cf-133">EN\_KILLFOCUS</span></span>](en-killfocus.md) | <span data-ttu-id="6f1cf-134">Посылается, когда элемент управления "IP-адрес" теряет фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="6f1cf-134">Sent when the IP address control loses the keyboard focus.</span></span>                                                                                                                                              |
| [<span data-ttu-id="6f1cf-135">\_изменение EN</span><span class="sxs-lookup"><span data-stu-id="6f1cf-135">EN\_CHANGE</span></span>](en-change.md)       | <span data-ttu-id="6f1cf-136">Посылается при изменении любого поля в элементе управления IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="6f1cf-136">Sent when any field in the IP address control changes.</span></span> <span data-ttu-id="6f1cf-137">Как и в случае уведомления о [ \_ смене](en-change.md) в стандартном элементе управления "поле ввода", это уведомление будет получено после обновления экрана.</span><span class="sxs-lookup"><span data-stu-id="6f1cf-137">Like the [EN\_CHANGE](en-change.md) notification from a standard edit control, this notification is received after the screen has been updated.</span></span> |



 

 

 