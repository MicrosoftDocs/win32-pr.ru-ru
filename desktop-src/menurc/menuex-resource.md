---
title: Ресурс МЕНУЕКС
description: Определяет содержимое ресурса меню. | Ресурс МЕНУЕКС
ms.assetid: a83e1e78-2af4-4257-906e-7eb6d98bcbc8
keywords:
- Меню ресурсов МЕНУЕКС и другие ресурсы
topic_type:
- apiref
api_name:
- MENUEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ed379fb97d2795a166571fb48cde2c233021a33
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105713411"
---
# <a name="menuex-resource"></a><span data-ttu-id="09a9a-105">Ресурс МЕНУЕКС</span><span class="sxs-lookup"><span data-stu-id="09a9a-105">MENUEX resource</span></span>

<span data-ttu-id="09a9a-106">Определяет содержимое ресурса меню.</span><span class="sxs-lookup"><span data-stu-id="09a9a-106">Defines the contents of a menu resource.</span></span> <span data-ttu-id="09a9a-107">Ресурс меню — это коллекция сведений, определяющих внешний вид и функции меню приложения.</span><span class="sxs-lookup"><span data-stu-id="09a9a-107">A menu resource is a collection of information that defines the appearance and function of an application menu.</span></span> <span data-ttu-id="09a9a-108">Меню — это специальное средство ввода, которое позволяет пользователю выбирать команды и открывать подменю из списка пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="09a9a-108">A menu is a special input tool that lets a user select commands and open submenus from a list of menu items.</span></span> <span data-ttu-id="09a9a-109">Он также определяет следующее:</span><span class="sxs-lookup"><span data-stu-id="09a9a-109">It also defines the following:</span></span>

