---
description: Реализация Ивикдевелоправ
ms.assetid: 08371790-b23b-4d2e-9aea-b2c95c854401
title: Реализация Ивикдевелоправ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683dc2baf0496694943b7640d3f3ed521dc477a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272835"
---
# <a name="implementing-iwicdevelopraw"></a><span data-ttu-id="1cf25-103">Реализация Ивикдевелоправ</span><span class="sxs-lookup"><span data-stu-id="1cf25-103">Implementing IWICDevelopRaw</span></span>

## <a name="iwicdevelopraw"></a><span data-ttu-id="1cf25-104">ивикдевелоправ</span><span class="sxs-lookup"><span data-stu-id="1cf25-104">IWICDevelopRaw</span></span>

<span data-ttu-id="1cf25-105">Интерфейс [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) предоставляет параметры обработки, характерные для обработки необработанных изображений.</span><span class="sxs-lookup"><span data-stu-id="1cf25-105">The [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface exposes processing options specific to raw image processing.</span></span> <span data-ttu-id="1cf25-106">Все необработанные кодеки должны поддерживать интерфейс **ивикдевелоправ** .</span><span class="sxs-lookup"><span data-stu-id="1cf25-106">All raw codecs must support the **IWICDevelopRaw** interface.</span></span> <span data-ttu-id="1cf25-107">Некоторые кодеки необработанных кодеков могут не поддерживать каждый параметр, предоставленный этим интерфейсом, но вы должны поддерживать все параметры, которые может выполнять кодек.</span><span class="sxs-lookup"><span data-stu-id="1cf25-107">Some raw codecs may not be able to support every setting exposed by this interface, but you should support all the settings that your codec is capable of performing.</span></span> <span data-ttu-id="1cf25-108">Как минимум каждый кодек RAW должен реализовывать методы [**сетротатион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) и [**сетрендермоде**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) .</span><span class="sxs-lookup"><span data-stu-id="1cf25-108">At minimum, every raw codec must implement the [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) and [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) methods.</span></span>

<span data-ttu-id="1cf25-109">Кроме того, для необработанных кодеков настоятельно рекомендуется использовать некоторые методы и интерфейсы, которые являются необязательными для других кодеков.</span><span class="sxs-lookup"><span data-stu-id="1cf25-109">Additionally, some methods and interfaces that are optional for other codecs are strongly recommended for raw codecs.</span></span> <span data-ttu-id="1cf25-110">К ним [**относятся методы**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) [**OnPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) и ивикбитмапсаурцетрансформ в классе декодера уровня контейнера, а также интерфейс [](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) для класса декодирования на уровне кадров.</span><span class="sxs-lookup"><span data-stu-id="1cf25-110">These include the [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) and [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) methods on the container-level decoder class, and the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) interface on the frame-level decode class.</span></span>

<span data-ttu-id="1cf25-111">Параметры, заданные с помощью методов [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) , должны сохраняться кодеком так, чтобы они соответствовали способу сохранения других метаданных, но не следует перезаписывать исходные параметры "как".</span><span class="sxs-lookup"><span data-stu-id="1cf25-111">Settings set by using the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) methods should be persisted by the codec in a way that’s consistent with the way other metadata is persisted, but you should never overwrite the original "As Shot" settings.</span></span> <span data-ttu-id="1cf25-112">Путем сохранения метаданных и реализации [**лоадпараметерсет**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) и [**жеткуррентпараметерсет**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset)вы включаете приложения обработки необработанных приложений для извлечения и применения параметров обработки в сеансах.</span><span class="sxs-lookup"><span data-stu-id="1cf25-112">By persisting the metadata and implementing [**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) and [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), you enable raw processing applications to retrieve and apply processing settings across sessions.</span></span>

