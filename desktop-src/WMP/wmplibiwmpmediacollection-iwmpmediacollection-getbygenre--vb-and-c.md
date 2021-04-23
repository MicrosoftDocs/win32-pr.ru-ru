---
title: Ивмпмедиаколлектион Жетбиженре, метод
description: Метод Жетбиженре возвращает интерфейс Ивмпплайлист, предоставляющий доступ к элементам мультимедиа указанного жанра.
ms.assetid: 0681e5a2-b56d-4c33-95ce-d9ef3cd5473d
keywords:
- Жетбиженре метод Windows Media Player
- Жетбиженре метод проигрывателя Windows Media Player, интерфейс Ивмпмедиаколлектион
- Интерфейс Ивмпмедиаколлектион Windows Media Player, метод Жетбиженре
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByGenre
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb6477a4cd212f354f5af3ab7e50fc2a87092cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669331"
---
# <a name="iwmpmediacollectiongetbygenre-method"></a><span data-ttu-id="2bcd2-106">Метод Ивмпмедиаколлектион:: Жетбиженре</span><span class="sxs-lookup"><span data-stu-id="2bcd2-106">IWMPMediaCollection::getByGenre method</span></span>

<span data-ttu-id="2bcd2-107">`getByGenre`Метод возвращает интерфейс **ивмпплайлист** , предоставляющий доступ к элементам мультимедиа указанного жанра.</span><span class="sxs-lookup"><span data-stu-id="2bcd2-107">The `getByGenre` method returns an **IWMPPlaylist** interface that provides access to media items of the specified genre.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bcd2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2bcd2-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByGenre(
  System.String bstrGenre
);
```


```VB

Public Function getByGenre( _
  ByVal bstrGenre As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByGenre
```





## <a name="parameters"></a><span data-ttu-id="2bcd2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2bcd2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bcd2-110">*бстрженре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2bcd2-110">*bstrGenre* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bcd2-111">**Строка System. String** , которая является именем жанра.</span><span class="sxs-lookup"><span data-stu-id="2bcd2-111">The **System.String** that is the name of the genre.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bcd2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2bcd2-112">Return value</span></span>

<span data-ttu-id="2bcd2-113">Интерфейс **вмплиб. ивмпплайлист** для извлеченных элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2bcd2-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bcd2-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2bcd2-114">Remarks</span></span>

<span data-ttu-id="2bcd2-115">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="2bcd2-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="2bcd2-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2bcd2-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="2bcd2-117">Существует два способа получения интерфейса **ивмпмедиаколлектион** , и поведение `getByGenre` метода зависит от того, какой из этих двух способов вы используете.</span><span class="sxs-lookup"><span data-stu-id="2bcd2-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the `getByGenre` method depends on which of those two ways you use.</span></span> <span data-ttu-id="2bcd2-118">При получении интерфейса путем вызова [аксвиндовсмедиаплайер. медиаколлектион](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) `getByGenre` метод возвращает все элементы мультимедиа в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="2bcd2-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the `getByGenre` method returns all the media items in the library.</span></span> <span data-ttu-id="2bcd2-119">Однако при получении интерфейса путем вызова [ивмплибрари. медиаколлектион](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) `getByGenre` метод возвращает только звуковые элементы в библиотеке с указанным атрибутом и значением.</span><span class="sxs-lookup"><span data-stu-id="2bcd2-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the `getByGenre` method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="2bcd2-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="2bcd2-120">Examples</span></span>

<span data-ttu-id="2bcd2-121">В следующем примере используется `getByGenre` для получения списка воспроизведения элементов мультимедиа, когда пользователь нажимает кнопку.</span><span class="sxs-lookup"><span data-stu-id="2bcd2-121">The following example uses `getByGenre` to retrieve a playlist of media items when the user clicks a button.</span></span> <span data-ttu-id="2bcd2-122">Список воспроизведения содержит элементы с жанром, указанным пользователем в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="2bcd2-122">The playlist contains items with the genre specified by the user in a text box.</span></span> <span data-ttu-id="2bcd2-123">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="2bcd2-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playGenre_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the genre that the user entered in the text box. 
    string genre = getGenre.Text;

    // Create the playlist using getByGenre. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByGenre(genre);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playGenre.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the genre that the user entered in the text box. 
    Dim genre As String = getGenre.Text

    &#39; Create the playlist using getByGenre. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByGenre(genre)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="2bcd2-124">Требования</span><span class="sxs-lookup"><span data-stu-id="2bcd2-124">Requirements</span></span>



| <span data-ttu-id="2bcd2-125">Требование</span><span class="sxs-lookup"><span data-stu-id="2bcd2-125">Requirement</span></span> | <span data-ttu-id="2bcd2-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2bcd2-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bcd2-127">Версия</span><span class="sxs-lookup"><span data-stu-id="2bcd2-127">Version</span></span><br/>   | <span data-ttu-id="2bcd2-128">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2bcd2-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2bcd2-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2bcd2-129">Namespace</span></span><br/> | <span data-ttu-id="2bcd2-130">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="2bcd2-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2bcd2-131">Сборка</span><span class="sxs-lookup"><span data-stu-id="2bcd2-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2bcd2-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2bcd2-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bcd2-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2bcd2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bcd2-134">**Интерфейс Ивмпмедиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2bcd2-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2bcd2-135">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2bcd2-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





