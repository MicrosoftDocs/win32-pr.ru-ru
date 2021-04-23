---
title: COLUMN. Колумнресиземоде
description: Атрибут Колумнресиземоде указывает или получает режим изменения размера для этого столбца.
ms.assetid: 95ece2a3-20a6-4b9d-a2eb-fc69fc612f29
keywords:
- Колумнресиземоде Windows Media Player
topic_type:
- apiref
api_name:
- COLUMN.columnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d17b1a2edd878fb15e69c595e3c061c1963a5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695005"
---
# <a name="columncolumnresizemode"></a><span data-ttu-id="9f35a-104">COLUMN. Колумнресиземоде</span><span class="sxs-lookup"><span data-stu-id="9f35a-104">COLUMN.columnResizeMode</span></span>

<span data-ttu-id="9f35a-105">Атрибут **колумнресиземоде** указывает или получает режим изменения размера для этого столбца.</span><span class="sxs-lookup"><span data-stu-id="9f35a-105">The **columnResizeMode** attribute specifies or retrieves the resize mode for this column.</span></span>

``` syntax
        elementID.columnResizeMode
```

## <a name="possible-values"></a><span data-ttu-id="9f35a-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="9f35a-106">Possible Values</span></span>

<span data-ttu-id="9f35a-107">Этот атрибут является **строкой** для чтения и записи, содержащей одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9f35a-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="9f35a-108">Значение</span><span class="sxs-lookup"><span data-stu-id="9f35a-108">Value</span></span>          | <span data-ttu-id="9f35a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="9f35a-109">Description</span></span>                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f35a-110">аутосизехеадер</span><span class="sxs-lookup"><span data-stu-id="9f35a-110">AutosizeHeader</span></span> | <span data-ttu-id="9f35a-111">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9f35a-111">Default.</span></span> <span data-ttu-id="9f35a-112">Столбец изменяется в соответствии со всеми данными в столбце и в заголовке.</span><span class="sxs-lookup"><span data-stu-id="9f35a-112">The column resizes to accommodate all data in both the column and the header.</span></span>                         |
| <span data-ttu-id="9f35a-113">аутосизедата</span><span class="sxs-lookup"><span data-stu-id="9f35a-113">AutosizeData</span></span>   | <span data-ttu-id="9f35a-114">Столбец изменяется в соответствии со всеми данными в столбце.</span><span class="sxs-lookup"><span data-stu-id="9f35a-114">The column resizes to accommodate all data in the column only.</span></span>                                                 |
| <span data-ttu-id="9f35a-115">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="9f35a-115">Fixed</span></span>          | <span data-ttu-id="9f35a-116">Столбец имеет фиксированный размер.</span><span class="sxs-lookup"><span data-stu-id="9f35a-116">The column is a fixed size.</span></span>                                                                                    |
| <span data-ttu-id="9f35a-117">Растягивается</span><span class="sxs-lookup"><span data-stu-id="9f35a-117">Stretches</span></span>      | <span data-ttu-id="9f35a-118">Размер столбца изменяется для использования оставшегося пространства в элементе управления **списка воспроизведения** после изменения размера всех остальных столбцов.</span><span class="sxs-lookup"><span data-stu-id="9f35a-118">The column resizes to use the remaining space in the **PLAYLIST** control after all other columns are resized.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="9f35a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="9f35a-119">Requirements</span></span>



| <span data-ttu-id="9f35a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="9f35a-120">Requirement</span></span> | <span data-ttu-id="9f35a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="9f35a-121">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="9f35a-122">Версия</span><span class="sxs-lookup"><span data-stu-id="9f35a-122">Version</span></span><br/> | <span data-ttu-id="9f35a-123">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9f35a-123">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9f35a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f35a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f35a-125">**COLUMN, элемент**</span><span class="sxs-lookup"><span data-stu-id="9f35a-125">**COLUMN Element**</span></span>](column-element.md)
</dt> </dl>

 

 





