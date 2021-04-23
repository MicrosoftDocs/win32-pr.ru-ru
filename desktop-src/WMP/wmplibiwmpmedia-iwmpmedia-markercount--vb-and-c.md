---
title: Ивмпмедиа Маркеркаунт, свойство
description: Свойство Маркеркаунт возвращает количество маркеров в элементе мультимедиа.
ms.assetid: d1ccaa9b-98fb-4c53-8064-ee4bf718d18a
keywords:
- Проигрыватель Windows Media для свойства Маркеркаунт
- Маркеркаунт свойство проигрывателя Windows Media Player, интерфейс Ивмпмедиа
- Интерфейс Ивмпмедиа Windows Media Player, свойство Маркеркаунт
topic_type:
- apiref
api_name:
- IWMPMedia.markerCount
- IWMPMedia.get_markerCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdad591d8be66dcd20bc5e59d206a637d9b1181f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669242"
---
# <a name="iwmpmediamarkercount-property"></a><span data-ttu-id="0228f-106">Свойство Ивмпмедиа:: Маркеркаунт</span><span class="sxs-lookup"><span data-stu-id="0228f-106">IWMPMedia::markerCount property</span></span>

<span data-ttu-id="0228f-107">Свойство **маркеркаунт** возвращает количество маркеров в элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0228f-107">The **markerCount** property gets the number of markers in the media item.</span></span>

<span data-ttu-id="0228f-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0228f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0228f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0228f-109">Syntax</span></span>


```CSharp
public System.Int32 markerCount {get;}
```


```VB

Public ReadOnly Property markerCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="0228f-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0228f-110">Property value</span></span>

<span data-ttu-id="0228f-111">Значение **System. Int32** , которое является счетчиком маркеров.</span><span class="sxs-lookup"><span data-stu-id="0228f-111">A **System.Int32** that is the marker count.</span></span>

## <a name="remarks"></a><span data-ttu-id="0228f-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0228f-112">Remarks</span></span>

<span data-ttu-id="0228f-113">Это свойство возвращает нуль, если файл не имеет маркеров, или если элемент мультимедиа не совпадает с указанным в Аксвиндовсмедиаплайер. Куррентмедиа.</span><span class="sxs-lookup"><span data-stu-id="0228f-113">This property returns zero if a file has no markers, or if the media item is not the same as the one specified in AxWindowsMediaPlayer.currentMedia.</span></span>

<span data-ttu-id="0228f-114">Номера маркеров начинаются с 1.</span><span class="sxs-lookup"><span data-stu-id="0228f-114">Marker numbers start at 1.</span></span>

<span data-ttu-id="0228f-115">Перед использованием этого свойства необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="0228f-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="0228f-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="0228f-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0228f-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="0228f-117">Examples</span></span>

<span data-ttu-id="0228f-118">В следующем примере **маркеркаунт** используется для получения количества маркеров в текущем элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0228f-118">The following example uses **markerCount** to retrieve the number of markers in the current media item.</span></span> <span data-ttu-id="0228f-119">Это значение затем используется в качестве верхней границы для циклической структуры, которая выполняет итерацию по списку маркеров для получения каждого имени маркера и отображает его в многострочном текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="0228f-119">That value is then used as the upper boundary for a looping structure, which iterates through the marker list to retrieve each marker name and display it in a multi-line text box.</span></span> <span data-ttu-id="0228f-120">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="0228f-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of markers.
string[] markerNames = new string[mcount];

// Verify that at least one marker exists in the current media item.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markerNames[i]= player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerList.Lines = markerNames;            
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of markers.
Dim markerNames(mcount) As String

&#39; Verify that at least one marker exists in the current media item.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker name in the array.
        markerNames(i) = player.currentMedia.getMarkerName(i)

    Next i

    &#39; Display the marker names in the text box.
    markerList.Lines = markerNames

End If
```





## <a name="requirements"></a><span data-ttu-id="0228f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0228f-121">Requirements</span></span>



| <span data-ttu-id="0228f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0228f-122">Requirement</span></span> | <span data-ttu-id="0228f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0228f-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0228f-124">Версия</span><span class="sxs-lookup"><span data-stu-id="0228f-124">Version</span></span><br/>   | <span data-ttu-id="0228f-125">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="0228f-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0228f-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0228f-126">Namespace</span></span><br/> | <span data-ttu-id="0228f-127">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="0228f-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0228f-128">Сборка</span><span class="sxs-lookup"><span data-stu-id="0228f-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0228f-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0228f-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0228f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0228f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0228f-131">**Аксвиндовсмедиаплайер. Куррентмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="0228f-131">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0228f-132">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="0228f-132">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





