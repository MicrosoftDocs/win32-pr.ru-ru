---
title: ШРИФТовый ресурс
description: Определяет файл, содержащий шрифт.
ms.assetid: 0e19edd5-6cfc-44e6-add4-7413eb94867a
keywords:
- Меню ресурсов шрифтов и другие ресурсы
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e205d80779a1a228ee50e062f6904c1ed4a4934
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784275"
---
# <a name="font-resource"></a><span data-ttu-id="890f4-104">ШРИФТовый ресурс</span><span class="sxs-lookup"><span data-stu-id="890f4-104">FONT resource</span></span>

<span data-ttu-id="890f4-105">Определяет файл, содержащий шрифт.</span><span class="sxs-lookup"><span data-stu-id="890f4-105">Defines a file that contains a font.</span></span>

``` syntax
nameID FONT filename
```

## <a name="parameters"></a><span data-ttu-id="890f4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="890f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="890f4-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="890f4-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="890f4-108">Уникальное 16-битовое целочисленное значение без знака, идентифицирующее ресурс.</span><span class="sxs-lookup"><span data-stu-id="890f4-108">Unique 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="890f4-109"><span id="filename"></span><span id="FILENAME"></span>*файлов*</span><span class="sxs-lookup"><span data-stu-id="890f4-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="890f4-110">Имя файла, содержащего ресурс.</span><span class="sxs-lookup"><span data-stu-id="890f4-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="890f4-111">Имя должно быть допустимым именем файла; Он должен быть полным путем, если файл не находится в текущем рабочем каталоге.</span><span class="sxs-lookup"><span data-stu-id="890f4-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="890f4-112">Путь должен представлять собой строку в кавычках.</span><span class="sxs-lookup"><span data-stu-id="890f4-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="890f4-113">Для обратной совместимости также поддерживаются некоторые атрибуты.</span><span class="sxs-lookup"><span data-stu-id="890f4-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="890f4-114">Дополнительные сведения см. в разделе [Общие атрибуты ресурсов](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="890f4-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="890f4-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="890f4-115">Examples</span></span>

<span data-ttu-id="890f4-116">В следующем примере определяется один ресурс шрифта:</span><span class="sxs-lookup"><span data-stu-id="890f4-116">The following example defines a single font resource:</span></span>

``` syntax
5 FONT  "cmroman.fnt"
```

 

 




