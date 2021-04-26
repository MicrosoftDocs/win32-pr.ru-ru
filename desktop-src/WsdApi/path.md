---
description: Указывает расположение и имя файла WSDL. Путь может быть абсолютным или относительным путем к файлу, но не должен быть URL-адресом.
ms.assetid: 0664dcc6-1e71-46cf-9084-1adc84861b52
title: элемент Path (веб-службы на устройствах)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48df5a156149f00b8b153ccc0d46d6d2d34a1ce
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994311"
---
# <a name="path-element"></a><span data-ttu-id="12e91-104">элемент Path</span><span class="sxs-lookup"><span data-stu-id="12e91-104">path element</span></span>

<span data-ttu-id="12e91-105">Указывает расположение и имя файла WSDL.</span><span class="sxs-lookup"><span data-stu-id="12e91-105">Specifies the location and filename of a WSDL file.</span></span> <span data-ttu-id="12e91-106">Путь может быть абсолютным или относительным путем к файлу, но не должен быть URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="12e91-106">The path may be an absolute or relative path to the file, but must not be an URL.</span></span>

## <a name="usage"></a><span data-ttu-id="12e91-107">Использование</span><span class="sxs-lookup"><span data-stu-id="12e91-107">Usage</span></span>

``` syntax
<path/>
```

## <a name="attributes"></a><span data-ttu-id="12e91-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="12e91-108">Attributes</span></span>

<span data-ttu-id="12e91-109">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="12e91-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="12e91-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="12e91-110">Child elements</span></span>

<span data-ttu-id="12e91-111">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="12e91-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="12e91-112">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="12e91-112">Parent elements</span></span>



| <span data-ttu-id="12e91-113">Элемент</span><span class="sxs-lookup"><span data-stu-id="12e91-113">Element</span></span>                         | <span data-ttu-id="12e91-114">Описание</span><span class="sxs-lookup"><span data-stu-id="12e91-114">Description</span></span>                                                             |
|---------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="12e91-115">**файле**</span><span class="sxs-lookup"><span data-stu-id="12e91-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="12e91-116">WSDL-файл для обработки сведений о контракте.</span><span class="sxs-lookup"><span data-stu-id="12e91-116">A WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="examples"></a><span data-ttu-id="12e91-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="12e91-117">Examples</span></span>

<span data-ttu-id="12e91-118">В следующем XML-коде показан допустимый элемент **path** .</span><span class="sxs-lookup"><span data-stu-id="12e91-118">The following XML shows a valid **path** element.</span></span>

``` syntax
<path>"..\wsdls\example.wsdl"</path>
```

## <a name="element-information"></a><span data-ttu-id="12e91-119">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="12e91-119">Element information</span></span>



| <span data-ttu-id="12e91-120">Метка</span><span class="sxs-lookup"><span data-stu-id="12e91-120">Label</span></span> | <span data-ttu-id="12e91-121">Значение</span><span class="sxs-lookup"><span data-stu-id="12e91-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="12e91-122">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="12e91-122">Minimum supported system</span></span><br/> | <span data-ttu-id="12e91-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12e91-123">Windows Vista</span></span> |
| <span data-ttu-id="12e91-124">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="12e91-124">Can be empty</span></span>                        | <span data-ttu-id="12e91-125">Да</span><span class="sxs-lookup"><span data-stu-id="12e91-125">Yes</span></span>           |



 

 




