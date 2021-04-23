---
title: Network. Довнлоадпрогресс
description: Свойство Довнлоадпрогресс извлекает процент завершенной загрузки.
ms.assetid: bb57ce84-babb-4dc2-bc2b-c40cbb587e91
keywords:
- Проигрыватель Windows Media Network. Довнлоадпрогресс
topic_type:
- apiref
api_name:
- Network.downloadProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 605d7d08b346c5cc279176098b2a6d593a2fb925
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704211"
---
# <a name="networkdownloadprogress"></a><span data-ttu-id="95510-104">Network. Довнлоадпрогресс</span><span class="sxs-lookup"><span data-stu-id="95510-104">Network.downloadProgress</span></span>

<span data-ttu-id="95510-105">Свойство **довнлоадпрогресс** извлекает процент завершенной загрузки.</span><span class="sxs-lookup"><span data-stu-id="95510-105">The **downloadProgress** property retrieves the percentage of download completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="95510-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95510-106">Syntax</span></span>

<span data-ttu-id="95510-107">*проигрыватель*. *сеть*. **довнлоадпрогресс**</span><span class="sxs-lookup"><span data-stu-id="95510-107">*player*.*network*.**downloadProgress**</span></span>

## <a name="possible-values"></a><span data-ttu-id="95510-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="95510-108">Possible Values</span></span>

<span data-ttu-id="95510-109">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="95510-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="95510-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95510-110">Remarks</span></span>

<span data-ttu-id="95510-111">Когда элемент управления проигрывателя Windows Media подключается к файлу мультимедиа, который можно воспроизвести и скачать одновременно, свойство **довнлоадпрогресс** Возвращает процент общего файла, который был скачан.</span><span class="sxs-lookup"><span data-stu-id="95510-111">When the Windows Media Player control is connected to a media file that can be played and downloaded at the same time, the **downloadProgress** property returns the percentage of the total file that has been downloaded.</span></span> <span data-ttu-id="95510-112">В настоящее время эта функция поддерживается только на веб-серверах.</span><span class="sxs-lookup"><span data-stu-id="95510-112">This feature is currently supported only on web servers.</span></span> <span data-ttu-id="95510-113">Следующие форматы файлов можно скачать и воспроизвести одновременно:</span><span class="sxs-lookup"><span data-stu-id="95510-113">The following file formats can be downloaded and played simultaneously:</span></span>

-   <span data-ttu-id="95510-114">Advanced Systems Format (ASF)</span><span class="sxs-lookup"><span data-stu-id="95510-114">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="95510-115">Звуковые файлы в формате WMA</span><span class="sxs-lookup"><span data-stu-id="95510-115">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="95510-116">Видеофайлы в формате WMV</span><span class="sxs-lookup"><span data-stu-id="95510-116">Windows Media Video (WMV)</span></span>
-   <span data-ttu-id="95510-117">MP3</span><span class="sxs-lookup"><span data-stu-id="95510-117">MP3</span></span>
-   <span data-ttu-id="95510-118">КОДИРОВЩИК</span><span class="sxs-lookup"><span data-stu-id="95510-118">MPEG</span></span>
-   <span data-ttu-id="95510-119">WAV</span><span class="sxs-lookup"><span data-stu-id="95510-119">WAV</span></span>
-   <span data-ttu-id="95510-120">Некоторые файлы AVI</span><span class="sxs-lookup"><span data-stu-id="95510-120">Some AVI files</span></span>

<span data-ttu-id="95510-121">Используйте *проигрыватель*. Событие **буферизации** для определения начала и окончания загрузки.</span><span class="sxs-lookup"><span data-stu-id="95510-121">Use the *Player*.**Buffering** event to determine when the downloading begins and ends.</span></span>

## <a name="examples"></a><span data-ttu-id="95510-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="95510-122">Examples</span></span>

<span data-ttu-id="95510-123">В следующем примере JScript используется *Network*. **довнлоадпрогресс** , чтобы отобразить процент завершенной загрузки.</span><span class="sxs-lookup"><span data-stu-id="95510-123">The following JScript example uses *Network*.**downloadProgress** to display the percentage of downloading completed.</span></span> <span data-ttu-id="95510-124">Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "DP".</span><span class="sxs-lookup"><span data-stu-id="95510-124">The information is displayed in an HTML DIV created with ID = "DP".</span></span> <span data-ttu-id="95510-125">В примере для обновления экрана используется таймер с интервалом в 1 секунду.</span><span class="sxs-lookup"><span data-stu-id="95510-125">The example uses a timer with a 1 second interval to update the display.</span></span> <span data-ttu-id="95510-126">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="95510-126">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.
   
   // Test whether downloading has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display.
      idI = window.setInterval("UpdateDP()", 1000);
   }
   else{
      // Downloading is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateDP(){
   DP.innerHTML = "";
   DP.innerHTML = "Download progress: " + Player.network.downloadProgress;
   DP.innerHTML += " percent complete";
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="95510-127">Требования</span><span class="sxs-lookup"><span data-stu-id="95510-127">Requirements</span></span>



| <span data-ttu-id="95510-128">Требование</span><span class="sxs-lookup"><span data-stu-id="95510-128">Requirement</span></span> | <span data-ttu-id="95510-129">Значение</span><span class="sxs-lookup"><span data-stu-id="95510-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="95510-130">Версия</span><span class="sxs-lookup"><span data-stu-id="95510-130">Version</span></span><br/> | <span data-ttu-id="95510-131">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="95510-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="95510-132">DLL</span><span class="sxs-lookup"><span data-stu-id="95510-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="95510-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95510-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95510-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95510-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95510-135">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="95510-135">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="95510-136">**Событие проигрывателя. буферизация**</span><span class="sxs-lookup"><span data-stu-id="95510-136">**Player.Buffering Event**</span></span>](player-player-buffering.md)
</dt> </dl>

 

 





