---
title: Управление IP-адресами
description: В этом разделе содержатся сведения об элементах программирования, используемых с элементами управления IP-адресами.
ms.assetid: vs|controls|~\controls\ipaddress\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c80fc87a12ce49038f4c1836e684fa0f8895bd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486697"
---
# <a name="ip-address-control"></a><span data-ttu-id="e86e5-103">Управление IP-адресами</span><span class="sxs-lookup"><span data-stu-id="e86e5-103">IP Address Control</span></span>

<span data-ttu-id="e86e5-104">В этом разделе содержатся сведения об элементах программирования, используемых с элементами управления IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="e86e5-104">This section contains information about the programming elements used with IP address controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="e86e5-105">Разделы общих сведений</span><span class="sxs-lookup"><span data-stu-id="e86e5-105">Overviews</span></span>



| <span data-ttu-id="e86e5-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="e86e5-106">Topic</span></span>                                          | <span data-ttu-id="e86e5-107">Содержимое</span><span class="sxs-lookup"><span data-stu-id="e86e5-107">Contents</span></span>                                                                                                                    |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e86e5-108">Элементы управления IP-адресами</span><span class="sxs-lookup"><span data-stu-id="e86e5-108">IP Address Controls</span></span>](ip-address-controls.md) | <span data-ttu-id="e86e5-109">Элемент управления IP-адреса позволяет пользователю ввести IP-адрес в удобном для понимания формате.</span><span class="sxs-lookup"><span data-stu-id="e86e5-109">An Internet Protocol (IP) address control allows the user to enter an IP address in an easily understood format.</span></span><br/> |



 

### <a name="macros"></a><span data-ttu-id="e86e5-110">Макросы</span><span class="sxs-lookup"><span data-stu-id="e86e5-110">Macros</span></span>



