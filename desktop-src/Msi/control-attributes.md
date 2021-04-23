---
description: Дополнительные сведения об атрибутах элементов управления см. в ссылке на конкретный элемент управления, который необходимо создать в элементах управления, а также ссылки на определенные атрибуты элемента управления в следующих списках.
ms.assetid: 948ce3d3-e463-40de-8b5f-21ef18b1a0ce
title: Атрибуты элемента управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d026e84dadefa67ce9d6e00146c6e1c2017cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347792"
---
# <a name="control-attributes"></a><span data-ttu-id="fcd72-103">Атрибуты элемента управления</span><span class="sxs-lookup"><span data-stu-id="fcd72-103">Control Attributes</span></span>

<span data-ttu-id="fcd72-104">Дополнительные сведения об атрибутах элементов управления см. в ссылке на конкретный элемент управления, который необходимо создать в [элементах управления](controls.md) , а также ссылки на определенные атрибуты элемента управления в следующих списках.</span><span class="sxs-lookup"><span data-stu-id="fcd72-104">For information on control attributes, see the link to the particular control that you need to create in [Controls](controls.md) as well as the links to particular control attributes in the following lists.</span></span>

<span data-ttu-id="fcd72-105">Для указания атрибутов элемента управления используются следующие методы:</span><span class="sxs-lookup"><span data-stu-id="fcd72-105">The following methods are used for specifying the attributes of a control:</span></span>

