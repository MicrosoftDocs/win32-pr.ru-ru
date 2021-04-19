---
title: ВИДЕО. полноэкранный режим
description: Атрибут «полный экран» указывает или получает значение, указывающее, отображается ли видео в полноэкранном режиме.
ms.assetid: de74d95a-31a2-4f65-811c-4e8018ee484a
keywords:
- ВИДЕО. полноэкранный проигрыватель Windows Media
topic_type:
- apiref
api_name:
- VIDEO.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c27fa1bde6437b55689494751410145995862d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708362"
---
# <a name="videofullscreen"></a><span data-ttu-id="58f47-104">ВИДЕО. полноэкранный режим</span><span class="sxs-lookup"><span data-stu-id="58f47-104">VIDEO.fullScreen</span></span>

<span data-ttu-id="58f47-105">Атрибут **«полный экран» указывает** или получает значение, указывающее, отображается ли видео в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="58f47-105">The **fullScreen** attribute specifies or retrieves a value indicating whether the video is displayed in full-screen mode.</span></span>

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a><span data-ttu-id="58f47-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="58f47-106">Possible Values</span></span>

<span data-ttu-id="58f47-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="58f47-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="58f47-108">Значение</span><span class="sxs-lookup"><span data-stu-id="58f47-108">Value</span></span> | <span data-ttu-id="58f47-109">Описание</span><span class="sxs-lookup"><span data-stu-id="58f47-109">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="58f47-110">true</span><span class="sxs-lookup"><span data-stu-id="58f47-110">true</span></span>  | <span data-ttu-id="58f47-111">Видео отображается в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="58f47-111">Video displays in full-screen mode.</span></span>                  |
| <span data-ttu-id="58f47-112">false</span><span class="sxs-lookup"><span data-stu-id="58f47-112">false</span></span> | <span data-ttu-id="58f47-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="58f47-113">Default.</span></span> <span data-ttu-id="58f47-114">Видео не отображается в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="58f47-114">Video does not display in full-screen mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="58f47-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58f47-115">Remarks</span></span>

<span data-ttu-id="58f47-116">Это свойство может быть задано только во время выполнения после загрузки файла.</span><span class="sxs-lookup"><span data-stu-id="58f47-116">This property can be specified only at run time, after a file has been loaded.</span></span> <span data-ttu-id="58f47-117">Поэтому он должен быть установлен в обработчике событий скрипта.</span><span class="sxs-lookup"><span data-stu-id="58f47-117">It must therefore be set within a script event handler.</span></span> <span data-ttu-id="58f47-118">Для возврата к нормальному просмотру используется управляющая кнопка.</span><span class="sxs-lookup"><span data-stu-id="58f47-118">The escape button is used to return to normal viewing.</span></span>

## <a name="requirements"></a><span data-ttu-id="58f47-119">Требования</span><span class="sxs-lookup"><span data-stu-id="58f47-119">Requirements</span></span>



| <span data-ttu-id="58f47-120">Требование</span><span class="sxs-lookup"><span data-stu-id="58f47-120">Requirement</span></span> | <span data-ttu-id="58f47-121">Значение</span><span class="sxs-lookup"><span data-stu-id="58f47-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="58f47-122">Версия</span><span class="sxs-lookup"><span data-stu-id="58f47-122">Version</span></span><br/> | <span data-ttu-id="58f47-123">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="58f47-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="58f47-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58f47-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58f47-125">**Элемент VIDEO**</span><span class="sxs-lookup"><span data-stu-id="58f47-125">**VIDEO Element**</span></span>](video-element.md)
</dt> <dt>

[<span data-ttu-id="58f47-126">**ВИДЕО. Маинтаинаспектратио**</span><span class="sxs-lookup"><span data-stu-id="58f47-126">**VIDEO.maintainAspectRatio**</span></span>](video-maintainaspectratio.md)
</dt> <dt>

[<span data-ttu-id="58f47-127">**ВИДЕО. Шринктофит**</span><span class="sxs-lookup"><span data-stu-id="58f47-127">**VIDEO.shrinkToFit**</span></span>](video-shrinktofit.md)
</dt> <dt>

[<span data-ttu-id="58f47-128">**ВИДЕО. Стретчтофит**</span><span class="sxs-lookup"><span data-stu-id="58f47-128">**VIDEO.stretchToFit**</span></span>](video-stretchtofit.md)
</dt> </dl>

 

 





