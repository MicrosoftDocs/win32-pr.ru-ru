---
description: Создает объявления констант C для типов портов.
ms.assetid: 05a06206-3cc4-428d-b9f2-b7945e63922c
title: Порттипедекларатионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c4e202f1451d93b519bd59ea51f591c37a92957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702045"
---
# <a name="porttypedeclarations-element"></a><span data-ttu-id="82089-103">Порттипедекларатионс, элемент</span><span class="sxs-lookup"><span data-stu-id="82089-103">portTypeDeclarations element</span></span>

<span data-ttu-id="82089-104">Создает объявления констант C для типов портов.</span><span class="sxs-lookup"><span data-stu-id="82089-104">Generates C constant declarations for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="82089-105">Использование</span><span class="sxs-lookup"><span data-stu-id="82089-105">Usage</span></span>

``` syntax
<portTypeDeclarations>
  child elements
</portTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="82089-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="82089-106">Attributes</span></span>

<span data-ttu-id="82089-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="82089-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="82089-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="82089-108">Child elements</span></span>



| <span data-ttu-id="82089-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="82089-109">Element</span></span>                                   | <span data-ttu-id="82089-110">Описание</span><span class="sxs-lookup"><span data-stu-id="82089-110">Description</span></span>                                                                                                                                                               |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82089-111">**Обеспечения**</span><span class="sxs-lookup"><span data-stu-id="82089-111">**codeName**</span></span>](codename.md)<br/>   | <span data-ttu-id="82089-112">Указывает имя, используемое для типа порта в созданном коде.</span><span class="sxs-lookup"><span data-stu-id="82089-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="82089-113">По умолчанию имя кода создается на основе полного имени типа порта.</span><span class="sxs-lookup"><span data-stu-id="82089-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="82089-114">**операцию**</span><span class="sxs-lookup"><span data-stu-id="82089-114">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="82089-115">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="82089-115">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                          |
| [<span data-ttu-id="82089-116">**Порта**</span><span class="sxs-lookup"><span data-stu-id="82089-116">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="82089-117">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="82089-117">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                         |



### <a name="child-element-sequence"></a><span data-ttu-id="82089-118">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="82089-118">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="82089-119">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="82089-119">Parent elements</span></span>



| <span data-ttu-id="82089-120">Элемент</span><span class="sxs-lookup"><span data-stu-id="82089-120">Element</span></span>                         | <span data-ttu-id="82089-121">Описание</span><span class="sxs-lookup"><span data-stu-id="82089-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="82089-122">**File**</span><span class="sxs-lookup"><span data-stu-id="82089-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="82089-123">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="82089-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="82089-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82089-124">Remarks</span></span>

<span data-ttu-id="82089-125">На объявления типа порта ссылается приложение и большая часть созданного кода.</span><span class="sxs-lookup"><span data-stu-id="82089-125">Port type declarations are referenced by the application and much of the generated code.</span></span> <span data-ttu-id="82089-126">Этот элемент используется для создания включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="82089-126">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="82089-127">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="82089-127">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="82089-128">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="82089-128">Minimum supported system</span></span><br/> | <span data-ttu-id="82089-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82089-129">Windows Vista</span></span> |
| <span data-ttu-id="82089-130">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="82089-130">Can be empty</span></span>                        | <span data-ttu-id="82089-131">Да</span><span class="sxs-lookup"><span data-stu-id="82089-131">Yes</span></span>           |



 

 




