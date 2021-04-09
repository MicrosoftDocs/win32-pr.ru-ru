---
description: Указывает типы кадров (I, P или B), к которым применяется параметр дискретизация (QP).
ms.assetid: 6331033F-7EEB-41B3-B166-29686D4AADB6
title: Свойство CODECAPI_AVEncVideoEncodeFrameTypeQP (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76e68e0cb6cbdc076dbf523f3ae9dfd7b5870f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143240"
---
# <a name="codecapi_avencvideoencodeframetypeqp-property"></a><span data-ttu-id="eb6c8-103">КОДЕКАПИ \_ авенквидеоенкодефраметипекп, свойство</span><span class="sxs-lookup"><span data-stu-id="eb6c8-103">CODECAPI\_AVEncVideoEncodeFrameTypeQP property</span></span>

<span data-ttu-id="eb6c8-104">Указывает типы кадров (I, P или B), к которым применяется параметр дискретизация (QP).</span><span class="sxs-lookup"><span data-stu-id="eb6c8-104">Specifies the frame types (I, P, or B) that the quantization parameter (QP) is applied to.</span></span>

## <a name="data-type"></a><span data-ttu-id="eb6c8-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="eb6c8-105">Data type</span></span>

<span data-ttu-id="eb6c8-106">**Улонгулонг** (VT \_ UI8)</span><span class="sxs-lookup"><span data-stu-id="eb6c8-106">**ULONGULONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="eb6c8-107">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="eb6c8-107">Property GUID</span></span>

<span data-ttu-id="eb6c8-108">**КОДЕКАПИ \_ авенквидеоенкодефраметипекп**</span><span class="sxs-lookup"><span data-stu-id="eb6c8-108">**CODECAPI\_AVEncVideoEncodeFrameTypeQP**</span></span>

## <a name="remarks"></a><span data-ttu-id="eb6c8-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb6c8-109">Remarks</span></span>

<span data-ttu-id="eb6c8-110">Для кодировщиков, поддерживающих настройку параметра дискретизация (QP) для различных типов кадров (I, P, B), они должны предоставлять этот API в дополнение к [кодекапи \_ авенквидеоенкодекп](codecapi-avencvideoencodeqp.md).</span><span class="sxs-lookup"><span data-stu-id="eb6c8-110">For encoders which support setting a quantization parameter (QP) for different frame types (I, P, B), they shall expose this API in addition to [CODECAPI\_AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md).</span></span> <span data-ttu-id="eb6c8-111">Если кодировщик поддерживает только один компонент QP для всех типов кадров, он должен поддерживать только КОДЕКАПИ \_ авенквидеоенкодекп.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-111">If an encoder supports only a single QP for all frame types, they shall support only CODECAPI\_AVEncVideoEncodeQP.</span></span>

<span data-ttu-id="eb6c8-112">Это динамическое свойство кодировки, означающее, что новое значение может быть задано в любое время в течение сеанса кодирования.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-112">This is a dynamic encoding property meaning that a new value can be set any time during the encoding session.</span></span>

<span data-ttu-id="eb6c8-113">**Кодировщики H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="eb6c8-113">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="eb6c8-114">Кодировщик должен поддерживать [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)и [**жетпараметерранже**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="eb6c8-114">Encoder shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="eb6c8-115">Набор из 4 16 битовых полей используется для указания кадра QPs в кодировке fixed-QP.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-115">A set of four 16-bit fields are used to specify the frame QPs in fixed-QP encoding.</span></span> <span data-ttu-id="eb6c8-116">Поля:</span><span class="sxs-lookup"><span data-stu-id="eb6c8-116">The fields are:</span></span>

-   <span data-ttu-id="eb6c8-117">**Bits 0-15:** Обработчик запросов, используемый для кадров I, допустимый диапазон \[ 0, 51 \] .</span><span class="sxs-lookup"><span data-stu-id="eb6c8-117">**Bits 0-15:** QP used for I frames, valid range \[0, 51\].</span></span>
-   <span data-ttu-id="eb6c8-118">**Bits 16-31:** QP, используемый для кадров P, допустимый диапазон \[ 0, 51 \] .</span><span class="sxs-lookup"><span data-stu-id="eb6c8-118">**Bits 16-31:** QP used for P frames, valid range \[0, 51\].</span></span>
-   <span data-ttu-id="eb6c8-119">**Bits 32-47:** QP, используемый для кадров B, допустимый диапазон \[ 0, 51\]</span><span class="sxs-lookup"><span data-stu-id="eb6c8-119">**Bits 32-47:** QP used for B frames, valid range \[0, 51\]</span></span>
-   <span data-ttu-id="eb6c8-120">**Bits 48-63:** зарезервировано</span><span class="sxs-lookup"><span data-stu-id="eb6c8-120">**Bits 48-63:** reserved</span></span>

<span data-ttu-id="eb6c8-121">Если этот Кодекапи поддерживается, кодировщики должны поддерживать настройку QP для типа кадра I, P и B.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-121">When this CodecAPI is supported, encoders shall support QP setting on frame type of I, P, and B.</span></span>

<span data-ttu-id="eb6c8-122">Значение по умолчанию должно быть 0x0000001a001a001a.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-122">Default value shall be 0x0000001a001a001a.</span></span> <span data-ttu-id="eb6c8-123">QP, равный 26 для I, P и B.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-123">QP equal to 26 for I, P and B.</span></span>

<span data-ttu-id="eb6c8-124">Когда [кодекапи \_ авенквидеоселектлайер](codecapi-avencvideoselectlayer.md) выбирает конкретный временный слой, [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) кодекапи \_ авенквидеоенкодефраметипекп должен установить QP для кадров I, P и B на этом временном слое.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-124">When [CODECAPI\_AVEncVideoSelectLayer](codecapi-avencvideoselectlayer.md) selects a specific temporal layer, [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) of CODECAPI\_AVEncVideoEncodeFrameTypeQP shall set QP for I, P, and B frames on that temporal layer.</span></span> <span data-ttu-id="eb6c8-125">По умолчанию он устанавливает QP для кадров I, P и B на базовом временном уровне 0.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-125">By default, it sets QP for I, P, and B frames on base temporal layer temporal layer 0.</span></span>

<span data-ttu-id="eb6c8-126">[Кодекапи \_ Авенквидеомакскп](codecapi-avencvideomaxqp.md) и [кодекапи \_ авенквидеоминкп](codecapi-avencvideominqp.md) должны использоваться для определения и ограничения диапазона QP для QPs всех типов изображений, I, P и B.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-126">[CODECAPI\_AVEncVideoMaxQP](codecapi-avencvideomaxqp.md) and [CODECAPI\_AVEncVideoMinQP](codecapi-avencvideominqp.md) shall be used to define and limit the QP range for QPs of all picture types, I, P and B.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb6c8-127">Требования</span><span class="sxs-lookup"><span data-stu-id="eb6c8-127">Requirements</span></span>



| <span data-ttu-id="eb6c8-128">Требование</span><span class="sxs-lookup"><span data-stu-id="eb6c8-128">Requirement</span></span> | <span data-ttu-id="eb6c8-129">Значение</span><span class="sxs-lookup"><span data-stu-id="eb6c8-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb6c8-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb6c8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="eb6c8-131">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="eb6c8-131">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="eb6c8-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb6c8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="eb6c8-133">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="eb6c8-133">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="eb6c8-134">Header</span><span class="sxs-lookup"><span data-stu-id="eb6c8-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb6c8-135"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb6c8-135"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb6c8-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb6c8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb6c8-137">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eb6c8-137">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

