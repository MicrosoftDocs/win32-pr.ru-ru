---
title: Событие Player. Плайлистколлектионплайлистремовед
description: Событие Плайлистколлектионплайлистремовед возникает при удалении списка воспроизведения из коллекции списков воспроизведения. | Событие Player. Плайлистколлектионплайлистремовед
ms.assetid: 2405be98-b4c2-4b4e-bea6-0c48a3e26f18
keywords:
- Проигрыватель Windows Media Event Плайлистколлектионплайлистремовед
- Проигрыватель Windows Media Event Плайлистколлектионплайлистремовед, класс Player
- Класс проигрывателя Windows Media Player, событие Плайлистколлектионплайлистремовед
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a449a7b00516f4fee613722d1cc126eb74227948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708577"
---
# <a name="playerplaylistcollectionplaylistremoved-event"></a><span data-ttu-id="9ae3d-107">Событие Player. Плайлистколлектионплайлистремовед</span><span class="sxs-lookup"><span data-stu-id="9ae3d-107">Player.PlaylistCollectionPlaylistRemoved event</span></span>

<span data-ttu-id="9ae3d-108">Событие **плайлистколлектионплайлистремовед** возникает при удалении списка воспроизведения из коллекции списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="9ae3d-108">The **PlaylistCollectionPlaylistRemoved** event occurs when a playlist is removed from the playlist collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ae3d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ae3d-109">Syntax</span></span>


```JScript
Player.PlaylistCollectionPlaylistRemoved(
  bstrPlaylistName
)
```



## <a name="parameters"></a><span data-ttu-id="9ae3d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ae3d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ae3d-111">*бстрплайлистнаме*</span><span class="sxs-lookup"><span data-stu-id="9ae3d-111">*bstrPlaylistName*</span></span> 
</dt> <dd>

<span data-ttu-id="9ae3d-112">**Строка** , указывающая имя списка воспроизведения, который был удален.</span><span class="sxs-lookup"><span data-stu-id="9ae3d-112">**String** specifying the name of the playlist that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ae3d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ae3d-113">Return value</span></span>

<span data-ttu-id="9ae3d-114">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9ae3d-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ae3d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ae3d-115">Remarks</span></span>

<span data-ttu-id="9ae3d-116">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="9ae3d-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="9ae3d-117">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="9ae3d-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="9ae3d-118">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9ae3d-118">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ae3d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="9ae3d-119">Requirements</span></span>



| <span data-ttu-id="9ae3d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="9ae3d-120">Requirement</span></span> | <span data-ttu-id="9ae3d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="9ae3d-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9ae3d-122">Версия</span><span class="sxs-lookup"><span data-stu-id="9ae3d-122">Version</span></span><br/> | <span data-ttu-id="9ae3d-123">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="9ae3d-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9ae3d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9ae3d-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="9ae3d-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ae3d-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ae3d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ae3d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ae3d-127">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="9ae3d-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="9ae3d-128">**Плайлистколлектион. Жетбинаме**</span><span class="sxs-lookup"><span data-stu-id="9ae3d-128">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





