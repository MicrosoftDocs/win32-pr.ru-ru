---
title: Ресурс всплывающего окна
description: Определяет пункт меню, который может содержать пункты меню и подменю.
ms.assetid: afca21c7-605e-4354-b6ec-576b81389b69
keywords:
- ВСПЛЫВАЮЩие меню ресурсов и другие ресурсы
topic_type:
- apiref
api_name:
- POPUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c7a1af3bd8ed9aae8908aa7ff926a3f4799ee5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104133178"
---
# <a name="popup-resource"></a><span data-ttu-id="b9704-104">Ресурс всплывающего окна</span><span class="sxs-lookup"><span data-stu-id="b9704-104">POPUP resource</span></span>

<span data-ttu-id="b9704-105">Определяет пункт меню, который может содержать пункты меню и подменю.</span><span class="sxs-lookup"><span data-stu-id="b9704-105">Defines a menu item that can contain menu items and submenus.</span></span>

``` syntax
POPUP text, [optionlist] {item-definitions ...}
```

## <a name="parameters"></a><span data-ttu-id="b9704-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9704-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9704-107"><span id="text"></span><span id="TEXT"></span>*полнотекстовым*</span><span class="sxs-lookup"><span data-stu-id="b9704-107"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="b9704-108">Строка, содержащая имя меню.</span><span class="sxs-lookup"><span data-stu-id="b9704-108">String that contains the name of the menu.</span></span> <span data-ttu-id="b9704-109">Эта строка должна быть заключена в двойные кавычки (**"**).</span><span class="sxs-lookup"><span data-stu-id="b9704-109">This string must be enclosed in double quotation marks (**"**).</span></span>

</dd> <dt>

<span data-ttu-id="b9704-110"><span id="optionlist"></span><span id="OPTIONLIST"></span>*оптионлист*</span><span class="sxs-lookup"><span data-stu-id="b9704-110"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span></span>
</dt> <dd>

<span data-ttu-id="b9704-111">Этот параметр указывает переопределенные параметры меню, которые определяют внешний вид пункта меню.</span><span class="sxs-lookup"><span data-stu-id="b9704-111">This parameter specifies redefined menu options that specify the appearance of the menu item.</span></span> <span data-ttu-id="b9704-112">Этот необязательный параметр может принимать одно или несколько из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="b9704-112">This optional parameter can be one or more of the following.</span></span>



