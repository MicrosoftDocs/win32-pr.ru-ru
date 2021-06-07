---
title: Другие роли объектов и поддерживаемые методы (Справочник по элементам пользовательского интерфейса MSAA)
description: В этом разделе содержатся сведения о ролях объектов, которые не включены в предыдущие разделы для элементов пользовательского интерфейса.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17e8573142a57e0acf08980895fdae3ea6d1841
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444005"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a><span data-ttu-id="ea606-103">Другие роли объектов и поддерживаемые методы (Справочник по элементам пользовательского интерфейса MSAA)</span><span class="sxs-lookup"><span data-stu-id="ea606-103">Other Object Roles and Supported Methods (MSAA UI Element Reference)</span></span>

<span data-ttu-id="ea606-104">В этом разделе содержатся сведения о ролях объектов, которые не включены в предыдущие разделы для элементов пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ea606-104">This topic provides information about object roles that are not included in the previous topics for UI elements.</span></span> <span data-ttu-id="ea606-105">Каждая роль объекта включает список методов и свойств [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , поддерживаемых для роли объекта.</span><span class="sxs-lookup"><span data-stu-id="ea606-105">Each object role includes a list of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties that are supported for the object role.</span></span> <span data-ttu-id="ea606-106">Другие разделы содержат поддерживаемые методы и свойства методов **IAccessible** для элементов пользовательского интерфейса. в этом разделе перечислены методы и свойства, которые можно использовать для конкретной роли объекта.</span><span class="sxs-lookup"><span data-stu-id="ea606-106">While other topics document supported **IAccessible** methods and properties for UI elements, this topic lists the methods and properties you can expect to be supported for a particular object role.</span></span> <span data-ttu-id="ea606-107">Многие элементы пользовательского интерфейса, которые могут иметь одну из перечисленных здесь ролей, обычно отображаются в браузерах.</span><span class="sxs-lookup"><span data-stu-id="ea606-107">Many of the UI elements which might have one of the roles listed here are typically seen in browsers.</span></span>

> [!Note]  
> <span data-ttu-id="ea606-108">Используйте этот раздел в качестве рекомендации.</span><span class="sxs-lookup"><span data-stu-id="ea606-108">Use this topic as a guideline.</span></span> <span data-ttu-id="ea606-109">Настоятельно рекомендуется использовать средства Microsoft Active Accessibility для проверки ожидаемого поведения отдельной роли объекта.</span><span class="sxs-lookup"><span data-stu-id="ea606-109">We strongly suggest that you use Microsoft Active Accessibility tools to verify expected behavior for an individual object role.</span></span>

 

<span data-ttu-id="ea606-110">В следующей таблице перечислены дополнительные роли объектов, которые Oleacc.dll поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="ea606-110">The following table lists additional object roles which Oleacc.dll supports.</span></span>



| &nbsp; |  &nbsp; |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="ea606-111">**\_ \_ оповещение системы роли**</span><span class="sxs-lookup"><span data-stu-id="ea606-111">**ROLE\_SYSTEM\_ALERT**</span></span>](/windows)                           | [<span data-ttu-id="ea606-112">**\_дроплист системы \_ ролей**</span><span class="sxs-lookup"><span data-stu-id="ea606-112">**ROLE\_SYSTEM\_DROPLIST**</span></span>](/windows)       |
| [<span data-ttu-id="ea606-113">**\_системное \_ приложение роли**</span><span class="sxs-lookup"><span data-stu-id="ea606-113">**ROLE\_SYSTEM\_APPLICATION**</span></span>](/windows)               | [<span data-ttu-id="ea606-114">**\_ \_ уравнение системы роли**</span><span class="sxs-lookup"><span data-stu-id="ea606-114">**ROLE\_SYSTEM\_EQUATION**</span></span>](/windows)       |
| [<span data-ttu-id="ea606-115">**\_граница системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="ea606-115">**ROLE\_SYSTEM\_BORDER**</span></span>](/windows)                         | [<span data-ttu-id="ea606-116">**\_график системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="ea606-116">**ROLE\_SYSTEM\_GRAPHIC**</span></span>](/windows)         |
| [<span data-ttu-id="ea606-117">**\_буттондропдовн системы \_ ролей**</span><span class="sxs-lookup"><span data-stu-id="ea606-117">**ROLE\_SYSTEM\_BUTTONDROPDOWN**</span></span>](/windows)         | [<span data-ttu-id="ea606-118">**\_хелпбаллун системы \_ ролей**</span><span class="sxs-lookup"><span data-stu-id="ea606-118">**ROLE\_SYSTEM\_HELPBALLOON**</span></span>](/windows) |
| [<span data-ttu-id="ea606-119">**\_буттондропдовнгрид системы \_ ролей**</span><span class="sxs-lookup"><span data-stu-id="ea606-119">**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**</span></span>](/windows) | [<span data-ttu-id="ea606-120">**\_IP- \_ адрес системы роли**</span><span class="sxs-lookup"><span data-stu-id="ea606-120">**ROLE\_SYSTEM\_IPADDRESS**</span></span>](/windows)     |
| [<span data-ttu-id="ea606-121">**\_буттонмену системы \_ ролей**</span><span class="sxs-lookup"><span data-stu-id="ea606-121">**ROLE\_SYSTEM\_BUTTONMENU**</span></span>](/windows)                 | [<span data-ttu-id="ea606-122">**\_ссылка на систему роли \_**</span><span class="sxs-lookup"><span data-stu-id="ea606-122">**ROLE\_SYSTEM\_LINK**</span></span>](/windows)               |
| [<span data-ttu-id="ea606-123">**\_системная \_ ЯЧЕЙКа роли**</span><span class="sxs-lookup"><span data-stu-id="ea606-123">**ROLE\_SYSTEM\_CELL**</span></span>](/windows)                             | [<span data-ttu-id="ea606-124">**\_область системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="ea606-124">**ROLE\_SYSTEM\_PANE**</span></span>](/windows)               |
| [<span data-ttu-id="ea606-125">**\_системный \_ символ роли**</span><span class="sxs-lookup"><span data-stu-id="ea606-125">**ROLE\_SYSTEM\_CHARACTER**</span></span>](/windows)                   | [<span data-ttu-id="ea606-126">**\_строка системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="ea606-126">**ROLE\_SYSTEM\_ROW**</span></span>](/windows)                 |
| [<span data-ttu-id="ea606-127">**\_системная \_ Диаграмма роли**</span><span class="sxs-lookup"><span data-stu-id="ea606-127">**ROLE\_SYSTEM\_CHART**</span></span>](/windows)                           | [<span data-ttu-id="ea606-128">**\_ровхеадер системы \_ ролей**</span><span class="sxs-lookup"><span data-stu-id="ea606-128">**ROLE\_SYSTEM\_ROWHEADER**</span></span>](/windows)     |
| [<span data-ttu-id="ea606-129">**\_системные \_ Часы для ролей**</span><span class="sxs-lookup"><span data-stu-id="ea606-129">**ROLE\_SYSTEM\_CLOCK**</span></span>](/windows)                           | [<span data-ttu-id="ea606-130">**\_Разделитель системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="ea606-130">**ROLE\_SYSTEM\_SEPARATOR**</span></span>](/windows)     |
| [<span data-ttu-id="ea606-131">**\_системный \_ столбец роли**</span><span class="sxs-lookup"><span data-stu-id="ea606-131">**ROLE\_SYSTEM\_COLUMN**</span></span>](/windows)                         | [<span data-ttu-id="ea606-132">**\_системный \_ звук роли**</span><span class="sxs-lookup"><span data-stu-id="ea606-132">**ROLE\_SYSTEM\_SOUND**</span></span>](/windows)             |
| [<span data-ttu-id="ea606-133">**\_Схема системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="ea606-133">**ROLE\_SYSTEM\_DIAGRAM**</span></span>](/windows)                       | [<span data-ttu-id="ea606-134">**\_SPLITBUTTON системы \_ ролей**</span><span class="sxs-lookup"><span data-stu-id="ea606-134">**ROLE\_SYSTEM\_SPLITBUTTON**</span></span>](/windows) |
| [<span data-ttu-id="ea606-135">**\_вызов системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="ea606-135">**ROLE\_SYSTEM\_DIAL**</span></span>](/windows)                             | [<span data-ttu-id="ea606-136">**\_системная \_ Таблица ролей**</span><span class="sxs-lookup"><span data-stu-id="ea606-136">**ROLE\_SYSTEM\_TABLE**</span></span>](/windows)             |
| [<span data-ttu-id="ea606-137">**\_документ системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="ea606-137">**ROLE\_SYSTEM\_DOCUMENT**</span></span>](/windows)                     | [<span data-ttu-id="ea606-138">**\_пробел в системе роли \_**</span><span class="sxs-lookup"><span data-stu-id="ea606-138">**ROLE\_SYSTEM\_WHITESPACE**</span></span>](/windows)   |



 

