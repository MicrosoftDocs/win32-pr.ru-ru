---
title: IWMPMedia3 Жетитеминфобитипе, метод
description: Метод Жетитеминфобитипе возвращает значение атрибута, соответствующего указанному типу атрибута и индексу.
ms.assetid: e4cf14b4-3c59-485f-a573-734a0076647b
keywords:
- Жетитеминфобитипе метод Windows Media Player
- Жетитеминфобитипе метод проигрывателя Windows Media Player, интерфейс IWMPMedia3
- Интерфейс IWMPMedia3 Windows Media Player, метод Жетитеминфобитипе
topic_type:
- apiref
api_name:
- IWMPMedia3.getItemInfoByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f37992201d5d19397724071f8c2a4b8e851aac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665103"
---
# <a name="iwmpmedia3getiteminfobytype-method"></a><span data-ttu-id="3385a-106">Метод IWMPMedia3:: Жетитеминфобитипе</span><span class="sxs-lookup"><span data-stu-id="3385a-106">IWMPMedia3::getItemInfoByType method</span></span>

<span data-ttu-id="3385a-107">Метод **жетитеминфобитипе** возвращает значение атрибута, соответствующего указанному типу атрибута и индексу.</span><span class="sxs-lookup"><span data-stu-id="3385a-107">The **getItemInfoByType** method returns the value of the attribute corresponding to the specified attribute type and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="3385a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3385a-108">Syntax</span></span>


```CSharp
public System.Object getItemInfoByType(
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lIndex
);
```


```VB

Public Function getItemInfoByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lIndex As System.Int32 _
) As System.Object
Implements IWMPMedia3.getItemInfoByType
```





## <a name="parameters"></a><span data-ttu-id="3385a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3385a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3385a-110">*бстртипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3385a-110">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3385a-111">**Строка System. String** , которая является типом атрибута.</span><span class="sxs-lookup"><span data-stu-id="3385a-111">A **System.String** that is the attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="3385a-112">*бстрлангуаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3385a-112">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3385a-113">**Строка System. String** , которая является языком.</span><span class="sxs-lookup"><span data-stu-id="3385a-113">A **System.String** that is the language.</span></span> <span data-ttu-id="3385a-114">Если задано значение null или строка нулевой длины (""), используется текущая строка языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="3385a-114">If the value is set to null or a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="3385a-115">В противном случае значение должно быть допустимой строкой языка RFC 1766, например "en-US".</span><span class="sxs-lookup"><span data-stu-id="3385a-115">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="3385a-116">*Линдекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3385a-116">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3385a-117">Объект **System. Int32** , который является индексом атрибута.</span><span class="sxs-lookup"><span data-stu-id="3385a-117">A **System.Int32** that is the attribute index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3385a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3385a-118">Return value</span></span>

<span data-ttu-id="3385a-119">Объект **System. Object** , являющийся значением атрибута.</span><span class="sxs-lookup"><span data-stu-id="3385a-119">A **System.Object** that is the value of the attribute.</span></span> <span data-ttu-id="3385a-120">Тип для приведения этого объекта зависит от типа атрибута.</span><span class="sxs-lookup"><span data-stu-id="3385a-120">The type to cast this object to depends on the type of the attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="3385a-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3385a-121">Remarks</span></span>

<span data-ttu-id="3385a-122">Этот метод возвращает метаданные для отдельного элемента цифрового носителя или элемента мультимедиа, который является частью списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="3385a-122">This method returns the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="3385a-123">Этот метод поддерживает атрибуты с несколькими значениями и атрибутами со сложными значениями.</span><span class="sxs-lookup"><span data-stu-id="3385a-123">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="3385a-124">Метод **getItemInfo** не поддерживает атрибуты с несколькими значениями и атрибутами со сложными значениями.</span><span class="sxs-lookup"><span data-stu-id="3385a-124">The **getItemInfo** method does not support attributes with multiple values and attributes with complex values.</span></span>

