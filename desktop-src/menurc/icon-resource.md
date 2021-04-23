---
title: Ресурс ЗНАЧКа
description: Определяет точечный рисунок, определяющий форму значка, который будет использоваться для данного приложения или анимированного значка.
ms.assetid: a8e3205e-e17a-4daf-a599-4dc89cb1e640
keywords:
- ЗНАЧОК меню ресурсов и других ресурсов
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f762c4f4b459d51a0243a9cdbd7367deda7b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533119"
---
# <a name="icon-resource"></a><span data-ttu-id="05b99-104">Ресурс ЗНАЧКа</span><span class="sxs-lookup"><span data-stu-id="05b99-104">ICON resource</span></span>

<span data-ttu-id="05b99-105">Определяет точечный рисунок, определяющий форму значка, который будет использоваться для данного приложения или анимированного значка.</span><span class="sxs-lookup"><span data-stu-id="05b99-105">Defines a bitmap that defines the shape of the icon to be used for a given application or an animated icon.</span></span>

``` syntax
nameID ICON filename
```

## <a name="parameters"></a><span data-ttu-id="05b99-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="05b99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05b99-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="05b99-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="05b99-108">Уникальное имя или 16-разрядное целочисленное значение без знака, идентифицирующее ресурс.</span><span class="sxs-lookup"><span data-stu-id="05b99-108">Unique name or a 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="05b99-109"><span id="filename"></span><span id="FILENAME"></span>*файлов*</span><span class="sxs-lookup"><span data-stu-id="05b99-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="05b99-110">Имя файла, содержащего ресурс.</span><span class="sxs-lookup"><span data-stu-id="05b99-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="05b99-111">Имя должно быть допустимым именем файла; Он должен быть полным путем, если файл не находится в текущем рабочем каталоге.</span><span class="sxs-lookup"><span data-stu-id="05b99-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="05b99-112">Путь должен представлять собой строку в кавычках.</span><span class="sxs-lookup"><span data-stu-id="05b99-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="05b99-113">Для обратной совместимости также поддерживаются некоторые атрибуты.</span><span class="sxs-lookup"><span data-stu-id="05b99-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="05b99-114">Дополнительные сведения см. в разделе [Общие атрибуты ресурсов](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="05b99-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="05b99-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05b99-115">Remarks</span></span>

<span data-ttu-id="05b99-116">Ресурсы значков и курсоров могут содержать более одного изображения.</span><span class="sxs-lookup"><span data-stu-id="05b99-116">Icon and cursor resources can contain more than one image.</span></span>

## <a name="examples"></a><span data-ttu-id="05b99-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="05b99-117">Examples</span></span>

<span data-ttu-id="05b99-118">В следующем примере определяются два ресурса значка:</span><span class="sxs-lookup"><span data-stu-id="05b99-118">The following example defines two icon resources:</span></span>

``` syntax
desk1   ICON "desk.ico"
11      ICON "custom.ico"
```

## <a name="see-also"></a><span data-ttu-id="05b99-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05b99-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05b99-120">Использование значков</span><span class="sxs-lookup"><span data-stu-id="05b99-120">Using Icons</span></span>](./using-icons.md)
</dt> </dl>

 

 