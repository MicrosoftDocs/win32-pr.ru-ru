---
description: Преобразования препроцессора для декодера MPEG
ms.assetid: c7ae0137-0d02-46da-9532-738d805e327d
title: Преобразования препроцессора для декодера MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d7bcf8eeda8062606ce0046a55e34d3c2d90fe
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908902"
---
# <a name="mpeg-decoder-preprocessing-transformations"></a><span data-ttu-id="219af-103">Преобразования препроцессора для декодера MPEG</span><span class="sxs-lookup"><span data-stu-id="219af-103">MPEG Decoder Preprocessing Transformations</span></span>

<span data-ttu-id="219af-104">**Леттербокс и Панскан**</span><span class="sxs-lookup"><span data-stu-id="219af-104">**Letterbox and PanScan**</span></span>

<span data-ttu-id="219af-105">Изображение 4x3 можно формировать с помощью заполнения верхнего и нижнего края изображения (называемого изображением Леттербокс) или путем извлечения 4x3 части изображения (называемой Панскан изображением).</span><span class="sxs-lookup"><span data-stu-id="219af-105">The 4x3 image can be formed by either padding the top and bottom of the image (referred to as a Letterbox image) or by extracting a 4x3 portion of the image (referred to as a PanScan image).</span></span> <span data-ttu-id="219af-106">Меню и потоки подизображений перемещаются поверх конечного изображения видео.</span><span class="sxs-lookup"><span data-stu-id="219af-106">The menus and subpicture streams are overlaid on top of the final video image.</span></span> <span data-ttu-id="219af-107">Изображения соотношения 16x9 хранятся в формате 4x3 анаморфик.</span><span class="sxs-lookup"><span data-stu-id="219af-107">The 16x9 ratio images are stored in a 4x3 anamorphic format.</span></span> <span data-ttu-id="219af-108">Растягивание пропорций анаморфик 4x3 с исходным видео на 16x9 пропорции образуют исходное изображение 16x9.</span><span class="sxs-lookup"><span data-stu-id="219af-108">Stretching the anamorphic 4x3 aspect ratio 720x480 source video to a 16x9 aspect ratio forms the original 16x9 aspect image.</span></span>

<span data-ttu-id="219af-109">Ниже приведено описание того, как правильно отобразить каждый из режимов и их выделение:</span><span class="sxs-lookup"><span data-stu-id="219af-109">Below is a description of how to correctly display each of the modes and their highlights:</span></span>