<span data-ttu-id="3385a-125">Свойство **аттрибутекаунт** возвращает количество имен атрибутов, доступных для данного элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3385a-125">The **attributeCount** property gets the number of attribute names available for a given media item.</span></span> <span data-ttu-id="3385a-126">Номера индексов можно использовать с методом **жетаттрибутенаме** для определения имени каждого доступного атрибута.</span><span class="sxs-lookup"><span data-stu-id="3385a-126">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="3385a-127">Имена отдельных атрибутов можно передать в параметр *Name* объекта **жетитеминфобитипе**.</span><span class="sxs-lookup"><span data-stu-id="3385a-127">Individual attribute names can be passed to the *name* parameter of **getItemInfoByType**.</span></span>

<span data-ttu-id="3385a-128">Метод **жетаттрибутекаунтбитипе** возвращает количество атрибутов, соответствующих определенному имени атрибута для данного элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3385a-128">The **getAttributeCountByType** method returns the number of attributes that correspond to a particular attribute name for a given media item.</span></span> <span data-ttu-id="3385a-129">Номера индексов можно передать в параметр *index* объекта **жетитеминфобитипе**.</span><span class="sxs-lookup"><span data-stu-id="3385a-129">Index numbers can then be passed to the *index* parameter of **getItemInfoByType**.</span></span> <span data-ttu-id="3385a-130">Это полезно, например, если элемент мультимедиа был отнесен к нескольким жанрам.</span><span class="sxs-lookup"><span data-stu-id="3385a-130">This is useful when a media item has been categorized under multiple genres, for example.</span></span>

<span data-ttu-id="3385a-131">Если элемент мультимедиа получен из библиотеки, полученной путем вызова [ивмплибрари. медиаколлектион](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), набор доступных атрибутов будет отличаться от тех, которые можно запрашивать из локальной библиотеки, полученной путем вызова [аксвиндовсмедиаплайер. медиаколлектион](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="3385a-131">If the media item came from a library that was retrieved by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), the set of available attributes will differ from those which can be queried from the local library retrieved by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span></span> <span data-ttu-id="3385a-132">Например, атрибуты, доступные из локальной библиотеки, извлеченной с помощью **ивмплибрари** , будут подмножеством атрибутов, доступных из локальной библиотеки, полученной с помощью **аксвиндовсмедиаплайер**.</span><span class="sxs-lookup"><span data-stu-id="3385a-132">For example, the attributes available from the local library retrieved by using **IWMPLibrary** will be a subset of the attributes available from the local library retrieved by using **AxWindowsMediaPlayer**.</span></span> <span data-ttu-id="3385a-133">Набор атрибутов, доступных из других источников (удаленные библиотеки, переносные устройства или компакт-диски, определяется другими источниками.</span><span class="sxs-lookup"><span data-stu-id="3385a-133">The set of attributes available from other sources (remote libraries, portable devices, or CDs is defined by the other sources.</span></span>

<span data-ttu-id="3385a-134">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="3385a-134">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="3385a-135">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3385a-135">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3385a-136">Требования</span><span class="sxs-lookup"><span data-stu-id="3385a-136">Requirements</span></span>



| <span data-ttu-id="3385a-137">Требование</span><span class="sxs-lookup"><span data-stu-id="3385a-137">Requirement</span></span> | <span data-ttu-id="3385a-138">Значение</span><span class="sxs-lookup"><span data-stu-id="3385a-138">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3385a-139">Версия</span><span class="sxs-lookup"><span data-stu-id="3385a-139">Version</span></span><br/>   | <span data-ttu-id="3385a-140">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="3385a-140">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3385a-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3385a-141">Namespace</span></span><br/> | <span data-ttu-id="3385a-142">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="3385a-142">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3385a-143">Сборка</span><span class="sxs-lookup"><span data-stu-id="3385a-143">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3385a-144"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3385a-144"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3385a-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3385a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3385a-146">**Интерфейс IWMPMedia3 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3385a-146">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3385a-147">**Ивмпмедиа. Аттрибутекаунт (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3385a-147">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3385a-148">**Ивмпмедиа. Жетаттрибутенаме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3385a-148">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3385a-149">**Ивмпмедиа. getItemInfo (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3385a-149">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3385a-150">**IWMPMedia3. Жетаттрибутекаунтбитипе (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3385a-150">**IWMPMedia3.getAttributeCountByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md)
</dt> </dl>

 

 





