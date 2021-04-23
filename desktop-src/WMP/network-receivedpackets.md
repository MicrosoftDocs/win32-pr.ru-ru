---
title: Network. Рецеиведпаккетс
description: Свойство Рецеиведпаккетс Извлекает число полученных пакетов.
ms.assetid: db4f6f08-c248-4db8-ab19-fdd5d2794085
keywords:
- Проигрыватель Windows Media Network. Рецеиведпаккетс
topic_type:
- apiref
api_name:
- Network.receivedPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc792330cd107ca428ad0fbec930fe262a2f131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698917"
---
# <a name="networkreceivedpackets"></a><span data-ttu-id="4cae1-104">Network. Рецеиведпаккетс</span><span class="sxs-lookup"><span data-stu-id="4cae1-104">Network.receivedPackets</span></span>

<span data-ttu-id="4cae1-105">Свойство **рецеиведпаккетс** Извлекает число полученных пакетов.</span><span class="sxs-lookup"><span data-stu-id="4cae1-105">The **receivedPackets** property retrieves the number of packets received.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cae1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4cae1-106">Syntax</span></span>

<span data-ttu-id="4cae1-107">*проигрыватель*. *сеть*. **рецеиведпаккетс**</span><span class="sxs-lookup"><span data-stu-id="4cae1-107">*player*.*network*.**receivedPackets**</span></span>

## <a name="possible-values"></a><span data-ttu-id="4cae1-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="4cae1-108">Possible Values</span></span>

<span data-ttu-id="4cae1-109">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="4cae1-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="4cae1-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4cae1-110">Remarks</span></span>

<span data-ttu-id="4cae1-111">Каждый раз, когда воспроизведение клипа останавливается и перезапускается, это свойство устанавливается в нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="4cae1-111">Each time clip playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="4cae1-112">Он не сбрасывается, если воспроизведение файла приостановлено.</span><span class="sxs-lookup"><span data-stu-id="4cae1-112">It is not reset if file playback is paused.</span></span>

## <a name="examples"></a><span data-ttu-id="4cae1-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="4cae1-113">Examples</span></span>

<span data-ttu-id="4cae1-114">В следующем примере JScript используется *Network*. **рецеиведпаккетс** для вывода числа полученных пакетов.</span><span class="sxs-lookup"><span data-stu-id="4cae1-114">The following JScript example uses *Network*.**receivedPackets** to display the number of packets received.</span></span> <span data-ttu-id="4cae1-115">Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "RP".</span><span class="sxs-lookup"><span data-stu-id="4cae1-115">The information is displayed in an HTML DIV created with ID = "RP".</span></span> <span data-ttu-id="4cae1-116">В примере для обновления экрана используется таймер с интервалом в 1 секунду.</span><span class="sxs-lookup"><span data-stu-id="4cae1-116">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="4cae1-117">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="4cae1-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>

   var idI; // Variable for the interval id.

   // Test whether packets may be arriving.
   switch (NewState){
      case 1, 2, 4, 5, 7, 8, 9:
          window.clearInterval(idI);
          break;

      default:
         idI = window.setInterval("UpdateRP()", 1000);

   }</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRP(){
   RP.innerHTML = "";
   RP.innerHTML = "Packets received: " + Player.network.receivedPackets;         
}

```



## <a name="requirements"></a><span data-ttu-id="4cae1-118">Требования</span><span class="sxs-lookup"><span data-stu-id="4cae1-118">Requirements</span></span>



| <span data-ttu-id="4cae1-119">Требование</span><span class="sxs-lookup"><span data-stu-id="4cae1-119">Requirement</span></span> | <span data-ttu-id="4cae1-120">Значение</span><span class="sxs-lookup"><span data-stu-id="4cae1-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4cae1-121">Версия</span><span class="sxs-lookup"><span data-stu-id="4cae1-121">Version</span></span><br/> | <span data-ttu-id="4cae1-122">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="4cae1-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4cae1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4cae1-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="4cae1-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cae1-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cae1-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cae1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cae1-126">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="4cae1-126">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





