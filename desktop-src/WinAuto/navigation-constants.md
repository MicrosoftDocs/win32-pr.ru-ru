---
title: Константы навигации (Олеакк. h)
description: В этом разделе описываются константные значения, определенные в олеакк. h, которые указывают на пространственный (вверх, вниз, слева и справа) или логическое (первое дочернее, Последнее, следующее и предыдущее) направление, наблюдаемое, когда клиенты используют IAccessible Аккнавигате для перехода от одного элемента пользовательского интерфейса к другому в пределах того же контейнера.
ms.assetid: 5859a7a3-bcd3-443e-8ff0-4952f4639517
topic_type:
- apiref
api_name:
- NAVDIR_DOWN
- NAVDIR_FIRSTCHILD
- NAVDIR_LASTCHILD
- NAVDIR_LEFT
- NAVDIR_NEXT
- NAVDIR_PREVIOUS
- NAVDIR_RIGHT
- NAVDIR_UP
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8de5f4eaa3fc7fb24583e49bdd14acb9633b2bd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657219"
---
# <a name="navigation-constants"></a><span data-ttu-id="d692b-103">Константы навигации</span><span class="sxs-lookup"><span data-stu-id="d692b-103">Navigation Constants</span></span>

<span data-ttu-id="d692b-104">В этом разделе описываются константные значения, определенные в олеакк. h, которые указывают на *пространственный* (вверх, вниз, слева и справа) или *логический* (первый дочерний, последний, следующий и предыдущий) направление, которое наблюдается, когда клиенты используют [**IAccessible:: аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) для перехода от одного элемента пользовательского интерфейса к другому в пределах того же контейнера.</span><span class="sxs-lookup"><span data-stu-id="d692b-104">This topic describes the constant values, defined in oleacc.h, that indicate the *spatial* (up, down, left, and right) or *logical* (first child, last, next, and previous) direction observed when clients use [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) to navigate from one user interface element to another within the same container.</span></span> <span data-ttu-id="d692b-105">Дополнительные сведения см. в разделе [Свойства и методы навигации по объектам](object-navigation-properties-and-methods.md).</span><span class="sxs-lookup"><span data-stu-id="d692b-105">For more information, see [Object Navigation Properties and Methods](object-navigation-properties-and-methods.md).</span></span>

<span data-ttu-id="d692b-106">Ниже перечислены константы навигации Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="d692b-106">The Microsoft Active Accessibility navigation constants are as follows:</span></span>



