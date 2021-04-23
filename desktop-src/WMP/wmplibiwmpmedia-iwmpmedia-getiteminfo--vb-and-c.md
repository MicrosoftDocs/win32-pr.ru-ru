---
title: Ивмпмедиа getItemInfo, метод
description: Метод getItemInfo возвращает значение указанного атрибута для элемента мультимедиа.
ms.assetid: b95fa61d-a600-4f31-a930-d80516204034
keywords:
- getItemInfo метод Windows Media Player
- getItemInfo метод проигрывателя Windows Media Player, интерфейс Ивмпмедиа
- Интерфейс Ивмпмедиа Windows Media Player, метод getItemInfo
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 523e57e68d13df55395cd4deca6e09904723bbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669258"
---
# <a name="iwmpmediagetiteminfo-method"></a><span data-ttu-id="71ca8-106">Метод Ивмпмедиа:: getItemInfo</span><span class="sxs-lookup"><span data-stu-id="71ca8-106">IWMPMedia::getItemInfo method</span></span>

<span data-ttu-id="71ca8-107">Метод **getItemInfo** возвращает значение указанного атрибута для элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="71ca8-107">The **getItemInfo** method returns the value of the specified attribute for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="71ca8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71ca8-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPMedia.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="71ca8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="71ca8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71ca8-110">*бстритемнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="71ca8-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71ca8-111">**Строка System. String** , которая является именем атрибута.</span><span class="sxs-lookup"><span data-stu-id="71ca8-111">A **System.String** that is the name of the attribute.</span></span> <span data-ttu-id="71ca8-112">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="71ca8-112">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71ca8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71ca8-113">Return value</span></span>

<span data-ttu-id="71ca8-114">**Строка System. String** , которая является значением указанного атрибута.</span><span class="sxs-lookup"><span data-stu-id="71ca8-114">A **System.String** that is the value of the specified attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="71ca8-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71ca8-115">Remarks</span></span>

<span data-ttu-id="71ca8-116">Этот метод возвращает метаданные для отдельного элемента мультимедиа или элемента мультимедиа, который является частью списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="71ca8-116">This method returns the metadata for an individual media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="71ca8-117">Свойство **аттрибутекаунт** возвращает количество имен атрибутов, доступных для данного элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="71ca8-117">The **attributeCount** property gets the number of attribute names available for a given media item.</span></span> <span data-ttu-id="71ca8-118">Номера индексов можно использовать с методом **жетаттрибутенаме** для определения имени каждого доступного атрибута.</span><span class="sxs-lookup"><span data-stu-id="71ca8-118">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="71ca8-119">Имена отдельных атрибутов можно передать в **getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="71ca8-119">Individual attribute names can be passed to **getItemInfo**.</span></span>

<span data-ttu-id="71ca8-120">Чтобы получить атрибуты с несколькими значениями и атрибутами со сложными значениями, используйте метод **жетитеминфобитипе** .</span><span class="sxs-lookup"><span data-stu-id="71ca8-120">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="71ca8-121">Если элемент мультимедиа получен из библиотеки, полученной путем вызова [ивмплибрари. медиаколлектион](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), набор доступных атрибутов будет отличаться от тех, которые можно запрашивать из локальной библиотеки, полученной путем вызова [аксвиндовсмедиаплайер. медиаколлектион](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="71ca8-121">If the media item came from a library that was retrieved by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), the set of available attributes will differ from those which can be queried from the local library retrieved by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span></span> <span data-ttu-id="71ca8-122">Например, атрибуты, доступные из локальной библиотеки, извлеченной с помощью **ивмплибрари** , будут подмножеством атрибутов, доступных из локальной библиотеки, полученной с помощью **ивмпкоре**.</span><span class="sxs-lookup"><span data-stu-id="71ca8-122">For example, the attributes available from the local library retrieved by using **IWMPLibrary** will be a subset of the attributes available from the local library retrieved by using **IWMPCore**.</span></span> <span data-ttu-id="71ca8-123">Набор атрибутов, доступных из других источников (удаленных библиотек, переносных устройств или компакт-дисков), определяется другими источниками.</span><span class="sxs-lookup"><span data-stu-id="71ca8-123">The set of attributes available from other sources (remote libraries, portable devices, or CDs) is defined by the other sources.</span></span>

<span data-ttu-id="71ca8-124">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="71ca8-124">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="71ca8-125">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="71ca8-125">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71ca8-126">Требования</span><span class="sxs-lookup"><span data-stu-id="71ca8-126">Requirements</span></span>



| <span data-ttu-id="71ca8-127">Требование</span><span class="sxs-lookup"><span data-stu-id="71ca8-127">Requirement</span></span> | <span data-ttu-id="71ca8-128">Значение</span><span class="sxs-lookup"><span data-stu-id="71ca8-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71ca8-129">Версия</span><span class="sxs-lookup"><span data-stu-id="71ca8-129">Version</span></span><br/>   | <span data-ttu-id="71ca8-130">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="71ca8-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="71ca8-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="71ca8-131">Namespace</span></span><br/> | <span data-ttu-id="71ca8-132">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="71ca8-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="71ca8-133">Сборка</span><span class="sxs-lookup"><span data-stu-id="71ca8-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="71ca8-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="71ca8-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71ca8-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71ca8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71ca8-136">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="71ca8-136">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="71ca8-137">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="71ca8-137">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="71ca8-138">**Ивмпмедиа. Аттрибутекаунт (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="71ca8-138">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="71ca8-139">**Ивмпмедиа. Жетаттрибутенаме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="71ca8-139">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="71ca8-140">**Ивмпмедиа. Сетитеминфо (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="71ca8-140">**IWMPMedia.setItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="71ca8-141">**IWMPMedia3. Жетитеминфобитипе (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="71ca8-141">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





