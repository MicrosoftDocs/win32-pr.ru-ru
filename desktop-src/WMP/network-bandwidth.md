---
title: Network. пропускная способность
description: Свойство пропускной способности извлекает текущую пропускную способность клипа.
ms.assetid: 2ef86f2a-98e9-4544-a740-c2237f06c135
keywords:
- Проигрыватель Windows Media Network. пропускная способность
topic_type:
- apiref
api_name:
- Network.bandWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4783d86160070fc61202f97b4cf3882f2cebcfb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704222"
---
# <a name="networkbandwidth"></a><span data-ttu-id="94f58-104">Network. пропускная способность</span><span class="sxs-lookup"><span data-stu-id="94f58-104">Network.bandWidth</span></span>

<span data-ttu-id="94f58-105">Свойство **пропускной способности** извлекает текущую пропускную способность клипа.</span><span class="sxs-lookup"><span data-stu-id="94f58-105">The **bandWidth** property retrieves the current bandwidth of the clip.</span></span>

## <a name="syntax"></a><span data-ttu-id="94f58-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94f58-106">Syntax</span></span>

<span data-ttu-id="94f58-107">*проигрыватель*. *сеть*. **пропускная способность**</span><span class="sxs-lookup"><span data-stu-id="94f58-107">*player*.*network*.**bandWidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="94f58-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="94f58-108">Possible Values</span></span>

<span data-ttu-id="94f58-109">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="94f58-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="94f58-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94f58-110">Remarks</span></span>

<span data-ttu-id="94f58-111">Это свойство возвращает нуль, если *игрок*. Свойство **URL-адреса** не задано.</span><span class="sxs-lookup"><span data-stu-id="94f58-111">This property returns zero if the *Player*.**URL** property is not set.</span></span> <span data-ttu-id="94f58-112">Это свойство допустимо только для потоковой передачи мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="94f58-112">This property is only valid for streaming media.</span></span>

## <a name="examples"></a><span data-ttu-id="94f58-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="94f58-113">Examples</span></span>

<span data-ttu-id="94f58-114">В следующем примере Microsoft JScript используется *Network*. **пропускная способность** для вывода текущей пропускной способности носителя.</span><span class="sxs-lookup"><span data-stu-id="94f58-114">The following Microsoft JScript example uses *Network*.**bandWidth** to display the current media bandwidth.</span></span> <span data-ttu-id="94f58-115">Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "BW".</span><span class="sxs-lookup"><span data-stu-id="94f58-115">The information is displayed in an HTML DIV created with ID = "BW".</span></span> <span data-ttu-id="94f58-116">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="94f58-116">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state.-->
<SCRIPT FOR = Player EVENT = PlayStateChange()>

   switch (Player.playState){

      case 3:

         if (Player.network.bandwidth != 0){
  
            BW.innerHTML = "Current Bandwidth: " + Player.network.bandWidth;
            BW.innerHTML += " K bits/second";
         }

         else
            BW.innerHTML = "Bandwidth is only available for streaming media.";

            break;

      default:
}
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="94f58-117">Требования</span><span class="sxs-lookup"><span data-stu-id="94f58-117">Requirements</span></span>



| <span data-ttu-id="94f58-118">Требование</span><span class="sxs-lookup"><span data-stu-id="94f58-118">Requirement</span></span> | <span data-ttu-id="94f58-119">Значение</span><span class="sxs-lookup"><span data-stu-id="94f58-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="94f58-120">Версия</span><span class="sxs-lookup"><span data-stu-id="94f58-120">Version</span></span><br/> | <span data-ttu-id="94f58-121">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="94f58-121">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="94f58-122">DLL</span><span class="sxs-lookup"><span data-stu-id="94f58-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="94f58-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94f58-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94f58-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94f58-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94f58-125">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="94f58-125">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="94f58-126">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="94f58-126">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





