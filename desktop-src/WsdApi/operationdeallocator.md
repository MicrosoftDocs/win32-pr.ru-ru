---
description: Задает дераспределитель типов, используемый функцией-заглушкой операции.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: Оператиондеаллокатор, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe3ae0d9f1d37a478ceca0895806ade6a011747e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994291"
---
# <a name="operationdeallocator-element"></a><span data-ttu-id="0e27a-103">Оператиондеаллокатор, элемент</span><span class="sxs-lookup"><span data-stu-id="0e27a-103">operationDeallocator element</span></span>

<span data-ttu-id="0e27a-104">Указывает дераспределитель типов, используемый функцией-заглушкой операции.</span><span class="sxs-lookup"><span data-stu-id="0e27a-104">Specifies the type deallocator to be used by an operation's stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="0e27a-105">Использование</span><span class="sxs-lookup"><span data-stu-id="0e27a-105">Usage</span></span>

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="0e27a-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0e27a-106">Attributes</span></span>



| <span data-ttu-id="0e27a-107">attribute</span><span class="sxs-lookup"><span data-stu-id="0e27a-107">Attribute</span></span>                  | <span data-ttu-id="0e27a-108">Тип</span><span class="sxs-lookup"><span data-stu-id="0e27a-108">Type</span></span>                         | <span data-ttu-id="0e27a-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="0e27a-109">Required</span></span>       | <span data-ttu-id="0e27a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0e27a-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e27a-111">**не предусматривающую**</span><span class="sxs-lookup"><span data-stu-id="0e27a-111">**deallocator**</span></span><br/> | <span data-ttu-id="0e27a-112">Символьная \_ строка</span><span class="sxs-lookup"><span data-stu-id="0e27a-112">character\_string</span></span><br/> | <span data-ttu-id="0e27a-113">Да</span><span class="sxs-lookup"><span data-stu-id="0e27a-113">Yes</span></span><br/> | <span data-ttu-id="0e27a-114">Дераспределитель, используемый для операции.</span><span class="sxs-lookup"><span data-stu-id="0e27a-114">The deallocator to use for the operation.</span></span><br/> <br/> <span data-ttu-id="0e27a-115">Следующие строки являются допустимыми значениями.</span><span class="sxs-lookup"><span data-stu-id="0e27a-115">The following strings are valid values.</span></span><br/> <br/> <dl><span data-ttu-id="0e27a-116"><span id="none"></span><span id="NONE"></span><dt>\* \* \* нет \* \*</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> \* \* \* \* \* \* <dt>Всдфрилинкедмемори \*</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> \* \* \* \* \* \* \* <dt>CoTaskMemFree \*</dt> <span id="free"></span> <span id="FREE"></span> \* \* \* \* \* \* \* <dt>бесплатная \*</dt> <span id="delete"></span> <span id="DELETE"></span> \* \* \* \* \* \* \* \* <dt>Delete \*</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> \* \* \* \* \* \* \* <dt>делетеаррай \*</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> \* \* \* \* \* \* \* <dt>Выпуск \*</dt> \* \* \*</span><span class="sxs-lookup"><span data-stu-id="0e27a-116"><span id="none"></span><span id="NONE"></span><dt>\*\*\*\*none\*\*\*\*</dt><span id="WSDFreeLinkedMemory"></span><span id="wsdfreelinkedmemory"></span><span id="WSDFREELINKEDMEMORY"></span><dt>\*\*\*\*WSDFreeLinkedMemory\*\*\*\*</dt><span id="CoTaskMemFree"></span><span id="cotaskmemfree"></span><span id="COTASKMEMFREE"></span><dt>\*\*\*\*CoTaskMemFree\*\*\*\*</dt><span id="free"></span><span id="FREE"></span><dt>\*\*\*\*free\*\*\*\*</dt><span id="delete"></span><span id="DELETE"></span><dt>\*\*\*\*delete\*\*\*\*</dt><span id="deleteArray"></span><span id="deletearray"></span><span id="DELETEARRAY"></span><dt>\*\*\*\*deleteArray\*\*\*\*</dt><span id="Release"></span><span id="release"></span><span id="RELEASE"></span><dt>\*\*\*\*Release\*\*\*\*</dt></span></span> </dl> |
| <span data-ttu-id="0e27a-117">**operation**</span><span class="sxs-lookup"><span data-stu-id="0e27a-117">**operation**</span></span><br/>   | <span data-ttu-id="0e27a-118">Символьная \_ строка</span><span class="sxs-lookup"><span data-stu-id="0e27a-118">character\_string</span></span><br/> | <span data-ttu-id="0e27a-119">Да</span><span class="sxs-lookup"><span data-stu-id="0e27a-119">Yes</span></span><br/> | <span data-ttu-id="0e27a-120">Имя операции.</span><span class="sxs-lookup"><span data-stu-id="0e27a-120">The name of the operation.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a><span data-ttu-id="0e27a-121">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0e27a-121">Child elements</span></span>

<span data-ttu-id="0e27a-122">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="0e27a-122">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="0e27a-123">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="0e27a-123">Parent elements</span></span>



| <span data-ttu-id="0e27a-124">Элемент</span><span class="sxs-lookup"><span data-stu-id="0e27a-124">Element</span></span>                                               | <span data-ttu-id="0e27a-125">Описание</span><span class="sxs-lookup"><span data-stu-id="0e27a-125">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e27a-126">**стубдефинитионс**</span><span class="sxs-lookup"><span data-stu-id="0e27a-126">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="0e27a-127">Создает реализации для функций-заглушек для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="0e27a-127">Generates implementations for stub functions for port type operations.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="0e27a-128">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0e27a-128">Element information</span></span>



| <span data-ttu-id="0e27a-129">Метка</span><span class="sxs-lookup"><span data-stu-id="0e27a-129">Label</span></span> | <span data-ttu-id="0e27a-130">Значение</span><span class="sxs-lookup"><span data-stu-id="0e27a-130">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="0e27a-131">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="0e27a-131">Minimum supported system</span></span><br/> | <span data-ttu-id="0e27a-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e27a-132">Windows Vista</span></span> |
| <span data-ttu-id="0e27a-133">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="0e27a-133">Can be empty</span></span>                        | <span data-ttu-id="0e27a-134">Да</span><span class="sxs-lookup"><span data-stu-id="0e27a-134">Yes</span></span>           |



 

 




