---
description: Указывает, кодируется ли двухканальный аудио-канал как стерео или два Mono.
ms.assetid: 37f25590-69c2-43bd-a5d4-2262457cb39d
title: Свойство Авенкаудиодуалмоно (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0a5b684638133a1449fc849348cdfd8627533fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105662053"
---
# <a name="avencaudiodualmono-property"></a><span data-ttu-id="edb89-103">Авенкаудиодуалмоно, свойство</span><span class="sxs-lookup"><span data-stu-id="edb89-103">AVEncAudioDualMono property</span></span>

<span data-ttu-id="edb89-104">Указывает, кодируется ли двухканальный аудио-канал как стерео или два Mono.</span><span class="sxs-lookup"><span data-stu-id="edb89-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="edb89-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="edb89-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="edb89-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="edb89-106">Data type</span></span>

<span data-ttu-id="edb89-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="edb89-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="edb89-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="edb89-108">Property GUID</span></span>

<span data-ttu-id="edb89-109">**КОДЕКАПИ \_ авенкаудиодуалмоно**</span><span class="sxs-lookup"><span data-stu-id="edb89-109">**CODECAPI\_AVEncAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="edb89-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="edb89-110">Property value</span></span>

<span data-ttu-id="edb89-111">Значение этого свойства является членом перечисления [**еавенкаудиодуалмоно**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) .</span><span class="sxs-lookup"><span data-stu-id="edb89-111">The value of this property is a member of the [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="edb89-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="edb89-112">Remarks</span></span>

<span data-ttu-id="edb89-113">Это свойство не применяется к кодировщикам аудио в формате MPEG.</span><span class="sxs-lookup"><span data-stu-id="edb89-113">This property does not apply to MPEG audio encoders.</span></span> <span data-ttu-id="edb89-114">Для звука MPEG используйте свойство [**авенкмпакодингмоде**](avencmpacodingmode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="edb89-114">For MPEG audio, use the [**AVEncMPACodingMode**](avencmpacodingmode-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="edb89-115">Требования</span><span class="sxs-lookup"><span data-stu-id="edb89-115">Requirements</span></span>



| <span data-ttu-id="edb89-116">Требование</span><span class="sxs-lookup"><span data-stu-id="edb89-116">Requirement</span></span> | <span data-ttu-id="edb89-117">Значение</span><span class="sxs-lookup"><span data-stu-id="edb89-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="edb89-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="edb89-118">Minimum supported client</span></span><br/> | <span data-ttu-id="edb89-119">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="edb89-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="edb89-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="edb89-120">Minimum supported server</span></span><br/> | <span data-ttu-id="edb89-121">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="edb89-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="edb89-122">Header</span><span class="sxs-lookup"><span data-stu-id="edb89-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="edb89-123"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="edb89-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edb89-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="edb89-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edb89-125">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="edb89-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="edb89-126">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="edb89-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

