---
title: Обнаружение возможностей форматирования устройств
description: Обнаружение возможностей форматирования устройств
ms.assetid: dd139816-dc8c-4e73-9a21-67287bfe6405
keywords:
- Диспетчер устройств Windows Media, возможности устройств
- Диспетчер устройств, возможности устройства
- рекомендации по программированию, возможности устройств
- Классические приложения, возможности устройств
- Создание приложений диспетчер устройств Windows Media, возможности устройств
- запись файлов на устройства, возможности устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0ee05476f6b84bc85bb81cc7cff5815649f5842
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691181"
---
# <a name="discovering-device-format-capabilities"></a><span data-ttu-id="3986e-109">Обнаружение возможностей форматирования устройств</span><span class="sxs-lookup"><span data-stu-id="3986e-109">Discovering Device Format Capabilities</span></span>

<span data-ttu-id="3986e-110">Приложение может попытаться определить возможности воспроизведения устройства перед отправкой файла.</span><span class="sxs-lookup"><span data-stu-id="3986e-110">Your application might try to determine a device's playback capabilities before sending a file to it.</span></span> <span data-ttu-id="3986e-111">Если устройство не может работать с форматом файла, который требуется отправить, приложение может попытаться перекодировать файл в формат, который может использовать устройство, или уведомить пользователя о том, что устройство не поддерживает запрошенный файл.</span><span class="sxs-lookup"><span data-stu-id="3986e-111">If a device cannot handle the format of a file you want to send, your application might attempt to transcode the file into a format that the device can use, or notify the user that the device cannot support the requested file.</span></span>

<span data-ttu-id="3986e-112">Обратите внимание, что некоторые устройства, такие как устройства класса запоминающих устройств, могут использоваться только как съемные носители носителей без возможности воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="3986e-112">Note that some devices, such as mass storage class devices, might serve only as removable storage media without playback capabilities.</span></span> <span data-ttu-id="3986e-113">В этом случае было бы нежелательным для приложения перекодировать файл перед его отправкой на устройство.</span><span class="sxs-lookup"><span data-stu-id="3986e-113">In this case, it would be inappropriate for your application to transcode a file before sending it to the device.</span></span>

<span data-ttu-id="3986e-114">Хотя метод [**ивмдмдевице:: GetType**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-gettype) позволяет устройству сообщать о своих возможностях, некоторые устройства возвращают неверные значения для этого метода.</span><span class="sxs-lookup"><span data-stu-id="3986e-114">Although the [**IWMDMDevice::GetType**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-gettype) method enables a device to report its capabilities, some devices return incorrect values for this method.</span></span> <span data-ttu-id="3986e-115">Перед копированием файла на устройство может потребоваться попросить пользователя о том, предназначено ли воспроизведение, и, если да, попытаться перекодировать файл в один из зарегистрированных форматов устройства (или в разумном формате, если устройство поддерживает утверждения любого формата).</span><span class="sxs-lookup"><span data-stu-id="3986e-115">Before copying a file to a device, you might want to ask the user whether playback is intended, and if so, attempt to transcode the file to one of the device's reported formats (or a reasonable format, if the device claims support for any format).</span></span> <span data-ttu-id="3986e-116">Другой подход заключается в том, что все форматы, специально перечисленные как поддерживаемые устройством, предназначены для воспроизведения, а все остальные файлы должны передаваться без изменений.</span><span class="sxs-lookup"><span data-stu-id="3986e-116">Another approach is to assume that any formats specifically listed as supported by the device are intended for playback, and all other files should be transferred unmodified.</span></span>

<span data-ttu-id="3986e-117">После обнаружения формата переносимого файла и форматов, поддерживаемых устройством, можно выбрать оптимальный формат целевого объекта для перекодирования.</span><span class="sxs-lookup"><span data-stu-id="3986e-117">After discovering the format of the file to be transferred, and the formats supported by a device, you can decide which is the best target format for transcoding.</span></span>

