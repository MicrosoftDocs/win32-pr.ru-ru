---
title: Ивмпмедиа Жетмаркертиме, метод
description: Метод Жетмаркертиме Возвращает время маркера по указанному индексу.
ms.assetid: 1c617e3a-0978-479c-a636-b655082232c1
keywords:
- Жетмаркертиме метод Windows Media Player
- Жетмаркертиме метод проигрывателя Windows Media Player, интерфейс Ивмпмедиа
- Интерфейс Ивмпмедиа Windows Media Player, метод Жетмаркертиме
topic_type:
- apiref
api_name:
- IWMPMedia.getMarkerTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df171977adeee3b597cab1f40469af1d975425c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669247"
---
# <a name="iwmpmediagetmarkertime-method"></a><span data-ttu-id="b6902-106">Метод Ивмпмедиа:: Жетмаркертиме</span><span class="sxs-lookup"><span data-stu-id="b6902-106">IWMPMedia::getMarkerTime method</span></span>

<span data-ttu-id="b6902-107">Метод **жетмаркертиме** Возвращает время маркера по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="b6902-107">The **getMarkerTime** method returns the time of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6902-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6902-108">Syntax</span></span>


```CSharp
public System.Double getMarkerTime(
  System.Int32 MarkerNum
);
```


```VB

Public Function getMarkerTime( _
  ByVal MarkerNum As System.Int32 _
) As System.Double
Implements IWMPMedia.getMarkerTime
```





## <a name="parameters"></a><span data-ttu-id="b6902-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6902-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6902-110">*Маркернум* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b6902-110">*MarkerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6902-111">Объект **System. Int32** , который является индексом маркера.</span><span class="sxs-lookup"><span data-stu-id="b6902-111">A **System.Int32** that is the marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6902-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6902-112">Return value</span></span>

<span data-ttu-id="b6902-113">Значение **System. Double** , которое является временем метки.</span><span class="sxs-lookup"><span data-stu-id="b6902-113">A **System.Double** that is the marker time.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6902-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6902-114">Remarks</span></span>

<span data-ttu-id="b6902-115">Этот метод возвращает **значение NULL** , если указанный маркер не существует.</span><span class="sxs-lookup"><span data-stu-id="b6902-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="b6902-116">Некоторые элементы мультимедиа не содержат маркеров.</span><span class="sxs-lookup"><span data-stu-id="b6902-116">Some media items do not contain markers.</span></span> <span data-ttu-id="b6902-117">Используйте **маркеркаунт** , чтобы узнать, сколько маркеров находится в текущем элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b6902-117">Use **markerCount** to find out how many markers are in the current media item.</span></span>

<span data-ttu-id="b6902-118">Номера индексов маркеров начинаются с 1.</span><span class="sxs-lookup"><span data-stu-id="b6902-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="b6902-119">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="b6902-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="b6902-120">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b6902-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b6902-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="b6902-121">Examples</span></span>

<span data-ttu-id="b6902-122">В следующем примере кода используется **жетмаркертиме** для заполнения многострочного текстового поля с расположением каждого маркера.</span><span class="sxs-lookup"><span data-stu-id="b6902-122">The following code example uses **getMarkerTime** to fill a multi-line text box with the location of each marker.</span></span> <span data-ttu-id="b6902-123">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="b6902-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of marker times.
string[] markers = new string[mcount];

// Verify that at least one marker exists in the current media.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker information in the array.
        markers[i] = "Marker number " + i + " occurs at ";
        markers[i] += player.currentMedia.getMarkerTime(i).ToString();
        markers[i] += " second(s).";
    }

    // Display the marker times in the text box.
    markerTimes.Lines = markers;
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of marker times.
Dim markers(mcount) As String

&#39; Verify that at least one marker exists in the current media.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker information in the array.
        markers(i) = (&quot;Marker number &quot; + i + &quot; occurs at &quot;)
        markers(i) += player.currentMedia.getMarkerTime(i).ToString()
        markers(i) += &quot; second(s).&quot;

    Next i

    &#39; Display the marker times in the text box.
    markerTimes.Lines = markers

End If
```





## <a name="requirements"></a><span data-ttu-id="b6902-124">Требования</span><span class="sxs-lookup"><span data-stu-id="b6902-124">Requirements</span></span>



| <span data-ttu-id="b6902-125">Требование</span><span class="sxs-lookup"><span data-stu-id="b6902-125">Requirement</span></span> | <span data-ttu-id="b6902-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b6902-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6902-127">Версия</span><span class="sxs-lookup"><span data-stu-id="b6902-127">Version</span></span><br/>   | <span data-ttu-id="b6902-128">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b6902-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b6902-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b6902-129">Namespace</span></span><br/> | <span data-ttu-id="b6902-130">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="b6902-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b6902-131">Сборка</span><span class="sxs-lookup"><span data-stu-id="b6902-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b6902-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b6902-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6902-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6902-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6902-134">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b6902-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b6902-135">**Ивмпмедиа. Маркеркаунт (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b6902-135">**IWMPMedia.markerCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





