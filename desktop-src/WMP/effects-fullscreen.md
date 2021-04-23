---
title: ЭФФЕКТЫ. полноэкранный режим
description: Атрибут «полноэкранный режим» указывает или получает значение, указывающее, отображается ли текущая визуализация в полноэкранном режиме. Этот атрибут можно задать только во время выполнения.
ms.assetid: 319b46a4-b6c2-4dda-8285-f12af6836b25
keywords:
- EFFECTs. полноэкранный проигрыватель Windows Media
topic_type:
- apiref
api_name:
- EFFECTS.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e1824e35793a083eb88ea42de0eb8858a4b76f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699103"
---
# <a name="effectsfullscreen"></a><span data-ttu-id="581a9-105">ЭФФЕКТЫ. полноэкранный режим</span><span class="sxs-lookup"><span data-stu-id="581a9-105">EFFECTS.fullScreen</span></span>

<span data-ttu-id="581a9-106">Атрибут « **полноэкранный** режим» указывает или получает значение, указывающее, отображается ли текущая визуализация в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="581a9-106">The **fullScreen** attribute specifies or retrieves a value indicating whether the current visualization is displayed full-screen.</span></span> <span data-ttu-id="581a9-107">Этот атрибут можно задать только во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="581a9-107">This attribute can only be set at run time.</span></span>

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a><span data-ttu-id="581a9-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="581a9-108">Possible Values</span></span>

<span data-ttu-id="581a9-109">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="581a9-109">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="581a9-110">Значение</span><span class="sxs-lookup"><span data-stu-id="581a9-110">Value</span></span> | <span data-ttu-id="581a9-111">Описание</span><span class="sxs-lookup"><span data-stu-id="581a9-111">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="581a9-112">true</span><span class="sxs-lookup"><span data-stu-id="581a9-112">true</span></span>  | <span data-ttu-id="581a9-113">Визуализация отображается в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="581a9-113">Visualization is displayed full-screen.</span></span>              |
| <span data-ttu-id="581a9-114">false</span><span class="sxs-lookup"><span data-stu-id="581a9-114">false</span></span> | <span data-ttu-id="581a9-115">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="581a9-115">Default.</span></span> <span data-ttu-id="581a9-116">Визуализация не отображается в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="581a9-116">Visualization is not displayed full-screen.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="581a9-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="581a9-117">Remarks</span></span>

<span data-ttu-id="581a9-118">Визуализацию можно перевести в полноэкранный режим только при воспроизведении или приостановке мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="581a9-118">A visualization can be put into full-screen mode only while media is playing or paused.</span></span> <span data-ttu-id="581a9-119">Если *проигрыватель*. **куррентмедиа** — видео, должен присутствовать подключаемый модуль видео.</span><span class="sxs-lookup"><span data-stu-id="581a9-119">If *Player*.**currentMedia** is video, a video plug-in must be present.</span></span> <span data-ttu-id="581a9-120">Если это звук, то должен присутствовать подключаемый модуль визуализации, поддерживающий полноэкранный режим отображения.</span><span class="sxs-lookup"><span data-stu-id="581a9-120">If it is audio, a visualization plug-in that supports full-screen display must be present.</span></span>

## <a name="requirements"></a><span data-ttu-id="581a9-121">Требования</span><span class="sxs-lookup"><span data-stu-id="581a9-121">Requirements</span></span>



| <span data-ttu-id="581a9-122">Требование</span><span class="sxs-lookup"><span data-stu-id="581a9-122">Requirement</span></span> | <span data-ttu-id="581a9-123">Значение</span><span class="sxs-lookup"><span data-stu-id="581a9-123">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="581a9-124">Версия</span><span class="sxs-lookup"><span data-stu-id="581a9-124">Version</span></span><br/> | <span data-ttu-id="581a9-125">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="581a9-125">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="581a9-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="581a9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="581a9-127">**EFFECTs, элемент**</span><span class="sxs-lookup"><span data-stu-id="581a9-127">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