<span data-ttu-id="1cf25-113">Основным назначением интерфейса [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) является предоставление разработчикам приложений возможности создавать пользовательский интерфейс для настройки необработанных параметров, которые будут работать как можно одинаково в разных кодеках.</span><span class="sxs-lookup"><span data-stu-id="1cf25-113">A main purpose of the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface is to enable application developers to build a user interface for adjusting raw parameters that will work as consistently as possible across different codecs.</span></span> <span data-ttu-id="1cf25-114">Предположим, что конечный пользователь настроит параметры с помощью ползунка с минимальным и максимальным значениями, сопоставленными с минимальным и максимальным диапазонами для параметра.</span><span class="sxs-lookup"><span data-stu-id="1cf25-114">Assume that an end user will adjust the parameters by using a slider control, with its minimum and maximum values mapped to the minimum and maximum ranges for the parameter.</span></span> <span data-ttu-id="1cf25-115">Для поддержки этой ситуации следует сделать все усилия, чтобы все диапазоны параметров считались линейными.</span><span class="sxs-lookup"><span data-stu-id="1cf25-115">To support this, you should make every effort to treat all parameter ranges as linear.</span></span> <span data-ttu-id="1cf25-116">Чтобы элементы управления "ползунок" не были избыточно конфиденциальными, необходимо также поддерживать как можно более широкий диапазон для каждого параметра, охватывающий по крайней мере 50 процентов от максимально возможного диапазона.</span><span class="sxs-lookup"><span data-stu-id="1cf25-116">To ensure that the slider controls aren’t overly sensitive, you should also support as broad a range as possible for each parameter, covering at least 50 percent of the maximum possible range.</span></span> <span data-ttu-id="1cf25-117">Например, если максимально возможный диапазон контрастов находится в диапазоне от чисто серого до чисто черного и белого, а значение по умолчанию сопоставляется с 0,0, минимальный диапазон, поддерживаемый кодеком, будет иметь размер не менее половины между значением по умолчанию и чистым серым в нижней части (– 1,0), по меньшей мере на половину между значением по умолчанию и чистым черным и белым в верхней 1,0</span><span class="sxs-lookup"><span data-stu-id="1cf25-117">For example, if the maximum possible range of contrast is from pure gray to pure black and white, with the default value being mapped to 0.0, the minimum range supported by a codec would be from at least halfway between the default value and pure gray on the low end (–1.0), to at least halfway between the default value and pure black and white on the high end (+1.0).</span></span>


```C++
interface IWICDevelopRaw : IWICBitmapFrameDecode
{
   HRESULT QueryRawCapabilitiesInfo ( WICRawCapabilitiesInfo *pInfo );
   HRESULT LoadParameterSet ( WICRawParameterSet ParameterSet );
   HRESULT GetCurrentParameterSet ( IPropertyBag2 **ppCurrentParameterSet );
   HRESULT SetExposureCompensation ( double ev );
   HRESULT GetExposureCompensation ( double *pEV );
   HRESULT SetWhitePointRGB ( UINT Red, UINT Green, UINT Blue );
   HRESULT GetWhitePointRGB ( UINT *pRed, UINT *pGreen, UINT *pBlue );
   HRESULT SetNamedWhitePoint ( WICNamedWhitePoint WhitePoint );
   HRESULT GetNamedWhitePoint ( WICNamedWhitePoint *pWhitePoint );
   HRESULT SetWhitePointKelvin ( UINT WhitePointKelvin );
   HRESULT GetWhitePointKelvin ( UINT *pWhitePointKelvin );
   HRESULT GetKelvinRangeInfo ( UINT *pMinKelvinTemp,
               UINT *pMaxKelvinTemp,
               UINT *pKelvinTempStepValue );
   HRESULT SetContrast ( double Contrast );
   HRESULT GetContrast ( double *pContrast );
   HRESULT SetGamma ( double Gamma );
   HRESULT GetGamma ( double *pGamma );
   HRESULT SetSharpness ( double Sharpness );
   HRESULT GetSharpness ( double *pSharpness );
   HRESULT SetSaturation ( double Saturation );
   HRESULT GetSaturation ( double *pSaturation );
   HRESULT SetTint ( double Tint );
   HRESULT GetTint ( double *pTint );
   HRESULT SetNoiseReduction ( double NoiseReduction );
   HRESULT GetNoiseReduction ( double *pNoiseReduction );
   HRESULT SetDestinationColorContext (const IWICColorContext *pColorContext );
   HRESULT SetToneCurve ( UINT cbToneCurveSize,
               const WICRawToneCurve *pToneCurve );
   HRESULT GetToneCurve ( UINT cbToneCurveBufferSize,
               WICRawToneCurve *pToneCurve,
               UINT *pcbActualToneCurveBufferSize );
   HRESULT SetRotation ( double Rotation );
   HRESULT GetRotation ( double *pRotation );
   HRESULT SetRenderMode ( WICRawRenderMode RenderMode );
   HRESULT GetRenderMode ( WICRawRenderMode *pRenderMode ); 
   HRESULT SetNotificationCallback ( IWICDevelopRawNotificationCallback 
               *pCallback );
}
```



