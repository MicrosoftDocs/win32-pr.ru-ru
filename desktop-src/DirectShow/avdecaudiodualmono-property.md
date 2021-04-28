---
description: Свойство Авдекаудиодуалмоно — указывает, кодируется ли двухканальный аудио-канал как стерео или два Mono.
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: Свойство Авдекаудиодуалмоно (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adc84e19d41840b358e3e79576152dbc8527e2bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096572"
---
# <a name="avdecaudiodualmono-property"></a><span data-ttu-id="93af6-103">Авдекаудиодуалмоно, свойство</span><span class="sxs-lookup"><span data-stu-id="93af6-103">AVDecAudioDualMono property</span></span>

<span data-ttu-id="93af6-104">Указывает, кодируется ли двухканальный аудио-канал как стерео или два Mono.</span><span class="sxs-lookup"><span data-stu-id="93af6-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="93af6-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="93af6-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="93af6-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="93af6-106">Data type</span></span>

<span data-ttu-id="93af6-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="93af6-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="93af6-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="93af6-108">Property GUID</span></span>

<span data-ttu-id="93af6-109">**КОДЕКАПИ \_ авдекаудиодуалмоно**</span><span class="sxs-lookup"><span data-stu-id="93af6-109">**CODECAPI\_AVDecAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="93af6-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="93af6-110">Property value</span></span>

<span data-ttu-id="93af6-111">Значение этого свойства является членом перечисления [**еавдекаудиодуалмоно**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) .</span><span class="sxs-lookup"><span data-stu-id="93af6-111">The value of this property is a member of the [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="93af6-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="93af6-112">Remarks</span></span>

<span data-ttu-id="93af6-113">Это свойство применяется только в том случае, если входной поток битов декодера содержит Двухканальный звук.</span><span class="sxs-lookup"><span data-stu-id="93af6-113">This property applies only when the decoder's input bit stream contains two-channel audio.</span></span> <span data-ttu-id="93af6-114">Двухканальный аудиопоток может быть закодирован как стерео или как двойной Моно.</span><span class="sxs-lookup"><span data-stu-id="93af6-114">A two-channel audio stream might be encoded as stereo or as dual mono.</span></span> <span data-ttu-id="93af6-115">Если звук является двойным моно, можно задать свойство [**авдекаудиодуалмонорепромоде**](avdecaudiodualmonorepromode-property.md) , чтобы настроить способ воспроизведения звука декодером.</span><span class="sxs-lookup"><span data-stu-id="93af6-115">If the audio is dual mono, you can set the [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) property to configure how the decoder reproduces the audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="93af6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="93af6-116">Requirements</span></span>



| <span data-ttu-id="93af6-117">Требование</span><span class="sxs-lookup"><span data-stu-id="93af6-117">Requirement</span></span> | <span data-ttu-id="93af6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="93af6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93af6-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93af6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="93af6-120">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="93af6-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="93af6-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93af6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="93af6-122">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="93af6-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="93af6-123">Header</span><span class="sxs-lookup"><span data-stu-id="93af6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="93af6-124"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="93af6-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93af6-125">См. также</span><span class="sxs-lookup"><span data-stu-id="93af6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93af6-126">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="93af6-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="93af6-127">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="93af6-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




