---
title: StringCollection. Жетитеминфобитипе, метод
description: Метод Жетитеминфобитипе извлекает значение, соответствующее указанному индексу StringCollection, имени, языку и индексу атрибута.
ms.assetid: 32a25c69-9399-4857-84c1-143c529be58f
keywords:
- Жетитеминфобитипе метод Windows Media Player
- Жетитеминфобитипе метод Windows Media Player, класс StringCollection
- Класс StringCollection Windows Media Player, метод Жетитеминфобитипе
topic_type:
- apiref
api_name:
- StringCollection.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b3aa8c5bc367095765f24f19f107dd7cb986ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717855"
---
# <a name="stringcollectiongetiteminfobytype-method"></a><span data-ttu-id="e2e41-106">StringCollection. Жетитеминфобитипе, метод</span><span class="sxs-lookup"><span data-stu-id="e2e41-106">StringCollection.getItemInfoByType method</span></span>

<span data-ttu-id="e2e41-107">Метод **жетитеминфобитипе** извлекает значение, соответствующее указанному индексу **StringCollection** , имени, языку и индексу атрибута.</span><span class="sxs-lookup"><span data-stu-id="e2e41-107">The **getItemInfoByType** method retrieves the value corresponding to the specified **StringCollection** index, name, language, and attribute index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2e41-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2e41-108">Syntax</span></span>


```JScript
retVal = StringCollection.getItemInfoByType(
  index,
  name,
  language,
  attributeIndex
)
```



## <a name="parameters"></a><span data-ttu-id="e2e41-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2e41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2e41-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2e41-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e41-111">**Число** (**Long**), указывающее Отсчитываемый от нуля индекс элемента **StringCollection** , из которого необходимо получить атрибут.</span><span class="sxs-lookup"><span data-stu-id="e2e41-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="e2e41-112">*имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2e41-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e41-113">**Строка** , содержащая имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="e2e41-113">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="e2e41-114">*языковая* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2e41-114">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e41-115">**Строка** , содержащая язык.</span><span class="sxs-lookup"><span data-stu-id="e2e41-115">**String** containing the language.</span></span> <span data-ttu-id="e2e41-116">Если задано значение null или пустая строка (""), используется текущая строка языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="e2e41-116">If the value is set to null or the empty string ("") the current locale string is used.</span></span> <span data-ttu-id="e2e41-117">В противном случае значение должно быть допустимой строкой языка RFC 1766, например "en-US".</span><span class="sxs-lookup"><span data-stu-id="e2e41-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="e2e41-118">*аттрибутеиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2e41-118">*attributeIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e41-119">**Число** (**Long**), содержащее Отсчитываемый от нуля индекс значения, извлекаемого из атрибута.</span><span class="sxs-lookup"><span data-stu-id="e2e41-119">**Number** (**long**) containing the zero-based index of the value to retrieve from the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2e41-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2e41-120">Return value</span></span>

<span data-ttu-id="e2e41-121">Этот метод возвращает **число**, **строку**, объект **метадатапиктуре** или объект **метадататекст** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e2e41-121">This method returns a **Number**, **String**, **MetadataPicture** object, or **MetadataText** object as indicated in the following table.</span></span>



