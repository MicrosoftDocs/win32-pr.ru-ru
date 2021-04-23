---
title: Ресурс HTML
description: Определяет HTML-файл.
ms.assetid: d3cf8348-8c10-41d9-a061-cdce0e13abf4
keywords:
- Меню ресурсов HTML и другие ресурсы
topic_type:
- apiref
api_name:
- HTML
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9db6477aed5180ae18b99f53f4ebadf9d0ad0c91
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889731"
---
# <a name="html-resource"></a><span data-ttu-id="434ef-104">Ресурс HTML</span><span class="sxs-lookup"><span data-stu-id="434ef-104">HTML resource</span></span>

<span data-ttu-id="434ef-105">Определяет HTML-файл.</span><span class="sxs-lookup"><span data-stu-id="434ef-105">Defines an HTML file.</span></span>

``` syntax
nameID HTML filename
```

## <a name="parameters"></a><span data-ttu-id="434ef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="434ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="434ef-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="434ef-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="434ef-108">Уникальное имя или 16-разрядное целочисленное значение без знака, идентифицирующее ресурс.</span><span class="sxs-lookup"><span data-stu-id="434ef-108">Unique name or a 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="434ef-109"><span id="filename"></span><span id="FILENAME"></span>*файлов*</span><span class="sxs-lookup"><span data-stu-id="434ef-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="434ef-110">Имя HTML-файла.</span><span class="sxs-lookup"><span data-stu-id="434ef-110">The name of the HTML file.</span></span> <span data-ttu-id="434ef-111">Он должен быть полным или относительным путем, если файл не находится в текущем рабочем каталоге.</span><span class="sxs-lookup"><span data-stu-id="434ef-111">It must be a full or relative path if the file is not in the current working directory.</span></span> <span data-ttu-id="434ef-112">Путь должен представлять собой строку в кавычках.</span><span class="sxs-lookup"><span data-stu-id="434ef-112">The path should be a quoted string.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="434ef-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="434ef-113">Examples</span></span>

<span data-ttu-id="434ef-114">В следующем примере определяется ресурс HTML:</span><span class="sxs-lookup"><span data-stu-id="434ef-114">The following example defines an HTML resource:</span></span>

``` syntax
ID_RESPONSE_ERROR_PAGE  HTML "res\\responseerorpage.htm"
```

 

 




