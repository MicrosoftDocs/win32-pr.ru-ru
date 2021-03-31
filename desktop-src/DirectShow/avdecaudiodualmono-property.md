---
description: Указывает, кодируется ли двухканальный аудио-канал как стерео или два Mono.
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: Свойство Авдекаудиодуалмоно (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 107adb00eb68cbb9ec19331b0c0f3f9db916a306
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894978"
---
# <a name="avdecaudiodualmono-property"></a><span data-ttu-id="6bee7-103">Авдекаудиодуалмоно, свойство</span><span class="sxs-lookup"><span data-stu-id="6bee7-103">AVDecAudioDualMono property</span></span>

<span data-ttu-id="6bee7-104">Указывает, кодируется ли двухканальный аудио-канал как стерео или два Mono.</span><span class="sxs-lookup"><span data-stu-id="6bee7-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="6bee7-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6bee7-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="6bee7-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6bee7-106">Data type</span></span>

<span data-ttu-id="6bee7-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="6bee7-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="6bee7-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="6bee7-108">Property GUID</span></span>

<span data-ttu-id="6bee7-109">**КОДЕКАПИ \_ авдекаудиодуалмоно**</span><span class="sxs-lookup"><span data-stu-id="6bee7-109">**CODECAPI\_AVDecAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="6bee7-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6bee7-110">Property value</span></span>

<span data-ttu-id="6bee7-111">Значение этого свойства является членом перечисления [**еавдекаудиодуалмоно**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) .</span><span class="sxs-lookup"><span data-stu-id="6bee7-111">The value of this property is a member of the [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bee7-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6bee7-112">Remarks</span></span>

<span data-ttu-id="6bee7-113">Это свойство применяется только в том случае, если входной поток битов декодера содержит Двухканальный звук.</span><span class="sxs-lookup"><span data-stu-id="6bee7-113">This property applies only when the decoder's input bit stream contains two-channel audio.</span></span> <span data-ttu-id="6bee7-114">Двухканальный аудиопоток может быть закодирован как стерео или как двойной Моно.</span><span class="sxs-lookup"><span data-stu-id="6bee7-114">A two-channel audio stream might be encoded as stereo or as dual mono.</span></span> <span data-ttu-id="6bee7-115">Если звук является двойным моно, можно задать свойство [**авдекаудиодуалмонорепромоде**](avdecaudiodualmonorepromode-property.md) , чтобы настроить способ воспроизведения звука декодером.</span><span class="sxs-lookup"><span data-stu-id="6bee7-115">If the audio is dual mono, you can set the [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) property to configure how the decoder reproduces the audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bee7-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6bee7-116">Requirements</span></span>



| <span data-ttu-id="6bee7-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6bee7-117">Requirement</span></span> | <span data-ttu-id="6bee7-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6bee7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6bee7-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6bee7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6bee7-120">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6bee7-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="6bee7-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6bee7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6bee7-122">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="6bee7-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="6bee7-123">Header</span><span class="sxs-lookup"><span data-stu-id="6bee7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bee7-124"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bee7-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bee7-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6bee7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bee7-126">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="6bee7-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="6bee7-127">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="6bee7-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




