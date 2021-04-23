---
title: Использование подклассов темы
description: Классы темы, представляющие такие элементы управления, как ComboBox, Edit, Експлорербар, главной панели, вкладки и панель инструментов, могут быть подклассами для предоставления вариантов темы для конкретного элемента управления.
ms.assetid: 4f5e26c1-72ae-48de-a407-9ac3c0d5f502
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c5448bb5fea90193beed854e833cd34e7691b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775584"
---
# <a name="using-theme-subclasses"></a><span data-ttu-id="db093-103">Использование подклассов темы</span><span class="sxs-lookup"><span data-stu-id="db093-103">Using Theme Subclasses</span></span>

<span data-ttu-id="db093-104">Классы темы, представляющие такие элементы управления, как ComboBox, Edit, Експлорербар, главной панели, вкладки и панель инструментов, могут быть подклассами для предоставления вариантов темы для конкретного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="db093-104">Theme classes that represent controls such as ComboBox, Edit, ExplorerBar, Rebar, Tab, and Toolbar can be subclassed in order to provide theme variations for that particular control.</span></span> <span data-ttu-id="db093-105">Например, класс **Button** является подклассом, `Start::Button` чтобы обеспечить управление темой, примененной к кнопке **Start** .</span><span class="sxs-lookup"><span data-stu-id="db093-105">For example, the **Button** class is subclassed as `Start::Button` in order to provide control over the theme applied to the **Start** button.</span></span>

> [!Note]  
> <span data-ttu-id="db093-106">Будьте внимательны при создании подклассов, как описано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="db093-106">Use caution when you create subclasses like those that are discussed in this topic.</span></span> <span data-ttu-id="db093-107">Поскольку подклассы могут быть изменены или недоступны в последующих версиях Windows, вам не рекомендуется их использовать.</span><span class="sxs-lookup"><span data-stu-id="db093-107">Because subclasses might be altered or unavailable in subsequent versions of Windows, you are discouraged from using them.</span></span>

 

## <a name="two-ways-to-use-a-theme-subclass"></a><span data-ttu-id="db093-108">Два способа использования подкласса темы</span><span class="sxs-lookup"><span data-stu-id="db093-108">Two Ways to Use a Theme Subclass</span></span>

<span data-ttu-id="db093-109">Приложение может использовать тему подклассов одним из следующих двух способов:</span><span class="sxs-lookup"><span data-stu-id="db093-109">An application can use a subclassed theme in one of these two ways:</span></span>

-   <span data-ttu-id="db093-110">Она может использовать функцию [**опенсемедата**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) со строкой формы `subclass::class` в параметре *псзкласслист* .</span><span class="sxs-lookup"><span data-stu-id="db093-110">It can use the [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) function with a string of the form `subclass::class` in the *pszClassList* parameter.</span></span>
-   <span data-ttu-id="db093-111">Он может вызвать [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) с именем подкласса темы в параметре *псзсубаппнаме* .</span><span class="sxs-lookup"><span data-stu-id="db093-111">It can call [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) with the theme subclass name in the *pszSubAppName* parameter.</span></span>

## <a name="using-theme-messages-that-set-visual-style"></a><span data-ttu-id="db093-112">Использование сообщений темы, устанавливающих визуальный стиль</span><span class="sxs-lookup"><span data-stu-id="db093-112">Using Theme Messages That Set Visual Style</span></span>

<span data-ttu-id="db093-113">Некоторые элементы управления, такие как Главная панель и панели инструментов, предоставляют определенные сообщения, которые можно отправить, чтобы указать элементу управления использовать подкласс темы.</span><span class="sxs-lookup"><span data-stu-id="db093-113">Certain controls, such as Rebar and Toolbar, provide specific messages that you can send to instruct the control to use a theme subclass.</span></span> <span data-ttu-id="db093-114">Для этих элементов управления укажите указатель на буфер, содержащий имя подкласса темы в параметре *lParam* сообщения.</span><span class="sxs-lookup"><span data-stu-id="db093-114">For those controls, provide a pointer to a buffer that contains the theme subclass name in the *lParam* parameter of the message.</span></span> <span data-ttu-id="db093-115">Используйте универсальное сообщение [**CCM \_ SETWINDOWTHEME**](ccm-setwindowtheme.md) или используйте конкретный вариант, аналогичный показанному в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="db093-115">Use the generic [**CCM\_SETWINDOWTHEME**](ccm-setwindowtheme.md) message, or use a specific variant like those shown in the following table.</span></span>



