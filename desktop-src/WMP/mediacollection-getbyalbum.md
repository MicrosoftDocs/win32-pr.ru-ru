---
title: Медиаколлектион. Жетбялбум, метод
description: Метод Жетбялбум извлекает список воспроизведения, содержащий элементы мультимедиа из указанного альбома.
ms.assetid: e7e72f0e-e0ae-4bbd-a8b7-966f0fc50059
keywords:
- Жетбялбум метод Windows Media Player
- Жетбялбум метод Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион Windows Media Player, метод Жетбялбум
topic_type:
- apiref
api_name:
- MediaCollection.getByAlbum
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d94cdfa880288893e9659b73b01bc754ac59bbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689059"
---
# <a name="mediacollectiongetbyalbum-method"></a><span data-ttu-id="fee01-106">Медиаколлектион. Жетбялбум, метод</span><span class="sxs-lookup"><span data-stu-id="fee01-106">MediaCollection.getByAlbum method</span></span>

<span data-ttu-id="fee01-107">Метод **жетбялбум** извлекает список воспроизведения, содержащий элементы мультимедиа из указанного альбома.</span><span class="sxs-lookup"><span data-stu-id="fee01-107">The **GetByAlbum** method retrieves a playlist containing the media items from the specified album.</span></span>

## <a name="syntax"></a><span data-ttu-id="fee01-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fee01-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAlbum(
  album
)
```



## <a name="parameters"></a><span data-ttu-id="fee01-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fee01-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fee01-110">*альбом* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fee01-110">*album* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fee01-111">**Строка** , содержащая имя альбома.</span><span class="sxs-lookup"><span data-stu-id="fee01-111">**String** containing the name of the album.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fee01-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fee01-112">Return value</span></span>

<span data-ttu-id="fee01-113">Этот метод возвращает объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="fee01-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fee01-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fee01-114">Remarks</span></span>

<span data-ttu-id="fee01-115">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="fee01-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="fee01-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="fee01-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fee01-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="fee01-117">Examples</span></span>

<span data-ttu-id="fee01-118">В следующем примере используется *медиаколлектион*. **жетбялбум** для получения списка воспроизведения элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fee01-118">The following example uses *MediaCollection*.**getByAlbum** to retrieve a playlist of media items.</span></span> <span data-ttu-id="fee01-119">Список воспроизведения содержит элементы с альбомом, указанным пользователем в HTML-элементе input TEXT с именем GetText.</span><span class="sxs-lookup"><span data-stu-id="fee01-119">The playlist contains items with the album specified by the user in an HTML TEXT input element named GetAlbum.</span></span> <span data-ttu-id="fee01-120">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="fee01-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and 
then play the digital media items. -->
<INPUT TYPE = "BUTTON"
       NAME = "PlayAlbum" 
       ID = "PlayAlbum"  
       VALUE = "Play Album"

onClick = "
    /* Retrieve the album title text from the user. */
    var album = GetAlbum.value;

    /* Create the playlist using getByAlbum. */
    var pl = Player.mediaCollection.getByAlbum(album);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media in the new playlist. */
    Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="fee01-121">Требования</span><span class="sxs-lookup"><span data-stu-id="fee01-121">Requirements</span></span>



| <span data-ttu-id="fee01-122">Требование</span><span class="sxs-lookup"><span data-stu-id="fee01-122">Requirement</span></span> | <span data-ttu-id="fee01-123">Значение</span><span class="sxs-lookup"><span data-stu-id="fee01-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fee01-124">Версия</span><span class="sxs-lookup"><span data-stu-id="fee01-124">Version</span></span><br/> | <span data-ttu-id="fee01-125">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="fee01-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fee01-126">DLL</span><span class="sxs-lookup"><span data-stu-id="fee01-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="fee01-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fee01-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fee01-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fee01-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fee01-129">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="fee01-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="fee01-130">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="fee01-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="fee01-131">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="fee01-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="fee01-132">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="fee01-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





