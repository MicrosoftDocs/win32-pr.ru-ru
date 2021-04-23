---
description: Создает константы C для таблиц схемы XML для типов сообщений.
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: Мессажетипедефинитионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f86043cc28b527778c91772ad731d3a271921f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263906"
---
# <a name="messagetypedefinitions-element"></a><span data-ttu-id="1d367-103">Мессажетипедефинитионс, элемент</span><span class="sxs-lookup"><span data-stu-id="1d367-103">messageTypeDefinitions element</span></span>

<span data-ttu-id="1d367-104">Создает константы C для таблиц схемы XML для типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="1d367-104">Generates C constants for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="1d367-105">Использование</span><span class="sxs-lookup"><span data-stu-id="1d367-105">Usage</span></span>

``` syntax
<messageTypeDefinitions>
  child elements
</messageTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="1d367-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1d367-106">Attributes</span></span>

<span data-ttu-id="1d367-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="1d367-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="1d367-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1d367-108">Child elements</span></span>



| <span data-ttu-id="1d367-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="1d367-109">Element</span></span>                                   | <span data-ttu-id="1d367-110">Описание</span><span class="sxs-lookup"><span data-stu-id="1d367-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="1d367-111">**операцию**</span><span class="sxs-lookup"><span data-stu-id="1d367-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="1d367-112">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="1d367-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="1d367-113">**Порта**</span><span class="sxs-lookup"><span data-stu-id="1d367-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="1d367-114">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="1d367-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="1d367-115">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="1d367-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="1d367-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="1d367-116">Parent elements</span></span>



| <span data-ttu-id="1d367-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="1d367-117">Element</span></span>                         | <span data-ttu-id="1d367-118">Описание</span><span class="sxs-lookup"><span data-stu-id="1d367-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="1d367-119">**File**</span><span class="sxs-lookup"><span data-stu-id="1d367-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="1d367-120">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="1d367-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="1d367-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d367-121">Remarks</span></span>

<span data-ttu-id="1d367-122">Этот элемент обычно используется в исходных файлах на языке C для предоставления таблиц схемы, объявленных с помощью [**мессажетипедекларатионс**](messagetypedeclarations.md).</span><span class="sxs-lookup"><span data-stu-id="1d367-122">This element is generally used in C source files to provide the schema tables declared by [**messageTypeDeclarations**](messagetypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="1d367-123">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1d367-123">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="1d367-124">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="1d367-124">Minimum supported system</span></span><br/> | <span data-ttu-id="1d367-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d367-125">Windows Vista</span></span> |
| <span data-ttu-id="1d367-126">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="1d367-126">Can be empty</span></span>                        | <span data-ttu-id="1d367-127">Да</span><span class="sxs-lookup"><span data-stu-id="1d367-127">Yes</span></span>           |



 

 




