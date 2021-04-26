---
description: Указывает тип дераспределителя, используемый функцией-заглушкой.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: элемент распределителя
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692ed2e57b3e649c0ee7af171f205c949496f9b4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994941"
---
# <a name="deallocator-element"></a><span data-ttu-id="f4da0-103">элемент распределителя</span><span class="sxs-lookup"><span data-stu-id="f4da0-103">deallocator element</span></span>

<span data-ttu-id="f4da0-104">Указывает тип дераспределителя, используемый функцией-заглушкой.</span><span class="sxs-lookup"><span data-stu-id="f4da0-104">Specifies the type of deallocator to be used by a stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="f4da0-105">Использование</span><span class="sxs-lookup"><span data-stu-id="f4da0-105">Usage</span></span>

``` syntax
<deallocator/>
```

## <a name="attributes"></a><span data-ttu-id="f4da0-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f4da0-106">Attributes</span></span>

<span data-ttu-id="f4da0-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="f4da0-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f4da0-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f4da0-108">Child elements</span></span>

<span data-ttu-id="f4da0-109">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="f4da0-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="f4da0-110">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f4da0-110">Parent elements</span></span>



| <span data-ttu-id="f4da0-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="f4da0-111">Element</span></span>                                               | <span data-ttu-id="f4da0-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f4da0-112">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4da0-113">**стубдефинитионс**</span><span class="sxs-lookup"><span data-stu-id="f4da0-113">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="f4da0-114">Создает реализации для функций-заглушек для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="f4da0-114">Generates implementations for stub functions for port-type operations.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f4da0-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="f4da0-115">Remarks</span></span>

<span data-ttu-id="f4da0-116">Тип дераспределителя должен быть заключен в пару <deallocator></deallocator> тегов.</span><span class="sxs-lookup"><span data-stu-id="f4da0-116">The deallocator type should be enclosed in a pair of <deallocator></deallocator> tags.</span></span> <span data-ttu-id="f4da0-117">Следующие строки являются допустимыми значениями для дераспределения:</span><span class="sxs-lookup"><span data-stu-id="f4da0-117">The following strings are valid deallocator values:</span></span>

-   <span data-ttu-id="f4da0-118">нет</span><span class="sxs-lookup"><span data-stu-id="f4da0-118">none</span></span>
-   <span data-ttu-id="f4da0-119">всдфрилинкедмемори</span><span class="sxs-lookup"><span data-stu-id="f4da0-119">WSDFreeLinkedMemory</span></span>
-   <span data-ttu-id="f4da0-120">CoTaskMemFree</span><span class="sxs-lookup"><span data-stu-id="f4da0-120">CoTaskMemFree</span></span>
-   <span data-ttu-id="f4da0-121">free</span><span class="sxs-lookup"><span data-stu-id="f4da0-121">free</span></span>
-   <span data-ttu-id="f4da0-122">удалить</span><span class="sxs-lookup"><span data-stu-id="f4da0-122">delete</span></span>
-   <span data-ttu-id="f4da0-123">делетеаррай</span><span class="sxs-lookup"><span data-stu-id="f4da0-123">deleteArray</span></span>
-   <span data-ttu-id="f4da0-124">Release</span><span class="sxs-lookup"><span data-stu-id="f4da0-124">Release</span></span>

## <a name="element-information"></a><span data-ttu-id="f4da0-125">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f4da0-125">Element information</span></span>



| <span data-ttu-id="f4da0-126">Метка</span><span class="sxs-lookup"><span data-stu-id="f4da0-126">Label</span></span> | <span data-ttu-id="f4da0-127">Значение</span><span class="sxs-lookup"><span data-stu-id="f4da0-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="f4da0-128">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="f4da0-128">Minimum supported system</span></span><br/> | <span data-ttu-id="f4da0-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4da0-129">Windows Vista</span></span> |
| <span data-ttu-id="f4da0-130">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="f4da0-130">Can be empty</span></span>                        | <span data-ttu-id="f4da0-131">Да</span><span class="sxs-lookup"><span data-stu-id="f4da0-131">Yes</span></span>           |



 

 




