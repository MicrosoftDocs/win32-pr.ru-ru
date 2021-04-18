---
description: 'Указывает расположение загрузки для директивы> <WSDL: Import, которая явно не задает расположение.'
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: Импорсинт, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce8da0a7fa45ed00489d405aaba8f1f6d7ab8fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702052"
---
# <a name="importhint-element"></a><span data-ttu-id="708e1-103">Импорсинт, элемент</span><span class="sxs-lookup"><span data-stu-id="708e1-103">importHint element</span></span>

<span data-ttu-id="708e1-104">Указывает расположение загрузки для директивы> <WSDL: Import, которая явно не задает расположение.</span><span class="sxs-lookup"><span data-stu-id="708e1-104">Specifies the download location for a <wsdl:import> directive that does not explicitly specify a location.</span></span>

## <a name="usage"></a><span data-ttu-id="708e1-105">Использование</span><span class="sxs-lookup"><span data-stu-id="708e1-105">Usage</span></span>

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a><span data-ttu-id="708e1-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="708e1-106">Attributes</span></span>

<span data-ttu-id="708e1-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="708e1-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="708e1-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="708e1-108">Child elements</span></span>



| <span data-ttu-id="708e1-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="708e1-109">Element</span></span>                                   | <span data-ttu-id="708e1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="708e1-110">Description</span></span>                                                                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="708e1-111">**места**</span><span class="sxs-lookup"><span data-stu-id="708e1-111">**location**</span></span>](location.md)<br/>   | <span data-ttu-id="708e1-112">Расположение импортируемого файла.</span><span class="sxs-lookup"><span data-stu-id="708e1-112">The location of the file to import.</span></span> <span data-ttu-id="708e1-113">Расположением может быть относительный путь, абсолютный путь или URL-адрес HTTP.</span><span class="sxs-lookup"><span data-stu-id="708e1-113">The location may be a relative path, an absolute path, or an HTTP URL.</span></span><br/> <br/> |
| [<span data-ttu-id="708e1-114">**Имен**</span><span class="sxs-lookup"><span data-stu-id="708e1-114">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="708e1-115">Импортируемое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="708e1-115">The namespace to import.</span></span> <span data-ttu-id="708e1-116">Оно должно соответствовать пространству имен, указанному в элементе <WSDL: Import>.</span><span class="sxs-lookup"><span data-stu-id="708e1-116">This should match the namespace specified in the <wsdl:import> element.</span></span><br/> <br/>     |



### <a name="child-element-sequence"></a><span data-ttu-id="708e1-117">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="708e1-117">Child element sequence</span></span>

``` syntax
(
  nameSpace, 
  location
)
```

## <a name="parent-elements"></a><span data-ttu-id="708e1-118">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="708e1-118">Parent elements</span></span>



| <span data-ttu-id="708e1-119">Элемент</span><span class="sxs-lookup"><span data-stu-id="708e1-119">Element</span></span>                         | <span data-ttu-id="708e1-120">Описание</span><span class="sxs-lookup"><span data-stu-id="708e1-120">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="708e1-121">**файле**</span><span class="sxs-lookup"><span data-stu-id="708e1-121">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="708e1-122">Указывает WSDL-файл для обработки сведений о контракте.</span><span class="sxs-lookup"><span data-stu-id="708e1-122">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="708e1-123">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="708e1-123">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="708e1-124">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="708e1-124">Minimum supported system</span></span><br/> | <span data-ttu-id="708e1-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="708e1-125">Windows Vista</span></span> |
| <span data-ttu-id="708e1-126">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="708e1-126">Can be empty</span></span>                        | <span data-ttu-id="708e1-127">Нет</span><span class="sxs-lookup"><span data-stu-id="708e1-127">No</span></span>            |



 

 




