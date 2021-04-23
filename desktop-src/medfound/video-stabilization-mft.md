---
description: Файл MFT видео стабилизации — это Microsoft Media Foundation преобразование (MFT), которое выполняет стабилизации Image в потоке видео.
ms.assetid: BBC42190-08E4-4C3B-972A-FD30621A6CC1
title: Стабилизация видео MFT (Камерауиконтрол. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65eb64b05e41842b1f7b3ad2e49a6c064be08f0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669277"
---
# <a name="video-stabilization-mft"></a><span data-ttu-id="44bb5-103">Стабилизация видео MFT</span><span class="sxs-lookup"><span data-stu-id="44bb5-103">Video Stabilization MFT</span></span>

<span data-ttu-id="44bb5-104">Файл MFT видео стабилизации — это Microsoft Media Foundation преобразование (MFT), которое выполняет стабилизации Image в потоке видео.</span><span class="sxs-lookup"><span data-stu-id="44bb5-104">The video stabilization MFT is a Microsoft Media Foundation transform (MFT) that performs image stabilization on a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="44bb5-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="44bb5-105">CLSID</span></span>

<span data-ttu-id="44bb5-106">\_КМСВИДЕОДСПМФТ CLSID</span><span class="sxs-lookup"><span data-stu-id="44bb5-106">CLSID\_CMSVideoDSPMFT</span></span>

## <a name="interfaces"></a><span data-ttu-id="44bb5-107">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="44bb5-107">Interfaces</span></span>

-   [<span data-ttu-id="44bb5-108">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="44bb5-108">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="44bb5-109">**имфаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="44bb5-109">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="44bb5-110">**имфкуалитядвисе**</span><span class="sxs-lookup"><span data-stu-id="44bb5-110">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="44bb5-111">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="44bb5-111">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="44bb5-112">**имедиаекстенсион**</span><span class="sxs-lookup"><span data-stu-id="44bb5-112">**IMediaExtension**</span></span>](/uwp/api/Windows.Media.IMediaExtension?view=winrt-19041)

## <a name="input-formats"></a><span data-ttu-id="44bb5-113">Форматы входных данных</span><span class="sxs-lookup"><span data-stu-id="44bb5-113">Input Formats</span></span>

<span data-ttu-id="44bb5-114">Следующие комбинации типа входного носителя и подтипа, принимаемые в файле MFT видео стабилизации для несжатого видео:</span><span class="sxs-lookup"><span data-stu-id="44bb5-114">The input media type and sub-type combinations accepted by the video stabilization MFT for uncompressed video are:</span></span>

-   <span data-ttu-id="44bb5-115">**\_видео MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="44bb5-115">**MEDIATYPE\_VIDEO**</span></span>
-   <span data-ttu-id="44bb5-116">**МЕДИАСУБТИПЕ \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="44bb5-116">**MEDIASUBTYPE\_NV12**</span></span>
-   <span data-ttu-id="44bb5-117">**МЕДИАСУБТИПЕ \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="44bb5-117">**MEDIASUBTYPE\_YUY2**</span></span>

## <a name="output-formats"></a><span data-ttu-id="44bb5-118">Форматы выходных данных</span><span class="sxs-lookup"><span data-stu-id="44bb5-118">Output Formats</span></span>

<span data-ttu-id="44bb5-119">Ниже приведены сочетания типа выходных данных и подтипов, принимаемые файлом MFT видео стабилизации.</span><span class="sxs-lookup"><span data-stu-id="44bb5-119">The output media type and sub-type combinations accepted by the video stabilization MFT are:</span></span>

-   <span data-ttu-id="44bb5-120">**\_видео MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="44bb5-120">**MEDIATYPE\_VIDEO**</span></span>
-   <span data-ttu-id="44bb5-121">**МЕДИАСУБТИПЕ \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="44bb5-121">**MEDIASUBTYPE\_NV12**</span></span>

<span data-ttu-id="44bb5-122">Входной тип носителя должен быть задан перед выходным типом носителя.</span><span class="sxs-lookup"><span data-stu-id="44bb5-122">The input media type must be set before the output media type.</span></span> <span data-ttu-id="44bb5-123">В большинстве случаев поддержка ограниченного формата не является проблемой, так как конвейер автоматически вставляет необходимые преобразования цветов.</span><span class="sxs-lookup"><span data-stu-id="44bb5-123">In most situations, the limited format support is not an issue because the pipeline automatically inserts the necessary color conversions.</span></span>

<span data-ttu-id="44bb5-124">Компонент Video стабилизации MFT поддерживает динамическое изменение формата при вводе изменений.</span><span class="sxs-lookup"><span data-stu-id="44bb5-124">The video stabilization MFT component is capable of dynamic format change when input changes.</span></span> <span data-ttu-id="44bb5-125">При изменении размера входного рисунка или изменении подтипа он вызывает динамическое изменение формата для выходного потока.</span><span class="sxs-lookup"><span data-stu-id="44bb5-125">When the input picture size changes or the subtype changes, it will trigger a dynamic format change on the output stream.</span></span>

<span data-ttu-id="44bb5-126">Файл MFT Video стабилизации будет выполнять преобразование цветов в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="44bb5-126">The video stabilization MFT will do color conversion in the following cases:</span></span>

-   <span data-ttu-id="44bb5-127">Если входной формат — **медиасубтипе \_ YUY2**.</span><span class="sxs-lookup"><span data-stu-id="44bb5-127">When the input format is **MEDIASUBTYPE\_YUY2**.</span></span>
-   <span data-ttu-id="44bb5-128">При использовании режима совместимости Microsoft DirectX 9,0.</span><span class="sxs-lookup"><span data-stu-id="44bb5-128">When Microsoft DirectX 9.0 compatibility mode is used.</span></span>

### <a name="attributes"></a><span data-ttu-id="44bb5-129">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="44bb5-129">Attributes</span></span>

<span data-ttu-id="44bb5-130">Следующие атрибуты поддерживаются видео стабилизации MFT через интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="44bb5-130">The following attributes are supported by the video stabilization MFT through the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

-   <span data-ttu-id="44bb5-131">Атрибут [MF \_ видеодсп \_ mode](mf-videodsp-mode.md) помещает файл MFT видео стабилизации в режим стабилизации или сквозной режим.</span><span class="sxs-lookup"><span data-stu-id="44bb5-131">The attribute [MF\_VIDEODSP\_MODE](mf-videodsp-mode.md) puts the video stabilization MFT into either stabilization mode or pass-through mode.</span></span> <span data-ttu-id="44bb5-132">Приложение должно вызывать [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) для **типа GUID MF \_ видеодсп \_** с целочисленным значением, соответствующим одному из следующих допустимых значений: **мфвидеодспмоде \_ стабилизации** = 4, **мфвидеодспмоде \_ passthrough** = 1.</span><span class="sxs-lookup"><span data-stu-id="44bb5-132">The application should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on the GUID **MF\_VIDEODSP\_TYPE** with an integer corresponding to one of the following valid values: **MFVideoDSPMode\_Stabilization** = 4, **MFVideoDSPMode\_Passthrough** = 1.</span></span> <span data-ttu-id="44bb5-133">\_Режим ВИДЕОДСП MF \_ можно изменить в любое время во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="44bb5-133">MF\_VIDEODSP\_MODE can be changed at any time during playback.</span></span> <span data-ttu-id="44bb5-134">Это приводит к изменению динамического режима.</span><span class="sxs-lookup"><span data-stu-id="44bb5-134">This causes a dynamic mode change.</span></span> <span data-ttu-id="44bb5-135">После изменения атрибута выходные данные будут переключаться на "стабилизация" или "передать" после 16 или 2 кадров (в зависимости от режима задержки).</span><span class="sxs-lookup"><span data-stu-id="44bb5-135">The output will switch to either stabilized or pass through after either 16 or 2 frames (depending on the latency mode) after the attribute is changed.</span></span>
-   <span data-ttu-id="44bb5-136">Атрибут [MF \_ Low \_ Задержка](mf-low-latency.md) помещает файл MFT видео стабилизации в режим с низкой задержкой или режим высокого качества.</span><span class="sxs-lookup"><span data-stu-id="44bb5-136">The attribute [MF\_LOW\_LATENCY](mf-low-latency.md) puts the video stabilization MFT into either low latency mode or high quality mode.</span></span> <span data-ttu-id="44bb5-137">Приложение должно вызвать [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) для идентификатора GUID **MF с \_ небольшой \_ задержкой** и целым числом, соответствующим одному из следующих допустимых значений: низкая задержка = 1 высокое качество = 0</span><span class="sxs-lookup"><span data-stu-id="44bb5-137">The application should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on the GUID **MF\_LOW\_LATENCY** with an integer corresponding to one of the following valid values: Low latency = 1 High Quality = 0</span></span>
-   <span data-ttu-id="44bb5-138">В конвейере используется атрибут [MF \_ SA \_ D3D11 \_ биндфлагс](mf-sa-d3d11-bindflags.md) для указания флагов привязки D3D11 для создания выходных образцов.</span><span class="sxs-lookup"><span data-stu-id="44bb5-138">The attribute [MF\_SA\_D3D11\_BINDFLAGS](mf-sa-d3d11-bindflags.md) is used by the pipeline to specify the D3D11 bind flags to create the output samples with.</span></span> <span data-ttu-id="44bb5-139">Любое сочетание значений из перечисления [**\_ \_ флагов привязки D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) является допустимым.</span><span class="sxs-lookup"><span data-stu-id="44bb5-139">Any combination of values from the [**D3D11\_BIND\_FLAG**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) enumeration is valid.</span></span>
-   <span data-ttu-id="44bb5-140">Для указания минимального числа выборок, которые компонент должен поддерживать в выходных данных, в конвейере используется атрибут с **\_ \_ минимальным количеством \_ выходных данных \_ \_ SA MF** .</span><span class="sxs-lookup"><span data-stu-id="44bb5-140">The attribute **MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT** is used by the pipeline to specify the minimum number of samples that this component must support on output.</span></span>
-   <span data-ttu-id="44bb5-141">Атрибут [мфсампликстенсион \_ видеодспмоде](mfsampleextension-videodspmode.md) устанавливается в каждом примере, созданном с помощью стабилизации, чтобы указать [действующий \_ \_ режим видеодсп MF](mf-videodsp-mode.md) , примененный к этому примеру (независимо от того, был ли этот пример изменен).</span><span class="sxs-lookup"><span data-stu-id="44bb5-141">The attribute [MFSampleExtension\_VideoDSPMode](mfsampleextension-videodspmode.md) is set on every sample produced by stabilization to indicate the effective [MF\_VIDEODSP\_MODE](mf-videodsp-mode.md) applied to that sample (whether or not the sample was stabilized).</span></span> <span data-ttu-id="44bb5-142">При определенных условиях выборка может быть невозможна (из-за высокой загрузки системы или запросов пользователя).</span><span class="sxs-lookup"><span data-stu-id="44bb5-142">Under certain conditions, samples may not be stabilized (due to high system load, or requests by the user).</span></span> <span data-ttu-id="44bb5-143">Этот атрибут имеет те же значения, что и \_ \_ атрибут режима MF видеодсп Mode (**Мфвидеодспмоде \_ стабилизации** and **мфвидеодспмоде \_ passthrough**).</span><span class="sxs-lookup"><span data-stu-id="44bb5-143">This attribute has the same values as the MF\_VIDEODSP\_MODE attribute (**MFVideoDSPMode\_Stabilization** and **MFVideoDSPMode\_Passthrough**).</span></span> <span data-ttu-id="44bb5-144">Чтобы получить значение этого атрибута, приложения должны вызывать [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) для GUID **мфсампликстенсион \_ видеодспмоде**.</span><span class="sxs-lookup"><span data-stu-id="44bb5-144">To get the value of this attribute applications should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on GUID **MFSampleExtension\_VideoDSPMode**.</span></span>

## <a name="remarks"></a><span data-ttu-id="44bb5-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44bb5-145">Remarks</span></span>

<span data-ttu-id="44bb5-146">Экземпляр поставщика схемы стабилизации видео можно создать одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="44bb5-146">An instance of the video stabilization DSP can be created in one of the following ways:</span></span>

-   <span data-ttu-id="44bb5-147">Путем вызова [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="44bb5-147">By calling [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="44bb5-148">DSP видео стабилизации регистрируется в категории " **\_ \_ \_ видеовоздействие категории MFT** ".</span><span class="sxs-lookup"><span data-stu-id="44bb5-148">The video stabilization DSP is registered under the **MFT\_CATEGORY\_VIDEO\_EFFECT** category.</span></span>
-   <span data-ttu-id="44bb5-149">Вызывая **функцию com** , мы передаем ей CLSID CLSID **\_ кмсвидеодспмфт**.</span><span class="sxs-lookup"><span data-stu-id="44bb5-149">By calling the COM function **CoCreateInstance** passing it the CLSID **CLSID\_CMSVideoDSPMFT**.</span></span> <span data-ttu-id="44bb5-150">Чтобы использовать этот метод, необходимо включить вмкодекдсп. h и связать с вмкодекдспууид. lib.</span><span class="sxs-lookup"><span data-stu-id="44bb5-150">To use this method, you must include wmcodecdsp.h and link against wmcodecdspuuid.lib.</span></span>

<span data-ttu-id="44bb5-151">Кроме того, стабилизации для видео DSP поддерживает создание экземпляров с помощью среда выполнения Windows в качестве расширения Windows Media.</span><span class="sxs-lookup"><span data-stu-id="44bb5-151">Additionally, the video stabilization DSP supports instantiation using Windows Runtime as a Windows Media Extension.</span></span> <span data-ttu-id="44bb5-152">Он определен в [**Windows. Media. видеоеффектс**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041), а его полное имя — "Windows. Media. Видеоеффектс. видеостабилизатион".</span><span class="sxs-lookup"><span data-stu-id="44bb5-152">It is defined on the [**Windows.Media.VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041), and its full name is "Windows.Media.VideoEffects.VideoStabilization".</span></span>

## <a name="requirements"></a><span data-ttu-id="44bb5-153">Требования</span><span class="sxs-lookup"><span data-stu-id="44bb5-153">Requirements</span></span>



| <span data-ttu-id="44bb5-154">Требование</span><span class="sxs-lookup"><span data-stu-id="44bb5-154">Requirement</span></span> | <span data-ttu-id="44bb5-155">Значение</span><span class="sxs-lookup"><span data-stu-id="44bb5-155">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="44bb5-156">Header</span><span class="sxs-lookup"><span data-stu-id="44bb5-156">Header</span></span><br/> | <dl> <span data-ttu-id="44bb5-157"><dt>Камерауиконтрол. h</dt></span><span class="sxs-lookup"><span data-stu-id="44bb5-157"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44bb5-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44bb5-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44bb5-159">Обработчики цифровых сигналов</span><span class="sxs-lookup"><span data-stu-id="44bb5-159">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> <dt>

[<span data-ttu-id="44bb5-160">**Windows.Media.VideoEffects**</span><span class="sxs-lookup"><span data-stu-id="44bb5-160">**Windows.Media.VideoEffects**</span></span>](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)
</dt> </dl>

 

 