| <span data-ttu-id="e86e5-111">Раздел</span><span class="sxs-lookup"><span data-stu-id="e86e5-111">Topic</span></span>                                         | <span data-ttu-id="e86e5-112">Содержимое</span><span class="sxs-lookup"><span data-stu-id="e86e5-112">Contents</span></span>                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e86e5-113">**ПЕРВЫЙ \_ IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="e86e5-113">**FIRST\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)   | <span data-ttu-id="e86e5-114">Извлекает значение поля 0 из упакованного IP-адреса, полученного с [**\_ сообщением IPM**](ipm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="e86e5-114">Extracts the field 0 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="e86e5-115">**Четвертый \_ IPAddress**</span><span class="sxs-lookup"><span data-stu-id="e86e5-115">**FOURTH\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) | <span data-ttu-id="e86e5-116">Извлекает значение поля 3 из упакованного IP-адреса, полученного с [**\_ сообщением IPM**](ipm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="e86e5-116">Extracts the field 3 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="e86e5-117">**макеипаддресс**</span><span class="sxs-lookup"><span data-stu-id="e86e5-117">**MAKEIPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress)        | <span data-ttu-id="e86e5-118">Упаковывает четыре значения типа Byte в одно значение LPARAM, которое подходит для использования с сообщением [**IPM \_ сетаддресс**](ipm-setaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="e86e5-118">Packs four byte-values into a single LPARAM suitable for use with the [**IPM\_SETADDRESS**](ipm-setaddress.md) message.</span></span> <br/>  |
| [<span data-ttu-id="e86e5-119">**макеипранже**</span><span class="sxs-lookup"><span data-stu-id="e86e5-119">**MAKEIPRANGE**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange)            | <span data-ttu-id="e86e5-120">Упаковывает два байтовых значения в одно значение LPARAM, которое подходит для использования с сообщением [**IPM \_ SETRANGE**](ipm-setrange.md) .</span><span class="sxs-lookup"><span data-stu-id="e86e5-120">Packs two byte-values into a single LPARAM suitable for use with the [**IPM\_SETRANGE**](ipm-setrange.md) message.</span></span> <br/>       |
| [<span data-ttu-id="e86e5-121">**ВТОРОЙ \_ IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="e86e5-121">**SECOND\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress) | <span data-ttu-id="e86e5-122">Извлекает значение поля 1 из упакованного IP-адреса, полученного с [**\_ сообщением IPM**](ipm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="e86e5-122">Extracts the field 1 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="e86e5-123">**Третий \_ IPAddress**</span><span class="sxs-lookup"><span data-stu-id="e86e5-123">**THIRD\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)   | <span data-ttu-id="e86e5-124">Извлекает значение поля 2 из упакованного IP-адреса, полученного с [**\_ сообщением IPM**](ipm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="e86e5-124">Extracts the field 2 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |



 

### <a name="messages"></a><span data-ttu-id="e86e5-125">Сообщения</span><span class="sxs-lookup"><span data-stu-id="e86e5-125">Messages</span></span>



| <span data-ttu-id="e86e5-126">Раздел</span><span class="sxs-lookup"><span data-stu-id="e86e5-126">Topic</span></span>                                         | <span data-ttu-id="e86e5-127">Содержимое</span><span class="sxs-lookup"><span data-stu-id="e86e5-127">Contents</span></span>                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e86e5-128">**\_КЛЕАРАДДРЕСС IPM**</span><span class="sxs-lookup"><span data-stu-id="e86e5-128">**IPM\_CLEARADDRESS**</span></span>](ipm-clearaddress.md) | <span data-ttu-id="e86e5-129">Очищает содержимое элемента управления "IP-адрес".</span><span class="sxs-lookup"><span data-stu-id="e86e5-129">Clears the contents of the IP address control.</span></span> <br/>                                                                            |
| [<span data-ttu-id="e86e5-130">**\_адрес IPM**</span><span class="sxs-lookup"><span data-stu-id="e86e5-130">**IPM\_GETADDRESS**</span></span>](ipm-getaddress.md)     | <span data-ttu-id="e86e5-131">Возвращает значения адреса для всех четырех полей в элементе управления IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="e86e5-131">Gets the address values for all four fields in the IP address control.</span></span> <br/>                                                    |
| [<span data-ttu-id="e86e5-132">**IPM \_**</span><span class="sxs-lookup"><span data-stu-id="e86e5-132">**IPM\_ISBLANK**</span></span>](ipm-isblank.md)           | <span data-ttu-id="e86e5-133">Определяет, являются ли все поля в элементе управления "IP-адрес" пустыми.</span><span class="sxs-lookup"><span data-stu-id="e86e5-133">Determines if all fields in the IP address control are blank.</span></span> <br/>                                                             |
| [<span data-ttu-id="e86e5-134">**\_СЕТАДДРЕСС IPM**</span><span class="sxs-lookup"><span data-stu-id="e86e5-134">**IPM\_SETADDRESS**</span></span>](ipm-setaddress.md)     | <span data-ttu-id="e86e5-135">Задает значения адреса для всех четырех полей в элементе управления "IP-адрес".</span><span class="sxs-lookup"><span data-stu-id="e86e5-135">Sets the address values for all four fields in the IP address control.</span></span> <br/>                                                    |
| [<span data-ttu-id="e86e5-136">**IPM \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="e86e5-136">**IPM\_SETFOCUS**</span></span>](ipm-setfocus.md)         | <span data-ttu-id="e86e5-137">Устанавливает фокус клавиатуры на указанное поле в элементе управления IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="e86e5-137">Sets the keyboard focus to the specified field in the IP address control.</span></span> <span data-ttu-id="e86e5-138">Будет выбран весь текст в этом поле.</span><span class="sxs-lookup"><span data-stu-id="e86e5-138">All of the text in that field will be selected.</span></span> <br/> |
| [<span data-ttu-id="e86e5-139">**IPM \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="e86e5-139">**IPM\_SETRANGE**</span></span>](ipm-setrange.md)         | <span data-ttu-id="e86e5-140">Задает допустимый диапазон для указанного поля в элементе управления IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="e86e5-140">Sets the valid range for the specified field in the IP address control.</span></span> <br/>                                                   |



 

### <a name="notifications"></a><span data-ttu-id="e86e5-141">Уведомления</span><span class="sxs-lookup"><span data-stu-id="e86e5-141">Notifications</span></span>



| <span data-ttu-id="e86e5-142">Раздел</span><span class="sxs-lookup"><span data-stu-id="e86e5-142">Topic</span></span>                                     | <span data-ttu-id="e86e5-143">Содержимое</span><span class="sxs-lookup"><span data-stu-id="e86e5-143">Contents</span></span>                                                                                                                                                                                   |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e86e5-144">ИПН \_ фиелдчанжед</span><span class="sxs-lookup"><span data-stu-id="e86e5-144">IPN\_FIELDCHANGED</span></span>](ipn-fieldchanged.md) | <span data-ttu-id="e86e5-145">Посылается, когда пользователь изменяет поле в элементе управления или перемещается из одного поля в другое.</span><span class="sxs-lookup"><span data-stu-id="e86e5-145">Sent when the user changes a field in the control or moves from one field to another.</span></span> <span data-ttu-id="e86e5-146">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e86e5-146">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="e86e5-147">Структуры</span><span class="sxs-lookup"><span data-stu-id="e86e5-147">Structures</span></span>



| <span data-ttu-id="e86e5-148">Раздел</span><span class="sxs-lookup"><span data-stu-id="e86e5-148">Topic</span></span>                              | <span data-ttu-id="e86e5-149">Содержимое</span><span class="sxs-lookup"><span data-stu-id="e86e5-149">Contents</span></span>                                                                                              |
|------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e86e5-150">**нмипаддресс**</span><span class="sxs-lookup"><span data-stu-id="e86e5-150">**NMIPADDRESS**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) | <span data-ttu-id="e86e5-151">Содержит сведения для кода уведомления [ИПН \_ фиелдчанжед](ipn-fieldchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="e86e5-151">Contains information for the [IPN\_FIELDCHANGED](ipn-fieldchanged.md) notification code.</span></span> <br/> |



 

 

 





