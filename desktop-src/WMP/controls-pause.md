---
title: Метод Controls. Pause
description: Метод Pause приостанавливает воспроизведение элемента мультимедиа. | Метод Controls. Pause
ms.assetid: 7307a3b2-e5d6-4067-bdb5-38011565142a
keywords:
- приостановить метод проигрыватель Windows Media Player
- приостановить метод проигрыватель Windows Media Player, класс Controls
- Управляет классом проигрывателя Windows Media Player, метод Pause
topic_type:
- apiref
api_name:
- Controls.pause
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 898efb51355a1301bc76717f6d0184d0b30d619d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698899"
---
# <a name="controlspause-method"></a><span data-ttu-id="7e9ef-107">Метод Controls. Pause</span><span class="sxs-lookup"><span data-stu-id="7e9ef-107">Controls.pause method</span></span>

<span data-ttu-id="7e9ef-108">Метод **Pause** приостанавливает воспроизведение элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7e9ef-108">The **pause** method pauses playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e9ef-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e9ef-109">Syntax</span></span>


```JScript
Controls.pause()
```



## <a name="parameters"></a><span data-ttu-id="7e9ef-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e9ef-110">Parameters</span></span>

<span data-ttu-id="7e9ef-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7e9ef-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7e9ef-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e9ef-112">Return value</span></span>

<span data-ttu-id="7e9ef-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7e9ef-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e9ef-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e9ef-114">Remarks</span></span>

<span data-ttu-id="7e9ef-115">При приостановке файла проигрыватель Windows Media не предоставляет никаких системных ресурсов, таких как звуковое устройство.</span><span class="sxs-lookup"><span data-stu-id="7e9ef-115">When a file is paused, Windows Media Player does not give up any system resources, such as the audio device.</span></span>

<span data-ttu-id="7e9ef-116">Невозможно приостановить определенные типы носителей, например динамические потоки.</span><span class="sxs-lookup"><span data-stu-id="7e9ef-116">Certain media types cannot be paused, such as live streams.</span></span> <span data-ttu-id="7e9ef-117">Чтобы определить, можно ли приостановить определенный тип носителя, используйте *элементы управления*. **доступно ("Pause")**.</span><span class="sxs-lookup"><span data-stu-id="7e9ef-117">To determine whether a particular media type can be paused, use *Controls*.**isAvailable('Pause')**.</span></span>

## <a name="examples"></a><span data-ttu-id="7e9ef-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="7e9ef-118">Examples</span></span>

<span data-ttu-id="7e9ef-119">В следующем примере создается HTML-элемент BUTTON, который использует **Pause** для приостановки воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="7e9ef-119">The following example creates an HTML BUTTON element that uses **pause** to pause playback.</span></span> <span data-ttu-id="7e9ef-120">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="7e9ef-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PAUSE"  NAME = "PAUSE"  VALUE = "||"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Pause'))

            /* Pause the Player. */
            Player.controls.pause();
">
```



## <a name="requirements"></a><span data-ttu-id="7e9ef-121">Требования</span><span class="sxs-lookup"><span data-stu-id="7e9ef-121">Requirements</span></span>



| <span data-ttu-id="7e9ef-122">Требование</span><span class="sxs-lookup"><span data-stu-id="7e9ef-122">Requirement</span></span> | <span data-ttu-id="7e9ef-123">Значение</span><span class="sxs-lookup"><span data-stu-id="7e9ef-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7e9ef-124">Версия</span><span class="sxs-lookup"><span data-stu-id="7e9ef-124">Version</span></span><br/> | <span data-ttu-id="7e9ef-125">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="7e9ef-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7e9ef-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7e9ef-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="7e9ef-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e9ef-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e9ef-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e9ef-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e9ef-129">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="7e9ef-129">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="7e9ef-130">**Элементы управления. доступно**</span><span class="sxs-lookup"><span data-stu-id="7e9ef-130">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> </dl>

 

 





