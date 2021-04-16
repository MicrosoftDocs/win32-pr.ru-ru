---
title: Метод Media. Жетитеминфобитипе
description: Метод Жетитеминфобитипе извлекает значение атрибута, соответствующего указанному имени атрибута, языку и индексу.
ms.assetid: 9d3377c2-7ae8-48ce-a42e-9c965f6b79f9
keywords:
- Жетитеминфобитипе метод Windows Media Player
- Жетитеминфобитипе метод Windows Media Player, класс мультимедиа
- Класс мультимедиа проигрыватель Windows Media Player, метод Жетитеминфобитипе
topic_type:
- apiref
api_name:
- Media.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2aff2bee7641075bbac1dd04526ee751ea077a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699096"
---
# <a name="mediagetiteminfobytype-method"></a><span data-ttu-id="a211c-106">Метод Media. Жетитеминфобитипе</span><span class="sxs-lookup"><span data-stu-id="a211c-106">Media.getItemInfoByType method</span></span>

<span data-ttu-id="a211c-107">Метод **жетитеминфобитипе** извлекает значение атрибута, соответствующего указанному имени атрибута, языку и индексу.</span><span class="sxs-lookup"><span data-stu-id="a211c-107">The **getItemInfoByType** method retrieves the value of the attribute corresponding to the specified attribute name, language, and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="a211c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a211c-108">Syntax</span></span>


```JScript
retVal = Media.getItemInfoByType(
  name,
  language,
  index
)
```



## <a name="parameters"></a><span data-ttu-id="a211c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a211c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a211c-110">*имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a211c-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a211c-111">**Строка** , содержащая имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="a211c-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="a211c-112">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a211c-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="a211c-113">*языковая* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a211c-113">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a211c-114">**Строка** , представляющая язык.</span><span class="sxs-lookup"><span data-stu-id="a211c-114">**String** representing the language.</span></span> <span data-ttu-id="a211c-115">Если задано значение null или "" (пустая строка), используется текущая строка языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="a211c-115">If the value is set to null or "" (empty string) the current locale string is used.</span></span> <span data-ttu-id="a211c-116">В противном случае значение должно быть допустимой строкой языка RFC 1766, например "en-US".</span><span class="sxs-lookup"><span data-stu-id="a211c-116">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="a211c-117">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a211c-117">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a211c-118">**Число** (**Long**), содержащее Отсчитываемый от нуля индекс значения, извлекаемого из атрибута.</span><span class="sxs-lookup"><span data-stu-id="a211c-118">**Number** (**long**) containing the zero-based index of the value to retrieve from the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a211c-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a211c-119">Return value</span></span>

<span data-ttu-id="a211c-120">Этот метод возвращает **число**, **строку**, объект **метадатапиктуре** или объект **метадататекст** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a211c-120">This method returns a **Number**, **String**, **MetadataPicture** object, or **MetadataText** object as indicated in the following table.</span></span>



| <span data-ttu-id="a211c-121">attribute</span><span class="sxs-lookup"><span data-stu-id="a211c-121">Attribute</span></span>                   | <span data-ttu-id="a211c-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a211c-122">Return value</span></span>                   |
|-----------------------------|--------------------------------|
| <span data-ttu-id="a211c-123">**синкстате**</span><span class="sxs-lookup"><span data-stu-id="a211c-123">**SyncState**</span></span>               | <span data-ttu-id="a211c-124">**Число** (**без знака**)</span><span class="sxs-lookup"><span data-stu-id="a211c-124">**Number** (**unsigned long**)</span></span> |
| <span data-ttu-id="a211c-125">**WM/ \_ синхронизированы песен**</span><span class="sxs-lookup"><span data-stu-id="a211c-125">**WM/Lyrics\_Synchronised**</span></span> | <span data-ttu-id="a211c-126">Объект **метадататекст**</span><span class="sxs-lookup"><span data-stu-id="a211c-126">**MetadataText** object</span></span>        |
| <span data-ttu-id="a211c-127">**WM/Picture**</span><span class="sxs-lookup"><span data-stu-id="a211c-127">**WM/Picture**</span></span>              | <span data-ttu-id="a211c-128">Объект **метадатапиктуре**</span><span class="sxs-lookup"><span data-stu-id="a211c-128">**MetadataPicture** object</span></span>     |
| <span data-ttu-id="a211c-129">**WM/Усервебурл**</span><span class="sxs-lookup"><span data-stu-id="a211c-129">**WM/UserWebURL**</span></span>           | <span data-ttu-id="a211c-130">Объект **метадататекст**</span><span class="sxs-lookup"><span data-stu-id="a211c-130">**MetadataText** object</span></span>        |
| <span data-ttu-id="a211c-131">Все остальные атрибуты</span><span class="sxs-lookup"><span data-stu-id="a211c-131">All other attributes</span></span>        | <span data-ttu-id="a211c-132">**String**</span><span class="sxs-lookup"><span data-stu-id="a211c-132">**String**</span></span>                     |



 

<span data-ttu-id="a211c-133">Для атрибутов, базовое значение которых является **логическим**, этот метод возвращает строку "true" или "false".</span><span class="sxs-lookup"><span data-stu-id="a211c-133">For attributes whose underlying value is **Boolean**, this method returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="a211c-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a211c-134">Remarks</span></span>

