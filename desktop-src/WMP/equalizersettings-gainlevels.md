---
title: ЕКУАЛИЗЕРСЕТТИНГС. Гаинлевелс
description: Атрибут Гаинлевелс указывает или получает уровень усиления диапазона, соответствующий указанному индексу.
ms.assetid: fb70e2ef-4cee-457e-a06b-7a1ae6930986
keywords:
- Проигрыватель Windows Media ЕКУАЛИЗЕРСЕТТИНГС. Гаинлевелс
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevels
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d083ac829582f2abc45837cf441b2f0a565ee03a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694782"
---
# <a name="equalizersettingsgainlevels"></a><span data-ttu-id="b0eaa-104">ЕКУАЛИЗЕРСЕТТИНГС. Гаинлевелс</span><span class="sxs-lookup"><span data-stu-id="b0eaa-104">EQUALIZERSETTINGS.gainLevels</span></span>

<span data-ttu-id="b0eaa-105">Атрибут **гаинлевелс** указывает или получает уровень усиления диапазона, соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="b0eaa-105">The **gainLevels** attribute specifies or retrieves the gain level of the band corresponding to the index provided.</span></span>

``` syntax
        elementID.gainLevels(theBand)
```

## <a name="possible-values"></a><span data-ttu-id="b0eaa-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="b0eaa-106">Possible Values</span></span>

<span data-ttu-id="b0eaa-107">Этот атрибут является **числом** для чтения и записи (**float**) со значением, которое обычно находится в диапазоне от 20 до + 20.</span><span class="sxs-lookup"><span data-stu-id="b0eaa-107">This attribute is a read/write **Number** (**float**) with a value normally ranging from  20 to +20.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0eaa-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0eaa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0eaa-109"><span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*себанд*</span><span class="sxs-lookup"><span data-stu-id="b0eaa-109"><span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*theBand*</span></span>
</dt> <dd>

<span data-ttu-id="b0eaa-110">**Число**(**Long**) от 1 до 10, указывающее индекс полосы.</span><span class="sxs-lookup"><span data-stu-id="b0eaa-110">**Number**(**long**) between 1 and 10 indicating the index of the band.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0eaa-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0eaa-111">Remarks</span></span>

<span data-ttu-id="b0eaa-112">Этот атрибут принимает параметр, но его значение указывается в коде скрипта так же, как и другие значения атрибутов.</span><span class="sxs-lookup"><span data-stu-id="b0eaa-112">This attribute takes a parameter, but its value is specified in script code the same way as other attribute values.</span></span> <span data-ttu-id="b0eaa-113">Он не может быть указан в элементе ЕКУАЛИЗЕРСЕТТИНГС и не может использоваться с атрибутом прослушивания **вмппроп** .</span><span class="sxs-lookup"><span data-stu-id="b0eaa-113">It cannot be specified in the EQUALIZERSETTINGS element, nor can it be used with the **wmpprop** listening attribute.</span></span> <span data-ttu-id="b0eaa-114">Вместо этого для таких ситуаций предоставляются пронумерованные атрибуты уровня прибыли.</span><span class="sxs-lookup"><span data-stu-id="b0eaa-114">Instead, the numbered gain level attributes are provided for these situations.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0eaa-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b0eaa-115">Requirements</span></span>



| <span data-ttu-id="b0eaa-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b0eaa-116">Requirement</span></span> | <span data-ttu-id="b0eaa-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b0eaa-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b0eaa-118">Версия</span><span class="sxs-lookup"><span data-stu-id="b0eaa-118">Version</span></span><br/> | <span data-ttu-id="b0eaa-119">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="b0eaa-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b0eaa-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0eaa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0eaa-121">**ЕКУАЛИЗЕРСЕТТИНГС, элемент**</span><span class="sxs-lookup"><span data-stu-id="b0eaa-121">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="b0eaa-122">**Атрибуты прослушивания**</span><span class="sxs-lookup"><span data-stu-id="b0eaa-122">**Listening Attributes**</span></span>](listening-attributes.md)
</dt> </dl>

 

 





