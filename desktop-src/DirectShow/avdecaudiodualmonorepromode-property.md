---
description: Указывает, как декодер воспроизводит два моно аудио.
ms.assetid: 3ef1f52c-13b2-4d9f-99fe-3317846be8a0
title: Свойство Авдекаудиодуалмонорепромоде (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71ebe7e003b2dc4b6eebc30901525ffb918a9a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806461"
---
# <a name="avdecaudiodualmonorepromode-property"></a><span data-ttu-id="26755-103">Авдекаудиодуалмонорепромоде, свойство</span><span class="sxs-lookup"><span data-stu-id="26755-103">AVDecAudioDualMonoReproMode property</span></span>

<span data-ttu-id="26755-104">Указывает, как декодер воспроизводит два моно аудио.</span><span class="sxs-lookup"><span data-stu-id="26755-104">Specifies how the decoder reproduces dual mono audio.</span></span>

<span data-ttu-id="26755-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="26755-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="26755-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="26755-106">Data type</span></span>

<span data-ttu-id="26755-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="26755-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="26755-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="26755-108">Property GUID</span></span>

<span data-ttu-id="26755-109">**КОДЕКАПИ \_ авдекаудиодуалмонорепромоде**</span><span class="sxs-lookup"><span data-stu-id="26755-109">**CODECAPI\_AVDecAudioDualMonoReproMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="26755-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="26755-110">Property value</span></span>

<span data-ttu-id="26755-111">Значение этого свойства является членом перечисления [**еавдекаудиодуалмонорепромоде**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode) .</span><span class="sxs-lookup"><span data-stu-id="26755-111">The value of this property is a member of the [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="26755-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26755-112">Remarks</span></span>

<span data-ttu-id="26755-113">Эти свойства применяются только в том случае, если входной поток битов декодера содержит два моно аудио.</span><span class="sxs-lookup"><span data-stu-id="26755-113">This properties applies only when the decoder's input bit stream contains dual mono audio.</span></span> <span data-ttu-id="26755-114">Чтобы проверить это условие, получите значение свойства [авдекаудиодуалмоно](avdecaudiodualmono-property.md) .</span><span class="sxs-lookup"><span data-stu-id="26755-114">To test this condition, get the value of the [AVDecAudioDualMono](avdecaudiodualmono-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="26755-115">Требования</span><span class="sxs-lookup"><span data-stu-id="26755-115">Requirements</span></span>



| <span data-ttu-id="26755-116">Требование</span><span class="sxs-lookup"><span data-stu-id="26755-116">Requirement</span></span> | <span data-ttu-id="26755-117">Значение</span><span class="sxs-lookup"><span data-stu-id="26755-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26755-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26755-118">Minimum supported client</span></span><br/> | <span data-ttu-id="26755-119">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="26755-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="26755-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26755-120">Minimum supported server</span></span><br/> | <span data-ttu-id="26755-121">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="26755-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="26755-122">Header</span><span class="sxs-lookup"><span data-stu-id="26755-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="26755-123"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="26755-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26755-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26755-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26755-125">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="26755-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="26755-126">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="26755-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




