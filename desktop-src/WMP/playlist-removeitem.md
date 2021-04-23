---
title: Метод списка воспроизведения. removeItem
description: Метод removeItem удаляет указанный элемент из списка воспроизведения.
ms.assetid: 294ba4fb-967b-4a03-b0c5-6e9c15db3bff
keywords:
- removeItem метод Windows Media Player
- removeItem метод Windows Media Player, класс списка воспроизведения
- Класс списка воспроизведения проигрыватель Windows Media Player, метод removeItem
topic_type:
- apiref
api_name:
- Playlist.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de03333e2373744f9e9197be8ed8582997c557d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704389"
---
# <a name="playlistremoveitem-method"></a><span data-ttu-id="a107d-106">Метод списка воспроизведения. removeItem</span><span class="sxs-lookup"><span data-stu-id="a107d-106">Playlist.removeItem method</span></span>

<span data-ttu-id="a107d-107">Метод **RemoveItem** удаляет указанный элемент из списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="a107d-107">The **removeItem** method removes the specified item from the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="a107d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a107d-108">Syntax</span></span>


```JScript
Playlist.removeItem(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="a107d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a107d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a107d-110">*элемент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a107d-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a107d-111">Объект **мультимедиа** для удаления.</span><span class="sxs-lookup"><span data-stu-id="a107d-111">**Media** object to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a107d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a107d-112">Return value</span></span>

<span data-ttu-id="a107d-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a107d-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a107d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a107d-114">Remarks</span></span>

<span data-ttu-id="a107d-115">Если удаляемый элемент является текущей воспроизводимой записью (*Player*.**Куррентмедиа**), воспроизведение останавливается, а следующий элемент списка воспроизведения переходит в текущий.</span><span class="sxs-lookup"><span data-stu-id="a107d-115">If the item removed is the currently playing track (*Player*.**currentMedia**), playback stops and the next item in the playlist becomes the current one.</span></span> <span data-ttu-id="a107d-116">Если следующий элемент отсутствует, используется предыдущий элемент или, если другие элементы отсутствуют, *проигрыватель*. **куррентмедиа** имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="a107d-116">If there is no next item, the previous item is used, or if there are no other items, then *Player*.**currentMedia** is set to **NULL**.</span></span>

<span data-ttu-id="a107d-117">Чтобы использовать этот метод, требуется полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="a107d-117">To use this method, full access to the library is required.</span></span> <span data-ttu-id="a107d-118">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a107d-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a107d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a107d-119">Requirements</span></span>



| <span data-ttu-id="a107d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a107d-120">Requirement</span></span> | <span data-ttu-id="a107d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a107d-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a107d-122">Версия</span><span class="sxs-lookup"><span data-stu-id="a107d-122">Version</span></span><br/> | <span data-ttu-id="a107d-123">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="a107d-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a107d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a107d-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="a107d-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a107d-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a107d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a107d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a107d-127">**Player. Куррентмедиа**</span><span class="sxs-lookup"><span data-stu-id="a107d-127">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="a107d-128">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="a107d-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="a107d-129">**Список воспроизведения. insertItem**</span><span class="sxs-lookup"><span data-stu-id="a107d-129">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="a107d-130">**Список воспроизведения. элемент**</span><span class="sxs-lookup"><span data-stu-id="a107d-130">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="a107d-131">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="a107d-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="a107d-132">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="a107d-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





