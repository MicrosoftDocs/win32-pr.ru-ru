---
description: Указывает расположение и имя файла WSDL. Путь может быть абсолютным или относительным путем к файлу, но не должен быть URL-адресом.
ms.assetid: 0664dcc6-1e71-46cf-9084-1adc84861b52
title: элемент Path (веб-службы на устройствах)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 763ad1479c20553fb7e62ab29e504d56bfa6d950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702291"
---
# <a name="path-element"></a><span data-ttu-id="9d894-104">элемент Path</span><span class="sxs-lookup"><span data-stu-id="9d894-104">path element</span></span>

<span data-ttu-id="9d894-105">Указывает расположение и имя файла WSDL.</span><span class="sxs-lookup"><span data-stu-id="9d894-105">Specifies the location and filename of a WSDL file.</span></span> <span data-ttu-id="9d894-106">Путь может быть абсолютным или относительным путем к файлу, но не должен быть URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="9d894-106">The path may be an absolute or relative path to the file, but must not be an URL.</span></span>

## <a name="usage"></a><span data-ttu-id="9d894-107">Использование</span><span class="sxs-lookup"><span data-stu-id="9d894-107">Usage</span></span>

``` syntax
<path/>
```

## <a name="attributes"></a><span data-ttu-id="9d894-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9d894-108">Attributes</span></span>

<span data-ttu-id="9d894-109">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="9d894-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9d894-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9d894-110">Child elements</span></span>

<span data-ttu-id="9d894-111">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="9d894-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="9d894-112">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="9d894-112">Parent elements</span></span>



| <span data-ttu-id="9d894-113">Элемент</span><span class="sxs-lookup"><span data-stu-id="9d894-113">Element</span></span>                         | <span data-ttu-id="9d894-114">Описание</span><span class="sxs-lookup"><span data-stu-id="9d894-114">Description</span></span>                                                             |
|---------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="9d894-115">**файле**</span><span class="sxs-lookup"><span data-stu-id="9d894-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="9d894-116">WSDL-файл для обработки сведений о контракте.</span><span class="sxs-lookup"><span data-stu-id="9d894-116">A WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="examples"></a><span data-ttu-id="9d894-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="9d894-117">Examples</span></span>

<span data-ttu-id="9d894-118">В следующем XML-коде показан допустимый элемент **path** .</span><span class="sxs-lookup"><span data-stu-id="9d894-118">The following XML shows a valid **path** element.</span></span>

``` syntax
<path>"..\wsdls\example.wsdl"</path>
```

## <a name="element-information"></a><span data-ttu-id="9d894-119">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9d894-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="9d894-120">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="9d894-120">Minimum supported system</span></span><br/> | <span data-ttu-id="9d894-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d894-121">Windows Vista</span></span> |
| <span data-ttu-id="9d894-122">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="9d894-122">Can be empty</span></span>                        | <span data-ttu-id="9d894-123">Да</span><span class="sxs-lookup"><span data-stu-id="9d894-123">Yes</span></span>           |



 

 




