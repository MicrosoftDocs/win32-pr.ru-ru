---
title: Ресурс ДИАЛОЖЕКС
description: Определяет диалоговое окно. | Ресурс ДИАЛОЖЕКС
ms.assetid: 3ff28b68-e8b4-444d-8e26-5119ed30e44e
keywords:
- Меню ресурсов ДИАЛОЖЕКС и другие ресурсы
topic_type:
- apiref
api_name:
- DIALOGEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd55bfb06b678742aa5e356c9e62b14229aa8d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273574"
---
# <a name="dialogex-resource"></a><span data-ttu-id="0d44a-105">Ресурс ДИАЛОЖЕКС</span><span class="sxs-lookup"><span data-stu-id="0d44a-105">DIALOGEX resource</span></span>

<span data-ttu-id="0d44a-106">Определяет диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="0d44a-106">Defines a dialog box.</span></span> <span data-ttu-id="0d44a-107">Оператор определяет расположение и размеры диалогового окна на экране, а также стиль диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0d44a-107">The statement defines the position and dimensions of the dialog box on the screen as well as the dialog box style.</span></span> <span data-ttu-id="0d44a-108">Он также определяет следующее:</span><span class="sxs-lookup"><span data-stu-id="0d44a-108">It also defines the following:</span></span>

-   <span data-ttu-id="0d44a-109">Идентификаторы справки в диалоговом окне, а также в элементах управления в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="0d44a-109">Help IDs on the dialog itself as well as on controls within the dialog box.</span></span>
-   <span data-ttu-id="0d44a-110">Используйте инструкцию [**операторе EXSTYLE**](exstyle-statement.md) для самого диалогового окна, а также для элементов управления в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="0d44a-110">Use of the [**EXSTYLE**](exstyle-statement.md) statement for the dialog box itself as well as on controls within the dialog box.</span></span>
-   <span data-ttu-id="0d44a-111">Параметры веса шрифта и курсива для шрифта, используемого в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="0d44a-111">Font weight and italic settings for the font to be used in the dialog box.</span></span>
-   <span data-ttu-id="0d44a-112">Данные, относящиеся к элементам управления, в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="0d44a-112">Control-specific data for controls within the dialog box.</span></span>
-   <span data-ttu-id="0d44a-113">Использование предопределенных имен системных классов **бедит**, **иедит** и **хедит** .</span><span class="sxs-lookup"><span data-stu-id="0d44a-113">Use of the **BEDIT**, **IEDIT**, and **HEDIT** predefined system class names.</span></span>

``` syntax
nameID DIALOGEX x, y, width, height [ , helpID] [optional-statements]  {control-statements}
```

## <a name="parameters"></a><span data-ttu-id="0d44a-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d44a-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d44a-115"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="0d44a-115"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="0d44a-116">Уникальное имя или уникальное 16-битовое целочисленное значение без знака, идентифицирующее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="0d44a-116">Unique name or a unique 16-bit unsigned integer value that identifies the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="0d44a-117"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="0d44a-117"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="0d44a-118">Расположение на экране левой части диалогового окна в диалоговом окне "единицы измерения".</span><span class="sxs-lookup"><span data-stu-id="0d44a-118">Location on the screen of the left side of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="0d44a-119"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="0d44a-119"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="0d44a-120">Расположение на экране в верхней части диалогового окна в диалоговом окне "единицы измерения".</span><span class="sxs-lookup"><span data-stu-id="0d44a-120">Location on the screen of the top of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="0d44a-121"><span id="width"></span><span id="WIDTH"></span>*Ширина*</span><span class="sxs-lookup"><span data-stu-id="0d44a-121"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="0d44a-122">Ширина диалогового окна в диалоговых единицах.</span><span class="sxs-lookup"><span data-stu-id="0d44a-122">Width of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="0d44a-123"><span id="height"></span><span id="HEIGHT"></span>*равно*</span><span class="sxs-lookup"><span data-stu-id="0d44a-123"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="0d44a-124">Высота диалогового окна в диалоговых единицах.</span><span class="sxs-lookup"><span data-stu-id="0d44a-124">Height of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="0d44a-125"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*Идентификатор справки*</span><span class="sxs-lookup"><span data-stu-id="0d44a-125"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*</span></span>
</dt> <dd>

