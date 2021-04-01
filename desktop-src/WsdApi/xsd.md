---
description: Указывает XSD-файл для обработки сведений о контракте.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: элемент XSD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9628a078129446f51729c92c447f8da5736dab88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103909955"
---
# <a name="xsd-element"></a><span data-ttu-id="ddf5e-103">элемент XSD</span><span class="sxs-lookup"><span data-stu-id="ddf5e-103">xsd element</span></span>

<span data-ttu-id="ddf5e-104">Указывает XSD-файл для обработки сведений о контракте.</span><span class="sxs-lookup"><span data-stu-id="ddf5e-104">Specifies an XSD file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="ddf5e-105">Использование</span><span class="sxs-lookup"><span data-stu-id="ddf5e-105">Usage</span></span>

``` syntax
<xsd
  path = "pathname string">
  child elements
</xsd>
```

## <a name="attributes"></a><span data-ttu-id="ddf5e-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ddf5e-106">Attributes</span></span>



| <span data-ttu-id="ddf5e-107">attribute</span><span class="sxs-lookup"><span data-stu-id="ddf5e-107">Attribute</span></span>           | <span data-ttu-id="ddf5e-108">Тип</span><span class="sxs-lookup"><span data-stu-id="ddf5e-108">Type</span></span>                       | <span data-ttu-id="ddf5e-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="ddf5e-109">Required</span></span>       | <span data-ttu-id="ddf5e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ddf5e-110">Description</span></span>                                                 |
|---------------------|----------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="ddf5e-111">**путь**</span><span class="sxs-lookup"><span data-stu-id="ddf5e-111">**path**</span></span><br/> | <span data-ttu-id="ddf5e-112">Строка пути</span><span class="sxs-lookup"><span data-stu-id="ddf5e-112">pathname string</span></span><br/> | <span data-ttu-id="ddf5e-113">Да</span><span class="sxs-lookup"><span data-stu-id="ddf5e-113">Yes</span></span><br/> | <span data-ttu-id="ddf5e-114">Файл и путь к входному файлу XSD.</span><span class="sxs-lookup"><span data-stu-id="ddf5e-114">File and path of the XSD input file.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="ddf5e-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ddf5e-115">Child elements</span></span>



| <span data-ttu-id="ddf5e-116">Элемент</span><span class="sxs-lookup"><span data-stu-id="ddf5e-116">Element</span></span>                               | <span data-ttu-id="ddf5e-117">Описание</span><span class="sxs-lookup"><span data-stu-id="ddf5e-117">Description</span></span>                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="ddf5e-118">**типеури**</span><span class="sxs-lookup"><span data-stu-id="ddf5e-118">**typeUri**</span></span>](typeuri.md)<br/> | <span data-ttu-id="ddf5e-119">Указывает тип, включаемый из XSD-файла.</span><span class="sxs-lookup"><span data-stu-id="ddf5e-119">Specifies a type to include from an XSD file.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="ddf5e-120">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="ddf5e-120">Child element sequence</span></span>

``` syntax
typeUri*
```

## <a name="parent-elements"></a><span data-ttu-id="ddf5e-121">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ddf5e-121">Parent elements</span></span>



| <span data-ttu-id="ddf5e-122">Элемент</span><span class="sxs-lookup"><span data-stu-id="ddf5e-122">Element</span></span>                                     | <span data-ttu-id="ddf5e-123">Описание</span><span class="sxs-lookup"><span data-stu-id="ddf5e-123">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="ddf5e-124">**всдкодежен**</span><span class="sxs-lookup"><span data-stu-id="ddf5e-124">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="ddf5e-125">Корневой элемент XML-файла скрипта генератора кода WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="ddf5e-125">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ddf5e-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ddf5e-126">Remarks</span></span>

<span data-ttu-id="ddf5e-127">Строка filename также должна содержать сведения о полном пути.</span><span class="sxs-lookup"><span data-stu-id="ddf5e-127">The filename string should include complete path information as well.</span></span>

## <a name="element-information"></a><span data-ttu-id="ddf5e-128">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ddf5e-128">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="ddf5e-129">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="ddf5e-129">Minimum supported system</span></span><br/> | <span data-ttu-id="ddf5e-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ddf5e-130">Windows Vista</span></span> |
| <span data-ttu-id="ddf5e-131">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="ddf5e-131">Can be empty</span></span>                        | <span data-ttu-id="ddf5e-132">Да</span><span class="sxs-lookup"><span data-stu-id="ddf5e-132">Yes</span></span>           |



 

 




