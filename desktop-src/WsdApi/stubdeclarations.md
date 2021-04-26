---
description: Создает объявления для функций-заглушек для операций с типом порта.
ms.assetid: d43baeff-c941-4ce9-a6ae-8aa61ef44048
title: Стубдекларатионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1543883b4d41e7571cd4a4725e2aeab181530d30
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996411"
---
# <a name="stubdeclarations-element"></a><span data-ttu-id="30f7f-103">Стубдекларатионс, элемент</span><span class="sxs-lookup"><span data-stu-id="30f7f-103">stubDeclarations element</span></span>

<span data-ttu-id="30f7f-104">Создает объявления для функций-заглушек для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="30f7f-104">Generates declarations for stub functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="30f7f-105">Использование</span><span class="sxs-lookup"><span data-stu-id="30f7f-105">Usage</span></span>

``` syntax
<stubDeclarations>
  child elements
</stubDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="30f7f-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="30f7f-106">Attributes</span></span>

<span data-ttu-id="30f7f-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="30f7f-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="30f7f-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="30f7f-108">Child elements</span></span>



| <span data-ttu-id="30f7f-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="30f7f-109">Element</span></span>                                   | <span data-ttu-id="30f7f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="30f7f-110">Description</span></span>                                                                                      |
|-------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30f7f-111">**событиях**</span><span class="sxs-lookup"><span data-stu-id="30f7f-111">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="30f7f-112">Указывает, включаются ли в создаваемые функции связанные события.</span><span class="sxs-lookup"><span data-stu-id="30f7f-112">Specifies whether related events are included in the generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="30f7f-113">**операцию**</span><span class="sxs-lookup"><span data-stu-id="30f7f-113">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="30f7f-114">Указывает операцию, для которой создается код.</span><span class="sxs-lookup"><span data-stu-id="30f7f-114">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                 |
| [<span data-ttu-id="30f7f-115">**Порта**</span><span class="sxs-lookup"><span data-stu-id="30f7f-115">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="30f7f-116">Указывает тип порта, для которого создается код.</span><span class="sxs-lookup"><span data-stu-id="30f7f-116">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                |



### <a name="child-element-sequence"></a><span data-ttu-id="30f7f-117">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="30f7f-117">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?
)
```

## <a name="parent-elements"></a><span data-ttu-id="30f7f-118">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="30f7f-118">Parent elements</span></span>



| <span data-ttu-id="30f7f-119">Элемент</span><span class="sxs-lookup"><span data-stu-id="30f7f-119">Element</span></span>                         | <span data-ttu-id="30f7f-120">Описание</span><span class="sxs-lookup"><span data-stu-id="30f7f-120">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="30f7f-121">**File**</span><span class="sxs-lookup"><span data-stu-id="30f7f-121">**file**</span></span>](file.md)<br/> | <span data-ttu-id="30f7f-122">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="30f7f-122">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="30f7f-123">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="30f7f-123">Element information</span></span>



| <span data-ttu-id="30f7f-124">Метка</span><span class="sxs-lookup"><span data-stu-id="30f7f-124">Label</span></span> | <span data-ttu-id="30f7f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="30f7f-125">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="30f7f-126">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="30f7f-126">Minimum supported system</span></span><br/> | <span data-ttu-id="30f7f-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30f7f-127">Windows Vista</span></span> |
| <span data-ttu-id="30f7f-128">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="30f7f-128">Can be empty</span></span>                        | <span data-ttu-id="30f7f-129">Да</span><span class="sxs-lookup"><span data-stu-id="30f7f-129">Yes</span></span>           |



 

 




