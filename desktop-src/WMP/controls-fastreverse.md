---
title: Controls. Фастреверсе, метод
description: Метод Фастреверсе запускает быстрое сканирование элемента мультимедиа в обратном направлении.
ms.assetid: 4fc61739-9006-4d62-b2c1-2b8e8830f2d9
keywords:
- Фастреверсе метод Windows Media Player
- метод Фастреверсе Windows Media Player, класс Controls
- Класс управляет проигрывателем Windows Media Player, метод Фастреверсе
topic_type:
- apiref
api_name:
- Controls.fastReverse
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e5a63c4299bf08c25e36e2d61924f3fb171792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694902"
---
# <a name="controlsfastreverse-method"></a><span data-ttu-id="b72cc-106">Controls. Фастреверсе, метод</span><span class="sxs-lookup"><span data-stu-id="b72cc-106">Controls.fastReverse method</span></span>

<span data-ttu-id="b72cc-107">Метод **фастреверсе** запускает быстрое сканирование элемента мультимедиа в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="b72cc-107">The **fastReverse** method starts fast scanning of the media item in the reverse direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="b72cc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b72cc-108">Syntax</span></span>


```JScript
Controls.fastReverse()
```



## <a name="parameters"></a><span data-ttu-id="b72cc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b72cc-109">Parameters</span></span>

<span data-ttu-id="b72cc-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b72cc-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b72cc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b72cc-111">Return value</span></span>

<span data-ttu-id="b72cc-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b72cc-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b72cc-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b72cc-113">Remarks</span></span>

<span data-ttu-id="b72cc-114">Метод **фастреверсе** просматривает клип в обратную, в пять раз превышающую нормальную скорость, отображая только ключевые кадры, если это видеофайл.</span><span class="sxs-lookup"><span data-stu-id="b72cc-114">The **fastReverse** method scans the clip in reverse at five times the normal speed, displaying only the key frames if it is a video file.</span></span> <span data-ttu-id="b72cc-115">При вызове **фастреверсе** изменяется *Настройка параметров*. Свойство **Rate** до 5,0.</span><span class="sxs-lookup"><span data-stu-id="b72cc-115">Invoking **fastReverse** changes the *Settings*.**rate** property to  5.0.</span></span> <span data-ttu-id="b72cc-116">Если **ставка** впоследствии изменилась или вызывается **Воспроизведение** или **прекращение** , проигрыватель Windows Media прекратит обратный.</span><span class="sxs-lookup"><span data-stu-id="b72cc-116">If **rate** is subsequently changed, or if **play** or **stop** is called, Windows Media Player will cease fast reverse.</span></span>

<span data-ttu-id="b72cc-117">Если элемент является частью списка воспроизведения, **фастреверсе** останавливается в начале текущей записи. Например, если параметр Track 3 находится в **фастреверсе**, то при достижении начала Track 3 проигрыватель Windows Media не будет переходить к разделу Track 2.</span><span class="sxs-lookup"><span data-stu-id="b72cc-117">If the item is part of a playlist, **fastReverse** stops at the beginning of the current track. For instance, if track 3 is in **fastReverse**, when the beginning of track 3 is reached, Windows Media Player will not go to track 2.</span></span> <span data-ttu-id="b72cc-118">При вызове **фастреверсе** Счетчик воспроизведения не увеличивается.</span><span class="sxs-lookup"><span data-stu-id="b72cc-118">The play count is not incremented when calling **fastReverse**.</span></span>

<span data-ttu-id="b72cc-119">Если вы вызываете **фастфорвард** , когда действует **фастреверсе** , **фастреверсе** будет остановлена, а **фастфорвард** начнется.</span><span class="sxs-lookup"><span data-stu-id="b72cc-119">If you call **fastForward** while **fastReverse** is in effect, **fastReverse** will be stopped and **fastForward** will begin.</span></span>

<span data-ttu-id="b72cc-120">Этот метод не работает для широковещательных трансляций и определенных типов носителей.</span><span class="sxs-lookup"><span data-stu-id="b72cc-120">This method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="b72cc-121">Чтобы определить, можно ли использовать функцию быстрого просмотра клипа, вызовите **метод «фастреверсе**».</span><span class="sxs-lookup"><span data-stu-id="b72cc-121">To determine whether you can use fast reverse in a clip, call **isAvailable**("FastReverse").</span></span>

## <a name="examples"></a><span data-ttu-id="b72cc-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="b72cc-122">Examples</span></span>

<span data-ttu-id="b72cc-123">В следующем примере создается HTML-элемент BUTTON, который использует **фастреверсе** для запуска быстрого воспроизведения элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b72cc-123">The following example creates an HTML BUTTON element that uses **fastReverse** to start fast-reverse play of the media item.</span></span> <span data-ttu-id="b72cc-124">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="b72cc-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "REW"  NAME = "REW"  VALUE = "<<"  

    /* Run JScript when the BUTTON is clicked. 
       Check first to make sure fast-reverse mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastReverse'))
        Player.controls.fastReverse();
">
```



## <a name="requirements"></a><span data-ttu-id="b72cc-125">Требования</span><span class="sxs-lookup"><span data-stu-id="b72cc-125">Requirements</span></span>



| <span data-ttu-id="b72cc-126">Требование</span><span class="sxs-lookup"><span data-stu-id="b72cc-126">Requirement</span></span> | <span data-ttu-id="b72cc-127">Значение</span><span class="sxs-lookup"><span data-stu-id="b72cc-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b72cc-128">Версия</span><span class="sxs-lookup"><span data-stu-id="b72cc-128">Version</span></span><br/> | <span data-ttu-id="b72cc-129">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="b72cc-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b72cc-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b72cc-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="b72cc-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b72cc-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b72cc-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b72cc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b72cc-133">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="b72cc-133">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="b72cc-134">**Controls. Фастфорвард**</span><span class="sxs-lookup"><span data-stu-id="b72cc-134">**Controls.fastForward**</span></span>](controls-fastforward.md)
</dt> <dt>

[<span data-ttu-id="b72cc-135">**Элементы управления. доступно**</span><span class="sxs-lookup"><span data-stu-id="b72cc-135">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> <dt>

[<span data-ttu-id="b72cc-136">**Controls. Play**</span><span class="sxs-lookup"><span data-stu-id="b72cc-136">**Controls.play**</span></span>](controls-play.md)
</dt> <dt>

[<span data-ttu-id="b72cc-137">**Controls. останавливаться**</span><span class="sxs-lookup"><span data-stu-id="b72cc-137">**Controls.stop**</span></span>](controls-stop.md)
</dt> <dt>

[<span data-ttu-id="b72cc-138">**Параметры. rate**</span><span class="sxs-lookup"><span data-stu-id="b72cc-138">**Settings.rate**</span></span>](settings-rate.md)
</dt> </dl>

 

 





