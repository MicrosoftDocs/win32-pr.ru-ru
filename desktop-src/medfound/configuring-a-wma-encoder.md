---
description: Задание типа выходных данных для кодировщика WMA
ms.assetid: 0a1a22bb-460f-4ac2-be76-4249997441de
title: Задание типа выходных данных для кодировщика WMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c6b078dc2426b062a90f706c5d113960f54ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143219"
---
# <a name="setting-an-output-type-for-a-wma-encoder"></a><span data-ttu-id="3ecae-103">Задание типа выходных данных для кодировщика WMA</span><span class="sxs-lookup"><span data-stu-id="3ecae-103">Setting an Output Type for a WMA Encoder</span></span>

<span data-ttu-id="3ecae-104">Чтобы создать допустимый тип выходных данных для кодировщика Windows Media Audio (WMA), необходимо иметь следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="3ecae-104">To create a valid output type for a Windows Media Audio (WMA) encoder, you must have the following information:</span></span>

-   <span data-ttu-id="3ecae-105">Подтип Audio, репесентс закодированный формат WMA.</span><span class="sxs-lookup"><span data-stu-id="3ecae-105">The audio subtype that repesents the encoded WMA format.</span></span> <span data-ttu-id="3ecae-106">См. раздел [идентификаторы GUID для звуковых подтипов](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="3ecae-106">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>
-   <span data-ttu-id="3ecae-107">Свойства конфигурации, заданные для кодировщика.</span><span class="sxs-lookup"><span data-stu-id="3ecae-107">The configuration properties to set on the encoder.</span></span>

    <span data-ttu-id="3ecae-108">Свойства конфигурации описаны в документации по API-интерфейсам аудио-и видеокодеков Windows Media и DSP.</span><span class="sxs-lookup"><span data-stu-id="3ecae-108">The configuration properties are documented in the Windows Media Audio and Video Codec and DSP APIs documentation.</span></span> <span data-ttu-id="3ecae-109">Дополнительные сведения см. в разделе "свойства аудиопотока в [свойствах кодировки](configuring-the-encoder.md)".</span><span class="sxs-lookup"><span data-stu-id="3ecae-109">For more information, see "Audio Stream Properties" in [Encoding Properties](configuring-the-encoder.md).</span></span>

### <a name="windows-vista-or-later"></a><span data-ttu-id="3ecae-110">Windows Vista или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="3ecae-110">Windows Vista or Later</span></span>

<span data-ttu-id="3ecae-111">Чтобы получить допустимый тип выходных данных для кодировщика, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3ecae-111">To get a valid output type for the encoder, perform the following steps.</span></span>

1.  <span data-ttu-id="3ecae-112">Используйте функцию [**мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) или [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) для создания экземпляра кодировщика.</span><span class="sxs-lookup"><span data-stu-id="3ecae-112">Use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function to create an instance of the encoder.</span></span>
2.  <span data-ttu-id="3ecae-113">Запросите кодировщик для интерфейса **ипропертисторе** .</span><span class="sxs-lookup"><span data-stu-id="3ecae-113">Query the encoder for the **IPropertyStore** interface.</span></span>
3.  <span data-ttu-id="3ecae-114">Используйте интерфейс **ипропертисторе** для настройки кодировщика.</span><span class="sxs-lookup"><span data-stu-id="3ecae-114">Use the **IPropertyStore** interface to configure the encoder.</span></span>
4.  <span data-ttu-id="3ecae-115">Получите Поддерживаемые типы выходных данных, вызвав [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) в цикле до тех пор, пока кодировщик **не возвратит MF \_ E больше \_ \_ \_ типов** и вы выбираете тип целевого носителя.</span><span class="sxs-lookup"><span data-stu-id="3ecae-115">Retrieve the supported output types by calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) in a loop until the encoder returns **MF\_E\_NO\_MORE\_TYPES** and you choose the target media type.</span></span> <span data-ttu-id="3ecae-116">I</span><span class="sxs-lookup"><span data-stu-id="3ecae-116">I</span></span>
5.  <span data-ttu-id="3ecae-117">Вызовите [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , чтобы задать тип сжатия мультимедиа для кодировщика.</span><span class="sxs-lookup"><span data-stu-id="3ecae-117">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

### <a name="windows-7"></a><span data-ttu-id="3ecae-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3ecae-118">Windows 7</span></span>

<span data-ttu-id="3ecae-119">Чтобы получить допустимый тип выходных данных кодировщика в Windows 7, Media Foundation предоставляет функцию [**мфтранскодежетаудиуутпутаваилаблетипес**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) .</span><span class="sxs-lookup"><span data-stu-id="3ecae-119">To get a valid output type for the encoder in Windows 7, Media Foundation provides the [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) function.</span></span> <span data-ttu-id="3ecae-120">Приложение должно пройти обязательное аудио подтип, репесентс закодированный WMA и свойства кодировки.</span><span class="sxs-lookup"><span data-stu-id="3ecae-120">An application must pass required the audio subtype that repesents the encoded WMA and the encoding properties.</span></span> <span data-ttu-id="3ecae-121">Свойства являются обязательными, так как кодировщик изменяет Поддерживаемые типы вывода в зависимости от набора режимов.</span><span class="sxs-lookup"><span data-stu-id="3ecae-121">The properties are required because the encoder changes the supported output types depending upon the mode set.</span></span>

> [!Note]  
> <span data-ttu-id="3ecae-122">[**Мфтранскодежетаудиуутпутаваилаблетипес**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)поддерживается только для [кодирования с постоянной скоростью потока](constant-bit-rate-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="3ecae-122">[**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)is only supported for [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span>

 

<span data-ttu-id="3ecae-123">Если вызов будет выполнен, приложение получит список указателей IUnknown поддерживаемых типов выходных данных в объекте [**имфколлектион**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) .</span><span class="sxs-lookup"><span data-stu-id="3ecae-123">If the call succeeds, the application receives a list of IUnknown pointers of the supported output media types in an [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) object.</span></span> <span data-ttu-id="3ecae-124">Чтобы задать тип выходного носителя, найдите тот, который соответствует типу целевого объекта, и вызовите [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , чтобы задать тип мультимедиа сжатия в кодировщике.</span><span class="sxs-lookup"><span data-stu-id="3ecae-124">To set the output media type, find the one that matches your target type and call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ecae-125">См. также</span><span class="sxs-lookup"><span data-stu-id="3ecae-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ecae-126">Создание экземпляра MFT для кодировщика</span><span class="sxs-lookup"><span data-stu-id="3ecae-126">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="3ecae-127">Кодировщики Windows Media</span><span class="sxs-lookup"><span data-stu-id="3ecae-127">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



