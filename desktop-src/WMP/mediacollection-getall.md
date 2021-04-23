---
title: Медиаколлектион. Жеталл, метод
description: Метод Жеталл извлекает список воспроизведения, содержащий все элементы мультимедиа в библиотеке.
ms.assetid: c22532ee-5714-4762-966f-7dc6543384f4
keywords:
- Жеталл метод Windows Media Player
- Жеталл метод Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион Windows Media Player, метод Жеталл
topic_type:
- apiref
api_name:
- MediaCollection.getAll
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1681cd533be4084123cb80cdcc199ab5e1ce2981
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689062"
---
# <a name="mediacollectiongetall-method"></a><span data-ttu-id="7db20-106">Медиаколлектион. Жеталл, метод</span><span class="sxs-lookup"><span data-stu-id="7db20-106">MediaCollection.getAll method</span></span>

<span data-ttu-id="7db20-107">Метод **жеталл** извлекает список воспроизведения, содержащий все элементы мультимедиа в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="7db20-107">The **getAll** method retrieves a playlist containing all media items in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="7db20-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7db20-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getAll()
```



## <a name="parameters"></a><span data-ttu-id="7db20-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7db20-109">Parameters</span></span>

<span data-ttu-id="7db20-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7db20-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7db20-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7db20-111">Return value</span></span>

<span data-ttu-id="7db20-112">Этот метод возвращает объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="7db20-112">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7db20-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7db20-113">Remarks</span></span>

<span data-ttu-id="7db20-114">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="7db20-114">To use this method, read access to the library is required.</span></span> <span data-ttu-id="7db20-115">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7db20-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7db20-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="7db20-116">Examples</span></span>

<span data-ttu-id="7db20-117">В следующем примере JScript используется *медиаколлектион*. **жеталл** для воспроизведения элементов мультимедиа случайным образом из коллекции носителей.</span><span class="sxs-lookup"><span data-stu-id="7db20-117">The following JScript example uses *MediaCollection*.**getAll** to play media items randomly from the media collection.</span></span> <span data-ttu-id="7db20-118">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="7db20-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the count of all media items in the media collection.
var count = Player.mediaCollection.getAll().count;

// Generate a random number using the media count.
var rand = Math.random() * count;

// Round down the random number to the nearest integer.
rand = Math.floor(rand);

// Make the random media item the current media item.
Player.currentMedia = Player.mediaCollection.getAll().item(rand);

// Play the media item.
// Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="7db20-119">Требования</span><span class="sxs-lookup"><span data-stu-id="7db20-119">Requirements</span></span>



| <span data-ttu-id="7db20-120">Требование</span><span class="sxs-lookup"><span data-stu-id="7db20-120">Requirement</span></span> | <span data-ttu-id="7db20-121">Значение</span><span class="sxs-lookup"><span data-stu-id="7db20-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7db20-122">Версия</span><span class="sxs-lookup"><span data-stu-id="7db20-122">Version</span></span><br/> | <span data-ttu-id="7db20-123">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="7db20-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7db20-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7db20-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="7db20-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7db20-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7db20-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7db20-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7db20-127">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="7db20-127">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="7db20-128">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="7db20-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="7db20-129">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="7db20-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="7db20-130">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="7db20-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





