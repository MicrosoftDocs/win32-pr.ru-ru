---
title: Метод списка воспроизведения. Item
description: Метод Item извлекает элемент мультимедиа по указанному индексу.
ms.assetid: a564f6db-ede4-4c85-87ca-0e2539d914c2
keywords:
- метод Item проигрыватель Windows Media Player
- метод Item проигрыватель Windows Media Player, класс списка воспроизведения
- Класс списка воспроизведения проигрыватель Windows Media Player, метод Item
topic_type:
- apiref
api_name:
- Playlist.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c69386871aeec33dbc36a066ce3f75e80d7514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708568"
---
# <a name="playlistitem-method"></a><span data-ttu-id="1facc-106">Метод списка воспроизведения. Item</span><span class="sxs-lookup"><span data-stu-id="1facc-106">Playlist.item method</span></span>

<span data-ttu-id="1facc-107">Метод **Item** извлекает элемент мультимедиа по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="1facc-107">The **item** method retrieves the media item at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="1facc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1facc-108">Syntax</span></span>


```JScript
retVal = Playlist.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="1facc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1facc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1facc-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1facc-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1facc-111">**Число** (**Long**), содержащее индекс извлекаемого элемента.</span><span class="sxs-lookup"><span data-stu-id="1facc-111">**Number** (**long**) containing the index of the item to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1facc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1facc-112">Return value</span></span>

<span data-ttu-id="1facc-113">Этот метод возвращает объект **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="1facc-113">This method returns a **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1facc-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1facc-114">Remarks</span></span>

<span data-ttu-id="1facc-115">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="1facc-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="1facc-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1facc-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1facc-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="1facc-117">Examples</span></span>

<span data-ttu-id="1facc-118">В следующем примере JScript используется *список воспроизведения*. **элемент** для извлечения элемента мультимедиа из текущего списка воспроизведения на основе выбора пользователя.</span><span class="sxs-lookup"><span data-stu-id="1facc-118">The following JScript example uses *Playlist*.**item** to retrieve a media item from the current playlist based on a user selection.</span></span> <span data-ttu-id="1facc-119">Был создан HTML-элемент SELECT с именем "список", который заполняется заголовками из текущего списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="1facc-119">An HTML SELECT element was created with name "weblist", and filled with the titles from the current playlist.</span></span> <span data-ttu-id="1facc-120">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="1facc-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the value of the selected item in the list box
// using the selectedIndex property.
var index = weblist.selectedIndex;

// Store the corresponding digital media object from the current playlist.
var listItem = Player.currentPlaylist.item(index);

// Set the URL using the listItem variable.
Player.URL = listItem.sourceURL;

```



## <a name="requirements"></a><span data-ttu-id="1facc-121">Требования</span><span class="sxs-lookup"><span data-stu-id="1facc-121">Requirements</span></span>



| <span data-ttu-id="1facc-122">Требование</span><span class="sxs-lookup"><span data-stu-id="1facc-122">Requirement</span></span> | <span data-ttu-id="1facc-123">Значение</span><span class="sxs-lookup"><span data-stu-id="1facc-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1facc-124">Версия</span><span class="sxs-lookup"><span data-stu-id="1facc-124">Version</span></span><br/> | <span data-ttu-id="1facc-125">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="1facc-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1facc-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1facc-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="1facc-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1facc-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1facc-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1facc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1facc-129">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="1facc-129">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="1facc-130">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="1facc-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="1facc-131">**Список воспроизведения. insertItem**</span><span class="sxs-lookup"><span data-stu-id="1facc-131">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="1facc-132">**Список воспроизведения. removeItem**</span><span class="sxs-lookup"><span data-stu-id="1facc-132">**Playlist.removeItem**</span></span>](playlist-removeitem.md)
</dt> <dt>

[<span data-ttu-id="1facc-133">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="1facc-133">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="1facc-134">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="1facc-134">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





