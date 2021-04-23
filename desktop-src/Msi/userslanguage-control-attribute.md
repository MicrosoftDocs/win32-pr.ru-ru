---
description: Если задан этот битовый флаг, шрифты создаются с использованием кодовой страницы пользовательского интерфейса по умолчанию. Если битовый флаг не установлен, шрифты создаются с помощью кодовой страницы базы данных.
ms.assetid: 6a3dbabe-6a14-4401-b46c-e8a0bd0cbe63
title: Атрибут элемента управления Усерслангуаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aff4109c5c0819b199343bb8ee38bfecc069ad4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673593"
---
# <a name="userslanguage-control-attribute"></a><span data-ttu-id="fb62a-104">Атрибут элемента управления Усерслангуаже</span><span class="sxs-lookup"><span data-stu-id="fb62a-104">UsersLanguage Control Attribute</span></span>

<span data-ttu-id="fb62a-105">Если задан этот битовый флаг, шрифты создаются с использованием кодовой страницы пользовательского интерфейса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fb62a-105">If this bit flag is set, fonts are created using the user's default UI code page.</span></span> <span data-ttu-id="fb62a-106">Если битовый флаг не установлен, шрифты создаются с помощью кодовой страницы базы данных.</span><span class="sxs-lookup"><span data-stu-id="fb62a-106">If the bit flag is not set, fonts are created using the database code page.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="fb62a-107">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="fb62a-107">Valid Controls</span></span>

[<span data-ttu-id="fb62a-108">Text</span><span class="sxs-lookup"><span data-stu-id="fb62a-108">Text</span></span>](text-control.md)

 

[<span data-ttu-id="fb62a-109">ListBox</span><span class="sxs-lookup"><span data-stu-id="fb62a-109">ListBox</span></span>](listbox-control.md)

 

[<span data-ttu-id="fb62a-110">ComboBox</span><span class="sxs-lookup"><span data-stu-id="fb62a-110">ComboBox</span></span>](combobox-control.md)

## <a name="value"></a><span data-ttu-id="fb62a-111">Значение</span><span class="sxs-lookup"><span data-stu-id="fb62a-111">Value</span></span>



| <span data-ttu-id="fb62a-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="fb62a-112">Decimal</span></span> | <span data-ttu-id="fb62a-113">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="fb62a-113">Hexadecimal</span></span> | <span data-ttu-id="fb62a-114">Константа</span><span class="sxs-lookup"><span data-stu-id="fb62a-114">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="fb62a-115">1048576</span><span class="sxs-lookup"><span data-stu-id="fb62a-115">1048576</span></span> | <span data-ttu-id="fb62a-116">0x00100000</span><span class="sxs-lookup"><span data-stu-id="fb62a-116">0x00100000</span></span>  | <span data-ttu-id="fb62a-117">**мсидбконтролаттрибутесусерслангуаже**</span><span class="sxs-lookup"><span data-stu-id="fb62a-117">**msidbControlAttributesUsersLanguage**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fb62a-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fb62a-118">Remarks</span></span>

<span data-ttu-id="fb62a-119">Этот атрибут элемента управления можно использовать для вывода текста, вводимых пользователем в элемент управления [Edit](edit-control.md) или [паседит](pathedit-control.md) .</span><span class="sxs-lookup"><span data-stu-id="fb62a-119">This control attribute can be used to display text that the user has entered into an [Edit](edit-control.md) or [PathEdit](pathedit-control.md) control.</span></span>

<span data-ttu-id="fb62a-120">Элемент управления Edit, Паседит Control, [директорилист Control](directorylist-control.md) и [директорикомбо](directorycombo-control.md) всегда использует шрифты, созданные в пользовательской кодовой странице пользовательского интерфейса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fb62a-120">The Edit control, PathEdit control, [DirectoryList control](directorylist-control.md) and [DirectoryCombo control](directorycombo-control.md) always use the fonts created in the user's default UI code page.</span></span> <span data-ttu-id="fb62a-121">Это может вызвать проблемы, если в операционной системе установлены дополнительные языки.</span><span class="sxs-lookup"><span data-stu-id="fb62a-121">This can cause problems if additional languages have been installed on the operating system.</span></span> <span data-ttu-id="fb62a-122">В этом случае шрифты на компьютере не могут представлять все символы в добавленных языках.</span><span class="sxs-lookup"><span data-stu-id="fb62a-122">In this case, the fonts on the computer may not be able to represent all the characters in the added languages.</span></span> <span data-ttu-id="fb62a-123">Чтобы определить, какие шрифты можно использовать, найдите значения в **hKey \_ Local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ фонтлинк \\ системлинк**.</span><span class="sxs-lookup"><span data-stu-id="fb62a-123">To determine what fonts can be used, look up the values in **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\FontLink\\SystemLink**.</span></span>

<span data-ttu-id="fb62a-124">Дополнительные сведения см. в разделе [Управление атрибутами](control-attributes.md) и [элементами управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="fb62a-124">For more information, see [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