| <span data-ttu-id="d692b-107">Константа</span><span class="sxs-lookup"><span data-stu-id="d692b-107">Constant</span></span>                                                                                                                                                                  | <span data-ttu-id="d692b-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d692b-108">Description</span></span>                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NAVDIR_DOWN"></span><span id="navdir_down"></span><dl> <span data-ttu-id="d692b-109"><dt>**НАВДИР \_ вниз**</dt></span><span class="sxs-lookup"><span data-stu-id="d692b-109"><dt>**NAVDIR\_DOWN**</dt></span></span> </dl>                   | <span data-ttu-id="d692b-110">Перейдите к родственному объекту, расположенному под начальным объектом.</span><span class="sxs-lookup"><span data-stu-id="d692b-110">Navigate to the sibling object that is located below the starting object.</span></span><br/>                                                                  |
| <span id="NAVDIR_FIRSTCHILD"></span><span id="navdir_firstchild"></span><dl> <span data-ttu-id="d692b-111"><dt>**НАВДИР \_ FIRSTCHILD**</dt></span><span class="sxs-lookup"><span data-stu-id="d692b-111"><dt>**NAVDIR\_FIRSTCHILD**</dt></span></span> </dl> | <span data-ttu-id="d692b-112">Перейдите к первому дочернему элементу этого объекта.</span><span class="sxs-lookup"><span data-stu-id="d692b-112">Navigate to the first child of this object.</span></span> <span data-ttu-id="d692b-113">При использовании этого флага член **лвал** параметра *варстарт* должен иметь значение чилдид \_ Self.</span><span class="sxs-lookup"><span data-stu-id="d692b-113">When this flag is used, the **lVal** member of the *varStart* parameter must be CHILDID\_SELF.</span></span><br/> |
| <span id="NAVDIR_LASTCHILD"></span><span id="navdir_lastchild"></span><dl> <span data-ttu-id="d692b-114"><dt>**НАВДИР \_ LASTCHILD**</dt></span><span class="sxs-lookup"><span data-stu-id="d692b-114"><dt>**NAVDIR\_LASTCHILD**</dt></span></span> </dl>    | <span data-ttu-id="d692b-115">Перейдите к последнему дочернему элементу этого объекта.</span><span class="sxs-lookup"><span data-stu-id="d692b-115">Navigate to the last child of this object.</span></span> <span data-ttu-id="d692b-116">При использовании этого флага член **лвал** параметра *варстарт* должен иметь значение чилдид \_ Self.</span><span class="sxs-lookup"><span data-stu-id="d692b-116">When using this flag, the **lVal** member of the *varStart* parameter must be CHILDID\_SELF.</span></span><br/>    |
| <span id="NAVDIR_LEFT"></span><span id="navdir_left"></span><dl> <span data-ttu-id="d692b-117"><dt>**НАВДИР \_ слева**</dt></span><span class="sxs-lookup"><span data-stu-id="d692b-117"><dt>**NAVDIR\_LEFT**</dt></span></span> </dl>                   | <span data-ttu-id="d692b-118">Перейдите к родственному объекту, расположенному слева от начального объекта.</span><span class="sxs-lookup"><span data-stu-id="d692b-118">Navigate to the sibling object located to the left of the starting object.</span></span><br/>                                                                 |
| <span id="NAVDIR_NEXT"></span><span id="navdir_next"></span><dl> <span data-ttu-id="d692b-119"><dt>**НАВДИР \_ Далее**</dt></span><span class="sxs-lookup"><span data-stu-id="d692b-119"><dt>**NAVDIR\_NEXT**</dt></span></span> </dl>                   | <span data-ttu-id="d692b-120">Перейдите к следующему логическому объекту. как правило, это элемент того же уровня, что и начальный объект.</span><span class="sxs-lookup"><span data-stu-id="d692b-120">Navigate to the next logical object; generally, it is a sibling of the starting object.</span></span><br/>                                                    |
| <span id="NAVDIR_PREVIOUS"></span><span id="navdir_previous"></span><dl> <span data-ttu-id="d692b-121"><dt>**НАВДИР \_ назад**</dt></span><span class="sxs-lookup"><span data-stu-id="d692b-121"><dt>**NAVDIR\_PREVIOUS**</dt></span></span> </dl>       | <span data-ttu-id="d692b-122">Перейдите к предыдущему логическому объекту. как правило, это элемент того же уровня, что и начальный объект.</span><span class="sxs-lookup"><span data-stu-id="d692b-122">Navigate to the previous logical object; generally, it is a sibling of the starting object.</span></span><br/>                                                |
| <span id="NAVDIR_RIGHT"></span><span id="navdir_right"></span><dl> <span data-ttu-id="d692b-123"><dt>**НАВДИР \_ вправо**</dt></span><span class="sxs-lookup"><span data-stu-id="d692b-123"><dt>**NAVDIR\_RIGHT**</dt></span></span> </dl>                | <span data-ttu-id="d692b-124">Перейдите к родственному объекту, расположенному справа от начального объекта.</span><span class="sxs-lookup"><span data-stu-id="d692b-124">Navigate to the sibling object that is located to the right of the starting object.</span></span><br/>                                                        |
| <span id="NAVDIR_UP"></span><span id="navdir_up"></span><dl> <span data-ttu-id="d692b-125"><dt>**НАВДИР \_ up**</dt></span><span class="sxs-lookup"><span data-stu-id="d692b-125"><dt>**NAVDIR\_UP**</dt></span></span> </dl>                         | <span data-ttu-id="d692b-126">Перейдите к родственному объекту, расположенному над начальным объектом.</span><span class="sxs-lookup"><span data-stu-id="d692b-126">Navigate to the sibling object that is located above the starting object.</span></span><br/>                                                                  |



## <a name="requirements"></a><span data-ttu-id="d692b-127">Требования</span><span class="sxs-lookup"><span data-stu-id="d692b-127">Requirements</span></span>



| <span data-ttu-id="d692b-128">Требование</span><span class="sxs-lookup"><span data-stu-id="d692b-128">Requirement</span></span> | <span data-ttu-id="d692b-129">Значение</span><span class="sxs-lookup"><span data-stu-id="d692b-129">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d692b-130">Header</span><span class="sxs-lookup"><span data-stu-id="d692b-130">Header</span></span><br/> | <dl> <span data-ttu-id="d692b-131"><dt>Олеакк. h</dt></span><span class="sxs-lookup"><span data-stu-id="d692b-131"><dt>Oleacc.h</dt></span></span> </dl> |



 

 





