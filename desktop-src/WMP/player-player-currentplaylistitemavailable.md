---
title: Событие Player. Куррентплайлиститемаваилабле
description: Событие Куррентплайлиститемаваилабле возникает, когда текущий список воспроизведения станет доступным. | Событие Player. Куррентплайлиститемаваилабле
ms.assetid: 4894e2fc-3464-413f-8abf-8b5e91899946
keywords:
- Проигрыватель Windows Media Event Куррентплайлиститемаваилабле
- Проигрыватель Windows Media Event Куррентплайлиститемаваилабле, класс Player
- Класс проигрывателя Windows Media Player, событие Куррентплайлиститемаваилабле
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe5809e50d572cfb8eb7a36220d083ec18a0a76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704506"
---
# <a name="playercurrentplaylistitemavailable-event"></a><span data-ttu-id="a3eb2-107">Событие Player. Куррентплайлиститемаваилабле</span><span class="sxs-lookup"><span data-stu-id="a3eb2-107">Player.CurrentPlaylistItemAvailable event</span></span>

<span data-ttu-id="a3eb2-108">Событие **куррентплайлиститемаваилабле** возникает, когда текущий список воспроизведения станет доступным.</span><span class="sxs-lookup"><span data-stu-id="a3eb2-108">The **CurrentPlaylistItemAvailable** event occurs when the current playlist becomes available.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3eb2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3eb2-109">Syntax</span></span>


```JScript
Player.CurrentPlaylistItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a><span data-ttu-id="a3eb2-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3eb2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3eb2-111">*бстритемнаме*</span><span class="sxs-lookup"><span data-stu-id="a3eb2-111">*bstrItemName*</span></span> 
</dt> <dd>

<span data-ttu-id="a3eb2-112">**Строка** , содержащая имя текущего элемента списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="a3eb2-112">**String** containing the name of the current playlist item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3eb2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3eb2-113">Return value</span></span>

<span data-ttu-id="a3eb2-114">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a3eb2-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3eb2-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3eb2-115">Remarks</span></span>

<span data-ttu-id="a3eb2-116">Имя текущего списка воспроизведения можно использовать для получения соответствующего объекта **списка воспроизведения** с помощью *плайлистколлектион*. метод **жетбинаме** .</span><span class="sxs-lookup"><span data-stu-id="a3eb2-116">The name of the current playlist can be used to retrieve the corresponding **Playlist** object using the *PlaylistCollection*.**getByName** method.</span></span>

<span data-ttu-id="a3eb2-117">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="a3eb2-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="a3eb2-118">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="a3eb2-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="a3eb2-119">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a3eb2-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3eb2-120">Требования</span><span class="sxs-lookup"><span data-stu-id="a3eb2-120">Requirements</span></span>



| <span data-ttu-id="a3eb2-121">Требование</span><span class="sxs-lookup"><span data-stu-id="a3eb2-121">Requirement</span></span> | <span data-ttu-id="a3eb2-122">Значение</span><span class="sxs-lookup"><span data-stu-id="a3eb2-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3eb2-123">Версия</span><span class="sxs-lookup"><span data-stu-id="a3eb2-123">Version</span></span><br/> | <span data-ttu-id="a3eb2-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="a3eb2-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a3eb2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a3eb2-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="a3eb2-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3eb2-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3eb2-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3eb2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3eb2-128">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="a3eb2-128">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="a3eb2-129">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="a3eb2-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="a3eb2-130">**Плайлистколлектион. Жетбинаме**</span><span class="sxs-lookup"><span data-stu-id="a3eb2-130">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