-   <span data-ttu-id="09a9a-110">Идентификаторы справки в меню.</span><span class="sxs-lookup"><span data-stu-id="09a9a-110">Help identifiers on menus.</span></span>
-   <span data-ttu-id="09a9a-111">Идентификаторы в меню.</span><span class="sxs-lookup"><span data-stu-id="09a9a-111">Identifiers on menus.</span></span>
-   <span data-ttu-id="09a9a-112">Использование флагов **MFT \_ \** _ типа и флагов состояния _*MFA \_ \*\*_ .</span><span class="sxs-lookup"><span data-stu-id="09a9a-112">Use of the **MFT\_\** _ type flags and _*MFS\_\*\*_ state flags.</span></span> <span data-ttu-id="09a9a-113">Дополнительные сведения об этих флагах см. в описании структуры [_ *объектами menuiteminfo* \*](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="09a9a-113">For more information on these flags, see the [_ *MENUITEMINFO*\*](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

``` syntax
menuID MENUEX{ [{[MENUITEM itemText [,[id][, [type][, state]]]] | 
    POPUP itemText [,[id][, [type][, [state][, helpID]]]] { popupBody } } . . .]}
```

## <a name="parameters"></a><span data-ttu-id="09a9a-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="09a9a-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09a9a-115"><span id="MENUITEM"></span><span id="menuitem"></span>[**MENUITEM**](menuitem-statement.md)</span><span class="sxs-lookup"><span data-stu-id="09a9a-115"><span id="MENUITEM"></span><span id="menuitem"></span>[**MENUITEM**](menuitem-statement.md)</span></span>
</dt> <dd>

<span data-ttu-id="09a9a-116">Определяет пункт меню.</span><span class="sxs-lookup"><span data-stu-id="09a9a-116">Defines a menu item.</span></span>

<dl> <dt>

<span data-ttu-id="09a9a-117"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*итемтекст*</span><span class="sxs-lookup"><span data-stu-id="09a9a-117"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span></span>
</dt> <dd>

<span data-ttu-id="09a9a-118">Строка, содержащая текст для пункта меню.</span><span class="sxs-lookup"><span data-stu-id="09a9a-118">String containing the text for the menu item.</span></span> <span data-ttu-id="09a9a-119">Дополнительные сведения см. в разделе [**MenuItem**](menuitem-statement.md).</span><span class="sxs-lookup"><span data-stu-id="09a9a-119">For more information, see [**MENUITEM**](menuitem-statement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09a9a-120"><span id="id"></span><span id="ID"></span>*удостоверения*</span><span class="sxs-lookup"><span data-stu-id="09a9a-120"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="09a9a-121">Числовое выражение, указывающее идентификатор элемента меню.</span><span class="sxs-lookup"><span data-stu-id="09a9a-121">Numeric expression indicating the identifier of the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="09a9a-122"><span id="type"></span><span id="TYPE"></span>*Тип*</span><span class="sxs-lookup"><span data-stu-id="09a9a-122"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="09a9a-123">Числовое выражение, указывающее тип элемента меню для использования предопределенных \_ \* значений типа MFT, включите следующую инструкцию в RC-файл:`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="09a9a-123">Numeric expression indicating the type of the menu item To use the predefined MFT\_\* type values, include the following statement in your .rc file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="09a9a-124"><span id="state"></span><span id="STATE"></span>*с*</span><span class="sxs-lookup"><span data-stu-id="09a9a-124"><span id="state"></span><span id="STATE"></span>*state*</span></span>
</dt> <dd>

<span data-ttu-id="09a9a-125">Числовое выражение, указывающее состояние пункта меню для использования предопределенных \_ \* значений состояния MFA, включите следующую инструкцию в. RC-файл:`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="09a9a-125">Numeric expression indicating the state of the menu item To use the predefined MFS\_\* state values, include the following statement in your .RC file: `#include "winuser.h"`</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="09a9a-126"><span id="POPUP"></span><span id="popup"></span>[**ПОДСКАЗКИ**](popup-resource.md)</span><span class="sxs-lookup"><span data-stu-id="09a9a-126"><span id="POPUP"></span><span id="popup"></span>[**POPUP**](popup-resource.md)</span></span>
</dt> <dd>

<span data-ttu-id="09a9a-127">Определяет пункт меню с связанным подменю.</span><span class="sxs-lookup"><span data-stu-id="09a9a-127">Defines a menu item that has a submenu associated with it.</span></span>

<dl> <dt>

<span data-ttu-id="09a9a-128"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*итемтекст*</span><span class="sxs-lookup"><span data-stu-id="09a9a-128"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span></span>
</dt> <dd>

<span data-ttu-id="09a9a-129">Строка, содержащая текст для пункта меню.</span><span class="sxs-lookup"><span data-stu-id="09a9a-129">String containing the text for the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="09a9a-130"><span id="id"></span><span id="ID"></span>*удостоверения*</span><span class="sxs-lookup"><span data-stu-id="09a9a-130"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="09a9a-131">Числовое выражение, указывающее идентификатор элемента меню.</span><span class="sxs-lookup"><span data-stu-id="09a9a-131">Numeric expression indicating the identifier of the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="09a9a-132"><span id="type"></span><span id="TYPE"></span>*Тип*</span><span class="sxs-lookup"><span data-stu-id="09a9a-132"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="09a9a-133">Числовое выражение, указывающее тип элемента меню для использования предопределенных \_ \* значений типа MFT, включите следующую инструкцию в. RC-файл:`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="09a9a-133">Numeric expression indicating the type of the menu item To use the predefined MFT\_\* type values, include the following statement in your .RC file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="09a9a-134"><span id="state"></span><span id="STATE"></span>*с*</span><span class="sxs-lookup"><span data-stu-id="09a9a-134"><span id="state"></span><span id="STATE"></span>*state*</span></span>
</dt> <dd>

<span data-ttu-id="09a9a-135">Числовое выражение, указывающее состояние пункта меню для использования предопределенных \_ \* значений состояния MFA, включите следующую инструкцию в RC-файл:`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="09a9a-135">Numeric expression indicating the state of the menu item To use the predefined MFS\_\* state values, include the following statement in your .rc file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="09a9a-136"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*Идентификатор справки*</span><span class="sxs-lookup"><span data-stu-id="09a9a-136"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*</span></span>
</dt> <dd>

<span data-ttu-id="09a9a-137">Числовое выражение, указывающее идентификатор, используемый для идентификации меню во время обработки [**\_ справки WM**](../shell/wm-help.md) .</span><span class="sxs-lookup"><span data-stu-id="09a9a-137">Numeric expression indicating the identifier used to identify the menu during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="09a9a-138"><span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*попупбоди*</span><span class="sxs-lookup"><span data-stu-id="09a9a-138"><span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*</span></span>
</dt> <dd>

<span data-ttu-id="09a9a-139">Содержит любое сочетание инструкций [**MenuItem**](menuitem-statement.md) и [**Popup**](popup-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="09a9a-139">Contains any combination of the [**MENUITEM**](menuitem-statement.md) and [**POPUP**](popup-resource.md) statements.</span></span>

</dd> </dl>

<span data-ttu-id="09a9a-140">Для обратной совместимости также поддерживаются некоторые атрибуты.</span><span class="sxs-lookup"><span data-stu-id="09a9a-140">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="09a9a-141">Дополнительные сведения см. в разделе [Общие атрибуты ресурсов](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="09a9a-141">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="09a9a-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="09a9a-142">Remarks</span></span>

<span data-ttu-id="09a9a-143">Допустимые арифметические и логические операции, которые могут содержаться в любом из числовых выражений в инструкциях **менуекс** , приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="09a9a-143">The valid arithmetic and Boolean operations that can be contained in any of the numeric expressions in the statements of **MENUEX** are as follows:</span></span>

-   <span data-ttu-id="09a9a-144">Добавить ("+")</span><span class="sxs-lookup"><span data-stu-id="09a9a-144">Add ('+')</span></span>
-   <span data-ttu-id="09a9a-145">Вычитание ("-")</span><span class="sxs-lookup"><span data-stu-id="09a9a-145">Subtract ('-')</span></span>
-   <span data-ttu-id="09a9a-146">Унарный минус ("-")</span><span class="sxs-lookup"><span data-stu-id="09a9a-146">Unary minus ('-')</span></span>
-   <span data-ttu-id="09a9a-147">Унарный оператор NOT (' ~ ')</span><span class="sxs-lookup"><span data-stu-id="09a9a-147">Unary NOT ('~')</span></span>
-   <span data-ttu-id="09a9a-148">И (' & ')</span><span class="sxs-lookup"><span data-stu-id="09a9a-148">AND ('&')</span></span>
-   <span data-ttu-id="09a9a-149">ИЛИ (' \| ')</span><span class="sxs-lookup"><span data-stu-id="09a9a-149">OR ('\|')</span></span>

## <a name="see-also"></a><span data-ttu-id="09a9a-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09a9a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09a9a-151">Использование меню</span><span class="sxs-lookup"><span data-stu-id="09a9a-151">Using Menus</span></span>](./using-menus.md)
</dt> <dt>

[<span data-ttu-id="09a9a-152">**Accelerator**</span><span class="sxs-lookup"><span data-stu-id="09a9a-152">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="09a9a-153">**ПОКАЗАТЕЛИ**</span><span class="sxs-lookup"><span data-stu-id="09a9a-153">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="09a9a-154">**Откроется**</span><span class="sxs-lookup"><span data-stu-id="09a9a-154">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="09a9a-155">**ЯЗЫКЕ**</span><span class="sxs-lookup"><span data-stu-id="09a9a-155">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="09a9a-156">**МЕНЮ**</span><span class="sxs-lookup"><span data-stu-id="09a9a-156">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="09a9a-157">**MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="09a9a-157">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> <dt>

[<span data-ttu-id="09a9a-158">**ПОДСКАЗКИ**</span><span class="sxs-lookup"><span data-stu-id="09a9a-158">**POPUP**</span></span>](popup-resource.md)
</dt> <dt>

[<span data-ttu-id="09a9a-159">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="09a9a-159">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="09a9a-160">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="09a9a-160">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="09a9a-161">**Версия**</span><span class="sxs-lookup"><span data-stu-id="09a9a-161">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
