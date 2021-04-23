---
description: Создает определения структуры C для известных типов.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: Структдефинитионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e33ca9ac9ce3f9e868646c0bfff260238c30e572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702461"
---
# <a name="structdefinitions-element"></a><span data-ttu-id="0b981-103">Структдефинитионс, элемент</span><span class="sxs-lookup"><span data-stu-id="0b981-103">structDefinitions element</span></span>

<span data-ttu-id="0b981-104">Создает определения структуры C для известных типов.</span><span class="sxs-lookup"><span data-stu-id="0b981-104">Generates C structure definitions for known types.</span></span>

## <a name="usage"></a><span data-ttu-id="0b981-105">Использование</span><span class="sxs-lookup"><span data-stu-id="0b981-105">Usage</span></span>

``` syntax
<structDefinitions/>
```

## <a name="attributes"></a><span data-ttu-id="0b981-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0b981-106">Attributes</span></span>

<span data-ttu-id="0b981-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="0b981-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0b981-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0b981-108">Child elements</span></span>

<span data-ttu-id="0b981-109">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="0b981-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="0b981-110">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="0b981-110">Parent elements</span></span>



| <span data-ttu-id="0b981-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="0b981-111">Element</span></span>                         | <span data-ttu-id="0b981-112">Описание</span><span class="sxs-lookup"><span data-stu-id="0b981-112">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="0b981-113">**File**</span><span class="sxs-lookup"><span data-stu-id="0b981-113">**file**</span></span>](file.md)<br/> | <span data-ttu-id="0b981-114">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="0b981-114">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0b981-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b981-115">Remarks</span></span>

<span data-ttu-id="0b981-116">На структуры известных типов ссылается большая часть созданного кода и кода приложения.</span><span class="sxs-lookup"><span data-stu-id="0b981-116">Structures for known types are referenced by much of the generated code and by application code.</span></span> <span data-ttu-id="0b981-117">Этот элемент используется для создания включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="0b981-117">This element is used to generate include files.</span></span> <span data-ttu-id="0b981-118">Этот элемент должен находиться после элемента [**структдекларатионс**](structdeclarations.md) , чтобы ссылки между структурами были правильно обработаны.</span><span class="sxs-lookup"><span data-stu-id="0b981-118">This element should occur after a [**structDeclarations**](structdeclarations.md) element so that references between structures are handled properly.</span></span>

## <a name="element-information"></a><span data-ttu-id="0b981-119">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0b981-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="0b981-120">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="0b981-120">Minimum supported system</span></span><br/> | <span data-ttu-id="0b981-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b981-121">Windows Vista</span></span> |
| <span data-ttu-id="0b981-122">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="0b981-122">Can be empty</span></span>                        | <span data-ttu-id="0b981-123">Да</span><span class="sxs-lookup"><span data-stu-id="0b981-123">Yes</span></span>           |



 

 




