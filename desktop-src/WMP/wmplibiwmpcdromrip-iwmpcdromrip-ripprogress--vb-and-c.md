---
title: Ивмпкдромрип Риппрогресс, свойство
description: Свойство Риппрогресс получает сведения о ходе копирования компакт-диска в процентах завершения.
ms.assetid: 00d4f074-a16d-4c5f-930f-4411b90303f1
keywords:
- Проигрыватель Windows Media для свойства Риппрогресс
- Риппрогресс свойство проигрывателя Windows Media Player, интерфейс Ивмпкдромрип
- Интерфейс Ивмпкдромрип Windows Media Player, свойство Риппрогресс
topic_type:
- apiref
api_name:
- IWMPCdromRip.ripProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 113b9fc716698156aa4f7731a7b19888e0edf438
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717955"
---
# <a name="iwmpcdromripripprogress-property"></a><span data-ttu-id="f928b-106">Свойство Ивмпкдромрип:: Риппрогресс</span><span class="sxs-lookup"><span data-stu-id="f928b-106">IWMPCdromRip::ripProgress property</span></span>

<span data-ttu-id="f928b-107">Свойство **риппрогресс** получает сведения о ходе копирования компакт-диска в процентах завершения.</span><span class="sxs-lookup"><span data-stu-id="f928b-107">The **ripProgress** property gets the CD ripping progress as percent complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="f928b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f928b-108">Syntax</span></span>


```CSharp
public System.Int32 ripProgress {get; set;}
```


```VB

Public ReadOnly Property ripProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="f928b-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f928b-109">Property value</span></span>

<span data-ttu-id="f928b-110">Значение **System. Int32** , которое является значением хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="f928b-110">A **System.Int32** that is the progress value.</span></span> <span data-ttu-id="f928b-111">Значения хода выполнения находятся в диапазоне от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="f928b-111">Progress values range from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="f928b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f928b-112">Remarks</span></span>

<span data-ttu-id="f928b-113">Значение Progress представляет завершенный процент всего процесса копирования.</span><span class="sxs-lookup"><span data-stu-id="f928b-113">The progress value represents the completed percentage of the entire ripping process.</span></span> <span data-ttu-id="f928b-114">Чтобы определить ход выполнения определенной записи, используйте [ивмпмедиа. getItemInfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) с **риппрогресс** в качестве имени атрибута.</span><span class="sxs-lookup"><span data-stu-id="f928b-114">To determine the progress of a specific track, use [IWMPMedia.getItemInfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) with **RipProgress** as the attribute name.</span></span> <span data-ttu-id="f928b-115">Чтобы получить индекс дорожки, скопированной в данный момент, вызовите Ивмпплайлист. getItemInfo с именем атрибута "Куррентриптраккиндекс".</span><span class="sxs-lookup"><span data-stu-id="f928b-115">To get the index of the track currently being ripped, call IWMPPlaylist.getItemInfo with "CurrentRipTrackIndex" as the attribute name.</span></span>

## <a name="requirements"></a><span data-ttu-id="f928b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f928b-116">Requirements</span></span>



| <span data-ttu-id="f928b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f928b-117">Requirement</span></span> | <span data-ttu-id="f928b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f928b-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f928b-119">Версия</span><span class="sxs-lookup"><span data-stu-id="f928b-119">Version</span></span><br/>   | <span data-ttu-id="f928b-120">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="f928b-120">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="f928b-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f928b-121">Namespace</span></span><br/> | <span data-ttu-id="f928b-122">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="f928b-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f928b-123">Сборка</span><span class="sxs-lookup"><span data-stu-id="f928b-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f928b-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f928b-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f928b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f928b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f928b-126">**Интерфейс Ивмпкдромрип (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f928b-126">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f928b-127">**Копирование компакт-диска**</span><span class="sxs-lookup"><span data-stu-id="f928b-127">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> </dl>

 

 





