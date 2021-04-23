---
title: Метод Player. Невплайлист
description: Метод Невплайлист создает новый объект списка воспроизведения.
ms.assetid: a566006e-8647-4c51-ab77-762728f25a30
keywords:
- Невплайлист метод Windows Media Player
- метод Невплайлист проигрывателя Windows Media Player, класс Player
- Класс проигрывателя Windows Media Player, метод Невплайлист
topic_type:
- apiref
api_name:
- Player.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa65ae4b453fe919116a33c5ee86b14ba353f681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704157"
---
# <a name="playernewplaylist-method"></a><span data-ttu-id="c401c-106">Метод Player. Невплайлист</span><span class="sxs-lookup"><span data-stu-id="c401c-106">Player.newPlaylist method</span></span>

<span data-ttu-id="c401c-107">Метод **невплайлист** создает новый объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="c401c-107">The **newPlaylist** method creates a new **Playlist** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c401c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c401c-108">Syntax</span></span>


```JScript
retVal = Player.newPlaylist(
  name,
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="c401c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c401c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c401c-110">*имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c401c-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c401c-111">**Строка** , содержащая имя нового списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="c401c-111">**String** containing the name of the new playlist.</span></span>

</dd> <dt>

<span data-ttu-id="c401c-112">*URL-адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c401c-112">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c401c-113">**Строка** , содержащая URL-адрес списка воспроизведения метафайла Windows Media для создания объекта **списка воспроизведения** с помощью.</span><span class="sxs-lookup"><span data-stu-id="c401c-113">**String** containing the URL of the Windows Media metafile playlist to create the **Playlist** object with.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c401c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c401c-114">Return value</span></span>

<span data-ttu-id="c401c-115">Этот метод возвращает объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="c401c-115">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c401c-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c401c-116">Remarks</span></span>

<span data-ttu-id="c401c-117">Если параметр *URL-адреса* имеет значение null или "" (пустая строка), будет создан пустой объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="c401c-117">If the *URL* parameter is set to null or "" (empty string), an empty **Playlist** object will be created.</span></span> <span data-ttu-id="c401c-118">Если для параметра *Name* задано значение "", используется имя в метафайле.</span><span class="sxs-lookup"><span data-stu-id="c401c-118">If the *name* parameter is set to "", the name in the metafile is used.</span></span>

<span data-ttu-id="c401c-119">Новый список воспроизведения, созданный с помощью этого метода, не добавляется в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="c401c-119">The new playlist created with this method is not added to the library.</span></span> <span data-ttu-id="c401c-120">Чтобы добавить новый список воспроизведения в библиотеку, используйте *плайлистколлектион*. **импортплайлист** или *плайлистколлектион*. **невплайлист**.</span><span class="sxs-lookup"><span data-stu-id="c401c-120">To add a new playlist to the library, use *PlaylistCollection*.**importPlaylist** or *PlaylistCollection*.**newPlaylist**.</span></span> <span data-ttu-id="c401c-121">Все начальные и конечные пробелы в имени списка воспроизведения автоматически удаляются при добавлении в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="c401c-121">Any leading or trailing spaces in the playlist name are automatically removed when it is added to the library.</span></span>

<span data-ttu-id="c401c-122">Так как библиотека допускает наличие нескольких списков воспроизведения с одинаковыми именами, перед добавлением нового списка воспроизведения может потребоваться проверить, есть ли у него указанное имя.</span><span class="sxs-lookup"><span data-stu-id="c401c-122">Because the library allows multiple playlists with the same name, you may want to check for the presence of a playlist with a given name before adding a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="c401c-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c401c-123">Requirements</span></span>



| <span data-ttu-id="c401c-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c401c-124">Requirement</span></span> | <span data-ttu-id="c401c-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c401c-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c401c-126">Версия</span><span class="sxs-lookup"><span data-stu-id="c401c-126">Version</span></span><br/> | <span data-ttu-id="c401c-127">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="c401c-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="c401c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c401c-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="c401c-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c401c-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c401c-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c401c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c401c-131">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="c401c-131">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="c401c-132">**Плайлистколлектион. Импортплайлист**</span><span class="sxs-lookup"><span data-stu-id="c401c-132">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

[<span data-ttu-id="c401c-133">**Плайлистколлектион. Невплайлист**</span><span class="sxs-lookup"><span data-stu-id="c401c-133">**PlaylistCollection.newPlaylist**</span></span>](playlistcollection-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="c401c-134">**Метафайлы Windows Media**</span><span class="sxs-lookup"><span data-stu-id="c401c-134">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 





