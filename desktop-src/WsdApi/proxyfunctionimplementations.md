---
description: Создает реализации для функций-посредников для операций с типом порта.
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: Проксифунктионимплементатионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9f03834ca59ede41f2f3c3dff00d7dacdd54db
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995761"
---
# <a name="proxyfunctionimplementations-element"></a><span data-ttu-id="31aed-103">Проксифунктионимплементатионс, элемент</span><span class="sxs-lookup"><span data-stu-id="31aed-103">proxyFunctionImplementations element</span></span>

<span data-ttu-id="31aed-104">Создает реализации для функций-посредников для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="31aed-104">Generates implementations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="31aed-105">Использование</span><span class="sxs-lookup"><span data-stu-id="31aed-105">Usage</span></span>

``` syntax
<proxyFunctionImplementations>
  child elements
</proxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="31aed-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="31aed-106">Attributes</span></span>

<span data-ttu-id="31aed-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="31aed-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="31aed-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="31aed-108">Child elements</span></span>



| <span data-ttu-id="31aed-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="31aed-109">Element</span></span>                                     | <span data-ttu-id="31aed-110">Описание</span><span class="sxs-lookup"><span data-stu-id="31aed-110">Description</span></span>                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31aed-111">**async**</span><span class="sxs-lookup"><span data-stu-id="31aed-111">**async**</span></span>](async.md)<br/>           | <span data-ttu-id="31aed-112">Указывает, включаются ли асинхронные операции в создаваемые прокси-функции.</span><span class="sxs-lookup"><span data-stu-id="31aed-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="31aed-113">**событиях**</span><span class="sxs-lookup"><span data-stu-id="31aed-113">**events**</span></span>](events.md)<br/>         | <span data-ttu-id="31aed-114">Указывает, включаются ли в создаваемые функции связанные события.</span><span class="sxs-lookup"><span data-stu-id="31aed-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="31aed-115">**фаултинфо**</span><span class="sxs-lookup"><span data-stu-id="31aed-115">**faultInfo**</span></span>](faultinfo.md)<br/>   | <span data-ttu-id="31aed-116">Указывает, включаются ли в создаваемые функции параметры, используемые для передачи сведений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="31aed-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="31aed-117">**операцию**</span><span class="sxs-lookup"><span data-stu-id="31aed-117">**operation**</span></span>](operation.md)<br/>   | <span data-ttu-id="31aed-118">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="31aed-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="31aed-119">**Порта**</span><span class="sxs-lookup"><span data-stu-id="31aed-119">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="31aed-120">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="31aed-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="31aed-121">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="31aed-121">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="31aed-122">Указывает имя класса прокси на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="31aed-122">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                                               |



### <a name="child-element-sequence"></a><span data-ttu-id="31aed-123">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="31aed-123">Child element sequence</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="31aed-124">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="31aed-124">Parent elements</span></span>



| <span data-ttu-id="31aed-125">Элемент</span><span class="sxs-lookup"><span data-stu-id="31aed-125">Element</span></span>                         | <span data-ttu-id="31aed-126">Описание</span><span class="sxs-lookup"><span data-stu-id="31aed-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="31aed-127">**File**</span><span class="sxs-lookup"><span data-stu-id="31aed-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="31aed-128">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="31aed-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="31aed-129">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="31aed-129">Element information</span></span>



| <span data-ttu-id="31aed-130">Метка</span><span class="sxs-lookup"><span data-stu-id="31aed-130">Label</span></span> | <span data-ttu-id="31aed-131">Значение</span><span class="sxs-lookup"><span data-stu-id="31aed-131">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="31aed-132">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="31aed-132">Minimum supported system</span></span><br/> | <span data-ttu-id="31aed-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31aed-133">Windows Vista</span></span> |
| <span data-ttu-id="31aed-134">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="31aed-134">Can be empty</span></span>                        | <span data-ttu-id="31aed-135">Да</span><span class="sxs-lookup"><span data-stu-id="31aed-135">Yes</span></span>           |



 

 




