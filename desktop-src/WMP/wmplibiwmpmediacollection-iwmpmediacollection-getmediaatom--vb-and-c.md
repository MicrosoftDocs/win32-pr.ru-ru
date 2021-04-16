---
title: Ивмпмедиаколлектион Жетмедиаатом, метод
description: Метод Жетмедиаатом возвращает индекс указанного атрибута в наборе доступных атрибутов.
ms.assetid: 01e3d073-677b-4939-96d3-63ae96eaa25d
keywords:
- Жетмедиаатом метод Windows Media Player
- Жетмедиаатом метод проигрывателя Windows Media Player, интерфейс Ивмпмедиаколлектион
- Интерфейс Ивмпмедиаколлектион Windows Media Player, метод Жетмедиаатом
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getMediaAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08487cf60c351ff4f8e0741209655cb78c30c3f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699199"
---
# <a name="iwmpmediacollectiongetmediaatom-method"></a><span data-ttu-id="28304-106">Метод Ивмпмедиаколлектион:: Жетмедиаатом</span><span class="sxs-lookup"><span data-stu-id="28304-106">IWMPMediaCollection::getMediaAtom method</span></span>

<span data-ttu-id="28304-107">`getMediaAtom`Метод возвращает индекс указанного атрибута в наборе доступных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="28304-107">The `getMediaAtom` method returns the index of a specified attribute within the set of available attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="28304-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28304-108">Syntax</span></span>


```CSharp
public System.Int32 getMediaAtom(
  System.String bstrItemName
);
```


```VB

Public Function getMediaAtom( _
  ByVal bstrItemName As System.String _
) As System.Int32
Implements IWMPMediaCollection.getMediaAtom
```





## <a name="parameters"></a><span data-ttu-id="28304-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="28304-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28304-110">*бстритемнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28304-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28304-111">**Строка System. String** , представляющая собой имя элемента, для которого должен быть получен индекс.</span><span class="sxs-lookup"><span data-stu-id="28304-111">The **System.String** that is the name of the item for which the index should be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28304-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28304-112">Return value</span></span>

<span data-ttu-id="28304-113">Значение **System. Int32** , которое является индексом.</span><span class="sxs-lookup"><span data-stu-id="28304-113">The **System.Int32** that is the index.</span></span>

## <a name="remarks"></a><span data-ttu-id="28304-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28304-114">Remarks</span></span>

<span data-ttu-id="28304-115">Номер индекса, полученный с помощью этого метода, может быть передан в **ивмпмедиа. жетитеминфобятом** для доступа к значениям атрибута.</span><span class="sxs-lookup"><span data-stu-id="28304-115">The index number retrieved with this method can be passed to the **IWMPMedia.getItemInfoByAtom** to access attribute values.</span></span> <span data-ttu-id="28304-116">Эта методика обычно более эффективна при работе с большими списками воспроизведения, чем доступ к значению атрибута по имени с помощью **ивмпмедиа. getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="28304-116">This technique is generally more efficient when working with large playlists than accessing an attribute value by name through **IWMPMedia.getItemInfo**.</span></span>

<span data-ttu-id="28304-117">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="28304-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="28304-118">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="28304-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="28304-119">Требования</span><span class="sxs-lookup"><span data-stu-id="28304-119">Requirements</span></span>



| <span data-ttu-id="28304-120">Требование</span><span class="sxs-lookup"><span data-stu-id="28304-120">Requirement</span></span> | <span data-ttu-id="28304-121">Значение</span><span class="sxs-lookup"><span data-stu-id="28304-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28304-122">Версия</span><span class="sxs-lookup"><span data-stu-id="28304-122">Version</span></span><br/>   | <span data-ttu-id="28304-123">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="28304-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="28304-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="28304-124">Namespace</span></span><br/> | <span data-ttu-id="28304-125">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="28304-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="28304-126">Сборка</span><span class="sxs-lookup"><span data-stu-id="28304-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="28304-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="28304-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28304-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28304-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28304-129">**Ивмпмедиа. getItemInfo (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="28304-129">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="28304-130">**Ивмпмедиа. Жетитеминфобятом (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="28304-130">**IWMPMedia.getItemInfoByAtom (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="28304-131">**Интерфейс Ивмпмедиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="28304-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





