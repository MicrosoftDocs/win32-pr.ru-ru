---
description: Создает реализации для функций-заглушек для операций с типом порта.
ms.assetid: 69899302-db54-493b-90de-596750be566f
title: Стубдефинитионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42c60b071c901538122751f6e92cfd7049f7be88
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994691"
---
# <a name="stubdefinitions-element"></a><span data-ttu-id="b7368-103">Стубдефинитионс, элемент</span><span class="sxs-lookup"><span data-stu-id="b7368-103">stubDefinitions element</span></span>

<span data-ttu-id="b7368-104">Создает реализации для функций-заглушек для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="b7368-104">Generates implementations for stub functions for port-type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="b7368-105">Использование</span><span class="sxs-lookup"><span data-stu-id="b7368-105">Usage</span></span>

``` syntax
<stubDefinitions>
  child elements
</stubDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="b7368-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b7368-106">Attributes</span></span>

<span data-ttu-id="b7368-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b7368-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b7368-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b7368-108">Child elements</span></span>



| <span data-ttu-id="b7368-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="b7368-109">Element</span></span>                                                         | <span data-ttu-id="b7368-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b7368-110">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7368-111">**не предусматривающую**</span><span class="sxs-lookup"><span data-stu-id="b7368-111">**deallocator**</span></span>](deallocator.md)<br/>                   | <span data-ttu-id="b7368-112">Указывает тип дераспределителя, используемый функцией-заглушкой.</span><span class="sxs-lookup"><span data-stu-id="b7368-112">Specifies the type of deallocator to be used by a stub function.</span></span><br/> <br/>                                 |
| [<span data-ttu-id="b7368-113">**eventArg**</span><span class="sxs-lookup"><span data-stu-id="b7368-113">**eventArg**</span></span>](eventarg.md)<br/>                         | <span data-ttu-id="b7368-114">Указывает, включаются ли в создаваемые функции связанные аргументы события.</span><span class="sxs-lookup"><span data-stu-id="b7368-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="b7368-115">**событиях**</span><span class="sxs-lookup"><span data-stu-id="b7368-115">**events**</span></span>](events.md)<br/>                             | <span data-ttu-id="b7368-116">Указывает, включаются ли в создаваемые функции связанные события.</span><span class="sxs-lookup"><span data-stu-id="b7368-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="b7368-117">**фаултинфо**</span><span class="sxs-lookup"><span data-stu-id="b7368-117">**faultInfo**</span></span>](faultinfo.md)<br/>                       | <span data-ttu-id="b7368-118">Указывает, включаются ли в создаваемые функции параметры, используемые для передачи сведений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="b7368-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="b7368-119">**операцию**</span><span class="sxs-lookup"><span data-stu-id="b7368-119">**operation**</span></span>](operation.md)<br/>                       | <span data-ttu-id="b7368-120">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="b7368-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="b7368-121">**оператиондеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="b7368-121">**operationDeallocator**</span></span>](operationdeallocator.md)<br/> | <span data-ttu-id="b7368-122">Указывает тип дераспределителя, используемый функцией-заглушкой операции.</span><span class="sxs-lookup"><span data-stu-id="b7368-122">Specifies the type of deallocator to be used by an operation's stub function.</span></span><br/> <br/>                    |
| [<span data-ttu-id="b7368-123">**Порта**</span><span class="sxs-lookup"><span data-stu-id="b7368-123">**portType**</span></span>](porttype.md)<br/>                         | <span data-ttu-id="b7368-124">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="b7368-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="b7368-125">**серверкласс**</span><span class="sxs-lookup"><span data-stu-id="b7368-125">**serverClass**</span></span>](serverclass.md)<br/>                   | <span data-ttu-id="b7368-126">Указывает имя класса сервера на стороне узла.</span><span class="sxs-lookup"><span data-stu-id="b7368-126">Specifies the name of the host-side server class.</span></span><br/> <br/>                                                |



### <a name="child-element-sequence"></a><span data-ttu-id="b7368-127">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="b7368-127">Child element sequence</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="b7368-128">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b7368-128">Parent elements</span></span>



| <span data-ttu-id="b7368-129">Элемент</span><span class="sxs-lookup"><span data-stu-id="b7368-129">Element</span></span>                         | <span data-ttu-id="b7368-130">Описание</span><span class="sxs-lookup"><span data-stu-id="b7368-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="b7368-131">**File**</span><span class="sxs-lookup"><span data-stu-id="b7368-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="b7368-132">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="b7368-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="b7368-133">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b7368-133">Element information</span></span>



| <span data-ttu-id="b7368-134">Метка</span><span class="sxs-lookup"><span data-stu-id="b7368-134">Label</span></span> | <span data-ttu-id="b7368-135">Значение</span><span class="sxs-lookup"><span data-stu-id="b7368-135">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="b7368-136">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="b7368-136">Minimum supported system</span></span><br/> | <span data-ttu-id="b7368-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7368-137">Windows Vista</span></span> |
| <span data-ttu-id="b7368-138">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="b7368-138">Can be empty</span></span>                        | <span data-ttu-id="b7368-139">нет</span><span class="sxs-lookup"><span data-stu-id="b7368-139">No</span></span>            |



 

 




