---
title: Up-Down элемент управления
description: В этом разделе содержатся сведения об элементах программирования, используемых с элементами управления "вверх-вниз".
ms.assetid: 48c6b4bd-65b4-4388-959e-efffa7658274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8364eb44ee01e27439c82d1d77e674bfb9e3165
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067811"
---
# <a name="up-down-control"></a><span data-ttu-id="603e6-103">Up-Down элемент управления</span><span class="sxs-lookup"><span data-stu-id="603e6-103">Up-Down Control</span></span>

<span data-ttu-id="603e6-104">В этом разделе содержатся сведения об элементах программирования, используемых с элементами управления "вверх-вниз".</span><span class="sxs-lookup"><span data-stu-id="603e6-104">This section contains information about the programming elements used with up-down controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="603e6-105">Разделы общих сведений</span><span class="sxs-lookup"><span data-stu-id="603e6-105">Overviews</span></span>



| <span data-ttu-id="603e6-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="603e6-106">Topic</span></span>                                    | <span data-ttu-id="603e6-107">Содержимое</span><span class="sxs-lookup"><span data-stu-id="603e6-107">Contents</span></span>                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="603e6-108">Элементы управления "вверх/вниз"</span><span class="sxs-lookup"><span data-stu-id="603e6-108">Up-Down Controls</span></span>](up-down-controls.md) | <span data-ttu-id="603e6-109">Элемент управления "вверх-вниз" — это пара кнопок со стрелками, которые пользователь может щелкнуть для увеличения или уменьшения значения, например, для прокрутки или числа, отображаемого в сопровождающем элементе управления (называемом дружественным окном).</span><span class="sxs-lookup"><span data-stu-id="603e6-109">An up-down control is a pair of arrow buttons that the user can click to increment or decrement a value, such as a scroll position or a number displayed in a companion control (called a buddy window).</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="603e6-110">Функции</span><span class="sxs-lookup"><span data-stu-id="603e6-110">Functions</span></span>



| <span data-ttu-id="603e6-111">Раздел</span><span class="sxs-lookup"><span data-stu-id="603e6-111">Topic</span></span>                                              | <span data-ttu-id="603e6-112">Содержимое</span><span class="sxs-lookup"><span data-stu-id="603e6-112">Contents</span></span>                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="603e6-113">**креатеупдовнконтрол**</span><span class="sxs-lookup"><span data-stu-id="603e6-113">**CreateUpDownControl**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-createupdowncontrol) | <span data-ttu-id="603e6-114">Создает элемент управления "вверх-вниз".</span><span class="sxs-lookup"><span data-stu-id="603e6-114">Creates an up-down control.</span></span> <span data-ttu-id="603e6-115">Примечание. Эта функция устарела.</span><span class="sxs-lookup"><span data-stu-id="603e6-115">Note: This function is obsolete.</span></span> <span data-ttu-id="603e6-116">Это 16-разрядная функция, которая не может работать с 32-разрядными значениями для диапазона и расположения.</span><span class="sxs-lookup"><span data-stu-id="603e6-116">It is a 16 bit function and cannot handle 32 bit values for range and position.</span></span><br/> |



 

### <a name="messages"></a><span data-ttu-id="603e6-117">Сообщения</span><span class="sxs-lookup"><span data-stu-id="603e6-117">Messages</span></span>



