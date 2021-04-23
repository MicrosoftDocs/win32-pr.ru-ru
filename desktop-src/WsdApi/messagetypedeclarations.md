---
description: Создает объявления констант C для таблиц схемы XML для типов сообщений.
ms.assetid: 17556708-9350-444f-84a3-d982270b31d1
title: Мессажетипедекларатионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 700511d3c0a83badcb15b0e07491a14ade53f454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999193"
---
# <a name="messagetypedeclarations-element"></a><span data-ttu-id="f21f1-103">Мессажетипедекларатионс, элемент</span><span class="sxs-lookup"><span data-stu-id="f21f1-103">messageTypeDeclarations element</span></span>

<span data-ttu-id="f21f1-104">Создает объявления констант C для таблиц схемы XML для типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="f21f1-104">Generates C constant declarations for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="f21f1-105">Использование</span><span class="sxs-lookup"><span data-stu-id="f21f1-105">Usage</span></span>

``` syntax
<messageTypeDeclarations>
  child elements
</messageTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="f21f1-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f21f1-106">Attributes</span></span>

<span data-ttu-id="f21f1-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="f21f1-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f21f1-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f21f1-108">Child elements</span></span>



| <span data-ttu-id="f21f1-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="f21f1-109">Element</span></span>                                   | <span data-ttu-id="f21f1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f21f1-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="f21f1-111">**операцию**</span><span class="sxs-lookup"><span data-stu-id="f21f1-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="f21f1-112">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="f21f1-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="f21f1-113">**Порта**</span><span class="sxs-lookup"><span data-stu-id="f21f1-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="f21f1-114">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="f21f1-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="f21f1-115">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="f21f1-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="f21f1-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f21f1-116">Parent elements</span></span>



| <span data-ttu-id="f21f1-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="f21f1-117">Element</span></span>                         | <span data-ttu-id="f21f1-118">Описание</span><span class="sxs-lookup"><span data-stu-id="f21f1-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="f21f1-119">**File**</span><span class="sxs-lookup"><span data-stu-id="f21f1-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="f21f1-120">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="f21f1-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f21f1-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f21f1-121">Remarks</span></span>

<span data-ttu-id="f21f1-122">На таблицы схемы ссылаются определения типов портов.</span><span class="sxs-lookup"><span data-stu-id="f21f1-122">Schema tables are referenced by port type definitions.</span></span> <span data-ttu-id="f21f1-123">Таким образом, этот элемент обычно используется непосредственно перед элементами [**порттипедефинитионс**](porttypedefinitions.md) .</span><span class="sxs-lookup"><span data-stu-id="f21f1-123">This element is therefore generally used just prior to [**portTypeDefinitions**](porttypedefinitions.md) elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="f21f1-124">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f21f1-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="f21f1-125">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="f21f1-125">Minimum supported system</span></span><br/> | <span data-ttu-id="f21f1-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f21f1-126">Windows Vista</span></span> |
| <span data-ttu-id="f21f1-127">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="f21f1-127">Can be empty</span></span>                        | <span data-ttu-id="f21f1-128">Да</span><span class="sxs-lookup"><span data-stu-id="f21f1-128">Yes</span></span>           |



 

 




