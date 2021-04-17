---
description: Создает функции для создания типизированных прокси-серверов.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: Проксибуилдеримплементатионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2cb64a6ea87b1083871931359a4f7c01ece9b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702745"
---
# <a name="proxybuilderimplementations-element"></a><span data-ttu-id="90d87-103">Проксибуилдеримплементатионс, элемент</span><span class="sxs-lookup"><span data-stu-id="90d87-103">proxyBuilderImplementations element</span></span>

<span data-ttu-id="90d87-104">Создает функции для создания типизированных прокси-серверов.</span><span class="sxs-lookup"><span data-stu-id="90d87-104">Generates functions to create typed proxies.</span></span>

## <a name="usage"></a><span data-ttu-id="90d87-105">Использование</span><span class="sxs-lookup"><span data-stu-id="90d87-105">Usage</span></span>

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a><span data-ttu-id="90d87-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="90d87-106">Attributes</span></span>

<span data-ttu-id="90d87-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="90d87-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="90d87-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="90d87-108">Child elements</span></span>



| <span data-ttu-id="90d87-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="90d87-109">Element</span></span>                                     | <span data-ttu-id="90d87-110">Описание</span><span class="sxs-lookup"><span data-stu-id="90d87-110">Description</span></span>                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90d87-111">**Обеспечения**</span><span class="sxs-lookup"><span data-stu-id="90d87-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="90d87-112">Имя, используемое для типа порта в созданном коде.</span><span class="sxs-lookup"><span data-stu-id="90d87-112">The name to be used for the port type in the generated code.</span></span> <span data-ttu-id="90d87-113">По умолчанию имя кода создается на основе полного имени типа порта.</span><span class="sxs-lookup"><span data-stu-id="90d87-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="90d87-114">**Порта**</span><span class="sxs-lookup"><span data-stu-id="90d87-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="90d87-115">Тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="90d87-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                             |
| [<span data-ttu-id="90d87-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="90d87-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="90d87-117">Имя класса, создаваемого из функции построителя прокси.</span><span class="sxs-lookup"><span data-stu-id="90d87-117">Class name to generate from the proxy builder function.</span></span><br/> <br/>                                                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="90d87-118">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="90d87-118">Child element sequence</span></span>

``` syntax
(
  proxyClass, 
  portType+, 
  codeName
)
```

## <a name="parent-elements"></a><span data-ttu-id="90d87-119">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="90d87-119">Parent elements</span></span>



| <span data-ttu-id="90d87-120">Элемент</span><span class="sxs-lookup"><span data-stu-id="90d87-120">Element</span></span>                         | <span data-ttu-id="90d87-121">Описание</span><span class="sxs-lookup"><span data-stu-id="90d87-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="90d87-122">**File**</span><span class="sxs-lookup"><span data-stu-id="90d87-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="90d87-123">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="90d87-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="90d87-124">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="90d87-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="90d87-125">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="90d87-125">Minimum supported system</span></span><br/> | <span data-ttu-id="90d87-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90d87-126">Windows Vista</span></span> |
| <span data-ttu-id="90d87-127">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="90d87-127">Can be empty</span></span>                        | <span data-ttu-id="90d87-128">Нет</span><span class="sxs-lookup"><span data-stu-id="90d87-128">No</span></span>            |



 

 




