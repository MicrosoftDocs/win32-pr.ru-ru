---
title: Метод Controls. Play
description: Метод Play заставляет текущий элемент мультимедиа начать воспроизведение или возобновить воспроизведение приостановленного элемента.
ms.assetid: 2218a13b-6294-45f5-bb6f-c5a1e433e0c6
keywords:
- воспроизвести метод проигрыватель Windows Media
- метод Play проигрыватель Windows Media Player, класс Controls
- Класс управляет проигрывателем Windows Media Player, методом Play
topic_type:
- apiref
api_name:
- Controls.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea66f3bc4cf01d194dc44bcdf7b7cc838e1f3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698897"
---
# <a name="controlsplay-method"></a><span data-ttu-id="289db-106">Метод Controls. Play</span><span class="sxs-lookup"><span data-stu-id="289db-106">Controls.play method</span></span>

<span data-ttu-id="289db-107">Метод **Play** заставляет текущий элемент мультимедиа начать воспроизведение или возобновить воспроизведение приостановленного элемента.</span><span class="sxs-lookup"><span data-stu-id="289db-107">The **play** method causes the current media item to start playing, or resumes play of a paused item.</span></span>

## <a name="syntax"></a><span data-ttu-id="289db-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="289db-108">Syntax</span></span>


```JScript
Controls.play()
```



## <a name="parameters"></a><span data-ttu-id="289db-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="289db-109">Parameters</span></span>

<span data-ttu-id="289db-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="289db-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="289db-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="289db-111">Return value</span></span>

<span data-ttu-id="289db-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="289db-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="289db-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="289db-113">Remarks</span></span>

<span data-ttu-id="289db-114">Если этот метод вызывается при быстрой пересылке или перемотки, значение *параметров*. **ставка** устанавливается равным 1,0.</span><span class="sxs-lookup"><span data-stu-id="289db-114">If this method is called while fast-forwarding or rewinding, the value of *Settings*.**rate** is set to 1.0.</span></span>

## <a name="examples"></a><span data-ttu-id="289db-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="289db-115">Examples</span></span>

<span data-ttu-id="289db-116">В следующем примере создается HTML-элемент BUTTON, который использует **Play** для воспроизведения текущего элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="289db-116">The following example creates an HTML BUTTON element that uses **play** to play the current media item.</span></span> <span data-ttu-id="289db-117">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="289db-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PLAY"  NAME = "PLAY"  VALUE = "Play"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Play'))

            /* Start playback. */
            Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="289db-118">Требования</span><span class="sxs-lookup"><span data-stu-id="289db-118">Requirements</span></span>



| <span data-ttu-id="289db-119">Требование</span><span class="sxs-lookup"><span data-stu-id="289db-119">Requirement</span></span> | <span data-ttu-id="289db-120">Значение</span><span class="sxs-lookup"><span data-stu-id="289db-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="289db-121">Версия</span><span class="sxs-lookup"><span data-stu-id="289db-121">Version</span></span><br/> | <span data-ttu-id="289db-122">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="289db-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="289db-123">DLL</span><span class="sxs-lookup"><span data-stu-id="289db-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="289db-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="289db-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="289db-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="289db-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="289db-126">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="289db-126">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





