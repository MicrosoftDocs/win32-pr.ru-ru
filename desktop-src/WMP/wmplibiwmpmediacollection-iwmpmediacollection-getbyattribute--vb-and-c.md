---
title: Ивмпмедиаколлектион Жетбяттрибуте, метод
description: Метод Жетбяттрибуте возвращает интерфейс Ивмпплайлист, соответствующий указанному атрибуту, имеющему указанное значение.
ms.assetid: ece70a2c-38bc-4652-8319-efcde5f9720a
keywords:
- Жетбяттрибуте метод Windows Media Player
- Жетбяттрибуте метод проигрывателя Windows Media Player, интерфейс Ивмпмедиаколлектион
- Интерфейс Ивмпмедиаколлектион Windows Media Player, метод Жетбяттрибуте
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAttribute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd7adba98fbfa450cd938b56ec6d91598b918d0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669482"
---
# <a name="iwmpmediacollectiongetbyattribute-method"></a><span data-ttu-id="7870a-106">Метод Ивмпмедиаколлектион:: Жетбяттрибуте</span><span class="sxs-lookup"><span data-stu-id="7870a-106">IWMPMediaCollection::getByAttribute method</span></span>

<span data-ttu-id="7870a-107">Метод **жетбяттрибуте** возвращает интерфейс **ивмпплайлист** , соответствующий указанному атрибуту, имеющему указанное значение.</span><span class="sxs-lookup"><span data-stu-id="7870a-107">The **getByAttribute** method returns an **IWMPPlaylist** interface that corresponds to the specified attribute having the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7870a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7870a-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAttribute(
  System.String bstrAttribute,
  System.String bstrValue
);
```


```VB

