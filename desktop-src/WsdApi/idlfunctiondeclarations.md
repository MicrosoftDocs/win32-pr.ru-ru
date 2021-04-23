---
description: Создает объявления IDL для функций-посредников для операций с типом порта.
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: Идлфунктиондекларатионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1afa43676898231f739804185b8bf5d6e2b4faf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711711"
---
# <a name="idlfunctiondeclarations-element"></a><span data-ttu-id="13760-103">Идлфунктиондекларатионс, элемент</span><span class="sxs-lookup"><span data-stu-id="13760-103">idlFunctionDeclarations element</span></span>

<span data-ttu-id="13760-104">Создает объявления IDL для функций-посредников для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="13760-104">Generates IDL declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="13760-105">Использование</span><span class="sxs-lookup"><span data-stu-id="13760-105">Usage</span></span>

``` syntax
<idlFunctionDeclarations>
  child elements
</idlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="13760-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="13760-106">Attributes</span></span>

<span data-ttu-id="13760-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="13760-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="13760-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="13760-108">Child elements</span></span>



| <span data-ttu-id="13760-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="13760-109">Element</span></span>                                   | <span data-ttu-id="13760-110">Описание</span><span class="sxs-lookup"><span data-stu-id="13760-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13760-111">**async**</span><span class="sxs-lookup"><span data-stu-id="13760-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="13760-112">Указывает, включаются ли асинхронные операции в создаваемые прокси-функции.</span><span class="sxs-lookup"><span data-stu-id="13760-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="13760-113">**eventArg**</span><span class="sxs-lookup"><span data-stu-id="13760-113">**eventArg**</span></span>](eventarg.md)<br/>   | <span data-ttu-id="13760-114">Указывает, включаются ли в создаваемые функции связанные аргументы события.</span><span class="sxs-lookup"><span data-stu-id="13760-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="13760-115">**событиях**</span><span class="sxs-lookup"><span data-stu-id="13760-115">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="13760-116">Указывает, включаются ли в создаваемые функции связанные события.</span><span class="sxs-lookup"><span data-stu-id="13760-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="13760-117">**фаултинфо**</span><span class="sxs-lookup"><span data-stu-id="13760-117">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="13760-118">Указывает, включаются ли в создаваемые функции параметры, используемые для передачи сведений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="13760-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="13760-119">**операцию**</span><span class="sxs-lookup"><span data-stu-id="13760-119">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="13760-120">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="13760-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="13760-121">**Порта**</span><span class="sxs-lookup"><span data-stu-id="13760-121">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="13760-122">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="13760-122">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="13760-123">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="13760-123">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  eventArg?, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="13760-124">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="13760-124">Parent elements</span></span>



| <span data-ttu-id="13760-125">Элемент</span><span class="sxs-lookup"><span data-stu-id="13760-125">Element</span></span>                         | <span data-ttu-id="13760-126">Описание</span><span class="sxs-lookup"><span data-stu-id="13760-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="13760-127">**File**</span><span class="sxs-lookup"><span data-stu-id="13760-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="13760-128">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="13760-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="13760-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13760-129">Remarks</span></span>

<span data-ttu-id="13760-130">Этот элемент создает объявления функций элементов, соответствующих операциям, вызываемым контрактом.</span><span class="sxs-lookup"><span data-stu-id="13760-130">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="13760-131">Эти объявления находятся в форме, подходящей для использования компилятором MIDL и обычно используются в IDL-файлах.</span><span class="sxs-lookup"><span data-stu-id="13760-131">These declarations are in a form appropriate for consumption by the MIDL compiler and are generally used in .idl files.</span></span>

<span data-ttu-id="13760-132">Пример.</span><span class="sxs-lookup"><span data-stu-id="13760-132">Example:</span></span>

``` syntax
<idlFunctionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="13760-133">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="13760-133">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="13760-134">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="13760-134">Minimum supported system</span></span><br/> | <span data-ttu-id="13760-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13760-135">Windows Vista</span></span> |
| <span data-ttu-id="13760-136">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="13760-136">Can be empty</span></span>                        | <span data-ttu-id="13760-137">Да</span><span class="sxs-lookup"><span data-stu-id="13760-137">Yes</span></span>           |



 

 




