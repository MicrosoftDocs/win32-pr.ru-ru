---
title: Ивмпплайлист insertItem, метод
description: Метод insertItem вставляет элемент мультимедиа в указанном месте в списке воспроизведения.
ms.assetid: 6e472f0a-13df-41d9-8e6f-8430d87fe978
keywords:
- insertItem метод Windows Media Player
- insertItem метод проигрывателя Windows Media Player, интерфейс Ивмпплайлист
- Интерфейс Ивмпплайлист Windows Media Player, метод insertItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.insertItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ef167a5f3931f34d4cd6fb91b3d044affb9484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708400"
---
# <a name="iwmpplaylistinsertitem-method"></a><span data-ttu-id="8ba8c-106">Метод Ивмпплайлист:: insertItem</span><span class="sxs-lookup"><span data-stu-id="8ba8c-106">IWMPPlaylist::insertItem method</span></span>

<span data-ttu-id="8ba8c-107">Метод **insertItem** вставляет элемент мультимедиа в указанном месте в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="8ba8c-107">The **insertItem** method inserts a media item at a specified location in a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ba8c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ba8c-108">Syntax</span></span>


```CSharp
public void insertItem(
  System.Int32 lIndex,
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub insertItem( _
  ByVal lIndex As System.Int32, _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.insertItem
```





## <a name="parameters"></a><span data-ttu-id="8ba8c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ba8c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ba8c-110">*Линдекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8ba8c-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba8c-111">Значение **System. Int32** , представляющее собой отсчитываемый от нуля индекс, по которому элемент мультимедиа будет вставлен в список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="8ba8c-111">A **System.Int32** that is the zero-based index at which the media item will be inserted in the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="8ba8c-112">*пивмпмедиа* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8ba8c-112">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba8c-113">Интерфейс **вмплиб. ивмпмедиа** , представляющий вставляемый элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8ba8c-113">A **WMPLib.IWMPMedia** interface that represents the media item to be inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ba8c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ba8c-114">Return value</span></span>

<span data-ttu-id="8ba8c-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8ba8c-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ba8c-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ba8c-116">Remarks</span></span>

<span data-ttu-id="8ba8c-117">Индексы всех элементов мультимедиа после вставленного элемента будут увеличены на один.</span><span class="sxs-lookup"><span data-stu-id="8ba8c-117">All media items after the inserted item will have their indexes increased by one.</span></span>

<span data-ttu-id="8ba8c-118">Перед вызовом этого метода необходимо иметь полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="8ba8c-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="8ba8c-119">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="8ba8c-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ba8c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="8ba8c-120">Requirements</span></span>



| <span data-ttu-id="8ba8c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="8ba8c-121">Requirement</span></span> | <span data-ttu-id="8ba8c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="8ba8c-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba8c-123">Версия</span><span class="sxs-lookup"><span data-stu-id="8ba8c-123">Version</span></span><br/>   | <span data-ttu-id="8ba8c-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8ba8c-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="8ba8c-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8ba8c-125">Namespace</span></span><br/> | <span data-ttu-id="8ba8c-126">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="8ba8c-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8ba8c-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="8ba8c-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8ba8c-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8ba8c-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ba8c-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ba8c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ba8c-130">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="8ba8c-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8ba8c-131">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="8ba8c-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8ba8c-132">**Ивмпплайлист. removeItem (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="8ba8c-132">**IWMPPlaylist.removeItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> </dl>

 

 





