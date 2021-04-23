---
title: Media. Маркеркаунт
description: Свойство Маркеркаунт извлекает количество маркеров в элементе мультимедиа.
ms.assetid: 48313395-b225-4008-b0e8-82fa22d6aaef
keywords:
- Media. Маркеркаунт проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Media.markerCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97a874211c0c00ebf9f242887d4314ec490b552
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695151"
---
# <a name="mediamarkercount"></a><span data-ttu-id="7921e-104">Media. Маркеркаунт</span><span class="sxs-lookup"><span data-stu-id="7921e-104">Media.markerCount</span></span>

<span data-ttu-id="7921e-105">Свойство **маркеркаунт** извлекает количество маркеров в элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7921e-105">The **markerCount** property retrieves the number of markers in the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="7921e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7921e-106">Syntax</span></span>

<span data-ttu-id="7921e-107">*проигрыватель*. *куррентмедиа*. **маркеркаунт**</span><span class="sxs-lookup"><span data-stu-id="7921e-107">*player*.*currentMedia*.**markerCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="7921e-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="7921e-108">Possible Values</span></span>

<span data-ttu-id="7921e-109">Это свойство является **числом** только для чтения (**длинное**), определяющим количество маркеров в файле.</span><span class="sxs-lookup"><span data-stu-id="7921e-109">This property is a read-only **Number** (**long**) specifying the number of markers in the file.</span></span>

## <a name="remarks"></a><span data-ttu-id="7921e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7921e-110">Remarks</span></span>

<span data-ttu-id="7921e-111">Это свойство возвращает нуль, если файл не имеет маркеров, или если элемент мультимедиа не совпадает с *проигрывателем*. **куррентмедиа**.</span><span class="sxs-lookup"><span data-stu-id="7921e-111">This property returns zero if a file has no markers, or if the media item is not the same as *Player*.**currentMedia**.</span></span>

<span data-ttu-id="7921e-112">Номера маркеров начинаются с 1.</span><span class="sxs-lookup"><span data-stu-id="7921e-112">Marker numbers start at 1.</span></span>

<span data-ttu-id="7921e-113">Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="7921e-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="7921e-114">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7921e-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7921e-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="7921e-115">Examples</span></span>

<span data-ttu-id="7921e-116">В следующем примере JScript используется *носитель*. **маркеркаунт** для получения количества маркеров в текущем элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7921e-116">The following JScript example uses *Media*.**markerCount** to retrieve the number of markers in the current media item.</span></span> <span data-ttu-id="7921e-117">Это значение затем используется в качестве верхней границы для циклической структуры, которая выполняет итерацию по списку маркеров для получения каждого имени маркера.</span><span class="sxs-lookup"><span data-stu-id="7921e-117">That value is then used as the upper boundary for a looping structure, which iterates through the marker list to retrieve each marker name.</span></span> <span data-ttu-id="7921e-118">Элемент TEXTAREA HTML с именем МНАМЕС отображает имена маркеров в текущем элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7921e-118">An HTML TEXTAREA element named MNAMES displays the names of the markers in the current media item.</span></span> <span data-ttu-id="7921e-119">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="7921e-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="7921e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="7921e-120">Requirements</span></span>



| <span data-ttu-id="7921e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="7921e-121">Requirement</span></span> | <span data-ttu-id="7921e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7921e-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7921e-123">Версия</span><span class="sxs-lookup"><span data-stu-id="7921e-123">Version</span></span><br/> | <span data-ttu-id="7921e-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="7921e-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7921e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7921e-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="7921e-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7921e-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7921e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7921e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7921e-128">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="7921e-128">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="7921e-129">**Player. Куррентмедиа**</span><span class="sxs-lookup"><span data-stu-id="7921e-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="7921e-130">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="7921e-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="7921e-131">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="7921e-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





