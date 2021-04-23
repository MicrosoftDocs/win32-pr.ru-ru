---
description: Заставляет кодировщик кодировать следующий кадр как ключевой кадр.
ms.assetid: 1E252967-6C28-4DA3-9E64-BD276E475753
title: Свойство CODECAPI_AVEncVideoForceKeyFrame (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72c555d5680e822e9a8308b3e143a754eb22b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701329"
---
# <a name="codecapi_avencvideoforcekeyframe-property"></a><span data-ttu-id="d1cce-103">КОДЕКАПИ \_ авенквидеофорцекэйфраме, свойство</span><span class="sxs-lookup"><span data-stu-id="d1cce-103">CODECAPI\_AVEncVideoForceKeyFrame property</span></span>

<span data-ttu-id="d1cce-104">Заставляет кодировщик кодировать следующий кадр как ключевой кадр.</span><span class="sxs-lookup"><span data-stu-id="d1cce-104">Forces the encoder to code the next frame as a key frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="d1cce-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d1cce-105">Data type</span></span>

<span data-ttu-id="d1cce-106">**Ulong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="d1cce-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d1cce-107">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="d1cce-107">Property GUID</span></span>

<span data-ttu-id="d1cce-108">**КОДЕКАПИ \_ авенквидеофорцекэйфраме**</span><span class="sxs-lookup"><span data-stu-id="d1cce-108">**CODECAPI\_AVEncVideoForceKeyFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="d1cce-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d1cce-109">Property value</span></span>

<span data-ttu-id="d1cce-110">Если значение не равно нулю, кодировщик будет кодировать следующий кадр в качестве ключевого кадра.</span><span class="sxs-lookup"><span data-stu-id="d1cce-110">If the value is nonzero, the encoder will code the next frame as a key frame.</span></span> <span data-ttu-id="d1cce-111">Если значение равно нулю, кодировщик выбирает, следует ли кодировать следующий кадр как ключевой кадр.</span><span class="sxs-lookup"><span data-stu-id="d1cce-111">If the value is zero, the encoder selects whether to encode the next frame as a key frame.</span></span>

<span data-ttu-id="d1cce-112">Это свойство применяется к следующему кадру, который кодировщик получает в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="d1cce-112">This property applies to the next frame that the encoder receives as input.</span></span> <span data-ttu-id="d1cce-113">Для Media Foundation преобразования (MFT) это следующий кадр, который передается методу [**имфтрансформ::P роцессинпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) .</span><span class="sxs-lookup"><span data-stu-id="d1cce-113">For a Media Foundation transform (MFT), this is the next frame that is passed to the [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method.</span></span> <span data-ttu-id="d1cce-114">Параметр сбрасывается в ноль после следующего кадра.</span><span class="sxs-lookup"><span data-stu-id="d1cce-114">The setting resets to zero after the next frame.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1cce-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1cce-115">Remarks</span></span>

<span data-ttu-id="d1cce-116">Это свойство также используется с [кодировщиками камер H. 264 увк 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="d1cce-116">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1cce-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d1cce-117">Requirements</span></span>



| <span data-ttu-id="d1cce-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d1cce-118">Requirement</span></span> | <span data-ttu-id="d1cce-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d1cce-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1cce-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1cce-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d1cce-121">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="d1cce-121">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="d1cce-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1cce-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d1cce-123">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="d1cce-123">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d1cce-124">Header</span><span class="sxs-lookup"><span data-stu-id="d1cce-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1cce-125"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1cce-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1cce-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1cce-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1cce-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d1cce-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d1cce-128">**икодекапи**</span><span class="sxs-lookup"><span data-stu-id="d1cce-128">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

