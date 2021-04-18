---
title: Медиаколлектион. Жетбяусор, метод
description: Метод Жетбяусор извлекает список воспроизведения элементов мультимедиа по указанному автору.
ms.assetid: 8f9b3ee3-a809-4d24-81ce-adad63e5347c
keywords:
- Жетбяусор метод Windows Media Player
- Жетбяусор метод Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион Windows Media Player, метод Жетбяусор
topic_type:
- apiref
api_name:
- MediaCollection.getByAuthor
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eae0928250e37e76bf3a39f38b43bef8a5691c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704121"
---
# <a name="mediacollectiongetbyauthor-method"></a><span data-ttu-id="033d4-106">Медиаколлектион. Жетбяусор, метод</span><span class="sxs-lookup"><span data-stu-id="033d4-106">MediaCollection.getByAuthor method</span></span>

<span data-ttu-id="033d4-107">Метод **жетбяусор** извлекает список воспроизведения элементов мультимедиа по указанному автору.</span><span class="sxs-lookup"><span data-stu-id="033d4-107">The **getByAuthor** method retrieves a playlist of the media items by the specified author.</span></span>

## <a name="syntax"></a><span data-ttu-id="033d4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="033d4-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAuthor(
  author
)
```



## <a name="parameters"></a><span data-ttu-id="033d4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="033d4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="033d4-110">*Автор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="033d4-110">*author* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="033d4-111">**Строка** , содержащая имя автора.</span><span class="sxs-lookup"><span data-stu-id="033d4-111">**String** containing the name of the author.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="033d4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="033d4-112">Return value</span></span>

<span data-ttu-id="033d4-113">Этот метод возвращает объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="033d4-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="033d4-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="033d4-114">Remarks</span></span>

<span data-ttu-id="033d4-115">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="033d4-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="033d4-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="033d4-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="033d4-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="033d4-117">Examples</span></span>

<span data-ttu-id="033d4-118">В следующем примере JScript используется *медиаколлектион*. **жетбяусор** для получения списка воспроизведения элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="033d4-118">The following JScript example uses *MediaCollection*.**getByAuthor** to retrieve a playlist of media items.</span></span> <span data-ttu-id="033d4-119">Список воспроизведения содержит элементы, соответствующие автору, указанному пользователем в HTML-элементе input TEXT с именем GetText.</span><span class="sxs-lookup"><span data-stu-id="033d4-119">The playlist contains items matching the author specified by the user in an HTML TEXT input element named GetAuthor.</span></span> <span data-ttu-id="033d4-120">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="033d4-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play the media items. -->
<INPUT TYPE = "BUTTON"  NAME = "PlayAuthor"  
       ID = "PlayAuthor"  
       VALUE = "Play Author"

onClick = "
    /* Retrieve the author name text from the user. */
    var author = GetAuthor.value;

    /* Create the playlist by using getByAuthor. */
    var pl = Player.mediaCollection.getByAuthor(Author);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media items in the new playlist. */
               Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="033d4-121">Требования</span><span class="sxs-lookup"><span data-stu-id="033d4-121">Requirements</span></span>



| <span data-ttu-id="033d4-122">Требование</span><span class="sxs-lookup"><span data-stu-id="033d4-122">Requirement</span></span> | <span data-ttu-id="033d4-123">Значение</span><span class="sxs-lookup"><span data-stu-id="033d4-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="033d4-124">Версия</span><span class="sxs-lookup"><span data-stu-id="033d4-124">Version</span></span><br/> | <span data-ttu-id="033d4-125">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="033d4-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="033d4-126">DLL</span><span class="sxs-lookup"><span data-stu-id="033d4-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="033d4-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="033d4-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="033d4-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="033d4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="033d4-129">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="033d4-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="033d4-130">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="033d4-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="033d4-131">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="033d4-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="033d4-132">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="033d4-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





