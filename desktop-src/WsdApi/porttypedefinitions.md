---
description: Создает константы C для типов портов.
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: Порттипедефинитионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff073eb7b0f9cbc4b0b6df87c8f9fc84d4f62882
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996551"
---
# <a name="porttypedefinitions-element"></a><span data-ttu-id="1deb9-103">Порттипедефинитионс, элемент</span><span class="sxs-lookup"><span data-stu-id="1deb9-103">portTypeDefinitions element</span></span>

<span data-ttu-id="1deb9-104">Создает константы C для типов портов.</span><span class="sxs-lookup"><span data-stu-id="1deb9-104">Generates C constants for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="1deb9-105">Использование</span><span class="sxs-lookup"><span data-stu-id="1deb9-105">Usage</span></span>

``` syntax
<portTypeDefinitions>
  child elements
</portTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="1deb9-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1deb9-106">Attributes</span></span>

<span data-ttu-id="1deb9-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="1deb9-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="1deb9-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1deb9-108">Child elements</span></span>



| <span data-ttu-id="1deb9-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="1deb9-109">Element</span></span>                                                   | <span data-ttu-id="1deb9-110">Описание</span><span class="sxs-lookup"><span data-stu-id="1deb9-110">Description</span></span>                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1deb9-111">**Обеспечения**</span><span class="sxs-lookup"><span data-stu-id="1deb9-111">**codeName**</span></span>](codename.md)<br/>                   | <span data-ttu-id="1deb9-112">Указывает имя, используемое для типа порта в созданном коде.</span><span class="sxs-lookup"><span data-stu-id="1deb9-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="1deb9-113">По умолчанию имя кода создается на основе полного имени типа порта.</span><span class="sxs-lookup"><span data-stu-id="1deb9-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/>         |
| [<span data-ttu-id="1deb9-114">**евентстубфунктион**</span><span class="sxs-lookup"><span data-stu-id="1deb9-114">**eventStubFunction**</span></span>](eventstubfunction.md)<br/> | <span data-ttu-id="1deb9-115">Указывает, должны ли ссылки на функции-заглушки включаться в структуры операций в определениях типов портов для операций уведомления.</span><span class="sxs-lookup"><span data-stu-id="1deb9-115">Specifies whether stub function references should be included in the operation structures in the port type definitions for notification operations.</span></span><br/> <br/>        |
| [<span data-ttu-id="1deb9-116">**операцию**</span><span class="sxs-lookup"><span data-stu-id="1deb9-116">**operation**</span></span>](operation.md)<br/>                 | <span data-ttu-id="1deb9-117">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="1deb9-117">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                                  |
| [<span data-ttu-id="1deb9-118">**Порта**</span><span class="sxs-lookup"><span data-stu-id="1deb9-118">**portType**</span></span>](porttype.md)<br/>                   | <span data-ttu-id="1deb9-119">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="1deb9-119">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                                 |
| [<span data-ttu-id="1deb9-120">**стубфунктион**</span><span class="sxs-lookup"><span data-stu-id="1deb9-120">**stubFunction**</span></span>](stubfunction.md)<br/>           | <span data-ttu-id="1deb9-121">Указывает, должны ли ссылки на функции-заглушки включаться в структуры операций в определениях типов портов для односторонних и двусторонних операций.</span><span class="sxs-lookup"><span data-stu-id="1deb9-121">Specifies whether stub function references should be included in the operation structures in the port type definitions for one-way and two-way operations.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="1deb9-122">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="1deb9-122">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  stubFunction?, 
  eventStubFunction?, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="1deb9-123">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="1deb9-123">Parent elements</span></span>



| <span data-ttu-id="1deb9-124">Элемент</span><span class="sxs-lookup"><span data-stu-id="1deb9-124">Element</span></span>                         | <span data-ttu-id="1deb9-125">Описание</span><span class="sxs-lookup"><span data-stu-id="1deb9-125">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="1deb9-126">**File**</span><span class="sxs-lookup"><span data-stu-id="1deb9-126">**file**</span></span>](file.md)<br/> | <span data-ttu-id="1deb9-127">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="1deb9-127">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="1deb9-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="1deb9-128">Remarks</span></span>

<span data-ttu-id="1deb9-129">Этот элемент обычно используется в исходных файлах на языке C для предоставления констант типа порта, объявленных с помощью [**порттипедекларатионс**](porttypedeclarations.md).</span><span class="sxs-lookup"><span data-stu-id="1deb9-129">This element is generally used in C source files to provide the port type constants declared by [**portTypeDeclarations**](porttypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="1deb9-130">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1deb9-130">Element information</span></span>



| <span data-ttu-id="1deb9-131">Метка</span><span class="sxs-lookup"><span data-stu-id="1deb9-131">Label</span></span> | <span data-ttu-id="1deb9-132">Значение</span><span class="sxs-lookup"><span data-stu-id="1deb9-132">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="1deb9-133">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="1deb9-133">Minimum supported system</span></span><br/> | <span data-ttu-id="1deb9-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1deb9-134">Windows Vista</span></span> |
| <span data-ttu-id="1deb9-135">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="1deb9-135">Can be empty</span></span>                        | <span data-ttu-id="1deb9-136">Да</span><span class="sxs-lookup"><span data-stu-id="1deb9-136">Yes</span></span>           |



 

 




