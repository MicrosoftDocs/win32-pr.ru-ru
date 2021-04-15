---
description: Указывает тип дераспределителя, используемый функцией-заглушкой.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: элемент распределителя
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3604f0efb366c3f88e2e0828c02344ee75606079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263913"
---
# <a name="deallocator-element"></a><span data-ttu-id="1beca-103">элемент распределителя</span><span class="sxs-lookup"><span data-stu-id="1beca-103">deallocator element</span></span>

<span data-ttu-id="1beca-104">Указывает тип дераспределителя, используемый функцией-заглушкой.</span><span class="sxs-lookup"><span data-stu-id="1beca-104">Specifies the type of deallocator to be used by a stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="1beca-105">Использование</span><span class="sxs-lookup"><span data-stu-id="1beca-105">Usage</span></span>

``` syntax
<deallocator/>
```

## <a name="attributes"></a><span data-ttu-id="1beca-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1beca-106">Attributes</span></span>

<span data-ttu-id="1beca-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="1beca-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="1beca-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1beca-108">Child elements</span></span>

<span data-ttu-id="1beca-109">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="1beca-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="1beca-110">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="1beca-110">Parent elements</span></span>



| <span data-ttu-id="1beca-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="1beca-111">Element</span></span>                                               | <span data-ttu-id="1beca-112">Описание</span><span class="sxs-lookup"><span data-stu-id="1beca-112">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1beca-113">**стубдефинитионс**</span><span class="sxs-lookup"><span data-stu-id="1beca-113">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="1beca-114">Создает реализации для функций-заглушек для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="1beca-114">Generates implementations for stub functions for port-type operations.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="1beca-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1beca-115">Remarks</span></span>

<span data-ttu-id="1beca-116">Тип дераспределителя должен быть заключен в пару <deallocator></deallocator> тегов.</span><span class="sxs-lookup"><span data-stu-id="1beca-116">The deallocator type should be enclosed in a pair of <deallocator></deallocator> tags.</span></span> <span data-ttu-id="1beca-117">Следующие строки являются допустимыми значениями для дераспределения:</span><span class="sxs-lookup"><span data-stu-id="1beca-117">The following strings are valid deallocator values:</span></span>

-   <span data-ttu-id="1beca-118">нет</span><span class="sxs-lookup"><span data-stu-id="1beca-118">none</span></span>
-   <span data-ttu-id="1beca-119">всдфрилинкедмемори</span><span class="sxs-lookup"><span data-stu-id="1beca-119">WSDFreeLinkedMemory</span></span>
-   <span data-ttu-id="1beca-120">CoTaskMemFree</span><span class="sxs-lookup"><span data-stu-id="1beca-120">CoTaskMemFree</span></span>
-   <span data-ttu-id="1beca-121">free</span><span class="sxs-lookup"><span data-stu-id="1beca-121">free</span></span>
-   <span data-ttu-id="1beca-122">удалить</span><span class="sxs-lookup"><span data-stu-id="1beca-122">delete</span></span>
-   <span data-ttu-id="1beca-123">делетеаррай</span><span class="sxs-lookup"><span data-stu-id="1beca-123">deleteArray</span></span>
-   <span data-ttu-id="1beca-124">Release</span><span class="sxs-lookup"><span data-stu-id="1beca-124">Release</span></span>

## <a name="element-information"></a><span data-ttu-id="1beca-125">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1beca-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="1beca-126">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="1beca-126">Minimum supported system</span></span><br/> | <span data-ttu-id="1beca-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1beca-127">Windows Vista</span></span> |
| <span data-ttu-id="1beca-128">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="1beca-128">Can be empty</span></span>                        | <span data-ttu-id="1beca-129">Да</span><span class="sxs-lookup"><span data-stu-id="1beca-129">Yes</span></span>           |



 

 




