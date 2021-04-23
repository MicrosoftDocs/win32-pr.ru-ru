---
title: Носитель. Длительность
description: Свойство Duration извлекает продолжительность текущего элемента мультимедиа за считанные секунды.
ms.assetid: d7d36858-812d-471b-84ce-fe2ab96b86b3
keywords:
- Media. Duration проигрывателя Windows Media
topic_type:
- apiref
api_name:
- Media.duration
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71586f6aa37401d56a9e9537bfbea6c5af23f318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708450"
---
# <a name="mediaduration"></a><span data-ttu-id="1696e-104">Носитель. Длительность</span><span class="sxs-lookup"><span data-stu-id="1696e-104">Media.duration</span></span>

<span data-ttu-id="1696e-105">Свойство **Duration** извлекает продолжительность текущего элемента мультимедиа за считанные секунды.</span><span class="sxs-lookup"><span data-stu-id="1696e-105">The **duration** property retrieves the duration of the current media item in seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="1696e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1696e-106">Syntax</span></span>

<span data-ttu-id="1696e-107">*проигрыватель*. *куррентмедиа*. **Длительность**</span><span class="sxs-lookup"><span data-stu-id="1696e-107">*player*.*currentMedia*.**duration**</span></span>

## <a name="possible-values"></a><span data-ttu-id="1696e-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="1696e-108">Possible Values</span></span>

<span data-ttu-id="1696e-109">Это свойство является **числом** только для чтения ( **Double**).</span><span class="sxs-lookup"><span data-stu-id="1696e-109">This property is a read-only **Number** ( **double**).</span></span>

## <a name="remarks"></a><span data-ttu-id="1696e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1696e-110">Remarks</span></span>

<span data-ttu-id="1696e-111">Если это свойство используется с элементом мультимедиа, отличным от указанного в *проигрывателе*. **куррентмедиа**, он может не содержать допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="1696e-111">If this property is used with a media item other than the one specified in *Player*.**currentMedia**, it may not contain a valid value.</span></span>

<span data-ttu-id="1696e-112">Чтобы получить длительность для файлов, которые не находятся в библиотеке пользователя, необходимо подождать, пока проигрыватель Windows Media откроет этот файл. то есть текущий Опенстате должен равняться Медиаопен.</span><span class="sxs-lookup"><span data-stu-id="1696e-112">To retrieve the duration for files that are not in the user's library, you must wait for Windows Media Player to open the file; that is, the current OpenState must equal MediaOpen.</span></span> <span data-ttu-id="1696e-113">Это можно проверить, обрабатывая *проигрыватель*. Событие **опенстатечанже** или путем периодической проверки значения *игрока*. **опенстате**.</span><span class="sxs-lookup"><span data-stu-id="1696e-113">You can verify this by handling the *Player*.**OpenStateChange** event or by periodically checking the value of *Player*.**openState**.</span></span>

<span data-ttu-id="1696e-114">Для списков воспроизведения продолжительность каждого элемента мультимедиа может быть получена при открытии отдельного элемента мультимедиа, а не при открытии списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="1696e-114">For playlists, the duration of each media item can be retrieved when the individual media item is opened, rather than the when the playlist is opened.</span></span>

<span data-ttu-id="1696e-115">Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="1696e-115">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="1696e-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1696e-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="1696e-117">В следующем примере JScript используется *носитель*. **Длительность** для показа времени, оставшегося в текущем элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1696e-117">The following JScript example uses *Media*.**duration** to display the time remaining in the current media item.</span></span> <span data-ttu-id="1696e-118">В элементе HTML DIV с именем Ремтиме отображаются сведения.</span><span class="sxs-lookup"><span data-stu-id="1696e-118">An HTML DIV element named RemTime displays the information.</span></span> <span data-ttu-id="1696e-119">Таймер HTML обновляет текст в элементе DIV каждую секунду.</span><span class="sxs-lookup"><span data-stu-id="1696e-119">An HTML timer updates the text in the DIV element every second.</span></span>

<span data-ttu-id="1696e-120">Таймер запускается в следующем коде JScript:</span><span class="sxs-lookup"><span data-stu-id="1696e-120">The following JScript code starts the timer:</span></span>


```JScript
// Execute the update() function at one-second intervals.
idTmr = window.setInterval("update()",1000);
```



<span data-ttu-id="1696e-121">Следующий код JScript останавливает таймер:</span><span class="sxs-lookup"><span data-stu-id="1696e-121">The following JScript code stops the timer:</span></span>


```JScript
window.clearInterval(idTmr);
```



<span data-ttu-id="1696e-122">Используйте *проигрыватель*. Событие **плайстатечанже** с инструкцией **switch** , чтобы определить время запуска и завершения таймера.</span><span class="sxs-lookup"><span data-stu-id="1696e-122">Use the *Player*.**PlayStateChange** event with a **switch** statement to determine when to start and stop the timer.</span></span>

<span data-ttu-id="1696e-123">Следующий код JScript выполняется каждый раз, когда таймер вызывает функцию Update:</span><span class="sxs-lookup"><span data-stu-id="1696e-123">The following JScript code executes each time the timer calls the update function:</span></span>


```JScript
// Store the current position of the current media item.
var TimeNow = Player.controls.currentPosition;

// Display the time remaining information.
RemTime.innerHTML = "Seconds remaining: ";

// Subtract the current position from the duration of the current media.
// Use the Math.floor method to round the result down to the nearest integer.
RemTime.innerHTML += Math.floor(Player.currentMedia.duration - TimeNow);
```



## <a name="requirements"></a><span data-ttu-id="1696e-124">Требования</span><span class="sxs-lookup"><span data-stu-id="1696e-124">Requirements</span></span>



| <span data-ttu-id="1696e-125">Требование</span><span class="sxs-lookup"><span data-stu-id="1696e-125">Requirement</span></span> | <span data-ttu-id="1696e-126">Значение</span><span class="sxs-lookup"><span data-stu-id="1696e-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1696e-127">Версия</span><span class="sxs-lookup"><span data-stu-id="1696e-127">Version</span></span><br/> | <span data-ttu-id="1696e-128">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="1696e-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1696e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="1696e-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="1696e-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1696e-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1696e-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1696e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1696e-132">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="1696e-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="1696e-133">**Player. Куррентмедиа**</span><span class="sxs-lookup"><span data-stu-id="1696e-133">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="1696e-134">**Событие Player. Плайстатечанже**</span><span class="sxs-lookup"><span data-stu-id="1696e-134">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="1696e-135">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="1696e-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="1696e-136">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="1696e-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





