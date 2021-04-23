---
title: Список воспроизведения. dropDownList
description: Атрибут dropDownList указывает или получает значение, указывающее, какие элементы отображаются в раскрывающемся списке для данного экземпляра элемента списка воспроизведения.
ms.assetid: 583041b0-25dc-4015-a3b2-37f3cfdcd496
keywords:
- Список воспроизведения. Windows Media Player. dropDownList
topic_type:
- apiref
api_name:
- PLAYLIST.dropDownList
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acf98dec7d50e2a3cd0b53acc07b0b8695f8461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704208"
---
# <a name="playlistdropdownlist"></a><span data-ttu-id="9b103-104">Список воспроизведения. dropDownList</span><span class="sxs-lookup"><span data-stu-id="9b103-104">PLAYLIST.dropDownList</span></span>

<span data-ttu-id="9b103-105">Атрибут **dropDownList** указывает или получает значение, указывающее, какие элементы отображаются в раскрывающемся списке для данного экземпляра элемента **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="9b103-105">The **dropDownList** attribute specifies or retrieves a value indicating which elements show up in the drop-down list box for a given instance of the **PLAYLIST** element.</span></span>

``` syntax
        elementID.dropDownList
```

## <a name="possible-values"></a><span data-ttu-id="9b103-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="9b103-106">Possible Values</span></span>

<span data-ttu-id="9b103-107">Этот атрибут является **строкой** для чтения и записи, содержащей одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9b103-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="9b103-108">Значение</span><span class="sxs-lookup"><span data-stu-id="9b103-108">Value</span></span>       | <span data-ttu-id="9b103-109">Описание</span><span class="sxs-lookup"><span data-stu-id="9b103-109">Description</span></span>                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b103-110">шовалбумс</span><span class="sxs-lookup"><span data-stu-id="9b103-110">showAlbums</span></span>  | <span data-ttu-id="9b103-111">Показывает альбомы.</span><span class="sxs-lookup"><span data-stu-id="9b103-111">Shows albums.</span></span>                                                                                    |
| <span data-ttu-id="9b103-112">showAll</span><span class="sxs-lookup"><span data-stu-id="9b103-112">showAll</span></span>     | <span data-ttu-id="9b103-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9b103-113">Default.</span></span> <span data-ttu-id="9b103-114">Отображает все доступные элементы, включая списки воспроизведения компакт-дисков, списки воспроизведения пользователей и предустановки радио.</span><span class="sxs-lookup"><span data-stu-id="9b103-114">Shows all available elements including CD playlists, user playlists, and radio presets.</span></span> |
| <span data-ttu-id="9b103-115">шовкд</span><span class="sxs-lookup"><span data-stu-id="9b103-115">showCD</span></span>      | <span data-ttu-id="9b103-116">Отображает список воспроизведения компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="9b103-116">Shows the CD playlist.</span></span>                                                                           |
| <span data-ttu-id="9b103-117">шовклипс</span><span class="sxs-lookup"><span data-stu-id="9b103-117">showClips</span></span>   | <span data-ttu-id="9b103-118">Показывает все клипы.</span><span class="sxs-lookup"><span data-stu-id="9b103-118">Shows all clips.</span></span>                                                                                 |
| <span data-ttu-id="9b103-119">шовкуррент</span><span class="sxs-lookup"><span data-stu-id="9b103-119">showCurrent</span></span> | <span data-ttu-id="9b103-120">Отображает текущий несохраненный список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="9b103-120">Shows the current, unsaved playlist.</span></span>                                                             |
| <span data-ttu-id="9b103-121">шовлибрари</span><span class="sxs-lookup"><span data-stu-id="9b103-121">showLibrary</span></span> | <span data-ttu-id="9b103-122">Отображает только списки воспроизведения библиотек.</span><span class="sxs-lookup"><span data-stu-id="9b103-122">Shows only library playlists.</span></span>                                                                    |
| <span data-ttu-id="9b103-123">шоврадио</span><span class="sxs-lookup"><span data-stu-id="9b103-123">showRadio</span></span>   | <span data-ttu-id="9b103-124">Отображает предустановки радио.</span><span class="sxs-lookup"><span data-stu-id="9b103-124">Shows radio presets.</span></span>                                                                             |
| <span data-ttu-id="9b103-125">шовкуериес</span><span class="sxs-lookup"><span data-stu-id="9b103-125">showQueries</span></span> | <span data-ttu-id="9b103-126">Показывает запросы.</span><span class="sxs-lookup"><span data-stu-id="9b103-126">Shows queries.</span></span>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="9b103-127">Требования</span><span class="sxs-lookup"><span data-stu-id="9b103-127">Requirements</span></span>



| <span data-ttu-id="9b103-128">Требование</span><span class="sxs-lookup"><span data-stu-id="9b103-128">Requirement</span></span> | <span data-ttu-id="9b103-129">Значение</span><span class="sxs-lookup"><span data-stu-id="9b103-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="9b103-130">Версия</span><span class="sxs-lookup"><span data-stu-id="9b103-130">Version</span></span><br/> | <span data-ttu-id="9b103-131">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="9b103-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9b103-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b103-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b103-133">**Элемент списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="9b103-133">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





