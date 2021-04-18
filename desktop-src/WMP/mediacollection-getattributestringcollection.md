---
title: Медиаколлектион. Жетаттрибутестрингколлектион, метод
description: Метод Жетаттрибутестрингколлектион извлекает объект StringCollection, представляющий набор всех значений для указанного атрибута в пределах указанного типа мультимедиа.
ms.assetid: 75563a75-88f5-419e-983b-d105bce02511
keywords:
- Жетаттрибутестрингколлектион метод Windows Media Player
- Жетаттрибутестрингколлектион метод Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион Windows Media Player, метод Жетаттрибутестрингколлектион
topic_type:
- apiref
api_name:
- MediaCollection.getAttributeStringCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d50d25488a05e6076c99802ce738edf02298ade
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689060"
---
# <a name="mediacollectiongetattributestringcollection-method"></a><span data-ttu-id="7fee9-106">Медиаколлектион. Жетаттрибутестрингколлектион, метод</span><span class="sxs-lookup"><span data-stu-id="7fee9-106">MediaCollection.getAttributeStringCollection method</span></span>

<span data-ttu-id="7fee9-107">Метод **жетаттрибутестрингколлектион** извлекает объект **StringCollection** , представляющий набор всех значений для указанного атрибута в пределах указанного типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7fee9-107">The **getAttributeStringCollection** method retrieves a **StringCollection** object representing the set of all values for a specified attribute within a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fee9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7fee9-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getAttributeStringCollection(
  attribute,
  mediaType
)
```



## <a name="parameters"></a><span data-ttu-id="7fee9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7fee9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fee9-110">*атрибут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7fee9-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fee9-111">**Строка** , указывающая атрибут.</span><span class="sxs-lookup"><span data-stu-id="7fee9-111">**String** specifying the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="7fee9-112">*mediaType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7fee9-112">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fee9-113">**Строка** , представляющая тип носителя.</span><span class="sxs-lookup"><span data-stu-id="7fee9-113">**String** representing the media type.</span></span> <span data-ttu-id="7fee9-114">Содержит одно из следующих значений: "звук", "видео", "список воспроизведения" или "другое".</span><span class="sxs-lookup"><span data-stu-id="7fee9-114">Contains one of the following values: "Audio", "Video", "Playlist", or "Other".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fee9-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7fee9-115">Return value</span></span>

<span data-ttu-id="7fee9-116">Этот метод возвращает объект **StringCollection** .</span><span class="sxs-lookup"><span data-stu-id="7fee9-116">This method returns a **StringCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fee9-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7fee9-117">Remarks</span></span>

<span data-ttu-id="7fee9-118">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="7fee9-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="7fee9-119">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7fee9-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="7fee9-120">Дополнительные сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в разделе [Справочник по атрибутам](attribute-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="7fee9-120">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md) section.</span></span>

## <a name="examples"></a><span data-ttu-id="7fee9-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="7fee9-121">Examples</span></span>

<span data-ttu-id="7fee9-122">В следующем примере JScript используется *медиаколлектион*. **жетаттрибутестрингколлектион** для вывода списка значений, соответствующих определенному атрибуту для звуковых элементов в коллекции мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7fee9-122">The following JScript example uses *MediaCollection*.**getAttributeStringCollection** to display a list of values that correspond to a particular attribute for audio items in the media collection.</span></span> <span data-ttu-id="7fee9-123">HTML-элемент SELECT, созданный с помощью ID = "Attribute", позволяет пользователю выбрать атрибут, например исполнитель, жанр или альбом.</span><span class="sxs-lookup"><span data-stu-id="7fee9-123">An HTML SELECT element, created with ID = "Attribute", allows the user to select an attribute, such as Artist, Genre, or Album.</span></span> <span data-ttu-id="7fee9-124">Элемент TEXTAREA HTML, созданный с помощью ID = "Аттрибутевалс", отображает результат.</span><span class="sxs-lookup"><span data-stu-id="7fee9-124">An HTML TEXTAREA element, created with ID = "AttributeVals", displays the result.</span></span> <span data-ttu-id="7fee9-125">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="7fee9-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Clear the text in the display area.
AttributeVals.value = "";

// Store the mediaCollection object.
var library = Player.mediaCollection;

// Get the string collection for the attribute type the user selects.
var all = library.getAttributeStringCollection(Attribute.value, "Audio");

// Loop through the string collection.
for (i = 0; i < all.count; i++){

    // Display the items one line at a time.
    AttributeVals.value += all.item(i);
    AttributeVals.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="7fee9-126">Требования</span><span class="sxs-lookup"><span data-stu-id="7fee9-126">Requirements</span></span>



| <span data-ttu-id="7fee9-127">Требование</span><span class="sxs-lookup"><span data-stu-id="7fee9-127">Requirement</span></span> | <span data-ttu-id="7fee9-128">Значение</span><span class="sxs-lookup"><span data-stu-id="7fee9-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7fee9-129">Версия</span><span class="sxs-lookup"><span data-stu-id="7fee9-129">Version</span></span><br/> | <span data-ttu-id="7fee9-130">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="7fee9-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7fee9-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7fee9-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="7fee9-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fee9-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fee9-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7fee9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fee9-134">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="7fee9-134">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="7fee9-135">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="7fee9-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="7fee9-136">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="7fee9-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="7fee9-137">**Объект StringCollection**</span><span class="sxs-lookup"><span data-stu-id="7fee9-137">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





