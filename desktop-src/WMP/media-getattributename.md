---
title: Метод Media. Жетаттрибутенаме
description: Метод Жетаттрибутенаме извлекает имя атрибута, соответствующего указанному индексу.
ms.assetid: f74d81c6-49f8-4b1e-a367-acb4a0914c5a
keywords:
- Жетаттрибутенаме метод Windows Media Player
- Жетаттрибутенаме метод Windows Media Player, класс мультимедиа
- Класс мультимедиа проигрыватель Windows Media Player, метод Жетаттрибутенаме
topic_type:
- apiref
api_name:
- Media.getAttributeName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7134b68837a7a5d1b765c64320ae68c56c6fc56
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694778"
---
# <a name="mediagetattributename-method"></a><span data-ttu-id="be873-106">Метод Media. Жетаттрибутенаме</span><span class="sxs-lookup"><span data-stu-id="be873-106">Media.getAttributeName method</span></span>

<span data-ttu-id="be873-107">Метод **жетаттрибутенаме** извлекает имя атрибута, соответствующего указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="be873-107">The **getAttributeName** method retrieves the name of the attribute corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="be873-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be873-108">Syntax</span></span>


```JScript
strRetVal = Media.getAttributeName(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="be873-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="be873-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be873-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be873-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be873-111">**Число** (**Long**), содержащее индекс атрибута.</span><span class="sxs-lookup"><span data-stu-id="be873-111">**Number** (**long**) containing the index of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be873-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be873-112">Return value</span></span>

<span data-ttu-id="be873-113">Этот метод возвращает **строку** , указывающую имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="be873-113">This method returns a **String** specifying the name of the attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="be873-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be873-114">Remarks</span></span>

<span data-ttu-id="be873-115">Возвращаемое имя атрибута можно использовать в сочетании с **getItemInfo** для получения значения для определенного именованного атрибута.</span><span class="sxs-lookup"><span data-stu-id="be873-115">The attribute name returned can be used in conjunction with **getItemInfo** to retrieve the value for a specific named attribute.</span></span>

<span data-ttu-id="be873-116">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="be873-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="be873-117">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="be873-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="be873-118">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="be873-118">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

<span data-ttu-id="be873-119">**Проигрыватель Windows Media 10 Mobile:** Атрибуты для элемента мультимедиа доступны только во время воспроизведения, если они не извлекаются из элемента через коллекцию мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="be873-119">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="examples"></a><span data-ttu-id="be873-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="be873-120">Examples</span></span>

<span data-ttu-id="be873-121">В следующем примере JScript используется *носитель*. **жетаттрибутенаме** для заполнения текстовой области HTML с именем myText с индексом и именем каждого атрибута для текущего элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="be873-121">The following JScript example uses *Media*.**getAttributeName** to fill an HTML text area named myText with the index and name of each attribute for the current media item.</span></span> <span data-ttu-id="be873-122">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="be873-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Get the number of attributes for the current media. 
var atCount = cm.attributeCount;

// Loop through the attribute list.
for(var i=0; i < atCount; i++){
   
   // Print each attribute index and name.   
   myText.value += "Attribute " + i +": ";
   myText.value += cm.getAttributeName(i);
   myText.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="be873-123">Требования</span><span class="sxs-lookup"><span data-stu-id="be873-123">Requirements</span></span>



| <span data-ttu-id="be873-124">Требование</span><span class="sxs-lookup"><span data-stu-id="be873-124">Requirement</span></span> | <span data-ttu-id="be873-125">Значение</span><span class="sxs-lookup"><span data-stu-id="be873-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="be873-126">Версия</span><span class="sxs-lookup"><span data-stu-id="be873-126">Version</span></span><br/> | <span data-ttu-id="be873-127">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="be873-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="be873-128">DLL</span><span class="sxs-lookup"><span data-stu-id="be873-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="be873-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be873-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be873-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be873-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be873-131">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="be873-131">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="be873-132">**Media. Аттрибутекаунт**</span><span class="sxs-lookup"><span data-stu-id="be873-132">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="be873-133">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="be873-133">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="be873-134">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="be873-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="be873-135">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="be873-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





