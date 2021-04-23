---
description: Определяет префикс, который будет использоваться в созданном коде для имен макросов в пространстве имен.
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: Макропрефикс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76c88dc48505e3344db1467463a9a99639edd881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711707"
---
# <a name="macroprefix-element"></a><span data-ttu-id="d8d46-103">Макропрефикс, элемент</span><span class="sxs-lookup"><span data-stu-id="d8d46-103">macroPrefix element</span></span>

<span data-ttu-id="d8d46-104">Определяет префикс, который будет использоваться в созданном коде для имен макросов в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="d8d46-104">Defines the prefix to be used in the generated code for names of macros in the namespace.</span></span>

## <a name="usage"></a><span data-ttu-id="d8d46-105">Использование</span><span class="sxs-lookup"><span data-stu-id="d8d46-105">Usage</span></span>

``` syntax
<macroPrefix/>
```

## <a name="attributes"></a><span data-ttu-id="d8d46-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d8d46-106">Attributes</span></span>

<span data-ttu-id="d8d46-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="d8d46-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d8d46-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d8d46-108">Child elements</span></span>

<span data-ttu-id="d8d46-109">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="d8d46-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="d8d46-110">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="d8d46-110">Parent elements</span></span>



| <span data-ttu-id="d8d46-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="d8d46-111">Element</span></span>                                   | <span data-ttu-id="d8d46-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d8d46-112">Description</span></span>                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="d8d46-113">**Имен**</span><span class="sxs-lookup"><span data-stu-id="d8d46-113">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="d8d46-114">Пространство имен, используемое для создания кода.</span><span class="sxs-lookup"><span data-stu-id="d8d46-114">A namespace to be used for code generation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="d8d46-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8d46-115">Remarks</span></span>

<span data-ttu-id="d8d46-116">Этот элемент переопределяет префикс URI по умолчанию, используемый для созданных макросов.</span><span class="sxs-lookup"><span data-stu-id="d8d46-116">This element overrides the default URI prefix used for generated macros.</span></span> <span data-ttu-id="d8d46-117">Например, если префиксом макроса является "AV \_ ", а имя — "тюнер", макрос, созданный для полного имени, будет иметь значение "AV \_ тюнер".</span><span class="sxs-lookup"><span data-stu-id="d8d46-117">For example, if the macro prefix is "AV\_" and the name is "Tuner", the macro generated for the qualified name will be "AV\_Tuner".</span></span>

<span data-ttu-id="d8d46-118">По умолчанию созданный код создает предпочтительный префикс макроса из универсального кода ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="d8d46-118">By default, the code generated creates a preferred macro prefix from the URI.</span></span>

## <a name="element-information"></a><span data-ttu-id="d8d46-119">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d8d46-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="d8d46-120">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="d8d46-120">Minimum supported system</span></span><br/> | <span data-ttu-id="d8d46-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8d46-121">Windows Vista</span></span> |
| <span data-ttu-id="d8d46-122">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="d8d46-122">Can be empty</span></span>                        | <span data-ttu-id="d8d46-123">Да</span><span class="sxs-lookup"><span data-stu-id="d8d46-123">Yes</span></span>           |



 

 




