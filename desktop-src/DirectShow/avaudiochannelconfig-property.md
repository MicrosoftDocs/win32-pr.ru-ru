---
description: Возвращает конфигурацию динамика для каналов звука в потоке звукового бита.
ms.assetid: ec13bb55-47af-4d79-9560-d297bce8e236
title: Свойство Аваудиочаннелконфиг (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ee1bc7897d92f7efa1b6d351d2f73c32867529
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072204"
---
# <a name="avaudiochannelconfig-property"></a><span data-ttu-id="260c0-103">Аваудиочаннелконфиг, свойство</span><span class="sxs-lookup"><span data-stu-id="260c0-103">AVAudioChannelConfig property</span></span>

<span data-ttu-id="260c0-104">Возвращает конфигурацию динамика для каналов звука в потоке звукового бита.</span><span class="sxs-lookup"><span data-stu-id="260c0-104">Gets the speaker configuration for the audio channels in the audio bit stream.</span></span>

<span data-ttu-id="260c0-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="260c0-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="260c0-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="260c0-106">Data type</span></span>

<span data-ttu-id="260c0-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="260c0-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="260c0-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="260c0-108">Property GUID</span></span>

<span data-ttu-id="260c0-109">**КОДЕКАПИ \_ аваудиочаннелконфиг**</span><span class="sxs-lookup"><span data-stu-id="260c0-109">**CODECAPI\_AVAudioChannelConfig**</span></span>

## <a name="property-value"></a><span data-ttu-id="260c0-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="260c0-110">Property value</span></span>

<span data-ttu-id="260c0-111">Значение этого свойства является побитовым или для элементов перечисления [**еаваудиочаннелконфиг**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig) .</span><span class="sxs-lookup"><span data-stu-id="260c0-111">The value of this property is a bitwise OR of members of the [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="260c0-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="260c0-112">Remarks</span></span>

<span data-ttu-id="260c0-113">Число каналов включает канал с низкой частотой (НИЗКОЧАСТОТный), если он присутствует.</span><span class="sxs-lookup"><span data-stu-id="260c0-113">The number of channels includes the low frequency effect (LFE) channel, if present.</span></span>

## <a name="requirements"></a><span data-ttu-id="260c0-114">Требования</span><span class="sxs-lookup"><span data-stu-id="260c0-114">Requirements</span></span>



| <span data-ttu-id="260c0-115">Требование</span><span class="sxs-lookup"><span data-stu-id="260c0-115">Requirement</span></span> | <span data-ttu-id="260c0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="260c0-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="260c0-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="260c0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="260c0-118">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="260c0-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="260c0-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="260c0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="260c0-120">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="260c0-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="260c0-121">Header</span><span class="sxs-lookup"><span data-stu-id="260c0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="260c0-122"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="260c0-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="260c0-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="260c0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="260c0-124">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="260c0-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="260c0-125">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="260c0-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




