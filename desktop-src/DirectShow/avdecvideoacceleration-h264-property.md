---
description: Включает или отключает аппаратное ускорение для декодирования H. 264.
ms.assetid: 3912136d-0fc1-49b0-bc79-0785d63041e6
title: Свойство AVDecVideoAcceleration_H264 (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbcedf2d038c010ee781030baf0a8289e68eab4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103895033"
---
# <a name="avdecvideoacceleration_h264-property"></a><span data-ttu-id="17fe9-103">Авдеквидеоакцелератион \_ H264 Single bitrate, свойство</span><span class="sxs-lookup"><span data-stu-id="17fe9-103">AVDecVideoAcceleration\_H264 property</span></span>

<span data-ttu-id="17fe9-104">Включает или отключает аппаратное ускорение для декодирования H. 264.</span><span class="sxs-lookup"><span data-stu-id="17fe9-104">Enables or disables hardware acceleration for H.264 video decoding.</span></span>

<span data-ttu-id="17fe9-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="17fe9-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="17fe9-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="17fe9-106">Data type</span></span>

<span data-ttu-id="17fe9-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="17fe9-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="17fe9-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="17fe9-108">Property GUID</span></span>

<span data-ttu-id="17fe9-109">**КОДЕКАПИ \_ авдеквидеоакцелератион \_ H264 Single bitrate**</span><span class="sxs-lookup"><span data-stu-id="17fe9-109">**CODECAPI\_AVDecVideoAcceleration\_H264**</span></span>

## <a name="remarks"></a><span data-ttu-id="17fe9-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17fe9-110">Remarks</span></span>

<span data-ttu-id="17fe9-111">Если значение равно нулю, декодер не использует ускорение видео DirectX (ДКСВА) для декодирования H. 264.</span><span class="sxs-lookup"><span data-stu-id="17fe9-111">If the value is zero, the decoder does not use DirectX Video Acceleration (DXVA) for H.264 video decoding.</span></span> <span data-ttu-id="17fe9-112">Для фильтров DirectShow установите это свойство перед подключением выходного ПИН-кода декодера.</span><span class="sxs-lookup"><span data-stu-id="17fe9-112">For DirectShow filters, set this property before the decoder's output pin is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="17fe9-113">Требования</span><span class="sxs-lookup"><span data-stu-id="17fe9-113">Requirements</span></span>



| <span data-ttu-id="17fe9-114">Требование</span><span class="sxs-lookup"><span data-stu-id="17fe9-114">Requirement</span></span> | <span data-ttu-id="17fe9-115">Значение</span><span class="sxs-lookup"><span data-stu-id="17fe9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17fe9-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17fe9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="17fe9-117">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="17fe9-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="17fe9-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17fe9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="17fe9-119">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="17fe9-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="17fe9-120">Header</span><span class="sxs-lookup"><span data-stu-id="17fe9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="17fe9-121"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="17fe9-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17fe9-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17fe9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17fe9-123">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="17fe9-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="17fe9-124">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="17fe9-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




