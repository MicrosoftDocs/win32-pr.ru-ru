---
title: Метод списка воспроизведения. Аппендитем
description: Метод Аппендитем добавляет элемент мультимедиа в конец списка воспроизведения.
ms.assetid: cc956491-7936-49e7-90ca-1f71e03448cd
keywords:
- Аппендитем метод Windows Media Player
- Аппендитем метод Windows Media Player, класс списка воспроизведения
- Класс списка воспроизведения проигрыватель Windows Media Player, метод Аппендитем
topic_type:
- apiref
api_name:
- Playlist.appendItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 828799d5b6e71e7ff0e7be4c1e55714f6343be51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704362"
---
# <a name="playlistappenditem-method"></a><span data-ttu-id="9db91-106">Метод списка воспроизведения. Аппендитем</span><span class="sxs-lookup"><span data-stu-id="9db91-106">Playlist.appendItem method</span></span>

<span data-ttu-id="9db91-107">Метод **аппендитем** добавляет элемент мультимедиа в конец списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="9db91-107">The **appendItem** method adds a media item to the end of the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="9db91-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9db91-108">Syntax</span></span>


```JScript
Playlist.appendItem(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="9db91-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9db91-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9db91-110">*элемент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9db91-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9db91-111">Добавляемый объект **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="9db91-111">**Media** object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9db91-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9db91-112">Return value</span></span>

<span data-ttu-id="9db91-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9db91-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9db91-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9db91-114">Remarks</span></span>

<span data-ttu-id="9db91-115">Чтобы использовать этот метод, требуется полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="9db91-115">To use this method, full access to the library is required.</span></span> <span data-ttu-id="9db91-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="9db91-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9db91-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="9db91-117">Examples</span></span>

<span data-ttu-id="9db91-118">В следующем примере JScript используется *список воспроизведения*. **аппендитем** добавить текущий элемент мультимедиа в список воспроизведения с именем "срилист".</span><span class="sxs-lookup"><span data-stu-id="9db91-118">The following JScript example uses *Playlist*.**appendItem** to add the current media item to the playlist named "ThreeList".</span></span> <span data-ttu-id="9db91-119">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="9db91-119">The **Player** object was created with ID="Player".</span></span>


```JScript
// Get the current media item.
var currMedia = Player.currentMedia;

// Get the playlist object by name.
var plThreeList = Player.playlistCollection.getByName("ThreeList").item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);

```



## <a name="requirements"></a><span data-ttu-id="9db91-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9db91-120">Requirements</span></span>



| <span data-ttu-id="9db91-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9db91-121">Requirement</span></span> | <span data-ttu-id="9db91-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9db91-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9db91-123">Версия</span><span class="sxs-lookup"><span data-stu-id="9db91-123">Version</span></span><br/> | <span data-ttu-id="9db91-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="9db91-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9db91-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9db91-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="9db91-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9db91-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9db91-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9db91-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9db91-128">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="9db91-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="9db91-129">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="9db91-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="9db91-130">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="9db91-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





