---
title: Ивмпмедиа Жетмаркернаме, метод
description: Метод Жетмаркернаме возвращает имя маркера по указанному индексу.
ms.assetid: 77f893cf-1669-41e3-9f62-8a1081e37add
keywords:
- Жетмаркернаме метод Windows Media Player
- Жетмаркернаме метод проигрывателя Windows Media Player, интерфейс Ивмпмедиа
- Интерфейс Ивмпмедиа Windows Media Player, метод Жетмаркернаме
topic_type:
- apiref
api_name:
- IWMPMedia.getMarkerName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6ba6a7bb640a397cce9c7dfd22b5f9b6203c47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669248"
---
# <a name="iwmpmediagetmarkername-method"></a><span data-ttu-id="a01d9-106">Метод Ивмпмедиа:: Жетмаркернаме</span><span class="sxs-lookup"><span data-stu-id="a01d9-106">IWMPMedia::getMarkerName method</span></span>

<span data-ttu-id="a01d9-107">Метод **жетмаркернаме** возвращает имя маркера по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="a01d9-107">The **getMarkerName** method returns the name of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="a01d9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a01d9-108">Syntax</span></span>


```CSharp
public System.String getMarkerName(
  System.Int32 MarkerNum
);
```


```VB

Public Function getMarkerName( _
  ByVal MarkerNum As System.Int32 _
) As System.String
Implements IWMPMedia.getMarkerName
```





## <a name="parameters"></a><span data-ttu-id="a01d9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a01d9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a01d9-110">*Маркернум* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a01d9-110">*MarkerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a01d9-111">Объект **System. Int32** , который является индексом маркера.</span><span class="sxs-lookup"><span data-stu-id="a01d9-111">A **System.Int32** that is the marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a01d9-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a01d9-112">Return value</span></span>

<span data-ttu-id="a01d9-113">**Строка System. String** , которая является именем маркера.</span><span class="sxs-lookup"><span data-stu-id="a01d9-113">A **System.String** that is the marker name.</span></span>

## <a name="remarks"></a><span data-ttu-id="a01d9-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a01d9-114">Remarks</span></span>

<span data-ttu-id="a01d9-115">Этот метод возвращает **значение NULL** , если указанный маркер не существует.</span><span class="sxs-lookup"><span data-stu-id="a01d9-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="a01d9-116">Некоторые элементы мультимедиа не содержат маркеров.</span><span class="sxs-lookup"><span data-stu-id="a01d9-116">Some media items do not contain markers.</span></span> <span data-ttu-id="a01d9-117">Используйте **маркеркаунт** , чтобы узнать, сколько маркеров находится в текущем элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a01d9-117">Use **markerCount** to find out how many markers are in the current media item.</span></span>

<span data-ttu-id="a01d9-118">Номера индексов маркеров начинаются с 1.</span><span class="sxs-lookup"><span data-stu-id="a01d9-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="a01d9-119">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="a01d9-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="a01d9-120">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a01d9-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a01d9-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="a01d9-121">Examples</span></span>

<span data-ttu-id="a01d9-122">В следующем примере кода используется **жетмаркернаме** для заполнения многострочного текстового поля с именами маркеров в текущем элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a01d9-122">The following code example uses **getMarkerName** to fill a multi-line text box with the names of the markers in the current media item.</span></span> <span data-ttu-id="a01d9-123">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="a01d9-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of marker names
string[] markers = new string[mcount];

// Verify that at least one marker exists in the current media.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markers[i] = player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerNames.Lines = markers;
}
```


```VB

' Get the number of markers in the current media item.
Dim mCount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of marker names
Dim markers(mCount) As String

&#39; Verify that at least one marker exists in the current media.
If (mCount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mCount

        &#39; Store the marker name in the array.
        markers(i) = player.currentMedia.getMarkerName(i)

    Next i

End If

&#39; Display the marker names in the text box.
markerNames.Lines = markers
```





## <a name="requirements"></a><span data-ttu-id="a01d9-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a01d9-124">Requirements</span></span>



| <span data-ttu-id="a01d9-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a01d9-125">Requirement</span></span> | <span data-ttu-id="a01d9-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a01d9-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a01d9-127">Версия</span><span class="sxs-lookup"><span data-stu-id="a01d9-127">Version</span></span><br/>   | <span data-ttu-id="a01d9-128">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a01d9-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a01d9-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a01d9-129">Namespace</span></span><br/> | <span data-ttu-id="a01d9-130">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="a01d9-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a01d9-131">Сборка</span><span class="sxs-lookup"><span data-stu-id="a01d9-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a01d9-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a01d9-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a01d9-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a01d9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a01d9-134">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a01d9-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a01d9-135">**Ивмпмедиа. Маркеркаунт (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a01d9-135">**IWMPMedia.markerCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





