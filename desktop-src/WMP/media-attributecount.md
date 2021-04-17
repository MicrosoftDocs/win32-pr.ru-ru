---
title: Media. Аттрибутекаунт
description: Свойство Аттрибутекаунт извлекает количество атрибутов, которые могут быть запрошены или заданы для элемента мультимедиа.
ms.assetid: d2a5286f-dde1-48b5-b486-6cee1be463f9
keywords:
- Media. Аттрибутекаунт проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Media.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df4979f670cdd6a79b1b309bc3eceff5a2798223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708451"
---
# <a name="mediaattributecount"></a><span data-ttu-id="92438-104">Media. Аттрибутекаунт</span><span class="sxs-lookup"><span data-stu-id="92438-104">Media.attributeCount</span></span>

<span data-ttu-id="92438-105">Свойство **аттрибутекаунт** извлекает количество атрибутов, которые могут быть запрошены или заданы для элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="92438-105">The **attributeCount** property retrieves the number of attributes that can be queried and/or set for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="92438-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92438-106">Syntax</span></span>

<span data-ttu-id="92438-107">*проигрыватель*. *куррентмедиа*. **аттрибутекаунт**</span><span class="sxs-lookup"><span data-stu-id="92438-107">*player*.*currentMedia*.**attributeCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="92438-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="92438-108">Possible Values</span></span>

<span data-ttu-id="92438-109">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="92438-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="92438-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92438-110">Remarks</span></span>

<span data-ttu-id="92438-111">Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="92438-111">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="92438-112">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="92438-112">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="92438-113">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="92438-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="92438-114">**Проигрыватель Windows Media 10 Mobile:** Атрибуты для элемента мультимедиа доступны только во время воспроизведения, если они не извлекаются из элемента через коллекцию мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="92438-114">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="examples"></a><span data-ttu-id="92438-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="92438-115">Examples</span></span>

<span data-ttu-id="92438-116">В следующем примере JScript используется *носитель*. **аттрибутекаунт** для определения количества атрибутов, доступных в текущем элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="92438-116">The following JScript example uses *Media*.**attributeCount** to determine the number of attributes available in the current media item.</span></span> <span data-ttu-id="92438-117">Код использует это значение для печати списка имен и значений атрибутов в текстовой области HTML с именем myText.</span><span class="sxs-lookup"><span data-stu-id="92438-117">The code uses that value to print a list of attribute names and values in an HTML text area, named myText.</span></span> <span data-ttu-id="92438-118">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="92438-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Create arrays to hold each attribute name and value.
var atNames = new Array();
var atValues = new Array();

// Loop through the attribute list.   
for(var i = 0; i < cm.attributeCount; i++){

   // Fill the arrays with the attribute info.
   atNames[i] = cm.getAttributeName(i);
   atValues[i] = cm.getItemInfo(atNames[i]);

   // Print the attribute information to the text area.
   myText.value += atNames[i] + ": " + atValues[i];
   myText.value += "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="92438-119">Требования</span><span class="sxs-lookup"><span data-stu-id="92438-119">Requirements</span></span>



| <span data-ttu-id="92438-120">Требование</span><span class="sxs-lookup"><span data-stu-id="92438-120">Requirement</span></span> | <span data-ttu-id="92438-121">Значение</span><span class="sxs-lookup"><span data-stu-id="92438-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92438-122">Версия</span><span class="sxs-lookup"><span data-stu-id="92438-122">Version</span></span><br/> | <span data-ttu-id="92438-123">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="92438-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="92438-124">DLL</span><span class="sxs-lookup"><span data-stu-id="92438-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="92438-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92438-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92438-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92438-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92438-127">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="92438-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="92438-128">**Media. Жетаттрибутенаме**</span><span class="sxs-lookup"><span data-stu-id="92438-128">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="92438-129">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="92438-129">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="92438-130">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="92438-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="92438-131">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="92438-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





