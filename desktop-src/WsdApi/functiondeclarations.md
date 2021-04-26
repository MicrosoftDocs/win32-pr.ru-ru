---
description: Создает объявления реализации для функций-посредников для операций с типом порта.
ms.assetid: 6ba7dbb6-6598-4569-97e1-d703e4b896c7
title: Функтиондекларатионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 508cbac6d220c0ebdee0c6306d5f8a8ab5f26770
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998821"
---
# <a name="functiondeclarations-element"></a><span data-ttu-id="89784-103">Функтиондекларатионс, элемент</span><span class="sxs-lookup"><span data-stu-id="89784-103">functionDeclarations element</span></span>

<span data-ttu-id="89784-104">Создает объявления реализации для функций-посредников для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="89784-104">Generates implementation declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="89784-105">Использование</span><span class="sxs-lookup"><span data-stu-id="89784-105">Usage</span></span>

``` syntax
<functionDeclarations>
  child elements
</functionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="89784-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="89784-106">Attributes</span></span>

<span data-ttu-id="89784-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="89784-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="89784-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="89784-108">Child elements</span></span>



| <span data-ttu-id="89784-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="89784-109">Element</span></span>                                   | <span data-ttu-id="89784-110">Описание</span><span class="sxs-lookup"><span data-stu-id="89784-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="89784-111">**async**</span><span class="sxs-lookup"><span data-stu-id="89784-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="89784-112">Указывает, включаются ли асинхронные операции в создаваемые прокси-функции.</span><span class="sxs-lookup"><span data-stu-id="89784-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="89784-113">**событиях**</span><span class="sxs-lookup"><span data-stu-id="89784-113">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="89784-114">Указывает, включаются ли в создаваемые функции связанные события.</span><span class="sxs-lookup"><span data-stu-id="89784-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="89784-115">**фаултинфо**</span><span class="sxs-lookup"><span data-stu-id="89784-115">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="89784-116">Указывает, включаются ли в создаваемые функции параметры, используемые для передачи сведений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="89784-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="89784-117">**операцию**</span><span class="sxs-lookup"><span data-stu-id="89784-117">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="89784-118">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="89784-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="89784-119">**Порта**</span><span class="sxs-lookup"><span data-stu-id="89784-119">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="89784-120">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="89784-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="89784-121">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="89784-121">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="89784-122">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="89784-122">Parent elements</span></span>



| <span data-ttu-id="89784-123">Элемент</span><span class="sxs-lookup"><span data-stu-id="89784-123">Element</span></span>                         | <span data-ttu-id="89784-124">Описание</span><span class="sxs-lookup"><span data-stu-id="89784-124">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="89784-125">**File**</span><span class="sxs-lookup"><span data-stu-id="89784-125">**file**</span></span>](file.md)<br/> | <span data-ttu-id="89784-126">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="89784-126">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="89784-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="89784-127">Remarks</span></span>

<span data-ttu-id="89784-128">Этот элемент создает объявления функций элементов, соответствующих операциям, вызываемым контрактом.</span><span class="sxs-lookup"><span data-stu-id="89784-128">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="89784-129">Эти объявления находятся в форме, подходящей для использования компилятором C++ и обычно используются в cpp-файлах.</span><span class="sxs-lookup"><span data-stu-id="89784-129">These declarations are in a form appropriate for consumption by a C++ compiler and are generally used in .cpp files.</span></span>

<span data-ttu-id="89784-130">Пример</span><span class="sxs-lookup"><span data-stu-id="89784-130">Example:</span></span>

``` syntax
<functionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="89784-131">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="89784-131">Element information</span></span>



| <span data-ttu-id="89784-132">Метка</span><span class="sxs-lookup"><span data-stu-id="89784-132">Label</span></span> | <span data-ttu-id="89784-133">Значение</span><span class="sxs-lookup"><span data-stu-id="89784-133">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="89784-134">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="89784-134">Minimum supported system</span></span><br/> | <span data-ttu-id="89784-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89784-135">Windows Vista</span></span> |
| <span data-ttu-id="89784-136">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="89784-136">Can be empty</span></span>                        | <span data-ttu-id="89784-137">Да</span><span class="sxs-lookup"><span data-stu-id="89784-137">Yes</span></span>           |



 

 




