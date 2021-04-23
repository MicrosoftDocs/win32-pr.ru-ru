---
title: EFFECTs. Алловалл
description: Атрибут Алловалл указывает или получает значение, указывающее, следует ли включать все визуализации, которые находятся в реестре.
ms.assetid: 8552cc06-05b2-4049-ba7d-f6bd770449e0
keywords:
- Effect. Алловалл Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.allowAll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56760021fe34522072677e9524fe6636e519e20f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694720"
---
# <a name="effectsallowall"></a><span data-ttu-id="93940-104">EFFECTs. Алловалл</span><span class="sxs-lookup"><span data-stu-id="93940-104">EFFECTS.allowAll</span></span>

<span data-ttu-id="93940-105">Атрибут **алловалл** указывает или получает значение, указывающее, следует ли включать все визуализации, которые находятся в реестре.</span><span class="sxs-lookup"><span data-stu-id="93940-105">The **allowAll** attribute specifies or retrieves a value indicating whether to include all the visualizations that are in the registry.</span></span>

``` syntax
        elementID.allowAll
```

## <a name="possible-values"></a><span data-ttu-id="93940-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="93940-106">Possible Values</span></span>

<span data-ttu-id="93940-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="93940-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="93940-108">Значение</span><span class="sxs-lookup"><span data-stu-id="93940-108">Value</span></span> | <span data-ttu-id="93940-109">Описание</span><span class="sxs-lookup"><span data-stu-id="93940-109">Description</span></span>                                                         |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="93940-110">true</span><span class="sxs-lookup"><span data-stu-id="93940-110">true</span></span>  | <span data-ttu-id="93940-111">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="93940-111">Default.</span></span> <span data-ttu-id="93940-112">Позволяет выполнять циклическое переключение всех визуализаций в системе пользователя.</span><span class="sxs-lookup"><span data-stu-id="93940-112">Allows cycling of all visualizations on the user's system.</span></span> |
| <span data-ttu-id="93940-113">false</span><span class="sxs-lookup"><span data-stu-id="93940-113">false</span></span> | <span data-ttu-id="93940-114">Ограничивает цикл визуализации до визуализаций, отображаемых в тегах **Effects** .</span><span class="sxs-lookup"><span data-stu-id="93940-114">Limits cycling to visualizations appearing within **EFFECTS** tags.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="93940-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93940-115">Remarks</span></span>

<span data-ttu-id="93940-116">Если этому атрибуту присвоено значение false, то только визуализации, появляющиеся в тегах **Effects** , могут быть циклически передаваться с помощью функции Previous/Next.</span><span class="sxs-lookup"><span data-stu-id="93940-116">If this attribute is set to false, only the visualizations appearing within **EFFECTS** tags can be cycled through using previous/next.</span></span> <span data-ttu-id="93940-117">Если задано значение true, то все визуализации, зарегистрированные в системе пользователя, можно циклически использовать.</span><span class="sxs-lookup"><span data-stu-id="93940-117">If it is set to true, then all visualizations that are registered on the user's system can be cycled through.</span></span> <span data-ttu-id="93940-118">Если задано значение true и вы указываете любые визуализации внутри тегов **Effect** , то атрибуты, указанные в этих тегах, применяются ко всем визуализациям в системе пользователя.</span><span class="sxs-lookup"><span data-stu-id="93940-118">If it is set to true and you specify any visualizations within **EFFECTS** tags, then the attributes specified in these tags are applied to all visualizations on the user's system.</span></span>

## <a name="requirements"></a><span data-ttu-id="93940-119">Требования</span><span class="sxs-lookup"><span data-stu-id="93940-119">Requirements</span></span>



| <span data-ttu-id="93940-120">Требование</span><span class="sxs-lookup"><span data-stu-id="93940-120">Requirement</span></span> | <span data-ttu-id="93940-121">Значение</span><span class="sxs-lookup"><span data-stu-id="93940-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="93940-122">Версия</span><span class="sxs-lookup"><span data-stu-id="93940-122">Version</span></span><br/> | <span data-ttu-id="93940-123">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="93940-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="93940-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93940-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93940-125">**EFFECTs, элемент**</span><span class="sxs-lookup"><span data-stu-id="93940-125">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





