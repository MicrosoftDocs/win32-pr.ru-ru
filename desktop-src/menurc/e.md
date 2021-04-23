---
title: E (меню и другие ресурсы)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 14e12ba3-8451-4a93-a555-e1c9e6040a67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f8d26d341a114ab7bfeae269a391f8df90423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134983"
---
# <a name="e-menus-and-other-resources"></a><span data-ttu-id="cd435-103">E (меню и другие ресурсы)</span><span class="sxs-lookup"><span data-stu-id="cd435-103">E (Menus and Other Resources)</span></span>

<span data-ttu-id="cd435-104">[A](a.md) [B](b.md) [C](c.md) D E [F](f.md) G р [. J K](i.md) L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="cd435-104">[A](a.md) [B](b.md) [C](c.md) D E [F](f.md) G H [I](i.md) J K L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="cd435-105"><span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**Пустые меню запрещены**</span><span class="sxs-lookup"><span data-stu-id="cd435-105"><span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**Empty menus not allowed**</span></span>
</dt> <dd>

<span data-ttu-id="cd435-106">Ключевое слово **End** появляется перед тем, как все пункты меню определены в инструкции [**меню**](menu-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="cd435-106">An **END** keyword appears before any menu items are defined in the [**MENU**](menu-resource.md) statement.</span></span> <span data-ttu-id="cd435-107">Пустые меню не разрешены компилятором ресурсов Microsoft Windows 32 (RC).</span><span class="sxs-lookup"><span data-stu-id="cd435-107">Empty menus are not permitted by Microsoft Windows 32 Resource Compiler (RC).</span></span> <span data-ttu-id="cd435-108">Убедитесь, что в операторе **меню** отсутствуют открывающие кавычки.</span><span class="sxs-lookup"><span data-stu-id="cd435-108">Make sure that you do not have any opening quotation marks within the **MENU** statement.</span></span>

</dd> <dt>

<span data-ttu-id="cd435-109"><span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**Ожидается END в диалоговом окне**</span><span class="sxs-lookup"><span data-stu-id="cd435-109"><span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**END expected in Dialog**</span></span>
</dt> <dd>

<span data-ttu-id="cd435-110">Ключевое слово **End** должно находиться в конце инструкции [**диалогового окна**](dialog-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="cd435-110">The **END** keyword must appear at the end of a [**DIALOG**](dialog-resource.md) statement.</span></span> <span data-ttu-id="cd435-111">Убедитесь, что в предыдущем операторе не осталось открывающих кавычек.</span><span class="sxs-lookup"><span data-stu-id="cd435-111">Make sure that there are no opening quotation marks left from the preceding statement.</span></span>

</dd> <dt>

<span data-ttu-id="cd435-112"><span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**КОНЕЦ ожидаемого в меню**</span><span class="sxs-lookup"><span data-stu-id="cd435-112"><span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**END expected in menu**</span></span>
</dt> <dd>

<span data-ttu-id="cd435-113">Ключевое слово **End** должно находиться в конце инструкции [**меню**](menu-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="cd435-113">The **END** keyword must appear at the end of a [**MENU**](menu-resource.md) statement.</span></span> <span data-ttu-id="cd435-114">Убедитесь, что отсутствуют несовпадающие операторы **Begin** и **End** .</span><span class="sxs-lookup"><span data-stu-id="cd435-114">Make sure that there are no mismatched **BEGIN** and **END** statements.</span></span>

</dd> <dt>

<span data-ttu-id="cd435-115"><span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Ошибка Креатингресаурце — имя**</span><span class="sxs-lookup"><span data-stu-id="cd435-115"><span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Error Creatingresource-name**</span></span>
</dt> <dd>

<span data-ttu-id="cd435-116">Компилятору ресурсов Microsoft Windows 32 (RC) не удалось создать указанный двоичный ресурс (. RES).</span><span class="sxs-lookup"><span data-stu-id="cd435-116">Microsoft Windows 32 Resource Compiler (RC) could not create the specified binary resource (.RES) file.</span></span> <span data-ttu-id="cd435-117">Убедитесь, что он не создается на диске только для чтения.</span><span class="sxs-lookup"><span data-stu-id="cd435-117">Make sure that it is not being created on a read-only drive.</span></span> <span data-ttu-id="cd435-118">Используйте параметр **/v** , чтобы узнать, создается ли файл.</span><span class="sxs-lookup"><span data-stu-id="cd435-118">Use the **/v** option to find out whether the file is being created.</span></span>

</dd> <dt>

<span data-ttu-id="cd435-119"><span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Ожидается запятая в таблице сочетаний клавиш**</span><span class="sxs-lookup"><span data-stu-id="cd435-119"><span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Expected Comma in Accelerator Table**</span></span>
</dt> <dd>

<span data-ttu-id="cd435-120">Компилятор ресурсов Microsoft Windows 32 (RC) требует запятую между параметрами *события* и *idvalue* в операторе [**ускорителей**](accelerators-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="cd435-120">Microsoft Windows 32 Resource Compiler (RC) requires a comma between the *event* and *idvalue* parameters in the [**ACCELERATORS**](accelerators-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="cd435-121"><span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Ожидаемое имя класса элемента управления**</span><span class="sxs-lookup"><span data-stu-id="cd435-121"><span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Expected control class name**</span></span>
</dt> <dd>

<span data-ttu-id="cd435-122">Параметр *Class* оператора [**Control**](control-control.md) в операторе [**DIALOG**](dialog-resource.md) должен быть одним из следующих типов элементов управления: **Button**, [**ComboBox**](combobox-control.md), **Edit**, [**ListBox**](listbox-control.md), [**ScrollBar**](scrollbar-control.md), **static** или defined, определяемый пользователем.</span><span class="sxs-lookup"><span data-stu-id="cd435-122">The *class* parameter of a [**CONTROL**](control-control.md) statement in the [**DIALOG**](dialog-resource.md) statement must be one of the following control types: **BUTTON**, [**COMBOBOX**](combobox-control.md), **EDIT**, [**LISTBOX**](listbox-control.md), [**SCROLLBAR**](scrollbar-control.md), **STATIC**, or user-defined.</span></span> <span data-ttu-id="cd435-123">Убедитесь, что класс написан правильно.</span><span class="sxs-lookup"><span data-stu-id="cd435-123">Make sure that the class is spelled correctly.</span></span>

</dd> <dt>

<span data-ttu-id="cd435-124"><span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Ожидаемое имя начертания шрифта**</span><span class="sxs-lookup"><span data-stu-id="cd435-124"><span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Expected font face name**</span></span>
</dt> <dd>

<span data-ttu-id="cd435-125">Параметр *гарнитуры* в операторе **Font** в [**диалоговом окне**](dialog-resource.md) должен быть символьной строкой, заключенной в двойные кавычки (").</span><span class="sxs-lookup"><span data-stu-id="cd435-125">The *typeface* parameter of the **FONT** statement in the [**DIALOG**](dialog-resource.md) statement must be a character string enclosed in double quotation marks (").</span></span> <span data-ttu-id="cd435-126">Этот параметр задает имя шрифта.</span><span class="sxs-lookup"><span data-stu-id="cd435-126">This parameter specifies the name of a font.</span></span>

</dd> <dt>

<span data-ttu-id="cd435-127"><span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Ожидаемое значение идентификатора для MenuItem**</span><span class="sxs-lookup"><span data-stu-id="cd435-127"><span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Expected ID value for Menuitem**</span></span>
</dt> <dd>

<span data-ttu-id="cd435-128">Оператор [**меню**](menu-resource.md) должен содержать инструкцию [**MenuItem**](menuitem-statement.md) , которая содержит либо целое число, либо символьную константу в параметре *менуид* .</span><span class="sxs-lookup"><span data-stu-id="cd435-128">The [**MENU**](menu-resource.md) statement must contain a [**MENUITEM**](menuitem-statement.md) statement, which has either an integer or a symbolic constant in the *MenuID* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="cd435-129"><span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Ожидается строка меню**</span><span class="sxs-lookup"><span data-stu-id="cd435-129"><span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Expected Menu String**</span></span>
</dt> <dd>

<span data-ttu-id="cd435-130">Каждая инструкция [**MenuItem**](menuitem-statement.md) и [**Popup**](popup-resource.md) должна содержать *текстовый* параметр.</span><span class="sxs-lookup"><span data-stu-id="cd435-130">Each [**MENUITEM**](menuitem-statement.md) and [**POPUP**](popup-resource.md) statement must contain a *text* parameter.</span></span> <span data-ttu-id="cd435-131">Этот параметр представляет собой строку, заключенную в двойные кавычки ("), которая указывает имя пункта меню или всплывающего меню.</span><span class="sxs-lookup"><span data-stu-id="cd435-131">This parameter is a string enclosed in double quotation marks (") that specifies the name of the menu item or pop-up menu.</span></span> <span data-ttu-id="cd435-132">Для инструкции- **разделителя MenuItem** не требуется строка в кавычках.</span><span class="sxs-lookup"><span data-stu-id="cd435-132">A **MENUITEM SEPARATOR** statement requires no quoted string.</span></span>

</dd> <dt>

<span data-ttu-id="cd435-133"><span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Ожидаемое числовое значение команды**</span><span class="sxs-lookup"><span data-stu-id="cd435-133"><span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Expected numeric command value**</span></span>
</dt> <dd>

<span data-ttu-id="cd435-134">Компилятор ресурсов Microsoft Windows (RC) ожидал числовой параметр *idvalue* в операторе [**ускорителей**](accelerators-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="cd435-134">Microsoft Windows Resource Compiler (RC) was expecting a numeric *idvalue* parameter in the [**ACCELERATORS**](accelerators-resource.md) statement.</span></span> <span data-ttu-id="cd435-135">Убедитесь, что вы использовали оператор [**\# define**](-define.md) для указания значения и что используемая константа написана правильно.</span><span class="sxs-lookup"><span data-stu-id="cd435-135">Make sure that you have used a [**\#define**](-define.md) statement to specify the value and that the constant used is spelled correctly.</span></span>

</dd> <dt>

<span data-ttu-id="cd435-136"><span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Ожидалась числовая константа в таблице строк**</span><span class="sxs-lookup"><span data-stu-id="cd435-136"><span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Expected numeric constant in string table**</span></span>
</dt> <dd>

<span data-ttu-id="cd435-137">Числовая константа, определенная в инструкции [**\# define**](-define.md) , должна следовать непосредственно за ключевым словом **Begin** в операторе [**STRINGTABLE**](stringtable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="cd435-137">A numeric constant, defined in a [**\#define**](-define.md) statement, must immediately follow the **BEGIN** keyword in a [**STRINGTABLE**](stringtable-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="cd435-138"><span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Ожидался размер числовой точки**</span><span class="sxs-lookup"><span data-stu-id="cd435-138"><span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Expected numeric point size**</span></span>
</dt> <dd>

<span data-ttu-id="cd435-139">Параметр *PointSize* инструкции [**Font**](font-statement.md) в [**диалоговом окне**](dialog-resource.md) должен иметь целочисленное значение размера точки.</span><span class="sxs-lookup"><span data-stu-id="cd435-139">The *pointsize* parameter of the [**FONT**](font-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be an integer point-size value.</span></span>

</dd> <dt>

<span data-ttu-id="cd435-140"><span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Ожидаемая числовая константа диалогового окна**</span><span class="sxs-lookup"><span data-stu-id="cd435-140"><span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Expected Numerical Dialog constant**</span></span>
</dt> <dd>

<span data-ttu-id="cd435-141">Для оператора [**диалогового окна**](dialog-resource.md) требуются целочисленные значения для параметров *x*, *y*, *Width* и *Height* .</span><span class="sxs-lookup"><span data-stu-id="cd435-141">A [**DIALOG**](dialog-resource.md) statement requires integer values for the *x*, *y*, *width*, and *height* parameters.</span></span> <span data-ttu-id="cd435-142">Убедитесь, что эти значения, которые включены после ключевого слова **DIALOG** , не являются отрицательными.</span><span class="sxs-lookup"><span data-stu-id="cd435-142">Make sure that these values, which are included after the **DIALOG** keyword, are not negative.</span></span>

</dd> <dt>

<span data-ttu-id="cd435-143"><span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Ожидалась строка в STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="cd435-143"><span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Expected String in STRINGTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="cd435-144">После каждого числового параметра *stringid* в операторе [**STRINGTABLE**](stringtable-resource.md) ожидается строка.</span><span class="sxs-lookup"><span data-stu-id="cd435-144">A string is expected after each numeric *stringid* parameter in a [**STRINGTABLE**](stringtable-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="cd435-145"><span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Требуется строка или константа в качестве команды сочетания клавиш**</span><span class="sxs-lookup"><span data-stu-id="cd435-145"><span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Expected String or Constant Accelerator command**</span></span>
</dt> <dd>

<span data-ttu-id="cd435-146">Компилятору ресурсов Microsoft Windows (RC) не удалось определить, какой ключ был настроен для ускорителя.</span><span class="sxs-lookup"><span data-stu-id="cd435-146">Microsoft Windows Resource Compiler (RC) was not able to determine which key was being set up for the accelerator.</span></span> <span data-ttu-id="cd435-147">Параметр *события* в операторе [**ускорителей**](accelerators-resource.md) может быть недопустимым.</span><span class="sxs-lookup"><span data-stu-id="cd435-147">The *event* parameter in the [**ACCELERATORS**](accelerators-resource.md) statement might be invalid.</span></span>

</dd> <dt>

<span data-ttu-id="cd435-148"><span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**Ожидаемое значение, блок или ключевое слово END.**</span><span class="sxs-lookup"><span data-stu-id="cd435-148"><span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**Expected VALUE, BLOCK, or END keyword.**</span></span>
</dt> <dd>

<span data-ttu-id="cd435-149">Для структуры [**versionInfo**](versioninfo-resource.md) требуется ключевое слово **value**, **Block** или **End** .</span><span class="sxs-lookup"><span data-stu-id="cd435-149">The [**VERSIONINFO**](versioninfo-resource.md) structure requires a **VALUE**, **BLOCK**, or **END** keyword.</span></span>

</dd> <dt>

<span data-ttu-id="cd435-150"><span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Ожидается номер для идентификатора**</span><span class="sxs-lookup"><span data-stu-id="cd435-150"><span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Expecting number for ID**</span></span>
</dt> <dd>

<span data-ttu-id="cd435-151">Для параметра *ID* инструкции [**Control**](control-control.md) в инструкции [**DIALOG**](dialog-resource.md) ожидается число.</span><span class="sxs-lookup"><span data-stu-id="cd435-151">A number is expected for the *id* parameter of a [**CONTROL**](control-control.md) statement in the [**DIALOG**](dialog-resource.md) statement.</span></span> <span data-ttu-id="cd435-152">Убедитесь, что у вас есть число или оператор [**\# define**](-define.md) для идентификатора элемента управления.</span><span class="sxs-lookup"><span data-stu-id="cd435-152">Make sure that you have a number or a [**\#define**](-define.md) statement for the control identifier.</span></span>

</dd> <dt>

<span data-ttu-id="cd435-153"><span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Ожидается строка в кавычках для ключа**</span><span class="sxs-lookup"><span data-stu-id="cd435-153"><span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Expecting quoted string for key**</span></span>
</dt> <dd>

<span data-ttu-id="cd435-154">Ключевая строка, следующая за ключевым словом **Block** или **value** , должна быть заключена в двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="cd435-154">The key string following the **BLOCK** or **VALUE** keyword should be enclosed in double quotation marks.</span></span>

</dd> <dt>

<span data-ttu-id="cd435-155"><span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Ожидается строка в кавычках в классе диалогового окна**</span><span class="sxs-lookup"><span data-stu-id="cd435-155"><span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Expecting quoted string in dialog class**</span></span>
</dt> <dd>

<span data-ttu-id="cd435-156">Параметр *класса* инструкции [**класса**](class-statement.md) в инструкции [**DIALOG**](dialog-resource.md) должен быть целым числом или строкой, заключенной в двойные кавычки (").</span><span class="sxs-lookup"><span data-stu-id="cd435-156">The *class* parameter of the [**CLASS**](class-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be an integer or a string enclosed in double quotation marks (").</span></span>

</dd> <dt>

<span data-ttu-id="cd435-157"><span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Ожидается строка в кавычках в заголовке диалогового окна**</span><span class="sxs-lookup"><span data-stu-id="cd435-157"><span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Expecting quoted string in dialog title**</span></span>
</dt> <dd>

<span data-ttu-id="cd435-158">Параметр *каптионтекст* инструкции [**Caption**](caption-statement.md) в инструкции [**DIALOG**](dialog-resource.md) должен быть символьной строкой, заключенной в двойные кавычки (").</span><span class="sxs-lookup"><span data-stu-id="cd435-158">The *captiontext* parameter of the [**CAPTION**](caption-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be a character string, enclosed in double quotation marks (").</span></span>

</dd> </dl>

 

 




