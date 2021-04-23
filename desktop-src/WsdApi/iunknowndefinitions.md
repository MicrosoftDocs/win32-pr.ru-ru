---
description: Создает реализации для функций QueryInterface, AddRef и Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Иункновндефинитионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ca92338e3dc97a12e04228510fc17eb2ef2483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711708"
---
# <a name="iunknowndefinitions-element"></a><span data-ttu-id="6e206-103">Иункновндефинитионс, элемент</span><span class="sxs-lookup"><span data-stu-id="6e206-103">IUnknownDefinitions element</span></span>

<span data-ttu-id="6e206-104">Создает реализации для функций QueryInterface, AddRef и Release.</span><span class="sxs-lookup"><span data-stu-id="6e206-104">Generates implementations for the QueryInterface, AddRef and Release functions.</span></span>

## <a name="usage"></a><span data-ttu-id="6e206-105">Использование</span><span class="sxs-lookup"><span data-stu-id="6e206-105">Usage</span></span>

``` syntax
<IUnknownDefinitions
  proxyClass = "character_string"
  refCountVar = "character_string">
  child elements
</IUnknownDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="6e206-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6e206-106">Attributes</span></span>



| <span data-ttu-id="6e206-107">attribute</span><span class="sxs-lookup"><span data-stu-id="6e206-107">Attribute</span></span>                  | <span data-ttu-id="6e206-108">Тип</span><span class="sxs-lookup"><span data-stu-id="6e206-108">Type</span></span>                         | <span data-ttu-id="6e206-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="6e206-109">Required</span></span>       | <span data-ttu-id="6e206-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6e206-110">Description</span></span>                                                |
|----------------------------|------------------------------|----------------|------------------------------------------------------------|
| <span data-ttu-id="6e206-111">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="6e206-111">**proxyClass**</span></span><br/>  | <span data-ttu-id="6e206-112">Символьная \_ строка</span><span class="sxs-lookup"><span data-stu-id="6e206-112">character\_string</span></span><br/> | <span data-ttu-id="6e206-113">Да</span><span class="sxs-lookup"><span data-stu-id="6e206-113">Yes</span></span><br/> | <span data-ttu-id="6e206-114">Имя реализующего класса.</span><span class="sxs-lookup"><span data-stu-id="6e206-114">The name of the implementing class.</span></span><br/> <br/> |
| <span data-ttu-id="6e206-115">**рефкаунтвар**</span><span class="sxs-lookup"><span data-stu-id="6e206-115">**refCountVar**</span></span><br/> | <span data-ttu-id="6e206-116">Символьная \_ строка</span><span class="sxs-lookup"><span data-stu-id="6e206-116">character\_string</span></span><br/> | <span data-ttu-id="6e206-117">Да</span><span class="sxs-lookup"><span data-stu-id="6e206-117">Yes</span></span><br/> | <span data-ttu-id="6e206-118">Имя переменной счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="6e206-118">The reference count variable name.</span></span><br/> <br/>  |



## <a name="child-elements"></a><span data-ttu-id="6e206-119">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6e206-119">Child elements</span></span>



| <span data-ttu-id="6e206-120">Элемент</span><span class="sxs-lookup"><span data-stu-id="6e206-120">Element</span></span>                                   | <span data-ttu-id="6e206-121">Описание</span><span class="sxs-lookup"><span data-stu-id="6e206-121">Description</span></span>                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="6e206-122">**интерфейс**</span><span class="sxs-lookup"><span data-stu-id="6e206-122">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="6e206-123">Имя интерфейса, возвращаемого QueryInterface.</span><span class="sxs-lookup"><span data-stu-id="6e206-123">The name of the interface to be returned by QueryInterface.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="6e206-124">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="6e206-124">Child element sequence</span></span>

``` syntax
interface
```

## <a name="parent-elements"></a><span data-ttu-id="6e206-125">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="6e206-125">Parent elements</span></span>



| <span data-ttu-id="6e206-126">Элемент</span><span class="sxs-lookup"><span data-stu-id="6e206-126">Element</span></span>                         | <span data-ttu-id="6e206-127">Описание</span><span class="sxs-lookup"><span data-stu-id="6e206-127">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="6e206-128">**File**</span><span class="sxs-lookup"><span data-stu-id="6e206-128">**file**</span></span>](file.md)<br/> | <span data-ttu-id="6e206-129">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="6e206-129">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="6e206-130">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6e206-130">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="6e206-131">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="6e206-131">Minimum supported system</span></span><br/> | <span data-ttu-id="6e206-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e206-132">Windows Vista</span></span> |
| <span data-ttu-id="6e206-133">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="6e206-133">Can be empty</span></span>                        | <span data-ttu-id="6e206-134">Нет</span><span class="sxs-lookup"><span data-stu-id="6e206-134">No</span></span>            |



 

 




