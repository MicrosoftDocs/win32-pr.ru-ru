---
title: сикслидер
description: Это Стандартный ПОЛЗУНок со следующими значениями по умолчанию. | сикслидер
ms.assetid: 9fdb0f70-e5ce-4dbc-aeba-44fa0e2c9b3c
keywords:
- СИКСЛИДЕР Windows Media Player
topic_type:
- apiref
api_name:
- SEEKSLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59808fa7c41acfcc28b715362b8724c7f113faee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648048"
---
# <a name="seekslider"></a><span data-ttu-id="6f7e1-105">сикслидер</span><span class="sxs-lookup"><span data-stu-id="6f7e1-105">SEEKSLIDER</span></span>

<span data-ttu-id="6f7e1-106">Это Стандартный **ползунок** со следующими значениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6f7e1-106">This is a predefined **SLIDER** with the following default values.</span></span>

``` syntax
toolTip="Seek"
foregroundProgress="wmpprop:player.network.downloadProgress"
max="wmpprop:player.currentMedia.duration"
min="0"
value="wmpprop:player.controls.currentPosition"
onDragEnd="jscript:player.controls.currentPosition=value;"
useForegroundProgress="true"
```

## <a name="remarks"></a><span data-ttu-id="6f7e1-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f7e1-107">Remarks</span></span>

<span data-ttu-id="6f7e1-108">При этом создается элемент управления " **ползунок** ", который ищет файл мультимедиа в любое положение.</span><span class="sxs-lookup"><span data-stu-id="6f7e1-108">This creates a **SLIDER** control that seeks the media file to any position.</span></span> <span data-ttu-id="6f7e1-109">Всплывающие подсказки локализованы.</span><span class="sxs-lookup"><span data-stu-id="6f7e1-109">The ToolTips are localized.</span></span> <span data-ttu-id="6f7e1-110">Все свойства этого **ползунка** можно переопределить, явно указав их.</span><span class="sxs-lookup"><span data-stu-id="6f7e1-110">All properties of this **SLIDER** can be overridden by explicitly specifying them.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f7e1-111">Требования</span><span class="sxs-lookup"><span data-stu-id="6f7e1-111">Requirements</span></span>



| <span data-ttu-id="6f7e1-112">Требование</span><span class="sxs-lookup"><span data-stu-id="6f7e1-112">Requirement</span></span> | <span data-ttu-id="6f7e1-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6f7e1-113">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="6f7e1-114">Версия</span><span class="sxs-lookup"><span data-stu-id="6f7e1-114">Version</span></span><br/> | <span data-ttu-id="6f7e1-115">Проигрыватель Windows Media 7,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="6f7e1-115">Windows Media Player 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6f7e1-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f7e1-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f7e1-117">**Элемент SLIDER**</span><span class="sxs-lookup"><span data-stu-id="6f7e1-117">**SLIDER Element**</span></span>](slider-element.md)
</dt> </dl>

 

 





