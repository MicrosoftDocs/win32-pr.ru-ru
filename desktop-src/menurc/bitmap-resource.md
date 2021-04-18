---
title: Ресурс ТОЧЕЧного рисунка
description: Определяет точечный рисунок, используемый приложением на экране экрана или в виде элемента в меню или элементе управления.
ms.assetid: 2db2f7f0-735f-4aac-9813-c04a2f7788b2
keywords:
- Меню ресурсов ТОЧЕЧных РИСУНКов и другие ресурсы
topic_type:
- apiref
api_name:
- BITMAP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5bed33fb66d9deb85e1f25165f3f7a0f664961
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412856"
---
# <a name="bitmap-resource"></a><span data-ttu-id="a8182-104">Ресурс ТОЧЕЧного рисунка</span><span class="sxs-lookup"><span data-stu-id="a8182-104">BITMAP resource</span></span>

<span data-ttu-id="a8182-105">Определяет точечный рисунок, используемый приложением на экране экрана или в виде элемента в меню или элементе управления.</span><span class="sxs-lookup"><span data-stu-id="a8182-105">Defines a bitmap that an application uses in its screen display or as an item in a menu or control.</span></span>

``` syntax
nameID BITMAP filename
```

## <a name="parameters"></a><span data-ttu-id="a8182-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8182-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8182-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="a8182-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="a8182-108">Уникальное имя или 16-разрядное целочисленное значение без знака, идентифицирующее ресурс.</span><span class="sxs-lookup"><span data-stu-id="a8182-108">Unique name or a 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="a8182-109"><span id="filename"></span><span id="FILENAME"></span>*файлов*</span><span class="sxs-lookup"><span data-stu-id="a8182-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="a8182-110">Имя файла, содержащего ресурс.</span><span class="sxs-lookup"><span data-stu-id="a8182-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="a8182-111">Имя должно быть допустимым именем файла; Он должен быть полным путем, если файл не находится в текущем рабочем каталоге.</span><span class="sxs-lookup"><span data-stu-id="a8182-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="a8182-112">Путь должен представлять собой строку в кавычках.</span><span class="sxs-lookup"><span data-stu-id="a8182-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="a8182-113">Для обратной совместимости также поддерживаются некоторые атрибуты.</span><span class="sxs-lookup"><span data-stu-id="a8182-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="a8182-114">Дополнительные сведения см. в разделе [Общие атрибуты ресурсов](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="a8182-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a8182-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="a8182-115">Examples</span></span>

<span data-ttu-id="a8182-116">В следующем примере определяются два ресурса точечного рисунка:</span><span class="sxs-lookup"><span data-stu-id="a8182-116">The following example defines two bitmap resources:</span></span>

``` syntax
disk1   BITMAP "disk.bmp"
12      BITMAP "diskette.bmp"
```

## <a name="see-also"></a><span data-ttu-id="a8182-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8182-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8182-118">Использование точечных рисунков</span><span class="sxs-lookup"><span data-stu-id="a8182-118">Using Bitmaps</span></span>](/windows/desktop/gdi/using-bitmaps)
</dt> <dt>

[<span data-ttu-id="a8182-119">**лоадбитмап**</span><span class="sxs-lookup"><span data-stu-id="a8182-119">**LoadBitmap**</span></span>](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)
</dt> <dt>

[<span data-ttu-id="a8182-120">**лоадимаже**</span><span class="sxs-lookup"><span data-stu-id="a8182-120">**LoadImage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
</dt> </dl>

 

 