---
title: Ивмпмедиаколлектион Жетбялбум, метод
description: Метод Жетбялбум возвращает интерфейс Ивмпплайлист, предоставляющий доступ к элементам мультимедиа из указанного альбома.
ms.assetid: 26f004c0-de46-4792-8212-9d4ac749bb21
keywords:
- Жетбялбум метод Windows Media Player
- Жетбялбум метод проигрывателя Windows Media Player, интерфейс Ивмпмедиаколлектион
- Интерфейс Ивмпмедиаколлектион Windows Media Player, метод Жетбялбум
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAlbum
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c455e9bd61038a4d72bb6537d7c62b30a5d0b733
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669483"
---
# <a name="iwmpmediacollectiongetbyalbum-method"></a><span data-ttu-id="2f11a-106">Метод Ивмпмедиаколлектион:: Жетбялбум</span><span class="sxs-lookup"><span data-stu-id="2f11a-106">IWMPMediaCollection::getByAlbum method</span></span>

<span data-ttu-id="2f11a-107">Метод **жетбялбум** возвращает интерфейс **ивмпплайлист** , предоставляющий доступ к элементам мультимедиа из указанного альбома.</span><span class="sxs-lookup"><span data-stu-id="2f11a-107">The **getByAlbum** method returns an **IWMPPlaylist** interface that provides access to media items from the specified album.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f11a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f11a-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAlbum(
  System.String bstrAlbum
);
```


```VB

Public Function getByAlbum( _
  ByVal bstrAlbum As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAlbum
```





## <a name="parameters"></a><span data-ttu-id="2f11a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f11a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f11a-110">*бстралбум* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2f11a-110">*bstrAlbum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f11a-111">**Строка System. String** , которая является заголовком альбома.</span><span class="sxs-lookup"><span data-stu-id="2f11a-111">The **System.String** that is the title of the album.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f11a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f11a-112">Return value</span></span>

<span data-ttu-id="2f11a-113">Интерфейс **вмплиб. ивмпплайлист** для извлеченных элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2f11a-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f11a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f11a-114">Remarks</span></span>

<span data-ttu-id="2f11a-115">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="2f11a-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="2f11a-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2f11a-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="2f11a-117">Существует два способа получения интерфейса **ивмпмедиаколлектион** , и поведение метода **жетбялбум** зависит от того, какой из этих двух способов вы используете.</span><span class="sxs-lookup"><span data-stu-id="2f11a-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getByAlbum** method depends on which of those two ways you use.</span></span> <span data-ttu-id="2f11a-118">При получении интерфейса путем вызова [аксвиндовсмедиаплайер. медиаколлектион](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)метод **жетбялбум** возвращает все элементы мультимедиа в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="2f11a-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getByAlbum** method returns all the media items in the library.</span></span> <span data-ttu-id="2f11a-119">Однако при получении интерфейса путем вызова [ивмплибрари. медиаколлектион](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)метод **жетбялбум** возвращает только звуковые элементы в библиотеке, которая принадлежит указанному альбому.</span><span class="sxs-lookup"><span data-stu-id="2f11a-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getByAlbum** method returns only the audio items in the library that belong to the specified album.</span></span>

## <a name="examples"></a><span data-ttu-id="2f11a-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="2f11a-120">Examples</span></span>

<span data-ttu-id="2f11a-121">В следующем примере **жетбялбум** используется для создания списка воспроизведения элементов мультимедиа, когда пользователь нажимает кнопку.</span><span class="sxs-lookup"><span data-stu-id="2f11a-121">The following example uses **getByAlbum** to create a playlist of media items when the user clicks a button.</span></span> <span data-ttu-id="2f11a-122">Список воспроизведения содержит элементы с альбомом, указанным пользователем в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="2f11a-122">The playlist contains items with the album specified by the user in a text box.</span></span> <span data-ttu-id="2f11a-123">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="2f11a-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playAlbum_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the album title text that the user entered in the text box. 
    string album = getAlbum.Text;

    // Create the playlist using getByAlbum. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAlbum(album);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAlbum_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAlbum.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the album title text that the user entered in the text box. 
    Dim album As String = getAlbum.Text

    &#39; Create the playlist using getByAlbum. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAlbum(album)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="2f11a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="2f11a-124">Requirements</span></span>



| <span data-ttu-id="2f11a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="2f11a-125">Requirement</span></span> | <span data-ttu-id="2f11a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2f11a-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f11a-127">Версия</span><span class="sxs-lookup"><span data-stu-id="2f11a-127">Version</span></span><br/>   | <span data-ttu-id="2f11a-128">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2f11a-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2f11a-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2f11a-129">Namespace</span></span><br/> | <span data-ttu-id="2f11a-130">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="2f11a-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2f11a-131">Сборка</span><span class="sxs-lookup"><span data-stu-id="2f11a-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2f11a-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2f11a-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f11a-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f11a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f11a-134">**Интерфейс Ивмпмедиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2f11a-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2f11a-135">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2f11a-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





