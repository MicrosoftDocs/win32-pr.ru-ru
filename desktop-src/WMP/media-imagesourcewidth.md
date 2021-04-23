---
title: Media. Имажесаурцевидс
description: Свойство Имажесаурцевидс извлекает ширину текущего элемента мультимедиа в пикселях.
ms.assetid: 6559bd51-cec2-4fc6-aab8-f2fdd1d59bae
keywords:
- Media. Имажесаурцевидс проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Media.imageSourceWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2a3fef7b74a3d033b058f0afd1f6eece007bd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695204"
---
# <a name="mediaimagesourcewidth"></a><span data-ttu-id="595fc-104">Media. Имажесаурцевидс</span><span class="sxs-lookup"><span data-stu-id="595fc-104">Media.imageSourceWidth</span></span>

<span data-ttu-id="595fc-105">Свойство **имажесаурцевидс** извлекает ширину текущего элемента мультимедиа в пикселях.</span><span class="sxs-lookup"><span data-stu-id="595fc-105">The **imageSourceWidth** property retrieves the width of the current media item in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="595fc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="595fc-106">Syntax</span></span>

<span data-ttu-id="595fc-107">*проигрыватель*. *куррентмедиа*. **имажесаурцевидс**</span><span class="sxs-lookup"><span data-stu-id="595fc-107">*player*.*currentMedia*.**imageSourceWidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="595fc-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="595fc-108">Possible Values</span></span>

<span data-ttu-id="595fc-109">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="595fc-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="595fc-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="595fc-110">Remarks</span></span>

<span data-ttu-id="595fc-111">Если элемент мультимедиа не является текущим, это свойство возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="595fc-111">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="595fc-112">Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="595fc-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="595fc-113">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="595fc-113">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="595fc-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="595fc-114">Examples</span></span>

<span data-ttu-id="595fc-115">В следующем примере JScript используется *носитель*. **имажесаурцевидс** для вывода размера изображения (в пикселях) **текущего элемента мультимедиа. Сведения выводятся в HTML-элемент TEXTAREA с именем Видеосизе. Объект Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="595fc-115">The following JScript example uses *Media*.**imageSourceWidth** to display the image size, in pixels, of the **current media item. The information is printed to an HTML TEXTAREA element named VideoSize. The Player** object was created with ID = "player".</span></span>


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player"  EVENT = OpenStateChange(NewState)>

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



## <a name="requirements"></a><span data-ttu-id="595fc-116">Требования</span><span class="sxs-lookup"><span data-stu-id="595fc-116">Requirements</span></span>



| <span data-ttu-id="595fc-117">Требование</span><span class="sxs-lookup"><span data-stu-id="595fc-117">Requirement</span></span> | <span data-ttu-id="595fc-118">Значение</span><span class="sxs-lookup"><span data-stu-id="595fc-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="595fc-119">Версия</span><span class="sxs-lookup"><span data-stu-id="595fc-119">Version</span></span><br/> | <span data-ttu-id="595fc-120">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="595fc-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="595fc-121">DLL</span><span class="sxs-lookup"><span data-stu-id="595fc-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="595fc-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="595fc-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="595fc-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="595fc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="595fc-124">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="595fc-124">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="595fc-125">**Player. Куррентмедиа**</span><span class="sxs-lookup"><span data-stu-id="595fc-125">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="595fc-126">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="595fc-126">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="595fc-127">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="595fc-127">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