<span data-ttu-id="3986e-118">В прошлом было распространено, что приложение возвращало ноль для свойства, чтобы указать поддержку любых значений этого свойства.</span><span class="sxs-lookup"><span data-stu-id="3986e-118">In the past, it was common for an application to return zero for a property to indicate support for any values of that property.</span></span> <span data-ttu-id="3986e-119">Например, нулевое значение для [**\_ вавеформатекс**](-waveformatex.md). нсамплесперсек указывает на поддержку любой скорости.</span><span class="sxs-lookup"><span data-stu-id="3986e-119">For example, a value of zero for [**\_WAVEFORMATEX**](-waveformatex.md).nSamplesPerSec would indicate support for any bit rate.</span></span> <span data-ttu-id="3986e-120">Теперь рекомендуемым способом указания поддержки любого значения является указание ВМДМ \_ Enum \_ prop \_ Допустимые \_ значения \_ any в [**вмдм \_ prop \_ DESC**](wmdm-prop-desc.md). Валидвалуесформ.</span><span class="sxs-lookup"><span data-stu-id="3986e-120">Now, the recommended way to indicate support for any value is to specify WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY in [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md).ValidValuesForm.</span></span> <span data-ttu-id="3986e-121">Однако некоторые свойства могут вернуть ноль, чтобы указать конкретную поддержку.</span><span class="sxs-lookup"><span data-stu-id="3986e-121">Some properties, though, can legitimately return zero to indicate specific support.</span></span> <span data-ttu-id="3986e-122">Например, если [**\_ битмапинфохеадер**](-bitmapinfoheader.md). бисизеимаже имеет значение 0, это указывает на битовую карту RGB для бизнес-аналитики \_ .</span><span class="sxs-lookup"><span data-stu-id="3986e-122">For example, if [**\_BITMAPINFOHEADER**](-bitmapinfoheader.md).biSizeImage is set to zero, this indicates a BI\_RGB bitmap.</span></span> <span data-ttu-id="3986e-123">Исключения для нулевых значений указаны в документации по соответствующим структурам.</span><span class="sxs-lookup"><span data-stu-id="3986e-123">Exceptions for zero values are noted in the documentation for the relevant structures.</span></span>

<span data-ttu-id="3986e-124">Однако важно отметить, что устройства часто не сообщают о своих возможностях формата или в стандартном виде.</span><span class="sxs-lookup"><span data-stu-id="3986e-124">However, it is important to note that devices often do not report their format capabilities properly, or in a standard way.</span></span> <span data-ttu-id="3986e-125">Например, устройства часто сообщают о том, что они поддерживают любой формат, когда на самом деле они могут работать только с конкретными форматами или с конкретными скоростями в формате формата.</span><span class="sxs-lookup"><span data-stu-id="3986e-125">For example, devices often report that they support any format, when in fact they can only handle specific formats, or specific bit rates within a format type.</span></span> <span data-ttu-id="3986e-126">Вы решаете, должно ли приложение принимать такие отчеты или должен ли он иметь некоторый верхний предел для возможностей воспроизведения устройства (например, 192 кбит/с).</span><span class="sxs-lookup"><span data-stu-id="3986e-126">It is up to you to decide whether your application should accept such reports, or whether it should assume some kind of upper limit to a device's playback abilities (for example, 192 kbps).</span></span>

<span data-ttu-id="3986e-127">Рекомендуемый способ запроса поддержки формата устройства — [**IWMDMDevice3:: жетформаткапабилити**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span><span class="sxs-lookup"><span data-stu-id="3986e-127">The recommended method for requesting a device's format support is [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span></span> <span data-ttu-id="3986e-128">Если этот метод не поддерживается, приложение должно возвращаться к [**ивмдмдевице:: жетформатсуппорт**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport).</span><span class="sxs-lookup"><span data-stu-id="3986e-128">If this method is not supported, your application should fall back on [**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport).</span></span> <span data-ttu-id="3986e-129">**Жетформатсуппорт**, в отличие от **GetFormatSupport2**, не возвращает сведения о видео.</span><span class="sxs-lookup"><span data-stu-id="3986e-129">**GetFormatSupport**, unlike **GetFormatSupport2**, does not return video information.</span></span>

<span data-ttu-id="3986e-130">Как приложение запрашивает возможности форматирования устройства, зависит от того, какой интерфейс поддерживает приложение.</span><span class="sxs-lookup"><span data-stu-id="3986e-130">How an application requests a device's format capabilities depends on which interface the application supports.</span></span> <span data-ttu-id="3986e-131">Дополнительные сведения см в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="3986e-131">For more details, see the following topics:</span></span>

-   [<span data-ttu-id="3986e-132">Получение возможностей форматирования на устройствах, поддерживающих IWMDMDevice3</span><span class="sxs-lookup"><span data-stu-id="3986e-132">Getting Format Capabilities on Devices That Support IWMDMDevice3</span></span>](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
-   [<span data-ttu-id="3986e-133">Получение возможностей форматирования на устройствах, поддерживающих только Ивмдмдевице</span><span class="sxs-lookup"><span data-stu-id="3986e-133">Getting Format Capabilities on Devices That Support Only IWMDMDevice</span></span>](getting-format-capabilities-on-devices-that-support-only-iwmdmdevice.md)

## <a name="related-topics"></a><span data-ttu-id="3986e-134">См. также</span><span class="sxs-lookup"><span data-stu-id="3986e-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3986e-135">**Запись файлов на устройство**</span><span class="sxs-lookup"><span data-stu-id="3986e-135">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




