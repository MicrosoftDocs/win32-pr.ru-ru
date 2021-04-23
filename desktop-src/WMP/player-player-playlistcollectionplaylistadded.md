---
title: Событие Player. Плайлистколлектионплайлистаддед
description: Событие Плайлистколлектионплайлистаддед возникает при добавлении списка воспроизведения в коллекцию списков воспроизведения. | Событие Player. Плайлистколлектионплайлистаддед
ms.assetid: 07acb5e6-d832-4f0b-a6bb-2b7ba27c368d
keywords:
- Проигрыватель Windows Media Event Плайлистколлектионплайлистаддед
- Проигрыватель Windows Media Event Плайлистколлектионплайлистаддед, класс Player
- Класс проигрывателя Windows Media Player, событие Плайлистколлектионплайлистаддед
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e6a229aff95d29ae93433dab538521d88c50c1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704533"
---
# <a name="playerplaylistcollectionplaylistadded-event"></a><span data-ttu-id="a4d16-107">Событие Player. Плайлистколлектионплайлистаддед</span><span class="sxs-lookup"><span data-stu-id="a4d16-107">Player.PlaylistCollectionPlaylistAdded event</span></span>

<span data-ttu-id="a4d16-108">Событие **плайлистколлектионплайлистаддед** возникает при добавлении списка воспроизведения в коллекцию списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="a4d16-108">The **PlaylistCollectionPlaylistAdded** event occurs when a playlist is added to the playlist collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4d16-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4d16-109">Syntax</span></span>


```JScript
Player.PlaylistCollectionPlaylistAdded(
  bstrPlaylistName
)
```



## <a name="parameters"></a><span data-ttu-id="a4d16-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4d16-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4d16-111">*бстрплайлистнаме*</span><span class="sxs-lookup"><span data-stu-id="a4d16-111">*bstrPlaylistName*</span></span> 
</dt> <dd>

<span data-ttu-id="a4d16-112">**Строка** , указывающая имя добавленного списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="a4d16-112">**String** specifying the name of the playlist that was added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4d16-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4d16-113">Return value</span></span>

<span data-ttu-id="a4d16-114">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a4d16-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4d16-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4d16-115">Remarks</span></span>

<span data-ttu-id="a4d16-116">Имя добавленного списка воспроизведения можно использовать для получения соответствующего объекта **списка воспроизведения** с помощью *плайлистколлектион*. метод **жетбинаме** .</span><span class="sxs-lookup"><span data-stu-id="a4d16-116">The name of the playlist that was added can be used to retrieve the corresponding **Playlist** object using the *PlaylistCollection*.**getByName** method.</span></span>

<span data-ttu-id="a4d16-117">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="a4d16-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="a4d16-118">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="a4d16-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="a4d16-119">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a4d16-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4d16-120">Требования</span><span class="sxs-lookup"><span data-stu-id="a4d16-120">Requirements</span></span>



| <span data-ttu-id="a4d16-121">Требование</span><span class="sxs-lookup"><span data-stu-id="a4d16-121">Requirement</span></span> | <span data-ttu-id="a4d16-122">Значение</span><span class="sxs-lookup"><span data-stu-id="a4d16-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a4d16-123">Версия</span><span class="sxs-lookup"><span data-stu-id="a4d16-123">Version</span></span><br/> | <span data-ttu-id="a4d16-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="a4d16-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a4d16-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a4d16-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="a4d16-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4d16-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4d16-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4d16-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4d16-128">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="a4d16-128">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="a4d16-129">**Плайлистколлектион. Жетбинаме**</span><span class="sxs-lookup"><span data-stu-id="a4d16-129">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





