---
description: Создает функции для создания типизированных прокси-серверов.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: Проксибуилдеримплементатионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ad22348b33c60689adf60c029e3a08c2f4d417c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996471"
---
# <a name="proxybuilderimplementations-element"></a><span data-ttu-id="7bb74-103">Проксибуилдеримплементатионс, элемент</span><span class="sxs-lookup"><span data-stu-id="7bb74-103">proxyBuilderImplementations element</span></span>

<span data-ttu-id="7bb74-104">Создает функции для создания типизированных прокси-серверов.</span><span class="sxs-lookup"><span data-stu-id="7bb74-104">Generates functions to create typed proxies.</span></span>

## <a name="usage"></a><span data-ttu-id="7bb74-105">Использование</span><span class="sxs-lookup"><span data-stu-id="7bb74-105">Usage</span></span>

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a><span data-ttu-id="7bb74-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7bb74-106">Attributes</span></span>

<span data-ttu-id="7bb74-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="7bb74-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7bb74-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7bb74-108">Child elements</span></span>



| <span data-ttu-id="7bb74-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="7bb74-109">Element</span></span>                                     | <span data-ttu-id="7bb74-110">Описание</span><span class="sxs-lookup"><span data-stu-id="7bb74-110">Description</span></span>                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7bb74-111">**Обеспечения**</span><span class="sxs-lookup"><span data-stu-id="7bb74-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="7bb74-112">Имя, используемое для типа порта в созданном коде.</span><span class="sxs-lookup"><span data-stu-id="7bb74-112">The name to be used for the port type in the generated code.</span></span> <span data-ttu-id="7bb74-113">По умолчанию имя кода создается на основе полного имени типа порта.</span><span class="sxs-lookup"><span data-stu-id="7bb74-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="7bb74-114">**Порта**</span><span class="sxs-lookup"><span data-stu-id="7bb74-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="7bb74-115">Тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="7bb74-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                             |
| [<span data-ttu-id="7bb74-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="7bb74-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="7bb74-117">Имя класса, создаваемого из функции построителя прокси.</span><span class="sxs-lookup"><span data-stu-id="7bb74-117">Class name to generate from the proxy builder function.</span></span><br/> <br/>                                                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="7bb74-118">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="7bb74-118">Child element sequence</span></span>

``` syntax
(
  proxyClass, 
  portType+, 
  codeName
)
```

## <a name="parent-elements"></a><span data-ttu-id="7bb74-119">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="7bb74-119">Parent elements</span></span>



| <span data-ttu-id="7bb74-120">Элемент</span><span class="sxs-lookup"><span data-stu-id="7bb74-120">Element</span></span>                         | <span data-ttu-id="7bb74-121">Описание</span><span class="sxs-lookup"><span data-stu-id="7bb74-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="7bb74-122">**File**</span><span class="sxs-lookup"><span data-stu-id="7bb74-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="7bb74-123">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="7bb74-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="7bb74-124">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7bb74-124">Element information</span></span>



| <span data-ttu-id="7bb74-125">Метка</span><span class="sxs-lookup"><span data-stu-id="7bb74-125">Label</span></span> | <span data-ttu-id="7bb74-126">Значение</span><span class="sxs-lookup"><span data-stu-id="7bb74-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="7bb74-127">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="7bb74-127">Minimum supported system</span></span><br/> | <span data-ttu-id="7bb74-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7bb74-128">Windows Vista</span></span> |
| <span data-ttu-id="7bb74-129">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="7bb74-129">Can be empty</span></span>                        | <span data-ttu-id="7bb74-130">нет</span><span class="sxs-lookup"><span data-stu-id="7bb74-130">No</span></span>            |



 

 




