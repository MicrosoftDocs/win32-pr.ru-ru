---
title: Controls. Плайитем, метод
description: Метод Плайитем воспроизводит указанный элемент мультимедиа. | Controls. Плайитем, метод
ms.assetid: 410e315d-8d5f-4f45-82a7-4249e656c809
keywords:
- Плайитем метод Windows Media Player
- метод Плайитем Windows Media Player, класс Controls
- Класс управляет проигрывателем Windows Media Player, метод Плайитем
topic_type:
- apiref
api_name:
- Controls.playItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9096e378a328f43147a0a94d97034c8e566b611
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699007"
---
# <a name="controlsplayitem-method"></a><span data-ttu-id="32ada-107">Controls. Плайитем, метод</span><span class="sxs-lookup"><span data-stu-id="32ada-107">Controls.playItem method</span></span>

<span data-ttu-id="32ada-108">Метод **плайитем** воспроизводит указанный элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="32ada-108">The **playItem** method plays the specified media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="32ada-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32ada-109">Syntax</span></span>


```JScript
Controls.playItem(
  theMediaItem
)
```



## <a name="parameters"></a><span data-ttu-id="32ada-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="32ada-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32ada-111">*семедиаитем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="32ada-111">*theMediaItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32ada-112">Объект **мультимедиа** для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="32ada-112">**Media** object to be played.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32ada-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32ada-113">Return value</span></span>

<span data-ttu-id="32ada-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="32ada-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="32ada-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32ada-115">Remarks</span></span>

<span data-ttu-id="32ada-116">Элемент мультимедиа будет загружаться и воспроизводиться автоматически независимо от значения *параметров*. свойство " **Автозапуск** ".</span><span class="sxs-lookup"><span data-stu-id="32ada-116">The media item will be loaded and played automatically, regardless of the value of the *Settings*.**autoStart** property.</span></span> <span data-ttu-id="32ada-117">Чтобы загрузить элемент без автоматического воспроизведения, задайте *Параметры*. **Автозапуск** в значение false и назначение значения *проигрывателю*. **URL-адрес**, после которого можно вызвать **Воспроизведение** , чтобы начать воспроизведение элемента.</span><span class="sxs-lookup"><span data-stu-id="32ada-117">To load an item without playing it automatically, set *Settings*.**autoStart** to false and assign a value to *Player*.**URL**, after which **play** can be called to start playing the item.</span></span>

<span data-ttu-id="32ada-118">Примечание</span><span class="sxs-lookup"><span data-stu-id="32ada-118">Note</span></span>

<span data-ttu-id="32ada-119">**плайитем** работает только с элементами в *куррентплайлист*.</span><span class="sxs-lookup"><span data-stu-id="32ada-119">**playItem** works only with items in *currentPlaylist*.</span></span> <span data-ttu-id="32ada-120">Вызов **плайитем** со ссылкой на сохраненный элемент мультимедиа не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="32ada-120">Calling **playItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="32ada-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="32ada-121">Examples</span></span>

<span data-ttu-id="32ada-122">В следующем примере JScript используется **плайитем** для воспроизведения элемента мультимедиа из текущего списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="32ada-122">The following JScript example uses **playItem** to play a media item from the current playlist.</span></span> <span data-ttu-id="32ada-123">Элемент для воспроизведения выбирается в зависимости от его позиции в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="32ada-123">The item to play is chosen based upon its position in the playlist.</span></span> <span data-ttu-id="32ada-124">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="32ada-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
var index = 3

// Retrieve the media item at the fourth position in the current playlist.
var media = Player.currentPlaylist.item(index);

// Play the media item.
Player.controls.playItem(media);

```



## <a name="requirements"></a><span data-ttu-id="32ada-125">Требования</span><span class="sxs-lookup"><span data-stu-id="32ada-125">Requirements</span></span>



| <span data-ttu-id="32ada-126">Требование</span><span class="sxs-lookup"><span data-stu-id="32ada-126">Requirement</span></span> | <span data-ttu-id="32ada-127">Значение</span><span class="sxs-lookup"><span data-stu-id="32ada-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="32ada-128">Версия</span><span class="sxs-lookup"><span data-stu-id="32ada-128">Version</span></span><br/> | <span data-ttu-id="32ada-129">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="32ada-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="32ada-130">DLL</span><span class="sxs-lookup"><span data-stu-id="32ada-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="32ada-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32ada-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32ada-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32ada-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32ada-133">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="32ada-133">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="32ada-134">**Список воспроизведения. элемент**</span><span class="sxs-lookup"><span data-stu-id="32ada-134">**Playlist.item**</span></span>](playlist-item.md)
</dt> </dl>

 

 





