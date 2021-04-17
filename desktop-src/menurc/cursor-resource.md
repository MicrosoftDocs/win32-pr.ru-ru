---
title: Ресурс КУРСОРа
description: Определяет точечный рисунок, определяющий форму курсора на экране экрана или анимированном курсоре.
ms.assetid: c087abca-5502-4625-8c9b-464e1718571f
keywords:
- Меню ресурсов КУРСОРа и другие ресурсы
topic_type:
- apiref
api_name:
- CURSOR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594f406420b3b18f88b8890ca4248345ba77fa8e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105672267"
---
# <a name="cursor-resource"></a><span data-ttu-id="ca5f7-104">Ресурс КУРСОРа</span><span class="sxs-lookup"><span data-stu-id="ca5f7-104">CURSOR resource</span></span>

<span data-ttu-id="ca5f7-105">Определяет точечный рисунок, определяющий форму курсора на экране экрана или анимированном курсоре.</span><span class="sxs-lookup"><span data-stu-id="ca5f7-105">Defines a bitmap that defines the shape of the cursor on the display screen or an animated cursor.</span></span>

``` syntax
nameID CURSOR filename
```

## <a name="parameters"></a><span data-ttu-id="ca5f7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca5f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca5f7-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="ca5f7-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="ca5f7-108">Уникальное имя или 16-разрядное целое число без знака, определяющее ресурс.</span><span class="sxs-lookup"><span data-stu-id="ca5f7-108">Unique name or a 16-bit unsigned integer identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="ca5f7-109"><span id="filename"></span><span id="FILENAME"></span>*файлов*</span><span class="sxs-lookup"><span data-stu-id="ca5f7-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="ca5f7-110">Имя файла, содержащего ресурс.</span><span class="sxs-lookup"><span data-stu-id="ca5f7-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="ca5f7-111">Имя должно быть допустимым именем файла; Он должен быть полным путем, если файл не находится в текущем рабочем каталоге.</span><span class="sxs-lookup"><span data-stu-id="ca5f7-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="ca5f7-112">Путь должен представлять собой строку в кавычках.</span><span class="sxs-lookup"><span data-stu-id="ca5f7-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="ca5f7-113">Для обратной совместимости также поддерживаются некоторые атрибуты.</span><span class="sxs-lookup"><span data-stu-id="ca5f7-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="ca5f7-114">Дополнительные сведения см. в разделе [Общие атрибуты ресурсов](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="ca5f7-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ca5f7-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca5f7-115">Remarks</span></span>

<span data-ttu-id="ca5f7-116">Ресурсы значков и курсоров могут содержать более одного изображения.</span><span class="sxs-lookup"><span data-stu-id="ca5f7-116">Icon and cursor resources can contain more than one image.</span></span>

## <a name="examples"></a><span data-ttu-id="ca5f7-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="ca5f7-117">Examples</span></span>

<span data-ttu-id="ca5f7-118">В следующем примере определяются два ресурса курсора: по имени (cursor1), а другое по номеру (2):</span><span class="sxs-lookup"><span data-stu-id="ca5f7-118">The following example defines two cursor resources; one by name (cursor1) and the other by number (2):</span></span>

``` syntax
cursor1 CURSOR "bullseye.cur"
2       CURSOR "d:\\cursor\\arrow.cur" 
```

## <a name="see-also"></a><span data-ttu-id="ca5f7-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca5f7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca5f7-120">Использование курсоров</span><span class="sxs-lookup"><span data-stu-id="ca5f7-120">Using Cursors</span></span>](./using-cursors.md)
</dt> </dl>

 

 