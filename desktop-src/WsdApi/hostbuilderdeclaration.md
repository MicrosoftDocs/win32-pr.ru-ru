---
description: Создает объявление для функции, которая создает типизированный узел.
ms.assetid: 3c08e913-b47e-4ca7-b8bc-7b036e57db01
title: Хостбуилдердекларатион, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16576050efc76264f42dff6a19549f69933185b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702882"
---
# <a name="hostbuilderdeclaration-element"></a><span data-ttu-id="fb8ff-103">Хостбуилдердекларатион, элемент</span><span class="sxs-lookup"><span data-stu-id="fb8ff-103">hostBuilderDeclaration element</span></span>

<span data-ttu-id="fb8ff-104">Создает объявление для функции, которая создает типизированный узел.</span><span class="sxs-lookup"><span data-stu-id="fb8ff-104">Generates a declaration for a function that creates a typed host.</span></span>

## <a name="usage"></a><span data-ttu-id="fb8ff-105">Использование</span><span class="sxs-lookup"><span data-stu-id="fb8ff-105">Usage</span></span>

``` syntax
<hostBuilderDeclaration>
  child elements
</hostBuilderDeclaration>
```

## <a name="attributes"></a><span data-ttu-id="fb8ff-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="fb8ff-106">Attributes</span></span>

<span data-ttu-id="fb8ff-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fb8ff-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="fb8ff-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="fb8ff-108">Child elements</span></span>



| <span data-ttu-id="fb8ff-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="fb8ff-109">Element</span></span>                                   | <span data-ttu-id="fb8ff-110">Описание</span><span class="sxs-lookup"><span data-stu-id="fb8ff-110">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb8ff-111">**интерфейс**</span><span class="sxs-lookup"><span data-stu-id="fb8ff-111">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="fb8ff-112">Имя интерфейса службы, включаемого в узел.</span><span class="sxs-lookup"><span data-stu-id="fb8ff-112">The name of service interface to be included for host.</span></span> <span data-ttu-id="fb8ff-113">Значение этого элемента должно соответствовать значению дочернего элемента [**Interface**](interface.md) в [**hostedService**](hostedservice.md).</span><span class="sxs-lookup"><span data-stu-id="fb8ff-113">The value of this element must match the value of the [**interface**](interface.md) child element of [**hostedService**](hostedservice.md).</span></span> <br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="fb8ff-114">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="fb8ff-114">Child element sequence</span></span>

``` syntax
interface+
```

## <a name="parent-elements"></a><span data-ttu-id="fb8ff-115">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="fb8ff-115">Parent elements</span></span>



| <span data-ttu-id="fb8ff-116">Элемент</span><span class="sxs-lookup"><span data-stu-id="fb8ff-116">Element</span></span>                         | <span data-ttu-id="fb8ff-117">Описание</span><span class="sxs-lookup"><span data-stu-id="fb8ff-117">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="fb8ff-118">**File**</span><span class="sxs-lookup"><span data-stu-id="fb8ff-118">**file**</span></span>](file.md)<br/> | <span data-ttu-id="fb8ff-119">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="fb8ff-119">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="fb8ff-120">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="fb8ff-120">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="fb8ff-121">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="fb8ff-121">Minimum supported system</span></span><br/> | <span data-ttu-id="fb8ff-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb8ff-122">Windows Vista</span></span> |
| <span data-ttu-id="fb8ff-123">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="fb8ff-123">Can be empty</span></span>                        | <span data-ttu-id="fb8ff-124">Нет</span><span class="sxs-lookup"><span data-stu-id="fb8ff-124">No</span></span>            |



 

 




