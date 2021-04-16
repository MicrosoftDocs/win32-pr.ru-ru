---
description: Общие сведения о ДКСВА 2 и его связи с ДКСВА 1.
ms.assetid: 190ed399-a8a8-4087-8d18-b1a715690e4c
title: О ДКСВА 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149f622c863f433be44bbce6460024ffb06bb1b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650554"
---
# <a name="about-dxva-20"></a><span data-ttu-id="928d3-103">О ДКСВА 2,0</span><span class="sxs-lookup"><span data-stu-id="928d3-103">About DXVA 2.0</span></span>

<span data-ttu-id="928d3-104">Ускорение видео DirectX (ДКСВА) — это API и соответствующий DDI для использования аппаратного ускорения для ускорения обработки видео.</span><span class="sxs-lookup"><span data-stu-id="928d3-104">DirectX Video Acceleration (DXVA) is an API and a corresponding DDI for using hardware acceleration to speed up video processing.</span></span> <span data-ttu-id="928d3-105">Программные кодеки и видеопроцессоры могут использовать ДКСВА для разгрузки определенных вычислительных операций в GPU.</span><span class="sxs-lookup"><span data-stu-id="928d3-105">Software codecs and software video processors can use DXVA to offload certain CPU-intensive operations to the GPU.</span></span> <span data-ttu-id="928d3-106">Например, программный декодер может разгрузить обратное дискретное преобразование косинуса (идкт) в GPU.</span><span class="sxs-lookup"><span data-stu-id="928d3-106">For example, a software decoder can offload the inverse discrete cosine transform (iDCT) to the GPU.</span></span>

<span data-ttu-id="928d3-107">В ДКСВА некоторые операции декодирования реализуются драйвером графического оборудования.</span><span class="sxs-lookup"><span data-stu-id="928d3-107">In DXVA, some decoding operations are implemented by the graphics hardware driver.</span></span> <span data-ttu-id="928d3-108">Этот набор функций называется *ускорителем*.</span><span class="sxs-lookup"><span data-stu-id="928d3-108">This set of functionality is termed the *accelerator*.</span></span> <span data-ttu-id="928d3-109">Другие операции декодирования реализуются программным обеспечением приложений пользовательского режима, которое называется *декодером узла* или *программным декодером*.</span><span class="sxs-lookup"><span data-stu-id="928d3-109">Other decoding operations are implemented by user-mode application software, called the *host decoder* or *software decoder*.</span></span> <span data-ttu-id="928d3-110">(Термины *основной декодер* и *программный декодер* эквивалентны.) Обработка, выполняемая ускорителем, называется *обработкой за пределами узла*.</span><span class="sxs-lookup"><span data-stu-id="928d3-110">(The terms *host decoder* and *software decoder* are equivalent.) Processing performed by the accelerator is called *off-host processing*.</span></span> <span data-ttu-id="928d3-111">Обычно ускоритель использует GPU для ускорения некоторых операций.</span><span class="sxs-lookup"><span data-stu-id="928d3-111">Typically the accelerator uses the GPU to speed up some operations.</span></span> <span data-ttu-id="928d3-112">Всякий раз, когда ускоритель выполняет операцию декодирования, декодер хоста должен передать в буферы ускорителя, содержащие сведения, необходимые для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="928d3-112">Whenever the accelerator performs a decoding operation, the host decoder must convey to the accelerator buffers containing the information needed to perform the operation</span></span>

<span data-ttu-id="928d3-113">Для работы API ДКСВА 2 требуется Windows Vista или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="928d3-113">The DXVA 2 API requires Windows Vista or later.</span></span> <span data-ttu-id="928d3-114">API ДКСВА 1 по-прежнему поддерживается в Windows Vista для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="928d3-114">The DXVA 1 API is still supported in Windows Vista for backward compatibility.</span></span> <span data-ttu-id="928d3-115">Предоставляется уровень эмуляции, который преобразуется между любой версией API и противоположной версией DDI:</span><span class="sxs-lookup"><span data-stu-id="928d3-115">An emulation layer is provided that converts between either version of the API and the opposite version of the DDI:</span></span>

-   <span data-ttu-id="928d3-116">Если графический драйвер соответствует модели WDDM, вызовы API ДКСВА 1 преобразуются в вызовы DDI ДКСВА 2.</span><span class="sxs-lookup"><span data-stu-id="928d3-116">If the graphics driver conforms to the Windows Display Driver Model (WDDM), DXVA 1 API calls are converted to DXVA 2 DDI calls.</span></span>
-   <span data-ttu-id="928d3-117">Если графические драйверы используют более старую модель драйвера экрана Windows XP (XPDM), вызовы API ДКСВА 2 преобразуются в вызовы DDI ДКСВА 1.</span><span class="sxs-lookup"><span data-stu-id="928d3-117">If the graphics drivers uses the older Windows XP Display Driver Model (XPDM), DXVA 2 API calls are converted to DXVA 1 DDI calls.</span></span>

