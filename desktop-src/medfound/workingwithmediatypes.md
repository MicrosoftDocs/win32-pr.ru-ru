---
description: Работа с типами мультимедиа DMO
ms.assetid: 1aaf7554-1a5f-439a-afb1-a031607e1a1e
title: Работа с типами мультимедиа DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db172538280a5dcdc6f4ffe91c19ac1d51e91ef9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999885"
---
# <a name="working-with-dmo-media-types"></a><span data-ttu-id="c72bd-103">Работа с типами мультимедиа DMO</span><span class="sxs-lookup"><span data-stu-id="c72bd-103">Working with DMO Media Types</span></span>

<span data-ttu-id="c72bd-104">Входные и выходные типы носителей, используемые кодеком дмос, определяются с помощью структуры [**\_ \_ типа мультимедиа DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) .</span><span class="sxs-lookup"><span data-stu-id="c72bd-104">The input and output media types that are used by the codec DMOs are defined using the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span> <span data-ttu-id="c72bd-105">Эта структура идентична обоим [**\_ \_ типам мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type), которые определены в пакете SDK формата Windows Media и имеют [**\_ \_ тип носителя**](/windows/win32/api/strmif/ns-strmif-am_media_type), который определен в® Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c72bd-105">This structure is identical to both [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type), which is defined in the Windows Media Format SDK, and [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type), which is defined in Microsoft DirectShow®.</span></span> <span data-ttu-id="c72bd-106">В зависимости от приложения вы можете использовать переменные, определенные как один из этих трех типов.</span><span class="sxs-lookup"><span data-stu-id="c72bd-106">Depending upon your application, you may use variables defined as any one of these three types.</span></span> <span data-ttu-id="c72bd-107">Можно спокойно привести указатель к одной из структур типа мультимедиа как другой.</span><span class="sxs-lookup"><span data-stu-id="c72bd-107">It is safe to cast a pointer to one of the media type structures as another.</span></span> <span data-ttu-id="c72bd-108">Пример:</span><span class="sxs-lookup"><span data-stu-id="c72bd-108">For example:</span></span>


```
    DMO_MEDIA_TYPE MediaType;
    WM_MEDIA_TYPE* pMedia = NULL;
    pMedia = (WM_MEDIA_TYPE*)&MediaType;
```



<span data-ttu-id="c72bd-109">Типы форматов, используемые кодеками, обычно ограничиваются теми, которые описаны структурами **видеоинфохеадер** и **вавеформатекс** .</span><span class="sxs-lookup"><span data-stu-id="c72bd-109">The format types that are used by the codecs are generally limited to those described by the **VIDEOINFOHEADER** and **WAVEFORMATEX** structures.</span></span> <span data-ttu-id="c72bd-110">Для удобства константы для этих типов форматов включаются в заголовочный файл вмкодекконст. h.</span><span class="sxs-lookup"><span data-stu-id="c72bd-110">For convenience, constants for these format types are included in the wmcodecconst.h header file.</span></span> <span data-ttu-id="c72bd-111">Имена констант — ВМКФОРМАТ \_ видеоинфо и вмкформат \_ вавеформатекс соответственно.</span><span class="sxs-lookup"><span data-stu-id="c72bd-111">The constant names are WMCFORMAT\_VideoInfo and WMCFORMAT\_WaveFormatEx respectively.</span></span> <span data-ttu-id="c72bd-112">Аудиокодеки могут работать со структурой **вавеформатекстенсибле** в некоторых обстоятельствах и должны использовать их в других.</span><span class="sxs-lookup"><span data-stu-id="c72bd-112">The audio codecs can work with the **WAVEFORMATEXTENSIBLE** structure in some circumstances, and must use it in others.</span></span> <span data-ttu-id="c72bd-113">Однако **\_ тип носителя DMO \_ . форматтипе** устанавливается равным тому же значению, что и для **вавеформатекс**.</span><span class="sxs-lookup"><span data-stu-id="c72bd-113">However, **DMO\_MEDIA\_TYPE.formattype** is set to the same value as it is for **WAVEFORMATEX**.</span></span> <span data-ttu-id="c72bd-114">Дополнительные сведения об использовании **вавеформатекстенсибле** см. [в разделе Использование High-Definition Audio](usinghighdefinitionaudio.md).</span><span class="sxs-lookup"><span data-stu-id="c72bd-114">For more information about using **WAVEFORMATEXTENSIBLE**, see [Using High-Definition Audio](usinghighdefinitionaudio.md).</span></span>

> [!Note]  
>    <span data-ttu-id="c72bd-115">Необходимо включить структуру типа формата, используемую в качестве выходных данных кодировщика, в любом контейнере, который используется для хранения сжатых данных.</span><span class="sxs-lookup"><span data-stu-id="c72bd-115">You must include the format type structure used as the encoder output in whatever container you use to store the compressed data.</span></span> <span data-ttu-id="c72bd-116">Для распаковки содержимого декодерам требуется исходная структура формата.</span><span class="sxs-lookup"><span data-stu-id="c72bd-116">The decoders require the original format structure to decompress the content.</span></span> <span data-ttu-id="c72bd-117">Помимо членов структуры, сжатым типам аудио и видео Windows Media требуются дополнительные сведения о форматировании, которые добавляются к структуре.</span><span class="sxs-lookup"><span data-stu-id="c72bd-117">In addition to the members of the structure, compressed Windows Media Audio and Video types require additional format information, which is appended to the structure.</span></span> <span data-ttu-id="c72bd-118">Дополнительные сведения см. в разделе [Работа с аудио](workingwithaudio.md) и [Работа с видео](workingwithvideo.md).</span><span class="sxs-lookup"><span data-stu-id="c72bd-118">For more information, see [Working with Audio](workingwithaudio.md) and [Working with Video](workingwithvideo.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c72bd-119">См. также</span><span class="sxs-lookup"><span data-stu-id="c72bd-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c72bd-120">Работа с кодеками дмос</span><span class="sxs-lookup"><span data-stu-id="c72bd-120">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
