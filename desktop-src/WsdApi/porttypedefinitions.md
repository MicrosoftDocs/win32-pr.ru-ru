---
description: Создает константы C для типов портов.
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: Порттипедефинитионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60f55408df938ed95af14c69b2676473ac1bda71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264642"
---
# <a name="porttypedefinitions-element"></a><span data-ttu-id="1ec6e-103">Порттипедефинитионс, элемент</span><span class="sxs-lookup"><span data-stu-id="1ec6e-103">portTypeDefinitions element</span></span>

<span data-ttu-id="1ec6e-104">Создает константы C для типов портов.</span><span class="sxs-lookup"><span data-stu-id="1ec6e-104">Generates C constants for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="1ec6e-105">Использование</span><span class="sxs-lookup"><span data-stu-id="1ec6e-105">Usage</span></span>

``` syntax
<portTypeDefinitions>
  child elements
</portTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="1ec6e-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1ec6e-106">Attributes</span></span>

<span data-ttu-id="1ec6e-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="1ec6e-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="1ec6e-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1ec6e-108">Child elements</span></span>



| <span data-ttu-id="1ec6e-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="1ec6e-109">Element</span></span>                                                   | <span data-ttu-id="1ec6e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="1ec6e-110">Description</span></span>                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ec6e-111">**Обеспечения**</span><span class="sxs-lookup"><span data-stu-id="1ec6e-111">**codeName**</span></span>](codename.md)<br/>                   | <span data-ttu-id="1ec6e-112">Указывает имя, используемое для типа порта в созданном коде.</span><span class="sxs-lookup"><span data-stu-id="1ec6e-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="1ec6e-113">По умолчанию имя кода создается на основе полного имени типа порта.</span><span class="sxs-lookup"><span data-stu-id="1ec6e-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/>         |
| [<span data-ttu-id="1ec6e-114">**евентстубфунктион**</span><span class="sxs-lookup"><span data-stu-id="1ec6e-114">**eventStubFunction**</span></span>](eventstubfunction.md)<br/> | <span data-ttu-id="1ec6e-115">Указывает, должны ли ссылки на функции-заглушки включаться в структуры операций в определениях типов портов для операций уведомления.</span><span class="sxs-lookup"><span data-stu-id="1ec6e-115">Specifies whether stub function references should be included in the operation structures in the port type definitions for notification operations.</span></span><br/> <br/>        |
| [<span data-ttu-id="1ec6e-116">**операцию**</span><span class="sxs-lookup"><span data-stu-id="1ec6e-116">**operation**</span></span>](operation.md)<br/>                 | <span data-ttu-id="1ec6e-117">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="1ec6e-117">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                                  |
| [<span data-ttu-id="1ec6e-118">**Порта**</span><span class="sxs-lookup"><span data-stu-id="1ec6e-118">**portType**</span></span>](porttype.md)<br/>                   | <span data-ttu-id="1ec6e-119">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="1ec6e-119">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                                 |
| [<span data-ttu-id="1ec6e-120">**стубфунктион**</span><span class="sxs-lookup"><span data-stu-id="1ec6e-120">**stubFunction**</span></span>](stubfunction.md)<br/>           | <span data-ttu-id="1ec6e-121">Указывает, должны ли ссылки на функции-заглушки включаться в структуры операций в определениях типов портов для односторонних и двусторонних операций.</span><span class="sxs-lookup"><span data-stu-id="1ec6e-121">Specifies whether stub function references should be included in the operation structures in the port type definitions for one-way and two-way operations.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="1ec6e-122">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="1ec6e-122">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  stubFunction?, 
  eventStubFunction?, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="1ec6e-123">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="1ec6e-123">Parent elements</span></span>



| <span data-ttu-id="1ec6e-124">Элемент</span><span class="sxs-lookup"><span data-stu-id="1ec6e-124">Element</span></span>                         | <span data-ttu-id="1ec6e-125">Описание</span><span class="sxs-lookup"><span data-stu-id="1ec6e-125">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="1ec6e-126">**File**</span><span class="sxs-lookup"><span data-stu-id="1ec6e-126">**file**</span></span>](file.md)<br/> | <span data-ttu-id="1ec6e-127">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="1ec6e-127">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="1ec6e-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ec6e-128">Remarks</span></span>

<span data-ttu-id="1ec6e-129">Этот элемент обычно используется в исходных файлах на языке C для предоставления констант типа порта, объявленных с помощью [**порттипедекларатионс**](porttypedeclarations.md).</span><span class="sxs-lookup"><span data-stu-id="1ec6e-129">This element is generally used in C source files to provide the port type constants declared by [**portTypeDeclarations**](porttypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="1ec6e-130">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1ec6e-130">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="1ec6e-131">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="1ec6e-131">Minimum supported system</span></span><br/> | <span data-ttu-id="1ec6e-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1ec6e-132">Windows Vista</span></span> |
| <span data-ttu-id="1ec6e-133">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="1ec6e-133">Can be empty</span></span>                        | <span data-ttu-id="1ec6e-134">Да</span><span class="sxs-lookup"><span data-stu-id="1ec6e-134">Yes</span></span>           |



 

 




