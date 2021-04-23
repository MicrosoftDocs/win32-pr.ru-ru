---
title: Player. Куррентмедиа
description: Свойство Куррентмедиа указывает или получает текущий объект мультимедиа.
ms.assetid: 5cf45a10-9d0d-435e-97f1-d2c9c51f4b47
keywords:
- Проигрыватель проигрывателя Windows Media Player. Куррентмедиа
topic_type:
- apiref
api_name:
- Player.currentMedia
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea90b7be72bcb10a8ec0d3c49116f3effceb9a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695033"
---
# <a name="playercurrentmedia"></a><span data-ttu-id="836da-104">Player. Куррентмедиа</span><span class="sxs-lookup"><span data-stu-id="836da-104">Player.currentMedia</span></span>

<span data-ttu-id="836da-105">Свойство **куррентмедиа** указывает или получает текущий объект мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="836da-105">The **currentMedia** property specifies or retrieves the current Media object.</span></span>

## <a name="syntax"></a><span data-ttu-id="836da-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="836da-106">Syntax</span></span>

<span data-ttu-id="836da-107">*проигрыватель* . **куррентмедиа**</span><span class="sxs-lookup"><span data-stu-id="836da-107">*player* .**currentMedia**</span></span>

## <a name="possible-values"></a><span data-ttu-id="836da-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="836da-108">Possible Values</span></span>

<span data-ttu-id="836da-109">Это свойство является объектом мультимедиа для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="836da-109">This property is a read/write Media object.</span></span>

## <a name="remarks"></a><span data-ttu-id="836da-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="836da-110">Remarks</span></span>

<span data-ttu-id="836da-111">Если *Параметры*. Свойство **автозапуска** имеет значение true, воспроизведение начинается автоматически при установке **куррентмедиа**.</span><span class="sxs-lookup"><span data-stu-id="836da-111">If the *Settings*.**autoStart** property is true, playback begins automatically whenever you set **currentMedia**.</span></span>

<span data-ttu-id="836da-112">Это свойство принимает объект мультимедиа, который можно получить с помощью *списка воспроизведения*. **элемент**.</span><span class="sxs-lookup"><span data-stu-id="836da-112">This property takes a Media object, which can be acquired by using *Playlist*.**item**.</span></span> <span data-ttu-id="836da-113">Чтобы загрузить элемент **мультимедиа** с помощью имени файла, задайте свойство URL-адреса или используйте **невмедиа**.</span><span class="sxs-lookup"><span data-stu-id="836da-113">To load a **Media** item using a file name, set the URL property or use **newMedia**.</span></span>

## <a name="examples"></a><span data-ttu-id="836da-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="836da-114">Examples</span></span>

<span data-ttu-id="836da-115">В следующем примере JScript извлекается первый элемент мультимедиа из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="836da-115">The following JScript example retrieves the first media item in the library.</span></span> <span data-ttu-id="836da-116">Затем он использует **куррентмедиа** , чтобы сделать полученный элемент мультимедиа текущим элементом мультимедиа, а затем отобразить имя текущего элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="836da-116">It then uses **currentMedia** to make the retrieved media item the current media item, and then to display the name of the current media item.</span></span> <span data-ttu-id="836da-117">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="836da-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first media item from the library.
var firstMedia = Player.mediaCollection.getAll().item(0);

// Make the retrieved media item the current media item.
Player.currentMedia = firstMedia;

// Display the name of the current media item.
document.write("Found first media item. Name = " + Player.currentMedia.name);
```



## <a name="requirements"></a><span data-ttu-id="836da-118">Требования</span><span class="sxs-lookup"><span data-stu-id="836da-118">Requirements</span></span>



| <span data-ttu-id="836da-119">Требование</span><span class="sxs-lookup"><span data-stu-id="836da-119">Requirement</span></span> | <span data-ttu-id="836da-120">Значение</span><span class="sxs-lookup"><span data-stu-id="836da-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="836da-121">Версия</span><span class="sxs-lookup"><span data-stu-id="836da-121">Version</span></span><br/> | <span data-ttu-id="836da-122">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="836da-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="836da-123">DLL</span><span class="sxs-lookup"><span data-stu-id="836da-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="836da-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="836da-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="836da-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="836da-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="836da-126">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="836da-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="836da-127">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="836da-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="836da-128">**Player. Невмедиа**</span><span class="sxs-lookup"><span data-stu-id="836da-128">**Player.newMedia**</span></span>](player-newmedia.md)
</dt> <dt>

[<span data-ttu-id="836da-129">**Список воспроизведения. элемент**</span><span class="sxs-lookup"><span data-stu-id="836da-129">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="836da-130">**Параметры. Автозапуск**</span><span class="sxs-lookup"><span data-stu-id="836da-130">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 





