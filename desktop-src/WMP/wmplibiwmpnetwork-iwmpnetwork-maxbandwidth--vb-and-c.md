---
title: Ивмпнетворк maxBandwidth, свойство
description: Свойство maxBandwidth Возвращает или задает максимально допустимую пропускную способность.
ms.assetid: ff7548d8-b80f-4cb4-bdd6-86d585fef329
keywords:
- Проигрыватель Windows Media для свойства maxBandwidth
- maxBandwidth свойство проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, свойство maxBandwidth
topic_type:
- apiref
api_name:
- IWMPNetwork.maxBandwidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3620d609db0f1786da673923f54d726b3c99994a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648851"
---
# <a name="iwmpnetworkmaxbandwidth-property"></a><span data-ttu-id="fb3e9-106">Свойство Ивмпнетворк:: maxBandwidth</span><span class="sxs-lookup"><span data-stu-id="fb3e9-106">IWMPNetwork::maxBandwidth property</span></span>

<span data-ttu-id="fb3e9-107">Свойство **maxBandwidth** Возвращает или задает максимально допустимую пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="fb3e9-107">The **maxBandwidth** property gets or sets the maximum allowed bandwidth.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb3e9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb3e9-108">Syntax</span></span>


```CSharp
public System.Int32 maxBandwidth {get; set;}
```


```VB

Public Property maxBandwidth As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="fb3e9-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fb3e9-109">Property value</span></span>

<span data-ttu-id="fb3e9-110">Значение **System. Int32** , которое является максимальной пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="fb3e9-110">A **System.Int32** that is the maximum bandwidth.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb3e9-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fb3e9-111">Remarks</span></span>

<span data-ttu-id="fb3e9-112">Это свойство не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fb3e9-112">This property does not have a default value.</span></span> <span data-ttu-id="fb3e9-113">Это значение можно указать во время воспроизведения проигрывателя Windows Media, но изменение вступит в силу только после освобождения текущего элемента мультимедиа, открыв другой элемент или вызвав **аксвиндовсмедиаплайер. Close**.</span><span class="sxs-lookup"><span data-stu-id="fb3e9-113">The value can be specified while Windows Media Player is playing, but the change will not take effect until the current media item is released by opening another one or by calling **AxWindowsMediaPlayer.close**.</span></span> <span data-ttu-id="fb3e9-114">Проигрыватель Windows Media пытается добиться максимально возможной пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="fb3e9-114">Windows Media Player attempts to achieve the highest bandwidth possible.</span></span> <span data-ttu-id="fb3e9-115">Если это значение не задано, то появление пропускной способности не преднамерено.</span><span class="sxs-lookup"><span data-stu-id="fb3e9-115">No intentional reduction of bandwidth will occur unless this value is set.</span></span>

<span data-ttu-id="fb3e9-116">Этот параметр полезен для уменьшения объема используемой пропускной способности, особенно в случае потока с несколькими скоростями (MBR).</span><span class="sxs-lookup"><span data-stu-id="fb3e9-116">This setting is useful for reducing the amount of bandwidth used, particularly in the case of a multiple bit rate (MBR) stream.</span></span> <span data-ttu-id="fb3e9-117">Поток MBR содержит несколько потоков с разной скоростью.</span><span class="sxs-lookup"><span data-stu-id="fb3e9-117">An MBR stream contains multiple streams with different bit rates.</span></span> <span data-ttu-id="fb3e9-118">В некоторых случаях может быть желательно использовать поток с более низкой скоростью, чем требуется клиенту.</span><span class="sxs-lookup"><span data-stu-id="fb3e9-118">In some cases, it may be desirable to use a stream with a lower bit rate than the client requires.</span></span> <span data-ttu-id="fb3e9-119">В этом случае при указании более низкого бита с помощью свойства **ивмпнетворк. maxBandwidth** выбирается поток с более низким битом.</span><span class="sxs-lookup"><span data-stu-id="fb3e9-119">In this case, specifying a lower bit rate with the **IWMPNetwork.maxBandwidth** property will select a lower bit-rate stream.</span></span> <span data-ttu-id="fb3e9-120">Например, поток MBR может включать потоки в кодировке 20 килобит в секунду (кбит/с), 37 кбит/с и 200 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="fb3e9-120">For example, an MBR stream might include streams encoded at 20 kilobits per second (Kbps), 37 Kbps, and 200 Kbps.</span></span> <span data-ttu-id="fb3e9-121">Использование **ивмпнетворк. maxBandwidth** для указания скорости 50 000 (50 кбит/с) выберет поток 37 кбит/с, а не поток 200 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="fb3e9-121">Using **IWMPNetwork.maxBandwidth** to specify a bit rate of 50,000 (50 Kbps) will select the 37 Kbps stream instead of the 200 Kbps stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb3e9-122">Требования</span><span class="sxs-lookup"><span data-stu-id="fb3e9-122">Requirements</span></span>



| <span data-ttu-id="fb3e9-123">Требование</span><span class="sxs-lookup"><span data-stu-id="fb3e9-123">Requirement</span></span> | <span data-ttu-id="fb3e9-124">Значение</span><span class="sxs-lookup"><span data-stu-id="fb3e9-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb3e9-125">Версия</span><span class="sxs-lookup"><span data-stu-id="fb3e9-125">Version</span></span><br/>   | <span data-ttu-id="fb3e9-126">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="fb3e9-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="fb3e9-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fb3e9-127">Namespace</span></span><br/> | <span data-ttu-id="fb3e9-128">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="fb3e9-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fb3e9-129">Сборка</span><span class="sxs-lookup"><span data-stu-id="fb3e9-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fb3e9-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fb3e9-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb3e9-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb3e9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb3e9-132">**Аксвиндовсмедиаплайер. Close (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="fb3e9-132">**AxWindowsMediaPlayer.close (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[<span data-ttu-id="fb3e9-133">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="fb3e9-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





