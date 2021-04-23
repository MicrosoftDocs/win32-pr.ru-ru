---
description: Указывает, должны ли ссылки на функции-заглушки включаться в структуры операций в определениях типов портов для односторонних и двусторонних операций.
ms.assetid: 2547f71d-8a30-4df8-ba38-6707c415708e
title: Стубфунктион, элемент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7282e7280c8d701710094b70b84a65756f7230ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266082"
---
# <a name="stubfunction-element"></a><span data-ttu-id="19205-103">Стубфунктион, элемент</span><span class="sxs-lookup"><span data-stu-id="19205-103">stubFunction element</span></span>

<span data-ttu-id="19205-104">Указывает, должны ли ссылки на функции-заглушки включаться в структуры операций в определениях типов портов для односторонних и двусторонних операций.</span><span class="sxs-lookup"><span data-stu-id="19205-104">Specifies whether stub function references should be included in the operation structures in the port type definitions for one-way and two-way operations.</span></span>

## <a name="usage"></a><span data-ttu-id="19205-105">Использование</span><span class="sxs-lookup"><span data-stu-id="19205-105">Usage</span></span>

``` syntax
<stubFunction/>
```

## <a name="attributes"></a><span data-ttu-id="19205-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="19205-106">Attributes</span></span>

<span data-ttu-id="19205-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="19205-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="19205-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="19205-108">Child elements</span></span>

<span data-ttu-id="19205-109">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="19205-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="19205-110">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="19205-110">Parent elements</span></span>



| <span data-ttu-id="19205-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="19205-111">Element</span></span>                                                       | <span data-ttu-id="19205-112">Описание</span><span class="sxs-lookup"><span data-stu-id="19205-112">Description</span></span>                                                  |
|---------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="19205-113">**порттипедефинитионс**</span><span class="sxs-lookup"><span data-stu-id="19205-113">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/> | <span data-ttu-id="19205-114">Создает константы C для типов портов.</span><span class="sxs-lookup"><span data-stu-id="19205-114">Generates C constants for port types.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="19205-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19205-115">Remarks</span></span>

<span data-ttu-id="19205-116">Ссылки на функции-заглушки используются в сценариях размещения для односторонних и двусторонних операций.</span><span class="sxs-lookup"><span data-stu-id="19205-116">Stub function references are used in hosting scenarios for one-way and two-way operations.</span></span>

<span data-ttu-id="19205-117">Допустимые значения для этого элемента: 1 (включены ссылки на функции-заглушки) и 0 (ложь/нет ссылок на функции-заглушки).</span><span class="sxs-lookup"><span data-stu-id="19205-117">Valid values for this element are 1 (TRUE/stub function references included) and 0 (FALSE/no stub function references included).</span></span>

## <a name="element-information"></a><span data-ttu-id="19205-118">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="19205-118">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="19205-119">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="19205-119">Minimum supported system</span></span><br/> | <span data-ttu-id="19205-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19205-120">Windows Vista</span></span> |
| <span data-ttu-id="19205-121">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="19205-121">Can be empty</span></span>                        | <span data-ttu-id="19205-122">Да</span><span class="sxs-lookup"><span data-stu-id="19205-122">Yes</span></span>           |



 

 




