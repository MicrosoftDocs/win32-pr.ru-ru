---
title: Ивмпмедиа Дуратионстринг, свойство
description: Свойство Дуратионстринг получает строку, указывающую длительность текущего элемента мультимедиа в формате чч мм СС.
ms.assetid: de33c737-d73e-41f0-9c1b-944279194738
keywords:
- Проигрыватель Windows Media для свойства Дуратионстринг
- Дуратионстринг свойство проигрывателя Windows Media Player, интерфейс Ивмпмедиа
- Интерфейс Ивмпмедиа Windows Media Player, свойство Дуратионстринг
topic_type:
- apiref
api_name:
- IWMPMedia.durationString
- IWMPMedia.get_durationString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e6bc732388036aa9e79aeedd988de94fa263bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669260"
---
# <a name="iwmpmediadurationstring-property"></a><span data-ttu-id="6c510-106">Ивмпмедиа: свойство Уратионстринг:d</span><span class="sxs-lookup"><span data-stu-id="6c510-106">IWMPMedia::durationString property</span></span>

<span data-ttu-id="6c510-107">Свойство **дуратионстринг** получает строку, указывающую длительность текущего элемента мультимедиа в формате чч: мм: СС.</span><span class="sxs-lookup"><span data-stu-id="6c510-107">The **durationString** property gets a string indicating the duration of the current media item in HH:MM:SS format.</span></span>

<span data-ttu-id="6c510-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6c510-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c510-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c510-109">Syntax</span></span>


```CSharp
public System.String durationString {get;}
```


```VB

Public ReadOnly Property durationString As System.String
```





## <a name="property-value"></a><span data-ttu-id="6c510-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6c510-110">Property value</span></span>

<span data-ttu-id="6c510-111">**Строка System. String** , которая является длительностью.</span><span class="sxs-lookup"><span data-stu-id="6c510-111">A **System.String** that is the duration.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c510-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c510-112">Remarks</span></span>

<span data-ttu-id="6c510-113">Если это свойство используется с элементом мультимедиа, отличным от указанного в Аксвиндовсмедиаплайер. Куррентмедиа, он может не содержать допустимого значения.</span><span class="sxs-lookup"><span data-stu-id="6c510-113">If this property is used with a media item other than the one specified in AxWindowsMediaPlayer.currentMedia, it may not contain a valid value.</span></span> <span data-ttu-id="6c510-114">Если размер элемента мультимедиа меньше часа, часть возвращаемого значения в часах не указывается.</span><span class="sxs-lookup"><span data-stu-id="6c510-114">If the media item is less than an hour long, the hours portion of the return value is omitted.</span></span>

<span data-ttu-id="6c510-115">Перед использованием этого свойства необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="6c510-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="6c510-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="6c510-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6c510-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="6c510-117">Examples</span></span>

<span data-ttu-id="6c510-118">В следующем примере используется **дуратионстринг** , чтобы отобразить продолжительность текущего элемента мультимедиа в виде форматированного текста в метке.</span><span class="sxs-lookup"><span data-stu-id="6c510-118">The following example uses **durationString** to display the duration of the current media item as formatted text in a label.</span></span> <span data-ttu-id="6c510-119">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="6c510-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create an event handler for the OpenStateChange event.
private void player_OpenStateChange(object sender, AxWMPLib._WMPOCXEvents_OpenStateChangeEvent e)
{
    // Test whether the current media item is open.
    if (e.newState == (int)WMPLib.WMPOpenState.wmposMediaOpen)
    {
         // Display the formatted duration string in the label.
         mediaDuration.Text = player.currentMedia.durationString;
    }
}
```


```VB

' Create an event handler for the OpenStateChange event.
Public Sub player_OpenStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_OpenStateChangeEvent) Handles player.OpenStateChange

    &#39; Test whether the current media item is open.
    If (e.newState = 13) Then

        &#39; Display the formatted duration string in the label.
        mediaDuration.Text = player.currentMedia.durationString

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="6c510-120">Требования</span><span class="sxs-lookup"><span data-stu-id="6c510-120">Requirements</span></span>



| <span data-ttu-id="6c510-121">Требование</span><span class="sxs-lookup"><span data-stu-id="6c510-121">Requirement</span></span> | <span data-ttu-id="6c510-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6c510-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c510-123">Версия</span><span class="sxs-lookup"><span data-stu-id="6c510-123">Version</span></span><br/>   | <span data-ttu-id="6c510-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="6c510-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6c510-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6c510-125">Namespace</span></span><br/> | <span data-ttu-id="6c510-126">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="6c510-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6c510-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="6c510-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6c510-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6c510-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c510-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c510-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c510-130">**Аксвиндовсмедиаплайер. Куррентмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="6c510-130">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6c510-131">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="6c510-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6c510-132">**Ивмпмедиа. Duration (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="6c510-132">**IWMPMedia.duration (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)
</dt> </dl>

 

 