| <span data-ttu-id="603e6-118">Раздел</span><span class="sxs-lookup"><span data-stu-id="603e6-118">Topic</span></span>                                                 | <span data-ttu-id="603e6-119">Содержимое</span><span class="sxs-lookup"><span data-stu-id="603e6-119">Contents</span></span>                                                                                                                                                                                                                               |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="603e6-120">**\_UDM**</span><span class="sxs-lookup"><span data-stu-id="603e6-120">**UDM\_GETACCEL**</span></span>](udm-getaccel.md)                 | <span data-ttu-id="603e6-121">Получает сведения о ускорении для элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="603e6-121">Retrieves acceleration information for an up-down control.</span></span> <br/>                                                                                                                                                                 |
| [<span data-ttu-id="603e6-122">**\_POLYBASE UDM**</span><span class="sxs-lookup"><span data-stu-id="603e6-122">**UDM\_GETBASE**</span></span>](udm-getbase.md)                   | <span data-ttu-id="603e6-123">Извлекает текущий базовый основание системы счисления (то есть базовый 10 или 16) для элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="603e6-123">Retrieves the current radix base (that is, either base 10 or 16) for an up-down control.</span></span> <br/>                                                                                                                                   |
| [<span data-ttu-id="603e6-124">**взаимоконтакт UDM \_**</span><span class="sxs-lookup"><span data-stu-id="603e6-124">**UDM\_GETBUDDY**</span></span>](udm-getbuddy.md)                 | <span data-ttu-id="603e6-125">Извлекает маркер текущего дружественного окна.</span><span class="sxs-lookup"><span data-stu-id="603e6-125">Retrieves the handle to the current buddy window.</span></span> <br/>                                                                                                                                                                          |
| [<span data-ttu-id="603e6-126">**\_ЖЕТПОС UDM**</span><span class="sxs-lookup"><span data-stu-id="603e6-126">**UDM\_GETPOS**</span></span>](udm-getpos.md)                     | <span data-ttu-id="603e6-127">Извлекает текущее расположение элемента управления "вверх-вниз" с 16-разрядной точностью.</span><span class="sxs-lookup"><span data-stu-id="603e6-127">Retrieves the current position of an up-down control with 16-bit precision.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="603e6-128">**\_GETPOS32 UDM**</span><span class="sxs-lookup"><span data-stu-id="603e6-128">**UDM\_GETPOS32**</span></span>](udm-getpos32.md)                 | <span data-ttu-id="603e6-129">Возвращает 32-разрядное расположение элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="603e6-129">Returns the 32-bit position of an up-down control.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="603e6-130">**многомерный \_ диапазон UDM**</span><span class="sxs-lookup"><span data-stu-id="603e6-130">**UDM\_GETRANGE**</span></span>](udm-getrange.md)                 | <span data-ttu-id="603e6-131">Извлекает минимальные и максимальные позиции (диапазон) для элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="603e6-131">Retrieves the minimum and maximum positions (range) for an up-down control.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="603e6-132">**\_GETRANGE32 UDM**</span><span class="sxs-lookup"><span data-stu-id="603e6-132">**UDM\_GETRANGE32**</span></span>](udm-getrange32.md)             | <span data-ttu-id="603e6-133">Извлекает 32-разрядный диапазон элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="603e6-133">Retrieves the 32-bit range of an up-down control.</span></span> <br/>                                                                                                                                                                          |
| [<span data-ttu-id="603e6-134">**\_ЖЕТУНИКОДЕФОРМАТ UDM**</span><span class="sxs-lookup"><span data-stu-id="603e6-134">**UDM\_GETUNICODEFORMAT**</span></span>](udm-getunicodeformat.md) | <span data-ttu-id="603e6-135">Возвращает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="603e6-135">Retrieves the Unicode character format flag for the control.</span></span> <br/>                                                                                                                                                               |
| [<span data-ttu-id="603e6-136">**\_СЕТАКЦЕЛ UDM**</span><span class="sxs-lookup"><span data-stu-id="603e6-136">**UDM\_SETACCEL**</span></span>](udm-setaccel.md)                 | <span data-ttu-id="603e6-137">Задает ускорение для элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="603e6-137">Sets the acceleration for an up-down control.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="603e6-138">**\_СЕТБАСЕ UDM**</span><span class="sxs-lookup"><span data-stu-id="603e6-138">**UDM\_SETBASE**</span></span>](udm-setbase.md)                   | <span data-ttu-id="603e6-139">Задает основание системы счисления для элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="603e6-139">Sets the radix base for an up-down control.</span></span> <span data-ttu-id="603e6-140">Базовое значение определяет, будут ли в окне собеседника отображаться числа в десятичных или шестнадцатеричных цифрах.</span><span class="sxs-lookup"><span data-stu-id="603e6-140">The base value determines whether the buddy window displays numbers in decimal or hexadecimal digits.</span></span> <span data-ttu-id="603e6-141">Шестнадцатеричные числа всегда являются беззнаковыми, а десятичные числа подписываются.</span><span class="sxs-lookup"><span data-stu-id="603e6-141">Hexadecimal numbers are always unsigned, and decimal numbers are signed.</span></span> <br/> |
| [<span data-ttu-id="603e6-142">**\_СЕТБУДДИ UDM**</span><span class="sxs-lookup"><span data-stu-id="603e6-142">**UDM\_SETBUDDY**</span></span>](udm-setbuddy.md)                 | <span data-ttu-id="603e6-143">Устанавливает окно собеседника для элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="603e6-143">Sets the buddy window for an up-down control.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="603e6-144">**\_СЕТПОС UDM**</span><span class="sxs-lookup"><span data-stu-id="603e6-144">**UDM\_SETPOS**</span></span>](udm-setpos.md)                     | <span data-ttu-id="603e6-145">Задает текущую точку для элемента управления "вверх/вниз" с 16-разрядной точностью.</span><span class="sxs-lookup"><span data-stu-id="603e6-145">Sets the current position for an up-down control with 16-bit precision.</span></span> <br/>                                                                                                                                                    |
| [<span data-ttu-id="603e6-146">**\_SETPOS32 UDM**</span><span class="sxs-lookup"><span data-stu-id="603e6-146">**UDM\_SETPOS32**</span></span>](udm-setpos32.md)                 | <span data-ttu-id="603e6-147">Задает расположение элемента управления "вверх-вниз" с 32-разрядной точностью.</span><span class="sxs-lookup"><span data-stu-id="603e6-147">Sets the position of an up-down control with 32-bit precision.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="603e6-148">**Унифицированная многомерная модель \_**</span><span class="sxs-lookup"><span data-stu-id="603e6-148">**UDM\_SETRANGE**</span></span>](udm-setrange.md)                 | <span data-ttu-id="603e6-149">Задает минимальное и максимальное положение (диапазон) для элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="603e6-149">Sets the minimum and maximum positions (range) for an up-down control.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="603e6-150">**\_SETRANGE32 UDM**</span><span class="sxs-lookup"><span data-stu-id="603e6-150">**UDM\_SETRANGE32**</span></span>](udm-setrange32.md)             | <span data-ttu-id="603e6-151">Задает 32-разрядный диапазон элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="603e6-151">Sets the 32-bit range of an up-down control.</span></span> <br/>                                                                                                                                                                               |
| [<span data-ttu-id="603e6-152">**\_СЕТУНИКОДЕФОРМАТ UDM**</span><span class="sxs-lookup"><span data-stu-id="603e6-152">**UDM\_SETUNICODEFORMAT**</span></span>](udm-setunicodeformat.md) | <span data-ttu-id="603e6-153">Задает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="603e6-153">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="603e6-154">Это сообщение позволяет изменить кодировку, используемую элементом управления во время выполнения, вместо того, чтобы повторно создавать элемент управления.</span><span class="sxs-lookup"><span data-stu-id="603e6-154">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <br/>                                   |



 

