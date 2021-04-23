---
title: Media. Дуратионстринг
description: Свойство Дуратионстринг извлекает строковое значение, указывающее длительность текущего элемента мультимедиа в формате чч мм СС.
ms.assetid: dfcb4c2e-c62c-4c3e-a9f4-fd147fb5b28c
keywords:
- Media. Дуратионстринг проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Media.durationString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1bbb89716ab1d06b176754396611ab22980659
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708449"
---
# <a name="mediadurationstring"></a><span data-ttu-id="5ff85-104">Media. Дуратионстринг</span><span class="sxs-lookup"><span data-stu-id="5ff85-104">Media.durationString</span></span>

<span data-ttu-id="5ff85-105">Свойство **дуратионстринг** извлекает **строковое** значение, указывающее длительность текущего элемента мультимедиа в формате чч: мм: СС.</span><span class="sxs-lookup"><span data-stu-id="5ff85-105">The **durationString** property retrieves a **String** value indicating the duration of the current media item in HH:MM:SS format.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ff85-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ff85-106">Syntax</span></span>

<span data-ttu-id="5ff85-107">*проигрыватель*. *куррентмедиа*. **дуратионстринг**</span><span class="sxs-lookup"><span data-stu-id="5ff85-107">*player*.*currentMedia*.**durationString**</span></span>

## <a name="possible-values"></a><span data-ttu-id="5ff85-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="5ff85-108">Possible Values</span></span>

<span data-ttu-id="5ff85-109">Это свойство является **строкой**, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5ff85-109">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ff85-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ff85-110">Remarks</span></span>

<span data-ttu-id="5ff85-111">Если это свойство используется с элементом мультимедиа, отличным от указанного в *проигрывателе*. **куррентмедиа**, он может не содержать допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="5ff85-111">If this property is used with a media item other than the one specified in *Player*.**currentMedia**, it may not contain a valid value.</span></span> <span data-ttu-id="5ff85-112">Если размер элемента мультимедиа меньше часа, часть значения чч: в возвращаемом значении не указывается.</span><span class="sxs-lookup"><span data-stu-id="5ff85-112">If the media item is less than an hour long, the HH: portion of the return value is omitted.</span></span>

<span data-ttu-id="5ff85-113">Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="5ff85-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="5ff85-114">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5ff85-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5ff85-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="5ff85-115">Examples</span></span>

<span data-ttu-id="5ff85-116">В следующем примере JScript используется *носитель*. **дуратионстринг** , чтобы отобразить длительность текущего элемента мультимедиа в виде форматированного текста.</span><span class="sxs-lookup"><span data-stu-id="5ff85-116">The following JScript example uses *Media*.**durationString** to display the duration of the current media item as formatted text.</span></span> <span data-ttu-id="5ff85-117">Элемент HTML DIV с именем файла MediaInfo отображает сведения о длительности.</span><span class="sxs-lookup"><span data-stu-id="5ff85-117">An HTML DIV element named MediaInfo displays the duration information.</span></span> <span data-ttu-id="5ff85-118">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="5ff85-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler to update the display when
 the current media item changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Write the formatted duration string to the DIV region.
   MediaInfo.innerHTML = "Duration: " + Player.currentMedia.durationString;
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="5ff85-119">Требования</span><span class="sxs-lookup"><span data-stu-id="5ff85-119">Requirements</span></span>



| <span data-ttu-id="5ff85-120">Требование</span><span class="sxs-lookup"><span data-stu-id="5ff85-120">Requirement</span></span> | <span data-ttu-id="5ff85-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5ff85-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5ff85-122">Версия</span><span class="sxs-lookup"><span data-stu-id="5ff85-122">Version</span></span><br/> | <span data-ttu-id="5ff85-123">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="5ff85-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5ff85-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5ff85-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="5ff85-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ff85-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ff85-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ff85-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ff85-127">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="5ff85-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="5ff85-128">**Носитель. Длительность**</span><span class="sxs-lookup"><span data-stu-id="5ff85-128">**Media.duration**</span></span>](media-duration.md)
</dt> <dt>

[<span data-ttu-id="5ff85-129">**Player. Куррентмедиа**</span><span class="sxs-lookup"><span data-stu-id="5ff85-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="5ff85-130">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="5ff85-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="5ff85-131">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="5ff85-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





