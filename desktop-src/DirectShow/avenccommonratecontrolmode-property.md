---
description: Задает режим управления скоростью.
ms.assetid: 4a0d49b1-30da-4ebe-abff-3fceef6dd94a
title: Свойство Авенккоммонратеконтролмоде (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d18d0d7cb68936326fb4c4ba08188e362fdc91d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262464"
---
# <a name="avenccommonratecontrolmode-property"></a><span data-ttu-id="04ef7-103">Авенккоммонратеконтролмоде, свойство</span><span class="sxs-lookup"><span data-stu-id="04ef7-103">AVEncCommonRateControlMode property</span></span>

<span data-ttu-id="04ef7-104">Задает режим управления скоростью.</span><span class="sxs-lookup"><span data-stu-id="04ef7-104">Specifies the rate control mode.</span></span>

<span data-ttu-id="04ef7-105">Приложения могут задать это свойство, чтобы задать режим управления скоростью.</span><span class="sxs-lookup"><span data-stu-id="04ef7-105">Applications can set this property to specify the rate control mode.</span></span> <span data-ttu-id="04ef7-106">Кодировщики также могут возвращать это свойство как возможность.</span><span class="sxs-lookup"><span data-stu-id="04ef7-106">Encoders can also return this property as a capability.</span></span>

<span data-ttu-id="04ef7-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="04ef7-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="04ef7-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="04ef7-108">Data type</span></span>

<span data-ttu-id="04ef7-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="04ef7-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="04ef7-110">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="04ef7-110">Property GUID</span></span>

<span data-ttu-id="04ef7-111">**КОДЕКАПИ \_ авенккоммонратеконтролмоде**</span><span class="sxs-lookup"><span data-stu-id="04ef7-111">**CODECAPI\_AVEncCommonRateControlMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="04ef7-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="04ef7-112">Property value</span></span>

<span data-ttu-id="04ef7-113">Значение этого свойства является членом перечисления [**еавенккоммонратеконтролмоде**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode) .</span><span class="sxs-lookup"><span data-stu-id="04ef7-113">The value of this property is a member of the [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="04ef7-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04ef7-114">Remarks</span></span>

<span data-ttu-id="04ef7-115">Это свойство также используется с [кодировщиками камер H. 264 увк 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="04ef7-115">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

<span data-ttu-id="04ef7-116">[Кодекапи \_ Авенквидеотемпораллайеркаунт](/windows/desktop/medfound/codecapi-avencvideotemporallayercount), [кодекапи \_ авенквидеаусаже](/windows/desktop/medfound/codecapi-avencvideousage)и кодекапи \_ авенккоммонратеконтролмоде являются статическими свойствами кодировщика.</span><span class="sxs-lookup"><span data-stu-id="04ef7-116">[CODECAPI\_AVEncVideoTemporalLayerCount](/windows/desktop/medfound/codecapi-avencvideotemporallayercount), [CODECAPI\_AVEncVideoUsage](/windows/desktop/medfound/codecapi-avencvideousage), and CODECAPI\_AVEncCommonRateControlMode are static encoder properties.</span></span> <span data-ttu-id="04ef7-117">После установки они вступят в силу только после того, как на выходном контакте камеры будет вызван тип набора носителей.</span><span class="sxs-lookup"><span data-stu-id="04ef7-117">Once set, these will only take effect after a set media type is called on the camera’s output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="04ef7-118">Требования</span><span class="sxs-lookup"><span data-stu-id="04ef7-118">Requirements</span></span>



| <span data-ttu-id="04ef7-119">Требование</span><span class="sxs-lookup"><span data-stu-id="04ef7-119">Requirement</span></span> | <span data-ttu-id="04ef7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="04ef7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04ef7-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04ef7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="04ef7-122">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="04ef7-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="04ef7-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04ef7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="04ef7-124">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="04ef7-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="04ef7-125">Header</span><span class="sxs-lookup"><span data-stu-id="04ef7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="04ef7-126"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="04ef7-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04ef7-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04ef7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04ef7-128">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="04ef7-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="04ef7-129">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="04ef7-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