<span data-ttu-id="928d3-118">В следующей таблице приведены требования к операционной системе и поддерживаемые модули обработки видео для каждой версии API ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="928d3-118">The following table shows the operating system requirements and the supported video renderers for each version of the DXVA API.</span></span>



| <span data-ttu-id="928d3-119">Версия API</span><span class="sxs-lookup"><span data-stu-id="928d3-119">API Version</span></span> | <span data-ttu-id="928d3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="928d3-120">Requirements</span></span>          | <span data-ttu-id="928d3-121">Поддержка модуля подготовки видео</span><span class="sxs-lookup"><span data-stu-id="928d3-121">Video Renderer Support</span></span>                        |
|-------------|-----------------------|-----------------------------------------------|
| <span data-ttu-id="928d3-122">ДКСВА 1</span><span class="sxs-lookup"><span data-stu-id="928d3-122">DXVA 1</span></span>      | <span data-ttu-id="928d3-123">Windows 2000 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="928d3-123">Windows 2000 or later</span></span> | <span data-ttu-id="928d3-124">Микшер наложения, VMR-7, VMR-9 (только DirectShow)</span><span class="sxs-lookup"><span data-stu-id="928d3-124">Overlay Mixer, VMR-7, VMR-9 (DirectShow only)</span></span> |
| <span data-ttu-id="928d3-125">ДКСВА 2</span><span class="sxs-lookup"><span data-stu-id="928d3-125">DXVA 2</span></span>      | <span data-ttu-id="928d3-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="928d3-126">Windows Vista</span></span>         | <span data-ttu-id="928d3-127">Евр (DirectShow и Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="928d3-127">EVR (DirectShow and Media Foundation)</span></span>         |



 

