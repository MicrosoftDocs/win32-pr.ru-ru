---
title: ПОЛЗУНок. Фореграундпрогресс
description: Атрибут Фореграундпрогресс указывает или получает текущую положение индикатора выполнения на передний план в процентах от области ползунка.
ms.assetid: 1218ca5a-445c-441b-aa62-74a184a25c2d
keywords:
- ПОЛЗУНок. Фореграундпрогресс Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4597630453444564411d0bcfad8dc6b39914d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657722"
---
# <a name="sliderforegroundprogress"></a><span data-ttu-id="ed654-104">ПОЛЗУНок. Фореграундпрогресс</span><span class="sxs-lookup"><span data-stu-id="ed654-104">SLIDER.foregroundProgress</span></span>

<span data-ttu-id="ed654-105">Атрибут **фореграундпрогресс** указывает или получает текущую положение индикатора выполнения на передний план в процентах от области ползунка.</span><span class="sxs-lookup"><span data-stu-id="ed654-105">The **foregroundProgress** attribute specifies or retrieves the current position of the foreground progress bar as a percentage of the slider area.</span></span>

``` syntax
        elementID.foregroundProgress
```

## <a name="possible-values"></a><span data-ttu-id="ed654-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="ed654-106">Possible Values</span></span>

<span data-ttu-id="ed654-107">Этот атрибут является **числом** для чтения и записи (**float**) в диапазоне от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="ed654-107">This attribute is a read/write **Number** (**float**) ranging from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed654-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed654-108">Remarks</span></span>

<span data-ttu-id="ed654-109">Этот атрибут используется в основном для отслеживания хода загрузки файла мультимедиа при одновременной отслеживании текущей позицией воспроизведения файла с помощью атрибута **value** .</span><span class="sxs-lookup"><span data-stu-id="ed654-109">This attribute is used primarily to track the download progress of a media file while simultaneously tracking the current play position of the file using the **value** attribute.</span></span> <span data-ttu-id="ed654-110">Положение ползунка ограничивается областью выполнения переднего плана.</span><span class="sxs-lookup"><span data-stu-id="ed654-110">The position of the slider thumb is constrained to the area of the foreground progress.</span></span> <span data-ttu-id="ed654-111">Это позволяет интерактивному поиску выполняться только в пределах доступной части загружаемого файла.</span><span class="sxs-lookup"><span data-stu-id="ed654-111">This allows interactive seeking to take place only within the available portion of a downloading file.</span></span>

<span data-ttu-id="ed654-112">Для использования этой функции атрибут **усефореграундпрогресс** должен иметь значение true.</span><span class="sxs-lookup"><span data-stu-id="ed654-112">To use this functionality, the **useForegroundProgress** attribute must be set to true.</span></span>

## <a name="examples"></a><span data-ttu-id="ed654-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="ed654-113">Examples</span></span>


```C++
<SLIDER
  id="seek"
  backgroundColor="blue"
  foregroundColor="red"
  thumbImage="seekthumb.bmp"
  min="0"
  max="wmpprop:player.currentMedia.duration"
  value="wmpprop:player.controls.currentPosition"
  useForegroundProgress="true"
  foregroundProgress="wmpprop:player.network.downloadProgress"
  ondragend="player.controls.currentposition=value"
/>

```



## <a name="requirements"></a><span data-ttu-id="ed654-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ed654-114">Requirements</span></span>



| <span data-ttu-id="ed654-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ed654-115">Requirement</span></span> | <span data-ttu-id="ed654-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ed654-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ed654-117">Версия</span><span class="sxs-lookup"><span data-stu-id="ed654-117">Version</span></span><br/> | <span data-ttu-id="ed654-118">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ed654-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed654-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed654-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed654-120">**Элемент SLIDER**</span><span class="sxs-lookup"><span data-stu-id="ed654-120">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="ed654-121">**SLIDER. min**</span><span class="sxs-lookup"><span data-stu-id="ed654-121">**SLIDER.min**</span></span>](slider-min.md)
</dt> <dt>

[<span data-ttu-id="ed654-122">**SLIDER. Max**</span><span class="sxs-lookup"><span data-stu-id="ed654-122">**SLIDER.max**</span></span>](slider-max.md)
</dt> <dt>

[<span data-ttu-id="ed654-123">**ПОЛЗУНок. Усефореграундпрогресс**</span><span class="sxs-lookup"><span data-stu-id="ed654-123">**SLIDER.useForegroundProgress**</span></span>](slider-useforegroundprogress.md)
</dt> <dt>

[<span data-ttu-id="ed654-124">**ПОЛЗУНок. Value**</span><span class="sxs-lookup"><span data-stu-id="ed654-124">**SLIDER.value**</span></span>](slider-value.md)
</dt> </dl>

 

 





