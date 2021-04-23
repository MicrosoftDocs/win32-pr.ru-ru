---
title: Ивмпмедиа Жетитеминфобятом, метод
description: Метод Жетитеминфобятом возвращает значение атрибута с указанным номером индекса.
ms.assetid: d9a4b737-add1-4bbd-8e03-e58f45d65a62
keywords:
- Жетитеминфобятом метод Windows Media Player
- Жетитеминфобятом метод проигрывателя Windows Media Player, интерфейс Ивмпмедиа
- Интерфейс Ивмпмедиа Windows Media Player, метод Жетитеминфобятом
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfoByAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb37243960360120fbfe508a39db31e37728ac39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669255"
---
# <a name="iwmpmediagetiteminfobyatom-method"></a><span data-ttu-id="9ae6d-106">Метод Ивмпмедиа:: Жетитеминфобятом</span><span class="sxs-lookup"><span data-stu-id="9ae6d-106">IWMPMedia::getItemInfoByAtom method</span></span>

<span data-ttu-id="9ae6d-107">Метод **жетитеминфобятом** возвращает значение атрибута с указанным номером индекса.</span><span class="sxs-lookup"><span data-stu-id="9ae6d-107">The **getItemInfoByAtom** method returns the value of the attribute with the specified index number.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ae6d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ae6d-108">Syntax</span></span>


```CSharp
public System.String getItemInfoByAtom(
  System.Int32 lAtom
);
```


```VB

Public Function getItemInfoByAtom( _
  ByVal lAtom As System.Int32 _
) As System.String
Implements IWMPMedia.getItemInfoByAtom
```





## <a name="parameters"></a><span data-ttu-id="9ae6d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ae6d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ae6d-110">*Латом* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9ae6d-110">*lAtom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ae6d-111">Объект **System. Int32** , указывающий индекс, в котором запрошенный атрибут находится в наборе доступных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="9ae6d-111">A **System.Int32** that specifies the index at which the requested attribute resides within the set of available attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ae6d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ae6d-112">Return value</span></span>

<span data-ttu-id="9ae6d-113">**Строка System. String** , которая является значением атрибута.</span><span class="sxs-lookup"><span data-stu-id="9ae6d-113">A **System.String** that is the value of the attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ae6d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ae6d-114">Remarks</span></span>

<span data-ttu-id="9ae6d-115">Этот метод можно использовать для получения метаданных для определенного элемента мультимедиа с помощью номера индекса атрибута.</span><span class="sxs-lookup"><span data-stu-id="9ae6d-115">This method can be used to retrieve metadata for a specific media item by using an attribute index number.</span></span> <span data-ttu-id="9ae6d-116">Свойство **аттрибутекаунт** можно использовать для определения количества атрибутов, доступных для элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9ae6d-116">The **attributeCount** property can be used to determine the number of attributes available for the media item.</span></span>

<span data-ttu-id="9ae6d-117">Метод **жетмедиаатом** интерфейса **ивмпмедиаколлектион** также можно использовать для получения индекса определенного атрибута.</span><span class="sxs-lookup"><span data-stu-id="9ae6d-117">The **getMediaAtom** method of the **IWMPMediaCollection** interface can also be used to retrieve the index of a particular attribute.</span></span> <span data-ttu-id="9ae6d-118">Этот метод, как правило, более эффективен, чем методы **getItemInfo** или **жетитеминфобитипе** при работе с большими списками воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="9ae6d-118">This technique is generally more efficient than the **getItemInfo** or **getItemInfoByType** methods when working with large playlists.</span></span>

<span data-ttu-id="9ae6d-119">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="9ae6d-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="9ae6d-120">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="9ae6d-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ae6d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="9ae6d-121">Requirements</span></span>



| <span data-ttu-id="9ae6d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="9ae6d-122">Requirement</span></span> | <span data-ttu-id="9ae6d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="9ae6d-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ae6d-124">Версия</span><span class="sxs-lookup"><span data-stu-id="9ae6d-124">Version</span></span><br/>   | <span data-ttu-id="9ae6d-125">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9ae6d-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9ae6d-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9ae6d-126">Namespace</span></span><br/> | <span data-ttu-id="9ae6d-127">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="9ae6d-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9ae6d-128">Сборка</span><span class="sxs-lookup"><span data-stu-id="9ae6d-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9ae6d-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9ae6d-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ae6d-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ae6d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ae6d-131">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9ae6d-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9ae6d-132">**Ивмпмедиа. Аттрибутекаунт (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9ae6d-132">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9ae6d-133">**Ивмпмедиа. getItemInfo (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9ae6d-133">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9ae6d-134">**Ивмпмедиа. Сетитеминфо (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9ae6d-134">**IWMPMedia.setItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9ae6d-135">**IWMPMedia3. Жетитеминфобитипе (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9ae6d-135">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9ae6d-136">**Ивмпмедиаколлектион. Жетмедиаатом (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9ae6d-136">**IWMPMediaCollection.getMediaAtom (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)
</dt> </dl>

 

 