### <a name="notifications"></a><span data-ttu-id="603e6-155">Уведомления</span><span class="sxs-lookup"><span data-stu-id="603e6-155">Notifications</span></span>



| <span data-ttu-id="603e6-156">Раздел</span><span class="sxs-lookup"><span data-stu-id="603e6-156">Topic</span></span>                                                            | <span data-ttu-id="603e6-157">Содержимое</span><span class="sxs-lookup"><span data-stu-id="603e6-157">Contents</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="603e6-158">NM \_ релеаседкаптуре (вверх/вниз)</span><span class="sxs-lookup"><span data-stu-id="603e6-158">NM\_RELEASEDCAPTURE (up-down)</span></span>](nm-releasedcapture-up-down-.md) | <span data-ttu-id="603e6-159">Уведомляет родительского окна элемента управления, что элемент управления освобождает захват мыши.</span><span class="sxs-lookup"><span data-stu-id="603e6-159">Notifies an up-down control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="603e6-160">Это уведомление отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="603e6-160">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/>                                                                                                                                                                       |
| [<span data-ttu-id="603e6-161">УДН \_ делтапос</span><span class="sxs-lookup"><span data-stu-id="603e6-161">UDN\_DELTAPOS</span></span>](udn-deltapos.md)                                | <span data-ttu-id="603e6-162">Отправляется операционной системой в родительское окно элемента управления "вверх/вниз", когда изменяется расположение элемента управления.</span><span class="sxs-lookup"><span data-stu-id="603e6-162">Sent by the operating system to the parent window of an up-down control when the position of the control is about to change.</span></span> <span data-ttu-id="603e6-163">Это происходит, когда пользователь запрашивает изменение значения, нажимая клавишу со стрелкой вверх или вниз элемента управления.</span><span class="sxs-lookup"><span data-stu-id="603e6-163">This happens when the user requests a change in the value by pressing the control's up or down arrow.</span></span> <span data-ttu-id="603e6-164">Сообщение [УДН \_ делтапос](udn-deltapos.md) отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="603e6-164">The [UDN\_DELTAPOS](udn-deltapos.md) message is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="603e6-165">Структуры</span><span class="sxs-lookup"><span data-stu-id="603e6-165">Structures</span></span>