| <span data-ttu-id="db093-116">Control</span><span class="sxs-lookup"><span data-stu-id="db093-116">Control</span></span>    | <span data-ttu-id="db093-117">Сообщение</span><span class="sxs-lookup"><span data-stu-id="db093-117">Message</span></span>                                             |
|------------|-----------------------------------------------------|
| <span data-ttu-id="db093-118">Всплывающая подсказка</span><span class="sxs-lookup"><span data-stu-id="db093-118">Tooltip</span></span>    | [<span data-ttu-id="db093-119">**ТТМ \_ SETWINDOWTHEME**</span><span class="sxs-lookup"><span data-stu-id="db093-119">**TTM\_SETWINDOWTHEME**</span></span>](ttm-setwindowtheme.md)   |
| <span data-ttu-id="db093-120">Панель инструментов</span><span class="sxs-lookup"><span data-stu-id="db093-120">Toolbar</span></span>    | [<span data-ttu-id="db093-121">**\_SETWINDOWTHEME ТБ**</span><span class="sxs-lookup"><span data-stu-id="db093-121">**TB\_SETWINDOWTHEME**</span></span>](tb-setwindowtheme.md)     |
| <span data-ttu-id="db093-122">Главной панели</span><span class="sxs-lookup"><span data-stu-id="db093-122">Rebar</span></span>      | [<span data-ttu-id="db093-123">**\_SETWINDOWTHEME RB**</span><span class="sxs-lookup"><span data-stu-id="db093-123">**RB\_SETWINDOWTHEME**</span></span>](rb-setwindowtheme.md)     |
| <span data-ttu-id="db093-124">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="db093-124">ComboBoxEx</span></span> | [<span data-ttu-id="db093-125">**КБЕМ \_ SETWINDOWTHEME**</span><span class="sxs-lookup"><span data-stu-id="db093-125">**CBEM\_SETWINDOWTHEME**</span></span>](cbem-setwindowtheme.md) |



 