| <span data-ttu-id="b9704-113">Параметр</span><span class="sxs-lookup"><span data-stu-id="b9704-113">Option</span></span>           | <span data-ttu-id="b9704-114">Описание</span><span class="sxs-lookup"><span data-stu-id="b9704-114">Description</span></span>                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9704-115">**ОТМЕЧЕН**</span><span class="sxs-lookup"><span data-stu-id="b9704-115">**CHECKED**</span></span>      | <span data-ttu-id="b9704-116">Рядом с пунктом меню стоит галочка.</span><span class="sxs-lookup"><span data-stu-id="b9704-116">Menu item has a check mark next to it.</span></span> <span data-ttu-id="b9704-117">Этот параметр недопустим для меню верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="b9704-117">This option is not valid for a top-level menu.</span></span>                                                                                 |
| <span data-ttu-id="b9704-118">**СЕРЫМ цветом**</span><span class="sxs-lookup"><span data-stu-id="b9704-118">**GRAYED**</span></span>       | <span data-ttu-id="b9704-119">Элемент меню изначально неактивен и отображается в меню серым или светлым затенением цвета текста меню.</span><span class="sxs-lookup"><span data-stu-id="b9704-119">Menu item is initially inactive and appears on the menu in gray or a lightened shade of the menu-text color.</span></span> <span data-ttu-id="b9704-120">Этот параметр нельзя использовать с параметром **Inactive** .</span><span class="sxs-lookup"><span data-stu-id="b9704-120">This option cannot be used with the **INACTIVE** option.</span></span> |
| <span data-ttu-id="b9704-121">**Справка**</span><span class="sxs-lookup"><span data-stu-id="b9704-121">**HELP**</span></span>         | <span data-ttu-id="b9704-122">Определяет элемент справки.</span><span class="sxs-lookup"><span data-stu-id="b9704-122">Identifies a help item.</span></span> <span data-ttu-id="b9704-123">Пункт меню размещается в правой части строки меню.</span><span class="sxs-lookup"><span data-stu-id="b9704-123">The menu item is place at the right-most position on the menu bar.</span></span>                                                                            |
| <span data-ttu-id="b9704-124">**Активный**</span><span class="sxs-lookup"><span data-stu-id="b9704-124">**INACTIVE**</span></span>     | <span data-ttu-id="b9704-125">Элемент меню отображается, но не может быть выбран.</span><span class="sxs-lookup"><span data-stu-id="b9704-125">Menu item is displayed but it cannot be selected.</span></span> <span data-ttu-id="b9704-126">Этот параметр нельзя использовать с **серым** параметром.</span><span class="sxs-lookup"><span data-stu-id="b9704-126">This option cannot be used with the **GRAYED** option.</span></span>                                                              |
| <span data-ttu-id="b9704-127">**менубарбреак**</span><span class="sxs-lookup"><span data-stu-id="b9704-127">**MENUBARBREAK**</span></span> | <span data-ttu-id="b9704-128">То же, что и **менубреак** , за исключением того, что для всплывающих меню он отделяет новый столбец от старого со вертикальной линией.</span><span class="sxs-lookup"><span data-stu-id="b9704-128">Same as **MENUBREAK** except that for pop-up menus, it separates the new column from the old column with a vertical line.</span></span>                                             |
| <span data-ttu-id="b9704-129">**менубреак**</span><span class="sxs-lookup"><span data-stu-id="b9704-129">**MENUBREAK**</span></span>    | <span data-ttu-id="b9704-130">Помещает пункт меню в новую строку для статических элементов строки меню.</span><span class="sxs-lookup"><span data-stu-id="b9704-130">Places the menu item on a new line for static menu-bar items.</span></span> <span data-ttu-id="b9704-131">Для меню он помещает пункт меню в новый столбец без разделительной линии между столбцами.</span><span class="sxs-lookup"><span data-stu-id="b9704-131">For menus, it places the menu item in a new column with no dividing line between the columns.</span></span>           |



 

</dd> </dl>

<span data-ttu-id="b9704-132">Для обратной совместимости также поддерживаются некоторые атрибуты.</span><span class="sxs-lookup"><span data-stu-id="b9704-132">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="b9704-133">Дополнительные сведения см. в разделе [Общие атрибуты ресурсов](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="b9704-133">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b9704-134">Примеры</span><span class="sxs-lookup"><span data-stu-id="b9704-134">Examples</span></span>

<span data-ttu-id="b9704-135">В следующем примере демонстрируется использование оператора **Popup** :</span><span class="sxs-lookup"><span data-stu-id="b9704-135">The following example demonstrates the use of the **POPUP** statement:</span></span>

``` syntax
chem MENU
{
    POPUP "&Elements"
    {
         MENUITEM "&Oxygen", 200
         MENUITEM "&Carbon", 201, CHECKED
         MENUITEM "&Hydrogen", 202
         MENUITEM SEPARATOR
         MENUITEM "&Sulfur", 203
         MENUITEM "Ch&lorine", 204
    } 
    POPUP "&Compounds"
    {
         POPUP "&Sugars"
         {
            MENUITEM "&Glucose", 301
            MENUITEM "&Sucrose", 302, CHECKED
            MENUITEM "&Lactose", 303, MENUBREAK
            MENUITEM "&Fructose", 304
         }
         POPUP "&Acids"
         {
              "&Hydrochloric", 401
              "&Sulfuric", 402
         }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="b9704-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9704-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9704-137">**МЕНЮ**</span><span class="sxs-lookup"><span data-stu-id="b9704-137">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="b9704-138">**MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="b9704-138">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> </dl>

 

 




