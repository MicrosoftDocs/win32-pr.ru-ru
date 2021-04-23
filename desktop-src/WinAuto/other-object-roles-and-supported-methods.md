---
title: Другие роли объектов и поддерживаемые методы (Справочник по элементам пользовательского интерфейса MSAA)
description: В этом разделе содержатся сведения о ролях объектов, которые не включены в предыдущие разделы для элементов пользовательского интерфейса.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3d7fbdbb6dfbf83729f3e1c1d4caa3027f8d51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792919"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a><span data-ttu-id="a45d1-103">Другие роли объектов и поддерживаемые методы (Справочник по элементам пользовательского интерфейса MSAA)</span><span class="sxs-lookup"><span data-stu-id="a45d1-103">Other Object Roles and Supported Methods (MSAA UI Element Reference)</span></span>

<span data-ttu-id="a45d1-104">В этом разделе содержатся сведения о ролях объектов, которые не включены в предыдущие разделы для элементов пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a45d1-104">This topic provides information about object roles that are not included in the previous topics for UI elements.</span></span> <span data-ttu-id="a45d1-105">Каждая роль объекта включает список методов и свойств [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , поддерживаемых для роли объекта.</span><span class="sxs-lookup"><span data-stu-id="a45d1-105">Each object role includes a list of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties that are supported for the object role.</span></span> <span data-ttu-id="a45d1-106">Другие разделы содержат поддерживаемые методы и свойства методов **IAccessible** для элементов пользовательского интерфейса. в этом разделе перечислены методы и свойства, которые можно использовать для конкретной роли объекта.</span><span class="sxs-lookup"><span data-stu-id="a45d1-106">While other topics document supported **IAccessible** methods and properties for UI elements, this topic lists the methods and properties you can expect to be supported for a particular object role.</span></span> <span data-ttu-id="a45d1-107">Многие элементы пользовательского интерфейса, которые могут иметь одну из перечисленных здесь ролей, обычно отображаются в браузерах.</span><span class="sxs-lookup"><span data-stu-id="a45d1-107">Many of the UI elements which might have one of the roles listed here are typically seen in browsers.</span></span>

> [!Note]  
> <span data-ttu-id="a45d1-108">Используйте этот раздел в качестве рекомендации.</span><span class="sxs-lookup"><span data-stu-id="a45d1-108">Use this topic as a guideline.</span></span> <span data-ttu-id="a45d1-109">Настоятельно рекомендуется использовать средства Microsoft Active Accessibility для проверки ожидаемого поведения отдельной роли объекта.</span><span class="sxs-lookup"><span data-stu-id="a45d1-109">We strongly suggest that you use Microsoft Active Accessibility tools to verify expected behavior for an individual object role.</span></span>

 

<span data-ttu-id="a45d1-110">В следующей таблице перечислены дополнительные роли объектов, которые Oleacc.dll поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="a45d1-110">The following table lists additional object roles which Oleacc.dll supports.</span></span>



