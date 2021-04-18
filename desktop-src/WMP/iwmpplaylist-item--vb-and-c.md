---
title: Ивмпплайлист. Item (VB и C)
description: Свойство Item ( \_ метод Get Item в C \) получает интерфейс для элемента мультимедиа по указанному индексу.
ms.assetid: 874663e2-0b89-4ef7-9d4a-3a334482b352
keywords:
- Проигрыватель Windows Media Ивмпплайлист. Item (VB и C)
topic_type:
- apiref
api_name:
- IWMPPlaylist.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1318f37c3f590eec2c97252e2f484b0d1bc6d83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685074"
---
# <a name="iwmpplaylistitem-vb-and-c"></a><span data-ttu-id="26e73-104">Ивмпплайлист. Item (VB и C#)</span><span class="sxs-lookup"><span data-stu-id="26e73-104">IWMPPlaylist.Item (VB and C#)</span></span>

<span data-ttu-id="26e73-105">Свойство **Item** (метод **Get \_ Item** в C#) получает интерфейс для элемента мультимедиа по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="26e73-105">The **Item** property (the **get\_Item** method in C#) gets an interface to the media item at the specified index.</span></span>


```
[Visual Basic]
ReadOnly Property Item(
  lIndex As System.Int32
) As IWMPMedia
```




```
[C#]
IWMPMedia get_Item (
  System.Int32 lIndex 
);
```



## <a name="parameters"></a><span data-ttu-id="26e73-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="26e73-106">Parameters</span></span>

<span data-ttu-id="26e73-107">*линдекс*</span><span class="sxs-lookup"><span data-stu-id="26e73-107">*lIndex*</span></span>

<span data-ttu-id="26e73-108">Объект **System. Int32** , который является индексом элемента мультимедиа в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="26e73-108">A **System.Int32** that is the index of the media item in the playlist.</span></span>

## <a name="property-value"></a><span data-ttu-id="26e73-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="26e73-109">Property Value</span></span>

<span data-ttu-id="26e73-110">Интерфейс **вмплиб. ивмпмедиа** , предоставляющий доступ к элементу мультимедиа по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="26e73-110">An **WMPLib.IWMPMedia** interface that provides access to the media item at the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="26e73-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26e73-111">Remarks</span></span>

<span data-ttu-id="26e73-112">**Ивмпплайлист. Item** — это свойство, доступное только для чтения, в Visual Basic, которое принимает параметр, а в C# называется методом **ивмпплайлист. Get \_ Item** .</span><span class="sxs-lookup"><span data-stu-id="26e73-112">**IWMPPlaylist.Item** is a read-only property in Visual Basic that takes a parameter, while in C# it is referred to as the **IWMPPlaylist.get\_Item** method.</span></span>

## <a name="examples"></a><span data-ttu-id="26e73-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="26e73-113">Examples</span></span>

<span data-ttu-id="26e73-114">В следующем примере свойство **Item** (метод **Get \_ Item** в C#) используется для извлечения элемента мультимедиа из списка воспроизведения на основе выбора пользователя.</span><span class="sxs-lookup"><span data-stu-id="26e73-114">The following example uses the **Item** property (the **get\_Item** method in C#) to retrieve a media item from a playlist based on a user selection.</span></span> <span data-ttu-id="26e73-115">Список был создан с именем "список" и заполняется заголовками из списка воспроизведения с именем Аудиоплайлист.</span><span class="sxs-lookup"><span data-stu-id="26e73-115">A list box was created with the name weblist, and filled with the titles from the playlist called audioPlaylist.</span></span> <span data-ttu-id="26e73-116">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="26e73-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void weblist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    // Store the index of the selected item in the list box.
    int index = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Store the corresponding media item from the playlist.
    WMPLib.IWMPMedia listItem = audioPlaylist.get_Item(index);

    // Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL;
}
```


```VB

Public Sub weblist_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles weblist.SelectedIndexChanged

    &#39; Store the index of the selected item in the list box.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim index As Integer = lb.SelectedIndex

    &#39; Store the corresponding media item from the playlist.
    Dim listItem As WMPLib.IWMPMedia = audioPlaylist.Item(index)

    &#39; Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL

End Sub
```





## <a name="requirements"></a><span data-ttu-id="26e73-117">Требования</span><span class="sxs-lookup"><span data-stu-id="26e73-117">Requirements</span></span>



| <span data-ttu-id="26e73-118">Требование</span><span class="sxs-lookup"><span data-stu-id="26e73-118">Requirement</span></span> | <span data-ttu-id="26e73-119">Значение</span><span class="sxs-lookup"><span data-stu-id="26e73-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26e73-120">Версия</span><span class="sxs-lookup"><span data-stu-id="26e73-120">Version</span></span><br/>   | <span data-ttu-id="26e73-121">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="26e73-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="26e73-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="26e73-122">Namespace</span></span><br/> | <span data-ttu-id="26e73-123">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="26e73-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="26e73-124">Сборка</span><span class="sxs-lookup"><span data-stu-id="26e73-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="26e73-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="26e73-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26e73-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26e73-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26e73-127">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="26e73-127">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="26e73-128">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="26e73-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="26e73-129">**Ивмпплайлист. insertItem (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="26e73-129">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="26e73-130">**Ивмпплайлист. removeItem (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="26e73-130">**IWMPPlaylist.removeItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="26e73-131">**IWMPSettings2. Медиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="26e73-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="26e73-132">**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="26e73-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





