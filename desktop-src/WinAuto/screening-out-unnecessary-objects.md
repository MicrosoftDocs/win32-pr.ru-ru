---
title: Блокировка ненужных объектов
description: При использовании проверки для изучения простого элемента управления, такого как кнопка "ОК" в программе Microsoft WordPad, видно, что эти объекты родительского окна также содержат несколько невидимых дочерних объектов.
ms.assetid: 30884e11-cc73-4bb8-9d9e-b9f1b53c4193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb341881ee2ea503b1f74643723a1f90c8e5d1d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700493"
---
# <a name="screening-out-unnecessary-objects"></a><span data-ttu-id="c77f6-103">Блокировка ненужных объектов</span><span class="sxs-lookup"><span data-stu-id="c77f6-103">Screening Out Unnecessary Objects</span></span>

<span data-ttu-id="c77f6-104">При использовании [проверки](inspect-objects.md) для изучения простого элемента управления, такого как кнопка "ОК" в программе Microsoft WordPad, видно, что эти объекты родительского окна также содержат несколько невидимых дочерних объектов.</span><span class="sxs-lookup"><span data-stu-id="c77f6-104">If you use [Inspect](inspect-objects.md) to examine a simple control such as an OK push button in the Microsoft WordPad accessory, you can see that these parent window objects also contain several invisible child objects.</span></span> <span data-ttu-id="c77f6-105">Эти невидимые объекты имеют то же имя класса окна, что и элемент управления, и [свойство State](state-property.md) [**\_ системы состояний \_ невидимо**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c77f6-105">These invisible objects have the same window class name as the control and have the [State property](state-property.md) of [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> <span data-ttu-id="c77f6-106">В следующей таблице перечислены невидимые дочерние объекты, создаваемые Microsoft Active Accessibility для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c77f6-106">The following table lists the invisible child objects that Microsoft Active Accessibility creates for the control.</span></span>



| <span data-ttu-id="c77f6-107">Имя</span><span class="sxs-lookup"><span data-stu-id="c77f6-107">Name</span></span>          | <span data-ttu-id="c77f6-108">Роль</span><span class="sxs-lookup"><span data-stu-id="c77f6-108">Role</span></span>                                                                  | <span data-ttu-id="c77f6-109">ChildCount</span><span class="sxs-lookup"><span data-stu-id="c77f6-109">ChildCount</span></span> |
|---------------|-----------------------------------------------------------------------|------------|
| <span data-ttu-id="c77f6-110">Системой</span><span class="sxs-lookup"><span data-stu-id="c77f6-110">"System"</span></span>      | [<span data-ttu-id="c77f6-111">**\_ \_ строка подменю системы ролей**</span><span class="sxs-lookup"><span data-stu-id="c77f6-111">**ROLE\_SYSTEM\_MENUBAR**</span></span>](object-roles.md)     | <span data-ttu-id="c77f6-112">0</span><span class="sxs-lookup"><span data-stu-id="c77f6-112">0</span></span>          |
| <span data-ttu-id="c77f6-113">None</span><span class="sxs-lookup"><span data-stu-id="c77f6-113">None</span></span>          | [<span data-ttu-id="c77f6-114">**\_заголовок системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="c77f6-114">**ROLE\_SYSTEM\_TITLEBAR**</span></span>](object-roles.md)   | <span data-ttu-id="c77f6-115">5</span><span class="sxs-lookup"><span data-stu-id="c77f6-115">5</span></span>          |
| <span data-ttu-id="c77f6-116">Приклад</span><span class="sxs-lookup"><span data-stu-id="c77f6-116">"Application"</span></span> | [<span data-ttu-id="c77f6-117">**\_ \_ строка подменю системы ролей**</span><span class="sxs-lookup"><span data-stu-id="c77f6-117">**ROLE\_SYSTEM\_MENUBAR**</span></span>](object-roles.md)     | <span data-ttu-id="c77f6-118">0</span><span class="sxs-lookup"><span data-stu-id="c77f6-118">0</span></span>          |
| <span data-ttu-id="c77f6-119">Вертикаль</span><span class="sxs-lookup"><span data-stu-id="c77f6-119">"Vertical"</span></span>    | [<span data-ttu-id="c77f6-120">**\_ \_ полоса прокрутки системы роли**</span><span class="sxs-lookup"><span data-stu-id="c77f6-120">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md) | <span data-ttu-id="c77f6-121">5</span><span class="sxs-lookup"><span data-stu-id="c77f6-121">5</span></span>          |
| <span data-ttu-id="c77f6-122">Горизонтал</span><span class="sxs-lookup"><span data-stu-id="c77f6-122">"Horizontal"</span></span>  | [<span data-ttu-id="c77f6-123">**\_ \_ полоса прокрутки системы роли**</span><span class="sxs-lookup"><span data-stu-id="c77f6-123">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md) | <span data-ttu-id="c77f6-124">5</span><span class="sxs-lookup"><span data-stu-id="c77f6-124">5</span></span>          |
| <span data-ttu-id="c77f6-125">"Поле размера"</span><span class="sxs-lookup"><span data-stu-id="c77f6-125">"Size Box"</span></span>    | [<span data-ttu-id="c77f6-126">**\_захват системы \_ ролей**</span><span class="sxs-lookup"><span data-stu-id="c77f6-126">**ROLE\_SYSTEM\_GRIP**</span></span>](object-roles.md)           | <span data-ttu-id="c77f6-127">0</span><span class="sxs-lookup"><span data-stu-id="c77f6-127">0</span></span>          |



 

<span data-ttu-id="c77f6-128">Разработчики клиентов должны определить и отфильтровать эти объекты родительского окна и невидимые дочерние объекты, так как они не предоставляют осмысленной информации конечным пользователям.</span><span class="sxs-lookup"><span data-stu-id="c77f6-128">Client developers must identify and filter out these parent window objects and invisible child objects because they do not provide meaningful information to end users.</span></span>

 

 




