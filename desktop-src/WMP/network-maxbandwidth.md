---
title: Network. maxBandwidth
description: Свойство maxBandwidth указывает или получает максимально допустимую пропускную способность.
ms.assetid: 303acf51-8d3a-4e58-8aa8-c0b6db1e4fbb
keywords:
- Проигрыватель Windows Media Network. maxBandwidth
topic_type:
- apiref
api_name:
- Network.maxBandwidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbe8283c4cc756a4f88fad1240df3a757b53a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647928"
---
# <a name="networkmaxbandwidth"></a><span data-ttu-id="08339-104">Network. maxBandwidth</span><span class="sxs-lookup"><span data-stu-id="08339-104">Network.maxBandwidth</span></span>

<span data-ttu-id="08339-105">Свойство **maxBandwidth** указывает или получает максимально допустимую пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="08339-105">The **maxBandwidth** property specifies or retrieves the maximum allowed bandwidth.</span></span>

## <a name="syntax"></a><span data-ttu-id="08339-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08339-106">Syntax</span></span>

<span data-ttu-id="08339-107">*проигрыватель*. *сеть*. **maxBandwidth**</span><span class="sxs-lookup"><span data-stu-id="08339-107">*player*.*network*.**maxBandwidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="08339-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="08339-108">Possible Values</span></span>

<span data-ttu-id="08339-109">Это свойство имеет **номер** для чтения и записи (**Long**).</span><span class="sxs-lookup"><span data-stu-id="08339-109">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="08339-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08339-110">Remarks</span></span>

<span data-ttu-id="08339-111">Это свойство не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="08339-111">This property has no default value.</span></span> <span data-ttu-id="08339-112">Его значение можно указать во время воспроизведения проигрывателя Windows Media, но изменение вступит в силу только после того, как текущий элемент мультимедиа освободится, открыв другой или вызвав *Player*. **закройте окно**.</span><span class="sxs-lookup"><span data-stu-id="08339-112">Its value can be specified while Windows Media Player is playing, but the change will not take effect until the current media item is released by opening another one or by calling *Player*.**close**.</span></span> <span data-ttu-id="08339-113">Проигрыватель Windows Media пытается добиться максимально возможной пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="08339-113">Windows Media Player attempts to achieve the highest bandwidth possible.</span></span> <span data-ttu-id="08339-114">Только в случае задания значения будет продолжено снижение пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="08339-114">Only in the case of the value being set will any bandwidth reduction occur.</span></span>

<span data-ttu-id="08339-115">Этот параметр полезен для уменьшения объема используемой пропускной способности, особенно в случае потока с несколькими скоростями (MBR).</span><span class="sxs-lookup"><span data-stu-id="08339-115">This setting is useful for reducing the amount of bandwidth used, particularly in the case of a multiple bit rate (MBR) stream.</span></span> <span data-ttu-id="08339-116">Поток MBR содержит несколько потоков с разной скоростью.</span><span class="sxs-lookup"><span data-stu-id="08339-116">An MBR stream contains multiple streams with different bit rates.</span></span> <span data-ttu-id="08339-117">В некоторых случаях может быть желательно использовать поток с более низкой скоростью, чем требуется клиенту.</span><span class="sxs-lookup"><span data-stu-id="08339-117">In some cases, it may be desirable to use a stream with a lower bit rate than the client requires.</span></span> <span data-ttu-id="08339-118">В этом случае при настройке свойства **maxBandwidth** будет выбран поток с более низким битом.</span><span class="sxs-lookup"><span data-stu-id="08339-118">In this case, setting the **maxBandwidth** property will select a lower bit-rate stream.</span></span>

<span data-ttu-id="08339-119">Например, поток MBR может включать потоки в кодировке 20 килобит в секунду (кбит/с), 37 кбит/с и 200 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="08339-119">For example, an MBR stream could include streams encoded at 20 kilobits per second (Kbps), 37 Kbps, and 200 Kbps.</span></span> <span data-ttu-id="08339-120">Если задать для свойства **maxBandwidth** значение 50 000 (50 кбит/с), вместо потока 200 кбит/с будет выбран поток 37 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="08339-120">Setting the **maxBandwidth** property to 50,000 (50 Kbps) will select the 37 Kbps stream instead of the 200 Kbps stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="08339-121">Требования</span><span class="sxs-lookup"><span data-stu-id="08339-121">Requirements</span></span>



| <span data-ttu-id="08339-122">Требование</span><span class="sxs-lookup"><span data-stu-id="08339-122">Requirement</span></span> | <span data-ttu-id="08339-123">Значение</span><span class="sxs-lookup"><span data-stu-id="08339-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="08339-124">Версия</span><span class="sxs-lookup"><span data-stu-id="08339-124">Version</span></span><br/> | <span data-ttu-id="08339-125">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="08339-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="08339-126">DLL</span><span class="sxs-lookup"><span data-stu-id="08339-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="08339-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08339-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08339-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08339-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08339-129">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="08339-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="08339-130">**Player. закрыть**</span><span class="sxs-lookup"><span data-stu-id="08339-130">**Player.close**</span></span>](player-close.md)
</dt> </dl>

 

 