<span data-ttu-id="a211c-135">Этот метод извлекает метаданные для отдельного элемента цифрового носителя или элемента мультимедиа, который является частью списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="a211c-135">This method retrieves the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="a211c-136">Этот метод поддерживает атрибуты с несколькими значениями и атрибутами со сложными значениями.</span><span class="sxs-lookup"><span data-stu-id="a211c-136">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="a211c-137">Метод **getItemInfo** не поддерживает атрибуты с несколькими значениями и атрибутами со сложными значениями.</span><span class="sxs-lookup"><span data-stu-id="a211c-137">The **getItemInfo** method does not support attributes with multiple values and attributes with complex values.</span></span>

<span data-ttu-id="a211c-138">Свойство **аттрибутекаунт** содержит количество имен атрибутов, доступных для данного объекта **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="a211c-138">The **attributeCount** property contains the number of attribute names available for a given **Media** object.</span></span> <span data-ttu-id="a211c-139">Номера индексов можно использовать с методом **жетаттрибутенаме** для определения имени каждого доступного атрибута.</span><span class="sxs-lookup"><span data-stu-id="a211c-139">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="a211c-140">Имена отдельных атрибутов можно передать в параметр *Name* объекта **жетитеминфобитипе**.</span><span class="sxs-lookup"><span data-stu-id="a211c-140">Individual attribute names can be passed to the *name* parameter of **getItemInfoByType**.</span></span>

<span data-ttu-id="a211c-141">Метод **жетаттрибутекаунтбитипе** возвращает количество атрибутов, соответствующих определенному имени атрибута для данного объекта **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="a211c-141">The **getAttributeCountByType** method returns the number of attributes that correspond to a particular attribute name for a given **Media** object.</span></span> <span data-ttu-id="a211c-142">Номера индексов можно передать в параметр *index* объекта **жетитеминфобитипе**.</span><span class="sxs-lookup"><span data-stu-id="a211c-142">Index numbers can then be passed to the *index* parameter of **getItemInfoByType**.</span></span> <span data-ttu-id="a211c-143">Это полезно, например, если для цифрового мультимедийного элемента была выполнена классификация по нескольким жанрам.</span><span class="sxs-lookup"><span data-stu-id="a211c-143">This is useful when a digital media item has been categorized under multiple genres, for example.</span></span>

<span data-ttu-id="a211c-144">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="a211c-144">To use this method, read access to the library is required.</span></span> <span data-ttu-id="a211c-145">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a211c-145">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="a211c-146">Этот метод может вызвать ошибки.</span><span class="sxs-lookup"><span data-stu-id="a211c-146">This method can cause errors.</span></span> <span data-ttu-id="a211c-147">При вызове этого метода необходимо включить код обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="a211c-147">You should include error-handling code when you call this method.</span></span> <span data-ttu-id="a211c-148">Например, в JScript можно реализовать обработку ошибок с помощью инструкции **try... перехватить... Наконец** , структура.</span><span class="sxs-lookup"><span data-stu-id="a211c-148">For example, in JScript you can implement error handling by using the **try...catch...finally** structure.</span></span>

<span data-ttu-id="a211c-149">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a211c-149">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="a211c-150">Требования</span><span class="sxs-lookup"><span data-stu-id="a211c-150">Requirements</span></span>



| <span data-ttu-id="a211c-151">Требование</span><span class="sxs-lookup"><span data-stu-id="a211c-151">Requirement</span></span> | <span data-ttu-id="a211c-152">Значение</span><span class="sxs-lookup"><span data-stu-id="a211c-152">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a211c-153">Версия</span><span class="sxs-lookup"><span data-stu-id="a211c-153">Version</span></span><br/> | <span data-ttu-id="a211c-154">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a211c-154">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="a211c-155">DLL</span><span class="sxs-lookup"><span data-stu-id="a211c-155">DLL</span></span><br/>     | <dl> <span data-ttu-id="a211c-156"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a211c-156"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a211c-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a211c-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a211c-158">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="a211c-158">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="a211c-159">**Media. Аттрибутекаунт**</span><span class="sxs-lookup"><span data-stu-id="a211c-159">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="a211c-160">**Media. Жетаттрибутекаунтбитипе**</span><span class="sxs-lookup"><span data-stu-id="a211c-160">**Media.getAttributeCountByType**</span></span>](media-getattributecountbytype.md)
</dt> <dt>

[<span data-ttu-id="a211c-161">**Media. Жетаттрибутенаме**</span><span class="sxs-lookup"><span data-stu-id="a211c-161">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="a211c-162">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="a211c-162">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="a211c-163">**Media. Сетитеминфо**</span><span class="sxs-lookup"><span data-stu-id="a211c-163">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="a211c-164">**Объект Метадатапиктуре**</span><span class="sxs-lookup"><span data-stu-id="a211c-164">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
</dt> <dt>

[<span data-ttu-id="a211c-165">**Объект Метадататекст**</span><span class="sxs-lookup"><span data-stu-id="a211c-165">**MetadataText Object**</span></span>](metadatatext-object.md)
</dt> <dt>

[<span data-ttu-id="a211c-166">**Считывание значений атрибутов**</span><span class="sxs-lookup"><span data-stu-id="a211c-166">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="a211c-167">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="a211c-167">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="a211c-168">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="a211c-168">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





