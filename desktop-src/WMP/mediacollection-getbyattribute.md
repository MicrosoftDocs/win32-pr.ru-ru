---
title: Медиаколлектион. Жетбяттрибуте, метод
description: Метод Жетбяттрибуте извлекает список воспроизведения элементов мультимедиа, содержащих указанное значение для указанного атрибута.
ms.assetid: a89f9c52-c655-4420-858e-c0eed661856f
keywords:
- Жетбяттрибуте метод Windows Media Player
- Жетбяттрибуте метод Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион Windows Media Player, метод Жетбяттрибуте
topic_type:
- apiref
api_name:
- MediaCollection.getByAttribute
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533823127364416f8f4492c82381e682173c5c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689058"
---
# <a name="mediacollectiongetbyattribute-method"></a><span data-ttu-id="2467d-106">Медиаколлектион. Жетбяттрибуте, метод</span><span class="sxs-lookup"><span data-stu-id="2467d-106">MediaCollection.getByAttribute method</span></span>

<span data-ttu-id="2467d-107">Метод **жетбяттрибуте** извлекает список воспроизведения элементов мультимедиа, содержащих указанное значение для указанного атрибута.</span><span class="sxs-lookup"><span data-stu-id="2467d-107">The **getByAttribute** method retrieves a playlist of media items that contain a specified value for a specified attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="2467d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2467d-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAttribute(
  attribute,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="2467d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2467d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2467d-110">*атрибут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2467d-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2467d-111">**Строка** , указывающая имя атрибута для поиска.</span><span class="sxs-lookup"><span data-stu-id="2467d-111">**String** indicating the name of the attribute to search.</span></span> <span data-ttu-id="2467d-112">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2467d-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="2467d-113">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2467d-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2467d-114">**Строка** , указывающая значение, которое должен иметь атрибут.</span><span class="sxs-lookup"><span data-stu-id="2467d-114">**String** indicating the value that the attribute should have.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2467d-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2467d-115">Return value</span></span>

<span data-ttu-id="2467d-116">Этот метод возвращает объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="2467d-116">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2467d-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2467d-117">Remarks</span></span>

<span data-ttu-id="2467d-118">Этот метод можно использовать для создания универсального запроса для элементов мультимедиа, которые соответствуют значению атрибута в базе данных.</span><span class="sxs-lookup"><span data-stu-id="2467d-118">This method can be used to create a generic query for media items that match a value for an attribute in the database.</span></span> <span data-ttu-id="2467d-119">Это полезно в случае определяемых пользователем атрибутов.</span><span class="sxs-lookup"><span data-stu-id="2467d-119">This is useful in the case of user-defined attributes.</span></span> <span data-ttu-id="2467d-120">Если атрибут не существует, возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="2467d-120">If the attribute does not exist, an error will result.</span></span>

<span data-ttu-id="2467d-121">Этот метод можно использовать для извлечения всех элементов мультимедиа определенного типа.</span><span class="sxs-lookup"><span data-stu-id="2467d-121">You can use this method to retrieve all of the media items of a specific type.</span></span> <span data-ttu-id="2467d-122">Используйте имя атрибута MediaType и одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="2467d-122">Use the attribute name "MediaType" and one of the following values:</span></span>



| <span data-ttu-id="2467d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2467d-123">Value</span></span>    | <span data-ttu-id="2467d-124">Описание</span><span class="sxs-lookup"><span data-stu-id="2467d-124">Description</span></span>                                                |
|----------|------------------------------------------------------------|
| <span data-ttu-id="2467d-125">звук</span><span class="sxs-lookup"><span data-stu-id="2467d-125">audio</span></span>    | <span data-ttu-id="2467d-126">Музыку и другие звуковые элементы.</span><span class="sxs-lookup"><span data-stu-id="2467d-126">Music and other audio-only items.</span></span>                          |
| <span data-ttu-id="2467d-127">список воспроизведения</span><span class="sxs-lookup"><span data-stu-id="2467d-127">playlist</span></span> | <span data-ttu-id="2467d-128">Списки воспроизведения, представленные в виде объектов **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="2467d-128">Playlists represented as **Media** objects.</span></span>                |
| <span data-ttu-id="2467d-129">radio</span><span class="sxs-lookup"><span data-stu-id="2467d-129">radio</span></span>    | <span data-ttu-id="2467d-130">Элементы радиостанции.</span><span class="sxs-lookup"><span data-stu-id="2467d-130">Radio station items.</span></span> <span data-ttu-id="2467d-131">Не используется проигрывателем Windows Media 10.</span><span class="sxs-lookup"><span data-stu-id="2467d-131">Not used by Windows Media Player 10.</span></span>  |
| <span data-ttu-id="2467d-132">видео</span><span class="sxs-lookup"><span data-stu-id="2467d-132">video</span></span>    | <span data-ttu-id="2467d-133">Элементы видео.</span><span class="sxs-lookup"><span data-stu-id="2467d-133">Video items.</span></span>                                               |
| <span data-ttu-id="2467d-134">фотография</span><span class="sxs-lookup"><span data-stu-id="2467d-134">photo</span></span>    | <span data-ttu-id="2467d-135">Элементы фото.</span><span class="sxs-lookup"><span data-stu-id="2467d-135">Photo items.</span></span> <span data-ttu-id="2467d-136">Требуется проигрыватель Windows Media 10.</span><span class="sxs-lookup"><span data-stu-id="2467d-136">Requires Windows Media Player 10.</span></span>             |
| <span data-ttu-id="2467d-137">др.</span><span class="sxs-lookup"><span data-stu-id="2467d-137">other</span></span>    | <span data-ttu-id="2467d-138">Другие элементы, такие как файлы ASF или URL-адреса для потокового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2467d-138">Other items, such as ASF files or URLs to streaming media.</span></span> |



 

<span data-ttu-id="2467d-139">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="2467d-139">To use this method, read access to the library is required.</span></span> <span data-ttu-id="2467d-140">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2467d-140">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2467d-141">Примеры</span><span class="sxs-lookup"><span data-stu-id="2467d-141">Examples</span></span>

<span data-ttu-id="2467d-142">В следующем примере JScript используется *медиаколлектион*. **жетбяттрибуте** воспроизвести все содержимое из библиотеки с помощью исполнителя с именем триоде 48.</span><span class="sxs-lookup"><span data-stu-id="2467d-142">The following JScript example uses *MediaCollection*.**getByAttribute** to play all content from the library by the artist named Triode 48.</span></span> <span data-ttu-id="2467d-143">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="2467d-143">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get a playlist object filled with media items by a 
// particular artist.
var pl = Player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
Player.currentPlaylist = pl;

// Start Windows Media Player.
Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="2467d-144">Требования</span><span class="sxs-lookup"><span data-stu-id="2467d-144">Requirements</span></span>



| <span data-ttu-id="2467d-145">Требование</span><span class="sxs-lookup"><span data-stu-id="2467d-145">Requirement</span></span> | <span data-ttu-id="2467d-146">Значение</span><span class="sxs-lookup"><span data-stu-id="2467d-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2467d-147">Версия</span><span class="sxs-lookup"><span data-stu-id="2467d-147">Version</span></span><br/> | <span data-ttu-id="2467d-148">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="2467d-148">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2467d-149">DLL</span><span class="sxs-lookup"><span data-stu-id="2467d-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="2467d-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2467d-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2467d-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2467d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2467d-152">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="2467d-152">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="2467d-153">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="2467d-153">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="2467d-154">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="2467d-154">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="2467d-155">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="2467d-155">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





