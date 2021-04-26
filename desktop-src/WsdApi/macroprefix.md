---
description: Определяет префикс, который будет использоваться в созданном коде для имен макросов в пространстве имен.
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: Макропрефикс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9590092d78ea4700715a868bb7e50f15833011
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998751"
---
# <a name="macroprefix-element"></a><span data-ttu-id="e1508-103">Макропрефикс, элемент</span><span class="sxs-lookup"><span data-stu-id="e1508-103">macroPrefix element</span></span>

<span data-ttu-id="e1508-104">Определяет префикс, который будет использоваться в созданном коде для имен макросов в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="e1508-104">Defines the prefix to be used in the generated code for names of macros in the namespace.</span></span>

## <a name="usage"></a><span data-ttu-id="e1508-105">Использование</span><span class="sxs-lookup"><span data-stu-id="e1508-105">Usage</span></span>

``` syntax
<macroPrefix/>
```

## <a name="attributes"></a><span data-ttu-id="e1508-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e1508-106">Attributes</span></span>

<span data-ttu-id="e1508-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="e1508-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e1508-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e1508-108">Child elements</span></span>

<span data-ttu-id="e1508-109">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="e1508-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="e1508-110">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e1508-110">Parent elements</span></span>



| <span data-ttu-id="e1508-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="e1508-111">Element</span></span>                                   | <span data-ttu-id="e1508-112">Описание</span><span class="sxs-lookup"><span data-stu-id="e1508-112">Description</span></span>                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="e1508-113">**Имен**</span><span class="sxs-lookup"><span data-stu-id="e1508-113">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="e1508-114">Пространство имен, используемое для создания кода.</span><span class="sxs-lookup"><span data-stu-id="e1508-114">A namespace to be used for code generation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="e1508-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="e1508-115">Remarks</span></span>

<span data-ttu-id="e1508-116">Этот элемент переопределяет префикс URI по умолчанию, используемый для созданных макросов.</span><span class="sxs-lookup"><span data-stu-id="e1508-116">This element overrides the default URI prefix used for generated macros.</span></span> <span data-ttu-id="e1508-117">Например, если префиксом макроса является "AV \_ ", а имя — "тюнер", макрос, созданный для полного имени, будет иметь значение "AV \_ тюнер".</span><span class="sxs-lookup"><span data-stu-id="e1508-117">For example, if the macro prefix is "AV\_" and the name is "Tuner", the macro generated for the qualified name will be "AV\_Tuner".</span></span>

<span data-ttu-id="e1508-118">По умолчанию созданный код создает предпочтительный префикс макроса из универсального кода ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="e1508-118">By default, the code generated creates a preferred macro prefix from the URI.</span></span>

## <a name="element-information"></a><span data-ttu-id="e1508-119">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e1508-119">Element information</span></span>



| <span data-ttu-id="e1508-120">Метка</span><span class="sxs-lookup"><span data-stu-id="e1508-120">Label</span></span> | <span data-ttu-id="e1508-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e1508-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="e1508-122">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="e1508-122">Minimum supported system</span></span><br/> | <span data-ttu-id="e1508-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1508-123">Windows Vista</span></span> |
| <span data-ttu-id="e1508-124">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="e1508-124">Can be empty</span></span>                        | <span data-ttu-id="e1508-125">Да</span><span class="sxs-lookup"><span data-stu-id="e1508-125">Yes</span></span>           |



 

 