<span data-ttu-id="928d3-128">В ДКСВА 1 программный декодер должен получить доступ к API через модуль подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="928d3-128">In DXVA 1, the software decoder must access the API through the video renderer.</span></span> <span data-ttu-id="928d3-129">Не существует способа использовать API ДКСВА 1 без вызова модуля подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="928d3-129">There is no way to use the DXVA 1 API without calling into the video renderer.</span></span> <span data-ttu-id="928d3-130">Это ограничение было удалено с помощью ДКСВА 2.</span><span class="sxs-lookup"><span data-stu-id="928d3-130">This limitation has been removed with DXVA 2.</span></span> <span data-ttu-id="928d3-131">С помощью ДКСВА 2 декодер узла (или любое приложение) может напрямую обращаться к API через интерфейс [**идиректксвидеодекодерсервице**](/windows/win32/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) .</span><span class="sxs-lookup"><span data-stu-id="928d3-131">Using DXVA 2, the host decoder (or any application) can access the API directly, through the [**IDirectXVideoDecoderService**](/windows/win32/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface.</span></span>

<span data-ttu-id="928d3-132">В документации по ДКСВА 1 описаны структуры декодирования, используемые для следующих стандартов видео:</span><span class="sxs-lookup"><span data-stu-id="928d3-132">The DXVA 1 documentation describes the decoding structures used for the following video standards:</span></span>

-   <span data-ttu-id="928d3-133">ITU-T Rec. H. 261</span><span class="sxs-lookup"><span data-stu-id="928d3-133">ITU-T Rec. H.261</span></span>
-   <span data-ttu-id="928d3-134">ITU-T Rec. H. 263</span><span class="sxs-lookup"><span data-stu-id="928d3-134">ITU-T Rec. H.263</span></span>
-   <span data-ttu-id="928d3-135">Видео MPEG-1</span><span class="sxs-lookup"><span data-stu-id="928d3-135">MPEG-1 video</span></span>
-   <span data-ttu-id="928d3-136">Видео о основном профиле MPEG-2</span><span class="sxs-lookup"><span data-stu-id="928d3-136">MPEG-2 Main Profile video</span></span>

<span data-ttu-id="928d3-137">Следующие спецификации определяют расширения ДКСВА для других стандартов видео:</span><span class="sxs-lookup"><span data-stu-id="928d3-137">The following specifications define DXVA extensions for other video standards:</span></span>

-   [<span data-ttu-id="928d3-138">Спецификация ДКСВА для декодирования H. 264/AVC</span><span class="sxs-lookup"><span data-stu-id="928d3-138">DXVA Specification for H.264/AVC Decoding</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=3d1c290b-310b-4ea2-bf76-714063a6d7a6&displaylang=en)
-   [<span data-ttu-id="928d3-139">Спецификация ДКСВА для H. 264/MPEG-4 AVC с поддержкой кодирования видео (MVC), включая высококачественный стереофонический профиль</span><span class="sxs-lookup"><span data-stu-id="928d3-139">DXVA Specification for H.264/MPEG-4 AVC Multiview Video Coding (MVC), Including the Stereo High Profile</span></span>](https://www.microsoft.com/download/details.aspx?id=25200)
-   <span data-ttu-id="928d3-140">[Спецификация дксва для MPEG-1 ВЛД и Объединенная декодирование видео MPEG-1/MPEG-2 ВЛД](https://www.microsoft.com/download/details.aspx?id=9374).</span><span class="sxs-lookup"><span data-stu-id="928d3-140">[DXVA Specification for MPEG-1 VLD and Combined MPEG-1/MPEG-2 VLD Video Decoding](https://www.microsoft.com/download/details.aspx?id=9374).</span></span>
-   [<span data-ttu-id="928d3-141">Спецификация ДКСВА для режима ВЛД Off-Host для MPEG-4 часть 2. декодирование видео</span><span class="sxs-lookup"><span data-stu-id="928d3-141">DXVA Specification for Off-Host VLD Mode for MPEG-4 Part 2 Video Decoding</span></span>](https://www.microsoft.com/download/details.aspx?id=21100)
-   [<span data-ttu-id="928d3-142">Спецификация ДКСВА для Windows Media Video® V8, V9 и ва декодирования (включая SMPTE 421M "VC-1")</span><span class="sxs-lookup"><span data-stu-id="928d3-142">DXVA Specification for Windows Media Video® v8, v9 and vA Decoding (Including SMPTE 421M "VC-1")</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=8792dfdb-8459-4cb7-adb4-fef30b609b31&displaylang=en)
-   [<span data-ttu-id="928d3-143">Спецификация ускорения видео DirectX (ДКСВА) для H. 264/MPEG-4 масштабируемая видеокодирование (SVC) Off-Host ВЛД режим декодирования</span><span class="sxs-lookup"><span data-stu-id="928d3-143">DirectX Video Acceleration (DXVA) Specification for H.264/MPEG-4 Scalable Video Coding (SVC) Off-Host VLD Mode Decoding</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=a38538b6-f52c-470b-94be-0cf7c28d46cc&displaylang=en)
-   [<span data-ttu-id="928d3-144">Спецификация ускорения видео DirectX для кодирования видео VP8 и VP9</span><span class="sxs-lookup"><span data-stu-id="928d3-144">DirectX Video Acceleration Specification for VP8 and VP9 Video Coding</span></span>](https://www.microsoft.com/download/details.aspx?id=49188)

<span data-ttu-id="928d3-145">ДКСВА 1 и ДКСВА 2 используют одни и те же структуры данных для декодирования.</span><span class="sxs-lookup"><span data-stu-id="928d3-145">DXVA 1 and DXVA 2 use the same data structures for decoding.</span></span> <span data-ttu-id="928d3-146">Однако процедура настройки сеанса декодирования изменилась.</span><span class="sxs-lookup"><span data-stu-id="928d3-146">However, the procedure for configuring the decoding session has changed.</span></span> <span data-ttu-id="928d3-147">ДКСВА 1 использует механизм проверки и блокировки, где декодер хоста может проверить различные конфигурации, прежде чем задавать нужную конфигурацию в ускорителе.</span><span class="sxs-lookup"><span data-stu-id="928d3-147">DXVA 1 uses a "probe and lock" mechanism, wherein the host decoder can test various configurations before setting the desired configuration on the accelerator.</span></span> <span data-ttu-id="928d3-148">В ДКСВА 2 ускоритель возвращает список поддерживаемых конфигураций, и декодер хоста выбирает его из списка.</span><span class="sxs-lookup"><span data-stu-id="928d3-148">In DXVA 2, the accelerator returns a list of supported configurations and the host decoder selects one from the list.</span></span> <span data-ttu-id="928d3-149">Дополнительные сведения приведены в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="928d3-149">Details are given in the following sections:</span></span>

-   [<span data-ttu-id="928d3-150">Поддержка ДКСВА 2,0 в DirectShow</span><span class="sxs-lookup"><span data-stu-id="928d3-150">Supporting DXVA 2.0 in DirectShow</span></span>](supporting-dxva-2-0-in-directshow.md)
-   [<span data-ttu-id="928d3-151">Поддержка ДКСВА 2,0 в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="928d3-151">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)

## <a name="related-topics"></a><span data-ttu-id="928d3-152">См. также</span><span class="sxs-lookup"><span data-stu-id="928d3-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="928d3-153">Ускорение видео DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="928d3-153">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="928d3-154">Спецификация ДКСВА 1,0</span><span class="sxs-lookup"><span data-stu-id="928d3-154">DXVA 1.0 specification</span></span>](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
