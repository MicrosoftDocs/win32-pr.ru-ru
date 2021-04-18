---
title: Controls. Куррентмаркер
description: Свойство Куррентмаркер указывает или получает номер текущего маркера.
ms.assetid: 4b4eacd4-3df0-4e11-8755-1ac326fad027
keywords:
- Проигрыватель Windows Media Controls. Куррентмаркер
topic_type:
- apiref
api_name:
- Controls.currentMarker
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aae8af226b62550b3faae9389385d321bf10aad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698790"
---
# <a name="controlscurrentmarker"></a><span data-ttu-id="1a3e1-104">Controls. Куррентмаркер</span><span class="sxs-lookup"><span data-stu-id="1a3e1-104">Controls.currentMarker</span></span>

<span data-ttu-id="1a3e1-105">Свойство **куррентмаркер** указывает или получает номер текущего маркера.</span><span class="sxs-lookup"><span data-stu-id="1a3e1-105">The **currentMarker** property specifies or retrieves the current marker number.</span></span>

``` syntax
player.controls.currentMarker
      
```

## <a name="possible-values"></a><span data-ttu-id="1a3e1-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="1a3e1-106">Possible Values</span></span>

<span data-ttu-id="1a3e1-107">Это свойство имеет **номер** для чтения и записи (**Long**) и значение по умолчанию 0.</span><span class="sxs-lookup"><span data-stu-id="1a3e1-107">This property is a read/write **Number** (**long**) with a default value of zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a3e1-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a3e1-108">Remarks</span></span>

<span data-ttu-id="1a3e1-109">Установка **куррентмаркер** приводит к запуску воспроизведения с указанного маркера.</span><span class="sxs-lookup"><span data-stu-id="1a3e1-109">Setting **currentMarker** causes playback to start from the specified marker.</span></span> <span data-ttu-id="1a3e1-110">Прежде чем приступить к установке **куррентмаркер**, определите, есть ли у файла маркеры и сколько он имеет с помощью **маркеркаунт**.</span><span class="sxs-lookup"><span data-stu-id="1a3e1-110">Before attempting to set **currentMarker**, determine whether a file has markers and how many it has by using **markerCount**.</span></span> <span data-ttu-id="1a3e1-111">Если у файла нет маркеров, установка **куррентмаркер** в любом случае, но ноль приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="1a3e1-111">If a file has no markers, setting **currentMarker** to anything but zero results in an error.</span></span> <span data-ttu-id="1a3e1-112">Установка **куррентмаркер** в число, превышающее **маркеркаунт** , также приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="1a3e1-112">Setting **currentMarker** to a number higher than **markerCount** also results in an error.</span></span>

<span data-ttu-id="1a3e1-113">Свойство **куррентмаркер** всегда возвращает текущий или последний маркер, то есть фактическое расположение файла может находиться либо на текущем маркере, либо перед следующим маркером.</span><span class="sxs-lookup"><span data-stu-id="1a3e1-113">The **currentMarker** property always returns the current or last marker, which means the actual file position can be either at the current marker or before the next marker.</span></span> <span data-ttu-id="1a3e1-114">Маркеры нумеруются, начиная с 1, поэтому если в файле есть маркеры, можно установить **куррентмаркер** в ноль, чтобы изменить расположение файла на ноль.</span><span class="sxs-lookup"><span data-stu-id="1a3e1-114">Markers are numbered beginning at 1, so if a file has markers, you can set **currentMarker** to zero to change the file position to zero.</span></span>

<span data-ttu-id="1a3e1-115">До тех пор, пока не будет задан текущий элемент мультимедиа (с помощью *проигрывателя*.**URL-адрес** или *проигрыватель*. **куррентмедиа**), **куррентмаркер** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="1a3e1-115">Until the current media item is set (using *Player*.**URL** or *Player*.**currentMedia**), **currentMarker** returns zero.</span></span>

## <a name="examples"></a><span data-ttu-id="1a3e1-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="1a3e1-116">Examples</span></span>

<span data-ttu-id="1a3e1-117">В следующем примере JScript используется **куррентмаркер** для запуска воспроизведения видео из маркера, соответствующего свойству **SelectedIndex** HTML-элемента SELECT.</span><span class="sxs-lookup"><span data-stu-id="1a3e1-117">The following JScript example uses **currentMarker** to start video playback from the marker that corresponds to the **selectedIndex** property of an HTML SELECT element.</span></span> <span data-ttu-id="1a3e1-118">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="1a3e1-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = "markers"  NAME = "markers"  LANGUAGE = "JScript"

    /* Seek to the marker number that corresponds to the SELECT element
       selectedIndex value when the list selection changes. */
    onChange = "Player.controls.currentMarker = markers.selectedIndex + 1;
">

    /* Fill the SELECT element with the marker identifiers. */
    <OPTION SELECTED>Sunrise
    <OPTION>Car chase 
    <OPTION>Happy ending
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="1a3e1-119">Требования</span><span class="sxs-lookup"><span data-stu-id="1a3e1-119">Requirements</span></span>



| <span data-ttu-id="1a3e1-120">Требование</span><span class="sxs-lookup"><span data-stu-id="1a3e1-120">Requirement</span></span> | <span data-ttu-id="1a3e1-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1a3e1-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1a3e1-122">Версия</span><span class="sxs-lookup"><span data-stu-id="1a3e1-122">Version</span></span><br/> | <span data-ttu-id="1a3e1-123">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="1a3e1-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1a3e1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1a3e1-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="1a3e1-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a3e1-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a3e1-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a3e1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a3e1-127">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="1a3e1-127">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="1a3e1-128">**Media. Маркеркаунт**</span><span class="sxs-lookup"><span data-stu-id="1a3e1-128">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="1a3e1-129">**Player. Куррентмедиа**</span><span class="sxs-lookup"><span data-stu-id="1a3e1-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="1a3e1-130">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="1a3e1-130">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





