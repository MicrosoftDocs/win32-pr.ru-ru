---
description: Указывает предоставляемые автором коэффициенты свертывания для декодирования многоканального звука для меньшего количества каналов, чем содержит закодированный поток.
ms.assetid: f6737c05-4b39-4209-9985-9402b28cf316
title: Свойство MFPKEY_WMADEC_FOLDDOWN_MATRIX (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92cb2495863d319c7f755d7d72f475ccf1eda75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711445"
---
# <a name="mfpkey_wmadec_folddown_matrix-property"></a><span data-ttu-id="1d191-103">МФПКЭЙ \_ вмадек \_ Фолддовн, \_ свойство матрицы</span><span class="sxs-lookup"><span data-stu-id="1d191-103">MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX Property</span></span>

<span data-ttu-id="1d191-104">Указывает предоставляемые автором коэффициенты свертывания для декодирования многоканального звука для меньшего количества каналов, чем содержит закодированный поток.</span><span class="sxs-lookup"><span data-stu-id="1d191-104">Specifies the author-supplied fold-down coefficients for decoding multichannel audio for fewer channels than the encoded stream contains.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1d191-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="1d191-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1d191-106">g \_ всзвмакфолддовнкстойчаннелс</span><span class="sxs-lookup"><span data-stu-id="1d191-106">g\_wszWMACFoldDownXToYChannels</span></span>

<span data-ttu-id="1d191-107">g \_ всзвмакфолдкстойчаннелсз</span><span class="sxs-lookup"><span data-stu-id="1d191-107">g\_wszWMACFoldXToYChannelsZ</span></span>

## <a name="data-type"></a><span data-ttu-id="1d191-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1d191-108">Data Type</span></span>

<span data-ttu-id="1d191-109">**VT \_ массив \| VT \_**</span><span class="sxs-lookup"><span data-stu-id="1d191-109">**VT\_ARRAY \| VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="1d191-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d191-110">Remarks</span></span>

<span data-ttu-id="1d191-111">Звуковой декодер может использоваться как объект мультимедиа DirectX (DMO) или как преобразование Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="1d191-111">An audio decoder can act as a DirectX Media Object (DMO) or as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="1d191-112">Сведения о том, когда декодер выступает в качестве DMO или MFT, см. на страницах справочника по отдельным кодекам в разделе [объекты кодека](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="1d191-112">For information on when a decoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="1d191-113">При использовании декодера в качестве DMO декодер может выполнять канал, а также перечислять выводимые типы выходных данных путем вызова [**имедиаобжект:: жетаутпуттипе**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span><span class="sxs-lookup"><span data-stu-id="1d191-113">When you use a decoder as a DMO, the decoder can perform channel fold down, and you can enumerate folded down output media types by calling [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span></span>

<span data-ttu-id="1d191-114">При использовании декодера в качестве MFT декодер по умолчанию не будет выполнять никаких свертывания и не будет предлагать типы выходных носителей со сведенными выпусками.</span><span class="sxs-lookup"><span data-stu-id="1d191-114">When you use a decoder as an MFT, the decoder by default will not perform any fold down, and will not offer folded down output media types.</span></span> <span data-ttu-id="1d191-115">Декодер, выступающий в виде MFT, будет выполняться только в том случае, если пользовательские коэффициенты свертывания задаются с помощью свойства **мфпкэй \_ вмадек \_ фолддовн \_ Matrix** .</span><span class="sxs-lookup"><span data-stu-id="1d191-115">A decoder acting as an MFT will perform fold down only if custom fold-down coefficients are set using the **MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX** property.</span></span>

<span data-ttu-id="1d191-116">Если свойство **мфпкэй \_ вмадек \_ фолддовн \_ Matrix** не задано в файле MFT звукового декодера и вы хотите выполнить свертывание, можно использовать (в виде MFT) обработчика цифровых сигналов для перевыборки звука.</span><span class="sxs-lookup"><span data-stu-id="1d191-116">If the **MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX** property is not set on the audio decoder MFT, and you want to perform a fold down, you can use (as an MFT) the Audio Resampler digital signal processor.</span></span>

<span data-ttu-id="1d191-117">Значение этого свойства представляет собой строку, содержащую коэффициенты свертывания в разделенный запятыми список целочисленных значений.</span><span class="sxs-lookup"><span data-stu-id="1d191-117">The value for this property is a string containing fold-down coefficients in a comma-separated list of integer values.</span></span> <span data-ttu-id="1d191-118">Список должен содержать несколько целых чисел для каждого канала в закодированном содержимом, равное количеству каналов в декодированном содержимом.</span><span class="sxs-lookup"><span data-stu-id="1d191-118">The list must contain a number of integers for each channel in the encoded content equal to the number of channels in the decoded content.</span></span>

<span data-ttu-id="1d191-119">Если коэффициент равен нулю, то значение, используемое в строке, должно быть "-2147483648"; в противном случае значение будет вычислено с помощью уравнения: 20 \* 65536 \* LOG10 (x).</span><span class="sxs-lookup"><span data-stu-id="1d191-119">If the coefficient is zero, the value to be used in the string must be "-2147483648";otherwise the value is computed using the equation: 20 \* 65536 \* log10(x).</span></span>

<span data-ttu-id="1d191-120">Коэффициенты перечисляются в порядке маски канала, как определено константами маски канала, которые включены в заголовочный файл ммрег. h.</span><span class="sxs-lookup"><span data-stu-id="1d191-120">Coefficients are listed in channel mask order, as defined by the channel mask constants that are included in the mmreg.h header file.</span></span> <span data-ttu-id="1d191-121">Таким образом, первые два значения в канале из 6 в 2 представляют части левого выходного канала и правый канал вывода, которые состоят из центрального левого канала в потоке 6 каналов.</span><span class="sxs-lookup"><span data-stu-id="1d191-121">Therefore, the first two values in a 6-to-2 channel fold-down represent the portions of the left output channel and the right output channel that are made up of the center left channel in the 6 channel stream.</span></span>

<span data-ttu-id="1d191-122">Это свойство следует задавать только в том случае, если предоставляемые автором значения свертывания сохраняются с кодированным содержимым.</span><span class="sxs-lookup"><span data-stu-id="1d191-122">You should set this property only if author-supplied fold-down values are persisted with the encoded content.</span></span> <span data-ttu-id="1d191-123">В противном случае позвольте декодеру выполнять собственные вычисления.</span><span class="sxs-lookup"><span data-stu-id="1d191-123">Otherwise, let the decoder make its own calculations.</span></span>

<span data-ttu-id="1d191-124">Кодек Windows Media Audio 10 профессиональная в настоящее время поддерживает только свертывание до двух каналов.</span><span class="sxs-lookup"><span data-stu-id="1d191-124">The Windows Media Audio 10 Professional codec currently only supports fold-down to two channels.</span></span>

<span data-ttu-id="1d191-125">Если для свойства [мфпкэй \_ вмадек \_ спкркфг](mfpkey-wmadec-spkrcfgproperty.md) задано значение **дсспеакер \_**, кодек будет игнорировать предоставленные автором коэффициенты свертывания и выполнить свертывание до 2-канального сигнала, который может быть обработан декодером матрицы получателя.</span><span class="sxs-lookup"><span data-stu-id="1d191-125">If the [MFPKEY\_WMADEC\_SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md) property is set to **DSSPEAKER\_SURROUND**, the codec will ignore author-supplied fold-down coefficients and fold down to a 2-channel signal that can be processed by the matrix decoder of the receiver.</span></span> <span data-ttu-id="1d191-126">Это позволяет окружающему оборудованию доставлять четыре канала.</span><span class="sxs-lookup"><span data-stu-id="1d191-126">This enables surround equipment to deliver four channels.</span></span> <span data-ttu-id="1d191-127">Этот режим поддерживается, только если источником является 5,1.</span><span class="sxs-lookup"><span data-stu-id="1d191-127">This mode is supported only if the source is 5.1.</span></span> <span data-ttu-id="1d191-128">Кодек может полагаться только на 8 каналов в 2 канала.</span><span class="sxs-lookup"><span data-stu-id="1d191-128">The codec can only fold 8 channels to 2 channels.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d191-129">Требования</span><span class="sxs-lookup"><span data-stu-id="1d191-129">Requirements</span></span>



| <span data-ttu-id="1d191-130">Требование</span><span class="sxs-lookup"><span data-stu-id="1d191-130">Requirement</span></span> | <span data-ttu-id="1d191-131">Значение</span><span class="sxs-lookup"><span data-stu-id="1d191-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d191-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d191-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1d191-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1d191-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1d191-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d191-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1d191-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1d191-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1d191-136">Header</span><span class="sxs-lookup"><span data-stu-id="1d191-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d191-137"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d191-137"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d191-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d191-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d191-139">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1d191-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
