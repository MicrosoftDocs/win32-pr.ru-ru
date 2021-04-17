---
title: Медиаколлектион. Жетбиженре, метод
description: Метод Жетбиженре извлекает список воспроизведения элементов мультимедиа с указанным жанром.
ms.assetid: 022a0c52-93e1-4ab4-90a7-632bcd6fc004
keywords:
- Жетбиженре метод Windows Media Player
- Жетбиженре метод Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион Windows Media Player, метод Жетбиженре
topic_type:
- apiref
api_name:
- MediaCollection.getByGenre
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b73cd7fe9bb3efa9115e2ba5d01b6d12c89898d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685415"
---
# <a name="mediacollectiongetbygenre-method"></a><span data-ttu-id="10e9d-106">Медиаколлектион. Жетбиженре, метод</span><span class="sxs-lookup"><span data-stu-id="10e9d-106">MediaCollection.getByGenre method</span></span>

<span data-ttu-id="10e9d-107">Метод **жетбиженре** извлекает список воспроизведения элементов мультимедиа с указанным жанром.</span><span class="sxs-lookup"><span data-stu-id="10e9d-107">The **getByGenre** method retrieves a playlist of the media items with the specified genre.</span></span>

## <a name="syntax"></a><span data-ttu-id="10e9d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10e9d-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByGenre(
  genre
)
```



## <a name="parameters"></a><span data-ttu-id="10e9d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="10e9d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10e9d-110">*Жанр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="10e9d-110">*genre* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10e9d-111">**Строка** , содержащая название жанра.</span><span class="sxs-lookup"><span data-stu-id="10e9d-111">**String** containing the name of the genre.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10e9d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10e9d-112">Return value</span></span>

<span data-ttu-id="10e9d-113">Этот метод возвращает объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="10e9d-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="10e9d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10e9d-114">Remarks</span></span>

<span data-ttu-id="10e9d-115">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="10e9d-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="10e9d-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="10e9d-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="10e9d-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="10e9d-117">Examples</span></span>

<span data-ttu-id="10e9d-118">В следующем примере JScript используется *медиаколлектион*. **жетбиженре** для получения списка воспроизведения элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="10e9d-118">The following JScript example uses *MediaCollection*.**getByGenre** to retrieve a playlist of media items.</span></span> <span data-ttu-id="10e9d-119">Список воспроизведения содержит элементы с жанром, указанным пользователем в HTML-элементе input TEXT с именем GetText.</span><span class="sxs-lookup"><span data-stu-id="10e9d-119">The playlist contains items with the genre specified by the user in an HTML TEXT input element named GetGenre.</span></span> <span data-ttu-id="10e9d-120">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="10e9d-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play 
the media items. -->
<INPUT TYPE = "BUTTON"  
       NAME = "PlayGenre"  
       ID = "PlayGenre"  
       VALUE = "Play Genre"

onClick = "
    /* Retrieve the genre text from the user. */
    var genre = GetGenre.value;

    /* Create the playlist using getByGenre. */
    var pl = Player.mediaCollection.getByGenre(genre);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the digital media item in the new playlist. */
    Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="10e9d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="10e9d-121">Requirements</span></span>



| <span data-ttu-id="10e9d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="10e9d-122">Requirement</span></span> | <span data-ttu-id="10e9d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="10e9d-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="10e9d-124">Версия</span><span class="sxs-lookup"><span data-stu-id="10e9d-124">Version</span></span><br/> | <span data-ttu-id="10e9d-125">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="10e9d-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="10e9d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="10e9d-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="10e9d-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10e9d-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10e9d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10e9d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10e9d-129">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="10e9d-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="10e9d-130">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="10e9d-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="10e9d-131">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="10e9d-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="10e9d-132">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="10e9d-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