-   <span data-ttu-id="219af-110">**Широкий экран:** Исходное видео было растянуто в самой крупной области 16x9 окна вывода.</span><span class="sxs-lookup"><span data-stu-id="219af-110">**Widescreen:** The source video stretched into the largest 16x9 area of the output window.</span></span> <span data-ttu-id="219af-111">Основные особенности находятся относительно внутренней области 16x9.</span><span class="sxs-lookup"><span data-stu-id="219af-111">The highlights are relative to the inside of the 16x9 area.</span></span> <span data-ttu-id="219af-112">Черные полосы следует добавлять к верхней и нижней сторонам, чтобы поддерживать 16x9 область.</span><span class="sxs-lookup"><span data-stu-id="219af-112">Black bars should be added to either the top and bottom or to the sides to maintain a 16x9 area.</span></span>
-   <span data-ttu-id="219af-113">**Просмотр панорамы:** В видео 16x9 используйте горизонтальное смещение, предоставленное в потоке MPEG2, для извлечения подокна 4x3.</span><span class="sxs-lookup"><span data-stu-id="219af-113">**Pan Scan:** From the 16x9 video, use the horizontal offset provided in the MPEG2 stream to extract a 4x3 subwindow.</span></span> <span data-ttu-id="219af-114">Поместите подокно 4x3 в самую крупную область 4x3 окна выходного клиента.</span><span class="sxs-lookup"><span data-stu-id="219af-114">Place the 4x3 subwindow into the largest 4x3 area of the output client window.</span></span> <span data-ttu-id="219af-115">Координаты выделения задаются относительно окна вывода 4x3 и не имеют связи с исходным видео 16x9.</span><span class="sxs-lookup"><span data-stu-id="219af-115">The highlight's coordinates are relative to the 4x3 output window and have no relationship to the source 16x9 video.</span></span> <span data-ttu-id="219af-116">Черные полосы следует добавлять к верхней и нижней сторонам, чтобы поддерживать 4x3 область.</span><span class="sxs-lookup"><span data-stu-id="219af-116">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span>
-   <span data-ttu-id="219af-117">**Леттербокс:** Вычислите наиболее крупную 4x3 область окна вывода.</span><span class="sxs-lookup"><span data-stu-id="219af-117">**Letterbox:** Compute the largest 4x3 area of the output window.</span></span> <span data-ttu-id="219af-118">Черные полосы следует добавлять к верхней и нижней сторонам, чтобы поддерживать 4x3 область.</span><span class="sxs-lookup"><span data-stu-id="219af-118">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span> <span data-ttu-id="219af-119">Исходное анаморфик 4x3 видео (представляющее образ 16x9) помещается в самый крупный подокно 16x9 в области 4x3.</span><span class="sxs-lookup"><span data-stu-id="219af-119">The source anamorphic 4x3 video (representing a 16x9 image) is placed in the largest 16x9 subwindow inside of the 4x3 area.</span></span> <span data-ttu-id="219af-120">Черные полосы должны быть добавлены в верхнюю и нижнюю часть подокна, чтобы поддерживать 16x9 область.</span><span class="sxs-lookup"><span data-stu-id="219af-120">Black bars should be added to the top and bottom of the subwindow to maintain a 16x9 area.</span></span> <span data-ttu-id="219af-121">Координаты выделения задаются относительно области 4x3 и не имеют связи с исходным видео 16x9.</span><span class="sxs-lookup"><span data-stu-id="219af-121">The highlight's coordinates are relative to the 4x3 area and have no relationship to the source 16x9 video.</span></span> <span data-ttu-id="219af-122">Диск может определять выделение, которое находится за пределами области 16x9 (но остается в окне 4x3).</span><span class="sxs-lookup"><span data-stu-id="219af-122">It is possible for a disk to specify a highlight that lies outside of the 16x9 area (but still in the 4x3 window).</span></span> <span data-ttu-id="219af-123">Для видео 4x3 видео помещается в самую большую область вывода 4x3 в окне выходного клиента.</span><span class="sxs-lookup"><span data-stu-id="219af-123">For 4x3 video, the video is placed in the largest 4x3 output area of the output client window.</span></span> <span data-ttu-id="219af-124">Черные полосы следует добавлять к верхней и нижней сторонам, чтобы поддерживать 4x3 область.</span><span class="sxs-lookup"><span data-stu-id="219af-124">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span>

<span data-ttu-id="219af-125">**Предварительная обработка MPEG с помощью навигатора по DVD и VMR**</span><span class="sxs-lookup"><span data-stu-id="219af-125">**MPEG preprocessing with the DVD Navigator and VMR**</span></span>