|                                                                         |                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="a45d1-111">**\_ \_ оповещение системы роли**</span><span class="sxs-lookup"><span data-stu-id="a45d1-111">**ROLE\_SYSTEM\_ALERT**</span></span>](/windows)                           | [<span data-ttu-id="a45d1-112">**\_дроплист системы \_ ролей**</span><span class="sxs-lookup"><span data-stu-id="a45d1-112">**ROLE\_SYSTEM\_DROPLIST**</span></span>](/windows)       |
| [<span data-ttu-id="a45d1-113">**\_системное \_ приложение роли**</span><span class="sxs-lookup"><span data-stu-id="a45d1-113">**ROLE\_SYSTEM\_APPLICATION**</span></span>](/windows)               | [<span data-ttu-id="a45d1-114">**\_ \_ уравнение системы роли**</span><span class="sxs-lookup"><span data-stu-id="a45d1-114">**ROLE\_SYSTEM\_EQUATION**</span></span>](/windows)       |
| [<span data-ttu-id="a45d1-115">**\_граница системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="a45d1-115">**ROLE\_SYSTEM\_BORDER**</span></span>](/windows)                         | [<span data-ttu-id="a45d1-116">**\_график системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="a45d1-116">**ROLE\_SYSTEM\_GRAPHIC**</span></span>](/windows)         |
| [<span data-ttu-id="a45d1-117">**\_буттондропдовн системы \_ ролей**</span><span class="sxs-lookup"><span data-stu-id="a45d1-117">**ROLE\_SYSTEM\_BUTTONDROPDOWN**</span></span>](/windows)         | [<span data-ttu-id="a45d1-118">**\_хелпбаллун системы \_ ролей**</span><span class="sxs-lookup"><span data-stu-id="a45d1-118">**ROLE\_SYSTEM\_HELPBALLOON**</span></span>](/windows) |
| [<span data-ttu-id="a45d1-119">**\_буттондропдовнгрид системы \_ ролей**</span><span class="sxs-lookup"><span data-stu-id="a45d1-119">**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**</span></span>](/windows) | [<span data-ttu-id="a45d1-120">**\_IP- \_ адрес системы роли**</span><span class="sxs-lookup"><span data-stu-id="a45d1-120">**ROLE\_SYSTEM\_IPADDRESS**</span></span>](/windows)     |
| [<span data-ttu-id="a45d1-121">**\_буттонмену системы \_ ролей**</span><span class="sxs-lookup"><span data-stu-id="a45d1-121">**ROLE\_SYSTEM\_BUTTONMENU**</span></span>](/windows)                 | [<span data-ttu-id="a45d1-122">**\_ссылка на систему роли \_**</span><span class="sxs-lookup"><span data-stu-id="a45d1-122">**ROLE\_SYSTEM\_LINK**</span></span>](/windows)               |
| [<span data-ttu-id="a45d1-123">**\_системная \_ ЯЧЕЙКа роли**</span><span class="sxs-lookup"><span data-stu-id="a45d1-123">**ROLE\_SYSTEM\_CELL**</span></span>](/windows)                             | [<span data-ttu-id="a45d1-124">**\_область системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="a45d1-124">**ROLE\_SYSTEM\_PANE**</span></span>](/windows)               |
| [<span data-ttu-id="a45d1-125">**\_системный \_ символ роли**</span><span class="sxs-lookup"><span data-stu-id="a45d1-125">**ROLE\_SYSTEM\_CHARACTER**</span></span>](/windows)                   | [<span data-ttu-id="a45d1-126">**\_строка системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="a45d1-126">**ROLE\_SYSTEM\_ROW**</span></span>](/windows)                 |
| [<span data-ttu-id="a45d1-127">**\_системная \_ Диаграмма роли**</span><span class="sxs-lookup"><span data-stu-id="a45d1-127">**ROLE\_SYSTEM\_CHART**</span></span>](/windows)                           | [<span data-ttu-id="a45d1-128">**\_ровхеадер системы \_ ролей**</span><span class="sxs-lookup"><span data-stu-id="a45d1-128">**ROLE\_SYSTEM\_ROWHEADER**</span></span>](/windows)     |
| [<span data-ttu-id="a45d1-129">**\_системные \_ Часы для ролей**</span><span class="sxs-lookup"><span data-stu-id="a45d1-129">**ROLE\_SYSTEM\_CLOCK**</span></span>](/windows)                           | [<span data-ttu-id="a45d1-130">**\_Разделитель системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="a45d1-130">**ROLE\_SYSTEM\_SEPARATOR**</span></span>](/windows)     |
| [<span data-ttu-id="a45d1-131">**\_системный \_ столбец роли**</span><span class="sxs-lookup"><span data-stu-id="a45d1-131">**ROLE\_SYSTEM\_COLUMN**</span></span>](/windows)                         | [<span data-ttu-id="a45d1-132">**\_системный \_ звук роли**</span><span class="sxs-lookup"><span data-stu-id="a45d1-132">**ROLE\_SYSTEM\_SOUND**</span></span>](/windows)             |
| [<span data-ttu-id="a45d1-133">**\_Схема системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="a45d1-133">**ROLE\_SYSTEM\_DIAGRAM**</span></span>](/windows)                       | [<span data-ttu-id="a45d1-134">**\_SPLITBUTTON системы \_ ролей**</span><span class="sxs-lookup"><span data-stu-id="a45d1-134">**ROLE\_SYSTEM\_SPLITBUTTON**</span></span>](/windows) |
| [<span data-ttu-id="a45d1-135">**\_вызов системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="a45d1-135">**ROLE\_SYSTEM\_DIAL**</span></span>](/windows)                             | [<span data-ttu-id="a45d1-136">**\_системная \_ Таблица ролей**</span><span class="sxs-lookup"><span data-stu-id="a45d1-136">**ROLE\_SYSTEM\_TABLE**</span></span>](/windows)             |
| [<span data-ttu-id="a45d1-137">**\_документ системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="a45d1-137">**ROLE\_SYSTEM\_DOCUMENT**</span></span>](/windows)                     | [<span data-ttu-id="a45d1-138">**\_пробел в системе роли \_**</span><span class="sxs-lookup"><span data-stu-id="a45d1-138">**ROLE\_SYSTEM\_WHITESPACE**</span></span>](/windows)   |



 

## <a name="role_system_alert"></a><span data-ttu-id="a45d1-139">\_ \_ оповещение системы роли</span><span class="sxs-lookup"><span data-stu-id="a45d1-139">ROLE\_SYSTEM\_ALERT</span></span>

