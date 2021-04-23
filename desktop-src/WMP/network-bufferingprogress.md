---
title: Network. Буфферингпрогресс
description: Свойство Буфферингпрогресс извлекает процент завершенной буферизации.
ms.assetid: d604159b-7c42-47f8-8085-53f859f24703
keywords:
- Проигрыватель Windows Media Network. Буфферингпрогресс
topic_type:
- apiref
api_name:
- Network.bufferingProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e3a4f37f8f6b8ffe8ff93ca72b0c9551d7e314
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704214"
---
# <a name="networkbufferingprogress"></a><span data-ttu-id="3afff-104">Network. Буфферингпрогресс</span><span class="sxs-lookup"><span data-stu-id="3afff-104">Network.bufferingProgress</span></span>

<span data-ttu-id="3afff-105">Свойство **буфферингпрогресс** извлекает процент завершенной буферизации.</span><span class="sxs-lookup"><span data-stu-id="3afff-105">The **bufferingProgress** property retrieves the percentage of buffering completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3afff-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3afff-106">Syntax</span></span>

<span data-ttu-id="3afff-107">*проигрыватель*. *сеть*. **буфферингпрогресс**</span><span class="sxs-lookup"><span data-stu-id="3afff-107">*player*.*network*.**bufferingProgress**</span></span>

## <a name="possible-values"></a><span data-ttu-id="3afff-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="3afff-108">Possible Values</span></span>

<span data-ttu-id="3afff-109">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="3afff-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="3afff-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3afff-110">Remarks</span></span>

<span data-ttu-id="3afff-111">Каждый раз, когда воспроизведение останавливается и перезапускается, это свойство устанавливается в нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="3afff-111">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="3afff-112">Если воспроизведение приостановлено, оно не сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="3afff-112">It is not reset if playback is paused.</span></span>

<span data-ttu-id="3afff-113">Буферизация применяется только к потоковой передаче содержимого.</span><span class="sxs-lookup"><span data-stu-id="3afff-113">Buffering only applies to streaming content.</span></span> <span data-ttu-id="3afff-114">Это свойство возвращает действительные сведения только во время выполнения, когда *игрок*. Задано свойство **URL-адреса** .</span><span class="sxs-lookup"><span data-stu-id="3afff-114">This property returns valid information only during run time, when the *Player*.**URL** property is set.</span></span>

<span data-ttu-id="3afff-115">Чтобы определить время запуска или остановки буферизации, используйте событие *Player*. \* \* \* \* буферизация \* \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="3afff-115">Use the *Player*.\*\*\*\*Buffering\*\*\*\* event to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="3afff-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="3afff-116">Examples</span></span>

<span data-ttu-id="3afff-117">В следующем примере JScript используется *Network*. **буфферингпрогресс** для вывода процента завершения буферизации.</span><span class="sxs-lookup"><span data-stu-id="3afff-117">The following JScript example uses *Network*.**bufferingProgress** to display the percentage of buffering completed.</span></span> <span data-ttu-id="3afff-118">Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = BP.</span><span class="sxs-lookup"><span data-stu-id="3afff-118">The information is displayed in an HTML DIV created with ID = "BP".</span></span> <span data-ttu-id="3afff-119">В примере для обновления экрана используется таймер с интервалом в 1 секунду.</span><span class="sxs-lookup"><span data-stu-id="3afff-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="3afff-120">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="3afff-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.

   // Test whether buffering has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display every second.
      idI = window.setInterval("UpdateBP()", 1000);
   }

   else{
      // Buffering is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateBP(){
   BP.innerHTML = "";
   BP.innerHTML = "Buffering progress: " + Player.network.bufferingProgress;
   BP.innerHTML += " percent complete";
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="3afff-121">Требования</span><span class="sxs-lookup"><span data-stu-id="3afff-121">Requirements</span></span>



| <span data-ttu-id="3afff-122">Требование</span><span class="sxs-lookup"><span data-stu-id="3afff-122">Requirement</span></span> | <span data-ttu-id="3afff-123">Значение</span><span class="sxs-lookup"><span data-stu-id="3afff-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3afff-124">Версия</span><span class="sxs-lookup"><span data-stu-id="3afff-124">Version</span></span><br/> | <span data-ttu-id="3afff-125">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="3afff-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3afff-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3afff-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="3afff-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3afff-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3afff-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3afff-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3afff-129">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="3afff-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="3afff-130">**Событие проигрывателя. буферизация**</span><span class="sxs-lookup"><span data-stu-id="3afff-130">**Player.Buffering Event**</span></span>](player-player-buffering.md)
</dt> <dt>

[<span data-ttu-id="3afff-131">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="3afff-131">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





