---
title: Network. Рековередпаккетс
description: Свойство Рековередпаккетс извлекает количество восстановленных пакетов.
ms.assetid: ce10b906-2e8b-4b9f-83d0-56ba67cacd3f
keywords:
- Проигрыватель Windows Media Network. Рековередпаккетс
topic_type:
- apiref
api_name:
- Network.recoveredPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a4222033d7e124e6ef29714bc47faf5664950fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695081"
---
# <a name="networkrecoveredpackets"></a><span data-ttu-id="7dc8c-104">Network. Рековередпаккетс</span><span class="sxs-lookup"><span data-stu-id="7dc8c-104">Network.recoveredPackets</span></span>

<span data-ttu-id="7dc8c-105">Свойство **рековередпаккетс** извлекает количество восстановленных пакетов.</span><span class="sxs-lookup"><span data-stu-id="7dc8c-105">The **recoveredPackets** property retrieves the number of recovered packets.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dc8c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7dc8c-106">Syntax</span></span>

<span data-ttu-id="7dc8c-107">*проигрыватель*. *сеть*. **рековередпаккетс**</span><span class="sxs-lookup"><span data-stu-id="7dc8c-107">*player*.*network*.**recoveredPackets**</span></span>

## <a name="possible-values"></a><span data-ttu-id="7dc8c-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="7dc8c-108">Possible Values</span></span>

<span data-ttu-id="7dc8c-109">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="7dc8c-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="7dc8c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7dc8c-110">Remarks</span></span>

<span data-ttu-id="7dc8c-111">Каждый раз, когда воспроизведение останавливается и перезапускается, это свойство устанавливается в нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="7dc8c-111">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="7dc8c-112">Если воспроизведение приостановлено, оно не сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="7dc8c-112">It is not reset if playback is paused.</span></span>

<span data-ttu-id="7dc8c-113">Это свойство возвращает действительные сведения только во время выполнения и только в случае, если *проигрыватель*. Также задано свойство **URL-адреса** .</span><span class="sxs-lookup"><span data-stu-id="7dc8c-113">This property returns valid information only during run time and only if the *Player*.**URL** property is also set.</span></span> <span data-ttu-id="7dc8c-114">При использовании протокола HTTP, который работает без потерь, он будет равен нулю.</span><span class="sxs-lookup"><span data-stu-id="7dc8c-114">It will equal zero when using the HTTP protocol, which is lossless.</span></span>

## <a name="examples"></a><span data-ttu-id="7dc8c-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="7dc8c-115">Examples</span></span>

<span data-ttu-id="7dc8c-116">В следующем примере JScript используется *Network*. **рековередпаккетс** , чтобы отобразить количество восстановленных пакетов.</span><span class="sxs-lookup"><span data-stu-id="7dc8c-116">The following JScript example uses *Network*.**recoveredPackets** to display the number of recovered packets.</span></span> <span data-ttu-id="7dc8c-117">Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "PR".</span><span class="sxs-lookup"><span data-stu-id="7dc8c-117">The information is displayed in an HTML DIV created with ID = "PR".</span></span> <span data-ttu-id="7dc8c-118">В примере для обновления экрана используется таймер с интервалом в 1 секунду.</span><span class="sxs-lookup"><span data-stu-id="7dc8c-118">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="7dc8c-119">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="7dc8c-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
      // Start the timer. Call the function to update the display every second.
      idI = window.setInterval("UpdatePR()", 1000);
   }
   else{
      // Not playing; stop the timer.
      window.clearInterval(idI);
   }   
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdatePR(){
   PR.innerHTML = "";
   PR.innerHTML = "Packets recovered: " + Player.network.recoveredPackets;
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="7dc8c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="7dc8c-120">Requirements</span></span>



| <span data-ttu-id="7dc8c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="7dc8c-121">Requirement</span></span> | <span data-ttu-id="7dc8c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7dc8c-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc8c-123">Версия</span><span class="sxs-lookup"><span data-stu-id="7dc8c-123">Version</span></span><br/> | <span data-ttu-id="7dc8c-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="7dc8c-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7dc8c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7dc8c-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="7dc8c-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dc8c-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dc8c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7dc8c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dc8c-128">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="7dc8c-128">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="7dc8c-129">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="7dc8c-129">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





