---
description: Определяет службу, размещаемую в функции конструктора узла.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: элемент hostedService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfcf2f4c67cadf90279221fd5bdfd518e285e844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898758"
---
# <a name="hostedservice-element"></a><span data-ttu-id="e95dd-103">элемент hostedService</span><span class="sxs-lookup"><span data-stu-id="e95dd-103">hostedService element</span></span>

<span data-ttu-id="e95dd-104">Определяет службу, размещаемую в функции конструктора узла.</span><span class="sxs-lookup"><span data-stu-id="e95dd-104">Defines a service to be hosted in a host builder function.</span></span>

## <a name="usage"></a><span data-ttu-id="e95dd-105">Использование</span><span class="sxs-lookup"><span data-stu-id="e95dd-105">Usage</span></span>

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a><span data-ttu-id="e95dd-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e95dd-106">Attributes</span></span>

<span data-ttu-id="e95dd-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="e95dd-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e95dd-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e95dd-108">Child elements</span></span>



| <span data-ttu-id="e95dd-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="e95dd-109">Element</span></span>                                     | <span data-ttu-id="e95dd-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e95dd-110">Description</span></span>                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e95dd-111">**Обеспечения**</span><span class="sxs-lookup"><span data-stu-id="e95dd-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="e95dd-112">Указывает имя, используемое для типа порта в созданном коде.</span><span class="sxs-lookup"><span data-stu-id="e95dd-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="e95dd-113">По умолчанию имя кода создается на основе полного имени типа порта.</span><span class="sxs-lookup"><span data-stu-id="e95dd-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="e95dd-114">**Порта**</span><span class="sxs-lookup"><span data-stu-id="e95dd-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="e95dd-115">Тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="e95dd-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                                       |
| [<span data-ttu-id="e95dd-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="e95dd-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="e95dd-117">Имя класса, создаваемого из функции построителя.</span><span class="sxs-lookup"><span data-stu-id="e95dd-117">Class name to generate from builder function.</span></span><br/> <br/>                                                                                                      |
| [<span data-ttu-id="e95dd-118">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="e95dd-118">**ServiceID**</span></span>](serviceid.md)<br/>   | <span data-ttu-id="e95dd-119">URI, представляющий идентификатор службы.</span><span class="sxs-lookup"><span data-stu-id="e95dd-119">A URI that represents the service identifier.</span></span><br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="e95dd-120">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="e95dd-120">Child element sequence</span></span>

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a><span data-ttu-id="e95dd-121">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e95dd-121">Parent elements</span></span>



| <span data-ttu-id="e95dd-122">Элемент</span><span class="sxs-lookup"><span data-stu-id="e95dd-122">Element</span></span>                         | <span data-ttu-id="e95dd-123">Описание</span><span class="sxs-lookup"><span data-stu-id="e95dd-123">Description</span></span>                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="e95dd-124">**File**</span><span class="sxs-lookup"><span data-stu-id="e95dd-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="e95dd-125">Спецификация выходного файла для генератора кода.</span><span class="sxs-lookup"><span data-stu-id="e95dd-125">The output file specification for the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="e95dd-126">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e95dd-126">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="e95dd-127">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="e95dd-127">Minimum supported system</span></span><br/> | <span data-ttu-id="e95dd-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e95dd-128">Windows Vista</span></span> |
| <span data-ttu-id="e95dd-129">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="e95dd-129">Can be empty</span></span>                        | <span data-ttu-id="e95dd-130">Нет</span><span class="sxs-lookup"><span data-stu-id="e95dd-130">No</span></span>            |



 

 




