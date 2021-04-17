---
description: Задает дераспределитель типов, используемый функцией-заглушкой операции.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: Оператиондеаллокатор, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c214b5dbc3245f63797c55880fe052d5c3ced15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693125"
---
# <a name="operationdeallocator-element"></a><span data-ttu-id="d5214-103">Оператиондеаллокатор, элемент</span><span class="sxs-lookup"><span data-stu-id="d5214-103">operationDeallocator element</span></span>

<span data-ttu-id="d5214-104">Указывает дераспределитель типов, используемый функцией-заглушкой операции.</span><span class="sxs-lookup"><span data-stu-id="d5214-104">Specifies the type deallocator to be used by an operation's stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="d5214-105">Использование</span><span class="sxs-lookup"><span data-stu-id="d5214-105">Usage</span></span>

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="d5214-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d5214-106">Attributes</span></span>



| <span data-ttu-id="d5214-107">attribute</span><span class="sxs-lookup"><span data-stu-id="d5214-107">Attribute</span></span>                  | <span data-ttu-id="d5214-108">Тип</span><span class="sxs-lookup"><span data-stu-id="d5214-108">Type</span></span>                         | <span data-ttu-id="d5214-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="d5214-109">Required</span></span>       | <span data-ttu-id="d5214-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d5214-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5214-111">**не предусматривающую**</span><span class="sxs-lookup"><span data-stu-id="d5214-111">**deallocator**</span></span><br/> | <span data-ttu-id="d5214-112">Символьная \_ строка</span><span class="sxs-lookup"><span data-stu-id="d5214-112">character\_string</span></span><br/> | <span data-ttu-id="d5214-113">Да</span><span class="sxs-lookup"><span data-stu-id="d5214-113">Yes</span></span><br/> | <span data-ttu-id="d5214-114">Дераспределитель, используемый для операции.</span><span class="sxs-lookup"><span data-stu-id="d5214-114">The deallocator to use for the operation.</span></span><br/> <br/> <span data-ttu-id="d5214-115">Следующие строки являются допустимыми значениями.</span><span class="sxs-lookup"><span data-stu-id="d5214-115">The following strings are valid values.</span></span><br/> <br/> <dl><span data-ttu-id="d5214-116"><span id="none"></span><span id="NONE"></span><dt>\* \* \* нет \* \*</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> \* \* \* \* \* \* <dt>Всдфрилинкедмемори \*</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> \* \* \* \* \* \* \* <dt>CoTaskMemFree \*</dt> <span id="free"></span> <span id="FREE"></span> \* \* \* \* \* \* \* <dt>бесплатная \*</dt> <span id="delete"></span> <span id="DELETE"></span> \* \* \* \* \* \* \* \* <dt>Delete \*</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> \* \* \* \* \* \* \* <dt>делетеаррай \*</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> \* \* \* \* \* \* \* <dt>Выпуск \*</dt> \* \* \*</span><span class="sxs-lookup"><span data-stu-id="d5214-116"><span id="none"></span><span id="NONE"></span><dt>\*\*\*\*none\*\*\*\*</dt><span id="WSDFreeLinkedMemory"></span><span id="wsdfreelinkedmemory"></span><span id="WSDFREELINKEDMEMORY"></span><dt>\*\*\*\*WSDFreeLinkedMemory\*\*\*\*</dt><span id="CoTaskMemFree"></span><span id="cotaskmemfree"></span><span id="COTASKMEMFREE"></span><dt>\*\*\*\*CoTaskMemFree\*\*\*\*</dt><span id="free"></span><span id="FREE"></span><dt>\*\*\*\*free\*\*\*\*</dt><span id="delete"></span><span id="DELETE"></span><dt>\*\*\*\*delete\*\*\*\*</dt><span id="deleteArray"></span><span id="deletearray"></span><span id="DELETEARRAY"></span><dt>\*\*\*\*deleteArray\*\*\*\*</dt><span id="Release"></span><span id="release"></span><span id="RELEASE"></span><dt>\*\*\*\*Release\*\*\*\*</dt></span></span> </dl> |
| <span data-ttu-id="d5214-117">**operation**</span><span class="sxs-lookup"><span data-stu-id="d5214-117">**operation**</span></span><br/>   | <span data-ttu-id="d5214-118">Символьная \_ строка</span><span class="sxs-lookup"><span data-stu-id="d5214-118">character\_string</span></span><br/> | <span data-ttu-id="d5214-119">Да</span><span class="sxs-lookup"><span data-stu-id="d5214-119">Yes</span></span><br/> | <span data-ttu-id="d5214-120">Имя операции.</span><span class="sxs-lookup"><span data-stu-id="d5214-120">The name of the operation.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a><span data-ttu-id="d5214-121">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d5214-121">Child elements</span></span>

<span data-ttu-id="d5214-122">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="d5214-122">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="d5214-123">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="d5214-123">Parent elements</span></span>



| <span data-ttu-id="d5214-124">Элемент</span><span class="sxs-lookup"><span data-stu-id="d5214-124">Element</span></span>                                               | <span data-ttu-id="d5214-125">Описание</span><span class="sxs-lookup"><span data-stu-id="d5214-125">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5214-126">**стубдефинитионс**</span><span class="sxs-lookup"><span data-stu-id="d5214-126">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="d5214-127">Создает реализации для функций-заглушек для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="d5214-127">Generates implementations for stub functions for port type operations.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="d5214-128">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d5214-128">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="d5214-129">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="d5214-129">Minimum supported system</span></span><br/> | <span data-ttu-id="d5214-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5214-130">Windows Vista</span></span> |
| <span data-ttu-id="d5214-131">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="d5214-131">Can be empty</span></span>                        | <span data-ttu-id="d5214-132">Да</span><span class="sxs-lookup"><span data-stu-id="d5214-132">Yes</span></span>           |



 

 




