---
title: Network. Рецептионкуалити
description: Свойство Рецептионкуалити извлекает процент полученных пакетов за последние 30 секунд.
ms.assetid: 432f7f0a-0130-4485-b4a3-daa80ce9bb36
keywords:
- Проигрыватель Windows Media Network. Рецептионкуалити
topic_type:
- apiref
api_name:
- Network.receptionQuality
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3706ba4d953f80c4a9e799971a7e73d49553c709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698916"
---
# <a name="networkreceptionquality"></a><span data-ttu-id="4482e-104">Network. Рецептионкуалити</span><span class="sxs-lookup"><span data-stu-id="4482e-104">Network.receptionQuality</span></span>

<span data-ttu-id="4482e-105">Свойство **рецептионкуалити** извлекает процент полученных пакетов за последние 30 секунд.</span><span class="sxs-lookup"><span data-stu-id="4482e-105">The **receptionQuality** property retrieves the percentage of packets received in the last 30 seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="4482e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4482e-106">Syntax</span></span>

<span data-ttu-id="4482e-107">*проигрыватель*. *сеть*. **рецептионкуалити**</span><span class="sxs-lookup"><span data-stu-id="4482e-107">*player*.*network*.**receptionQuality**</span></span>

## <a name="possible-values"></a><span data-ttu-id="4482e-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="4482e-108">Possible Values</span></span>

<span data-ttu-id="4482e-109">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="4482e-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="4482e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4482e-110">Remarks</span></span>

<span data-ttu-id="4482e-111">Количество пакетов, полученных, потерянных и восстановленных во время потоковой передачи, отслеживается каждую секунду.</span><span class="sxs-lookup"><span data-stu-id="4482e-111">The number of packets received, lost, and recovered during streaming is monitored once every second.</span></span> <span data-ttu-id="4482e-112">**рецептионкуалити** — процент пакетов, которые не были потеряны за последние 30 секунд.</span><span class="sxs-lookup"><span data-stu-id="4482e-112">**receptionQuality** is the percentage of packets not lost during the last 30 seconds.</span></span>

<span data-ttu-id="4482e-113">Каждый раз, когда воспроизведение останавливается и перезапускается, это свойство устанавливается в нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="4482e-113">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="4482e-114">Если воспроизведение приостановлено, оно не сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="4482e-114">It is not reset if playback is paused.</span></span>

<span data-ttu-id="4482e-115">Это свойство возвращает действительные сведения только во время выполнения и только в случае, если *проигрыватель*. Также задано свойство **URL-адреса** .</span><span class="sxs-lookup"><span data-stu-id="4482e-115">This property returns valid information only during run time and only if the *Player*.**URL** property is also set.</span></span>

## <a name="examples"></a><span data-ttu-id="4482e-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="4482e-116">Examples</span></span>

<span data-ttu-id="4482e-117">В следующем примере JScript используется *Network*. **рецептионкуалити** , чтобы отобразить процент полученных пакетов.</span><span class="sxs-lookup"><span data-stu-id="4482e-117">The following JScript example uses *Network*.**receptionQuality** to display the percentage of packets received.</span></span> <span data-ttu-id="4482e-118">Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "РК".</span><span class="sxs-lookup"><span data-stu-id="4482e-118">The information is displayed in an HTML DIV created with ID = "RQ".</span></span> <span data-ttu-id="4482e-119">В примере для обновления экрана используется таймер с 30-секундным интервалом.</span><span class="sxs-lookup"><span data-stu-id="4482e-119">The example uses a timer with a 30-second interval to update the display.</span></span> <span data-ttu-id="4482e-120">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="4482e-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
         // Start the timer. Update the display every 30 seconds.
         idI = window.setInterval("UpdateRQ()", 30000);
   }

      else{
         // Not playing; stop the timer.
         window.clearInterval(idI);
      }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRQ(){
         RQ.innerHTML = "";
         RQ.innerHTML = "Reception quality: " + Player.network.receptionQuality;
         RQ.innerHTML += "%";         
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="4482e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4482e-121">Requirements</span></span>



| <span data-ttu-id="4482e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4482e-122">Requirement</span></span> | <span data-ttu-id="4482e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4482e-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4482e-124">Версия</span><span class="sxs-lookup"><span data-stu-id="4482e-124">Version</span></span><br/> | <span data-ttu-id="4482e-125">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="4482e-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4482e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4482e-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="4482e-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4482e-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4482e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4482e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4482e-129">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="4482e-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="4482e-130">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="4482e-130">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





