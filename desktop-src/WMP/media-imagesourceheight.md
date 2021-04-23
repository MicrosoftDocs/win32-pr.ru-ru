---
title: Media. Имажесаурцехеигхт
description: Свойство Имажесаурцехеигхт извлекает высоту текущего элемента мультимедиа в пикселях.
ms.assetid: fa98ec62-4c58-46ab-98f3-8017096d46d8
keywords:
- Media. Имажесаурцехеигхт проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Media.imageSourceHeight
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de364243e71c6653085b4c9c9ff81f148dc299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695205"
---
# <a name="mediaimagesourceheight"></a><span data-ttu-id="57aae-104">Media. Имажесаурцехеигхт</span><span class="sxs-lookup"><span data-stu-id="57aae-104">Media.imageSourceHeight</span></span>

<span data-ttu-id="57aae-105">Свойство **имажесаурцехеигхт** извлекает высоту текущего элемента мультимедиа в пикселях.</span><span class="sxs-lookup"><span data-stu-id="57aae-105">The **ImageSourceHeight** property retrieves the height of the current media item in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="57aae-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57aae-106">Syntax</span></span>

<span data-ttu-id="57aae-107">*проигрыватель*. *куррентмедиа*. **имажесаурцехеигхт**</span><span class="sxs-lookup"><span data-stu-id="57aae-107">*player*.*currentMedia*.**imageSourceHeight**</span></span>

## <a name="possible-values"></a><span data-ttu-id="57aae-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="57aae-108">Possible Values</span></span>

<span data-ttu-id="57aae-109">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="57aae-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="57aae-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="57aae-110">Remarks</span></span>

<span data-ttu-id="57aae-111">Если элемент мультимедиа не является текущим, это свойство возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="57aae-111">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="57aae-112">Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="57aae-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="57aae-113">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="57aae-113">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="57aae-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="57aae-114">Examples</span></span>

<span data-ttu-id="57aae-115">В следующем примере на языке JScript используется *Media*. имажесаурцехеигхт для вывода размера изображения (в пикселях) текущего элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="57aae-115">The following JScript example uses *Media*.imageSourceHeight to display the image size, in pixels, of the current media item.</span></span> <span data-ttu-id="57aae-116">Сведения выводятся в HTML-элемент TEXTAREA с именем Видеосизе.</span><span class="sxs-lookup"><span data-stu-id="57aae-116">The information is printed to an HTML TEXTAREA element named VideoSize.</span></span> <span data-ttu-id="57aae-117">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="57aae-117">The **Player** object was created with ID = "player".</span></span>


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Store the height and width of the new media item.
   var Height = Player.currentMedia.imageSourceHeight;
   var Width =  Player.currentMedia.imageSourceWidth;

   // Erase the information in the text area.
   VideoSize.value = "";

   // Test whether an image is visible.
   if (Height != 0 && Width != 0)

      // Display the image size information.
      VideoSize.value = Width + " x " + Height;
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="57aae-118">Требования</span><span class="sxs-lookup"><span data-stu-id="57aae-118">Requirements</span></span>



| <span data-ttu-id="57aae-119">Требование</span><span class="sxs-lookup"><span data-stu-id="57aae-119">Requirement</span></span> | <span data-ttu-id="57aae-120">Значение</span><span class="sxs-lookup"><span data-stu-id="57aae-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="57aae-121">Версия</span><span class="sxs-lookup"><span data-stu-id="57aae-121">Version</span></span><br/> | <span data-ttu-id="57aae-122">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="57aae-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="57aae-123">DLL</span><span class="sxs-lookup"><span data-stu-id="57aae-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="57aae-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57aae-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57aae-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57aae-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57aae-126">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="57aae-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="57aae-127">**Player. Куррентмедиа**</span><span class="sxs-lookup"><span data-stu-id="57aae-127">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="57aae-128">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="57aae-128">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="57aae-129">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="57aae-129">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





