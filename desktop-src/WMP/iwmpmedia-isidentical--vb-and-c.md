---
title: Ивмпмедиа. одинаковы (VB и C)
description: Свойство «идентично» (метод Get \_ одинаковы в C \) возвращает значение, указывающее, совпадает ли указанный элемент мультимедиа с текущим.
ms.assetid: 1406a0ff-2dc8-4cde-8b71-4a39b8608fb1
keywords:
- Проигрыватель Windows Media Ивмпмедиа. одинаковы (VB и C)
topic_type:
- apiref
api_name:
- IWMPMedia.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a488ad300362c1f8dccfd0fa6f6c7e4dee7676
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689193"
---
# <a name="iwmpmediaisidentical-vb-and-c"></a><span data-ttu-id="25f8b-104">Ивмпмедиа. одинаковы (VB и C#)</span><span class="sxs-lookup"><span data-stu-id="25f8b-104">IWMPMedia.isIdentical (VB and C#)</span></span>

<span data-ttu-id="25f8b-105">Свойство « **идентично** » (метод **Get \_ одинаковы** в C#) возвращает значение, указывающее, совпадает ли указанный элемент мультимедиа с текущим.</span><span class="sxs-lookup"><span data-stu-id="25f8b-105">The **isIdentical** property (the **get\_isIdentical** method in C#) gets a value indicating whether the specified media item is the same as the current one.</span></span>


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPMedia As IWMPMedia
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPMedia pIWMPMedia
);
```



## <a name="parameters"></a><span data-ttu-id="25f8b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="25f8b-106">Parameters</span></span>

<span data-ttu-id="25f8b-107">*пивмпмедиа*</span><span class="sxs-lookup"><span data-stu-id="25f8b-107">*pIWMPMedia*</span></span>

<span data-ttu-id="25f8b-108">Интерфейс **вмплиб. ивмпмедиа** для элемента мультимедиа, сравниваемый с текущим элементом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="25f8b-108">A **WMPLib.IWMPMedia** interface to the media item to be compared with the current media item.</span></span>

## <a name="property-value"></a><span data-ttu-id="25f8b-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="25f8b-109">Property Value</span></span>

<span data-ttu-id="25f8b-110">Значение **System. Boolean** , указывающее, идентичны ли два элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="25f8b-110">A **System.Boolean** value that indicates whether the two media items are identical.</span></span>

## <a name="remarks"></a><span data-ttu-id="25f8b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="25f8b-111">Remarks</span></span>

<span data-ttu-id="25f8b-112">**Ивмпмедиа. идентично** — это свойство в Visual Basic, которое принимает параметр.</span><span class="sxs-lookup"><span data-stu-id="25f8b-112">**IWMPMedia.isIdentical** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="25f8b-113">В C# он называется **ивмпмедиа. Get \_ тождественным** методом.</span><span class="sxs-lookup"><span data-stu-id="25f8b-113">In C# it is referred to as the **IWMPMedia.get\_isIdentical** method.</span></span>

## <a name="examples"></a><span data-ttu-id="25f8b-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="25f8b-114">Examples</span></span>

<span data-ttu-id="25f8b-115">В следующем примере используется свойство « **идентично** » (метод **Get \_ одинаковы** в C#), чтобы проверить, совпадает ли элемент мультимедиа с именем невмедиа и текущий элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="25f8b-115">The following example uses the **isIdentical** property (the **get\_isIdentical** method in C#) to check whether a media item named newMedia is the same as the current media item.</span></span> <span data-ttu-id="25f8b-116">Если они не совпадают, будет воспроизведен новый элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="25f8b-116">If they are not the same, the new media item is played.</span></span> <span data-ttu-id="25f8b-117">В противном случае текущий носитель продолжит воспроизводиться без прерывания.</span><span class="sxs-lookup"><span data-stu-id="25f8b-117">Otherwise, the current media continues to play uninterrupted.</span></span> <span data-ttu-id="25f8b-118">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="25f8b-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
if (newMedia.get_isIdentical(player.currentMedia) != true)
{
    // Change the current media to the new media item.
    player.currentMedia = newMedia;

    // Play the new media item.
    player.Ctlcontrols.play();
}
```


```VB

If (newMedia.isIdentical(player.currentMedia) <> True) Then

    &#39; Change the current media to the new media item.
    player.currentMedia = newMedia

    &#39; Play the new media item.
    player.Ctlcontrols.play()

End If
```





## <a name="requirements"></a><span data-ttu-id="25f8b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="25f8b-119">Requirements</span></span>



| <span data-ttu-id="25f8b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="25f8b-120">Requirement</span></span> | <span data-ttu-id="25f8b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="25f8b-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25f8b-122">Версия</span><span class="sxs-lookup"><span data-stu-id="25f8b-122">Version</span></span><br/>   | <span data-ttu-id="25f8b-123">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="25f8b-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="25f8b-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="25f8b-124">Namespace</span></span><br/> | <span data-ttu-id="25f8b-125">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="25f8b-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="25f8b-126">Сборка</span><span class="sxs-lookup"><span data-stu-id="25f8b-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="25f8b-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="25f8b-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25f8b-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25f8b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25f8b-129">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="25f8b-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





