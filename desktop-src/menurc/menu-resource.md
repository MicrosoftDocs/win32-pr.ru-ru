---
title: Ресурс меню
description: Определяет содержимое ресурса меню. | Ресурс меню
ms.assetid: fcb420b6-d42e-4044-89ee-028eed1f21ee
keywords:
- МЕНЮ ресурсов MENU и другие ресурсы
topic_type:
- apiref
api_name:
- MENU
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5cdb564c7bf012255b339a13691d2ecf214a86
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105713422"
---
# <a name="menu-resource"></a><span data-ttu-id="8ec66-105">Ресурс меню</span><span class="sxs-lookup"><span data-stu-id="8ec66-105">MENU resource</span></span>

<span data-ttu-id="8ec66-106">Определяет содержимое ресурса меню.</span><span class="sxs-lookup"><span data-stu-id="8ec66-106">Defines the contents of a menu resource.</span></span> <span data-ttu-id="8ec66-107">Ресурс меню — это коллекция сведений, определяющих внешний вид и функции меню приложения.</span><span class="sxs-lookup"><span data-stu-id="8ec66-107">A menu resource is a collection of information that defines the appearance and function of an application menu.</span></span> <span data-ttu-id="8ec66-108">Меню — это специальное средство ввода, которое позволяет пользователю выбирать команды и открывать подменю из списка пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="8ec66-108">A menu is a special input tool that lets a user select commands and open submenus from a list of menu items.</span></span>

``` syntax
menuID MENU  [optional-statements]  {item-definitions ... }
```

## <a name="parameters"></a><span data-ttu-id="8ec66-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ec66-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ec66-110"><span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*менуид*</span><span class="sxs-lookup"><span data-stu-id="8ec66-110"><span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*menuID*</span></span>
</dt> <dd>

<span data-ttu-id="8ec66-111">Число, идентифицирующее меню.</span><span class="sxs-lookup"><span data-stu-id="8ec66-111">Number that identifies the menu.</span></span> <span data-ttu-id="8ec66-112">Это значение является уникальной строкой или уникальным 16-битовым целочисленным значением без знака в диапазоне от 1 до 65 535.</span><span class="sxs-lookup"><span data-stu-id="8ec66-112">This value is either a unique string or a unique 16-bit unsigned integer value in the range of 1 to 65,535.</span></span>

</dd> <dt>

<span data-ttu-id="8ec66-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*Необязательные операторы*</span><span class="sxs-lookup"><span data-stu-id="8ec66-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="8ec66-114">Этот параметр может быть больше нуля из следующих инструкций.</span><span class="sxs-lookup"><span data-stu-id="8ec66-114">This parameter can be zero of more of the following statements.</span></span>



| <span data-ttu-id="8ec66-115">Инструкция</span><span class="sxs-lookup"><span data-stu-id="8ec66-115">Statement</span></span>                                                        | <span data-ttu-id="8ec66-116">Описание</span><span class="sxs-lookup"><span data-stu-id="8ec66-116">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ec66-117">[**Параметры**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="8ec66-117">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="8ec66-118">Определяемая пользователем информация о ресурсе, который может использоваться средствами чтения и записи файлов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ec66-118">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="8ec66-119">Дополнительные сведения см. в разделе [**характеристики**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="8ec66-119">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="8ec66-120">[](language-statement.md) *Язык* языка, *подязык*</span><span class="sxs-lookup"><span data-stu-id="8ec66-120">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="8ec66-121">Язык для ресурса.</span><span class="sxs-lookup"><span data-stu-id="8ec66-121">Language for the resource.</span></span> <span data-ttu-id="8ec66-122">Дополнительные сведения см. в разделе [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="8ec66-122">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                            |
| <span data-ttu-id="8ec66-123">[**Версия**](version-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="8ec66-123">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="8ec66-124">Определяемый пользователем номер версии ресурса, который может использоваться инструментами, считывающими и записывающими файлы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ec66-124">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="8ec66-125">Дополнительные сведения см. в разделе [**версия**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="8ec66-125">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> </dl>

<span data-ttu-id="8ec66-126">Для обратной совместимости также поддерживаются некоторые атрибуты.</span><span class="sxs-lookup"><span data-stu-id="8ec66-126">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="8ec66-127">Дополнительные сведения см. в разделе [Общие атрибуты ресурсов](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="8ec66-127">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8ec66-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="8ec66-128">Examples</span></span>

<span data-ttu-id="8ec66-129">Ниже приведен пример полного оператора **меню** :</span><span class="sxs-lookup"><span data-stu-id="8ec66-129">The following is an example of a complete **MENU** statement:</span></span>

``` syntax
sample MENU
{
     MENUITEM "&Soup", 100
     MENUITEM "S&alad", 101
     POPUP "&Entree"
     {
          MENUITEM "&Fish", 200
          MENUITEM "&Chicken", 201, CHECKED
          POPUP "&Beef"
          {
               MENUITEM "&Steak", 301
               MENUITEM "&Prime Rib", 302
          }
     }
     MENUITEM "&Dessert", 103
}
```

## <a name="see-also"></a><span data-ttu-id="8ec66-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ec66-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ec66-131">Использование меню</span><span class="sxs-lookup"><span data-stu-id="8ec66-131">Using Menus</span></span>](./using-menus.md)
</dt> <dt>

[<span data-ttu-id="8ec66-132">**Accelerator**</span><span class="sxs-lookup"><span data-stu-id="8ec66-132">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="8ec66-133">**ПОКАЗАТЕЛИ**</span><span class="sxs-lookup"><span data-stu-id="8ec66-133">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="8ec66-134">**ЯЗЫКЕ**</span><span class="sxs-lookup"><span data-stu-id="8ec66-134">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="8ec66-135">**менуекс**</span><span class="sxs-lookup"><span data-stu-id="8ec66-135">**MENUEX**</span></span>](menuex-resource.md)
</dt> <dt>

[<span data-ttu-id="8ec66-136">**MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="8ec66-136">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> <dt>

[<span data-ttu-id="8ec66-137">**ПОДСКАЗКИ**</span><span class="sxs-lookup"><span data-stu-id="8ec66-137">**POPUP**</span></span>](popup-resource.md)
</dt> <dt>

[<span data-ttu-id="8ec66-138">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="8ec66-138">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="8ec66-139">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="8ec66-139">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="8ec66-140">**Версия**</span><span class="sxs-lookup"><span data-stu-id="8ec66-140">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
