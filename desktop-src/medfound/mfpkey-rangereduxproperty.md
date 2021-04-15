---
description: Указывает степень, до которой кодек должен уменьшить действующий цветовой диапазон видео.
ms.assetid: 7227957b-59c9-4dd9-ad2b-a383e888cd46
title: Свойство MFPKEY_RANGEREDUX (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ec326e5d21a72792aab38f08d8c8c9207ab867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702116"
---
# <a name="mfpkey_rangeredux-property"></a><span data-ttu-id="28d23-103">МФПКЭЙ \_ ранжередукс, свойство</span><span class="sxs-lookup"><span data-stu-id="28d23-103">MFPKEY\_RANGEREDUX Property</span></span>

<span data-ttu-id="28d23-104">Указывает степень, до которой кодек должен уменьшить действующий цветовой диапазон видео.</span><span class="sxs-lookup"><span data-stu-id="28d23-104">Specifies the degree to which the codec should reduce the effective color range of the video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="28d23-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="28d23-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="28d23-106">g \_ всзвмвкранжередукс</span><span class="sxs-lookup"><span data-stu-id="28d23-106">g\_wszWMVCRangeRedux</span></span>

## <a name="data-type"></a><span data-ttu-id="28d23-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="28d23-107">Data Type</span></span>

<span data-ttu-id="28d23-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="28d23-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="28d23-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="28d23-109">Default Value</span></span>

<span data-ttu-id="28d23-110">0</span><span class="sxs-lookup"><span data-stu-id="28d23-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="28d23-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28d23-111">Remarks</span></span>

<span data-ttu-id="28d23-112">Сокращение диапазона определяет степень, до которой кодек должен уменьшить яркости и чрома диапазон видео.</span><span class="sxs-lookup"><span data-stu-id="28d23-112">Range reduction specifies the degree to which the codec should reduce luma and chroma range of the video.</span></span> <span data-ttu-id="28d23-113">Уменьшение диапазона сокращает размер закодированных видеокадров, но также сокращает сведения о цвете видео.</span><span class="sxs-lookup"><span data-stu-id="28d23-113">Reducing range reduces the size of encoded video frames but also reduces the color detail of the video.</span></span>

<span data-ttu-id="28d23-114">Сокращение диапазона состоит из сокращения во время кодирования и расширения во время декодирования.</span><span class="sxs-lookup"><span data-stu-id="28d23-114">Range reduction consists of reduction during encoding and expansion during decoding.</span></span> <span data-ttu-id="28d23-115">Можно сделать так, чтобы коэффициенты расширения отличались от факторов снижения, но это не рекомендуется в большинстве сценариев, где можно использовать повторное сопоставление диапазонов.</span><span class="sxs-lookup"><span data-stu-id="28d23-115">It is possible to make the expansion factors different than the reduction factors, but this is not recommended in most scenarios where range remapping is useful.</span></span>

<span data-ttu-id="28d23-116">Сокращение диапазона и расширение выполняется отдельно для каналов яркости и чрома.</span><span class="sxs-lookup"><span data-stu-id="28d23-116">Range reduction and expansion is performed separately on luma and chroma channels.</span></span> <span data-ttu-id="28d23-117">Сокращение диапазона может быть эффективным способом снижения сложности видео с низкой скоростью, не снижая детализацию изображения.</span><span class="sxs-lookup"><span data-stu-id="28d23-117">Reducing range can be an efficient way to reduce the complexity of low bit-rate video without sacrificing image detail.</span></span> <span data-ttu-id="28d23-118">Установка для всех четырех значений значения 8 сокращает количество яркости и чрома данных на половину, оставляя больше битов для сохранения сведений об образе.</span><span class="sxs-lookup"><span data-stu-id="28d23-118">Setting all four values to 8 reduces the amount of luma and chroma information by half, leaving more bits to be directed to preserving image detail.</span></span>

<span data-ttu-id="28d23-119">Кодек может автоматически использовать сокращение диапазонов при кодировании видео с очень низкими скоростями.</span><span class="sxs-lookup"><span data-stu-id="28d23-119">The codec can choose to automatically use range reduction when encoding video at very low bit-rates.</span></span> <span data-ttu-id="28d23-120">Установка значения 0 для всех четырех значений полностью отключает сокращение диапазона даже в сценариях с низкой скоростью.</span><span class="sxs-lookup"><span data-stu-id="28d23-120">Setting all four values to 0 completely disables range reduction even in low bit-rate scenarios.</span></span>

<span data-ttu-id="28d23-121">Уменьшение цветового диапазона сокращает закодированный размер видеокадров, но может привести к образованию размытия в декодированных кадрах.</span><span class="sxs-lookup"><span data-stu-id="28d23-121">Reducing the color range reduces the encoded size of video frames but can introduce blurriness in the decoded frames.</span></span>

<span data-ttu-id="28d23-122">Если это свойство не задано, кодек определяет, следует ли использовать сокращение диапазонов во время кодирования.</span><span class="sxs-lookup"><span data-stu-id="28d23-122">If this property is not set, the codec determines whether to use range reduction at encoding time.</span></span> <span data-ttu-id="28d23-123">Как правило, этот параметр выбирается кодеком только с низкими скоростями.</span><span class="sxs-lookup"><span data-stu-id="28d23-123">Typically this option is selected by the codec only at low bit rates.</span></span>

<span data-ttu-id="28d23-124">Значение этого свойства представляет собой комбинацию из четырех компонентов, разделенных нулями, в формате 0x0M0m0N0n, где:</span><span class="sxs-lookup"><span data-stu-id="28d23-124">The value of this property is a combination of four components, separated by zeros, formatted as 0x0M0m0N0n, where:</span></span>

-   <span data-ttu-id="28d23-125">M — это коэффициент уменьшения диапазона кодирования для компонента Y.</span><span class="sxs-lookup"><span data-stu-id="28d23-125">M is the encoding range reduction factor for the Y component.</span></span>
-   <span data-ttu-id="28d23-126">m — это коэффициент расширения диапазона декодирования для компонента Y (обычно такой же, как M).</span><span class="sxs-lookup"><span data-stu-id="28d23-126">m is the decoding range expansion factor for the Y component (usually the same as M).</span></span>
-   <span data-ttu-id="28d23-127">N — коэффициент уменьшения диапазона кодирования для компонента UV.</span><span class="sxs-lookup"><span data-stu-id="28d23-127">N is the encoding range reduction factor for the UV component.</span></span>
-   <span data-ttu-id="28d23-128">n — это коэффициент расширения диапазона для компонента UV (обычно такой же, как N).</span><span class="sxs-lookup"><span data-stu-id="28d23-128">n is the decoding range expansion factor for the UV component (usually the same as N).</span></span>

<span data-ttu-id="28d23-129">Каждый фактор представляет собой цифру от 0 до 8, где 0 не уменьшается и не расширяется, а 8 — максимальное сокращение или расширение.</span><span class="sxs-lookup"><span data-stu-id="28d23-129">Each factor is a digit from 0 to 8, where 0 is no reduction or expansion and 8 is the maximum reduction or expansion.</span></span>

<span data-ttu-id="28d23-130">Если задать значение 0x00000000, сокращение диапазона будет полностью отключено.</span><span class="sxs-lookup"><span data-stu-id="28d23-130">If you set the value to 0x00000000, range reduction is completely disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="28d23-131">Требования</span><span class="sxs-lookup"><span data-stu-id="28d23-131">Requirements</span></span>



| <span data-ttu-id="28d23-132">Требование</span><span class="sxs-lookup"><span data-stu-id="28d23-132">Requirement</span></span> | <span data-ttu-id="28d23-133">Значение</span><span class="sxs-lookup"><span data-stu-id="28d23-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28d23-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28d23-134">Minimum supported client</span></span><br/> | <span data-ttu-id="28d23-135">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="28d23-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="28d23-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28d23-136">Minimum supported server</span></span><br/> | <span data-ttu-id="28d23-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="28d23-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="28d23-138">Header</span><span class="sxs-lookup"><span data-stu-id="28d23-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="28d23-139"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="28d23-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28d23-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28d23-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28d23-141">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="28d23-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




