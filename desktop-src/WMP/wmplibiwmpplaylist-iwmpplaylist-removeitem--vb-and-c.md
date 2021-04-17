---
title: Ивмпплайлист removeItem, метод
description: Метод removeItem удаляет указанный элемент мультимедиа из списка воспроизведения.
ms.assetid: 8b5a4c34-863d-4963-97c8-cc5aa2223ab5
keywords:
- removeItem метод Windows Media Player
- removeItem метод проигрывателя Windows Media Player, интерфейс Ивмпплайлист
- Интерфейс Ивмпплайлист Windows Media Player, метод removeItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.removeItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec845b7657e04f17c47119dd169032ebe5815786
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704179"
---
# <a name="iwmpplaylistremoveitem-method"></a><span data-ttu-id="2b4a4-106">Метод Ивмпплайлист:: removeItem</span><span class="sxs-lookup"><span data-stu-id="2b4a4-106">IWMPPlaylist::removeItem method</span></span>

<span data-ttu-id="2b4a4-107">Метод **RemoveItem** удаляет указанный элемент мультимедиа из списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-107">The **removeItem** method removes the specified media item from the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b4a4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b4a4-108">Syntax</span></span>


```CSharp
public void removeItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub removeItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.removeItem
```





## <a name="parameters"></a><span data-ttu-id="2b4a4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b4a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b4a4-110">*пивмпмедиа* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b4a4-110">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b4a4-111">Интерфейс **вмплиб. ивмпмедиа** , представляющий элемент мультимедиа, который необходимо удалить из списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-111">A **WMPLib.IWMPMedia** interface that represents the media item to remove from the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b4a4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b4a4-112">Return value</span></span>

<span data-ttu-id="2b4a4-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b4a4-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b4a4-114">Remarks</span></span>

<span data-ttu-id="2b4a4-115">Если элемент удален в текущий момент, воспроизведение останавливается, а следующий элемент списка воспроизведения становится текущим.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-115">If the item removed is the currently playing track, playback stops and the next item in the playlist becomes the current one.</span></span>

<span data-ttu-id="2b4a4-116">Если следующий элемент отсутствует, используется предыдущий элемент.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-116">If there is no next item, the previous item is used.</span></span> <span data-ttu-id="2b4a4-117">Если других элементов нет, свойство **аксвиндовсмедиаплайер. куррентмедиа** вернет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-117">If there are no other items, then the **AxWindowsMediaPlayer.currentMedia** property will return **NULL**.</span></span>

<span data-ttu-id="2b4a4-118">Перед вызовом этого метода необходимо иметь полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="2b4a4-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="2b4a4-119">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2b4a4-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b4a4-120">Требования</span><span class="sxs-lookup"><span data-stu-id="2b4a4-120">Requirements</span></span>



| <span data-ttu-id="2b4a4-121">Требование</span><span class="sxs-lookup"><span data-stu-id="2b4a4-121">Requirement</span></span> | <span data-ttu-id="2b4a4-122">Значение</span><span class="sxs-lookup"><span data-stu-id="2b4a4-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b4a4-123">Версия</span><span class="sxs-lookup"><span data-stu-id="2b4a4-123">Version</span></span><br/>   | <span data-ttu-id="2b4a4-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2b4a4-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2b4a4-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2b4a4-125">Namespace</span></span><br/> | <span data-ttu-id="2b4a4-126">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="2b4a4-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2b4a4-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="2b4a4-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2b4a4-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2b4a4-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b4a4-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b4a4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b4a4-130">**Аксвиндовсмедиаплайер. Куррентмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2b4a4-130">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b4a4-131">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2b4a4-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b4a4-132">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2b4a4-132">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b4a4-133">**Ивмпплайлист. insertItem (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2b4a4-133">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b4a4-134">**Ивмпплайлист. Item (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2b4a4-134">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b4a4-135">**IWMPSettings2. Медиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2b4a4-135">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b4a4-136">**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2b4a4-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





