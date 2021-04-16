---
title: Метод Media. Жетитеминфобятом
description: Метод Жетитеминфобятом извлекает значение атрибута с указанным номером индекса.
ms.assetid: 6e2dea0c-c722-4737-9e8e-f5cb74156cea
keywords:
- Жетитеминфобятом метод Windows Media Player
- Жетитеминфобятом метод Windows Media Player, класс мультимедиа
- Класс мультимедиа проигрыватель Windows Media Player, метод Жетитеминфобятом
topic_type:
- apiref
api_name:
- Media.getItemInfoByAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf54d2ae177a65e1a71b5726090bba90f4ee4e5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699097"
---
# <a name="mediagetiteminfobyatom-method"></a><span data-ttu-id="aaa8a-106">Метод Media. Жетитеминфобятом</span><span class="sxs-lookup"><span data-stu-id="aaa8a-106">Media.getItemInfoByAtom method</span></span>

<span data-ttu-id="aaa8a-107">Метод **жетитеминфобятом** извлекает значение атрибута с указанным номером индекса.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-107">The **getItemInfoByAtom** method retrieves the value of the attribute with the specified index number.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaa8a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aaa8a-108">Syntax</span></span>


```JScript
strRetVal = Media.getItemInfoByAtom(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="aaa8a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="aaa8a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaa8a-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aaa8a-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa8a-111">**Число** (**длинное**), определяющее индекс, по которому данный атрибут находится в наборе доступных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-111">**Number** (**long**) specifying the index at which a given attribute resides within the set of available attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaa8a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aaa8a-112">Return value</span></span>

<span data-ttu-id="aaa8a-113">Этот метод возвращает **строку** , представляющую значение указанного атрибута.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-113">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="aaa8a-114">Для атрибутов, базовое значение которых является **логическим**, оно возвращает строку "true" или "false".</span><span class="sxs-lookup"><span data-stu-id="aaa8a-114">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="aaa8a-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aaa8a-115">Remarks</span></span>

<span data-ttu-id="aaa8a-116">Этот метод можно использовать для получения метаданных для конкретного цифрового элемента мультимедиа с помощью номера индекса атрибута.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-116">This method can be used to retrieve metadata for a specific digital media item by using an attribute index number.</span></span> <span data-ttu-id="aaa8a-117">Свойство **аттрибутекаунт** можно использовать для определения количества атрибутов, доступных для элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-117">The **attributeCount** property can be used to determine the number of attributes available for the media item.</span></span>

<span data-ttu-id="aaa8a-118">Метод **жетмедиаатом** объекта **медиаколлектион** также может использоваться для получения индекса определенного атрибута.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-118">The **getMediaAtom** method of the **MediaCollection** object can also be used to retrieve the index of a particular attribute.</span></span> <span data-ttu-id="aaa8a-119">Этот метод, как правило, более эффективен, чем методы **getItemInfo** или **жетитеминфобитипе** при работе с большими списками воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-119">This technique is generally more efficient than the **getItemInfo** or **getItemInfoByType** methods when working with large playlists.</span></span>

<span data-ttu-id="aaa8a-120">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-120">To use this method, read access to the library is required.</span></span> <span data-ttu-id="aaa8a-121">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="aaa8a-121">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="aaa8a-122">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-122">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

<span data-ttu-id="aaa8a-123">**Проигрыватель Windows Media 10 Mobile:** Атрибуты для элемента мультимедиа доступны только во время воспроизведения, если они не извлекаются из элемента через коллекцию мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-123">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaa8a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="aaa8a-124">Requirements</span></span>



| <span data-ttu-id="aaa8a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="aaa8a-125">Requirement</span></span> | <span data-ttu-id="aaa8a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="aaa8a-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aaa8a-127">Версия</span><span class="sxs-lookup"><span data-stu-id="aaa8a-127">Version</span></span><br/> | <span data-ttu-id="aaa8a-128">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="aaa8a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="aaa8a-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="aaa8a-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aaa8a-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaa8a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aaa8a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaa8a-132">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="aaa8a-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="aaa8a-133">**Media. Аттрибутекаунт**</span><span class="sxs-lookup"><span data-stu-id="aaa8a-133">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="aaa8a-134">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="aaa8a-134">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="aaa8a-135">**Media. Жетитеминфобитипе**</span><span class="sxs-lookup"><span data-stu-id="aaa8a-135">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="aaa8a-136">**Media. Сетитеминфо**</span><span class="sxs-lookup"><span data-stu-id="aaa8a-136">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="aaa8a-137">**Медиаколлектион. Жетмедиаатом**</span><span class="sxs-lookup"><span data-stu-id="aaa8a-137">**MediaCollection.getMediaAtom**</span></span>](mediacollection-getmediaatom.md)
</dt> <dt>

[<span data-ttu-id="aaa8a-138">**Считывание значений атрибутов**</span><span class="sxs-lookup"><span data-stu-id="aaa8a-138">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="aaa8a-139">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="aaa8a-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="aaa8a-140">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="aaa8a-140">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