<span data-ttu-id="219af-126">В настоящее время декодеру передается \_ \_ тип видеоматериала формата MPEG2 (чей блок форматирования указывает на структуру [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) ).</span><span class="sxs-lookup"><span data-stu-id="219af-126">Currently, the decoder is passed a FORMAT\_MPEG2\_VIDEO media type (whose format block points to a [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure).</span></span> <span data-ttu-id="219af-127">На выходных закреплениях декодер создает \_ тип мультимедиа VIDEOINFO2 формата, блок формата которого указывает на структуру [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="219af-127">On the output pins, the decoder produces a FORMAT\_VideoInfo2 media type, whose format block points to a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure.</span></span> <span data-ttu-id="219af-128">Поле **двресервед** структуры было переименовано в флаги **двконтролс** .</span><span class="sxs-lookup"><span data-stu-id="219af-128">The structure's **dwReserved** field has been renamed to **dwControls** flags.</span></span>

<span data-ttu-id="219af-129">Теперь элемент **двконтролфлагс** будет содержать новые биты.</span><span class="sxs-lookup"><span data-stu-id="219af-129">The **dwControlFlags** member will now contain the new bits.</span></span>



| <span data-ttu-id="219af-130">Метка</span><span class="sxs-lookup"><span data-stu-id="219af-130">Label</span></span> | <span data-ttu-id="219af-131">Значение</span><span class="sxs-lookup"><span data-stu-id="219af-131">Value</span></span> |
|--------------------------|------------|
| <span data-ttu-id="219af-132">\_используется амконтрол</span><span class="sxs-lookup"><span data-stu-id="219af-132">AMCONTROL\_USED</span></span>          | <span data-ttu-id="219af-133">0x00000001</span><span class="sxs-lookup"><span data-stu-id="219af-133">0x00000001</span></span> |
| <span data-ttu-id="219af-134">АМКОНТРОЛ \_ Pad \_ на \_ 4x3</span><span class="sxs-lookup"><span data-stu-id="219af-134">AMCONTROL\_PAD\_TO\_4x3</span></span>  | <span data-ttu-id="219af-135">0x00000002</span><span class="sxs-lookup"><span data-stu-id="219af-135">0x00000002</span></span> |
| <span data-ttu-id="219af-136">АМКОНТРОЛ \_ Pad \_ на \_ 16x9</span><span class="sxs-lookup"><span data-stu-id="219af-136">AMCONTROL\_PAD\_TO\_16x9</span></span> | <span data-ttu-id="219af-137">0x00000004</span><span class="sxs-lookup"><span data-stu-id="219af-137">0x00000004</span></span> |



 

<span data-ttu-id="219af-138">АМКОНТРОЛ используется \_ для проверки того, поддерживаются ли эти новые флаги.</span><span class="sxs-lookup"><span data-stu-id="219af-138">AMCONTROL\_USED is used to test whether these new flags are supported.</span></span> <span data-ttu-id="219af-139">Фильтр источника должен установить \_ флаг амконтрол и проверить успешность куерякцепт (MediaType) в нисходящем ПИН-коде.</span><span class="sxs-lookup"><span data-stu-id="219af-139">A source filter should set the AMCONTROL\_USED flag and see if QueryAccept(MediaType) succeeds on the downstream pin.</span></span> <span data-ttu-id="219af-140">Если он отклонен, то нельзя использовать флаги АМКОНТРОЛ, и dwReserved1 должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="219af-140">If it is rejected, then the AMCONTROL flags cannot be used and dwReserved1 must be set to 0.</span></span>

<span data-ttu-id="219af-141">АМКОНТРОЛ \_ панель \_ \_ 4x3 указывает, что изображение должно быть заполнено и отображено в области 4x3.</span><span class="sxs-lookup"><span data-stu-id="219af-141">AMCONTROL\_PAD\_TO\_4x3 indicates that the image should be padded and displayed in a 4x3 area.</span></span>

<span data-ttu-id="219af-142">АМКОНТРОЛ \_ панель \_ \_ 16x9 указывает, что изображение должно быть заполнено и отображено в области 16x9.</span><span class="sxs-lookup"><span data-stu-id="219af-142">AMCONTROL\_PAD\_TO\_16x9 indicates that the image should be padded and displayed in a 16x9 area.</span></span>

<span data-ttu-id="219af-143">Декодер должен либо самостоятельно копировать, либо обрабатывать биты.</span><span class="sxs-lookup"><span data-stu-id="219af-143">The decoder should either blindly copy or process the bits.</span></span> <span data-ttu-id="219af-144">Если декодер самостоятельно выполняет пустых, он должен изменить пропорцию пикселя, заполнить изображение и удалить соответствующие \_ \* биты амконтрол.</span><span class="sxs-lookup"><span data-stu-id="219af-144">If the decoder performs letterboxing itself, then it must alter the pixel aspect ratio, pad the image and remove the corresponding AMCONTROL\_\* bits.</span></span>

<span data-ttu-id="219af-145">MPEG2VIDEOINFO. dwFlags теперь содержит три флага для управления отображением содержимого:</span><span class="sxs-lookup"><span data-stu-id="219af-145">The MPEG2VIDEOINFO.dwFlags now contains three flags for controlling for controlling how the content should be displayed:</span></span>

-   <span data-ttu-id="219af-146">`AMMPEG2_DoPanScan (0x00000001)`. Если этот флаг установлен, декодер видео MPEG-2 должен обрезать выходное изображение на основе векторов панорамного просмотра в расширении изображения \_ \_ и изменить пропорции рисунка на 4x3.</span><span class="sxs-lookup"><span data-stu-id="219af-146">`AMMPEG2_DoPanScan (0x00000001)`: If this flag is set, the MPEG-2 video decoder should crop the output image based on pan-scan vectors in picture\_display\_extension and change the picture aspect ratio to 4x3.</span></span> <span data-ttu-id="219af-147">VMR не должен получить пример 16x9 с этим флагом.</span><span class="sxs-lookup"><span data-stu-id="219af-147">The VMR should not receive a 16x9 sample with this flag.</span></span> <span data-ttu-id="219af-148">Простая реализация может изменить исходный прямоугольник, чтобы указать на ширину в 540-е регионе источника с левой границей, равной смещению отображения \_ в \_ расширении изображения.</span><span class="sxs-lookup"><span data-stu-id="219af-148">A simple implementation might alter the source rectangle to indicate a 540 wide source region with a left edge equal to the display offset in the picture\_display\_extension.</span></span>
-   <span data-ttu-id="219af-149">`AMMPEG2_LetterboxAnalogOut (0x00000020)`. Когда аппаратный декодер отображает этот поток на выходе видео (обычно это соединитель СВИДЕО на карте), он должен применить правила для отображения образца 16x9 на экране 4x3.</span><span class="sxs-lookup"><span data-stu-id="219af-149">`AMMPEG2_LetterboxAnalogOut (0x00000020)`: When a hardware decoder displays this stream to a video output (usually an SVIDEO connector on the card), it should apply the rules for displaying a 16x9 sample on a 4x3 display.</span></span>

    <span data-ttu-id="219af-150">Программный декодер (или аппаратный декодер, создающий данные, отправляемые в VMR) имеет два варианта обработки изображений:</span><span class="sxs-lookup"><span data-stu-id="219af-150">A software decoder (or a hardware decoder producing output sent to the VMR) has two options when processing images:</span></span>

    1.  <span data-ttu-id="219af-151">Проигнорируйте этот флаг и передайте содержимое VideoInfoHeader2 в VMR (АМКОНТРОЛ \_ Pad \_ to \_ 4x3 будет уже установлен в качестве образца [DVD-навигатора](dvd-navigator-filter.md) в образце).</span><span class="sxs-lookup"><span data-stu-id="219af-151">Ignore this flag and pass the VideoInfoHeader2 contents to the VMR (the AMCONTROL\_PAD\_TO\_4x3 flag will already be set by the [DVD Navigator](dvd-navigator-filter.md) on the sample).</span></span> <span data-ttu-id="219af-152">Фильтр VMR получит пример видео 16x9 с \_ панелью амконтрол \_ в \_ набор флагов 4x3 и поток 4x3 субтитров.</span><span class="sxs-lookup"><span data-stu-id="219af-152">The VMR will encounter a 16x9 video sample with the AMCONTROL\_PAD\_TO\_4x3 flag set and a 4x3 subpicture stream.</span></span> <span data-ttu-id="219af-153">Приложение должно установить одинаковую ширину выходных нормализованных конечных прямоугольников для двух потоков.</span><span class="sxs-lookup"><span data-stu-id="219af-153">The application must set the output normalized destination rectangles of the two streams to be the same width.</span></span>
    2.  <span data-ttu-id="219af-154">Преобразуйте поток анаморфик в изображение 4x3, добавив отступы в верхнюю и нижнюю часть изображения и установив пропорции изображения в 4x3 (см. Леттербокс выше) и удалив АМКОНТРОЛ \_ Pad \_ в \_ 4X3 бит из VIDEOINFOHEADER2.</span><span class="sxs-lookup"><span data-stu-id="219af-154">Convert the anamorphic stream to a 4x3 image by padding the top and bottom of the image and setting the image aspect ratio to 4x3 (see Letterbox above) and removing the AMCONTROL\_PAD\_TO\_4x3 bit from the VIDEOINFOHEADER2.</span></span>

    <span data-ttu-id="219af-155">Декодеры Директксва, которые накладывают потоки видео и субтитров, должны будут обрабатывать этот флаг.</span><span class="sxs-lookup"><span data-stu-id="219af-155">DirectXVA decoders that blend the video and subpicture streams will have to process this flag.</span></span> <span data-ttu-id="219af-156">Если оборудование не может масштабировать накладываемое подизображение, то декодер должен создать отдельный поток субтитров для того, чтобы смешать с видео.</span><span class="sxs-lookup"><span data-stu-id="219af-156">If the hardware cannot scale the blended subpicture, then the decoder should produce a separate subpicture stream for the VMR to blend with the video.</span></span>

-   <span data-ttu-id="219af-157">`AMMPEG2_WidescreenAnalogOut (0x00000200)`. Когда аппаратный декодер отображает этот поток на выходе видео (обычно это соединитель СВИДЕО на карте), он должен иметь 16x9 (анаморфик).</span><span class="sxs-lookup"><span data-stu-id="219af-157">`AMMPEG2_WidescreenAnalogOut (0x00000200)`: When a hardware decoder displays this stream to a video output (usually an SVIDEO connector on the card), it should assume a 16x9 (anamorphic) display.</span></span>

    <span data-ttu-id="219af-158">Программный декодер (или аппаратный декодер, создающий данные, отправляемые на VMR) имеет два варианта обработки образа анаморфик:</span><span class="sxs-lookup"><span data-stu-id="219af-158">A software decoder (or a hardware decoder producing output sent to the VMR) has two options when processing an anamorphic image:</span></span>

    1.  <span data-ttu-id="219af-159">Пропустите этот флаг и скопируйте содержимое VideoInfoHeader2 в VMR.</span><span class="sxs-lookup"><span data-stu-id="219af-159">Ignore this flag and copy the VideoInfoHeader2 contents to the VMR.</span></span> <span data-ttu-id="219af-160">Фильтр VMR будет заполнять 4x3 изображения на 16x9, если АМКОНТРОЛ \_ Pad \_ \_ 16x9 Set.</span><span class="sxs-lookup"><span data-stu-id="219af-160">The VMR will pad 4x3 images to 16x9 if they have the AMCONTROL\_PAD\_TO\_16x9 set.</span></span>
    2.  <span data-ttu-id="219af-161">Выводите выходной образ в образ 16x9 и удаляет панель АМКОНТРОЛ \_ \_ в \_ 16x9 bit.</span><span class="sxs-lookup"><span data-stu-id="219af-161">Pad the output image to a 16x9 image and remove the AMCONTROL\_PAD\_TO\_16x9 bit.</span></span>

<span data-ttu-id="219af-162">Большинство декодеров должны использовать **жетмедиатипе** для обнаружения изменения носителя на входном ПИН-коде и копирования содержимого **VIDEOINFOHEADER2** (содержится в **MPEG2INFOHEADER**) в выходной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="219af-162">Most decoders should use **GetMediaType** to detect a media change on the input pin and copy the **VIDEOINFOHEADER2** contents (contained in the **MPEG2INFOHEADER**) to the output pin.</span></span> <span data-ttu-id="219af-163">Скорее всего, они будут обрабатывать только Панскан бит.</span><span class="sxs-lookup"><span data-stu-id="219af-163">They will probably only process the PanScan bit.</span></span>

<span data-ttu-id="219af-164">В следующем примере кода показано, как скопировать содержимое **VIDEOINFOHEADER2** из входного контакта в выходной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="219af-164">The following example code shows how to copy the **VIDEOINFOHEADER2** contents from an input pin to an output pin.</span></span>


```C++
#include <dvdmedia.h>
HRESULT CopyMPeg2ToVideoInfoHeader2(CMediaSample* pInSample, CMediaSample* pOutSample)
{
    HRESULT hr = S_OK;
    // Check for a media type on the input sample.
    AM_MEDIA_TYPE* pInType;
    if (pInSample->GetMediaType(&pInType) == S_OK) 
    {
        // Make sure it's an MPEG2 Video format.
        if ((pInType->formattype == FORMAT_MPEG2_VIDEO) &&
            (pInType->cbFormat >= sizeof(MPEG2VIDEOINFO)))
        {
            hr = S_OK; // Initialize hr for the CMediaType constructor.
            CMediaType outType(*pInType, &hr);
            if (FAILED(hr))
            {
                DeleteMediaType( pInType );
                return hr;
            }

            // Set the format type GUID.
            outType.SetFormatType(&FORMAT_VideoInfo2);
                
            // Truncate the format block to include just the VIDEOINFOHEADER part.
            MPEG2VIDEOINFO *pMPeg2Header = (MPEG2VIDEOINFO*)pInType->pbFormat;
            BYTE *pVIH = (BYTE*)&pMPeg2Header->hdr;
            hr = (outType.SetFormat(pVIH, sizeof(VIDEOINFOHEADER2)) ? S_OK : E_OUTOFMEMORY);
            if (SUCCEEDED(hr))
            {
                hr = pOutSample->SetMediaType(&outType);
            }
        } 
        else 
        {
            ASSERT(FALSE); // Not a MPEG2 header.
            hr = VFW_E_INVALIDMEDIATYPE;
        }
        DeleteMediaType( pInType );
    } 

    return hr;
}
```



 

 