<span data-ttu-id="db093-126">В следующей таблице перечислены некоторые подклассы, которые определяет Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="db093-126">The following table lists some of the subclasses that Windows Vista defines.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db093-127">Класс</span><span class="sxs-lookup"><span data-stu-id="db093-127">Class</span></span></th>
<th><span data-ttu-id="db093-128">используются подклассы ;</span><span class="sxs-lookup"><span data-stu-id="db093-128">Subclasses</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db093-129">ComboBox</span><span class="sxs-lookup"><span data-stu-id="db093-129">ComboBox</span></span></td>
<td><ul>
<li><span data-ttu-id="db093-130">Адрес</span><span class="sxs-lookup"><span data-stu-id="db093-130">Address</span></span></li>
<li><span data-ttu-id="db093-131">аддресскомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-131">AddressComposited</span></span></li>
<li><span data-ttu-id="db093-132">инактивеаддресс</span><span class="sxs-lookup"><span data-stu-id="db093-132">InactiveAddress</span></span></li>
<li><span data-ttu-id="db093-133">инактивеаддресскомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-133">InactiveAddressComposited</span></span></li>
<li><span data-ttu-id="db093-134">максаддресс</span><span class="sxs-lookup"><span data-stu-id="db093-134">MaxAddress</span></span></li>
<li><span data-ttu-id="db093-135">максаддресскомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-135">MaxAddressComposited</span></span></li>
<li><span data-ttu-id="db093-136">максинактивеаддресс</span><span class="sxs-lookup"><span data-stu-id="db093-136">MaxInactiveAddress</span></span></li>
<li><span data-ttu-id="db093-137">максинактивеаддресскомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-137">MaxInactiveAddressComposited</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db093-138">Изменить</span><span class="sxs-lookup"><span data-stu-id="db093-138">Edit</span></span></td>
<td><ul>
<li><span data-ttu-id="db093-139">Адрес</span><span class="sxs-lookup"><span data-stu-id="db093-139">Address</span></span></li>
<li><span data-ttu-id="db093-140">аддресскомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-140">AddressComposited</span></span></li>
<li><span data-ttu-id="db093-141">инактивеаддресс</span><span class="sxs-lookup"><span data-stu-id="db093-141">InactiveAddress</span></span></li>
<li><span data-ttu-id="db093-142">инактивеаддресскомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-142">InactiveAddressComposited</span></span></li>
<li><span data-ttu-id="db093-143">инактивесеарчбокседит</span><span class="sxs-lookup"><span data-stu-id="db093-143">InactiveSearchBoxEdit</span></span></li>
<li><span data-ttu-id="db093-144">инактивесеарчбокседиткомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-144">InactiveSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="db093-145">максаддресс</span><span class="sxs-lookup"><span data-stu-id="db093-145">MaxAddress</span></span></li>
<li><span data-ttu-id="db093-146">максаддресскомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-146">MaxAddressComposited</span></span></li>
<li><span data-ttu-id="db093-147">максинактивеаддресс</span><span class="sxs-lookup"><span data-stu-id="db093-147">MaxInactiveAddress</span></span></li>
<li><span data-ttu-id="db093-148">максинактивеаддресскомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-148">MaxInactiveAddressComposited</span></span></li>
<li><span data-ttu-id="db093-149">максинактивесеарчбокседит</span><span class="sxs-lookup"><span data-stu-id="db093-149">MaxInactiveSearchBoxEdit</span></span></li>
<li><span data-ttu-id="db093-150">максинактивесеарчбокседиткомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-150">MaxInactiveSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="db093-151">макссеарчбокседит</span><span class="sxs-lookup"><span data-stu-id="db093-151">MaxSearchBoxEdit</span></span></li>
<li><span data-ttu-id="db093-152">макссеарчбокседиткомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-152">MaxSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="db093-153">сеарчбокседит</span><span class="sxs-lookup"><span data-stu-id="db093-153">SearchBoxEdit</span></span></li>
<li><span data-ttu-id="db093-154">сеарчбокседиткомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-154">SearchBoxEditComposited</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db093-155">Главной панели</span><span class="sxs-lookup"><span data-stu-id="db093-155">Rebar</span></span></td>
<td><ul>
<li><span data-ttu-id="db093-156">бровсертаббар</span><span class="sxs-lookup"><span data-stu-id="db093-156">BrowserTabBar</span></span></li>
<li><span data-ttu-id="db093-157">инактивенавбар</span><span class="sxs-lookup"><span data-stu-id="db093-157">InactiveNavbar</span></span></li>
<li><span data-ttu-id="db093-158">инактивенавбаркомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-158">InactiveNavbarComposited</span></span></li>
<li><span data-ttu-id="db093-159">максинактивенавбар</span><span class="sxs-lookup"><span data-stu-id="db093-159">MaxInactiveNavbar</span></span></li>
<li><span data-ttu-id="db093-160">максинактивенавбаркомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-160">MaxInactiveNavbarComposited</span></span></li>
<li><span data-ttu-id="db093-161">макснавбар</span><span class="sxs-lookup"><span data-stu-id="db093-161">MaxNavbar</span></span></li>
<li><span data-ttu-id="db093-162">макснавбаркомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-162">MaxNavbarComposited</span></span></li>
<li><span data-ttu-id="db093-163">Панель навигации</span><span class="sxs-lookup"><span data-stu-id="db093-163">Navbar</span></span></li>
<li><span data-ttu-id="db093-164">навбаркомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-164">NavbarComposited</span></span></li>
<li><span data-ttu-id="db093-165">навбарнонтопмост</span><span class="sxs-lookup"><span data-stu-id="db093-165">NavbarNonTopmost</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db093-166">Вкладка</span><span class="sxs-lookup"><span data-stu-id="db093-166">Tab</span></span></td>
<td><ul>
<li><span data-ttu-id="db093-167">бровсертаб</span><span class="sxs-lookup"><span data-stu-id="db093-167">BrowserTab</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db093-168">Панель инструментов</span><span class="sxs-lookup"><span data-stu-id="db093-168">Toolbar</span></span></td>
<td><ul>
<li><span data-ttu-id="db093-169">Go</span><span class="sxs-lookup"><span data-stu-id="db093-169">Go</span></span></li>
<li><span data-ttu-id="db093-170">гокомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-170">GoComposited</span></span></li>
<li><span data-ttu-id="db093-171">инактивего</span><span class="sxs-lookup"><span data-stu-id="db093-171">InactiveGo</span></span></li>
<li><span data-ttu-id="db093-172">инактивегокомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-172">InactiveGoComposited</span></span></li>
<li><span data-ttu-id="db093-173">максго</span><span class="sxs-lookup"><span data-stu-id="db093-173">MaxGo</span></span></li>
<li><span data-ttu-id="db093-174">максгокомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-174">MaxGoComposited</span></span></li>
<li><span data-ttu-id="db093-175">максинактивего</span><span class="sxs-lookup"><span data-stu-id="db093-175">MaxInactiveGo</span></span></li>
<li><span data-ttu-id="db093-176">максинактивегокомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-176">MaxInactiveGoComposited</span></span></li>
<li><span data-ttu-id="db093-177">SearchButton</span><span class="sxs-lookup"><span data-stu-id="db093-177">SearchButton</span></span></li>
<li><span data-ttu-id="db093-178">сеарчбуттонкомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-178">SearchButtonComposited</span></span></li>
<li><span data-ttu-id="db093-179">Командировки</span><span class="sxs-lookup"><span data-stu-id="db093-179">Travel</span></span></li>
<li><span data-ttu-id="db093-180">травелкомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-180">TravelComposited</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="internet-explorer-subclasses"></a><span data-ttu-id="db093-181">Подклассы Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="db093-181">Internet Explorer Subclasses</span></span>