## <a name="role_system_alert"></a><span data-ttu-id="ea606-139">\_ \_ оповещение системы роли</span><span class="sxs-lookup"><span data-stu-id="ea606-139">ROLE\_SYSTEM\_ALERT</span></span>

<span data-ttu-id="ea606-140">Дополнительные сведения об этой роли см. в [**разделе \_ \_ предупреждение системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-140">For more information on this role, see [**ROLE\_SYSTEM\_ALERT**](object-roles.md).</span></span>

<span data-ttu-id="ea606-141">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-141">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-142">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-142">get\_accName</span></span>
-   <span data-ttu-id="ea606-143">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-143">get\_accRole</span></span>
-   <span data-ttu-id="ea606-144">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-144">get\_accState</span></span>

## <a name="role_system_application"></a><span data-ttu-id="ea606-145">\_системное \_ приложение роли</span><span class="sxs-lookup"><span data-stu-id="ea606-145">ROLE\_SYSTEM\_APPLICATION</span></span>

<span data-ttu-id="ea606-146">Дополнительные сведения об этой роли см. в [**разделе \_ \_ приложение системы ролей**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-146">For more information on this role, see [**ROLE\_SYSTEM\_APPLICATION**](object-roles.md).</span></span>

<span data-ttu-id="ea606-147">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-147">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-148">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-148">accHitTest</span></span>
-   <span data-ttu-id="ea606-149">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-149">accLocation</span></span>
-   <span data-ttu-id="ea606-150">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-150">accNavigate</span></span>
-   <span data-ttu-id="ea606-151">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="ea606-151">get\_accChild</span></span>
-   <span data-ttu-id="ea606-152">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="ea606-152">get\_accChildCount</span></span>
-   <span data-ttu-id="ea606-153">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-153">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-154">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="ea606-154">get\_accHelp</span></span>
-   <span data-ttu-id="ea606-155">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="ea606-155">get\_accHelpTopic</span></span>
-   <span data-ttu-id="ea606-156">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="ea606-156">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="ea606-157">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-157">get\_accName</span></span>
-   <span data-ttu-id="ea606-158">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-158">get\_accParent</span></span>
-   <span data-ttu-id="ea606-159">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-159">get\_accRole</span></span>
-   <span data-ttu-id="ea606-160">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-160">get\_accState</span></span>

## <a name="role_system_border"></a><span data-ttu-id="ea606-161">\_граница системы \_ роли</span><span class="sxs-lookup"><span data-stu-id="ea606-161">ROLE\_SYSTEM\_BORDER</span></span>

<span data-ttu-id="ea606-162">Дополнительные сведения об этой роли см. в [**разделе \_ \_ граница системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-162">For more information on this role, see [**ROLE\_SYSTEM\_BORDER**](object-roles.md).</span></span>

<span data-ttu-id="ea606-163">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-163">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-164">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-164">accHitTest</span></span>
-   <span data-ttu-id="ea606-165">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-165">accLocation</span></span>
-   <span data-ttu-id="ea606-166">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-166">accNavigate</span></span>
-   <span data-ttu-id="ea606-167">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-167">get\_accRole</span></span>
-   <span data-ttu-id="ea606-168">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-168">get\_accState</span></span>

## <a name="role_system_buttondropdown"></a><span data-ttu-id="ea606-169">\_буттондропдовн системы \_ ролей</span><span class="sxs-lookup"><span data-stu-id="ea606-169">ROLE\_SYSTEM\_BUTTONDROPDOWN</span></span>

<span data-ttu-id="ea606-170">Дополнительные сведения об этой роли см. в разделе [**Role \_ System \_ буттондропдовн**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-170">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWN**](object-roles.md).</span></span>

<span data-ttu-id="ea606-171">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-171">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-172">аккдодефаултактион</span><span class="sxs-lookup"><span data-stu-id="ea606-172">accDoDefaultAction</span></span>
-   <span data-ttu-id="ea606-173">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-173">accHitTest</span></span>
-   <span data-ttu-id="ea606-174">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-174">accLocation</span></span>
-   <span data-ttu-id="ea606-175">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-175">accNavigate</span></span>
-   <span data-ttu-id="ea606-176">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="ea606-176">get\_accChild</span></span>
-   <span data-ttu-id="ea606-177">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="ea606-177">get\_accChildCount</span></span>
-   <span data-ttu-id="ea606-178">получить \_ аккдефаултактион</span><span class="sxs-lookup"><span data-stu-id="ea606-178">get\_accDefaultAction</span></span>
-   <span data-ttu-id="ea606-179">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-179">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-180">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="ea606-180">get\_accHelp</span></span>
-   <span data-ttu-id="ea606-181">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="ea606-181">get\_accHelpTopic</span></span>
-   <span data-ttu-id="ea606-182">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="ea606-182">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="ea606-183">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-183">get\_accName</span></span>
-   <span data-ttu-id="ea606-184">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-184">get\_accParent</span></span>
-   <span data-ttu-id="ea606-185">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-185">get\_accRole</span></span>
-   <span data-ttu-id="ea606-186">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-186">get\_accState</span></span>

## <a name="role_system_buttondropdowngrid"></a><span data-ttu-id="ea606-187">\_буттондропдовнгрид системы \_ ролей</span><span class="sxs-lookup"><span data-stu-id="ea606-187">ROLE\_SYSTEM\_BUTTONDROPDOWNGRID</span></span>

<span data-ttu-id="ea606-188">Дополнительные сведения об этой роли см. в разделе [**Role \_ System \_ буттондропдовнгрид**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-188">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**](object-roles.md).</span></span>

<span data-ttu-id="ea606-189">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-189">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-190">аккдодефаултактион</span><span class="sxs-lookup"><span data-stu-id="ea606-190">accDoDefaultAction</span></span>
-   <span data-ttu-id="ea606-191">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-191">accHitTest</span></span>
-   <span data-ttu-id="ea606-192">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-192">accLocation</span></span>
-   <span data-ttu-id="ea606-193">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-193">accNavigate</span></span>
-   <span data-ttu-id="ea606-194">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="ea606-194">get\_accChild</span></span>
-   <span data-ttu-id="ea606-195">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="ea606-195">get\_accChildCount</span></span>
-   <span data-ttu-id="ea606-196">получить \_ аккдефаултактион</span><span class="sxs-lookup"><span data-stu-id="ea606-196">get\_accDefaultAction</span></span>
-   <span data-ttu-id="ea606-197">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-197">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-198">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="ea606-198">get\_accHelp</span></span>
-   <span data-ttu-id="ea606-199">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="ea606-199">get\_accHelpTopic</span></span>
-   <span data-ttu-id="ea606-200">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="ea606-200">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="ea606-201">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-201">get\_accName</span></span>
-   <span data-ttu-id="ea606-202">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-202">get\_accParent</span></span>
-   <span data-ttu-id="ea606-203">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-203">get\_accRole</span></span>
-   <span data-ttu-id="ea606-204">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-204">get\_accState</span></span>

## <a name="role_system_buttonmenu"></a><span data-ttu-id="ea606-205">\_буттонмену системы \_ ролей</span><span class="sxs-lookup"><span data-stu-id="ea606-205">ROLE\_SYSTEM\_BUTTONMENU</span></span>

<span data-ttu-id="ea606-206">Дополнительные сведения об этой роли см. в разделе [**Role \_ System \_ буттонмену**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-206">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONMENU**](object-roles.md).</span></span>

<span data-ttu-id="ea606-207">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-207">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-208">аккдодефаултактион</span><span class="sxs-lookup"><span data-stu-id="ea606-208">accDoDefaultAction</span></span>
-   <span data-ttu-id="ea606-209">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-209">accHitTest</span></span>
-   <span data-ttu-id="ea606-210">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-210">accLocation</span></span>
-   <span data-ttu-id="ea606-211">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-211">accNavigate</span></span>
-   <span data-ttu-id="ea606-212">получить \_ аккдефаултактион</span><span class="sxs-lookup"><span data-stu-id="ea606-212">get\_accDefaultAction</span></span>
-   <span data-ttu-id="ea606-213">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-213">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-214">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="ea606-214">get\_accHelp</span></span>
-   <span data-ttu-id="ea606-215">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="ea606-215">get\_accHelpTopic</span></span>
-   <span data-ttu-id="ea606-216">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="ea606-216">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="ea606-217">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-217">get\_accName</span></span>
-   <span data-ttu-id="ea606-218">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-218">get\_accParent</span></span>
-   <span data-ttu-id="ea606-219">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-219">get\_accRole</span></span>
-   <span data-ttu-id="ea606-220">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-220">get\_accState</span></span>

## <a name="role_system_cell"></a><span data-ttu-id="ea606-221">\_системная \_ ЯЧЕЙКа роли</span><span class="sxs-lookup"><span data-stu-id="ea606-221">ROLE\_SYSTEM\_CELL</span></span>

<span data-ttu-id="ea606-222">Дополнительные сведения об этой роли см. в статье [**роль \_ системной \_ ячейки**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-222">For more information on this role, see [**ROLE\_SYSTEM\_CELL**](object-roles.md).</span></span>

<span data-ttu-id="ea606-223">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-223">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-224">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-224">accHitTest</span></span>
-   <span data-ttu-id="ea606-225">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-225">accLocation</span></span>
-   <span data-ttu-id="ea606-226">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-226">accNavigate</span></span>
-   <span data-ttu-id="ea606-227">аккселект</span><span class="sxs-lookup"><span data-stu-id="ea606-227">accSelect</span></span>
-   <span data-ttu-id="ea606-228">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="ea606-228">get\_accChild</span></span>
-   <span data-ttu-id="ea606-229">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="ea606-229">get\_accChildCount</span></span>
-   <span data-ttu-id="ea606-230">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-230">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-231">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="ea606-231">get\_accHelp</span></span>
-   <span data-ttu-id="ea606-232">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="ea606-232">get\_accHelpTopic</span></span>
-   <span data-ttu-id="ea606-233">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="ea606-233">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="ea606-234">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-234">get\_accName</span></span>
-   <span data-ttu-id="ea606-235">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-235">get\_accParent</span></span>
-   <span data-ttu-id="ea606-236">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-236">get\_accRole</span></span>
-   <span data-ttu-id="ea606-237">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-237">get\_accState</span></span>
-   <span data-ttu-id="ea606-238">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="ea606-238">get\_accValue</span></span>

## <a name="role_system_character"></a><span data-ttu-id="ea606-239">\_системный \_ символ роли</span><span class="sxs-lookup"><span data-stu-id="ea606-239">ROLE\_SYSTEM\_CHARACTER</span></span>

<span data-ttu-id="ea606-240">Дополнительные сведения об этой роли см. в [**разделе \_ системный \_ символ роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-240">For more information on this role, see [**ROLE\_SYSTEM\_CHARACTER**](object-roles.md).</span></span>

<span data-ttu-id="ea606-241">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-241">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-242">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-242">accHitTest</span></span>
-   <span data-ttu-id="ea606-243">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-243">accLocation</span></span>
-   <span data-ttu-id="ea606-244">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-244">accNavigate</span></span>
-   <span data-ttu-id="ea606-245">получить \_ аккдескриптион</span><span class="sxs-lookup"><span data-stu-id="ea606-245">get\_accDescription</span></span>
-   <span data-ttu-id="ea606-246">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-246">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-247">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="ea606-247">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="ea606-248">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-248">get\_accName</span></span>
-   <span data-ttu-id="ea606-249">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-249">get\_accParent</span></span>
-   <span data-ttu-id="ea606-250">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-250">get\_accRole</span></span>
-   <span data-ttu-id="ea606-251">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-251">get\_accState</span></span>
-   <span data-ttu-id="ea606-252">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="ea606-252">get\_accValue</span></span>

## <a name="role_system_chart"></a><span data-ttu-id="ea606-253">\_системная \_ Диаграмма роли</span><span class="sxs-lookup"><span data-stu-id="ea606-253">ROLE\_SYSTEM\_CHART</span></span>

<span data-ttu-id="ea606-254">Дополнительные сведения об этой роли см. в [**разделе \_ \_ Диаграмма системы ролей**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-254">For more information on this role, see [**ROLE\_SYSTEM\_CHART**](object-roles.md).</span></span>

<span data-ttu-id="ea606-255">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-255">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-256">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-256">accHitTest</span></span>
-   <span data-ttu-id="ea606-257">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-257">accLocation</span></span>
-   <span data-ttu-id="ea606-258">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-258">accNavigate</span></span>
-   <span data-ttu-id="ea606-259">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="ea606-259">get\_accChild</span></span>
-   <span data-ttu-id="ea606-260">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="ea606-260">get\_accChildCount</span></span>
-   <span data-ttu-id="ea606-261">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-261">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-262">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="ea606-262">get\_accHelp</span></span>
-   <span data-ttu-id="ea606-263">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="ea606-263">get\_accHelpTopic</span></span>
-   <span data-ttu-id="ea606-264">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="ea606-264">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="ea606-265">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-265">get\_accName</span></span>
-   <span data-ttu-id="ea606-266">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-266">get\_accParent</span></span>
-   <span data-ttu-id="ea606-267">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-267">get\_accRole</span></span>
-   <span data-ttu-id="ea606-268">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-268">get\_accState</span></span>

## <a name="role_system_clock"></a><span data-ttu-id="ea606-269">\_системные \_ Часы для ролей</span><span class="sxs-lookup"><span data-stu-id="ea606-269">ROLE\_SYSTEM\_CLOCK</span></span>

<span data-ttu-id="ea606-270">Дополнительные сведения об этой роли см. в [**разделе \_ системные \_ часы системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-270">For more information on this role, see [**ROLE\_SYSTEM\_CLOCK**](object-roles.md).</span></span>

<span data-ttu-id="ea606-271">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-271">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-272">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-272">accHitTest</span></span>
-   <span data-ttu-id="ea606-273">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-273">accLocation</span></span>
-   <span data-ttu-id="ea606-274">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-274">accNavigate</span></span>
-   <span data-ttu-id="ea606-275">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-275">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-276">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="ea606-276">get\_accHelp</span></span>
-   <span data-ttu-id="ea606-277">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="ea606-277">get\_accHelpTopic</span></span>
-   <span data-ttu-id="ea606-278">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="ea606-278">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="ea606-279">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-279">get\_accName</span></span>
-   <span data-ttu-id="ea606-280">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-280">get\_accParent</span></span>
-   <span data-ttu-id="ea606-281">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-281">get\_accRole</span></span>
-   <span data-ttu-id="ea606-282">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-282">get\_accState</span></span>
-   <span data-ttu-id="ea606-283">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="ea606-283">get\_accValue</span></span>

## <a name="role_system_column"></a><span data-ttu-id="ea606-284">\_системный \_ столбец роли</span><span class="sxs-lookup"><span data-stu-id="ea606-284">ROLE\_SYSTEM\_COLUMN</span></span>

<span data-ttu-id="ea606-285">Дополнительные сведения об этой роли см. в [**разделе \_ \_ столбец системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-285">For more information on this role, see [**ROLE\_SYSTEM\_COLUMN**](object-roles.md).</span></span>

<span data-ttu-id="ea606-286">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-286">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-287">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-287">accHitTest</span></span>
-   <span data-ttu-id="ea606-288">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-288">accLocation</span></span>
-   <span data-ttu-id="ea606-289">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-289">accNavigate</span></span>
-   <span data-ttu-id="ea606-290">аккселект</span><span class="sxs-lookup"><span data-stu-id="ea606-290">accSelect</span></span>
-   <span data-ttu-id="ea606-291">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="ea606-291">get\_accChild</span></span>
-   <span data-ttu-id="ea606-292">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="ea606-292">get\_accChildCount</span></span>
-   <span data-ttu-id="ea606-293">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-293">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-294">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-294">get\_accName</span></span>
-   <span data-ttu-id="ea606-295">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-295">get\_accParent</span></span>
-   <span data-ttu-id="ea606-296">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-296">get\_accRole</span></span>
-   <span data-ttu-id="ea606-297">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-297">get\_accState</span></span>
-   <span data-ttu-id="ea606-298">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="ea606-298">get\_accValue</span></span>

## <a name="role_system_diagram"></a><span data-ttu-id="ea606-299">\_Схема системы \_ роли</span><span class="sxs-lookup"><span data-stu-id="ea606-299">ROLE\_SYSTEM\_DIAGRAM</span></span>

<span data-ttu-id="ea606-300">Дополнительные сведения об этой роли см. в [**разделе \_ \_ Схема системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-300">For more information on this role, see [**ROLE\_SYSTEM\_DIAGRAM**](object-roles.md).</span></span>

<span data-ttu-id="ea606-301">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-301">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-302">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-302">accHitTest</span></span>
-   <span data-ttu-id="ea606-303">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-303">accLocation</span></span>
-   <span data-ttu-id="ea606-304">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-304">accNavigate</span></span>
-   <span data-ttu-id="ea606-305">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="ea606-305">get\_accChild</span></span>
-   <span data-ttu-id="ea606-306">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="ea606-306">get\_accChildCount</span></span>
-   <span data-ttu-id="ea606-307">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-307">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-308">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="ea606-308">get\_accHelp</span></span>
-   <span data-ttu-id="ea606-309">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="ea606-309">get\_accHelpTopic</span></span>
-   <span data-ttu-id="ea606-310">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="ea606-310">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="ea606-311">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-311">get\_accName</span></span>
-   <span data-ttu-id="ea606-312">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-312">get\_accParent</span></span>
-   <span data-ttu-id="ea606-313">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-313">get\_accRole</span></span>
-   <span data-ttu-id="ea606-314">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-314">get\_accState</span></span>

## <a name="role_system_dial"></a><span data-ttu-id="ea606-315">\_вызов системы \_ роли</span><span class="sxs-lookup"><span data-stu-id="ea606-315">ROLE\_SYSTEM\_DIAL</span></span>

<span data-ttu-id="ea606-316">Дополнительные сведения об этой роли см. в разделе [**Role \_ System \_ Dialin**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-316">For more information on this role, see [**ROLE\_SYSTEM\_DIAL**](object-roles.md).</span></span>

<span data-ttu-id="ea606-317">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-317">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-318">аккдодефаултактион</span><span class="sxs-lookup"><span data-stu-id="ea606-318">accDoDefaultAction</span></span>
-   <span data-ttu-id="ea606-319">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-319">accHitTest</span></span>
-   <span data-ttu-id="ea606-320">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-320">accLocation</span></span>
-   <span data-ttu-id="ea606-321">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-321">accNavigate</span></span>
-   <span data-ttu-id="ea606-322">получить \_ аккдефаултактион</span><span class="sxs-lookup"><span data-stu-id="ea606-322">get\_accDefaultAction</span></span>
-   <span data-ttu-id="ea606-323">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-323">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-324">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="ea606-324">get\_accHelp</span></span>
-   <span data-ttu-id="ea606-325">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="ea606-325">get\_accHelpTopic</span></span>
-   <span data-ttu-id="ea606-326">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="ea606-326">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="ea606-327">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-327">get\_accName</span></span>
-   <span data-ttu-id="ea606-328">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-328">get\_accParent</span></span>
-   <span data-ttu-id="ea606-329">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-329">get\_accRole</span></span>
-   <span data-ttu-id="ea606-330">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-330">get\_accState</span></span>
-   <span data-ttu-id="ea606-331">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="ea606-331">get\_accValue</span></span>

## <a name="role_system_document"></a><span data-ttu-id="ea606-332">\_документ системы \_ роли</span><span class="sxs-lookup"><span data-stu-id="ea606-332">ROLE\_SYSTEM\_DOCUMENT</span></span>

<span data-ttu-id="ea606-333">Дополнительные сведения об этой роли см. в [**разделе \_ \_ документ системы ролей**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-333">For more information on this role, see [**ROLE\_SYSTEM\_DOCUMENT**](object-roles.md).</span></span>

<span data-ttu-id="ea606-334">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-334">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-335">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-335">accHitTest</span></span>
-   <span data-ttu-id="ea606-336">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-336">accLocation</span></span>
-   <span data-ttu-id="ea606-337">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-337">accNavigate</span></span>
-   <span data-ttu-id="ea606-338">аккселект</span><span class="sxs-lookup"><span data-stu-id="ea606-338">accSelect</span></span>
-   <span data-ttu-id="ea606-339">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="ea606-339">get\_accChild</span></span>
-   <span data-ttu-id="ea606-340">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="ea606-340">get\_accChildCount</span></span>
-   <span data-ttu-id="ea606-341">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-341">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-342">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-342">get\_accName</span></span>
-   <span data-ttu-id="ea606-343">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-343">get\_accParent</span></span>
-   <span data-ttu-id="ea606-344">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-344">get\_accRole</span></span>
-   <span data-ttu-id="ea606-345">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-345">get\_accState</span></span>

## <a name="role_system_droplist"></a><span data-ttu-id="ea606-346">\_дроплист системы \_ ролей</span><span class="sxs-lookup"><span data-stu-id="ea606-346">ROLE\_SYSTEM\_DROPLIST</span></span>

<span data-ttu-id="ea606-347">Дополнительные сведения об этой роли см. в разделе [**Role \_ System \_ дроплист**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-347">For more information on this role, see [**ROLE\_SYSTEM\_DROPLIST**](object-roles.md).</span></span>

<span data-ttu-id="ea606-348">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-348">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-349">аккдодефаултактион</span><span class="sxs-lookup"><span data-stu-id="ea606-349">accDoDefaultAction</span></span>
-   <span data-ttu-id="ea606-350">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-350">accHitTest</span></span>
-   <span data-ttu-id="ea606-351">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-351">accLocation</span></span>
-   <span data-ttu-id="ea606-352">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-352">accNavigate</span></span>
-   <span data-ttu-id="ea606-353">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="ea606-353">get\_accChild</span></span>
-   <span data-ttu-id="ea606-354">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="ea606-354">get\_accChildCount</span></span>
-   <span data-ttu-id="ea606-355">получить \_ аккдефаултактион</span><span class="sxs-lookup"><span data-stu-id="ea606-355">get\_accDefaultAction</span></span>
-   <span data-ttu-id="ea606-356">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-356">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-357">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="ea606-357">get\_accHelp</span></span>
-   <span data-ttu-id="ea606-358">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="ea606-358">get\_accHelpTopic</span></span>
-   <span data-ttu-id="ea606-359">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="ea606-359">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="ea606-360">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-360">get\_accName</span></span>
-   <span data-ttu-id="ea606-361">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-361">get\_accParent</span></span>
-   <span data-ttu-id="ea606-362">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-362">get\_accRole</span></span>
-   <span data-ttu-id="ea606-363">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-363">get\_accState</span></span>

## <a name="role_system_equation"></a><span data-ttu-id="ea606-364">\_ \_ уравнение системы роли</span><span class="sxs-lookup"><span data-stu-id="ea606-364">ROLE\_SYSTEM\_EQUATION</span></span>

<span data-ttu-id="ea606-365">Дополнительные сведения об этой роли см. в [**разделе \_ \_ уравнение системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-365">For more information on this role, see [**ROLE\_SYSTEM\_EQUATION**](object-roles.md).</span></span>

<span data-ttu-id="ea606-366">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-366">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-367">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-367">accHitTest</span></span>
-   <span data-ttu-id="ea606-368">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-368">accLocation</span></span>
-   <span data-ttu-id="ea606-369">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-369">accNavigate</span></span>
-   <span data-ttu-id="ea606-370">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-370">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-371">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-371">get\_accName</span></span>
-   <span data-ttu-id="ea606-372">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-372">get\_accParent</span></span>
-   <span data-ttu-id="ea606-373">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-373">get\_accRole</span></span>
-   <span data-ttu-id="ea606-374">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-374">get\_accState</span></span>
-   <span data-ttu-id="ea606-375">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="ea606-375">get\_accValue</span></span>

## <a name="role_system_graphic"></a><span data-ttu-id="ea606-376">\_график системы \_ роли</span><span class="sxs-lookup"><span data-stu-id="ea606-376">ROLE\_SYSTEM\_GRAPHIC</span></span>

<span data-ttu-id="ea606-377">Дополнительные сведения об этой роли см. в [**разделе \_ \_ график системы ролей**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-377">For more information on this role, see [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

<span data-ttu-id="ea606-378">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-378">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-379">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-379">accHitTest</span></span>
-   <span data-ttu-id="ea606-380">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-380">accLocation</span></span>
-   <span data-ttu-id="ea606-381">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-381">accNavigate</span></span>
-   <span data-ttu-id="ea606-382">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-382">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-383">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="ea606-383">get\_accHelp</span></span>
-   <span data-ttu-id="ea606-384">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="ea606-384">get\_accHelpTopic</span></span>
-   <span data-ttu-id="ea606-385">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="ea606-385">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="ea606-386">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-386">get\_accName</span></span>
-   <span data-ttu-id="ea606-387">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-387">get\_accParent</span></span>
-   <span data-ttu-id="ea606-388">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-388">get\_accRole</span></span>
-   <span data-ttu-id="ea606-389">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-389">get\_accState</span></span>

## <a name="role_system_helpballoon"></a><span data-ttu-id="ea606-390">\_хелпбаллун системы \_ ролей</span><span class="sxs-lookup"><span data-stu-id="ea606-390">ROLE\_SYSTEM\_HELPBALLOON</span></span>

<span data-ttu-id="ea606-391">Дополнительные сведения об этой роли см. в разделе [**Role \_ System \_ хелпбаллун**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-391">For more information on this role, see [**ROLE\_SYSTEM\_HELPBALLOON**](object-roles.md).</span></span>

<span data-ttu-id="ea606-392">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-392">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-393">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-393">accHitTest</span></span>
-   <span data-ttu-id="ea606-394">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-394">accLocation</span></span>
-   <span data-ttu-id="ea606-395">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-395">accNavigate</span></span>
-   <span data-ttu-id="ea606-396">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="ea606-396">get\_accChild</span></span>
-   <span data-ttu-id="ea606-397">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="ea606-397">get\_accChildCount</span></span>
-   <span data-ttu-id="ea606-398">получить \_ аккдефаултактион</span><span class="sxs-lookup"><span data-stu-id="ea606-398">get\_accDefaultAction</span></span>
-   <span data-ttu-id="ea606-399">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-399">get\_accName</span></span>
-   <span data-ttu-id="ea606-400">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-400">get\_accParent</span></span>
-   <span data-ttu-id="ea606-401">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-401">get\_accRole</span></span>
-   <span data-ttu-id="ea606-402">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-402">get\_accState</span></span>
-   <span data-ttu-id="ea606-403">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="ea606-403">get\_accValue</span></span>

## <a name="role_system_ipaddress"></a><span data-ttu-id="ea606-404">\_IP- \_ адрес системы роли</span><span class="sxs-lookup"><span data-stu-id="ea606-404">ROLE\_SYSTEM\_IPADDRESS</span></span>

<span data-ttu-id="ea606-405">Дополнительные сведения об этой роли см. в [**разделе \_ \_ IP-адрес системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-405">For more information on this role, see [**ROLE\_SYSTEM\_IPADDRESS**](object-roles.md).</span></span>

<span data-ttu-id="ea606-406">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-406">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-407">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-407">accHitTest</span></span>
-   <span data-ttu-id="ea606-408">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-408">accLocation</span></span>
-   <span data-ttu-id="ea606-409">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-409">accNavigate</span></span>
-   <span data-ttu-id="ea606-410">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="ea606-410">get\_accChild</span></span>
-   <span data-ttu-id="ea606-411">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="ea606-411">get\_accChildCount</span></span>
-   <span data-ttu-id="ea606-412">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-412">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-413">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="ea606-413">get\_accHelp</span></span>
-   <span data-ttu-id="ea606-414">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="ea606-414">get\_accHelpTopic</span></span>
-   <span data-ttu-id="ea606-415">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="ea606-415">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="ea606-416">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-416">get\_accName</span></span>
-   <span data-ttu-id="ea606-417">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-417">get\_accParent</span></span>
-   <span data-ttu-id="ea606-418">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-418">get\_accRole</span></span>
-   <span data-ttu-id="ea606-419">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-419">get\_accState</span></span>
-   <span data-ttu-id="ea606-420">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="ea606-420">get\_accValue</span></span>

## <a name="role_system_link"></a><span data-ttu-id="ea606-421">\_ссылка на систему роли \_</span><span class="sxs-lookup"><span data-stu-id="ea606-421">ROLE\_SYSTEM\_LINK</span></span>

<span data-ttu-id="ea606-422">Дополнительные сведения об этой роли см. в [**разделе \_ \_ ссылка на систему роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-422">For more information on this role, see [**ROLE\_SYSTEM\_LINK**](object-roles.md).</span></span>

<span data-ttu-id="ea606-423">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-423">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-424">аккдодефаултактион</span><span class="sxs-lookup"><span data-stu-id="ea606-424">accDoDefaultAction</span></span>
-   <span data-ttu-id="ea606-425">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-425">accHitTest</span></span>
-   <span data-ttu-id="ea606-426">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-426">accLocation</span></span>
-   <span data-ttu-id="ea606-427">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-427">accNavigate</span></span>
-   <span data-ttu-id="ea606-428">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="ea606-428">get\_accChild</span></span>
-   <span data-ttu-id="ea606-429">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="ea606-429">get\_accChildCount</span></span>
-   <span data-ttu-id="ea606-430">получить \_ аккдефаултактион</span><span class="sxs-lookup"><span data-stu-id="ea606-430">get\_accDefaultAction</span></span>
-   <span data-ttu-id="ea606-431">получить \_ аккдескриптион</span><span class="sxs-lookup"><span data-stu-id="ea606-431">get\_accDescription</span></span>
-   <span data-ttu-id="ea606-432">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-432">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-433">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="ea606-433">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="ea606-434">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-434">get\_accName</span></span>
-   <span data-ttu-id="ea606-435">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-435">get\_accParent</span></span>
-   <span data-ttu-id="ea606-436">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-436">get\_accRole</span></span>
-   <span data-ttu-id="ea606-437">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-437">get\_accState</span></span>
-   <span data-ttu-id="ea606-438">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="ea606-438">get\_accValue</span></span>

## <a name="role_system_pane"></a><span data-ttu-id="ea606-439">\_область системы \_ роли</span><span class="sxs-lookup"><span data-stu-id="ea606-439">ROLE\_SYSTEM\_PANE</span></span>

<span data-ttu-id="ea606-440">Дополнительные сведения об этой роли см. в [**разделе \_ \_ область системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-440">For more information on this role, see [**ROLE\_SYSTEM\_PANE**](object-roles.md).</span></span>

<span data-ttu-id="ea606-441">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-441">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-442">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-442">accHitTest</span></span>
-   <span data-ttu-id="ea606-443">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-443">accLocation</span></span>
-   <span data-ttu-id="ea606-444">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-444">accNavigate</span></span>
-   <span data-ttu-id="ea606-445">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="ea606-445">get\_accChild</span></span>
-   <span data-ttu-id="ea606-446">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="ea606-446">get\_accChildCount</span></span>
-   <span data-ttu-id="ea606-447">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-447">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-448">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="ea606-448">get\_accHelp</span></span>
-   <span data-ttu-id="ea606-449">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="ea606-449">get\_accHelpTopic</span></span>
-   <span data-ttu-id="ea606-450">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="ea606-450">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="ea606-451">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-451">get\_accName</span></span>
-   <span data-ttu-id="ea606-452">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-452">get\_accParent</span></span>
-   <span data-ttu-id="ea606-453">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-453">get\_accRole</span></span>
-   <span data-ttu-id="ea606-454">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-454">get\_accState</span></span>

## <a name="role_system_row"></a><span data-ttu-id="ea606-455">\_строка системы \_ роли</span><span class="sxs-lookup"><span data-stu-id="ea606-455">ROLE\_SYSTEM\_ROW</span></span>

<span data-ttu-id="ea606-456">Дополнительные сведения об этой роли см. в [**разделе \_ \_ строка системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-456">For more information on this role, see [**ROLE\_SYSTEM\_ROW**](object-roles.md).</span></span>

<span data-ttu-id="ea606-457">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-457">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-458">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-458">accHitTest</span></span>
-   <span data-ttu-id="ea606-459">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-459">accLocation</span></span>
-   <span data-ttu-id="ea606-460">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-460">accNavigate</span></span>
-   <span data-ttu-id="ea606-461">аккселект</span><span class="sxs-lookup"><span data-stu-id="ea606-461">accSelect</span></span>
-   <span data-ttu-id="ea606-462">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="ea606-462">get\_accChild</span></span>
-   <span data-ttu-id="ea606-463">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="ea606-463">get\_accChildCount</span></span>
-   <span data-ttu-id="ea606-464">получить \_ аккдескриптион</span><span class="sxs-lookup"><span data-stu-id="ea606-464">get\_accDescription</span></span>
-   <span data-ttu-id="ea606-465">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-465">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-466">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-466">get\_accName</span></span>
-   <span data-ttu-id="ea606-467">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-467">get\_accParent</span></span>
-   <span data-ttu-id="ea606-468">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-468">get\_accRole</span></span>
-   <span data-ttu-id="ea606-469">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-469">get\_accState</span></span>
-   <span data-ttu-id="ea606-470">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="ea606-470">get\_accValue</span></span>

## <a name="role_system_rowheader"></a><span data-ttu-id="ea606-471">\_ровхеадер системы \_ ролей</span><span class="sxs-lookup"><span data-stu-id="ea606-471">ROLE\_SYSTEM\_ROWHEADER</span></span>

<span data-ttu-id="ea606-472">Дополнительные сведения об этой роли см. в разделе [**Role \_ System \_ ровхеадер**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-472">For more information on this role, see [**ROLE\_SYSTEM\_ROWHEADER**](object-roles.md).</span></span>

<span data-ttu-id="ea606-473">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-473">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-474">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-474">accHitTest</span></span>
-   <span data-ttu-id="ea606-475">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-475">accLocation</span></span>
-   <span data-ttu-id="ea606-476">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-476">accNavigate</span></span>
-   <span data-ttu-id="ea606-477">аккселект</span><span class="sxs-lookup"><span data-stu-id="ea606-477">accSelect</span></span>
-   <span data-ttu-id="ea606-478">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="ea606-478">get\_accChild</span></span>
-   <span data-ttu-id="ea606-479">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="ea606-479">get\_accChildCount</span></span>
-   <span data-ttu-id="ea606-480">получить \_ аккдефаултактион</span><span class="sxs-lookup"><span data-stu-id="ea606-480">get\_accDefaultAction</span></span>
-   <span data-ttu-id="ea606-481">получить \_ аккдескриптион</span><span class="sxs-lookup"><span data-stu-id="ea606-481">get\_accDescription</span></span>
-   <span data-ttu-id="ea606-482">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-482">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-483">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-483">get\_accName</span></span>
-   <span data-ttu-id="ea606-484">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-484">get\_accParent</span></span>
-   <span data-ttu-id="ea606-485">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-485">get\_accRole</span></span>
-   <span data-ttu-id="ea606-486">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-486">get\_accState</span></span>
-   <span data-ttu-id="ea606-487">получить \_ акквалуе</span><span class="sxs-lookup"><span data-stu-id="ea606-487">get\_accValue</span></span>

## <a name="role_system_separator"></a><span data-ttu-id="ea606-488">\_Разделитель системы \_ роли</span><span class="sxs-lookup"><span data-stu-id="ea606-488">ROLE\_SYSTEM\_SEPARATOR</span></span>

<span data-ttu-id="ea606-489">Дополнительные сведения об этой роли см. в [**статье \_ \_ Разделитель системы ролей**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-489">For more information on this role, see [**ROLE\_SYSTEM\_SEPARATOR**](object-roles.md).</span></span>

<span data-ttu-id="ea606-490">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-490">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-491">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-491">accHitTest</span></span>
-   <span data-ttu-id="ea606-492">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-492">accLocation</span></span>
-   <span data-ttu-id="ea606-493">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="ea606-493">get\_accChild</span></span>
-   <span data-ttu-id="ea606-494">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="ea606-494">get\_accChildCount</span></span>
-   <span data-ttu-id="ea606-495">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-495">get\_accParent</span></span>
-   <span data-ttu-id="ea606-496">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-496">get\_accRole</span></span>
-   <span data-ttu-id="ea606-497">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-497">get\_accState</span></span>

## <a name="role_system_sound"></a><span data-ttu-id="ea606-498">\_системный \_ звук роли</span><span class="sxs-lookup"><span data-stu-id="ea606-498">ROLE\_SYSTEM\_SOUND</span></span>

<span data-ttu-id="ea606-499">Дополнительные сведения об этой роли см. в [**разделе \_ системный \_ звук роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-499">For more information on this role, see [**ROLE\_SYSTEM\_SOUND**](object-roles.md).</span></span>

<span data-ttu-id="ea606-500">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-500">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-501">получить \_ аккдескриптион</span><span class="sxs-lookup"><span data-stu-id="ea606-501">get\_accDescription</span></span>
-   <span data-ttu-id="ea606-502">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-502">get\_accName</span></span>
-   <span data-ttu-id="ea606-503">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-503">get\_accRole</span></span>
-   <span data-ttu-id="ea606-504">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-504">get\_accState</span></span>

## <a name="role_system_splitbutton"></a><span data-ttu-id="ea606-505">\_SPLITBUTTON системы \_ ролей</span><span class="sxs-lookup"><span data-stu-id="ea606-505">ROLE\_SYSTEM\_SPLITBUTTON</span></span>

<span data-ttu-id="ea606-506">Дополнительные сведения об этой роли см. в [**разделе \_ \_ SPLITBUTTON системы ролей**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-506">For more information on this role, see [**ROLE\_SYSTEM\_SPLITBUTTON**](object-roles.md).</span></span>

<span data-ttu-id="ea606-507">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-507">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-508">аккдодефаултактион</span><span class="sxs-lookup"><span data-stu-id="ea606-508">accDoDefaultAction</span></span>
-   <span data-ttu-id="ea606-509">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-509">accHitTest</span></span>
-   <span data-ttu-id="ea606-510">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-510">accLocation</span></span>
-   <span data-ttu-id="ea606-511">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-511">accNavigate</span></span>
-   <span data-ttu-id="ea606-512">получить \_ аккдефаултактион</span><span class="sxs-lookup"><span data-stu-id="ea606-512">get\_accDefaultAction</span></span>
-   <span data-ttu-id="ea606-513">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="ea606-513">get\_accHelp</span></span>
-   <span data-ttu-id="ea606-514">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="ea606-514">get\_accHelpTopic</span></span>
-   <span data-ttu-id="ea606-515">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="ea606-515">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="ea606-516">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-516">get\_accName</span></span>
-   <span data-ttu-id="ea606-517">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-517">get\_accParent</span></span>
-   <span data-ttu-id="ea606-518">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-518">get\_accRole</span></span>
-   <span data-ttu-id="ea606-519">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-519">get\_accState</span></span>

## <a name="role_system_table"></a><span data-ttu-id="ea606-520">\_системная \_ Таблица ролей</span><span class="sxs-lookup"><span data-stu-id="ea606-520">ROLE\_SYSTEM\_TABLE</span></span>

<span data-ttu-id="ea606-521">Дополнительные сведения об этой роли см. в [**разделе \_ системная \_ Таблица ролей**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-521">For more information on this role, see [**ROLE\_SYSTEM\_TABLE**](object-roles.md).</span></span>

<span data-ttu-id="ea606-522">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-522">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-523">акчиттест</span><span class="sxs-lookup"><span data-stu-id="ea606-523">accHitTest</span></span>
-   <span data-ttu-id="ea606-524">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-524">accLocation</span></span>
-   <span data-ttu-id="ea606-525">аккнавигате</span><span class="sxs-lookup"><span data-stu-id="ea606-525">accNavigate</span></span>
-   <span data-ttu-id="ea606-526">аккселект</span><span class="sxs-lookup"><span data-stu-id="ea606-526">accSelect</span></span>
-   <span data-ttu-id="ea606-527">получить \_ аккчилд</span><span class="sxs-lookup"><span data-stu-id="ea606-527">get\_accChild</span></span>
-   <span data-ttu-id="ea606-528">получить \_ аккчилдкаунт</span><span class="sxs-lookup"><span data-stu-id="ea606-528">get\_accChildCount</span></span>
-   <span data-ttu-id="ea606-529">получить \_ аккдескриптион</span><span class="sxs-lookup"><span data-stu-id="ea606-529">get\_accDescription</span></span>
-   <span data-ttu-id="ea606-530">получить \_ аккфокус</span><span class="sxs-lookup"><span data-stu-id="ea606-530">get\_accFocus</span></span>
-   <span data-ttu-id="ea606-531">получить \_ акчелп</span><span class="sxs-lookup"><span data-stu-id="ea606-531">get\_accHelp</span></span>
-   <span data-ttu-id="ea606-532">получить \_ акчелптопик</span><span class="sxs-lookup"><span data-stu-id="ea606-532">get\_accHelpTopic</span></span>
-   <span data-ttu-id="ea606-533">получить \_ акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="ea606-533">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="ea606-534">получить \_ аккнаме</span><span class="sxs-lookup"><span data-stu-id="ea606-534">get\_accName</span></span>
-   <span data-ttu-id="ea606-535">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-535">get\_accParent</span></span>
-   <span data-ttu-id="ea606-536">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-536">get\_accRole</span></span>
-   <span data-ttu-id="ea606-537">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-537">get\_accState</span></span>

## <a name="role_system_whitespace"></a><span data-ttu-id="ea606-538">\_пробел в системе роли \_</span><span class="sxs-lookup"><span data-stu-id="ea606-538">ROLE\_SYSTEM\_WHITESPACE</span></span>

<span data-ttu-id="ea606-539">Дополнительные сведения об этой роли см. в [**разделе \_ \_ пробел в системе роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ea606-539">For more information on this role, see [**ROLE\_SYSTEM\_WHITESPACE**](object-roles.md).</span></span>

<span data-ttu-id="ea606-540">**Поддерживаемые свойства и методы**</span><span class="sxs-lookup"><span data-stu-id="ea606-540">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="ea606-541">акклокатион</span><span class="sxs-lookup"><span data-stu-id="ea606-541">accLocation</span></span>
-   <span data-ttu-id="ea606-542">аккселект</span><span class="sxs-lookup"><span data-stu-id="ea606-542">accSelect</span></span>
-   <span data-ttu-id="ea606-543">получить \_ аккпарент</span><span class="sxs-lookup"><span data-stu-id="ea606-543">get\_accParent</span></span>
-   <span data-ttu-id="ea606-544">получить \_ аккроле</span><span class="sxs-lookup"><span data-stu-id="ea606-544">get\_accRole</span></span>
-   <span data-ttu-id="ea606-545">получить \_ аккстате</span><span class="sxs-lookup"><span data-stu-id="ea606-545">get\_accState</span></span>

 

 