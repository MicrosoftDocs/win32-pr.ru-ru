---
description: Создает реализации для функций-посредников для операций с типом порта.
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: Проксифунктионимплементатионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a27e217cfa3d0a9efd204a1b18c7b2f0ca16f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911963"
---
# <a name="proxyfunctionimplementations-element"></a><span data-ttu-id="7a7f4-103">Проксифунктионимплементатионс, элемент</span><span class="sxs-lookup"><span data-stu-id="7a7f4-103">proxyFunctionImplementations element</span></span>

<span data-ttu-id="7a7f4-104">Создает реализации для функций-посредников для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-104">Generates implementations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="7a7f4-105">Использование</span><span class="sxs-lookup"><span data-stu-id="7a7f4-105">Usage</span></span>

``` syntax
<proxyFunctionImplementations>
  child elements
</proxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="7a7f4-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7a7f4-106">Attributes</span></span>

<span data-ttu-id="7a7f4-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7a7f4-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7a7f4-108">Child elements</span></span>



| <span data-ttu-id="7a7f4-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="7a7f4-109">Element</span></span>                                     | <span data-ttu-id="7a7f4-110">Описание</span><span class="sxs-lookup"><span data-stu-id="7a7f4-110">Description</span></span>                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7a7f4-111">**async**</span><span class="sxs-lookup"><span data-stu-id="7a7f4-111">**async**</span></span>](async.md)<br/>           | <span data-ttu-id="7a7f4-112">Указывает, включаются ли асинхронные операции в создаваемые прокси-функции.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="7a7f4-113">**событиях**</span><span class="sxs-lookup"><span data-stu-id="7a7f4-113">**events**</span></span>](events.md)<br/>         | <span data-ttu-id="7a7f4-114">Указывает, включаются ли в создаваемые функции связанные события.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="7a7f4-115">**фаултинфо**</span><span class="sxs-lookup"><span data-stu-id="7a7f4-115">**faultInfo**</span></span>](faultinfo.md)<br/>   | <span data-ttu-id="7a7f4-116">Указывает, включаются ли в создаваемые функции параметры, используемые для передачи сведений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="7a7f4-117">**операцию**</span><span class="sxs-lookup"><span data-stu-id="7a7f4-117">**operation**</span></span>](operation.md)<br/>   | <span data-ttu-id="7a7f4-118">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="7a7f4-119">**Порта**</span><span class="sxs-lookup"><span data-stu-id="7a7f4-119">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="7a7f4-120">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="7a7f4-121">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="7a7f4-121">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="7a7f4-122">Указывает имя класса прокси на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-122">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                                               |



### <a name="child-element-sequence"></a><span data-ttu-id="7a7f4-123">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="7a7f4-123">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="7a7f4-124">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="7a7f4-124">Parent elements</span></span>



| <span data-ttu-id="7a7f4-125">Элемент</span><span class="sxs-lookup"><span data-stu-id="7a7f4-125">Element</span></span>                         | <span data-ttu-id="7a7f4-126">Описание</span><span class="sxs-lookup"><span data-stu-id="7a7f4-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="7a7f4-127">**File**</span><span class="sxs-lookup"><span data-stu-id="7a7f4-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="7a7f4-128">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="7a7f4-129">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7a7f4-129">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="7a7f4-130">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="7a7f4-130">Minimum supported system</span></span><br/> | <span data-ttu-id="7a7f4-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a7f4-131">Windows Vista</span></span> |
| <span data-ttu-id="7a7f4-132">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="7a7f4-132">Can be empty</span></span>                        | <span data-ttu-id="7a7f4-133">Да</span><span class="sxs-lookup"><span data-stu-id="7a7f4-133">Yes</span></span>           |



 

 