<span data-ttu-id="0d44a-126">Числовое выражение, указывающее идентификатор, используемый для идентификации диалогового окна во время обработки [**\_ справки WM**](../shell/wm-help.md) .</span><span class="sxs-lookup"><span data-stu-id="0d44a-126">Numeric expression indicating the ID used to identify the dialog box during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> <dt>

<span data-ttu-id="0d44a-127"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*Необязательные операторы*</span><span class="sxs-lookup"><span data-stu-id="0d44a-127"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="0d44a-128">Параметры для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0d44a-128">Options for the dialog box.</span></span> <span data-ttu-id="0d44a-129">Это может быть ноль или более следующих инструкций.</span><span class="sxs-lookup"><span data-stu-id="0d44a-129">This can be zero or more of the following statements.</span></span>



| <span data-ttu-id="0d44a-130">Инструкция</span><span class="sxs-lookup"><span data-stu-id="0d44a-130">Statement</span></span>                                                         | <span data-ttu-id="0d44a-131">Описание</span><span class="sxs-lookup"><span data-stu-id="0d44a-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d44a-132">**Заголовок** "*Text*"</span><span class="sxs-lookup"><span data-stu-id="0d44a-132">**CAPTION** "*text*"</span></span>                                              | <span data-ttu-id="0d44a-133">Заголовок диалогового окна, если у него есть заголовок.</span><span class="sxs-lookup"><span data-stu-id="0d44a-133">Caption of the dialog box if it has a title bar.</span></span> <span data-ttu-id="0d44a-134">Дополнительные сведения см. в разделе [**инструкция Caption**](caption-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0d44a-134">For more information, see [**CAPTION Statement**](caption-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="0d44a-135">**Параметры** *DWORD*</span><span class="sxs-lookup"><span data-stu-id="0d44a-135">**CHARACTERISTICS** *dword*</span></span>                                       | <span data-ttu-id="0d44a-136">Определяемое пользователем значение **DWORD** для использования инструментами ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0d44a-136">User-defined **DWORD** value for use by resource tools.</span></span> <span data-ttu-id="0d44a-137">Это значение не используется системой.</span><span class="sxs-lookup"><span data-stu-id="0d44a-137">This value is not used by the system.</span></span> <span data-ttu-id="0d44a-138">Дополнительные сведения см. в разделе [**инструкция характеристик**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0d44a-138">For more information, see [**CHARACTERISTICS Statement**](characteristics-statement.md).</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="0d44a-139">_Класс_ класса</span><span class="sxs-lookup"><span data-stu-id="0d44a-139">**CLASS**_class_</span></span>                                                  | <span data-ttu-id="0d44a-140">16-разрядное целое число без знака или строка, заключенная в двойные кавычки ("), которая определяет класс диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0d44a-140">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="0d44a-141">Дополнительные сведения см. в разделе [**оператор Class**](class-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0d44a-141">For more information, see [**CLASS Statement**](class-statement.md).</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="0d44a-142">**Операторе EXSTYLE** =  *Расширенные стили*</span><span class="sxs-lookup"><span data-stu-id="0d44a-142">**EXSTYLE**= *extended-styles*</span></span>                                    | <span data-ttu-id="0d44a-143">Расширенный стиль окна для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0d44a-143">Extended window style of the dialog box.</span></span> <span data-ttu-id="0d44a-144">Дополнительные сведения см. в разделе [**операторе EXSTYLE Statement**](exstyle-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0d44a-144">For more information, see [**EXSTYLE Statement**](exstyle-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="0d44a-145">**Font** *PointSize*,*гарнитура*, *Weight*, *курсив*, *CharSet*</span><span class="sxs-lookup"><span data-stu-id="0d44a-145">**FONT** *pointsize*, "*typeface*", *weight*, *italic*, *charset*</span></span> | <span data-ttu-id="0d44a-146">Кегль и гарнитура шрифта.</span><span class="sxs-lookup"><span data-stu-id="0d44a-146">Point size and typeface for the font.</span></span> <span data-ttu-id="0d44a-147">Для *веса* используйте значения \**FW \_ \** _, определенные в вингди. h.</span><span class="sxs-lookup"><span data-stu-id="0d44a-147">For *weight*, use the \**FW\_\** _ values defined in WinGDI.h.</span></span> <span data-ttu-id="0d44a-148">Для _italic \* Укажите TRUE для использования курсивного шрифта; в противном случае — FALSE.</span><span class="sxs-lookup"><span data-stu-id="0d44a-148">For _italic\*, specify TRUE to use an italic font, FALSE otherwise.</span></span> <span data-ttu-id="0d44a-149">Для *CharSet* используйте значение, определенное в элементе **лфчарсет** структуры [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="0d44a-149">For *charset*, use the value defined in the **lfCharSet** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="0d44a-150">Чтобы получить окончательный шрифт для диалогового окна, приложение должно указать *CharSet* вместе с другими свойствами шрифта.</span><span class="sxs-lookup"><span data-stu-id="0d44a-150">To get the definitive font for a dialog box, an application should specify *charset* along with other font properties.</span></span> <span data-ttu-id="0d44a-151">Дополнительные сведения см. в разделе [**инструкция Font**](font-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0d44a-151">For more information, see [**FONT Statement**](font-statement.md).</span></span> |
| <span data-ttu-id="0d44a-152"> *Язык* языка, *подязык*</span><span class="sxs-lookup"><span data-stu-id="0d44a-152">**LANGUAGE** *language*, *sublanguage*</span></span>                            | <span data-ttu-id="0d44a-153">Язык диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0d44a-153">Language of the dialog box.</span></span> <span data-ttu-id="0d44a-154">Дополнительные сведения см. в разделе [**языковая инструкция**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0d44a-154">For more information, see [**LANGUAGE Statement**](language-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="0d44a-155"> *Menuname* меню</span><span class="sxs-lookup"><span data-stu-id="0d44a-155">**MENU** *menuname*</span></span>                                               | <span data-ttu-id="0d44a-156">Используемое меню.</span><span class="sxs-lookup"><span data-stu-id="0d44a-156">Menu to be used.</span></span> <span data-ttu-id="0d44a-157">Это значение является либо именем меню, либо его целочисленным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="0d44a-157">This value is either the name of the menu or its integer identifier.</span></span> <span data-ttu-id="0d44a-158">Дополнительные сведения см. в разделе [**инструкция меню**](menu-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0d44a-158">For more information, see [**MENU Statement**](menu-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="0d44a-159"> *Стили* стилей</span><span class="sxs-lookup"><span data-stu-id="0d44a-159">**STYLE** *styles*</span></span>                                                | <span data-ttu-id="0d44a-160">Стили диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0d44a-160">Styles of the dialog box.</span></span> <span data-ttu-id="0d44a-161">Дополнительные сведения см. в разделе [**оператор Style**](style-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0d44a-161">For more information, see [**STYLE Statement**](style-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="0d44a-162">**Версия** *DWORD*</span><span class="sxs-lookup"><span data-stu-id="0d44a-162">**VERSION** *dword*</span></span>                                               | <span data-ttu-id="0d44a-163">Определяемое пользователем значение **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="0d44a-163">User-defined **DWORD** value.</span></span> <span data-ttu-id="0d44a-164">Эта инструкция предназначена для использования дополнительными инструментами ресурсов и не используется системой.</span><span class="sxs-lookup"><span data-stu-id="0d44a-164">This statement is intended for use by additional resource tools and is not used by the system.</span></span> <span data-ttu-id="0d44a-165">Дополнительные сведения см. в разделе [**оператор версии**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0d44a-165">For more information, see [**VERSION Statement**](version-statement.md).</span></span>                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="0d44a-166"><span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*операторы Control*</span><span class="sxs-lookup"><span data-stu-id="0d44a-166"><span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*control-statements*</span></span>
</dt> <dd>

<span data-ttu-id="0d44a-167">Тело ресурса **диаложекс** состоит из любого числа управляющих инструкций.</span><span class="sxs-lookup"><span data-stu-id="0d44a-167">Body of the **DIALOGEX** resource is made up of any number of control statements.</span></span> <span data-ttu-id="0d44a-168">Существует четыре семейства управляющих операторов: универсальные, статические, кнопки и Правка.</span><span class="sxs-lookup"><span data-stu-id="0d44a-168">There are four families of control statements: generic, static, button, and edit.</span></span> <span data-ttu-id="0d44a-169">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="0d44a-169">For more information, see Remarks.</span></span>

</dd> </dl>

<span data-ttu-id="0d44a-170">Для обратной совместимости также поддерживаются некоторые атрибуты.</span><span class="sxs-lookup"><span data-stu-id="0d44a-170">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="0d44a-171">Дополнительные сведения см. в разделе [Общие атрибуты ресурсов](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="0d44a-171">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0d44a-172">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d44a-172">Remarks</span></span>

<span data-ttu-id="0d44a-173">Допустимые операции, которые могут содержаться в любом из числовых выражений в инструкциях **диаложекс** , приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="0d44a-173">The valid operations that may be contained in any of the numeric expressions in the statements of **DIALOGEX** are as follows:</span></span>

-   <span data-ttu-id="0d44a-174">Добавить ("+")</span><span class="sxs-lookup"><span data-stu-id="0d44a-174">Add ('+')</span></span>
-   <span data-ttu-id="0d44a-175">Вычитание ("-")</span><span class="sxs-lookup"><span data-stu-id="0d44a-175">Subtract ('-')</span></span>
-   <span data-ttu-id="0d44a-176">Унарный минус ("-")</span><span class="sxs-lookup"><span data-stu-id="0d44a-176">Unary minus ('-')</span></span>
-   <span data-ttu-id="0d44a-177">Унарный оператор NOT (' ~ ')</span><span class="sxs-lookup"><span data-stu-id="0d44a-177">Unary NOT ('~')</span></span>
-   <span data-ttu-id="0d44a-178">И (' & ')</span><span class="sxs-lookup"><span data-stu-id="0d44a-178">AND ('&')</span></span>
-   <span data-ttu-id="0d44a-179">ИЛИ (' \| ')</span><span class="sxs-lookup"><span data-stu-id="0d44a-179">OR ('\|')</span></span>

<span data-ttu-id="0d44a-180">Текст ресурса состоит из универсальных, статических операторов, кнопок и элементов управления Edit.</span><span class="sxs-lookup"><span data-stu-id="0d44a-180">The body of the resource is made up of generic, static, button, and edit control statements.</span></span> <span data-ttu-id="0d44a-181">Хотя каждая из этих семейств инструкций использует другой синтаксис для определения конкретных функций элементов управления, все они совместно используют общий синтаксис для определения положения, размера, расширенных стилей, идентификационного номера справки и данных, относящихся к конкретному элементу управления.</span><span class="sxs-lookup"><span data-stu-id="0d44a-181">While each of these families of statements uses a different syntax for defining specific features of its controls, they all share a common syntax for defining the position, size, extended styles, help identification number, and control-specific data.</span></span> <span data-ttu-id="0d44a-182">Дополнительные сведения см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0d44a-182">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

### <a name="generic-control-statements"></a><span data-ttu-id="0d44a-183">Универсальные операторы управления</span><span class="sxs-lookup"><span data-stu-id="0d44a-183">Generic Control Statements</span></span>

``` syntax
CONTROL controlText, id, className, style
```

<dl> <dt>

<span data-ttu-id="0d44a-184"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*контролтекст*</span><span class="sxs-lookup"><span data-stu-id="0d44a-184"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="0d44a-185">Текст окна для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0d44a-185">Window text for the control.</span></span> <span data-ttu-id="0d44a-186">Дополнительные сведения см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0d44a-186">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d44a-187"><span id="id"></span><span id="ID"></span>*удостоверения*</span><span class="sxs-lookup"><span data-stu-id="0d44a-187"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="0d44a-188">Идентификатор элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0d44a-188">Control identifier.</span></span> <span data-ttu-id="0d44a-189">Дополнительные сведения см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0d44a-189">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d44a-190"><span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*className*</span><span class="sxs-lookup"><span data-stu-id="0d44a-190"><span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*className*</span></span>
</dt> <dd>

<span data-ttu-id="0d44a-191">Имя класса.</span><span class="sxs-lookup"><span data-stu-id="0d44a-191">Name of the class.</span></span> <span data-ttu-id="0d44a-192">Это может быть либо строка, заключенная в двойные кавычки ("), либо один из следующих стандартных системных классов: **кнопка**, **статический**, **Правка**, **список**, **полоса прокрутки** или **поле со списком**.</span><span class="sxs-lookup"><span data-stu-id="0d44a-192">This may be either a string enclosed in double quotation marks (") or one of the following predefined system classes: **BUTTON**, **STATIC**, **EDIT**, **LISTBOX**, **SCROLLBAR**, or **COMBOBOX**.</span></span>

</dd> <dt>

<span data-ttu-id="0d44a-193"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="0d44a-193"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="0d44a-194">Стили окна (явные значения **WS \_ \* *_, _* BS \_ \* *_, _* SS \_ \* *_, _* ES \_ \* *_, _* фунтов \_ \* *_, _* SBS \_ \* *_ и _* \_ \*** в стиле CBS, определенные в файле WinUser. H, можно использовать, добавив include в RC-файл: `#include "winuser.h"` ).</span><span class="sxs-lookup"><span data-stu-id="0d44a-194">Window styles (explicit **WS\_\**_, _\* BS\_\**_, _\* SS\_\*\*_, _\* ES\_\*\*_, _\* LBS\_\*\*_, _\* SBS\_\*\*_, and _\* CBS\_\*\*\* style values defined in Winuser.H can be used by adding an include to the .rc file: `#include "winuser.h"`).</span></span> <span data-ttu-id="0d44a-195">Дополнительные сведения см. в разделе [стили окон](/windows/desktop/winmsg/window-styles).</span><span class="sxs-lookup"><span data-stu-id="0d44a-195">For more information, see [Window Styles](/windows/desktop/winmsg/window-styles).</span></span>

</dd> </dl>

### <a name="static-control-statements"></a><span data-ttu-id="0d44a-196">Статические операторы управления</span><span class="sxs-lookup"><span data-stu-id="0d44a-196">Static Control Statements</span></span>

``` syntax
staticClass controlText, id
```

<dl> <dt>

<span data-ttu-id="0d44a-197"><span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*статиккласс*</span><span class="sxs-lookup"><span data-stu-id="0d44a-197"><span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticClass*</span></span>
</dt> <dd>

<span data-ttu-id="0d44a-198">**Лтекст**, **ртекст** или **столбец ctext**.</span><span class="sxs-lookup"><span data-stu-id="0d44a-198">**LTEXT**, **RTEXT**, or **CTEXT**.</span></span>

</dd> <dt>

<span data-ttu-id="0d44a-199"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*контролтекст*</span><span class="sxs-lookup"><span data-stu-id="0d44a-199"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="0d44a-200">Текст окна для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0d44a-200">Window text for the control.</span></span> <span data-ttu-id="0d44a-201">Дополнительные сведения см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0d44a-201">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d44a-202"><span id="id"></span><span id="ID"></span>*удостоверения*</span><span class="sxs-lookup"><span data-stu-id="0d44a-202"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="0d44a-203">Идентификатор элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0d44a-203">Control identifier.</span></span> <span data-ttu-id="0d44a-204">Дополнительные сведения см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0d44a-204">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

### <a name="button-control-statements"></a><span data-ttu-id="0d44a-205">Операторы управления кнопками</span><span class="sxs-lookup"><span data-stu-id="0d44a-205">Button Control Statements</span></span>

``` syntax
buttonClass controlText, id
```

<dl> <dt>

<span data-ttu-id="0d44a-206"><span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*буттонкласс*</span><span class="sxs-lookup"><span data-stu-id="0d44a-206"><span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*buttonClass*</span></span>
</dt> <dd>

<span data-ttu-id="0d44a-207">**AUTO3STATE**, **автофлажок**, **автоradiobutton**, **CheckBox**, **пушбокс**, **кнопка**, **RADIOBUTTON**, **STATE3** или **усербуттон**.</span><span class="sxs-lookup"><span data-stu-id="0d44a-207">**AUTO3STATE**, **AUTOCHECKBOX**, **AUTORADIOBUTTON**, **CHECKBOX**, **PUSHBOX**, **PUSHBUTTON**, **RADIOBUTTON**, **STATE3**, or **USERBUTTON**.</span></span>

</dd> <dt>

<span data-ttu-id="0d44a-208"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*контролтекст*</span><span class="sxs-lookup"><span data-stu-id="0d44a-208"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="0d44a-209">Текст окна для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0d44a-209">Window text for the control.</span></span> <span data-ttu-id="0d44a-210">Дополнительные сведения см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0d44a-210">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d44a-211"><span id="id"></span><span id="ID"></span>*удостоверения*</span><span class="sxs-lookup"><span data-stu-id="0d44a-211"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="0d44a-212">Идентификатор элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0d44a-212">Control identifier.</span></span> <span data-ttu-id="0d44a-213">Дополнительные сведения см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0d44a-213">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

### <a name="edit-control-statements"></a><span data-ttu-id="0d44a-214">Изменить операторы управления</span><span class="sxs-lookup"><span data-stu-id="0d44a-214">Edit Control Statements</span></span>

``` syntax
editClass id
```

<dl> <dt>

<span data-ttu-id="0d44a-215"><span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*едиткласс*</span><span class="sxs-lookup"><span data-stu-id="0d44a-215"><span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*editClass*</span></span>
</dt> <dd>

<span data-ttu-id="0d44a-216">**EditText**, **бедит**, **хедит** или **иедит**.</span><span class="sxs-lookup"><span data-stu-id="0d44a-216">**EDITTEXT**, **BEDIT**, **HEDIT**, or **IEDIT**.</span></span>

</dd> <dt>

<span data-ttu-id="0d44a-217"><span id="id"></span><span id="ID"></span>*удостоверения*</span><span class="sxs-lookup"><span data-stu-id="0d44a-217"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="0d44a-218">Идентификатор элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0d44a-218">Control identifier.</span></span> <span data-ttu-id="0d44a-219">Дополнительные сведения см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0d44a-219">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="0d44a-220">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d44a-220">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d44a-221">Использование диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="0d44a-221">Using Dialog Boxes</span></span>](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[<span data-ttu-id="0d44a-222">**Accelerator**</span><span class="sxs-lookup"><span data-stu-id="0d44a-222">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="0d44a-223">**ПОКАЗАТЕЛИ**</span><span class="sxs-lookup"><span data-stu-id="0d44a-223">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="0d44a-224">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="0d44a-224">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="0d44a-225">**креатедиалог**</span><span class="sxs-lookup"><span data-stu-id="0d44a-225">**CreateDialog**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[<span data-ttu-id="0d44a-226">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="0d44a-226">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="0d44a-227">**диалогбокс**</span><span class="sxs-lookup"><span data-stu-id="0d44a-227">**DialogBox**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[<span data-ttu-id="0d44a-228">**жетдиалогбасеунитс**</span><span class="sxs-lookup"><span data-stu-id="0d44a-228">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="0d44a-229">**ЯЗЫКЕ**</span><span class="sxs-lookup"><span data-stu-id="0d44a-229">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="0d44a-230">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="0d44a-230">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[<span data-ttu-id="0d44a-231">МЕНЮ</span><span class="sxs-lookup"><span data-stu-id="0d44a-231">MENU</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="0d44a-232">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="0d44a-232">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="0d44a-233">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="0d44a-233">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="0d44a-234">**Версия**</span><span class="sxs-lookup"><span data-stu-id="0d44a-234">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
