---
title: Controls. Фастфорвард, метод
description: Метод Фастфорвард запускает быстрое воспроизведение элемента мультимедиа в прямом направлении. | Controls. Фастфорвард, метод
ms.assetid: 69cee803-f76b-4a8c-a2c2-1870665afaf9
keywords:
- Фастфорвард метод Windows Media Player
- метод Фастфорвард Windows Media Player, класс Controls
- Класс управляет проигрывателем Windows Media Player, метод Фастфорвард
topic_type:
- apiref
api_name:
- Controls.fastForward
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20d033b8b025955e57a9c3ebed00a6d7a92a666e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694903"
---
# <a name="controlsfastforward-method"></a><span data-ttu-id="8e4cf-107">Controls. Фастфорвард, метод</span><span class="sxs-lookup"><span data-stu-id="8e4cf-107">Controls.fastForward method</span></span>

<span data-ttu-id="8e4cf-108">Метод **фастфорвард** запускает быстрое воспроизведение элемента мультимедиа в прямом направлении.</span><span class="sxs-lookup"><span data-stu-id="8e4cf-108">The **fastForward** method starts fast play of the media item in the forward direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e4cf-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e4cf-109">Syntax</span></span>


```JScript
Controls.fastForward()
```



## <a name="parameters"></a><span data-ttu-id="8e4cf-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e4cf-110">Parameters</span></span>

<span data-ttu-id="8e4cf-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8e4cf-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e4cf-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e4cf-112">Return value</span></span>

<span data-ttu-id="8e4cf-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8e4cf-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e4cf-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e4cf-114">Remarks</span></span>

<span data-ttu-id="8e4cf-115">Метод **фастфорвард** воспроизводит клип назад в пять раз подряд с обычной скоростью.</span><span class="sxs-lookup"><span data-stu-id="8e4cf-115">The **fastForward** method plays the clip back at five times the normal speed.</span></span> <span data-ttu-id="8e4cf-116">При вызове **фастфорвард** изменяется *Настройка параметров*. Свойство **Rate** до 5,0.</span><span class="sxs-lookup"><span data-stu-id="8e4cf-116">Invoking **fastForward** changes the *Settings*.**rate** property to 5.0.</span></span> <span data-ttu-id="8e4cf-117">Если **ставка** впоследствии изменилась или вызывается **Воспроизведение** или **Остановка** , проигрыватель Windows Media прекратит быструю пересылку.</span><span class="sxs-lookup"><span data-stu-id="8e4cf-117">If **rate** is subsequently changed, or if **play** or **stop** is called, Windows Media Player will cease fast forwarding.</span></span>

<span data-ttu-id="8e4cf-118">Метод **фастфорвард** не работает для широковещательных трансляций и определенных типов носителей.</span><span class="sxs-lookup"><span data-stu-id="8e4cf-118">The **fastForward** method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="8e4cf-119">Чтобы определить, можно ли быстро перемотать клип, **вызовите метод «фастфорвард**».</span><span class="sxs-lookup"><span data-stu-id="8e4cf-119">To determine whether you can fast forward in a clip, call **isAvailable**("FastForward").</span></span>

## <a name="examples"></a><span data-ttu-id="8e4cf-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="8e4cf-120">Examples</span></span>

<span data-ttu-id="8e4cf-121">В следующем примере создается HTML-элемент BUTTON, который использует **фастфорвард** для запуска быстрого воспроизведения элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8e4cf-121">The following example creates an HTML BUTTON element that uses **fastForward** to start fast play of the media item.</span></span> <span data-ttu-id="8e4cf-122">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="8e4cf-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "FF"  NAME = "FF"  VALUE = ">>"  

    /* Execute JScript when the BUTTON is clicked. 
       Check first to make sure fast-forward mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastForward'))
        Player.controls.fastForward();
">

```



## <a name="requirements"></a><span data-ttu-id="8e4cf-123">Требования</span><span class="sxs-lookup"><span data-stu-id="8e4cf-123">Requirements</span></span>



| <span data-ttu-id="8e4cf-124">Требование</span><span class="sxs-lookup"><span data-stu-id="8e4cf-124">Requirement</span></span> | <span data-ttu-id="8e4cf-125">Значение</span><span class="sxs-lookup"><span data-stu-id="8e4cf-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8e4cf-126">Версия</span><span class="sxs-lookup"><span data-stu-id="8e4cf-126">Version</span></span><br/> | <span data-ttu-id="8e4cf-127">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="8e4cf-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8e4cf-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8e4cf-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="8e4cf-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e4cf-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e4cf-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e4cf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e4cf-131">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="8e4cf-131">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="8e4cf-132">**Элементы управления. доступно**</span><span class="sxs-lookup"><span data-stu-id="8e4cf-132">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> <dt>

[<span data-ttu-id="8e4cf-133">**Controls. Play**</span><span class="sxs-lookup"><span data-stu-id="8e4cf-133">**Controls.play**</span></span>](controls-play.md)
</dt> <dt>

[<span data-ttu-id="8e4cf-134">**Controls. останавливаться**</span><span class="sxs-lookup"><span data-stu-id="8e4cf-134">**Controls.stop**</span></span>](controls-stop.md)
</dt> <dt>

[<span data-ttu-id="8e4cf-135">**Параметры. rate**</span><span class="sxs-lookup"><span data-stu-id="8e4cf-135">**Settings.rate**</span></span>](settings-rate.md)
</dt> </dl>

 

 





