---
title: Метод Media. getItemInfo
description: Метод getItemInfo извлекает значение указанного атрибута для текущего элемента мультимедиа.
ms.assetid: a1ee0d40-b979-424b-bd4e-d1acf6354d8d
keywords:
- getItemInfo метод Windows Media Player
- getItemInfo метод Windows Media Player, класс мультимедиа
- Класс мультимедиа проигрыватель Windows Media Player, метод getItemInfo
topic_type:
- apiref
api_name:
- Media.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7e7348e73e3550ed668f6694ccfe9ed615215b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699098"
---
# <a name="mediagetiteminfo-method"></a><span data-ttu-id="fb4e2-106">Метод Media. getItemInfo</span><span class="sxs-lookup"><span data-stu-id="fb4e2-106">Media.getItemInfo method</span></span>

<span data-ttu-id="fb4e2-107">Метод **getItemInfo** извлекает значение указанного атрибута для текущего элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-107">The **getItemInfo** method retrieves the value of the specified attribute for the current media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb4e2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb4e2-108">Syntax</span></span>


```JScript
strRetVal = Media.getItemInfo(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="fb4e2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb4e2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb4e2-110">*имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fb4e2-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb4e2-111">**Строка** , содержащая имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="fb4e2-112">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb4e2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb4e2-113">Return value</span></span>

<span data-ttu-id="fb4e2-114">Этот метод возвращает **строку** , представляющую значение указанного атрибута.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-114">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="fb4e2-115">Для атрибутов, базовое значение которых является **логическим**, оно возвращает строку "true" или "false".</span><span class="sxs-lookup"><span data-stu-id="fb4e2-115">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="fb4e2-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fb4e2-116">Remarks</span></span>

<span data-ttu-id="fb4e2-117">Этот метод извлекает метаданные для отдельного элемента цифрового носителя или элемента мультимедиа, который является частью списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-117">This method retrieves the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="fb4e2-118">Свойство **аттрибутекаунт** содержит количество имен атрибутов, доступных для данного объекта **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="fb4e2-118">The **attributeCount** property contains the number of attribute names available for a given **Media** object.</span></span> <span data-ttu-id="fb4e2-119">Номера индексов можно использовать с методом **жетаттрибутенаме** для определения имени каждого доступного атрибута.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-119">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="fb4e2-120">Имена отдельных атрибутов можно передать в **getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-120">Individual attribute names can be passed to **getItemInfo**.</span></span>

<span data-ttu-id="fb4e2-121">Чтобы получить атрибуты с несколькими значениями и атрибутами со сложными значениями, используйте метод **жетитеминфобитипе** .</span><span class="sxs-lookup"><span data-stu-id="fb4e2-121">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="fb4e2-122">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-122">To use this method, read access to the library is required.</span></span> <span data-ttu-id="fb4e2-123">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="fb4e2-123">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="fb4e2-124">Чтобы предоставить общий доступ к библиотекам Windows Media через UPnP, проигрыватель Windows Media создает службу каталогов содержимого (CD), доступную через UPnP.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-124">To share the Windows media libraries over UPnP, Windows Media Player creates a content directory service (CDS) that is exposed over UPnP.</span></span> <span data-ttu-id="fb4e2-125">После этого другие устройства могут перемещаться по библиотекам и просматривать их.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-125">Other devices can then navigate and browse the libraries.</span></span>

<span data-ttu-id="fb4e2-126">В Windows 7 приложение может использовать атрибуты [**TrackingID**](trackingid-attribute.md) и [**mediaType**](mediatype-attribute.md) проигрывателя Windows Media для создания идентификатора объекта для каждого элемента на компакт-диске.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-126">In Windows 7, an application can use the Windows Media Player [**TrackingID**](trackingid-attribute.md) and [**MediaType**](mediatype-attribute.md) attributes to construct the object ID of each item in the CDS.</span></span> <span data-ttu-id="fb4e2-127">Обратите внимание, что эта конструкция может измениться в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-127">Note that this construction might change in future versions of Windows.</span></span> <span data-ttu-id="fb4e2-128">Приложение передает каждую из этих строк атрибута в параметре *Name* в вызове **getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-128">The application passes each of these attribute strings in the *name* parameter in a call to **getItemInfo**.</span></span> <span data-ttu-id="fb4e2-129">**getItemInfo** возвращает значение для каждого атрибута в возвращаемом значении.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-129">**getItemInfo** returns the value for each attribute in the return value.</span></span> <span data-ttu-id="fb4e2-130">Затем приложение использует следующий синтаксис для создания каждого идентификатора объекта:</span><span class="sxs-lookup"><span data-stu-id="fb4e2-130">The application then uses the following syntax to construct each object ID:</span></span>

<span data-ttu-id="fb4e2-131">*TrackingID*. 0. *Медиатипеид*</span><span class="sxs-lookup"><span data-stu-id="fb4e2-131">*TrackingID*.0.*MediaTypeID*</span></span>

<span data-ttu-id="fb4e2-132">Этот синтаксис имеет следующий смысл:</span><span class="sxs-lookup"><span data-stu-id="fb4e2-132">This syntax has the following meaning:</span></span>

-   <span data-ttu-id="fb4e2-133">*TrackingID* — это строка, которая хранится в атрибуте [**TrackingID**](trackingid-attribute.md) проигрывателя Windows Media элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-133">*TrackingID* is the string that is stored in the Windows Media Player [**TrackingID**](trackingid-attribute.md) attribute of the media item.</span></span>
-   <span data-ttu-id="fb4e2-134">*Медиатипеид* зависит от значения атрибута [**mediaType**](mediatype-attribute.md) , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-134">*MediaTypeID* depends on the value of the [**MediaType**](mediatype-attribute.md) attribute, as shown in the following table:</span></span>

    | <span data-ttu-id="fb4e2-135">Атрибут MediaType</span><span class="sxs-lookup"><span data-stu-id="fb4e2-135">MediaType attribute</span></span>                      | <span data-ttu-id="fb4e2-136">медиатипеид</span><span class="sxs-lookup"><span data-stu-id="fb4e2-136">MediaTypeID</span></span> |
    |------------------------------------------|-------------|
    | [<span data-ttu-id="fb4e2-137">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="fb4e2-137">Audio Items</span></span>](audio-item-attributes.md) | <span data-ttu-id="fb4e2-138">4</span><span class="sxs-lookup"><span data-stu-id="fb4e2-138">4</span></span>           |
    | [<span data-ttu-id="fb4e2-139">Элементы фото</span><span class="sxs-lookup"><span data-stu-id="fb4e2-139">Photo Items</span></span>](photo-item-attributes.md) | <span data-ttu-id="fb4e2-140">B</span><span class="sxs-lookup"><span data-stu-id="fb4e2-140">B</span></span>           |
    | [<span data-ttu-id="fb4e2-141">Элементы видео</span><span class="sxs-lookup"><span data-stu-id="fb4e2-141">Video Items</span></span>](video-item-attributes.md) | <span data-ttu-id="fb4e2-142">8</span><span class="sxs-lookup"><span data-stu-id="fb4e2-142">8</span></span>           |

    

     

<span data-ttu-id="fb4e2-143">**Проигрыватель Windows Media 10 Mobile:** Атрибуты для элемента мультимедиа доступны только во время воспроизведения, если они не извлекаются из элемента через коллекцию мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-143">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb4e2-144">Требования</span><span class="sxs-lookup"><span data-stu-id="fb4e2-144">Requirements</span></span>



| <span data-ttu-id="fb4e2-145">Требование</span><span class="sxs-lookup"><span data-stu-id="fb4e2-145">Requirement</span></span> | <span data-ttu-id="fb4e2-146">Значение</span><span class="sxs-lookup"><span data-stu-id="fb4e2-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb4e2-147">Версия</span><span class="sxs-lookup"><span data-stu-id="fb4e2-147">Version</span></span><br/> | <span data-ttu-id="fb4e2-148">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-148">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fb4e2-149">DLL</span><span class="sxs-lookup"><span data-stu-id="fb4e2-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="fb4e2-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb4e2-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb4e2-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb4e2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb4e2-152">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="fb4e2-152">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="fb4e2-153">**Media. Аттрибутекаунт**</span><span class="sxs-lookup"><span data-stu-id="fb4e2-153">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="fb4e2-154">**Media. Жетаттрибутенаме**</span><span class="sxs-lookup"><span data-stu-id="fb4e2-154">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="fb4e2-155">**Media. Жетитеминфобитипе**</span><span class="sxs-lookup"><span data-stu-id="fb4e2-155">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="fb4e2-156">**Media. Сетитеминфо**</span><span class="sxs-lookup"><span data-stu-id="fb4e2-156">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="fb4e2-157">**Считывание значений атрибутов**</span><span class="sxs-lookup"><span data-stu-id="fb4e2-157">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="fb4e2-158">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="fb4e2-158">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="fb4e2-159">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="fb4e2-159">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





