---
title: Плайлистколлектион. Жетбинаме, метод
description: Метод Жетбинаме извлекает объект Плайлистаррай, содержащий списки воспроизведения с указанным именем, если таковые имеются.
ms.assetid: 0308a98d-1149-4367-b602-33fa54c1760f
keywords:
- Жетбинаме метод Windows Media Player
- Жетбинаме метод Windows Media Player, класс Плайлистколлектион
- Класс Плайлистколлектион Windows Media Player, метод Жетбинаме
topic_type:
- apiref
api_name:
- PlaylistCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7954df8e0ccc487df77ea31b3a26dce9eea6d2e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718033"
---
# <a name="playlistcollectiongetbyname-method"></a><span data-ttu-id="539de-106">Плайлистколлектион. Жетбинаме, метод</span><span class="sxs-lookup"><span data-stu-id="539de-106">PlaylistCollection.getByName method</span></span>

<span data-ttu-id="539de-107">Метод **жетбинаме** извлекает объект **плайлистаррай** , содержащий списки воспроизведения с указанным именем, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="539de-107">The **getByName** method retrieves a **PlaylistArray** object containing playlists with the specified name, if any exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="539de-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="539de-108">Syntax</span></span>


```JScript
retVal = PlaylistCollection.getByName(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="539de-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="539de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="539de-110">*имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="539de-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="539de-111">**Строка** , содержащая имена списков воспроизведения для извлечения.</span><span class="sxs-lookup"><span data-stu-id="539de-111">**String** containing the name of the playlists to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="539de-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="539de-112">Return value</span></span>

<span data-ttu-id="539de-113">Этот метод возвращает объект **плайлистаррай** .</span><span class="sxs-lookup"><span data-stu-id="539de-113">This method returns a **PlaylistArray** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="539de-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="539de-114">Remarks</span></span>

<span data-ttu-id="539de-115">Используйте *плайлистаррай*. **количество** , определяющее, существует ли список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="539de-115">Use *PlaylistArray*.**count** to determine whether a playlist exists.</span></span> <span data-ttu-id="539de-116">Если значение **Count** равно нулю, список воспроизведения не существует.</span><span class="sxs-lookup"><span data-stu-id="539de-116">If **count** is zero, a playlist does not exist.</span></span>

<span data-ttu-id="539de-117">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="539de-117">To use this method, read access to the library is required.</span></span> <span data-ttu-id="539de-118">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="539de-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="539de-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="539de-119">Examples</span></span>

<span data-ttu-id="539de-120">В следующем примере JScript используется *плайлистколлектион*. **жетбинаме** , чтобы проверить объект **плайлистколлектион** для списка воспроизведения с именем "срилист".</span><span class="sxs-lookup"><span data-stu-id="539de-120">The following JScript example uses *playlistCollection*.**getByName** to check the **playlistCollection** object for a playlist named "ThreeList".</span></span> <span data-ttu-id="539de-121">Если существует список воспроизведения "Срилист", **жетбинаме** устанавливает в качестве текущего списка воспроизведения "срилист".</span><span class="sxs-lookup"><span data-stu-id="539de-121">If the "Threelist" playlist exists, **getByName** sets "ThreeList" as the current playlist.</span></span> <span data-ttu-id="539de-122">Объект **Player** был создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="539de-122">The **Player** object was created with the ID = "Player".</span></span>


```JScript
//Retrieve the count of the playlists named "ThreeList".
var Checkit = Player.playlistCollection.getByName("ThreeList").count;

//Since duplicate playlist names are allowed, the count returned
//will be either zero (no playlist) or greater than zero 
//(playlist exists).
if (Checkit > 0){ 
    
   //Retrieve a playlistArray object containing "ThreeList". Assume that
   //there is only one playlist with that name, and assign it to the 
   //current playlist.
   Player.currentPlaylist = Player.playlistCollection.getByName("ThreeList").item(0);
}

```



## <a name="requirements"></a><span data-ttu-id="539de-123">Требования</span><span class="sxs-lookup"><span data-stu-id="539de-123">Requirements</span></span>



| <span data-ttu-id="539de-124">Требование</span><span class="sxs-lookup"><span data-stu-id="539de-124">Requirement</span></span> | <span data-ttu-id="539de-125">Значение</span><span class="sxs-lookup"><span data-stu-id="539de-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="539de-126">Версия</span><span class="sxs-lookup"><span data-stu-id="539de-126">Version</span></span><br/> | <span data-ttu-id="539de-127">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="539de-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="539de-128">DLL</span><span class="sxs-lookup"><span data-stu-id="539de-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="539de-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="539de-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="539de-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="539de-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="539de-131">**Объект Плайлистаррай**</span><span class="sxs-lookup"><span data-stu-id="539de-131">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="539de-132">**Плайлистаррай. Count**</span><span class="sxs-lookup"><span data-stu-id="539de-132">**PlaylistArray.count**</span></span>](playlistarray-count.md)
</dt> <dt>

[<span data-ttu-id="539de-133">**Объект Плайлистколлектион**</span><span class="sxs-lookup"><span data-stu-id="539de-133">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="539de-134">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="539de-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="539de-135">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="539de-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