| <span data-ttu-id="e2e41-122">attribute</span><span class="sxs-lookup"><span data-stu-id="e2e41-122">Attribute</span></span>                   | <span data-ttu-id="e2e41-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2e41-123">Return value</span></span>                   |
|-----------------------------|--------------------------------|
| <span data-ttu-id="e2e41-124">**синкстате**</span><span class="sxs-lookup"><span data-stu-id="e2e41-124">**SyncState**</span></span>               | <span data-ttu-id="e2e41-125">**Число** (**без знака**)</span><span class="sxs-lookup"><span data-stu-id="e2e41-125">**Number** (**unsigned long**)</span></span> |
| <span data-ttu-id="e2e41-126">**WM/ \_ синхронизированы песен**</span><span class="sxs-lookup"><span data-stu-id="e2e41-126">**WM/Lyrics\_Synchronised**</span></span> | <span data-ttu-id="e2e41-127">Объект **метадататекст**</span><span class="sxs-lookup"><span data-stu-id="e2e41-127">**MetadataText** object</span></span>        |
| <span data-ttu-id="e2e41-128">**WM/Picture**</span><span class="sxs-lookup"><span data-stu-id="e2e41-128">**WM/Picture**</span></span>              | <span data-ttu-id="e2e41-129">Объект **метадатапиктуре**</span><span class="sxs-lookup"><span data-stu-id="e2e41-129">**MetadataPicture** object</span></span>     |
| <span data-ttu-id="e2e41-130">**WM/Усервебурл**</span><span class="sxs-lookup"><span data-stu-id="e2e41-130">**WM/UserWebURL**</span></span>           | <span data-ttu-id="e2e41-131">Объект **метадататекст**</span><span class="sxs-lookup"><span data-stu-id="e2e41-131">**MetadataText** object</span></span>        |
| <span data-ttu-id="e2e41-132">Все остальные атрибуты</span><span class="sxs-lookup"><span data-stu-id="e2e41-132">All other attributes</span></span>        | <span data-ttu-id="e2e41-133">Строка</span><span class="sxs-lookup"><span data-stu-id="e2e41-133">String</span></span>                         |



 

<span data-ttu-id="e2e41-134">Для атрибутов, базовое значение которых является **логическим**, этот метод возвращает строку "true" или "false".</span><span class="sxs-lookup"><span data-stu-id="e2e41-134">For attributes whose underlying value is **Boolean**, this method returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="e2e41-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2e41-135">Remarks</span></span>

<span data-ttu-id="e2e41-136">Этот метод поддерживает атрибуты с несколькими значениями и атрибуты со сложными значениями.</span><span class="sxs-lookup"><span data-stu-id="e2e41-136">This method supports attributes with multiple values, and attributes with complex values.</span></span> <span data-ttu-id="e2e41-137">Метод **getItemInfo** не поддерживает атрибуты с несколькими или сложными значениями.</span><span class="sxs-lookup"><span data-stu-id="e2e41-137">The **getItemInfo** method does not support attributes with multiple or complex values.</span></span>

<span data-ttu-id="e2e41-138">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="e2e41-138">To use this method, read access to the library is required.</span></span> <span data-ttu-id="e2e41-139">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e2e41-139">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2e41-140">Требования</span><span class="sxs-lookup"><span data-stu-id="e2e41-140">Requirements</span></span>



| <span data-ttu-id="e2e41-141">Требование</span><span class="sxs-lookup"><span data-stu-id="e2e41-141">Requirement</span></span> | <span data-ttu-id="e2e41-142">Значение</span><span class="sxs-lookup"><span data-stu-id="e2e41-142">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e2e41-143">Версия</span><span class="sxs-lookup"><span data-stu-id="e2e41-143">Version</span></span><br/> | <span data-ttu-id="e2e41-144">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="e2e41-144">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="e2e41-145">DLL</span><span class="sxs-lookup"><span data-stu-id="e2e41-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="e2e41-146"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2e41-146"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2e41-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2e41-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2e41-148">**Объект Метадатапиктуре**</span><span class="sxs-lookup"><span data-stu-id="e2e41-148">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
</dt> <dt>

[<span data-ttu-id="e2e41-149">**Объект Метадататекст**</span><span class="sxs-lookup"><span data-stu-id="e2e41-149">**MetadataText Object**</span></span>](metadatatext-object.md)
</dt> <dt>

[<span data-ttu-id="e2e41-150">**StringCollection. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="e2e41-150">**StringCollection.getItemInfo**</span></span>](stringcollection-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="e2e41-151">**Объект StringCollection**</span><span class="sxs-lookup"><span data-stu-id="e2e41-151">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





