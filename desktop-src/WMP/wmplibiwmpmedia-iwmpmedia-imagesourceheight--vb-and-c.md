---
title: Ивмпмедиа Имажесаурцехеигхт, свойство
description: Свойство Имажесаурцехеигхт Получает высоту текущего элемента мультимедиа в пикселях.
ms.assetid: d60f1713-7110-4605-9009-45825c380546
keywords:
- Проигрыватель Windows Media для свойства Имажесаурцехеигхт
- Имажесаурцехеигхт свойство проигрывателя Windows Media Player, интерфейс Ивмпмедиа
- Интерфейс Ивмпмедиа Windows Media Player, свойство Имажесаурцехеигхт
topic_type:
- apiref
api_name:
- IWMPMedia.imageSourceHeight
- IWMPMedia.get_imageSourceHeight
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b80a702f119ba72220e5ac3ac86b524ce8c11c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669246"
---
# <a name="iwmpmediaimagesourceheight-property"></a><span data-ttu-id="0f901-106">Свойство Ивмпмедиа:: Имажесаурцехеигхт</span><span class="sxs-lookup"><span data-stu-id="0f901-106">IWMPMedia::imageSourceHeight property</span></span>

<span data-ttu-id="0f901-107">Свойство **имажесаурцехеигхт** Получает высоту текущего элемента мультимедиа в пикселях.</span><span class="sxs-lookup"><span data-stu-id="0f901-107">The **imageSourceHeight** property gets the height of the current media item in pixels.</span></span>

<span data-ttu-id="0f901-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0f901-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f901-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f901-109">Syntax</span></span>


```CSharp
public System.Int32 imageSourceHeight {get;}
```


```VB

Public ReadOnly Property imageSourceHeight As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="0f901-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0f901-110">Property value</span></span>

<span data-ttu-id="0f901-111">Значение **System. Int32** , которое является высотой элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0f901-111">A **System.Int32** that is the height of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f901-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f901-112">Remarks</span></span>

<span data-ttu-id="0f901-113">Если элемент мультимедиа не является текущим, это свойство возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="0f901-113">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="0f901-114">Перед использованием этого свойства необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="0f901-114">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="0f901-115">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="0f901-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0f901-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="0f901-116">Examples</span></span>

<span data-ttu-id="0f901-117">В следующем примере **имажесаурцехеигхт** используется для вывода размера изображения (в пикселях) текущего элемента мультимедиа в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="0f901-117">The following example uses **imageSourceHeight** to display the image size, in pixels, of the current media item in a text box.</span></span> <span data-ttu-id="0f901-118">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="0f901-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create an event handler for the OpenStateChange event.
private void player_OpenStateChange(object sender, AxWMPLib._WMPOCXEvents_OpenStateChangeEvent e)
{
    // Test whether the current media item is open.
    if (e.newState == (int)WMPLib.WMPOpenState.wmposMediaOpen)
    {
         // Store the height and width of the new media item.
         int height = player.currentMedia.imageSourceHeight;
         int width = player.currentMedia.imageSourceWidth;

         // Clear all the information in the text box.
         videoSize.Clear();

         // Test whether an image is visible.
         if (height != 0 && width != 0)
         {
            // Display the image size information.
            videoSize.Text = (width.ToString() + " x " + height.ToString());
         }
    }
}
```


```VB

' Create an event handler for the OpenStateChange event.
Public Sub player_OpenStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_OpenStateChangeEvent) Handles player.OpenStateChange

    &#39; Test whether the current media item is open.
    If (e.newState = WMPLib.WMPOpenState.wmposMediaOpen) Then

        &#39; Store the height and width of the new media item.
        Dim Height As Integer = player.currentMedia.imageSourceHeight
        Dim Width As Integer = player.currentMedia.imageSourceWidth

        &#39; Clear all the information in the text box.
        videoSize.Clear()

        &#39; Test whether an image is visible.
        If (Height <> 0 And Width <> 0) Then

            &#39; Display the image size information.
            videoSize.Text = (Width.ToString() + &quot; x &quot; + Height.ToString())

        End If

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="0f901-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0f901-119">Requirements</span></span>



| <span data-ttu-id="0f901-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0f901-120">Requirement</span></span> | <span data-ttu-id="0f901-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0f901-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f901-122">Версия</span><span class="sxs-lookup"><span data-stu-id="0f901-122">Version</span></span><br/>   | <span data-ttu-id="0f901-123">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="0f901-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0f901-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0f901-124">Namespace</span></span><br/> | <span data-ttu-id="0f901-125">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="0f901-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0f901-126">Сборка</span><span class="sxs-lookup"><span data-stu-id="0f901-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0f901-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0f901-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f901-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f901-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f901-129">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="0f901-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