Public Function getByAttribute( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAttribute
```





## <a name="parameters"></a><span data-ttu-id="7870a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7870a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7870a-110">*бстраттрибуте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7870a-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7870a-111">**Строка System. String** , которая является указанным атрибутом.</span><span class="sxs-lookup"><span data-stu-id="7870a-111">The **System.String** that is the specified attribute.</span></span>

</dd> <dt>

<span data-ttu-id="7870a-112">*бстрвалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7870a-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7870a-113">**Строка System. String** , которая является указанным значением.</span><span class="sxs-lookup"><span data-stu-id="7870a-113">The **System.String** that is the specified value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7870a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7870a-114">Return value</span></span>

<span data-ttu-id="7870a-115">Интерфейс **вмплиб. ивмпплайлист** для извлеченных элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7870a-115">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="7870a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7870a-116">Remarks</span></span>

<span data-ttu-id="7870a-117">Этот метод можно использовать для создания универсального запроса для элементов мультимедиа, которые соответствуют значению атрибута в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="7870a-117">This method can be used to create a generic query for media items that match a value for an attribute in the library.</span></span> <span data-ttu-id="7870a-118">Это полезно в случае определяемых пользователем атрибутов.</span><span class="sxs-lookup"><span data-stu-id="7870a-118">This is useful in the case of user-defined attributes.</span></span> <span data-ttu-id="7870a-119">Если атрибут не существует, возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="7870a-119">If the attribute does not exist, an error will result.</span></span>

<span data-ttu-id="7870a-120">Этот метод можно использовать для извлечения всех элементов мультимедиа определенного типа.</span><span class="sxs-lookup"><span data-stu-id="7870a-120">You can use this method to retrieve all of the media items of a specific type.</span></span> <span data-ttu-id="7870a-121">Используйте имя атрибута **mediaType** и одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7870a-121">Use the attribute name **MediaType** and one of the following values.</span></span>



| <span data-ttu-id="7870a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7870a-122">Value</span></span>    | <span data-ttu-id="7870a-123">Описание</span><span class="sxs-lookup"><span data-stu-id="7870a-123">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="7870a-124">звук</span><span class="sxs-lookup"><span data-stu-id="7870a-124">audio</span></span>    | <span data-ttu-id="7870a-125">Музыка и другие звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="7870a-125">Music and other audio-only items</span></span>                          |
| <span data-ttu-id="7870a-126">др.</span><span class="sxs-lookup"><span data-stu-id="7870a-126">other</span></span>    | <span data-ttu-id="7870a-127">Другие элементы, например файлы ASF или URL-адрес потока.</span><span class="sxs-lookup"><span data-stu-id="7870a-127">Other items, such as an .asf file or the URL of a stream.</span></span> |
| <span data-ttu-id="7870a-128">фотография</span><span class="sxs-lookup"><span data-stu-id="7870a-128">photo</span></span>    | <span data-ttu-id="7870a-129">Элементы фото.</span><span class="sxs-lookup"><span data-stu-id="7870a-129">Photo items.</span></span> <span data-ttu-id="7870a-130">Требуется проигрыватель Windows Media 10.</span><span class="sxs-lookup"><span data-stu-id="7870a-130">Requires Windows Media Player 10.</span></span>            |
| <span data-ttu-id="7870a-131">список воспроизведения</span><span class="sxs-lookup"><span data-stu-id="7870a-131">playlist</span></span> | <span data-ttu-id="7870a-132">Списки воспроизведения, представленные в виде элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7870a-132">Playlists represented as media items.</span></span>                     |
| <span data-ttu-id="7870a-133">radio</span><span class="sxs-lookup"><span data-stu-id="7870a-133">radio</span></span>    | <span data-ttu-id="7870a-134">Элементы радиостанции.</span><span class="sxs-lookup"><span data-stu-id="7870a-134">Radio station items.</span></span> <span data-ttu-id="7870a-135">Не используется проигрывателем Windows Media 10.</span><span class="sxs-lookup"><span data-stu-id="7870a-135">Not used by Windows Media Player 10.</span></span> |
| <span data-ttu-id="7870a-136">видео</span><span class="sxs-lookup"><span data-stu-id="7870a-136">video</span></span>    | <span data-ttu-id="7870a-137">Элементы видео.</span><span class="sxs-lookup"><span data-stu-id="7870a-137">Video items.</span></span>                                              |



 

<span data-ttu-id="7870a-138">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="7870a-138">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="7870a-139">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7870a-139">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="7870a-140">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="7870a-140">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="7870a-141">Существует два способа получения интерфейса **ивмпмедиаколлектион** , и поведение метода **жетбяттрибуте** зависит от того, какой из этих двух способов вы используете.</span><span class="sxs-lookup"><span data-stu-id="7870a-141">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getByAttribute** method depends on which of those two ways you use.</span></span> <span data-ttu-id="7870a-142">При получении интерфейса путем вызова [аксвиндовсмедиаплайер. медиаколлектион](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)метод **жетбяттрибуте** возвращает все элементы мультимедиа в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="7870a-142">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getByAttribute** method returns all the media items in the library.</span></span> <span data-ttu-id="7870a-143">Однако при получении интерфейса путем вызова [ивмплибрари. медиаколлектион](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)метод **жетбяттрибуте** возвращает только звуковые элементы в библиотеке с указанным атрибутом и значением.</span><span class="sxs-lookup"><span data-stu-id="7870a-143">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getByAttribute** method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="7870a-144">Примеры</span><span class="sxs-lookup"><span data-stu-id="7870a-144">Examples</span></span>

<span data-ttu-id="7870a-145">В следующем примере кода используется **жетбяттрибуте** для воспроизведения всего содержимого из библиотеки исполнителем с именем триоде 48.</span><span class="sxs-lookup"><span data-stu-id="7870a-145">The following code example uses **getByAttribute** to play all content from the library by the artist named Triode 48.</span></span> <span data-ttu-id="7870a-146">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="7870a-146">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to a playlist that contains media items by a particular artist.
WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
player.currentPlaylist = pl;

// Play the media items in the current playlist. 
player.Ctlcontrols.play();
```


```VB

' Get an interface to a playlist that contains media items by a particular artist.
Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAttribute(&quot;Artist&quot;, &quot;Triode 48&quot;)

&#39; Make the new playlist the current one.
player.currentPlaylist = pl

&#39; Play the media items in the current playlist. 
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="7870a-147">Требования</span><span class="sxs-lookup"><span data-stu-id="7870a-147">Requirements</span></span>



| <span data-ttu-id="7870a-148">Требование</span><span class="sxs-lookup"><span data-stu-id="7870a-148">Requirement</span></span> | <span data-ttu-id="7870a-149">Значение</span><span class="sxs-lookup"><span data-stu-id="7870a-149">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7870a-150">Версия</span><span class="sxs-lookup"><span data-stu-id="7870a-150">Version</span></span><br/>   | <span data-ttu-id="7870a-151">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7870a-151">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7870a-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7870a-152">Namespace</span></span><br/> | <span data-ttu-id="7870a-153">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="7870a-153">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7870a-154">Сборка</span><span class="sxs-lookup"><span data-stu-id="7870a-154">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7870a-155"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7870a-155"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7870a-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7870a-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7870a-157">**Интерфейс Ивмпмедиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7870a-157">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7870a-158">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7870a-158">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7870a-159">**Ивмпплайлистколлектион. Жеталл (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7870a-159">**IWMPPlaylistCollection.getAll (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)
</dt> </dl>

 

 





