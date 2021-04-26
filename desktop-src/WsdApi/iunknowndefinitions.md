---
description: Создает реализации для функций QueryInterface, AddRef и Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Иункновндефинитионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb3a4f76145e585411e64c10ea7af922db931846
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995151"
---
# <a name="iunknowndefinitions-element"></a><span data-ttu-id="1687a-103">Иункновндефинитионс, элемент</span><span class="sxs-lookup"><span data-stu-id="1687a-103">IUnknownDefinitions element</span></span>

<span data-ttu-id="1687a-104">Создает реализации для функций QueryInterface, AddRef и Release.</span><span class="sxs-lookup"><span data-stu-id="1687a-104">Generates implementations for the QueryInterface, AddRef and Release functions.</span></span>

## <a name="usage"></a><span data-ttu-id="1687a-105">Использование</span><span class="sxs-lookup"><span data-stu-id="1687a-105">Usage</span></span>

``` syntax
<IUnknownDefinitions
  proxyClass = "character_string"
  refCountVar = "character_string">
  child elements
</IUnknownDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="1687a-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1687a-106">Attributes</span></span>



| <span data-ttu-id="1687a-107">attribute</span><span class="sxs-lookup"><span data-stu-id="1687a-107">Attribute</span></span>                  | <span data-ttu-id="1687a-108">Тип</span><span class="sxs-lookup"><span data-stu-id="1687a-108">Type</span></span>                         | <span data-ttu-id="1687a-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="1687a-109">Required</span></span>       | <span data-ttu-id="1687a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="1687a-110">Description</span></span>                                                |
|----------------------------|------------------------------|----------------|------------------------------------------------------------|
| <span data-ttu-id="1687a-111">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="1687a-111">**proxyClass**</span></span><br/>  | <span data-ttu-id="1687a-112">Символьная \_ строка</span><span class="sxs-lookup"><span data-stu-id="1687a-112">character\_string</span></span><br/> | <span data-ttu-id="1687a-113">Да</span><span class="sxs-lookup"><span data-stu-id="1687a-113">Yes</span></span><br/> | <span data-ttu-id="1687a-114">Имя реализующего класса.</span><span class="sxs-lookup"><span data-stu-id="1687a-114">The name of the implementing class.</span></span><br/> <br/> |
| <span data-ttu-id="1687a-115">**рефкаунтвар**</span><span class="sxs-lookup"><span data-stu-id="1687a-115">**refCountVar**</span></span><br/> | <span data-ttu-id="1687a-116">Символьная \_ строка</span><span class="sxs-lookup"><span data-stu-id="1687a-116">character\_string</span></span><br/> | <span data-ttu-id="1687a-117">Да</span><span class="sxs-lookup"><span data-stu-id="1687a-117">Yes</span></span><br/> | <span data-ttu-id="1687a-118">Имя переменной счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="1687a-118">The reference count variable name.</span></span><br/> <br/>  |



## <a name="child-elements"></a><span data-ttu-id="1687a-119">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1687a-119">Child elements</span></span>



| <span data-ttu-id="1687a-120">Элемент</span><span class="sxs-lookup"><span data-stu-id="1687a-120">Element</span></span>                                   | <span data-ttu-id="1687a-121">Описание</span><span class="sxs-lookup"><span data-stu-id="1687a-121">Description</span></span>                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="1687a-122">**интерфейс**</span><span class="sxs-lookup"><span data-stu-id="1687a-122">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="1687a-123">Имя интерфейса, возвращаемого QueryInterface.</span><span class="sxs-lookup"><span data-stu-id="1687a-123">The name of the interface to be returned by QueryInterface.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="1687a-124">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="1687a-124">Child element sequence</span></span>

``` syntax
interface
```

## <a name="parent-elements"></a><span data-ttu-id="1687a-125">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="1687a-125">Parent elements</span></span>



| <span data-ttu-id="1687a-126">Элемент</span><span class="sxs-lookup"><span data-stu-id="1687a-126">Element</span></span>                         | <span data-ttu-id="1687a-127">Описание</span><span class="sxs-lookup"><span data-stu-id="1687a-127">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="1687a-128">**File**</span><span class="sxs-lookup"><span data-stu-id="1687a-128">**file**</span></span>](file.md)<br/> | <span data-ttu-id="1687a-129">Выводит файл из генератора кода.</span><span class="sxs-lookup"><span data-stu-id="1687a-129">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="1687a-130">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1687a-130">Element information</span></span>



| <span data-ttu-id="1687a-131">Метка</span><span class="sxs-lookup"><span data-stu-id="1687a-131">Label</span></span> | <span data-ttu-id="1687a-132">Значение</span><span class="sxs-lookup"><span data-stu-id="1687a-132">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="1687a-133">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="1687a-133">Minimum supported system</span></span><br/> | <span data-ttu-id="1687a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1687a-134">Windows Vista</span></span> |
| <span data-ttu-id="1687a-135">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="1687a-135">Can be empty</span></span>                        | <span data-ttu-id="1687a-136">нет</span><span class="sxs-lookup"><span data-stu-id="1687a-136">No</span></span>            |



 

 