-   [<span data-ttu-id="1cf25-118">куериравкапабилитиесинфо</span><span class="sxs-lookup"><span data-stu-id="1cf25-118">QueryRawCapabilitiesInfo</span></span>](#queryrawcapabilitiesinfo)
-   [<span data-ttu-id="1cf25-119">лоадпараметерсет</span><span class="sxs-lookup"><span data-stu-id="1cf25-119">LoadParameterSet</span></span>](#loadparameterset)
-   [<span data-ttu-id="1cf25-120">жеткуррентпараметерсет</span><span class="sxs-lookup"><span data-stu-id="1cf25-120">GetCurrentParameterSet</span></span>](#getcurrentparameterset)
-   [<span data-ttu-id="1cf25-121">Set/Жетекспосурекомпенсатион</span><span class="sxs-lookup"><span data-stu-id="1cf25-121">Set/GetExposureCompensation</span></span>](#setgetexposurecompensation)
-   [<span data-ttu-id="1cf25-122">Set/Жеткуррентпараметерргб, Set/Жетнамедвхитепоинт, Set/Жетвхитепоинткелвин</span><span class="sxs-lookup"><span data-stu-id="1cf25-122">Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin</span></span>](#setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin)
-   [<span data-ttu-id="1cf25-123">Set/контрастность</span><span class="sxs-lookup"><span data-stu-id="1cf25-123">Set/GetContrast</span></span>](#setgetcontrast)
-   [<span data-ttu-id="1cf25-124">Set/-гамма</span><span class="sxs-lookup"><span data-stu-id="1cf25-124">Set/GetGamma</span></span>](#setgetgamma)
-   [<span data-ttu-id="1cf25-125">Set/диез</span><span class="sxs-lookup"><span data-stu-id="1cf25-125">Set/GetSharpness</span></span>](#setgetsharpness)
-   [<span data-ttu-id="1cf25-126">Задание/перенасыщенность</span><span class="sxs-lookup"><span data-stu-id="1cf25-126">Set/GetSaturation</span></span>](#setgetsaturation)
-   [<span data-ttu-id="1cf25-127">Set/-тонированный</span><span class="sxs-lookup"><span data-stu-id="1cf25-127">Set/GetTint</span></span>](#setgettint)
-   [<span data-ttu-id="1cf25-128">Set/Жетноисередуктион</span><span class="sxs-lookup"><span data-stu-id="1cf25-128">Set/GetNoiseReduction</span></span>](#setgetnoisereduction)
-   [<span data-ttu-id="1cf25-129">сетдестинатионколорконтекст</span><span class="sxs-lookup"><span data-stu-id="1cf25-129">SetDestinationColorContext</span></span>](#setdestinationcolorcontext)
-   [<span data-ttu-id="1cf25-130">Set/Жеттонекурве</span><span class="sxs-lookup"><span data-stu-id="1cf25-130">Set/GetToneCurve</span></span>](#setgettonecurve)
-   [<span data-ttu-id="1cf25-131">Задание/вращение</span><span class="sxs-lookup"><span data-stu-id="1cf25-131">Set/GetRotation</span></span>](#setgetrotation)
-   [<span data-ttu-id="1cf25-132">Set/Жетрендермоде</span><span class="sxs-lookup"><span data-stu-id="1cf25-132">Set/GetRenderMode</span></span>](#setgetrendermode)
-   [<span data-ttu-id="1cf25-133">сетнотификатионкаллбакк</span><span class="sxs-lookup"><span data-stu-id="1cf25-133">SetNotificationCallback</span></span>](#setnotificationcallback)

### <a name="queryrawcapabilitiesinfo"></a><span data-ttu-id="1cf25-134">куериравкапабилитиесинфо</span><span class="sxs-lookup"><span data-stu-id="1cf25-134">QueryRawCapabilitiesInfo</span></span>

<span data-ttu-id="1cf25-135">[**Куериравкапабилитиесинфо**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) возвращает набор поддерживаемых возможностей для этого необработанного файла.</span><span class="sxs-lookup"><span data-stu-id="1cf25-135">[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) returns the set of supported capabilities for this raw file.</span></span> <span data-ttu-id="1cf25-136">Структура [**викравкапабилитиесинфо**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1cf25-136">The [**WICRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) structure is defined as follows:</span></span>


```C++
struct WICRawCapabilitiesInfo
{
   UINT cbSize;
   UINT CodecMajorVersion;
   UINT CodecMinorVersion;
   WICRawCapabilities ExposureCompensationSupport;
   WICRawCapabilities ContrastSupport;
   WICRawCapabilities RGBWhitePointSupport;
   WICRawCapabilities NamedWhitePointSupport;
   UINT NamedWhitePointSupportMask;
   WICRawCapabilities KelvinWhitePointSupport;
   WICRawCapabilities GammaSupport;
   WICRawCapabilities TintSupport;
   WICRawCapabilities SaturationSupport;
   WICRawCapabilities SharpnessSupport;
   WICRawCapabilities NoiseReductionSupport;
   WICRawCapabilities DestinationColorProfileSupport;
   WICRawCapabilities ToneCurveSupport;
   WICRawRotationCapabilities RotationSupport;              
}
```



<span data-ttu-id="1cf25-137">Перечисление [**викравкапабилитиес**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) , используемое в этой структуре, определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1cf25-137">The [**WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) enumeration used in this structure is defined as:</span></span>


```C++
enum WICRawCapabilities 
{   
   WICRawCapabilityNotSupported,
   WICRawCapabilityGetSupported,
   WICRawCapabilityFullySupported
}
```



<span data-ttu-id="1cf25-138">Последним полем является перечисление [**викравротатионкапабилитиес**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) , определенное следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1cf25-138">The final field is a [**WICRawRotationCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) enumeration, defined as:</span></span>


```C++
enum WICRawRotationCapabilities                    
{
   WICRawRotationCapabilityNotSupported,
   WICRawRotationCapabilityGetSupported,
   WICRawRotationCapabilityNinetyDegreesSupported
   WICRawRotationCapabilityFullySupported
}
```



### <a name="loadparameterset"></a><span data-ttu-id="1cf25-139">лоадпараметерсет</span><span class="sxs-lookup"><span data-stu-id="1cf25-139">LoadParameterSet</span></span>

<span data-ttu-id="1cf25-140">[**Лоадпараметерсет**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) позволяет пользователю указать, следует ли использовать в качестве параметров снимка, использовать настроенные пользователем параметры или запросить автоматическое исправление образа в декодере.</span><span class="sxs-lookup"><span data-stu-id="1cf25-140">[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) enables the user to specify whether to use As Shot settings, use user-adjusted settings, or request the decoder to auto-correct the image.</span></span>


```C++
enum WICRawParameterSet
{
   WICAsShotParameterSet,
   WICUserAdjustedParameterSet,
   WICAutoAdjustedParameterSet
}
```



### <a name="getcurrentparameterset"></a><span data-ttu-id="1cf25-141">жеткуррентпараметерсет</span><span class="sxs-lookup"><span data-stu-id="1cf25-141">GetCurrentParameterSet</span></span>

<span data-ttu-id="1cf25-142">[**Жеткуррентпараметерсет**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) возвращает **IPropertyBag2** с текущим набором параметров.</span><span class="sxs-lookup"><span data-stu-id="1cf25-142">[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) returns an **IPropertyBag2** with the current parameter set.</span></span> <span data-ttu-id="1cf25-143">Затем вызывающий объект может передать этот набор параметров кодировщику для использования в качестве параметров кодировщика.</span><span class="sxs-lookup"><span data-stu-id="1cf25-143">The caller can then pass this parameter set to the encoder to use as the encoder options.</span></span>

### <a name="setgetexposurecompensation"></a><span data-ttu-id="1cf25-144">Set/Жетекспосурекомпенсатион</span><span class="sxs-lookup"><span data-stu-id="1cf25-144">Set/GetExposureCompensation</span></span>

<span data-ttu-id="1cf25-145">[**Жетекспосурекомпенсатион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) и [**сетекспосурекомпенсатион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) указывают компенсацию экспозиции, применяемую к окончательному выходу.</span><span class="sxs-lookup"><span data-stu-id="1cf25-145">[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) and [**SetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) indicate the exposure compensation to apply to the final output.</span></span> <span data-ttu-id="1cf25-146">Допустимый диапазон для EV — от – 5,0 до + 5,0.</span><span class="sxs-lookup"><span data-stu-id="1cf25-146">The valid range for EV is –5.0 to +5.0 stops.</span></span>

### <a name="setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin"></a><span data-ttu-id="1cf25-147">Set/Жеткуррентпараметерргб, Set/Жетнамедвхитепоинт, Set/Жетвхитепоинткелвин</span><span class="sxs-lookup"><span data-stu-id="1cf25-147">Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin</span></span>

<span data-ttu-id="1cf25-148">Все эти функции предоставляют способы получения и задания белого пункта как значения RGB, предустановки именованного значения или в качестве значения Кельвина.</span><span class="sxs-lookup"><span data-stu-id="1cf25-148">These functions all provide ways to get and set the white point, either as an RGB value, a preset named value, or as a Kelvin value.</span></span> <span data-ttu-id="1cf25-149">Допустимый диапазон для Кельвина — 1 500 – 30 000.</span><span class="sxs-lookup"><span data-stu-id="1cf25-149">The acceptable range for Kelvin is 1,500 – 30,000.</span></span>

### <a name="setgetcontrast"></a><span data-ttu-id="1cf25-150">Set/контрастность</span><span class="sxs-lookup"><span data-stu-id="1cf25-150">Set/GetContrast</span></span>

<span data-ttu-id="1cf25-151">Параметр " [**контрастность**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) " и [**сетконтраст**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) указывает степень контрастности, применяемую к выходным данным.</span><span class="sxs-lookup"><span data-stu-id="1cf25-151">[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) and [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) indicate the amount of contrast to apply to the output.</span></span> <span data-ttu-id="1cf25-152">Допустимый диапазон для указания контрастности — от – 1,0 до + 1,0, а контраст по умолчанию — 0,0.</span><span class="sxs-lookup"><span data-stu-id="1cf25-152">The valid range to specify contrast is –1.0 to +1.0, with the default contrast being 0.0.</span></span>

### <a name="setgetgamma"></a><span data-ttu-id="1cf25-153">Set/-гамма</span><span class="sxs-lookup"><span data-stu-id="1cf25-153">Set/GetGamma</span></span>

<span data-ttu-id="1cf25-154">Параметр [**сетгамма**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) указывает гамму [**, которую**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="1cf25-154">[**GetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) and [**SetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) indicate the Gamma to apply.</span></span> <span data-ttu-id="1cf25-155">Допустимый диапазон для гаммы — 0,2 – 5,0, значение по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="1cf25-155">The valid range for Gamma is 0.2 to 5.0, with 1.0 being the default.</span></span> <span data-ttu-id="1cf25-156">Гамма обычно реализуется с помощью традиционной функции гаммы-коррекции мощности (линейная функция питания с помощью Unity).</span><span class="sxs-lookup"><span data-stu-id="1cf25-156">Gamma typically is implemented using the traditional Gamma power function (a linear power function with unity gain).</span></span> <span data-ttu-id="1cf25-157">Яркость увеличивается с увеличением гамма и уменьшается при приближении к нулевому гамме.</span><span class="sxs-lookup"><span data-stu-id="1cf25-157">Brightness is increased with increasing Gamma and decreased as Gamma approaches zero.</span></span> <span data-ttu-id="1cf25-158">(Обратите внимание, что минимальное значение не равно нулю, поскольку ноль приведет к ошибке деления на ноль в традиционных вычислениях гаммы.</span><span class="sxs-lookup"><span data-stu-id="1cf25-158">(Note that the minimum value is non-zero, because zero would result in a divide-by-zero error in traditional Gamma calculations.</span></span> <span data-ttu-id="1cf25-159">Логический минимальный предел — 1/Max, поэтому минимальное значение — 0,2.)</span><span class="sxs-lookup"><span data-stu-id="1cf25-159">The logical minimum limit is 1/max, which is why the minimum is 0.2.)</span></span>

### <a name="setgetsharpness"></a><span data-ttu-id="1cf25-160">Set/диез</span><span class="sxs-lookup"><span data-stu-id="1cf25-160">Set/GetSharpness</span></span>

<span data-ttu-id="1cf25-161">[**Четкость**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) и [**сетшарпнесс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) указывают объем данных, которые нужно применить.</span><span class="sxs-lookup"><span data-stu-id="1cf25-161">[**GetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) and [**SetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) indicate the amount of sharpening to apply.</span></span> <span data-ttu-id="1cf25-162">Допустимый диапазон — от – 1,0 до + 1,0, где 0,0 — это значение по умолчанию, а – 1,0, указывающее на отсутствие резкости.</span><span class="sxs-lookup"><span data-stu-id="1cf25-162">The valid range is –1.0 to +1.0, with 0.0 being the default amount of sharpening, and –1.0 indicating no sharpening at all.</span></span>

### <a name="setgetsaturation"></a><span data-ttu-id="1cf25-163">Задание/перенасыщенность</span><span class="sxs-lookup"><span data-stu-id="1cf25-163">Set/GetSaturation</span></span>

<span data-ttu-id="1cf25-164">Параметр [**сетсатуратион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) указывает степень насыщенности [**, которую**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="1cf25-164">[**GetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) and [**SetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) indicate the amount of saturation to apply.</span></span> <span data-ttu-id="1cf25-165">Допустимый диапазон для указания насыщенности — от – 1,0 до + 1,0, а 0,0 — нормальная насыщенность, – 1,0 представляет полную раснасыщенность, а + 1,0 — полную насыщенность.</span><span class="sxs-lookup"><span data-stu-id="1cf25-165">The valid range to specify saturation is –1.0 to +1.0, with 0.0 being normal saturation, –1.0 representing complete desaturation, and +1.0 representing full saturation.</span></span>

### <a name="setgettint"></a><span data-ttu-id="1cf25-166">Set/-тонированный</span><span class="sxs-lookup"><span data-stu-id="1cf25-166">Set/GetTint</span></span>

<span data-ttu-id="1cf25-167">Параметр [**сеттинт**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) указывает, какой [**оттенок следует**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) применить, с зеленым или пурпурным смещением.</span><span class="sxs-lookup"><span data-stu-id="1cf25-167">[**GetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) and [**SetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) indicate the tint to apply, on a green/magenta bias.</span></span> <span data-ttu-id="1cf25-168">Допустимый диапазон — от – 1,0 до + 1,0, зеленый — на отрицательной стороне шкалы и пурпурный на положительном.</span><span class="sxs-lookup"><span data-stu-id="1cf25-168">The valid range is –1.0 to +1.0, with green being on the negative side of the scale and magenta on the positive.</span></span> <span data-ttu-id="1cf25-169">Шкала оттенков определяется как ортогональная цветовая температура.</span><span class="sxs-lookup"><span data-stu-id="1cf25-169">The tint scale is defined as orthogonal to color temperature.</span></span>

### <a name="setgetnoisereduction"></a><span data-ttu-id="1cf25-170">Set/Жетноисередуктион</span><span class="sxs-lookup"><span data-stu-id="1cf25-170">Set/GetNoiseReduction</span></span>

<span data-ttu-id="1cf25-171">[**Жетноисередуктион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) и [**сетноисередуктион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) указывают объем применяемого снижения шума.</span><span class="sxs-lookup"><span data-stu-id="1cf25-171">[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) and [**SetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) indicate the amount of noise reduction to apply.</span></span> <span data-ttu-id="1cf25-172">Допустимый диапазон — от – 1,0 до + 1,0, с 0,0, указывающим значение по умолчанию для снижения шума, – 1,0, указывающее на отсутствие шума и + 1,0, указывающее на максимальное снижение шума.</span><span class="sxs-lookup"><span data-stu-id="1cf25-172">The valid range to is –1.0 to +1.0, with 0.0 indicating the default amount of noise reduction, –1.0 indicating no noise reduction and +1.0 indicating maximum noise reduction.</span></span>

### <a name="setdestinationcolorcontext"></a><span data-ttu-id="1cf25-173">сетдестинатионколорконтекст</span><span class="sxs-lookup"><span data-stu-id="1cf25-173">SetDestinationColorContext</span></span>

<span data-ttu-id="1cf25-174">[**Сетдестинатионколорконтекст**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) указывает цветовой профиль, применяемый к изображению.</span><span class="sxs-lookup"><span data-stu-id="1cf25-174">[**SetDestinationColorContext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) specifies the color profile to apply to the image.</span></span> <span data-ttu-id="1cf25-175">Для получения текущего цветового профиля можно вызвать [**жетколорконтекстс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) .</span><span class="sxs-lookup"><span data-stu-id="1cf25-175">You can call [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) to retrieve the current color profile.</span></span>

### <a name="setgettonecurve"></a><span data-ttu-id="1cf25-176">Set/Жеттонекурве</span><span class="sxs-lookup"><span data-stu-id="1cf25-176">Set/GetToneCurve</span></span>

<span data-ttu-id="1cf25-177">[**Жеттонекурве**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) и [**сеттонекурве**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) определяют применяемую кривую тона.</span><span class="sxs-lookup"><span data-stu-id="1cf25-177">[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) and [**SetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) specify the tone curve to apply.</span></span> <span data-ttu-id="1cf25-178">Предположим линейную интерполяцию между точками.</span><span class="sxs-lookup"><span data-stu-id="1cf25-178">Assume linear interpolation between points.</span></span> <span data-ttu-id="1cf25-179">**Птонекурве** — это структура [**викравтонекурве**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) , которая содержит массив структур [**викравтонекурвепоинт**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) и количество точек в массиве.</span><span class="sxs-lookup"><span data-stu-id="1cf25-179">The **pToneCurve** is a [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) structure, which contains an array of [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) structures, and a count of the number of points in the array.</span></span>


```C++
struct WICRawToneCurve 
{
   UINT cPoints;
   WICRawToneCurvePoint aPoints[];
}
```



<span data-ttu-id="1cf25-180">[**Викравтонекурвепоинт**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) содержит входное значение и выходное значение.</span><span class="sxs-lookup"><span data-stu-id="1cf25-180">A [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) contains an input value and an output value.</span></span>


```C++
struct WICRawToneCurvePoint 
{
   double Input;
   double Output;
}
```



<span data-ttu-id="1cf25-181">Когда вызывающий объект передает **значение NULL** в параметре *птонекурве* , необходимо передать обратно необходимый размер для [**викравтонекурве**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) в параметре *пкбактуалтонекурвебуфферсизе* .</span><span class="sxs-lookup"><span data-stu-id="1cf25-181">When the caller passes **NULL** in the *pToneCurve* parameter, you should pass back the required size for the [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) in the *pcbActualToneCurveBufferSize* parameter.</span></span>

### <a name="setgetrotation"></a><span data-ttu-id="1cf25-182">Задание/вращение</span><span class="sxs-lookup"><span data-stu-id="1cf25-182">Set/GetRotation</span></span>

<span data-ttu-id="1cf25-183">[**Вращение**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) и [**сетротатион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) указывают степень поворота для применения.</span><span class="sxs-lookup"><span data-stu-id="1cf25-183">[**GetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) and [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) indicate the degree of rotation to apply.</span></span> <span data-ttu-id="1cf25-184">При повороте 90,0 будет задан поворот на 90 градусов по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="1cf25-184">A rotation of 90.0 would specify a rotation of 90 degrees clockwise.</span></span> <span data-ttu-id="1cf25-185">(Разница между использованием **сетротатион** и заданием вращения с помощью метода [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) заключается в том, что угол поворота, заданный с помощью **сетротатион** , должен сохраняться кодеком, а установка вращения через **CopyPixels** только поворачивает изображение в памяти.</span><span class="sxs-lookup"><span data-stu-id="1cf25-185">(The difference between using **SetRotation** and setting rotation using the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) method is that the rotation angle set using **SetRotation** should be persisted by the codec, while setting rotation through **CopyPixels** only rotates the image in memory.</span></span>

### <a name="setgetrendermode"></a><span data-ttu-id="1cf25-186">Set/Жетрендермоде</span><span class="sxs-lookup"><span data-stu-id="1cf25-186">Set/GetRenderMode</span></span>

<span data-ttu-id="1cf25-187">[**Жетрендермоде**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) и [**сетрендермоде**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) указывают уровень качества выходных данных, необходимых вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="1cf25-187">[**GetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) and [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) indicate the quality level of output the caller requires.</span></span> <span data-ttu-id="1cf25-188">Когда пользователь настраивает параметры, в приложении должно отображаться очень быстрое приближение того, как будет выглядеть фактический образ при применении изменений.</span><span class="sxs-lookup"><span data-stu-id="1cf25-188">When a user is adjusting parameters, the application should display a very fast approximation of what the actual image will look like if the changes are applied.</span></span> <span data-ttu-id="1cf25-189">Для этой цели изображение обычно отображается при разрешении экрана или меньше, а не на фактическом разрешении изображения, чтобы обеспечить немедленную отклики пользователя.</span><span class="sxs-lookup"><span data-stu-id="1cf25-189">For this purpose, the image is usually displayed at screen resolution or less, rather than the actual image resolution, to provide immediate feedback to the user.</span></span> <span data-ttu-id="1cf25-190">Это происходит, когда приложение запрашивает качество режима черновика, поэтому это должно быть очень быстрым.</span><span class="sxs-lookup"><span data-stu-id="1cf25-190">This is when an application would request Draft Mode quality, so this should be very fast.</span></span> <span data-ttu-id="1cf25-191">Когда пользователь внес все изменения, просматривает их в режиме черновика и решил декодировать полное изображение с текущими параметрами, приложение запрашивает оптимальное качество расшифровки.</span><span class="sxs-lookup"><span data-stu-id="1cf25-191">When the user has made all changes, previewed them in draft mode, and decided to decode the full image with the current settings, the application requests a Best Quality decode.</span></span> <span data-ttu-id="1cf25-192">Обычно это также требуется для печати.</span><span class="sxs-lookup"><span data-stu-id="1cf25-192">This is usually also requested for printing.</span></span> <span data-ttu-id="1cf25-193">Если требуется разумное компромиссное качество, приложение запрашивает нормальное качество.</span><span class="sxs-lookup"><span data-stu-id="1cf25-193">Where a reasonable tradeoff between speed an quality is required, the application requests Normal Quality.</span></span>


```C++
enum WICRawRenderMode
{
   WICRawRenderModeDraftMode,
   WICRawRenderModeNormalQuality ,
   WICRawRenderModeBestQuality
}
```



### <a name="setnotificationcallback"></a><span data-ttu-id="1cf25-194">сетнотификатионкаллбакк</span><span class="sxs-lookup"><span data-stu-id="1cf25-194">SetNotificationCallback</span></span>

<span data-ttu-id="1cf25-195">[**Сетнотификатионкаллбакк**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) регистрирует функцию обратного вызова для вызова декодера при изменении любого из параметров обработки необработанных данных.</span><span class="sxs-lookup"><span data-stu-id="1cf25-195">[**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) registers a callback function for the decoder to call when any of the Raw processing parameters change.</span></span> <span data-ttu-id="1cf25-196">Сигнатура для [**ивикдевелоправнотификатионкаллбакк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) имеет только один метод, именуемый [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify).</span><span class="sxs-lookup"><span data-stu-id="1cf25-196">The signature for the [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) has only one method, called [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify).</span></span> <span data-ttu-id="1cf25-197">**Notify** имеет единственный параметр — маску, указывающую, какие из параметров обработки необработанных данных были изменены.</span><span class="sxs-lookup"><span data-stu-id="1cf25-197">**Notify** has a single parameter, which is a mask that indicates which of the raw processing parameters have changed.</span></span>


```C++
HRESULT Notify ( UINT NotificationMask );
```



<span data-ttu-id="1cf25-198">Операция OR выполняется для следующих значений Нотификатионмаск.</span><span class="sxs-lookup"><span data-stu-id="1cf25-198">An OR operation is performed on the following values for the NotificationMask.</span></span>


```C++
WICRawChangeNotification_ExposureCompensation
WICRawChangeNotification_NamedWhitePoint
WICRawChangeNotification_KelvinWhitePoint
WICRawChangeNotification_RGBWhitePoint
WICRawChangeNotification_Contrast
WICRawChangeNotification_Gamma
WICRawChangeNotification_Sharpness
WICRawChangeNotification_Saturation
WICRawChangeNotification_Tint
WICRawChangeNotification_NoiseReduction
WICRawChangeNotification_DestinationColorContext
WICRawChangeNotification_ToneCurve
WICRawChangeNotification_Rotation
WICRawChangeNotification_RenderMode
```



## <a name="related-topics"></a><span data-ttu-id="1cf25-199">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="1cf25-199">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1cf25-200">**Reference**</span><span class="sxs-lookup"><span data-stu-id="1cf25-200">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1cf25-201">**ивикдевелоправ**</span><span class="sxs-lookup"><span data-stu-id="1cf25-201">**IWICDevelopRaw**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)
</dt> <dt>

<span data-ttu-id="1cf25-202">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="1cf25-202">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1cf25-203">Реализация Ивикбитмапсаурцетрансформ</span><span class="sxs-lookup"><span data-stu-id="1cf25-203">Implementing IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[<span data-ttu-id="1cf25-204">Реализация кодировщика WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="1cf25-204">Implementing a WIC-Enabled Encoder</span></span>](-wic-implementingwicencoder.md)
</dt> <dt>

[<span data-ttu-id="1cf25-205">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="1cf25-205">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="1cf25-206">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="1cf25-206">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