| <span data-ttu-id="603e6-166">Раздел</span><span class="sxs-lookup"><span data-stu-id="603e6-166">Topic</span></span>                        | <span data-ttu-id="603e6-167">Содержимое</span><span class="sxs-lookup"><span data-stu-id="603e6-167">Contents</span></span>                                                                                                                                          |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="603e6-168">**нмупдовн**</span><span class="sxs-lookup"><span data-stu-id="603e6-168">**NMUPDOWN**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmupdown) | <span data-ttu-id="603e6-169">Содержит сведения, относящиеся к перекрывающимся уведомлениям элемента управления.</span><span class="sxs-lookup"><span data-stu-id="603e6-169">Contains information specific to up-down control notification messages.</span></span> <span data-ttu-id="603e6-170">Он идентичен и заменяет структуру " **nm" \_** .</span><span class="sxs-lookup"><span data-stu-id="603e6-170">It is identical to and replaces the **NM\_UPDOWN** structure.</span></span> <br/> |
| [<span data-ttu-id="603e6-171">**удакцел**</span><span class="sxs-lookup"><span data-stu-id="603e6-171">**UDACCEL**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)   | <span data-ttu-id="603e6-172">Содержит сведения об ускорении для элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="603e6-172">Contains acceleration information for an up-down control.</span></span> <br/>                                                                             |



 

### <a name="constants"></a><span data-ttu-id="603e6-173">Константы</span><span class="sxs-lookup"><span data-stu-id="603e6-173">Constants</span></span>



| <span data-ttu-id="603e6-174">Раздел</span><span class="sxs-lookup"><span data-stu-id="603e6-174">Topic</span></span>                                                | <span data-ttu-id="603e6-175">Содержимое</span><span class="sxs-lookup"><span data-stu-id="603e6-175">Contents</span></span>                                                                      |
|------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="603e6-176">Стили элементов управления "вверх/вниз"</span><span class="sxs-lookup"><span data-stu-id="603e6-176">Up-Down Control Styles</span></span>](up-down-control-styles.md) | <span data-ttu-id="603e6-177">В этом разделе перечислены стили, используемые при создании элементов управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="603e6-177">This section lists the styles used when creating up-down controls.</span></span><br/> |



 

 

 





