---
description: Создает объявления констант C для таблиц схемы XML для типов сообщений.
ms.assetid: 17556708-9350-444f-84a3-d982270b31d1
title: Мессажетипедекларатионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696cd6d30e6a791f68c152e0d0c5d0b1a7300769
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998731"
---
# <a name="messagetypedeclarations-element"></a><span data-ttu-id="18448-103">Мессажетипедекларатионс, элемент</span><span class="sxs-lookup"><span data-stu-id="18448-103">messageTypeDeclarations element</span></span>

<span data-ttu-id="18448-104">Создает объявления констант C для таблиц схемы XML для типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="18448-104">Generates C constant declarations for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="18448-105">Использование</span><span class="sxs-lookup"><span data-stu-id="18448-105">Usage</span></span>

``` syntax
<messageTypeDeclarations>
  child elements
</messageTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="18448-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="18448-106">Attributes</span></span>

<span data-ttu-id="18448-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="18448-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="18448-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="18448-108">Child elements</span></span>



| <span data-ttu-id="18448-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="18448-109">Element</span></span>                                   | <span data-ttu-id="18448-110">Описание</span><span class="sxs-lookup"><span data-stu-id="18448-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="18448-111">**operation**</span><span class="sxs-lookup"><span data-stu-id="18448-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="18448-112">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="18448-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="18448-113">**Порта**</span><span class="sxs-lookup"><span data-stu-id="18448-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="18448-114">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="18448-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="18448-115">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="18448-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="18448-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="18448-116">Parent elements</span></span>



| <span data-ttu-id="18448-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="18448-117">Element</span></span>                         | <span data-ttu-id="18448-118">Описание</span><span class="sxs-lookup"><span data-stu-id="18448-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="18448-119">**File**</span><span class="sxs-lookup"><span data-stu-id="18448-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="18448-120">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="18448-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="18448-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="18448-121">Remarks</span></span>

<span data-ttu-id="18448-122">На таблицы схемы ссылаются определения типов портов.</span><span class="sxs-lookup"><span data-stu-id="18448-122">Schema tables are referenced by port type definitions.</span></span> <span data-ttu-id="18448-123">Таким образом, этот элемент обычно используется непосредственно перед элементами [**порттипедефинитионс**](porttypedefinitions.md) .</span><span class="sxs-lookup"><span data-stu-id="18448-123">This element is therefore generally used just prior to [**portTypeDefinitions**](porttypedefinitions.md) elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="18448-124">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="18448-124">Element information</span></span>



| <span data-ttu-id="18448-125">Метка</span><span class="sxs-lookup"><span data-stu-id="18448-125">Label</span></span> | <span data-ttu-id="18448-126">Значение</span><span class="sxs-lookup"><span data-stu-id="18448-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="18448-127">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="18448-127">Minimum supported system</span></span><br/> | <span data-ttu-id="18448-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18448-128">Windows Vista</span></span> |
| <span data-ttu-id="18448-129">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="18448-129">Can be empty</span></span>                        | <span data-ttu-id="18448-130">Да</span><span class="sxs-lookup"><span data-stu-id="18448-130">Yes</span></span>           |



 

 




