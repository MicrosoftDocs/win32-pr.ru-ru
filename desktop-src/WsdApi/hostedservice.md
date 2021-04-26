---
description: Определяет службу, размещаемую в функции конструктора узла.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: элемент hostedService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96c9f6e010989f4844d93299bb34f1ab8893236
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994791"
---
# <a name="hostedservice-element"></a><span data-ttu-id="46f83-103">элемент hostedService</span><span class="sxs-lookup"><span data-stu-id="46f83-103">hostedService element</span></span>

<span data-ttu-id="46f83-104">Определяет службу, размещаемую в функции конструктора узла.</span><span class="sxs-lookup"><span data-stu-id="46f83-104">Defines a service to be hosted in a host builder function.</span></span>

## <a name="usage"></a><span data-ttu-id="46f83-105">Использование</span><span class="sxs-lookup"><span data-stu-id="46f83-105">Usage</span></span>

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a><span data-ttu-id="46f83-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="46f83-106">Attributes</span></span>

<span data-ttu-id="46f83-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="46f83-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="46f83-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="46f83-108">Child elements</span></span>



| <span data-ttu-id="46f83-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="46f83-109">Element</span></span>                                     | <span data-ttu-id="46f83-110">Описание</span><span class="sxs-lookup"><span data-stu-id="46f83-110">Description</span></span>                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46f83-111">**Обеспечения**</span><span class="sxs-lookup"><span data-stu-id="46f83-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="46f83-112">Указывает имя, используемое для типа порта в созданном коде.</span><span class="sxs-lookup"><span data-stu-id="46f83-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="46f83-113">По умолчанию имя кода создается на основе полного имени типа порта.</span><span class="sxs-lookup"><span data-stu-id="46f83-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="46f83-114">**Порта**</span><span class="sxs-lookup"><span data-stu-id="46f83-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="46f83-115">Тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="46f83-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                                       |
| [<span data-ttu-id="46f83-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="46f83-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="46f83-117">Имя класса, создаваемого из функции построителя.</span><span class="sxs-lookup"><span data-stu-id="46f83-117">Class name to generate from builder function.</span></span><br/> <br/>                                                                                                      |
| [<span data-ttu-id="46f83-118">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="46f83-118">**ServiceID**</span></span>](serviceid.md)<br/>   | <span data-ttu-id="46f83-119">URI, представляющий идентификатор службы.</span><span class="sxs-lookup"><span data-stu-id="46f83-119">A URI that represents the service identifier.</span></span><br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="46f83-120">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="46f83-120">Child element sequence</span></span>

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a><span data-ttu-id="46f83-121">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="46f83-121">Parent elements</span></span>



| <span data-ttu-id="46f83-122">Элемент</span><span class="sxs-lookup"><span data-stu-id="46f83-122">Element</span></span>                         | <span data-ttu-id="46f83-123">Описание</span><span class="sxs-lookup"><span data-stu-id="46f83-123">Description</span></span>                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="46f83-124">**File**</span><span class="sxs-lookup"><span data-stu-id="46f83-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="46f83-125">Спецификация выходного файла для генератора кода.</span><span class="sxs-lookup"><span data-stu-id="46f83-125">The output file specification for the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="46f83-126">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="46f83-126">Element information</span></span>



| <span data-ttu-id="46f83-127">Метка</span><span class="sxs-lookup"><span data-stu-id="46f83-127">Label</span></span> | <span data-ttu-id="46f83-128">Значение</span><span class="sxs-lookup"><span data-stu-id="46f83-128">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="46f83-129">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="46f83-129">Minimum supported system</span></span><br/> | <span data-ttu-id="46f83-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46f83-130">Windows Vista</span></span> |
| <span data-ttu-id="46f83-131">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="46f83-131">Can be empty</span></span>                        | <span data-ttu-id="46f83-132">нет</span><span class="sxs-lookup"><span data-stu-id="46f83-132">No</span></span>            |



 

 




