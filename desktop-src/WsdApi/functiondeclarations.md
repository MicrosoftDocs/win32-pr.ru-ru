---
description: Создает объявления реализации для функций-посредников для операций с типом порта.
ms.assetid: 6ba7dbb6-6598-4569-97e1-d703e4b896c7
title: Функтиондекларатионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b82aca30f94fc8fcec80701a74b56e83ab674c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264647"
---
# <a name="functiondeclarations-element"></a><span data-ttu-id="0676b-103">Функтиондекларатионс, элемент</span><span class="sxs-lookup"><span data-stu-id="0676b-103">functionDeclarations element</span></span>

<span data-ttu-id="0676b-104">Создает объявления реализации для функций-посредников для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="0676b-104">Generates implementation declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="0676b-105">Использование</span><span class="sxs-lookup"><span data-stu-id="0676b-105">Usage</span></span>

``` syntax
<functionDeclarations>
  child elements
</functionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="0676b-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0676b-106">Attributes</span></span>

<span data-ttu-id="0676b-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="0676b-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0676b-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0676b-108">Child elements</span></span>



| <span data-ttu-id="0676b-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="0676b-109">Element</span></span>                                   | <span data-ttu-id="0676b-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0676b-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0676b-111">**async**</span><span class="sxs-lookup"><span data-stu-id="0676b-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="0676b-112">Указывает, включаются ли асинхронные операции в создаваемые прокси-функции.</span><span class="sxs-lookup"><span data-stu-id="0676b-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="0676b-113">**событиях**</span><span class="sxs-lookup"><span data-stu-id="0676b-113">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="0676b-114">Указывает, включаются ли в создаваемые функции связанные события.</span><span class="sxs-lookup"><span data-stu-id="0676b-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="0676b-115">**фаултинфо**</span><span class="sxs-lookup"><span data-stu-id="0676b-115">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="0676b-116">Указывает, включаются ли в создаваемые функции параметры, используемые для передачи сведений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="0676b-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="0676b-117">**операцию**</span><span class="sxs-lookup"><span data-stu-id="0676b-117">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="0676b-118">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="0676b-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="0676b-119">**Порта**</span><span class="sxs-lookup"><span data-stu-id="0676b-119">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="0676b-120">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="0676b-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="0676b-121">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="0676b-121">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="0676b-122">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="0676b-122">Parent elements</span></span>



| <span data-ttu-id="0676b-123">Элемент</span><span class="sxs-lookup"><span data-stu-id="0676b-123">Element</span></span>                         | <span data-ttu-id="0676b-124">Описание</span><span class="sxs-lookup"><span data-stu-id="0676b-124">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="0676b-125">**File**</span><span class="sxs-lookup"><span data-stu-id="0676b-125">**file**</span></span>](file.md)<br/> | <span data-ttu-id="0676b-126">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="0676b-126">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0676b-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0676b-127">Remarks</span></span>

<span data-ttu-id="0676b-128">Этот элемент создает объявления функций элементов, соответствующих операциям, вызываемым контрактом.</span><span class="sxs-lookup"><span data-stu-id="0676b-128">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="0676b-129">Эти объявления находятся в форме, подходящей для использования компилятором C++ и обычно используются в cpp-файлах.</span><span class="sxs-lookup"><span data-stu-id="0676b-129">These declarations are in a form appropriate for consumption by a C++ compiler and are generally used in .cpp files.</span></span>

<span data-ttu-id="0676b-130">Пример.</span><span class="sxs-lookup"><span data-stu-id="0676b-130">Example:</span></span>

``` syntax
<functionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="0676b-131">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0676b-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="0676b-132">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="0676b-132">Minimum supported system</span></span><br/> | <span data-ttu-id="0676b-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0676b-133">Windows Vista</span></span> |
| <span data-ttu-id="0676b-134">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="0676b-134">Can be empty</span></span>                        | <span data-ttu-id="0676b-135">Да</span><span class="sxs-lookup"><span data-stu-id="0676b-135">Yes</span></span>           |



 

 




