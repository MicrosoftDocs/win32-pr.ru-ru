---
title: Событие Player. Куррентитемчанже
description: Событие Куррентитемчанже возникает при изменении Controls. currentItem.
ms.assetid: e6f68aeb-d7e7-460b-adc9-647f28c678a1
keywords:
- Проигрыватель Windows Media Event Куррентитемчанже
- Проигрыватель Windows Media Event Куррентитемчанже, класс Player
- Класс проигрывателя Windows Media Player, событие Куррентитемчанже
topic_type:
- apiref
api_name:
- Player.CurrentItemChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c425184bf4b338177ec892ed5362c085dd8cb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708579"
---
# <a name="playercurrentitemchange-event"></a><span data-ttu-id="6e20c-106">Событие Player. Куррентитемчанже</span><span class="sxs-lookup"><span data-stu-id="6e20c-106">Player.CurrentItemChange event</span></span>

<span data-ttu-id="6e20c-107">Событие **куррентитемчанже** возникает при использовании *элементов управления*. **currentItem** изменения.</span><span class="sxs-lookup"><span data-stu-id="6e20c-107">The **CurrentItemChange** event occurs when *Controls*.**currentItem** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e20c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e20c-108">Syntax</span></span>


```JScript
Player.CurrentItemChange()
```



## <a name="parameters"></a><span data-ttu-id="6e20c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e20c-109">Parameters</span></span>

<span data-ttu-id="6e20c-110">У этого события нет параметров.</span><span class="sxs-lookup"><span data-stu-id="6e20c-110">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6e20c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6e20c-111">Return value</span></span>

<span data-ttu-id="6e20c-112">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6e20c-112">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="6e20c-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="6e20c-113">Examples</span></span>

<span data-ttu-id="6e20c-114">В следующем примере JScript демонстрируется обработчик событий для *проигрывателя*. событие **куррентитемчанже** .</span><span class="sxs-lookup"><span data-stu-id="6e20c-114">The following JScript example demonstrates an event handler for the *Player*.**currentItemChange** event.</span></span> <span data-ttu-id="6e20c-115">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="6e20c-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML text box to display the media item name. -->
<INPUT TYPE="TEXT" NAME="MEDIA">

<!-- Create an event handler. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = currentItemChange()>

   // Display the name of the new media item.
   MEDIA.value = Player.currentMedia.name;

</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="6e20c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6e20c-116">Requirements</span></span>



| <span data-ttu-id="6e20c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6e20c-117">Requirement</span></span> | <span data-ttu-id="6e20c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6e20c-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6e20c-119">Версия</span><span class="sxs-lookup"><span data-stu-id="6e20c-119">Version</span></span><br/> | <span data-ttu-id="6e20c-120">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="6e20c-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6e20c-121">DLL</span><span class="sxs-lookup"><span data-stu-id="6e20c-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="6e20c-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e20c-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e20c-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e20c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e20c-124">**Controls. currentItem**</span><span class="sxs-lookup"><span data-stu-id="6e20c-124">**Controls.currentItem**</span></span>](controls-currentitem.md)
</dt> <dt>

[<span data-ttu-id="6e20c-125">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="6e20c-125">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