<span data-ttu-id="a45d1-140">Дополнительные сведения об этой роли см. в [**разделе \_ \_ предупреждение системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-140">For more information on this role, see [**ROLE\_SYSTEM\_ALERT**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-141">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-141">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-142">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-142">get\_accName</span></span>
-   <span data-ttu-id="a45d1-143">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-143">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-144">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-144">get\_accState</span></span>

## <a name="role_system_application"></a><span data-ttu-id="a45d1-145">\_системное \_ приложение роли</span><span class="sxs-lookup"><span data-stu-id="a45d1-145">ROLE\_SYSTEM\_APPLICATION</span></span>

<span data-ttu-id="a45d1-146">Дополнительные сведения об этой роли см. в [**разделе \_ \_ приложение системы ролей**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-146">For more information on this role, see [**ROLE\_SYSTEM\_APPLICATION**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-147">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-147">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-148">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-148">accHitTest</span></span>
-   <span data-ttu-id="a45d1-149">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-149">accLocation</span></span>
-   <span data-ttu-id="a45d1-150">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-150">accNavigate</span></span>
-   <span data-ttu-id="a45d1-151">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="a45d1-151">get\_accChild</span></span>
-   <span data-ttu-id="a45d1-152">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="a45d1-152">get\_accChildCount</span></span>
-   <span data-ttu-id="a45d1-153">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-153">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-154">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="a45d1-154">get\_accHelp</span></span>
-   <span data-ttu-id="a45d1-155">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="a45d1-155">get\_accHelpTopic</span></span>
-   <span data-ttu-id="a45d1-156">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="a45d1-156">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="a45d1-157">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-157">get\_accName</span></span>
-   <span data-ttu-id="a45d1-158">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-158">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-159">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-159">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-160">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-160">get\_accState</span></span>

## <a name="role_system_border"></a><span data-ttu-id="a45d1-161">\_граница системы \_ роли</span><span class="sxs-lookup"><span data-stu-id="a45d1-161">ROLE\_SYSTEM\_BORDER</span></span>

<span data-ttu-id="a45d1-162">Дополнительные сведения об этой роли см. в [**разделе \_ \_ граница системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-162">For more information on this role, see [**ROLE\_SYSTEM\_BORDER**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-163">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-163">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-164">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-164">accHitTest</span></span>
-   <span data-ttu-id="a45d1-165">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-165">accLocation</span></span>
-   <span data-ttu-id="a45d1-166">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-166">accNavigate</span></span>
-   <span data-ttu-id="a45d1-167">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-167">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-168">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-168">get\_accState</span></span>

## <a name="role_system_buttondropdown"></a><span data-ttu-id="a45d1-169">\_буттондропдовн системы \_ ролей</span><span class="sxs-lookup"><span data-stu-id="a45d1-169">ROLE\_SYSTEM\_BUTTONDROPDOWN</span></span>

<span data-ttu-id="a45d1-170">Дополнительные сведения об этой роли см. в разделе [**Role \_ System \_ буттондропдовн**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-170">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWN**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-171">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-171">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-172">аккдодефаултактион</span><span class="sxs-lookup"><span data-stu-id="a45d1-172">accDoDefaultAction</span></span>
-   <span data-ttu-id="a45d1-173">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-173">accHitTest</span></span>
-   <span data-ttu-id="a45d1-174">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-174">accLocation</span></span>
-   <span data-ttu-id="a45d1-175">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-175">accNavigate</span></span>
-   <span data-ttu-id="a45d1-176">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="a45d1-176">get\_accChild</span></span>
-   <span data-ttu-id="a45d1-177">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="a45d1-177">get\_accChildCount</span></span>
-   <span data-ttu-id="a45d1-178">получить \_ аккдефаултактион</span><span class="sxs-lookup"><span data-stu-id="a45d1-178">get\_accDefaultAction</span></span>
-   <span data-ttu-id="a45d1-179">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-179">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-180">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="a45d1-180">get\_accHelp</span></span>
-   <span data-ttu-id="a45d1-181">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="a45d1-181">get\_accHelpTopic</span></span>
-   <span data-ttu-id="a45d1-182">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="a45d1-182">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="a45d1-183">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-183">get\_accName</span></span>
-   <span data-ttu-id="a45d1-184">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-184">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-185">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-185">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-186">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-186">get\_accState</span></span>

## <a name="role_system_buttondropdowngrid"></a><span data-ttu-id="a45d1-187">\_буттондропдовнгрид системы \_ ролей</span><span class="sxs-lookup"><span data-stu-id="a45d1-187">ROLE\_SYSTEM\_BUTTONDROPDOWNGRID</span></span>

<span data-ttu-id="a45d1-188">Дополнительные сведения об этой роли см. в разделе [**Role \_ System \_ буттондропдовнгрид**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-188">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-189">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-189">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-190">аккдодефаултактион</span><span class="sxs-lookup"><span data-stu-id="a45d1-190">accDoDefaultAction</span></span>
-   <span data-ttu-id="a45d1-191">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-191">accHitTest</span></span>
-   <span data-ttu-id="a45d1-192">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-192">accLocation</span></span>
-   <span data-ttu-id="a45d1-193">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-193">accNavigate</span></span>
-   <span data-ttu-id="a45d1-194">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="a45d1-194">get\_accChild</span></span>
-   <span data-ttu-id="a45d1-195">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="a45d1-195">get\_accChildCount</span></span>
-   <span data-ttu-id="a45d1-196">получить \_ аккдефаултактион</span><span class="sxs-lookup"><span data-stu-id="a45d1-196">get\_accDefaultAction</span></span>
-   <span data-ttu-id="a45d1-197">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-197">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-198">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="a45d1-198">get\_accHelp</span></span>
-   <span data-ttu-id="a45d1-199">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="a45d1-199">get\_accHelpTopic</span></span>
-   <span data-ttu-id="a45d1-200">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="a45d1-200">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="a45d1-201">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-201">get\_accName</span></span>
-   <span data-ttu-id="a45d1-202">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-202">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-203">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-203">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-204">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-204">get\_accState</span></span>

## <a name="role_system_buttonmenu"></a><span data-ttu-id="a45d1-205">\_буттонмену системы \_ ролей</span><span class="sxs-lookup"><span data-stu-id="a45d1-205">ROLE\_SYSTEM\_BUTTONMENU</span></span>

<span data-ttu-id="a45d1-206">Дополнительные сведения об этой роли см. в разделе [**Role \_ System \_ буттонмену**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-206">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONMENU**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-207">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-207">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-208">аккдодефаултактион</span><span class="sxs-lookup"><span data-stu-id="a45d1-208">accDoDefaultAction</span></span>
-   <span data-ttu-id="a45d1-209">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-209">accHitTest</span></span>
-   <span data-ttu-id="a45d1-210">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-210">accLocation</span></span>
-   <span data-ttu-id="a45d1-211">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-211">accNavigate</span></span>
-   <span data-ttu-id="a45d1-212">получить \_ аккдефаултактион</span><span class="sxs-lookup"><span data-stu-id="a45d1-212">get\_accDefaultAction</span></span>
-   <span data-ttu-id="a45d1-213">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-213">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-214">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="a45d1-214">get\_accHelp</span></span>
-   <span data-ttu-id="a45d1-215">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="a45d1-215">get\_accHelpTopic</span></span>
-   <span data-ttu-id="a45d1-216">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="a45d1-216">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="a45d1-217">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-217">get\_accName</span></span>
-   <span data-ttu-id="a45d1-218">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-218">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-219">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-219">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-220">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-220">get\_accState</span></span>

## <a name="role_system_cell"></a><span data-ttu-id="a45d1-221">\_системная \_ ЯЧЕЙКа роли</span><span class="sxs-lookup"><span data-stu-id="a45d1-221">ROLE\_SYSTEM\_CELL</span></span>

<span data-ttu-id="a45d1-222">Дополнительные сведения об этой роли см. в статье [**роль \_ системной \_ ячейки**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-222">For more information on this role, see [**ROLE\_SYSTEM\_CELL**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-223">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-223">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-224">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-224">accHitTest</span></span>
-   <span data-ttu-id="a45d1-225">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-225">accLocation</span></span>
-   <span data-ttu-id="a45d1-226">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-226">accNavigate</span></span>
-   <span data-ttu-id="a45d1-227">аккселект</span><span class="sxs-lookup"><span data-stu-id="a45d1-227">accSelect</span></span>
-   <span data-ttu-id="a45d1-228">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="a45d1-228">get\_accChild</span></span>
-   <span data-ttu-id="a45d1-229">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="a45d1-229">get\_accChildCount</span></span>
-   <span data-ttu-id="a45d1-230">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-230">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-231">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="a45d1-231">get\_accHelp</span></span>
-   <span data-ttu-id="a45d1-232">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="a45d1-232">get\_accHelpTopic</span></span>
-   <span data-ttu-id="a45d1-233">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="a45d1-233">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="a45d1-234">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-234">get\_accName</span></span>
-   <span data-ttu-id="a45d1-235">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-235">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-236">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-236">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-237">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-237">get\_accState</span></span>
-   <span data-ttu-id="a45d1-238">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="a45d1-238">get\_accValue</span></span>

## <a name="role_system_character"></a><span data-ttu-id="a45d1-239">\_системный \_ символ роли</span><span class="sxs-lookup"><span data-stu-id="a45d1-239">ROLE\_SYSTEM\_CHARACTER</span></span>

<span data-ttu-id="a45d1-240">Дополнительные сведения об этой роли см. в [**разделе \_ системный \_ символ роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-240">For more information on this role, see [**ROLE\_SYSTEM\_CHARACTER**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-241">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-241">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-242">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-242">accHitTest</span></span>
-   <span data-ttu-id="a45d1-243">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-243">accLocation</span></span>
-   <span data-ttu-id="a45d1-244">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-244">accNavigate</span></span>
-   <span data-ttu-id="a45d1-245">получить \_ аккдескриптион</span><span class="sxs-lookup"><span data-stu-id="a45d1-245">get\_accDescription</span></span>
-   <span data-ttu-id="a45d1-246">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-246">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-247">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="a45d1-247">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="a45d1-248">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-248">get\_accName</span></span>
-   <span data-ttu-id="a45d1-249">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-249">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-250">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-250">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-251">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-251">get\_accState</span></span>
-   <span data-ttu-id="a45d1-252">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="a45d1-252">get\_accValue</span></span>

## <a name="role_system_chart"></a><span data-ttu-id="a45d1-253">\_системная \_ Диаграмма роли</span><span class="sxs-lookup"><span data-stu-id="a45d1-253">ROLE\_SYSTEM\_CHART</span></span>

<span data-ttu-id="a45d1-254">Дополнительные сведения об этой роли см. в [**разделе \_ \_ Диаграмма системы ролей**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-254">For more information on this role, see [**ROLE\_SYSTEM\_CHART**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-255">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-255">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-256">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-256">accHitTest</span></span>
-   <span data-ttu-id="a45d1-257">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-257">accLocation</span></span>
-   <span data-ttu-id="a45d1-258">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-258">accNavigate</span></span>
-   <span data-ttu-id="a45d1-259">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="a45d1-259">get\_accChild</span></span>
-   <span data-ttu-id="a45d1-260">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="a45d1-260">get\_accChildCount</span></span>
-   <span data-ttu-id="a45d1-261">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-261">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-262">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="a45d1-262">get\_accHelp</span></span>
-   <span data-ttu-id="a45d1-263">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="a45d1-263">get\_accHelpTopic</span></span>
-   <span data-ttu-id="a45d1-264">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="a45d1-264">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="a45d1-265">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-265">get\_accName</span></span>
-   <span data-ttu-id="a45d1-266">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-266">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-267">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-267">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-268">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-268">get\_accState</span></span>

## <a name="role_system_clock"></a><span data-ttu-id="a45d1-269">\_системные \_ Часы для ролей</span><span class="sxs-lookup"><span data-stu-id="a45d1-269">ROLE\_SYSTEM\_CLOCK</span></span>

<span data-ttu-id="a45d1-270">Дополнительные сведения об этой роли см. в [**разделе \_ системные \_ часы системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-270">For more information on this role, see [**ROLE\_SYSTEM\_CLOCK**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-271">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-271">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-272">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-272">accHitTest</span></span>
-   <span data-ttu-id="a45d1-273">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-273">accLocation</span></span>
-   <span data-ttu-id="a45d1-274">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-274">accNavigate</span></span>
-   <span data-ttu-id="a45d1-275">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-275">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-276">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="a45d1-276">get\_accHelp</span></span>
-   <span data-ttu-id="a45d1-277">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="a45d1-277">get\_accHelpTopic</span></span>
-   <span data-ttu-id="a45d1-278">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="a45d1-278">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="a45d1-279">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-279">get\_accName</span></span>
-   <span data-ttu-id="a45d1-280">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-280">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-281">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-281">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-282">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-282">get\_accState</span></span>
-   <span data-ttu-id="a45d1-283">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="a45d1-283">get\_accValue</span></span>

## <a name="role_system_column"></a><span data-ttu-id="a45d1-284">\_системный \_ столбец роли</span><span class="sxs-lookup"><span data-stu-id="a45d1-284">ROLE\_SYSTEM\_COLUMN</span></span>

<span data-ttu-id="a45d1-285">Дополнительные сведения об этой роли см. в [**разделе \_ \_ столбец системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-285">For more information on this role, see [**ROLE\_SYSTEM\_COLUMN**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-286">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-286">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-287">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-287">accHitTest</span></span>
-   <span data-ttu-id="a45d1-288">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-288">accLocation</span></span>
-   <span data-ttu-id="a45d1-289">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-289">accNavigate</span></span>
-   <span data-ttu-id="a45d1-290">аккселект</span><span class="sxs-lookup"><span data-stu-id="a45d1-290">accSelect</span></span>
-   <span data-ttu-id="a45d1-291">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="a45d1-291">get\_accChild</span></span>
-   <span data-ttu-id="a45d1-292">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="a45d1-292">get\_accChildCount</span></span>
-   <span data-ttu-id="a45d1-293">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-293">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-294">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-294">get\_accName</span></span>
-   <span data-ttu-id="a45d1-295">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-295">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-296">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-296">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-297">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-297">get\_accState</span></span>
-   <span data-ttu-id="a45d1-298">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="a45d1-298">get\_accValue</span></span>

## <a name="role_system_diagram"></a><span data-ttu-id="a45d1-299">\_Схема системы \_ роли</span><span class="sxs-lookup"><span data-stu-id="a45d1-299">ROLE\_SYSTEM\_DIAGRAM</span></span>

<span data-ttu-id="a45d1-300">Дополнительные сведения об этой роли см. в [**разделе \_ \_ Схема системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-300">For more information on this role, see [**ROLE\_SYSTEM\_DIAGRAM**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-301">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-301">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-302">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-302">accHitTest</span></span>
-   <span data-ttu-id="a45d1-303">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-303">accLocation</span></span>
-   <span data-ttu-id="a45d1-304">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-304">accNavigate</span></span>
-   <span data-ttu-id="a45d1-305">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="a45d1-305">get\_accChild</span></span>
-   <span data-ttu-id="a45d1-306">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="a45d1-306">get\_accChildCount</span></span>
-   <span data-ttu-id="a45d1-307">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-307">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-308">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="a45d1-308">get\_accHelp</span></span>
-   <span data-ttu-id="a45d1-309">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="a45d1-309">get\_accHelpTopic</span></span>
-   <span data-ttu-id="a45d1-310">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="a45d1-310">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="a45d1-311">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-311">get\_accName</span></span>
-   <span data-ttu-id="a45d1-312">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-312">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-313">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-313">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-314">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-314">get\_accState</span></span>

## <a name="role_system_dial"></a><span data-ttu-id="a45d1-315">\_вызов системы \_ роли</span><span class="sxs-lookup"><span data-stu-id="a45d1-315">ROLE\_SYSTEM\_DIAL</span></span>

<span data-ttu-id="a45d1-316">Дополнительные сведения об этой роли см. в разделе [**Role \_ System \_ Dialin**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-316">For more information on this role, see [**ROLE\_SYSTEM\_DIAL**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-317">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-317">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-318">аккдодефаултактион</span><span class="sxs-lookup"><span data-stu-id="a45d1-318">accDoDefaultAction</span></span>
-   <span data-ttu-id="a45d1-319">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-319">accHitTest</span></span>
-   <span data-ttu-id="a45d1-320">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-320">accLocation</span></span>
-   <span data-ttu-id="a45d1-321">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-321">accNavigate</span></span>
-   <span data-ttu-id="a45d1-322">получить \_ аккдефаултактион</span><span class="sxs-lookup"><span data-stu-id="a45d1-322">get\_accDefaultAction</span></span>
-   <span data-ttu-id="a45d1-323">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-323">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-324">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="a45d1-324">get\_accHelp</span></span>
-   <span data-ttu-id="a45d1-325">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="a45d1-325">get\_accHelpTopic</span></span>
-   <span data-ttu-id="a45d1-326">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="a45d1-326">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="a45d1-327">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-327">get\_accName</span></span>
-   <span data-ttu-id="a45d1-328">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-328">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-329">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-329">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-330">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-330">get\_accState</span></span>
-   <span data-ttu-id="a45d1-331">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="a45d1-331">get\_accValue</span></span>

## <a name="role_system_document"></a><span data-ttu-id="a45d1-332">\_документ системы \_ роли</span><span class="sxs-lookup"><span data-stu-id="a45d1-332">ROLE\_SYSTEM\_DOCUMENT</span></span>

<span data-ttu-id="a45d1-333">Дополнительные сведения об этой роли см. в [**разделе \_ \_ документ системы ролей**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-333">For more information on this role, see [**ROLE\_SYSTEM\_DOCUMENT**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-334">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-334">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-335">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-335">accHitTest</span></span>
-   <span data-ttu-id="a45d1-336">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-336">accLocation</span></span>
-   <span data-ttu-id="a45d1-337">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-337">accNavigate</span></span>
-   <span data-ttu-id="a45d1-338">аккселект</span><span class="sxs-lookup"><span data-stu-id="a45d1-338">accSelect</span></span>
-   <span data-ttu-id="a45d1-339">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="a45d1-339">get\_accChild</span></span>
-   <span data-ttu-id="a45d1-340">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="a45d1-340">get\_accChildCount</span></span>
-   <span data-ttu-id="a45d1-341">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-341">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-342">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-342">get\_accName</span></span>
-   <span data-ttu-id="a45d1-343">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-343">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-344">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-344">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-345">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-345">get\_accState</span></span>

## <a name="role_system_droplist"></a><span data-ttu-id="a45d1-346">\_дроплист системы \_ ролей</span><span class="sxs-lookup"><span data-stu-id="a45d1-346">ROLE\_SYSTEM\_DROPLIST</span></span>

<span data-ttu-id="a45d1-347">Дополнительные сведения об этой роли см. в разделе [**Role \_ System \_ дроплист**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-347">For more information on this role, see [**ROLE\_SYSTEM\_DROPLIST**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-348">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-348">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-349">аккдодефаултактион</span><span class="sxs-lookup"><span data-stu-id="a45d1-349">accDoDefaultAction</span></span>
-   <span data-ttu-id="a45d1-350">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-350">accHitTest</span></span>
-   <span data-ttu-id="a45d1-351">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-351">accLocation</span></span>
-   <span data-ttu-id="a45d1-352">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-352">accNavigate</span></span>
-   <span data-ttu-id="a45d1-353">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="a45d1-353">get\_accChild</span></span>
-   <span data-ttu-id="a45d1-354">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="a45d1-354">get\_accChildCount</span></span>
-   <span data-ttu-id="a45d1-355">получить \_ аккдефаултактион</span><span class="sxs-lookup"><span data-stu-id="a45d1-355">get\_accDefaultAction</span></span>
-   <span data-ttu-id="a45d1-356">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-356">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-357">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="a45d1-357">get\_accHelp</span></span>
-   <span data-ttu-id="a45d1-358">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="a45d1-358">get\_accHelpTopic</span></span>
-   <span data-ttu-id="a45d1-359">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="a45d1-359">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="a45d1-360">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-360">get\_accName</span></span>
-   <span data-ttu-id="a45d1-361">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-361">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-362">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-362">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-363">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-363">get\_accState</span></span>

## <a name="role_system_equation"></a><span data-ttu-id="a45d1-364">\_ \_ уравнение системы роли</span><span class="sxs-lookup"><span data-stu-id="a45d1-364">ROLE\_SYSTEM\_EQUATION</span></span>

<span data-ttu-id="a45d1-365">Дополнительные сведения об этой роли см. в [**разделе \_ \_ уравнение системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-365">For more information on this role, see [**ROLE\_SYSTEM\_EQUATION**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-366">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-366">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-367">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-367">accHitTest</span></span>
-   <span data-ttu-id="a45d1-368">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-368">accLocation</span></span>
-   <span data-ttu-id="a45d1-369">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-369">accNavigate</span></span>
-   <span data-ttu-id="a45d1-370">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-370">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-371">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-371">get\_accName</span></span>
-   <span data-ttu-id="a45d1-372">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-372">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-373">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-373">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-374">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-374">get\_accState</span></span>
-   <span data-ttu-id="a45d1-375">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="a45d1-375">get\_accValue</span></span>

## <a name="role_system_graphic"></a><span data-ttu-id="a45d1-376">\_график системы \_ роли</span><span class="sxs-lookup"><span data-stu-id="a45d1-376">ROLE\_SYSTEM\_GRAPHIC</span></span>

<span data-ttu-id="a45d1-377">Дополнительные сведения об этой роли см. в [**разделе \_ \_ график системы ролей**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-377">For more information on this role, see [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-378">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-378">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-379">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-379">accHitTest</span></span>
-   <span data-ttu-id="a45d1-380">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-380">accLocation</span></span>
-   <span data-ttu-id="a45d1-381">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-381">accNavigate</span></span>
-   <span data-ttu-id="a45d1-382">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-382">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-383">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="a45d1-383">get\_accHelp</span></span>
-   <span data-ttu-id="a45d1-384">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="a45d1-384">get\_accHelpTopic</span></span>
-   <span data-ttu-id="a45d1-385">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="a45d1-385">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="a45d1-386">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-386">get\_accName</span></span>
-   <span data-ttu-id="a45d1-387">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-387">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-388">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-388">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-389">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-389">get\_accState</span></span>

## <a name="role_system_helpballoon"></a><span data-ttu-id="a45d1-390">\_хелпбаллун системы \_ ролей</span><span class="sxs-lookup"><span data-stu-id="a45d1-390">ROLE\_SYSTEM\_HELPBALLOON</span></span>

<span data-ttu-id="a45d1-391">Дополнительные сведения об этой роли см. в разделе [**Role \_ System \_ хелпбаллун**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-391">For more information on this role, see [**ROLE\_SYSTEM\_HELPBALLOON**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-392">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-392">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-393">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-393">accHitTest</span></span>
-   <span data-ttu-id="a45d1-394">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-394">accLocation</span></span>
-   <span data-ttu-id="a45d1-395">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-395">accNavigate</span></span>
-   <span data-ttu-id="a45d1-396">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="a45d1-396">get\_accChild</span></span>
-   <span data-ttu-id="a45d1-397">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="a45d1-397">get\_accChildCount</span></span>
-   <span data-ttu-id="a45d1-398">получить \_ аккдефаултактион</span><span class="sxs-lookup"><span data-stu-id="a45d1-398">get\_accDefaultAction</span></span>
-   <span data-ttu-id="a45d1-399">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-399">get\_accName</span></span>
-   <span data-ttu-id="a45d1-400">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-400">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-401">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-401">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-402">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-402">get\_accState</span></span>
-   <span data-ttu-id="a45d1-403">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="a45d1-403">get\_accValue</span></span>

## <a name="role_system_ipaddress"></a><span data-ttu-id="a45d1-404">\_IP- \_ адрес системы роли</span><span class="sxs-lookup"><span data-stu-id="a45d1-404">ROLE\_SYSTEM\_IPADDRESS</span></span>

<span data-ttu-id="a45d1-405">Дополнительные сведения об этой роли см. в [**разделе \_ \_ IP-адрес системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-405">For more information on this role, see [**ROLE\_SYSTEM\_IPADDRESS**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-406">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-406">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-407">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-407">accHitTest</span></span>
-   <span data-ttu-id="a45d1-408">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-408">accLocation</span></span>
-   <span data-ttu-id="a45d1-409">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-409">accNavigate</span></span>
-   <span data-ttu-id="a45d1-410">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="a45d1-410">get\_accChild</span></span>
-   <span data-ttu-id="a45d1-411">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="a45d1-411">get\_accChildCount</span></span>
-   <span data-ttu-id="a45d1-412">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-412">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-413">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="a45d1-413">get\_accHelp</span></span>
-   <span data-ttu-id="a45d1-414">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="a45d1-414">get\_accHelpTopic</span></span>
-   <span data-ttu-id="a45d1-415">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="a45d1-415">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="a45d1-416">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-416">get\_accName</span></span>
-   <span data-ttu-id="a45d1-417">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-417">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-418">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-418">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-419">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-419">get\_accState</span></span>
-   <span data-ttu-id="a45d1-420">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="a45d1-420">get\_accValue</span></span>

## <a name="role_system_link"></a><span data-ttu-id="a45d1-421">\_ссылка на систему роли \_</span><span class="sxs-lookup"><span data-stu-id="a45d1-421">ROLE\_SYSTEM\_LINK</span></span>

<span data-ttu-id="a45d1-422">Дополнительные сведения об этой роли см. в [**разделе \_ \_ ссылка на систему роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-422">For more information on this role, see [**ROLE\_SYSTEM\_LINK**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-423">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-423">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-424">аккдодефаултактион</span><span class="sxs-lookup"><span data-stu-id="a45d1-424">accDoDefaultAction</span></span>
-   <span data-ttu-id="a45d1-425">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-425">accHitTest</span></span>
-   <span data-ttu-id="a45d1-426">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-426">accLocation</span></span>
-   <span data-ttu-id="a45d1-427">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-427">accNavigate</span></span>
-   <span data-ttu-id="a45d1-428">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="a45d1-428">get\_accChild</span></span>
-   <span data-ttu-id="a45d1-429">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="a45d1-429">get\_accChildCount</span></span>
-   <span data-ttu-id="a45d1-430">получить \_ аккдефаултактион</span><span class="sxs-lookup"><span data-stu-id="a45d1-430">get\_accDefaultAction</span></span>
-   <span data-ttu-id="a45d1-431">получить \_ аккдескриптион</span><span class="sxs-lookup"><span data-stu-id="a45d1-431">get\_accDescription</span></span>
-   <span data-ttu-id="a45d1-432">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-432">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-433">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="a45d1-433">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="a45d1-434">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-434">get\_accName</span></span>
-   <span data-ttu-id="a45d1-435">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-435">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-436">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-436">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-437">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-437">get\_accState</span></span>
-   <span data-ttu-id="a45d1-438">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="a45d1-438">get\_accValue</span></span>

## <a name="role_system_pane"></a><span data-ttu-id="a45d1-439">\_область системы \_ роли</span><span class="sxs-lookup"><span data-stu-id="a45d1-439">ROLE\_SYSTEM\_PANE</span></span>

<span data-ttu-id="a45d1-440">Дополнительные сведения об этой роли см. в [**разделе \_ \_ область системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-440">For more information on this role, see [**ROLE\_SYSTEM\_PANE**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-441">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-441">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-442">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-442">accHitTest</span></span>
-   <span data-ttu-id="a45d1-443">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-443">accLocation</span></span>
-   <span data-ttu-id="a45d1-444">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-444">accNavigate</span></span>
-   <span data-ttu-id="a45d1-445">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="a45d1-445">get\_accChild</span></span>
-   <span data-ttu-id="a45d1-446">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="a45d1-446">get\_accChildCount</span></span>
-   <span data-ttu-id="a45d1-447">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-447">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-448">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="a45d1-448">get\_accHelp</span></span>
-   <span data-ttu-id="a45d1-449">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="a45d1-449">get\_accHelpTopic</span></span>
-   <span data-ttu-id="a45d1-450">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="a45d1-450">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="a45d1-451">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-451">get\_accName</span></span>
-   <span data-ttu-id="a45d1-452">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-452">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-453">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-453">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-454">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-454">get\_accState</span></span>

## <a name="role_system_row"></a><span data-ttu-id="a45d1-455">\_строка системы \_ роли</span><span class="sxs-lookup"><span data-stu-id="a45d1-455">ROLE\_SYSTEM\_ROW</span></span>

<span data-ttu-id="a45d1-456">Дополнительные сведения об этой роли см. в [**разделе \_ \_ строка системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-456">For more information on this role, see [**ROLE\_SYSTEM\_ROW**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-457">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-457">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-458">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-458">accHitTest</span></span>
-   <span data-ttu-id="a45d1-459">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-459">accLocation</span></span>
-   <span data-ttu-id="a45d1-460">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-460">accNavigate</span></span>
-   <span data-ttu-id="a45d1-461">аккселект</span><span class="sxs-lookup"><span data-stu-id="a45d1-461">accSelect</span></span>
-   <span data-ttu-id="a45d1-462">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="a45d1-462">get\_accChild</span></span>
-   <span data-ttu-id="a45d1-463">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="a45d1-463">get\_accChildCount</span></span>
-   <span data-ttu-id="a45d1-464">получить \_ аккдескриптион</span><span class="sxs-lookup"><span data-stu-id="a45d1-464">get\_accDescription</span></span>
-   <span data-ttu-id="a45d1-465">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-465">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-466">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-466">get\_accName</span></span>
-   <span data-ttu-id="a45d1-467">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-467">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-468">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-468">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-469">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-469">get\_accState</span></span>
-   <span data-ttu-id="a45d1-470">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="a45d1-470">get\_accValue</span></span>

## <a name="role_system_rowheader"></a><span data-ttu-id="a45d1-471">\_ровхеадер системы \_ ролей</span><span class="sxs-lookup"><span data-stu-id="a45d1-471">ROLE\_SYSTEM\_ROWHEADER</span></span>

<span data-ttu-id="a45d1-472">Дополнительные сведения об этой роли см. в разделе [**Role \_ System \_ ровхеадер**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-472">For more information on this role, see [**ROLE\_SYSTEM\_ROWHEADER**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-473">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-473">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-474">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-474">accHitTest</span></span>
-   <span data-ttu-id="a45d1-475">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-475">accLocation</span></span>
-   <span data-ttu-id="a45d1-476">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-476">accNavigate</span></span>
-   <span data-ttu-id="a45d1-477">аккселект</span><span class="sxs-lookup"><span data-stu-id="a45d1-477">accSelect</span></span>
-   <span data-ttu-id="a45d1-478">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="a45d1-478">get\_accChild</span></span>
-   <span data-ttu-id="a45d1-479">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="a45d1-479">get\_accChildCount</span></span>
-   <span data-ttu-id="a45d1-480">получить \_ аккдефаултактион</span><span class="sxs-lookup"><span data-stu-id="a45d1-480">get\_accDefaultAction</span></span>
-   <span data-ttu-id="a45d1-481">получить \_ аккдескриптион</span><span class="sxs-lookup"><span data-stu-id="a45d1-481">get\_accDescription</span></span>
-   <span data-ttu-id="a45d1-482">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-482">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-483">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-483">get\_accName</span></span>
-   <span data-ttu-id="a45d1-484">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-484">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-485">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-485">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-486">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-486">get\_accState</span></span>
-   <span data-ttu-id="a45d1-487">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="a45d1-487">get\_accValue</span></span>

## <a name="role_system_separator"></a><span data-ttu-id="a45d1-488">\_Разделитель системы \_ роли</span><span class="sxs-lookup"><span data-stu-id="a45d1-488">ROLE\_SYSTEM\_SEPARATOR</span></span>

<span data-ttu-id="a45d1-489">Дополнительные сведения об этой роли см. в [**статье \_ \_ Разделитель системы ролей**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-489">For more information on this role, see [**ROLE\_SYSTEM\_SEPARATOR**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-490">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-490">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-491">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-491">accHitTest</span></span>
-   <span data-ttu-id="a45d1-492">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-492">accLocation</span></span>
-   <span data-ttu-id="a45d1-493">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="a45d1-493">get\_accChild</span></span>
-   <span data-ttu-id="a45d1-494">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="a45d1-494">get\_accChildCount</span></span>
-   <span data-ttu-id="a45d1-495">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-495">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-496">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-496">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-497">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-497">get\_accState</span></span>

## <a name="role_system_sound"></a><span data-ttu-id="a45d1-498">\_системный \_ звук роли</span><span class="sxs-lookup"><span data-stu-id="a45d1-498">ROLE\_SYSTEM\_SOUND</span></span>

<span data-ttu-id="a45d1-499">Дополнительные сведения об этой роли см. в [**разделе \_ системный \_ звук роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-499">For more information on this role, see [**ROLE\_SYSTEM\_SOUND**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-500">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-500">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-501">получить \_ аккдескриптион</span><span class="sxs-lookup"><span data-stu-id="a45d1-501">get\_accDescription</span></span>
-   <span data-ttu-id="a45d1-502">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-502">get\_accName</span></span>
-   <span data-ttu-id="a45d1-503">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-503">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-504">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-504">get\_accState</span></span>

## <a name="role_system_splitbutton"></a><span data-ttu-id="a45d1-505">\_SPLITBUTTON системы \_ ролей</span><span class="sxs-lookup"><span data-stu-id="a45d1-505">ROLE\_SYSTEM\_SPLITBUTTON</span></span>

<span data-ttu-id="a45d1-506">Дополнительные сведения об этой роли см. в [**разделе \_ \_ SPLITBUTTON системы ролей**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-506">For more information on this role, see [**ROLE\_SYSTEM\_SPLITBUTTON**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-507">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-507">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-508">аккдодефаултактион</span><span class="sxs-lookup"><span data-stu-id="a45d1-508">accDoDefaultAction</span></span>
-   <span data-ttu-id="a45d1-509">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-509">accHitTest</span></span>
-   <span data-ttu-id="a45d1-510">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-510">accLocation</span></span>
-   <span data-ttu-id="a45d1-511">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-511">accNavigate</span></span>
-   <span data-ttu-id="a45d1-512">получить \_ аккдефаултактион</span><span class="sxs-lookup"><span data-stu-id="a45d1-512">get\_accDefaultAction</span></span>
-   <span data-ttu-id="a45d1-513">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="a45d1-513">get\_accHelp</span></span>
-   <span data-ttu-id="a45d1-514">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="a45d1-514">get\_accHelpTopic</span></span>
-   <span data-ttu-id="a45d1-515">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="a45d1-515">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="a45d1-516">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-516">get\_accName</span></span>
-   <span data-ttu-id="a45d1-517">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-517">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-518">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-518">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-519">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-519">get\_accState</span></span>

## <a name="role_system_table"></a><span data-ttu-id="a45d1-520">\_системная \_ Таблица ролей</span><span class="sxs-lookup"><span data-stu-id="a45d1-520">ROLE\_SYSTEM\_TABLE</span></span>

<span data-ttu-id="a45d1-521">Дополнительные сведения об этой роли см. в [**разделе \_ системная \_ Таблица ролей**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-521">For more information on this role, see [**ROLE\_SYSTEM\_TABLE**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-522">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-522">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-523">акчиттест</span><span class="sxs-lookup"><span data-stu-id="a45d1-523">accHitTest</span></span>
-   <span data-ttu-id="a45d1-524">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-524">accLocation</span></span>
-   <span data-ttu-id="a45d1-525">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="a45d1-525">accNavigate</span></span>
-   <span data-ttu-id="a45d1-526">аккселект</span><span class="sxs-lookup"><span data-stu-id="a45d1-526">accSelect</span></span>
-   <span data-ttu-id="a45d1-527">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="a45d1-527">get\_accChild</span></span>
-   <span data-ttu-id="a45d1-528">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="a45d1-528">get\_accChildCount</span></span>
-   <span data-ttu-id="a45d1-529">получить \_ аккдескриптион</span><span class="sxs-lookup"><span data-stu-id="a45d1-529">get\_accDescription</span></span>
-   <span data-ttu-id="a45d1-530">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="a45d1-530">get\_accFocus</span></span>
-   <span data-ttu-id="a45d1-531">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="a45d1-531">get\_accHelp</span></span>
-   <span data-ttu-id="a45d1-532">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="a45d1-532">get\_accHelpTopic</span></span>
-   <span data-ttu-id="a45d1-533">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="a45d1-533">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="a45d1-534">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="a45d1-534">get\_accName</span></span>
-   <span data-ttu-id="a45d1-535">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-535">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-536">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-536">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-537">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-537">get\_accState</span></span>

## <a name="role_system_whitespace"></a><span data-ttu-id="a45d1-538">\_пробел в системе роли \_</span><span class="sxs-lookup"><span data-stu-id="a45d1-538">ROLE\_SYSTEM\_WHITESPACE</span></span>

<span data-ttu-id="a45d1-539">Дополнительные сведения об этой роли см. в [**разделе \_ \_ пробел в системе роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a45d1-539">For more information on this role, see [**ROLE\_SYSTEM\_WHITESPACE**](object-roles.md).</span></span>

<span data-ttu-id="a45d1-540">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="a45d1-540">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="a45d1-541">акклокатион</span><span class="sxs-lookup"><span data-stu-id="a45d1-541">accLocation</span></span>
-   <span data-ttu-id="a45d1-542">аккселект</span><span class="sxs-lookup"><span data-stu-id="a45d1-542">accSelect</span></span>
-   <span data-ttu-id="a45d1-543">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="a45d1-543">get\_accParent</span></span>
-   <span data-ttu-id="a45d1-544">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="a45d1-544">get\_accRole</span></span>
-   <span data-ttu-id="a45d1-545">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="a45d1-545">get\_accState</span></span>

 

 