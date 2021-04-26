---
description: Создает константы C для таблиц схемы XML для типов сообщений.
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: Мессажетипедефинитионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f1b6563254a93122960b4a990fe0bd18ab1453
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998711"
---
# <a name="messagetypedefinitions-element"></a><span data-ttu-id="ed7a9-103">Мессажетипедефинитионс, элемент</span><span class="sxs-lookup"><span data-stu-id="ed7a9-103">messageTypeDefinitions element</span></span>

<span data-ttu-id="ed7a9-104">Создает константы C для таблиц схемы XML для типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="ed7a9-104">Generates C constants for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="ed7a9-105">Использование</span><span class="sxs-lookup"><span data-stu-id="ed7a9-105">Usage</span></span>

``` syntax
<messageTypeDefinitions>
  child elements
</messageTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="ed7a9-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ed7a9-106">Attributes</span></span>

<span data-ttu-id="ed7a9-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="ed7a9-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ed7a9-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ed7a9-108">Child elements</span></span>



| <span data-ttu-id="ed7a9-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="ed7a9-109">Element</span></span>                                   | <span data-ttu-id="ed7a9-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ed7a9-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="ed7a9-111">**operation**</span><span class="sxs-lookup"><span data-stu-id="ed7a9-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="ed7a9-112">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="ed7a9-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="ed7a9-113">**Порта**</span><span class="sxs-lookup"><span data-stu-id="ed7a9-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="ed7a9-114">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="ed7a9-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="ed7a9-115">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="ed7a9-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="ed7a9-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ed7a9-116">Parent elements</span></span>



| <span data-ttu-id="ed7a9-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="ed7a9-117">Element</span></span>                         | <span data-ttu-id="ed7a9-118">Описание</span><span class="sxs-lookup"><span data-stu-id="ed7a9-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="ed7a9-119">**File**</span><span class="sxs-lookup"><span data-stu-id="ed7a9-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="ed7a9-120">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="ed7a9-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ed7a9-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="ed7a9-121">Remarks</span></span>

<span data-ttu-id="ed7a9-122">Этот элемент обычно используется в исходных файлах на языке C для предоставления таблиц схемы, объявленных с помощью [**мессажетипедекларатионс**](messagetypedeclarations.md).</span><span class="sxs-lookup"><span data-stu-id="ed7a9-122">This element is generally used in C source files to provide the schema tables declared by [**messageTypeDeclarations**](messagetypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="ed7a9-123">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ed7a9-123">Element information</span></span>



| <span data-ttu-id="ed7a9-124">Метка</span><span class="sxs-lookup"><span data-stu-id="ed7a9-124">Label</span></span> | <span data-ttu-id="ed7a9-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ed7a9-125">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="ed7a9-126">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="ed7a9-126">Minimum supported system</span></span><br/> | <span data-ttu-id="ed7a9-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed7a9-127">Windows Vista</span></span> |
| <span data-ttu-id="ed7a9-128">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="ed7a9-128">Can be empty</span></span>                        | <span data-ttu-id="ed7a9-129">Да</span><span class="sxs-lookup"><span data-stu-id="ed7a9-129">Yes</span></span>           |



 

 




