---
title: Ивмпмедиаколлектион Жетбяусор, метод
description: Метод Жетбяусор возвращает интерфейс Ивмпплайлист, предоставляющий доступ к элементам мультимедиа по указанному автору.
ms.assetid: eb3793f6-bad1-4c80-991e-c6d0093ae57f
keywords:
- Жетбяусор метод Windows Media Player
- Жетбяусор метод проигрывателя Windows Media Player, интерфейс Ивмпмедиаколлектион
- Интерфейс Ивмпмедиаколлектион Windows Media Player, метод Жетбяусор
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAuthor
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e594de010a65c15088e2a31a3ccbac2ac5a1fc6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669481"
---
# <a name="iwmpmediacollectiongetbyauthor-method"></a><span data-ttu-id="62b7c-106">Метод Ивмпмедиаколлектион:: Жетбяусор</span><span class="sxs-lookup"><span data-stu-id="62b7c-106">IWMPMediaCollection::getByAuthor method</span></span>

<span data-ttu-id="62b7c-107">`getByAuthor`Метод возвращает интерфейс **ивмпплайлист** , предоставляющий доступ к элементам мультимедиа по указанному автору.</span><span class="sxs-lookup"><span data-stu-id="62b7c-107">The `getByAuthor` method returns an **IWMPPlaylist** interface that provides access to the media items by the specified author.</span></span>

## <a name="syntax"></a><span data-ttu-id="62b7c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62b7c-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAuthor(
  System.String bstrAuthor
);
```


```VB

Public Function getByAuthor( _
  ByVal bstrAuthor As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAuthor
```





## <a name="parameters"></a><span data-ttu-id="62b7c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="62b7c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62b7c-110">*бстраусор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="62b7c-110">*bstrAuthor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62b7c-111">**Строка System. String** , которая является именем автора.</span><span class="sxs-lookup"><span data-stu-id="62b7c-111">The **System.String** that is the name of the author.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62b7c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62b7c-112">Return value</span></span>

<span data-ttu-id="62b7c-113">Интерфейс **вмплиб. ивмпплайлист** для извлеченных элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="62b7c-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="62b7c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62b7c-114">Remarks</span></span>

<span data-ttu-id="62b7c-115">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="62b7c-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="62b7c-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="62b7c-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="62b7c-117">Существует два способа получения интерфейса **ивмпмедиаколлектион** , и поведение `getByAuthor` метода зависит от того, какой из этих двух способов вы используете.</span><span class="sxs-lookup"><span data-stu-id="62b7c-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the `getByAuthor` method depends on which of those two ways you use.</span></span> <span data-ttu-id="62b7c-118">При получении интерфейса путем вызова [аксвиндовсмедиаплайер. медиаколлектион](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) `getByAuthor` метод возвращает все элементы мультимедиа в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="62b7c-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the `getByAuthor` method returns all the media items in the library.</span></span> <span data-ttu-id="62b7c-119">Однако при получении интерфейса путем вызова [ивмплибрари. медиаколлектион](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) `getByAuthor` метод возвращает только звуковые элементы в библиотеке с указанным атрибутом и значением.</span><span class="sxs-lookup"><span data-stu-id="62b7c-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the `getByAuthor` method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="62b7c-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="62b7c-120">Examples</span></span>

<span data-ttu-id="62b7c-121">В следующем примере используется `getByAuthor` для создания списка воспроизведения элементов мультимедиа, когда пользователь нажимает кнопку.</span><span class="sxs-lookup"><span data-stu-id="62b7c-121">The following example uses `getByAuthor` to create a playlist of media items when the user clicks a button.</span></span> <span data-ttu-id="62b7c-122">Список воспроизведения содержит элементы, соответствующие имени автора, заданному пользователем, в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="62b7c-122">The playlist contains items matching the author's name specified by the user in a text box.</span></span> <span data-ttu-id="62b7c-123">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="62b7c-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playAuthor_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the author's name from the text box. 
    string author = getAuthor.Text;

    // Create the playlist using getByAuthor. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAuthor(author);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAuthor_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAuthor.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the author&#39;s name from the text box. 
    Dim author As String = getAuthor.Text

    &#39; Create the playlist using getByAuthor. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAuthor(author)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="62b7c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="62b7c-124">Requirements</span></span>



| <span data-ttu-id="62b7c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="62b7c-125">Requirement</span></span> | <span data-ttu-id="62b7c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="62b7c-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62b7c-127">Версия</span><span class="sxs-lookup"><span data-stu-id="62b7c-127">Version</span></span><br/>   | <span data-ttu-id="62b7c-128">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="62b7c-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="62b7c-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="62b7c-129">Namespace</span></span><br/> | <span data-ttu-id="62b7c-130">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="62b7c-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="62b7c-131">Сборка</span><span class="sxs-lookup"><span data-stu-id="62b7c-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="62b7c-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="62b7c-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62b7c-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62b7c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62b7c-134">**Интерфейс Ивмпмедиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="62b7c-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="62b7c-135">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="62b7c-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





