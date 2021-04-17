---
title: Метод Controls. останавливаться
description: Метод Stop останавливает воспроизведение элемента мультимедиа. | Метод Controls. останавливаться
ms.assetid: ace95fde-9c94-4737-88f2-94321cbc687c
keywords:
- метод завершения проигрывателя Windows Media Player
- метод завершения Windows Media Player, класс Controls
- Управляет проигрывателем Windows Media Player, методом завершения
topic_type:
- apiref
api_name:
- Controls.stop
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1ffc581fffbce0a341559e82c6bd196f712149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694941"
---
# <a name="controlsstop-method"></a><span data-ttu-id="d57a7-107">Метод Controls. останавливаться</span><span class="sxs-lookup"><span data-stu-id="d57a7-107">Controls.stop method</span></span>

<span data-ttu-id="d57a7-108">Метод **Stop** останавливает воспроизведение элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d57a7-108">The **stop** method stops playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="d57a7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d57a7-109">Syntax</span></span>


```JScript
Controls.stop()
```



## <a name="parameters"></a><span data-ttu-id="d57a7-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d57a7-110">Parameters</span></span>

<span data-ttu-id="d57a7-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d57a7-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d57a7-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d57a7-112">Return value</span></span>

<span data-ttu-id="d57a7-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d57a7-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d57a7-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d57a7-114">Remarks</span></span>

<span data-ttu-id="d57a7-115">Этот метод заставляет проигрыватель Windows Media освобождать любые системные ресурсы, которые он использует, например звуковое устройство.</span><span class="sxs-lookup"><span data-stu-id="d57a7-115">This method causes Windows Media Player to release any system resources it is using, such as the audio device.</span></span> <span data-ttu-id="d57a7-116">Однако текущий элемент мультимедиа не освобожден.</span><span class="sxs-lookup"><span data-stu-id="d57a7-116">The current media item, however, is not released.</span></span>

<span data-ttu-id="d57a7-117">Когда игрок остановлен, запись начнется на начало.</span><span class="sxs-lookup"><span data-stu-id="d57a7-117">When the player is stopped, the track rewinds to the beginning.</span></span> <span data-ttu-id="d57a7-118">Вызов **Play** начнет воспроизведение клипа с самого начала.</span><span class="sxs-lookup"><span data-stu-id="d57a7-118">Calling **play** will then begin playback of the clip from the beginning.</span></span> <span data-ttu-id="d57a7-119">Чтобы остановить операцию воспроизведения без изменения текущей позицией, используйте метод **Pause** .</span><span class="sxs-lookup"><span data-stu-id="d57a7-119">To halt a play operation without changing the current position, use the **pause** method.</span></span>

## <a name="examples"></a><span data-ttu-id="d57a7-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="d57a7-120">Examples</span></span>

<span data-ttu-id="d57a7-121">В следующем примере создается HTML-элемент BUTTON, который **использует метод «приостанавливает»** для отмены воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d57a7-121">The following example creates an HTML BUTTON element that uses **stop** to stop playback.</span></span> <span data-ttu-id="d57a7-122">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="d57a7-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "STOP"  NAME = "STOP"  VALUE = "Stop"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Stop'))

            /* Stop the Player. */
            Player.controls.stop();
">

```



## <a name="requirements"></a><span data-ttu-id="d57a7-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d57a7-123">Requirements</span></span>



| <span data-ttu-id="d57a7-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d57a7-124">Requirement</span></span> | <span data-ttu-id="d57a7-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d57a7-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d57a7-126">Версия</span><span class="sxs-lookup"><span data-stu-id="d57a7-126">Version</span></span><br/> | <span data-ttu-id="d57a7-127">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="d57a7-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d57a7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d57a7-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="d57a7-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d57a7-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d57a7-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d57a7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d57a7-131">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="d57a7-131">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="d57a7-132">**Controls. Next**</span><span class="sxs-lookup"><span data-stu-id="d57a7-132">**Controls.next**</span></span>](controls-next.md)
</dt> <dt>

[<span data-ttu-id="d57a7-133">**Controls. Pause**</span><span class="sxs-lookup"><span data-stu-id="d57a7-133">**Controls.pause**</span></span>](controls-pause.md)
</dt> <dt>

[<span data-ttu-id="d57a7-134">**Controls. Previous**</span><span class="sxs-lookup"><span data-stu-id="d57a7-134">**Controls.previous**</span></span>](controls-previous.md)
</dt> </dl>

 

 





