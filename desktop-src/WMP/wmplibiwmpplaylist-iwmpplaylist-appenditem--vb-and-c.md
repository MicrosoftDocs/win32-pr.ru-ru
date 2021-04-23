---
title: Ивмпплайлист Аппендитем, метод
description: Метод Аппендитем добавляет элемент мультимедиа в конец списка воспроизведения.
ms.assetid: d659298b-ec4e-4771-8e9b-8cfd7b3e0eb2
keywords:
- Аппендитем метод Windows Media Player
- Аппендитем метод проигрывателя Windows Media Player, интерфейс Ивмпплайлист
- Интерфейс Ивмпплайлист Windows Media Player, метод Аппендитем
topic_type:
- apiref
api_name:
- IWMPPlaylist.appendItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a94e1b515ec6301830af2de06bae32602bdf66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708496"
---
# <a name="iwmpplaylistappenditem-method"></a><span data-ttu-id="cb24d-106">Метод Ивмпплайлист:: Аппендитем</span><span class="sxs-lookup"><span data-stu-id="cb24d-106">IWMPPlaylist::appendItem method</span></span>

<span data-ttu-id="cb24d-107">Метод **аппендитем** добавляет элемент мультимедиа в конец списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="cb24d-107">The **appendItem** method adds a media item to the end of a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb24d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb24d-108">Syntax</span></span>


```CSharp
public void appendItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub appendItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.appendItem
```





## <a name="parameters"></a><span data-ttu-id="cb24d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb24d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb24d-110">*пивмпмедиа* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cb24d-110">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb24d-111">Интерфейс **вмплиб. ивмпмедиа** , представляющий добавляемый элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cb24d-111">An **WMPLib.IWMPMedia** interface that represents the media item to be appended.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb24d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb24d-112">Return value</span></span>

<span data-ttu-id="cb24d-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cb24d-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb24d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb24d-114">Remarks</span></span>

<span data-ttu-id="cb24d-115">Перед вызовом этого метода необходимо иметь полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="cb24d-115">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="cb24d-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="cb24d-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="cb24d-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="cb24d-117">Examples</span></span>

<span data-ttu-id="cb24d-118">В следующем примере **аппендитем** используется для добавления текущего элемента мультимедиа в список воспроизведения с именем «срилист».</span><span class="sxs-lookup"><span data-stu-id="cb24d-118">The following example uses **appendItem** to add the current media item to the playlist named "ThreeList".</span></span> <span data-ttu-id="cb24d-119">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="cb24d-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the current media item.
WMPLib.IWMPMedia currMedia = player.currentMedia;

// Get an interface to the playlist named "ThreeList".
WMPLib.IWMPPlaylist plThreeList = player.playlistCollection.getByName("ThreeList").Item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);
```


```VB

' Get an interface to the current media item.
Dim currMedia As WMPLib.IWMPMedia = player.currentMedia

&#39; Get an interface to the playlist named &quot;ThreeList&quot;.
Dim plThreeList As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;ThreeList&quot;).Item(0)

&#39; Append the media item to the playlist.
plThreeList.appendItem(currMedia)
```





## <a name="requirements"></a><span data-ttu-id="cb24d-120">Требования</span><span class="sxs-lookup"><span data-stu-id="cb24d-120">Requirements</span></span>



| <span data-ttu-id="cb24d-121">Требование</span><span class="sxs-lookup"><span data-stu-id="cb24d-121">Requirement</span></span> | <span data-ttu-id="cb24d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="cb24d-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb24d-123">Версия</span><span class="sxs-lookup"><span data-stu-id="cb24d-123">Version</span></span><br/>   | <span data-ttu-id="cb24d-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="cb24d-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="cb24d-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cb24d-125">Namespace</span></span><br/> | <span data-ttu-id="cb24d-126">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="cb24d-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cb24d-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="cb24d-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cb24d-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cb24d-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb24d-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb24d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb24d-130">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="cb24d-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cb24d-131">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="cb24d-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