<span data-ttu-id="db093-182">В Windows Vista доступны подклассы определенных классов, внутренние для Windows Internet Explorer и проводника Windows, даже если сами классы отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="db093-182">In Windows Vista, the subclasses of certain classes internal to Windows Internet Explorer and Windows Explorer are available even though the classes themselves are not.</span></span> <span data-ttu-id="db093-183">В следующей таблице перечислены доступные подклассы.</span><span class="sxs-lookup"><span data-stu-id="db093-183">The following table lists the available subclasses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db093-184">аддрессбанд</span><span class="sxs-lookup"><span data-stu-id="db093-184">AddressBand</span></span></td>
<td><ul>
<li><span data-ttu-id="db093-185">AB</span><span class="sxs-lookup"><span data-stu-id="db093-185">AB</span></span></li>
<li><span data-ttu-id="db093-186">абгрин</span><span class="sxs-lookup"><span data-stu-id="db093-186">ABGreen</span></span></li>
<li><span data-ttu-id="db093-187">абгринкомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-187">ABGreenComposited</span></span></li>
<li><span data-ttu-id="db093-188">абред</span><span class="sxs-lookup"><span data-stu-id="db093-188">ABRed</span></span></li>
<li><span data-ttu-id="db093-189">абредкомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-189">ABRedComposited</span></span></li>
<li><span data-ttu-id="db093-190">абеллов</span><span class="sxs-lookup"><span data-stu-id="db093-190">ABYellow</span></span></li>
<li><span data-ttu-id="db093-191">абелловкомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-191">ABYellowComposited</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db093-192">SearchBox</span><span class="sxs-lookup"><span data-stu-id="db093-192">SearchBox</span></span></td>
<td><ul>
<li><span data-ttu-id="db093-193">инактивесеарчбокс</span><span class="sxs-lookup"><span data-stu-id="db093-193">InactiveSearchBox</span></span></li>
<li><span data-ttu-id="db093-194">инактивесеарчбокскомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-194">InactiveSearchBoxComposited</span></span></li>
<li><span data-ttu-id="db093-195">максинактивесеарчбокс</span><span class="sxs-lookup"><span data-stu-id="db093-195">MaxInactiveSearchBox</span></span></li>
<li><span data-ttu-id="db093-196">максинактивесеарчбокскомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-196">MaxInactiveSearchBoxComposited</span></span></li>
<li><span data-ttu-id="db093-197">макссеарчбокс</span><span class="sxs-lookup"><span data-stu-id="db093-197">MaxSearchBox</span></span></li>
<li><span data-ttu-id="db093-198">макссеарчбокскомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-198">MaxSearchBoxComposited</span></span></li>
<li><span data-ttu-id="db093-199">сеарчбокскомпоситед</span><span class="sxs-lookup"><span data-stu-id="db093-199">SearchBoxComposited</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="db093-200">В следующей таблице показаны особенности этих классов.</span><span class="sxs-lookup"><span data-stu-id="db093-200">The following table shows the specifics of these classes.</span></span>



| <span data-ttu-id="db093-201">Control</span><span class="sxs-lookup"><span data-stu-id="db093-201">Control</span></span>     | <span data-ttu-id="db093-202">Отделение</span><span class="sxs-lookup"><span data-stu-id="db093-202">Part</span></span>         | <span data-ttu-id="db093-203">Состояния</span><span class="sxs-lookup"><span data-stu-id="db093-203">States</span></span>                                                 |
|-------------|--------------|--------------------------------------------------------|
| <span data-ttu-id="db093-204">аддрессбанд</span><span class="sxs-lookup"><span data-stu-id="db093-204">ADDRESSBAND</span></span> | <span data-ttu-id="db093-205">аббаккграунд</span><span class="sxs-lookup"><span data-stu-id="db093-205">ABBACKGROUND</span></span> | <span data-ttu-id="db093-206">Обычная (0x1), горячий (0x2), отключен (0x3), с УПОРом (0x4)</span><span class="sxs-lookup"><span data-stu-id="db093-206">NORMAL (0x1), HOT (0x2), DISABLED (0x3), FOCUSED (0x4)</span></span> |
| <span data-ttu-id="db093-207">сеарчбокс</span><span class="sxs-lookup"><span data-stu-id="db093-207">SEARCHBOX</span></span>   | <span data-ttu-id="db093-208">сббаккграунд</span><span class="sxs-lookup"><span data-stu-id="db093-208">SBBACKGROUND</span></span> | <span data-ttu-id="db093-209">Обычная (0x1), горячий (0x2), отключен (0x3), с УПОРом (0x4)</span><span class="sxs-lookup"><span data-stu-id="db093-209">NORMAL (0x1), HOT (0x2), DISABLED (0x3), FOCUSED (0x4)</span></span> |



 

 

 




