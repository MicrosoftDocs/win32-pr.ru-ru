---
title: Медиаколлектион. Add, метод
description: Метод Add добавляет новый элемент мультимедиа или список воспроизведения в библиотеку. | Медиаколлектион. Add, метод
ms.assetid: 8adf93d1-368b-4916-937f-342901a1592b
keywords:
- Добавление метода Windows Media Player
- Добавление метода Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион проигрыватель Windows Media Player, метод Add
topic_type:
- apiref
api_name:
- MediaCollection.add
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7731a42c8e1317355b129acb6921676c0a33f4a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689064"
---
# <a name="mediacollectionadd-method"></a><span data-ttu-id="3fbfe-107">Медиаколлектион. Add, метод</span><span class="sxs-lookup"><span data-stu-id="3fbfe-107">MediaCollection.add method</span></span>

<span data-ttu-id="3fbfe-108">Метод **Add** добавляет новый элемент мультимедиа или список воспроизведения в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="3fbfe-108">The **add** method adds a new media item or playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fbfe-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3fbfe-109">Syntax</span></span>


```JScript
retVal = MediaCollection.add(
  path
)
```



## <a name="parameters"></a><span data-ttu-id="3fbfe-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="3fbfe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fbfe-111">*путь* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3fbfe-111">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fbfe-112">**Строка** , содержащая путь.</span><span class="sxs-lookup"><span data-stu-id="3fbfe-112">**String** containing the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fbfe-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3fbfe-113">Return value</span></span>

<span data-ttu-id="3fbfe-114">Этот метод возвращает объект **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="3fbfe-114">This method returns a **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fbfe-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3fbfe-115">Remarks</span></span>

<span data-ttu-id="3fbfe-116">Этот метод загружает существующий элемент мультимедиа или список воспроизведения в библиотеку по заданному пути к файлу.</span><span class="sxs-lookup"><span data-stu-id="3fbfe-116">This method loads an existing media item or playlist into the library, given a path to a file.</span></span> <span data-ttu-id="3fbfe-117">Этот метод не перемещает и не изменяет файл.</span><span class="sxs-lookup"><span data-stu-id="3fbfe-117">This method does not move or change the file.</span></span> <span data-ttu-id="3fbfe-118">Этот метод завершается ошибкой, если задан недопустимый локальный путь, но перед добавлением в библиотеку цифровые файлы мультимедиа не проверяются на допустимость.</span><span class="sxs-lookup"><span data-stu-id="3fbfe-118">This method fails if given an invalid local path, but digital media files are not checked for validity before they are added to the library.</span></span>

<span data-ttu-id="3fbfe-119">Этот метод принимает как статические, так и автоматические файлы списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="3fbfe-119">This method accepts both static and auto playlist files.</span></span> <span data-ttu-id="3fbfe-120">*Плайлистколлектион*. метод **импортплайлист** также можно использовать для добавления статического списка воспроизведения в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="3fbfe-120">The *PlaylistCollection*.**importPlaylist** method can also be used to add a static playlist to the library.</span></span>

<span data-ttu-id="3fbfe-121">Чтобы использовать этот метод, требуется полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="3fbfe-121">To use this method, full access to the library is required.</span></span> <span data-ttu-id="3fbfe-122">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3fbfe-122">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3fbfe-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="3fbfe-123">Examples</span></span>

<span data-ttu-id="3fbfe-124">Следующий пример Microsoft JScript добавляет три объекта мультимедиа в коллекцию носителей проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3fbfe-124">The following Microsoft JScript example adds three media objects to the Windows Media Player media collection.</span></span> <span data-ttu-id="3fbfe-125">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="3fbfe-125">The **Player** object was created with ID="Player".</span></span>


```JScript
// Adding a media object using a website.
Player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// You must add an escape sequence of a backslash for 
// every original backslash.
Player.mediaCollection.add("\\\\yourservername\\Public\\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Be sure to add appropriate escape sequences.
Player.mediaCollection.add("C:\\WMSDK\\WMPSDK\\docs\\samples\\media\\house.wma");
```



## <a name="requirements"></a><span data-ttu-id="3fbfe-126">Требования</span><span class="sxs-lookup"><span data-stu-id="3fbfe-126">Requirements</span></span>



| <span data-ttu-id="3fbfe-127">Требование</span><span class="sxs-lookup"><span data-stu-id="3fbfe-127">Requirement</span></span> | <span data-ttu-id="3fbfe-128">Значение</span><span class="sxs-lookup"><span data-stu-id="3fbfe-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3fbfe-129">Версия</span><span class="sxs-lookup"><span data-stu-id="3fbfe-129">Version</span></span><br/> | <span data-ttu-id="3fbfe-130">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="3fbfe-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3fbfe-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3fbfe-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="3fbfe-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fbfe-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fbfe-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3fbfe-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fbfe-134">**Управление списками воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="3fbfe-134">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="3fbfe-135">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="3fbfe-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="3fbfe-136">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="3fbfe-136">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="3fbfe-137">**Медиаколлектион. Remove**</span><span class="sxs-lookup"><span data-stu-id="3fbfe-137">**MediaCollection.remove**</span></span>](mediacollection-remove.md)
</dt> <dt>

[<span data-ttu-id="3fbfe-138">**Плайлистколлектион. Импортплайлист**</span><span class="sxs-lookup"><span data-stu-id="3fbfe-138">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

[<span data-ttu-id="3fbfe-139">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="3fbfe-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="3fbfe-140">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="3fbfe-140">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





