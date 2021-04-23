---
title: Player. Куррентплайлист
description: Свойство Куррентплайлист указывает или получает текущий объект списка воспроизведения.
ms.assetid: fabfb927-5f64-4fc4-8ee5-e2449082dfbc
keywords:
- Проигрыватель проигрывателя Windows Media Player. Куррентплайлист
topic_type:
- apiref
api_name:
- Player.currentPlaylist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceae33a201086d268942e47496874678ec13f459
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698880"
---
# <a name="playercurrentplaylist"></a><span data-ttu-id="c8524-104">Player. Куррентплайлист</span><span class="sxs-lookup"><span data-stu-id="c8524-104">Player.currentPlaylist</span></span>

<span data-ttu-id="c8524-105">Свойство Куррентплайлист указывает или получает текущий объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="c8524-105">The currentPlaylist property specifies or retrieves the current **Playlist** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8524-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8524-106">Syntax</span></span>

<span data-ttu-id="c8524-107">*проигрыватель* . **куррентплайлист**</span><span class="sxs-lookup"><span data-stu-id="c8524-107">*player* .**currentPlaylist**</span></span>

## <a name="possible-values"></a><span data-ttu-id="c8524-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="c8524-108">Possible Values</span></span>

<span data-ttu-id="c8524-109">Это свойство является объектом **списка воспроизведения** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c8524-109">This property is a read/write **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8524-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c8524-110">Remarks</span></span>

<span data-ttu-id="c8524-111">Если *Параметры*. Свойство **автозапуска** имеет значение true, воспроизведение начинается автоматически при установке **куррентплайлист**.</span><span class="sxs-lookup"><span data-stu-id="c8524-111">If the *Settings*.**autoStart** property is true, playback begins automatically whenever you set **currentPlaylist**.</span></span>

<span data-ttu-id="c8524-112">Это свойство принимает объект списка воспроизведения, который может быть получен несколькими способами, например путем вызова *плайлистаррай*. **Item** или *плайлистколлектион*. **невплайлист**.</span><span class="sxs-lookup"><span data-stu-id="c8524-112">This property takes a Playlist object, which can be acquired in several ways, such as by calling *PlaylistArray*.**item** or *PlaylistCollection*.**newPlaylist**.</span></span> <span data-ttu-id="c8524-113">Чтобы загрузить элемент **списка воспроизведения** с помощью имени файла, задайте свойство URL-адреса или используйте *проигрыватель*. **невплайлист**.</span><span class="sxs-lookup"><span data-stu-id="c8524-113">To load a **Playlist** item using a file name, set the URL property or use *Player*.**newPlaylist**.</span></span>

## <a name="examples"></a><span data-ttu-id="c8524-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="c8524-114">Examples</span></span>

<span data-ttu-id="c8524-115">В следующем примере JScript извлекается первый список воспроизведения в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="c8524-115">The following JScript example retrieves the first playlist in the library.</span></span> <span data-ttu-id="c8524-116">Затем он использует **куррентплайлист** , чтобы сделать полученный список воспроизведения текущим списком воспроизведения, а затем отобразить имя текущего списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="c8524-116">It then uses **currentPlaylist** to make the retrieved playlist the current playlist, and then to display the name of the current playlist.</span></span> <span data-ttu-id="c8524-117">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="c8524-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first playlist from the library.
var firstPL = Player.playlistCollection.getAll().item(0);

// Make the retrieved playlist the current playlist.
Player.currentPlaylist = firstPL;

// Display the name of the current playlist.
document.write("Found first playlist. Name: " + Player.currentPlaylist.name);
```



## <a name="requirements"></a><span data-ttu-id="c8524-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c8524-118">Requirements</span></span>



| <span data-ttu-id="c8524-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c8524-119">Requirement</span></span> | <span data-ttu-id="c8524-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c8524-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c8524-121">Версия</span><span class="sxs-lookup"><span data-stu-id="c8524-121">Version</span></span><br/> | <span data-ttu-id="c8524-122">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="c8524-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c8524-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c8524-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="c8524-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8524-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8524-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8524-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8524-126">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="c8524-126">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="c8524-127">**Player. Невплайлист**</span><span class="sxs-lookup"><span data-stu-id="c8524-127">**Player.newPlaylist**</span></span>](player-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="c8524-128">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="c8524-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="c8524-129">**Плайлистаррай. Item**</span><span class="sxs-lookup"><span data-stu-id="c8524-129">**PlaylistArray.item**</span></span>](playlistarray-item.md)
</dt> <dt>

[<span data-ttu-id="c8524-130">**Плайлистколлектион. Невплайлист**</span><span class="sxs-lookup"><span data-stu-id="c8524-130">**PlaylistCollection.newPlaylist**</span></span>](playlistcollection-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="c8524-131">**Параметры. Автозапуск**</span><span class="sxs-lookup"><span data-stu-id="c8524-131">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 





