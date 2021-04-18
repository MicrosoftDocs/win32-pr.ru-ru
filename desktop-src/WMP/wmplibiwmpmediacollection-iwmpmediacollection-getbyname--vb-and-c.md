---
title: Ивмпмедиаколлектион Жетбинаме, метод
description: Метод Жетбинаме возвращает интерфейс Ивмпплайлист, предоставляющий доступ к элементам мультимедиа с указанным именем.
ms.assetid: 137e938c-eb9f-4a87-8962-880e71a11ca2
keywords:
- Жетбинаме метод Windows Media Player
- Жетбинаме метод проигрывателя Windows Media Player, интерфейс Ивмпмедиаколлектион
- Интерфейс Ивмпмедиаколлектион Windows Media Player, метод Жетбинаме
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64c68e2a5359eadf9c6212571ed948c103c01bdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669421"
---
# <a name="iwmpmediacollectiongetbyname-method"></a><span data-ttu-id="c292a-106">Метод Ивмпмедиаколлектион:: Жетбинаме</span><span class="sxs-lookup"><span data-stu-id="c292a-106">IWMPMediaCollection::getByName method</span></span>

<span data-ttu-id="c292a-107">`getByName`Метод возвращает интерфейс **ивмпплайлист** , предоставляющий доступ к элементам мультимедиа с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="c292a-107">The `getByName` method returns an **IWMPPlaylist** interface that provides access to media items with the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="c292a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c292a-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByName(
  System.String bstrName
);
```


```VB

Public Function getByName( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByName
```





## <a name="parameters"></a><span data-ttu-id="c292a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c292a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c292a-110">*bstrName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c292a-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c292a-111">**Строка System. String** , которая является заданным именем.</span><span class="sxs-lookup"><span data-stu-id="c292a-111">The **System.String** that is the specified name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c292a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c292a-112">Return value</span></span>

<span data-ttu-id="c292a-113">Интерфейс **вмплиб. ивмпплайлист** для извлеченных элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c292a-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="c292a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c292a-114">Remarks</span></span>

<span data-ttu-id="c292a-115">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="c292a-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="c292a-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c292a-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="c292a-117">Существует два способа получения интерфейса **ивмпмедиаколлектион** , и поведение `getByName` метода зависит от того, какой из этих двух способов вы используете.</span><span class="sxs-lookup"><span data-stu-id="c292a-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the `getByName` method depends on which of those two ways you use.</span></span> <span data-ttu-id="c292a-118">При получении интерфейса путем вызова [аксвиндовсмедиаплайер. медиаколлектион](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) `getByName` метод возвращает все элементы мультимедиа в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="c292a-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the `getByName` method returns all the media items in the library.</span></span> <span data-ttu-id="c292a-119">Однако при получении интерфейса путем вызова [ивмплибрари. медиаколлектион](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) `getByName` метод возвращает только звуковые элементы в библиотеке с указанным атрибутом и значением.</span><span class="sxs-lookup"><span data-stu-id="c292a-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the `getByName` method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="c292a-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="c292a-120">Examples</span></span>

<span data-ttu-id="c292a-121">В следующем примере используется `getByName` для получения трех элементов из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="c292a-121">The following example uses `getByName` to retrieve three items from the library.</span></span> <span data-ttu-id="c292a-122">Затем каждый элемент добавляется к текущему списку воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="c292a-122">Each item is then appended to the current playlist.</span></span> <span data-ttu-id="c292a-123">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="c292a-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// In each case, use the name exactly as it appears in the library.
// Windows Media Player does not include file name extensions or file paths
// in the name. Internet URLs include the entire path, but not the 
// file name extension.

// Get an interface to a playlist that contains an Internet URL.
WMPLib.IWMPPlaylist one = player.mediaCollection.getByName("https://www.proseware.com/Media/Laure");

// Get an interface to a playlist that contains a file on a network server.
WMPLib.IWMPPlaylist two = player.mediaCollection.getByName("Jeanne");

// Get an interface to a playlist that contains a file on a local drive.
WMPLib.IWMPPlaylist three = player.mediaCollection.getByName("house");

// Append each item to the current playlist. Since each playlist retrieved
// using getByName contains one digital media item, use the get_Item
// method with an index of zero to reference that item.
player.currentPlaylist.appendItem(one.get_Item(0));
player.currentPlaylist.appendItem(two.get_Item(0));
player.currentPlaylist.appendItem(three.get_Item(0));
```


```VB

' In each case, use the name exactly as it appears in the library.
&#39; Windows Media Player does not include file name extensions or file paths
&#39; in the name. Internet URLs include the entire path, but not the 
&#39; file name extension.

&#39; Get an interface to a playlist that contains an Internet URL.
Dim one As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;https://www.proseware.com/Media/Laure&quot;)

&#39; Get an interface to a playlist that contains a file on a network server.
Dim two As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;Jeanne&quot;)

&#39; Get an interface to a playlist that contains a file on a local drive.
Dim three As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;house&quot;)

&#39; Append each item to the current playlist. Since each playlist retrieved
&#39; using getByName contains one digital media item, use the Item
&#39; property with an index of zero to reference that item.
player.currentPlaylist.appendItem(one.Item(0))
player.currentPlaylist.appendItem(two.Item(0))
player.currentPlaylist.appendItem(three.Item(0))
```





## <a name="requirements"></a><span data-ttu-id="c292a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="c292a-124">Requirements</span></span>



| <span data-ttu-id="c292a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="c292a-125">Requirement</span></span> | <span data-ttu-id="c292a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c292a-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c292a-127">Версия</span><span class="sxs-lookup"><span data-stu-id="c292a-127">Version</span></span><br/>   | <span data-ttu-id="c292a-128">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="c292a-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c292a-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c292a-129">Namespace</span></span><br/> | <span data-ttu-id="c292a-130">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="c292a-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c292a-131">Сборка</span><span class="sxs-lookup"><span data-stu-id="c292a-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c292a-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c292a-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c292a-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c292a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c292a-134">**Интерфейс Ивмпмедиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="c292a-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c292a-135">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="c292a-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





