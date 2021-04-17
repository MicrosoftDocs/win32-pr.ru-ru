---
title: Controls. currentItem
description: Свойство currentItem указывает или получает текущий элемент мультимедиа.
ms.assetid: 77e21585-3cc8-41f5-97b5-da6eb992c7bc
keywords:
- Проигрыватель Windows Media Controls. currentItem
topic_type:
- apiref
api_name:
- Controls.currentItem
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81658665cb6f31acd327f5050a733a2fc3c70371
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698794"
---
# <a name="controlscurrentitem"></a><span data-ttu-id="97a4d-104">Controls. currentItem</span><span class="sxs-lookup"><span data-stu-id="97a4d-104">Controls.currentItem</span></span>

<span data-ttu-id="97a4d-105">Свойство **currentItem** указывает или получает текущий элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="97a4d-105">The **currentItem** property specifies or retrieves the current media item.</span></span>

``` syntax
player.controls.currentItem
      
```

## <a name="possible-values"></a><span data-ttu-id="97a4d-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="97a4d-106">Possible Values</span></span>

<span data-ttu-id="97a4d-107">Это свойство является объектом **мультимедиа** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="97a4d-107">This property is a read/write **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="97a4d-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97a4d-108">Remarks</span></span>

<span data-ttu-id="97a4d-109">Этот метод работает только с элементами в *проигрывателе*. **куррентплайлист**.</span><span class="sxs-lookup"><span data-stu-id="97a4d-109">This method works only with items in *Player*.**currentPlaylist**.</span></span> <span data-ttu-id="97a4d-110">Вызов **currentItem** со ссылкой на сохраненный элемент мультимедиа не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="97a4d-110">Calling **currentItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="97a4d-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="97a4d-111">Examples</span></span>

<span data-ttu-id="97a4d-112">В следующем примере JScript используется **currentItem** , чтобы установить проигрыватель для управления текущим элементом мультимедиа на выбранное значение в HTML-элементе SELECT.</span><span class="sxs-lookup"><span data-stu-id="97a4d-112">The following JScript example uses **currentItem** to set the player control current media item to the selected value in an HTML SELECT element.</span></span> <span data-ttu-id="97a4d-113">Текущий список воспроизведения был впервые указан с помощью *плайлистколлектион*. **жетбинаме**.</span><span class="sxs-lookup"><span data-stu-id="97a4d-113">The current playlist was first specified by using *PlaylistCollection*.**getByName**.</span></span> <span data-ttu-id="97a4d-114">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="97a4d-114">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = playItem  NAME = "playItem"  LANGUAGE = "JScript"

    /* Specify the current item when the selected list value changes. */
    onChange = "Player.controls.currentItem = Player.currentPlaylist.item(playItem.value);">

    /* Fill the SELECT element list with three items that match
       the songs in the playlist. */
    <OPTION VALUE = 0 >Laure
    <OPTION VALUE = 1 >Jeanne
    <OPTION VALUE = 2 >House
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="97a4d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="97a4d-115">Requirements</span></span>



| <span data-ttu-id="97a4d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="97a4d-116">Requirement</span></span> | <span data-ttu-id="97a4d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="97a4d-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="97a4d-118">Версия</span><span class="sxs-lookup"><span data-stu-id="97a4d-118">Version</span></span><br/> | <span data-ttu-id="97a4d-119">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="97a4d-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="97a4d-120">DLL</span><span class="sxs-lookup"><span data-stu-id="97a4d-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="97a4d-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97a4d-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97a4d-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97a4d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97a4d-123">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="97a4d-123">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="97a4d-124">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="97a4d-124">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="97a4d-125">**Плайлистколлектион. Жетбинаме**</span><span class="sxs-lookup"><span data-stu-id="97a4d-125">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





