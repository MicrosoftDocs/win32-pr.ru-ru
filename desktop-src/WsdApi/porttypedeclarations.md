---
description: Создает объявления констант C для типов портов.
ms.assetid: 05a06206-3cc4-428d-b9f2-b7945e63922c
title: Порттипедекларатионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e19780d4a48c95cd47872b0428b368e6b7e99887
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996561"
---
# <a name="porttypedeclarations-element"></a><span data-ttu-id="4a8ac-103">Порттипедекларатионс, элемент</span><span class="sxs-lookup"><span data-stu-id="4a8ac-103">portTypeDeclarations element</span></span>

<span data-ttu-id="4a8ac-104">Создает объявления констант C для типов портов.</span><span class="sxs-lookup"><span data-stu-id="4a8ac-104">Generates C constant declarations for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="4a8ac-105">Использование</span><span class="sxs-lookup"><span data-stu-id="4a8ac-105">Usage</span></span>

``` syntax
<portTypeDeclarations>
  child elements
</portTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="4a8ac-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4a8ac-106">Attributes</span></span>

<span data-ttu-id="4a8ac-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="4a8ac-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4a8ac-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4a8ac-108">Child elements</span></span>



| <span data-ttu-id="4a8ac-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="4a8ac-109">Element</span></span>                                   | <span data-ttu-id="4a8ac-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4a8ac-110">Description</span></span>                                                                                                                                                               |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a8ac-111">**Обеспечения**</span><span class="sxs-lookup"><span data-stu-id="4a8ac-111">**codeName**</span></span>](codename.md)<br/>   | <span data-ttu-id="4a8ac-112">Указывает имя, используемое для типа порта в созданном коде.</span><span class="sxs-lookup"><span data-stu-id="4a8ac-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="4a8ac-113">По умолчанию имя кода создается на основе полного имени типа порта.</span><span class="sxs-lookup"><span data-stu-id="4a8ac-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="4a8ac-114">**операцию**</span><span class="sxs-lookup"><span data-stu-id="4a8ac-114">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="4a8ac-115">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="4a8ac-115">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                          |
| [<span data-ttu-id="4a8ac-116">**Порта**</span><span class="sxs-lookup"><span data-stu-id="4a8ac-116">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="4a8ac-117">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="4a8ac-117">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                         |



### <a name="child-element-sequence"></a><span data-ttu-id="4a8ac-118">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="4a8ac-118">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="4a8ac-119">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="4a8ac-119">Parent elements</span></span>



| <span data-ttu-id="4a8ac-120">Элемент</span><span class="sxs-lookup"><span data-stu-id="4a8ac-120">Element</span></span>                         | <span data-ttu-id="4a8ac-121">Описание</span><span class="sxs-lookup"><span data-stu-id="4a8ac-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="4a8ac-122">**File**</span><span class="sxs-lookup"><span data-stu-id="4a8ac-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="4a8ac-123">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="4a8ac-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4a8ac-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a8ac-124">Remarks</span></span>

<span data-ttu-id="4a8ac-125">На объявления типа порта ссылается приложение и большая часть созданного кода.</span><span class="sxs-lookup"><span data-stu-id="4a8ac-125">Port type declarations are referenced by the application and much of the generated code.</span></span> <span data-ttu-id="4a8ac-126">Этот элемент используется для создания включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="4a8ac-126">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="4a8ac-127">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4a8ac-127">Element information</span></span>



| <span data-ttu-id="4a8ac-128">Метка</span><span class="sxs-lookup"><span data-stu-id="4a8ac-128">Label</span></span> | <span data-ttu-id="4a8ac-129">Значение</span><span class="sxs-lookup"><span data-stu-id="4a8ac-129">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="4a8ac-130">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="4a8ac-130">Minimum supported system</span></span><br/> | <span data-ttu-id="4a8ac-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a8ac-131">Windows Vista</span></span> |
| <span data-ttu-id="4a8ac-132">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="4a8ac-132">Can be empty</span></span>                        | <span data-ttu-id="4a8ac-133">Да</span><span class="sxs-lookup"><span data-stu-id="4a8ac-133">Yes</span></span>           |



 

 




