---
title: Медиаколлектион. Жетбинаме, метод
description: Метод Жетбинаме извлекает список воспроизведения элементов мультимедиа с указанным именем.
ms.assetid: f9395a4f-06d6-438b-b7c5-7a063abdf59f
keywords:
- Жетбинаме метод Windows Media Player
- Жетбинаме метод Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион Windows Media Player, метод Жетбинаме
topic_type:
- apiref
api_name:
- MediaCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01a3fc6e34b508fa094f79d2fbbd1d44ab712789
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685414"
---
# <a name="mediacollectiongetbyname-method"></a><span data-ttu-id="5fb06-106">Медиаколлектион. Жетбинаме, метод</span><span class="sxs-lookup"><span data-stu-id="5fb06-106">MediaCollection.getByName method</span></span>

<span data-ttu-id="5fb06-107">Метод **жетбинаме** извлекает список воспроизведения элементов мультимедиа с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="5fb06-107">The **getByName** method retrieves a playlist of the media items with the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fb06-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fb06-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByName(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="5fb06-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5fb06-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fb06-110">*имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5fb06-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fb06-111">**Строка** , содержащая имя.</span><span class="sxs-lookup"><span data-stu-id="5fb06-111">**String** containing the name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fb06-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5fb06-112">Return value</span></span>

<span data-ttu-id="5fb06-113">Этот метод возвращает объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="5fb06-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fb06-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5fb06-114">Remarks</span></span>

<span data-ttu-id="5fb06-115">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="5fb06-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="5fb06-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5fb06-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5fb06-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="5fb06-117">Examples</span></span>

<span data-ttu-id="5fb06-118">В следующем примере JScript используется *медиаколлектион*. **жетбинаме** для получения трех элементов из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="5fb06-118">The following JScript example uses *MediaCollection*.**getByName** to retrieve three items from the library.</span></span> <span data-ttu-id="5fb06-119">Затем каждый элемент добавляется к текущему списку воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="5fb06-119">Each item is then appended to the current playlist.</span></span> <span data-ttu-id="5fb06-120">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="5fb06-120">The **Player** object was created with ID="Player".</span></span>


```JScript
// In each case, use the name exactly as it appears in the library.
// Windows Media Player does not include file name extensions or file paths
// in the name. Internet URLs include the entire path, but not the 
// file name extension.

// Get a playlist object that contains an Internet URL.
var One = Player.mediaCollection.getByName("https://www.proseware.com/Media/Laure");
 
// Get a playlist object that contains a file on a network server.
var Two = Player.mediaCollection.getByName("Jeanne");

// Get a playlist object that contains a file on a local drive.
var Three = Player.mediaCollection.getByName("house");

// Append each item to the current playlist. Since each playlist retrieved
// using getByName contains one digital media item, use Playlist.item with
// an index of zero to reference that item.
Player.currentPlaylist.appendItem(One.item(0));
Player.currentPlaylist.appendItem(Two.item(0));
Player.currentPlaylist.appendItem(Three.item(0));

```



## <a name="requirements"></a><span data-ttu-id="5fb06-121">Требования</span><span class="sxs-lookup"><span data-stu-id="5fb06-121">Requirements</span></span>



| <span data-ttu-id="5fb06-122">Требование</span><span class="sxs-lookup"><span data-stu-id="5fb06-122">Requirement</span></span> | <span data-ttu-id="5fb06-123">Значение</span><span class="sxs-lookup"><span data-stu-id="5fb06-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5fb06-124">Версия</span><span class="sxs-lookup"><span data-stu-id="5fb06-124">Version</span></span><br/> | <span data-ttu-id="5fb06-125">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="5fb06-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5fb06-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5fb06-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="5fb06-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fb06-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fb06-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5fb06-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fb06-129">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="5fb06-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="5fb06-130">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="5fb06-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="5fb06-131">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="5fb06-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="5fb06-132">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="5fb06-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





