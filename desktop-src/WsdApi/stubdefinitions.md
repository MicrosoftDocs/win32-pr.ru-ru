---
description: Создает реализации для функций-заглушек для операций с типом порта.
ms.assetid: 69899302-db54-493b-90de-596750be566f
title: Стубдефинитионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6676cfc6cf55aa9c9961bd614506500d847def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693154"
---
# <a name="stubdefinitions-element"></a><span data-ttu-id="9a98f-103">Стубдефинитионс, элемент</span><span class="sxs-lookup"><span data-stu-id="9a98f-103">stubDefinitions element</span></span>

<span data-ttu-id="9a98f-104">Создает реализации для функций-заглушек для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="9a98f-104">Generates implementations for stub functions for port-type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="9a98f-105">Использование</span><span class="sxs-lookup"><span data-stu-id="9a98f-105">Usage</span></span>

``` syntax
<stubDefinitions>
  child elements
</stubDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="9a98f-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9a98f-106">Attributes</span></span>

<span data-ttu-id="9a98f-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="9a98f-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9a98f-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9a98f-108">Child elements</span></span>



| <span data-ttu-id="9a98f-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="9a98f-109">Element</span></span>                                                         | <span data-ttu-id="9a98f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9a98f-110">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a98f-111">**не предусматривающую**</span><span class="sxs-lookup"><span data-stu-id="9a98f-111">**deallocator**</span></span>](deallocator.md)<br/>                   | <span data-ttu-id="9a98f-112">Указывает тип дераспределителя, используемый функцией-заглушкой.</span><span class="sxs-lookup"><span data-stu-id="9a98f-112">Specifies the type of deallocator to be used by a stub function.</span></span><br/> <br/>                                 |
| [<span data-ttu-id="9a98f-113">**eventArg**</span><span class="sxs-lookup"><span data-stu-id="9a98f-113">**eventArg**</span></span>](eventarg.md)<br/>                         | <span data-ttu-id="9a98f-114">Указывает, включаются ли в создаваемые функции связанные аргументы события.</span><span class="sxs-lookup"><span data-stu-id="9a98f-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="9a98f-115">**событиях**</span><span class="sxs-lookup"><span data-stu-id="9a98f-115">**events**</span></span>](events.md)<br/>                             | <span data-ttu-id="9a98f-116">Указывает, включаются ли в создаваемые функции связанные события.</span><span class="sxs-lookup"><span data-stu-id="9a98f-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="9a98f-117">**фаултинфо**</span><span class="sxs-lookup"><span data-stu-id="9a98f-117">**faultInfo**</span></span>](faultinfo.md)<br/>                       | <span data-ttu-id="9a98f-118">Указывает, включаются ли в создаваемые функции параметры, используемые для передачи сведений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="9a98f-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="9a98f-119">**операцию**</span><span class="sxs-lookup"><span data-stu-id="9a98f-119">**operation**</span></span>](operation.md)<br/>                       | <span data-ttu-id="9a98f-120">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="9a98f-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="9a98f-121">**оператиондеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="9a98f-121">**operationDeallocator**</span></span>](operationdeallocator.md)<br/> | <span data-ttu-id="9a98f-122">Указывает тип дераспределителя, используемый функцией-заглушкой операции.</span><span class="sxs-lookup"><span data-stu-id="9a98f-122">Specifies the type of deallocator to be used by an operation's stub function.</span></span><br/> <br/>                    |
| [<span data-ttu-id="9a98f-123">**Порта**</span><span class="sxs-lookup"><span data-stu-id="9a98f-123">**portType**</span></span>](porttype.md)<br/>                         | <span data-ttu-id="9a98f-124">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="9a98f-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="9a98f-125">**серверкласс**</span><span class="sxs-lookup"><span data-stu-id="9a98f-125">**serverClass**</span></span>](serverclass.md)<br/>                   | <span data-ttu-id="9a98f-126">Указывает имя класса сервера на стороне узла.</span><span class="sxs-lookup"><span data-stu-id="9a98f-126">Specifies the name of the host-side server class.</span></span><br/> <br/>                                                |



### <a name="child-element-sequence"></a><span data-ttu-id="9a98f-127">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="9a98f-127">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  serverClass, 
  eventArg?, 
  events?, 
  operationDeallocator*, 
  deallocator?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="9a98f-128">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="9a98f-128">Parent elements</span></span>



| <span data-ttu-id="9a98f-129">Элемент</span><span class="sxs-lookup"><span data-stu-id="9a98f-129">Element</span></span>                         | <span data-ttu-id="9a98f-130">Описание</span><span class="sxs-lookup"><span data-stu-id="9a98f-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="9a98f-131">**File**</span><span class="sxs-lookup"><span data-stu-id="9a98f-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="9a98f-132">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="9a98f-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="9a98f-133">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9a98f-133">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="9a98f-134">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="9a98f-134">Minimum supported system</span></span><br/> | <span data-ttu-id="9a98f-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a98f-135">Windows Vista</span></span> |
| <span data-ttu-id="9a98f-136">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="9a98f-136">Can be empty</span></span>                        | <span data-ttu-id="9a98f-137">Нет</span><span class="sxs-lookup"><span data-stu-id="9a98f-137">No</span></span>            |



 

 




