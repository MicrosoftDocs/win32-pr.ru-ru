---
description: Указывает XSD-файл для обработки сведений о контракте.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: элемент XSD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851ce31230ff88ea2465040c33dc131e0902392c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994551"
---
# <a name="xsd-element"></a><span data-ttu-id="6dda4-103">элемент XSD</span><span class="sxs-lookup"><span data-stu-id="6dda4-103">xsd element</span></span>

<span data-ttu-id="6dda4-104">Указывает XSD-файл для обработки сведений о контракте.</span><span class="sxs-lookup"><span data-stu-id="6dda4-104">Specifies an XSD file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="6dda4-105">Использование</span><span class="sxs-lookup"><span data-stu-id="6dda4-105">Usage</span></span>

``` syntax
<xsd
  path = "pathname string">
  child elements
</xsd>
```

## <a name="attributes"></a><span data-ttu-id="6dda4-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6dda4-106">Attributes</span></span>



| <span data-ttu-id="6dda4-107">attribute</span><span class="sxs-lookup"><span data-stu-id="6dda4-107">Attribute</span></span>           | <span data-ttu-id="6dda4-108">Тип</span><span class="sxs-lookup"><span data-stu-id="6dda4-108">Type</span></span>                       | <span data-ttu-id="6dda4-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="6dda4-109">Required</span></span>       | <span data-ttu-id="6dda4-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6dda4-110">Description</span></span>                                                 |
|---------------------|----------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="6dda4-111">**путь**</span><span class="sxs-lookup"><span data-stu-id="6dda4-111">**path**</span></span><br/> | <span data-ttu-id="6dda4-112">Строка пути</span><span class="sxs-lookup"><span data-stu-id="6dda4-112">pathname string</span></span><br/> | <span data-ttu-id="6dda4-113">Да</span><span class="sxs-lookup"><span data-stu-id="6dda4-113">Yes</span></span><br/> | <span data-ttu-id="6dda4-114">Файл и путь к входному файлу XSD.</span><span class="sxs-lookup"><span data-stu-id="6dda4-114">File and path of the XSD input file.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="6dda4-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6dda4-115">Child elements</span></span>



| <span data-ttu-id="6dda4-116">Элемент</span><span class="sxs-lookup"><span data-stu-id="6dda4-116">Element</span></span>                               | <span data-ttu-id="6dda4-117">Описание</span><span class="sxs-lookup"><span data-stu-id="6dda4-117">Description</span></span>                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="6dda4-118">**типеури**</span><span class="sxs-lookup"><span data-stu-id="6dda4-118">**typeUri**</span></span>](typeuri.md)<br/> | <span data-ttu-id="6dda4-119">Указывает тип, включаемый из XSD-файла.</span><span class="sxs-lookup"><span data-stu-id="6dda4-119">Specifies a type to include from an XSD file.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="6dda4-120">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="6dda4-120">Child element sequence</span></span>

``` syntax
typeUri*
```

## <a name="parent-elements"></a><span data-ttu-id="6dda4-121">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="6dda4-121">Parent elements</span></span>



| <span data-ttu-id="6dda4-122">Элемент</span><span class="sxs-lookup"><span data-stu-id="6dda4-122">Element</span></span>                                     | <span data-ttu-id="6dda4-123">Описание</span><span class="sxs-lookup"><span data-stu-id="6dda4-123">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="6dda4-124">**всдкодежен**</span><span class="sxs-lookup"><span data-stu-id="6dda4-124">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="6dda4-125">Корневой элемент XML-файла скрипта генератора кода WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="6dda4-125">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6dda4-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="6dda4-126">Remarks</span></span>

<span data-ttu-id="6dda4-127">Строка filename также должна содержать сведения о полном пути.</span><span class="sxs-lookup"><span data-stu-id="6dda4-127">The filename string should include complete path information as well.</span></span>

## <a name="element-information"></a><span data-ttu-id="6dda4-128">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6dda4-128">Element information</span></span>



| <span data-ttu-id="6dda4-129">Метка</span><span class="sxs-lookup"><span data-stu-id="6dda4-129">Label</span></span> | <span data-ttu-id="6dda4-130">Значение</span><span class="sxs-lookup"><span data-stu-id="6dda4-130">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="6dda4-131">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="6dda4-131">Minimum supported system</span></span><br/> | <span data-ttu-id="6dda4-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6dda4-132">Windows Vista</span></span> |
| <span data-ttu-id="6dda4-133">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="6dda4-133">Can be empty</span></span>                        | <span data-ttu-id="6dda4-134">Да</span><span class="sxs-lookup"><span data-stu-id="6dda4-134">Yes</span></span>           |



 

 