-   <span data-ttu-id="fcd72-106">Используйте [таблицу таблица controlcondition](controlcondition-table.md) для отключения, включения, скрытия или отображения элемента управления в соответствии со значением свойства или условного оператора.</span><span class="sxs-lookup"><span data-stu-id="fcd72-106">Use the [ControlCondition table](controlcondition-table.md) to disable, enable, hide, or show a control according to the value of a property or conditional statement.</span></span> <span data-ttu-id="fcd72-107">Эту таблицу также можно использовать для переопределения элемента управления по умолчанию, указанного в [таблице диалоговых окон](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="fcd72-107">You can also use this table to override the default control specified in the [Dialog table](dialog-table.md).</span></span>
-   <span data-ttu-id="fcd72-108">Подпишите элемент управления на таблице ControlEvent событие в [таблице таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="fcd72-108">Subscribe the control to a ControlEvent in the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="fcd72-109">Введите идентификатор атрибута в столбце атрибут и идентификатор таблице ControlEvent событие в столбце Event этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="fcd72-109">Enter the attribute's identifier in the Attribute column and the ControlEvent's identifier in the Event column of this table.</span></span>
-   <span data-ttu-id="fcd72-110">Задайте битовые флаги атрибута элемента управления в столбце Атрибут [таблицы Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="fcd72-110">Set the control attribute bit flags for the control in the Attribute column of the [Control table](control-table.md).</span></span> <span data-ttu-id="fcd72-111">Это задает атрибуты при создании элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fcd72-111">This sets the attributes upon the creation of the control.</span></span>

<span data-ttu-id="fcd72-112">Некоторые атрибуты не могут быть заданы для каждого элемента управления или заданы всеми вышеупомянутыми методами.</span><span class="sxs-lookup"><span data-stu-id="fcd72-112">Some attributes cannot be set for every control or be specified by all of the above methods.</span></span> <span data-ttu-id="fcd72-113">Дополнительные сведения см. в разделах, посвященных конкретным элементам управления и атрибутам.</span><span class="sxs-lookup"><span data-stu-id="fcd72-113">See the particular control and attribute topics for details.</span></span>

<span data-ttu-id="fcd72-114">Начальные значения некоторых атрибутов элементов управления можно задать с помощью битов в [таблице управления](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="fcd72-114">The initial values of some control attributes can be set with bits in the [Control table](control-table.md).</span></span>



| <span data-ttu-id="fcd72-115">attribute</span><span class="sxs-lookup"><span data-stu-id="fcd72-115">Attribute</span></span>                                          | <span data-ttu-id="fcd72-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="fcd72-116">Decimal</span></span> | <span data-ttu-id="fcd72-117">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="fcd72-117">Hexadecimal</span></span> | <span data-ttu-id="fcd72-118">Константа</span><span class="sxs-lookup"><span data-stu-id="fcd72-118">Constant</span></span>                               |
|----------------------------------------------------|---------|-------------|----------------------------------------|
| [<span data-ttu-id="fcd72-119">Письмо</span><span class="sxs-lookup"><span data-stu-id="fcd72-119">BiDi</span></span>](bidi-control-attribute.md)                 | <span data-ttu-id="fcd72-120">224</span><span class="sxs-lookup"><span data-stu-id="fcd72-120">224</span></span>     | <span data-ttu-id="fcd72-121">0x000000E0</span><span class="sxs-lookup"><span data-stu-id="fcd72-121">0x000000E0</span></span>  | <span data-ttu-id="fcd72-122">**мсидбконтролаттрибутесбиди**</span><span class="sxs-lookup"><span data-stu-id="fcd72-122">**msidbControlAttributesBiDi**</span></span>         |
| [<span data-ttu-id="fcd72-123">Enabled</span><span class="sxs-lookup"><span data-stu-id="fcd72-123">Enabled</span></span>](enabled-control-attribute.md)           | <span data-ttu-id="fcd72-124">2</span><span class="sxs-lookup"><span data-stu-id="fcd72-124">2</span></span>       | <span data-ttu-id="fcd72-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="fcd72-125">0x00000002</span></span>  | <span data-ttu-id="fcd72-126">**мсидбконтролаттрибутесенаблед**</span><span class="sxs-lookup"><span data-stu-id="fcd72-126">**msidbControlAttributesEnabled**</span></span>      |
| [<span data-ttu-id="fcd72-127">Косвенные</span><span class="sxs-lookup"><span data-stu-id="fcd72-127">Indirect</span></span>](indirect-control-attribute.md)         | <span data-ttu-id="fcd72-128">8</span><span class="sxs-lookup"><span data-stu-id="fcd72-128">8</span></span>       | <span data-ttu-id="fcd72-129">0x00000008</span><span class="sxs-lookup"><span data-stu-id="fcd72-129">0x00000008</span></span>  | <span data-ttu-id="fcd72-130">**мсидбконтролаттрибутесиндирект**</span><span class="sxs-lookup"><span data-stu-id="fcd72-130">**msidbControlAttributesIndirect**</span></span>     |
| [<span data-ttu-id="fcd72-131">Целочисленный элемент управления</span><span class="sxs-lookup"><span data-stu-id="fcd72-131">Integer Control</span></span>](integer-control-attribute.md)   | <span data-ttu-id="fcd72-132">16</span><span class="sxs-lookup"><span data-stu-id="fcd72-132">16</span></span>      | <span data-ttu-id="fcd72-133">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fcd72-133">0x00000010</span></span>  | <span data-ttu-id="fcd72-134">**мсидбконтролаттрибутесинтежер**</span><span class="sxs-lookup"><span data-stu-id="fcd72-134">**msidbControlAttributesInteger**</span></span>      |
| [<span data-ttu-id="fcd72-135">лефтскролл</span><span class="sxs-lookup"><span data-stu-id="fcd72-135">LeftScroll</span></span>](leftscroll-control-attribute.md)     | <span data-ttu-id="fcd72-136">128</span><span class="sxs-lookup"><span data-stu-id="fcd72-136">128</span></span>     | <span data-ttu-id="fcd72-137">0x00000080</span><span class="sxs-lookup"><span data-stu-id="fcd72-137">0x00000080</span></span>  | <span data-ttu-id="fcd72-138">**мсидбконтролаттрибутеслефтскролл**</span><span class="sxs-lookup"><span data-stu-id="fcd72-138">**msidbControlAttributesLeftScroll**</span></span>   |
| [<span data-ttu-id="fcd72-139">ригхталигнед</span><span class="sxs-lookup"><span data-stu-id="fcd72-139">RightAligned</span></span>](rightaligned-control-attribute.md) | <span data-ttu-id="fcd72-140">64</span><span class="sxs-lookup"><span data-stu-id="fcd72-140">64</span></span>      | <span data-ttu-id="fcd72-141">0x00000040</span><span class="sxs-lookup"><span data-stu-id="fcd72-141">0x00000040</span></span>  | <span data-ttu-id="fcd72-142">**мсидбконтролаттрибутесригхталигнед**</span><span class="sxs-lookup"><span data-stu-id="fcd72-142">**msidbControlAttributesRightAligned**</span></span> |
| [<span data-ttu-id="fcd72-143">ртлро</span><span class="sxs-lookup"><span data-stu-id="fcd72-143">RTLRO</span></span>](rtlro-control-attribute.md)               | <span data-ttu-id="fcd72-144">32</span><span class="sxs-lookup"><span data-stu-id="fcd72-144">32</span></span>      | <span data-ttu-id="fcd72-145">0x00000020</span><span class="sxs-lookup"><span data-stu-id="fcd72-145">0x00000020</span></span>  | <span data-ttu-id="fcd72-146">**мсидбконтролаттрибутесртлро**</span><span class="sxs-lookup"><span data-stu-id="fcd72-146">**msidbControlAttributesRTLRO**</span></span>        |
| [<span data-ttu-id="fcd72-147">Sunken</span><span class="sxs-lookup"><span data-stu-id="fcd72-147">Sunken</span></span>](sunken-control-attribute.md)             | <span data-ttu-id="fcd72-148">4</span><span class="sxs-lookup"><span data-stu-id="fcd72-148">4</span></span>       | <span data-ttu-id="fcd72-149">0x00000004</span><span class="sxs-lookup"><span data-stu-id="fcd72-149">0x00000004</span></span>  | <span data-ttu-id="fcd72-150">**мсидбконтролаттрибутессункен**</span><span class="sxs-lookup"><span data-stu-id="fcd72-150">**msidbControlAttributesSunken**</span></span>       |
| [<span data-ttu-id="fcd72-151">Visible</span><span class="sxs-lookup"><span data-stu-id="fcd72-151">Visible</span></span>](visible-control-attribute.md)           | <span data-ttu-id="fcd72-152">1</span><span class="sxs-lookup"><span data-stu-id="fcd72-152">1</span></span>       | <span data-ttu-id="fcd72-153">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fcd72-153">0x00000001</span></span>  | <span data-ttu-id="fcd72-154">**мсидбконтролаттрибутесвисибле**</span><span class="sxs-lookup"><span data-stu-id="fcd72-154">**msidbControlAttributesVisible**</span></span>      |



 

<span data-ttu-id="fcd72-155">Эти атрибуты элементов управления "текст" задаются с помощью битов.</span><span class="sxs-lookup"><span data-stu-id="fcd72-155">These attributes of Text controls are set with bits.</span></span>



| <span data-ttu-id="fcd72-156">attribute</span><span class="sxs-lookup"><span data-stu-id="fcd72-156">Attribute</span></span>                                            | <span data-ttu-id="fcd72-157">Decimal</span><span class="sxs-lookup"><span data-stu-id="fcd72-157">Decimal</span></span> | <span data-ttu-id="fcd72-158">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="fcd72-158">Hexadecimal</span></span> | <span data-ttu-id="fcd72-159">Константа</span><span class="sxs-lookup"><span data-stu-id="fcd72-159">Constant</span></span>                                |
|------------------------------------------------------|---------|-------------|-----------------------------------------|
| [<span data-ttu-id="fcd72-160">форматсизе</span><span class="sxs-lookup"><span data-stu-id="fcd72-160">FormatSize</span></span>](formatsize-control-attribute.md)       | <span data-ttu-id="fcd72-161">524288</span><span class="sxs-lookup"><span data-stu-id="fcd72-161">524288</span></span>  | <span data-ttu-id="fcd72-162">0x00080000</span><span class="sxs-lookup"><span data-stu-id="fcd72-162">0x00080000</span></span>  | <span data-ttu-id="fcd72-163">**мсидбконтролаттрибутесформатсизе**</span><span class="sxs-lookup"><span data-stu-id="fcd72-163">**msidbControlAttributesFormatSize**</span></span>    |
| [<span data-ttu-id="fcd72-164">Префикс не</span><span class="sxs-lookup"><span data-stu-id="fcd72-164">NoPrefix</span></span>](noprefix-control-attribute.md)           | <span data-ttu-id="fcd72-165">131072</span><span class="sxs-lookup"><span data-stu-id="fcd72-165">131072</span></span>  | <span data-ttu-id="fcd72-166">0x00020000</span><span class="sxs-lookup"><span data-stu-id="fcd72-166">0x00020000</span></span>  | <span data-ttu-id="fcd72-167">**мсидбконтролаттрибутеснопрефикс**</span><span class="sxs-lookup"><span data-stu-id="fcd72-167">**msidbControlAttributesNoPrefix**</span></span>      |
| [<span data-ttu-id="fcd72-168">Не переносить</span><span class="sxs-lookup"><span data-stu-id="fcd72-168">NoWrap</span></span>](nowrap-control-attribute.md)               | <span data-ttu-id="fcd72-169">262144</span><span class="sxs-lookup"><span data-stu-id="fcd72-169">262144</span></span>  | <span data-ttu-id="fcd72-170">0x00040000</span><span class="sxs-lookup"><span data-stu-id="fcd72-170">0x00040000</span></span>  | <span data-ttu-id="fcd72-171">**мсидбконтролаттрибутесноврап**</span><span class="sxs-lookup"><span data-stu-id="fcd72-171">**msidbControlAttributesNoWrap**</span></span>        |
| [<span data-ttu-id="fcd72-172">Пароль</span><span class="sxs-lookup"><span data-stu-id="fcd72-172">Password</span></span>](password-control-attribute.md)           | <span data-ttu-id="fcd72-173">2097152</span><span class="sxs-lookup"><span data-stu-id="fcd72-173">2097152</span></span> | <span data-ttu-id="fcd72-174">0x00200000</span><span class="sxs-lookup"><span data-stu-id="fcd72-174">0x00200000</span></span>  | <span data-ttu-id="fcd72-175">**мсидбконтролаттрибутеспассвординпут**</span><span class="sxs-lookup"><span data-stu-id="fcd72-175">**msidbControlAttributesPasswordInput**</span></span> |
| [<span data-ttu-id="fcd72-176">Прозрачный</span><span class="sxs-lookup"><span data-stu-id="fcd72-176">Transparent</span></span>](transparent-control-attribute.md)     | <span data-ttu-id="fcd72-177">65536</span><span class="sxs-lookup"><span data-stu-id="fcd72-177">65536</span></span>   | <span data-ttu-id="fcd72-178">0x00010000</span><span class="sxs-lookup"><span data-stu-id="fcd72-178">0x00010000</span></span>  | <span data-ttu-id="fcd72-179">**мсидбконтролаттрибутестранспарент**</span><span class="sxs-lookup"><span data-stu-id="fcd72-179">**msidbControlAttributesTransparent**</span></span>   |
| [<span data-ttu-id="fcd72-180">усерслангуаже</span><span class="sxs-lookup"><span data-stu-id="fcd72-180">UsersLanguage</span></span>](userslanguage-control-attribute.md) | <span data-ttu-id="fcd72-181">1048576</span><span class="sxs-lookup"><span data-stu-id="fcd72-181">1048576</span></span> | <span data-ttu-id="fcd72-182">0x00100000</span><span class="sxs-lookup"><span data-stu-id="fcd72-182">0x00100000</span></span>  | <span data-ttu-id="fcd72-183">**мсидбконтролаттрибутесусерслангуаже**</span><span class="sxs-lookup"><span data-stu-id="fcd72-183">**msidbControlAttributesUsersLanguage**</span></span> |



 

<span data-ttu-id="fcd72-184">Для этого атрибута элемента управления ProgressBar задается бит.</span><span class="sxs-lookup"><span data-stu-id="fcd72-184">This attribute of the ProgressBar control is set with a bit.</span></span>



| <span data-ttu-id="fcd72-185">attribute</span><span class="sxs-lookup"><span data-stu-id="fcd72-185">Attribute</span></span>                                      | <span data-ttu-id="fcd72-186">Decimal</span><span class="sxs-lookup"><span data-stu-id="fcd72-186">Decimal</span></span> | <span data-ttu-id="fcd72-187">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="fcd72-187">Hexadecimal</span></span> | <span data-ttu-id="fcd72-188">Константа</span><span class="sxs-lookup"><span data-stu-id="fcd72-188">Constant</span></span>                             |
|------------------------------------------------|---------|-------------|--------------------------------------|
| [<span data-ttu-id="fcd72-189">Progress95</span><span class="sxs-lookup"><span data-stu-id="fcd72-189">Progress95</span></span>](progress95-control-attribute.md) | <span data-ttu-id="fcd72-190">65536</span><span class="sxs-lookup"><span data-stu-id="fcd72-190">65536</span></span>   | <span data-ttu-id="fcd72-191">0x00010000</span><span class="sxs-lookup"><span data-stu-id="fcd72-191">0x00010000</span></span>  | <span data-ttu-id="fcd72-192">**msidbControlAttributesProgress95**</span><span class="sxs-lookup"><span data-stu-id="fcd72-192">**msidbControlAttributesProgress95**</span></span> |



 

<span data-ttu-id="fcd72-193">Эти атрибуты элементов управления томами и Селекткомбо каталога задаются с помощью BITS.</span><span class="sxs-lookup"><span data-stu-id="fcd72-193">These attributes of Volume and Directory SelectCombo controls are set with bits.</span></span>



| <span data-ttu-id="fcd72-194">attribute</span><span class="sxs-lookup"><span data-stu-id="fcd72-194">Attribute</span></span>                                                | <span data-ttu-id="fcd72-195">Decimal</span><span class="sxs-lookup"><span data-stu-id="fcd72-195">Decimal</span></span> | <span data-ttu-id="fcd72-196">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="fcd72-196">Hexadecimal</span></span> | <span data-ttu-id="fcd72-197">Константа</span><span class="sxs-lookup"><span data-stu-id="fcd72-197">Constant</span></span>                                  |
|----------------------------------------------------------|---------|-------------|-------------------------------------------|
| [<span data-ttu-id="fcd72-198">кдромволуме</span><span class="sxs-lookup"><span data-stu-id="fcd72-198">CDROMVolume</span></span>](cdromvolume-control-attribute.md)         | <span data-ttu-id="fcd72-199">524288</span><span class="sxs-lookup"><span data-stu-id="fcd72-199">524288</span></span>  | <span data-ttu-id="fcd72-200">0x00080000</span><span class="sxs-lookup"><span data-stu-id="fcd72-200">0x00080000</span></span>  | <span data-ttu-id="fcd72-201">**мсидбконтролаттрибутескдромволуме**</span><span class="sxs-lookup"><span data-stu-id="fcd72-201">**msidbControlAttributesCDROMVolume**</span></span>     |
| [<span data-ttu-id="fcd72-202">фикседволуме</span><span class="sxs-lookup"><span data-stu-id="fcd72-202">FixedVolume</span></span>](fixedvolume-control-attribute.md)         | <span data-ttu-id="fcd72-203">131072</span><span class="sxs-lookup"><span data-stu-id="fcd72-203">131072</span></span>  | <span data-ttu-id="fcd72-204">0x00020000</span><span class="sxs-lookup"><span data-stu-id="fcd72-204">0x00020000</span></span>  | <span data-ttu-id="fcd72-205">**мсидбконтролаттрибутесфикседволуме**</span><span class="sxs-lookup"><span data-stu-id="fcd72-205">**msidbControlAttributesFixedVolume**</span></span>     |
| [<span data-ttu-id="fcd72-206">флоппиволуме</span><span class="sxs-lookup"><span data-stu-id="fcd72-206">FloppyVolume</span></span>](floppyvolume-control-attribute.md)       | <span data-ttu-id="fcd72-207">2097152</span><span class="sxs-lookup"><span data-stu-id="fcd72-207">2097152</span></span> | <span data-ttu-id="fcd72-208">0x00200000</span><span class="sxs-lookup"><span data-stu-id="fcd72-208">0x00200000</span></span>  | <span data-ttu-id="fcd72-209">**мсидбконтролаттрибутесфлоппиволуме**</span><span class="sxs-lookup"><span data-stu-id="fcd72-209">**msidbControlAttributesFloppyVolume**</span></span>    |
| [<span data-ttu-id="fcd72-210">рамдискволуме</span><span class="sxs-lookup"><span data-stu-id="fcd72-210">RAMDiskVolume</span></span>](ramdiskvolume-control-attribute.md)     | <span data-ttu-id="fcd72-211">1048576</span><span class="sxs-lookup"><span data-stu-id="fcd72-211">1048576</span></span> | <span data-ttu-id="fcd72-212">0x00100000</span><span class="sxs-lookup"><span data-stu-id="fcd72-212">0x00100000</span></span>  | <span data-ttu-id="fcd72-213">**мсидбконтролаттрибутесрамдискволуме**</span><span class="sxs-lookup"><span data-stu-id="fcd72-213">**msidbControlAttributesRAMDiskVolume**</span></span>   |
| [<span data-ttu-id="fcd72-214">ремотеволуме</span><span class="sxs-lookup"><span data-stu-id="fcd72-214">RemoteVolume</span></span>](remotevolume-control-attribute.md)       | <span data-ttu-id="fcd72-215">262144</span><span class="sxs-lookup"><span data-stu-id="fcd72-215">262144</span></span>  | <span data-ttu-id="fcd72-216">0x00040000</span><span class="sxs-lookup"><span data-stu-id="fcd72-216">0x00040000</span></span>  | <span data-ttu-id="fcd72-217">**мсидбконтролаттрибутесремотеволуме**</span><span class="sxs-lookup"><span data-stu-id="fcd72-217">**msidbControlAttributesRemoteVolume**</span></span>    |
| [<span data-ttu-id="fcd72-218">ремоваблеволуме</span><span class="sxs-lookup"><span data-stu-id="fcd72-218">RemovableVolume</span></span>](removablevolume-control-attribute.md) | <span data-ttu-id="fcd72-219">65536</span><span class="sxs-lookup"><span data-stu-id="fcd72-219">65536</span></span>   | <span data-ttu-id="fcd72-220">0x00010000</span><span class="sxs-lookup"><span data-stu-id="fcd72-220">0x00010000</span></span>  | <span data-ttu-id="fcd72-221">**мсидбконтролаттрибутесремоваблеволуме**</span><span class="sxs-lookup"><span data-stu-id="fcd72-221">**msidbControlAttributesRemovableVolume**</span></span> |



 

<span data-ttu-id="fcd72-222">Эти атрибуты элементов управления ListBox и ComboBox задаются с помощью битов.</span><span class="sxs-lookup"><span data-stu-id="fcd72-222">These attributes of ListBox and ComboBox controls are set with bits.</span></span>



| <span data-ttu-id="fcd72-223">attribute</span><span class="sxs-lookup"><span data-stu-id="fcd72-223">Attribute</span></span>                                            | <span data-ttu-id="fcd72-224">Decimal</span><span class="sxs-lookup"><span data-stu-id="fcd72-224">Decimal</span></span> | <span data-ttu-id="fcd72-225">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="fcd72-225">Hexadecimal</span></span> | <span data-ttu-id="fcd72-226">Константа</span><span class="sxs-lookup"><span data-stu-id="fcd72-226">Constant</span></span>                            |
|------------------------------------------------------|---------|-------------|-------------------------------------|
| [<span data-ttu-id="fcd72-227">Элемент управления Комболист</span><span class="sxs-lookup"><span data-stu-id="fcd72-227">ComboList Control</span></span>](combolist-control-attribute.md) | <span data-ttu-id="fcd72-228">131072</span><span class="sxs-lookup"><span data-stu-id="fcd72-228">131072</span></span>  | <span data-ttu-id="fcd72-229">0x00020000</span><span class="sxs-lookup"><span data-stu-id="fcd72-229">0x00020000</span></span>  | <span data-ttu-id="fcd72-230">**мсидбконтролаттрибутескомболист**</span><span class="sxs-lookup"><span data-stu-id="fcd72-230">**msidbControlAttributesComboList**</span></span> |
| [<span data-ttu-id="fcd72-231">Отсортированный элемент управления</span><span class="sxs-lookup"><span data-stu-id="fcd72-231">Sorted Control</span></span>](sorted-control-attribute.md)       | <span data-ttu-id="fcd72-232">65536</span><span class="sxs-lookup"><span data-stu-id="fcd72-232">65536</span></span>   | <span data-ttu-id="fcd72-233">0x00010000</span><span class="sxs-lookup"><span data-stu-id="fcd72-233">0x00010000</span></span>  | <span data-ttu-id="fcd72-234">**мсидбконтролаттрибутессортед**</span><span class="sxs-lookup"><span data-stu-id="fcd72-234">**msidbControlAttributesSorted**</span></span>    |



 

<span data-ttu-id="fcd72-235">Для этого атрибута элемента управления "поле ввода" задан бит.</span><span class="sxs-lookup"><span data-stu-id="fcd72-235">This attribute of the Edit control is set with a bit.</span></span>



| <span data-ttu-id="fcd72-236">attribute</span><span class="sxs-lookup"><span data-stu-id="fcd72-236">Attribute</span></span>                                    | <span data-ttu-id="fcd72-237">Decimal</span><span class="sxs-lookup"><span data-stu-id="fcd72-237">Decimal</span></span> | <span data-ttu-id="fcd72-238">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="fcd72-238">Hexadecimal</span></span> | <span data-ttu-id="fcd72-239">Константа</span><span class="sxs-lookup"><span data-stu-id="fcd72-239">Constant</span></span>                            |
|----------------------------------------------|---------|-------------|-------------------------------------|
| [<span data-ttu-id="fcd72-240">Нескольких</span><span class="sxs-lookup"><span data-stu-id="fcd72-240">MultiLine</span></span>](multiline-control-attribute.md) | <span data-ttu-id="fcd72-241">65536</span><span class="sxs-lookup"><span data-stu-id="fcd72-241">65536</span></span>   | <span data-ttu-id="fcd72-242">0x00010000</span><span class="sxs-lookup"><span data-stu-id="fcd72-242">0x00010000</span></span>  | <span data-ttu-id="fcd72-243">**мсидбконтролаттрибутесмултилине**</span><span class="sxs-lookup"><span data-stu-id="fcd72-243">**msidbControlAttributesMultiline**</span></span> |



 

<span data-ttu-id="fcd72-244">Эти атрибуты элементов управления Пиктуребуттон задаются с помощью битов.</span><span class="sxs-lookup"><span data-stu-id="fcd72-244">These attributes of PictureButton controls are set with bits.</span></span>



| <span data-ttu-id="fcd72-245">attribute</span><span class="sxs-lookup"><span data-stu-id="fcd72-245">Attribute</span></span>                                          | <span data-ttu-id="fcd72-246">Decimal</span><span class="sxs-lookup"><span data-stu-id="fcd72-246">Decimal</span></span> | <span data-ttu-id="fcd72-247">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="fcd72-247">Hexadecimal</span></span> | <span data-ttu-id="fcd72-248">Константа</span><span class="sxs-lookup"><span data-stu-id="fcd72-248">Constant</span></span>                             |
|----------------------------------------------------|---------|-------------|--------------------------------------|
| [<span data-ttu-id="fcd72-249">Bitmap</span><span class="sxs-lookup"><span data-stu-id="fcd72-249">Bitmap</span></span>](bitmap-control-attribute.md)             | <span data-ttu-id="fcd72-250">262144</span><span class="sxs-lookup"><span data-stu-id="fcd72-250">262144</span></span>  | <span data-ttu-id="fcd72-251">0x00040000</span><span class="sxs-lookup"><span data-stu-id="fcd72-251">0x00040000</span></span>  | <span data-ttu-id="fcd72-252">**мсидбконтролаттрибутесбитмап**</span><span class="sxs-lookup"><span data-stu-id="fcd72-252">**msidbControlAttributesBitmap**</span></span>     |
| [<span data-ttu-id="fcd72-253">FixedSize</span><span class="sxs-lookup"><span data-stu-id="fcd72-253">FixedSize</span></span>](fixedsize-control-attribute.md)       | <span data-ttu-id="fcd72-254">1048576</span><span class="sxs-lookup"><span data-stu-id="fcd72-254">1048576</span></span> | <span data-ttu-id="fcd72-255">0x00100000</span><span class="sxs-lookup"><span data-stu-id="fcd72-255">0x00100000</span></span>  | <span data-ttu-id="fcd72-256">**мсидбконтролаттрибутесфикседсизе**</span><span class="sxs-lookup"><span data-stu-id="fcd72-256">**msidbControlAttributesFixedSize**</span></span>  |
| <span data-ttu-id="fcd72-257">[Значок](icon-control-attribute.md):</span><span class="sxs-lookup"><span data-stu-id="fcd72-257">[Icon](icon-control-attribute.md)</span></span>                 | <span data-ttu-id="fcd72-258">524288</span><span class="sxs-lookup"><span data-stu-id="fcd72-258">524288</span></span>  | <span data-ttu-id="fcd72-259">0x00080000</span><span class="sxs-lookup"><span data-stu-id="fcd72-259">0x00080000</span></span>  | <span data-ttu-id="fcd72-260">**мсидбконтролаттрибутесикон**</span><span class="sxs-lookup"><span data-stu-id="fcd72-260">**msidbControlAttributesIcon**</span></span>       |
| [<span data-ttu-id="fcd72-261">IconSize16</span><span class="sxs-lookup"><span data-stu-id="fcd72-261">IconSize16</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="fcd72-262">2097152</span><span class="sxs-lookup"><span data-stu-id="fcd72-262">2097152</span></span> | <span data-ttu-id="fcd72-263">0x00200000</span><span class="sxs-lookup"><span data-stu-id="fcd72-263">0x00200000</span></span>  | <span data-ttu-id="fcd72-264">**msidbControlAttributesIconSize16**</span><span class="sxs-lookup"><span data-stu-id="fcd72-264">**msidbControlAttributesIconSize16**</span></span> |
| [<span data-ttu-id="fcd72-265">IconSize32</span><span class="sxs-lookup"><span data-stu-id="fcd72-265">IconSize32</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="fcd72-266">4194304</span><span class="sxs-lookup"><span data-stu-id="fcd72-266">4194304</span></span> | <span data-ttu-id="fcd72-267">0x00400000</span><span class="sxs-lookup"><span data-stu-id="fcd72-267">0x00400000</span></span>  | <span data-ttu-id="fcd72-268">**msidbControlAttributesIconSize32**</span><span class="sxs-lookup"><span data-stu-id="fcd72-268">**msidbControlAttributesIconSize32**</span></span> |
| [<span data-ttu-id="fcd72-269">IconSize48</span><span class="sxs-lookup"><span data-stu-id="fcd72-269">IconSize48</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="fcd72-270">6291456</span><span class="sxs-lookup"><span data-stu-id="fcd72-270">6291456</span></span> | <span data-ttu-id="fcd72-271">0x00600000</span><span class="sxs-lookup"><span data-stu-id="fcd72-271">0x00600000</span></span>  | <span data-ttu-id="fcd72-272">**msidbControlAttributesIconSize48**</span><span class="sxs-lookup"><span data-stu-id="fcd72-272">**msidbControlAttributesIconSize48**</span></span> |
| [<span data-ttu-id="fcd72-273">Элемент управления Пушлике</span><span class="sxs-lookup"><span data-stu-id="fcd72-273">PushLike Control</span></span>](pushlike-control-attribute.md) | <span data-ttu-id="fcd72-274">131072</span><span class="sxs-lookup"><span data-stu-id="fcd72-274">131072</span></span>  | <span data-ttu-id="fcd72-275">0x00020000</span><span class="sxs-lookup"><span data-stu-id="fcd72-275">0x00020000</span></span>  | <span data-ttu-id="fcd72-276">**мсидбконтролаттрибутеспушлике**</span><span class="sxs-lookup"><span data-stu-id="fcd72-276">**msidbControlAttributesPushLike**</span></span>   |



 

<span data-ttu-id="fcd72-277">Этот атрибут элемента управления RadioButton задается битом.</span><span class="sxs-lookup"><span data-stu-id="fcd72-277">This attribute of RadioButton control is set with a bit.</span></span>



| <span data-ttu-id="fcd72-278">attribute</span><span class="sxs-lookup"><span data-stu-id="fcd72-278">Attribute</span></span>                                    | <span data-ttu-id="fcd72-279">Decimal</span><span class="sxs-lookup"><span data-stu-id="fcd72-279">Decimal</span></span>  | <span data-ttu-id="fcd72-280">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="fcd72-280">Hexadecimal</span></span> | <span data-ttu-id="fcd72-281">Константа</span><span class="sxs-lookup"><span data-stu-id="fcd72-281">Constant</span></span>                            |
|----------------------------------------------|----------|-------------|-------------------------------------|
| [<span data-ttu-id="fcd72-282">хасбордер</span><span class="sxs-lookup"><span data-stu-id="fcd72-282">HasBorder</span></span>](hasborder-control-attribute.md) | <span data-ttu-id="fcd72-283">16777216</span><span class="sxs-lookup"><span data-stu-id="fcd72-283">16777216</span></span> | <span data-ttu-id="fcd72-284">0x01000000</span><span class="sxs-lookup"><span data-stu-id="fcd72-284">0x01000000</span></span>  | <span data-ttu-id="fcd72-285">**мсидбконтролаттрибутешасбордер**</span><span class="sxs-lookup"><span data-stu-id="fcd72-285">**msidbControlAttributesHasBorder**</span></span> |



 

<span data-ttu-id="fcd72-286">Этот атрибут элемента управления "Кнопка" задан с битом.</span><span class="sxs-lookup"><span data-stu-id="fcd72-286">This attribute of PushButton control is set with a bit.</span></span>



| <span data-ttu-id="fcd72-287">attribute</span><span class="sxs-lookup"><span data-stu-id="fcd72-287">Attribute</span></span>                                        | <span data-ttu-id="fcd72-288">Decimal</span><span class="sxs-lookup"><span data-stu-id="fcd72-288">Decimal</span></span> | <span data-ttu-id="fcd72-289">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="fcd72-289">Hexadecimal</span></span> | <span data-ttu-id="fcd72-290">Константа</span><span class="sxs-lookup"><span data-stu-id="fcd72-290">Constant</span></span>                                  |
|--------------------------------------------------|---------|-------------|-------------------------------------------|
| [<span data-ttu-id="fcd72-291">елеватионшиелд</span><span class="sxs-lookup"><span data-stu-id="fcd72-291">ElevationShield</span></span>](elevationshield-attribute.md) | <span data-ttu-id="fcd72-292">8388608</span><span class="sxs-lookup"><span data-stu-id="fcd72-292">8388608</span></span> | <span data-ttu-id="fcd72-293">0x00800000</span><span class="sxs-lookup"><span data-stu-id="fcd72-293">0x00800000</span></span>  | <span data-ttu-id="fcd72-294">**мсидбконтролаттрибутеселеватионшиелд**</span><span class="sxs-lookup"><span data-stu-id="fcd72-294">**msidbControlAttributesElevationShield**</span></span> |



 

<span data-ttu-id="fcd72-295">Для этого атрибута элемента управления Волумекостлист задан бит.</span><span class="sxs-lookup"><span data-stu-id="fcd72-295">This attribute of VolumeCostList control is set with a bit.</span></span>



| <span data-ttu-id="fcd72-296">attribute</span><span class="sxs-lookup"><span data-stu-id="fcd72-296">Attribute</span></span>                                                                | <span data-ttu-id="fcd72-297">Decimal</span><span class="sxs-lookup"><span data-stu-id="fcd72-297">Decimal</span></span> | <span data-ttu-id="fcd72-298">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="fcd72-298">Hexadecimal</span></span> | <span data-ttu-id="fcd72-299">Константа</span><span class="sxs-lookup"><span data-stu-id="fcd72-299">Constant</span></span>                         |
|--------------------------------------------------------------------------|---------|-------------|----------------------------------|
| [<span data-ttu-id="fcd72-300">контролшовроллбакккост</span><span class="sxs-lookup"><span data-stu-id="fcd72-300">ControlShowRollbackCost</span></span>](controlshowrollbackcost-control-attribute.md) | <span data-ttu-id="fcd72-301">4194304</span><span class="sxs-lookup"><span data-stu-id="fcd72-301">4194304</span></span> | <span data-ttu-id="fcd72-302">0x00400000</span><span class="sxs-lookup"><span data-stu-id="fcd72-302">0x00400000</span></span>  | <span data-ttu-id="fcd72-303">**мсидбконтролшовроллбакккост**</span><span class="sxs-lookup"><span data-stu-id="fcd72-303">**msidbControlShowRollbackCost**</span></span> |



 

<span data-ttu-id="fcd72-304">Следующие атрибуты элемента управления не задаются с помощью BITS.</span><span class="sxs-lookup"><span data-stu-id="fcd72-304">The following control attributes are not set with bits.</span></span> <span data-ttu-id="fcd72-305">Эти атрибуты созданы в таблицах пользовательского интерфейса или задаются с помощью [событий элемента управления](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="fcd72-305">These attributes are authored into the user interface tables or are set using [Control Events](control-events.md).</span></span>

[<span data-ttu-id="fcd72-306">биллбоарднаме</span><span class="sxs-lookup"><span data-stu-id="fcd72-306">BillboardName</span></span>](billboardname-control-attribute.md)

 

[<span data-ttu-id="fcd72-307">индиректпропертинаме</span><span class="sxs-lookup"><span data-stu-id="fcd72-307">IndirectPropertyName</span></span>](indirectpropertyname-control-attribute.md)

 

[<span data-ttu-id="fcd72-308">Позиция</span><span class="sxs-lookup"><span data-stu-id="fcd72-308">Position</span></span>](position-control-attribute.md)

 

[<span data-ttu-id="fcd72-309">Управление ходом выполнения</span><span class="sxs-lookup"><span data-stu-id="fcd72-309">Progress Control</span></span>](progress-control-attribute.md)

 

[<span data-ttu-id="fcd72-310">PropertyName</span><span class="sxs-lookup"><span data-stu-id="fcd72-310">PropertyName</span></span>](propertyname-control-attribute.md)

 

[<span data-ttu-id="fcd72-311">PropertyValue</span><span class="sxs-lookup"><span data-stu-id="fcd72-311">PropertyValue</span></span>](propertyvalue-control-attribute.md)

 

[<span data-ttu-id="fcd72-312">Text Control</span><span class="sxs-lookup"><span data-stu-id="fcd72-312">Text Control</span></span>](text-control-attribute.md)

 

[<span data-ttu-id="fcd72-313">TimeRemaining</span><span class="sxs-lookup"><span data-stu-id="fcd72-313">TimeRemaining</span></span>](timeremaining-control-attribute.md)

<span data-ttu-id="fcd72-314">См. раздел [Добавление элементов управления и текста](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="fcd72-314">See [Adding Controls and Text](adding-controls-and-text.md).</span></span>

 

 



