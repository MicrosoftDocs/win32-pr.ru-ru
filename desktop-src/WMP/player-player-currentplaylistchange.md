---
title: Событие Player. Куррентплайлистчанже
description: Событие Куррентплайлистчанже возникает при изменении в текущем списке воспроизведения. | Событие Player. Куррентплайлистчанже
ms.assetid: 5270373e-e401-40c6-bf8c-ef0557610372
keywords:
- Проигрыватель Windows Media Event Куррентплайлистчанже
- Проигрыватель Windows Media Event Куррентплайлистчанже, класс Player
- Класс проигрывателя Windows Media Player, событие Куррентплайлистчанже
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4722db224285587198e3ddb021022ec5d8f2cea6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704227"
---
# <a name="playercurrentplaylistchange-event"></a><span data-ttu-id="93e56-107">Событие Player. Куррентплайлистчанже</span><span class="sxs-lookup"><span data-stu-id="93e56-107">Player.CurrentPlaylistChange event</span></span>

<span data-ttu-id="93e56-108">Событие **куррентплайлистчанже** возникает при изменении в текущем списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="93e56-108">The **CurrentPlaylistChange** event occurs when something changes within the current playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="93e56-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93e56-109">Syntax</span></span>


```JScript
Player.CurrentPlaylistChange(
  change
)
```



## <a name="parameters"></a><span data-ttu-id="93e56-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="93e56-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93e56-111">*change*</span><span class="sxs-lookup"><span data-stu-id="93e56-111">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="93e56-112">**Число** (**длинное**), указывающее тип изменений, произошедших в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="93e56-112">**Number** (**long**) indicating what type of change occurred to the playlist.</span></span> <span data-ttu-id="93e56-113">См. *проигрыватель*. Событие **плайлистчанже** для таблицы возможных значений.</span><span class="sxs-lookup"><span data-stu-id="93e56-113">See the *Player*.**PlaylistChange** event for a table of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93e56-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93e56-114">Return value</span></span>

<span data-ttu-id="93e56-115">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="93e56-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="93e56-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93e56-116">Remarks</span></span>

<span data-ttu-id="93e56-117">Это событие не происходит, если другой список воспроизведения попадает в текущий список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="93e56-117">This event does not occur when a different playlist becomes the current playlist.</span></span> <span data-ttu-id="93e56-118">Это происходит только в том случае, если изменение происходит в текущем списке воспроизведения, например при добавлении элемента мультимедиа в список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="93e56-118">It only occurs when a change happens within the current playlist, such as a media item being appended to the playlist.</span></span>

<span data-ttu-id="93e56-119">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="93e56-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="93e56-120">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="93e56-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="examples"></a><span data-ttu-id="93e56-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="93e56-121">Examples</span></span>

<span data-ttu-id="93e56-122">В следующем примере кода JScript обновляется текст в элементе HTML DIV с именем Плитемс, чтобы отобразить имена элементов мультимедиа в текущем списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="93e56-122">The following JScript example updates the text in an HTML DIV element, named PlItems, to display the names of the media items in the current playlist.</span></span> <span data-ttu-id="93e56-123">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="93e56-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for current playlist change. -->
<SCRIPT FOR = "Player" EVENT = "currentPlaylistChange(change)">
   switch (change){
      // Only update for move, delete, insert, and append events.
      case 3, 4, 5, 6:

         // Clear the contents of the DIV.
         PlItems.innerHTML = "";

         // Loop through the playlist and display each item name.
         for (var i = 0; i < Player.currentPlaylist.count; i++){
            PlItems.innerHTML += Player.currentPlaylist.item(i).name;
            PlItems.innerHTML += "<br>";
         }
         break;
      
      default:
   } 
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="93e56-124">Требования</span><span class="sxs-lookup"><span data-stu-id="93e56-124">Requirements</span></span>



| <span data-ttu-id="93e56-125">Требование</span><span class="sxs-lookup"><span data-stu-id="93e56-125">Requirement</span></span> | <span data-ttu-id="93e56-126">Значение</span><span class="sxs-lookup"><span data-stu-id="93e56-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="93e56-127">Версия</span><span class="sxs-lookup"><span data-stu-id="93e56-127">Version</span></span><br/> | <span data-ttu-id="93e56-128">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="93e56-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="93e56-129">DLL</span><span class="sxs-lookup"><span data-stu-id="93e56-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="93e56-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93e56-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93e56-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93e56-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93e56-132">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="93e56-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="93e56-133">**Player. Куррентплайлист**</span><span class="sxs-lookup"><span data-stu-id="93e56-133">**Player.currentPlaylist**</span></span>](player-currentplaylist.md)
</dt> <dt>

[<span data-ttu-id="93e56-134">**Player. Плайлистчанже**</span><span class="sxs-lookup"><span data-stu-id="93e56-134">**Player.PlaylistChange**</span></span>](player-player-playlistchange.md)
</dt> </dl>

 

 





