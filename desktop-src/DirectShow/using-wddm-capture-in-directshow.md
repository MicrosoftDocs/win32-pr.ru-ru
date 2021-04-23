---
description: Использование захвата WDDM в DirectShow
ms.assetid: 57ee86b0-50bc-4992-94d4-f290f83d2afc
title: Использование захвата WDDM в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7926af70a3b7f1c4ba67c791d98c9928c3809b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673985"
---
# <a name="using-wddm-capture-in-directshow"></a><span data-ttu-id="8e6c1-103">Использование захвата WDDM в DirectShow</span><span class="sxs-lookup"><span data-stu-id="8e6c1-103">Using WDDM Capture in DirectShow</span></span>

<span data-ttu-id="8e6c1-104">Этот раздел относится к Windows Vista и более поздним версиям.</span><span class="sxs-lookup"><span data-stu-id="8e6c1-104">This topic applies to Windows Vista and later.</span></span>

<span data-ttu-id="8e6c1-105">Некоторые видеоадаптеры имеют встроенные функции видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="8e6c1-105">Some video cards have integrated video capture functionality.</span></span> <span data-ttu-id="8e6c1-106">На этих картах захваченные видеоматериалы помещаются в видеопамяти (видеопамять).</span><span class="sxs-lookup"><span data-stu-id="8e6c1-106">On these cards, captured video frames are placed in video memory (VRAM).</span></span> <span data-ttu-id="8e6c1-107">До Windows Vista стандартный механизм обработки кадров, оставшихся в видеопамяти, не существовал.</span><span class="sxs-lookup"><span data-stu-id="8e6c1-107">Prior to Windows Vista, there was no standard mechanism for processing the frames while they remained in VRAM.</span></span> <span data-ttu-id="8e6c1-108">Вместо этого данные должны быть скопированы в системную память, обработаны, а затем скопированы обратно в видеоадаптер для вывода.</span><span class="sxs-lookup"><span data-stu-id="8e6c1-108">Instead, the data had to be copied into system memory, processed, and then copied back to VRAM for display.</span></span> <span data-ttu-id="8e6c1-109">В Windows Vista DirectShow теперь поддерживает механизм хранения кадров видео в видеопамяти на протяжении всего конвейера обработки, от записи до вывода.</span><span class="sxs-lookup"><span data-stu-id="8e6c1-109">In Windows Vista, DirectShow now supports a mechanism for keeping the video frames in VRAM throughout the processing pipeline, from capture to display.</span></span>

<span data-ttu-id="8e6c1-110">Фильтр Кспрокси определяет, поддерживает ли драйвер захват видеоповерхности путем запроса драйвера для \_ Свойства "Предпочтительная \_ поверхность захвата кспроперти" \_ .</span><span class="sxs-lookup"><span data-stu-id="8e6c1-110">The KsProxy filter determines if the driver supports VRAM surface capture by querying the driver for the KSPROPERTY\_PREFERRED\_CAPTURE\_SURFACE property.</span></span> <span data-ttu-id="8e6c1-111">(Это свойство описано в документации к пакету драйверов Windows.) Если драйвер поддерживает захват видеоповерхности, Кспрокси выделяет специальный вид мультимедийного примера, который содержит указатель на поверхность Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8e6c1-111">(This property is documented in the Windows Driver Kit documentation.) If the driver supports VRAM surface capture, KsProxy allocates a special kind of media sample that holds a pointer to a Direct3D surface.</span></span>

<span data-ttu-id="8e6c1-112">Затем Кспрокси определяет, поддерживает ли нисходящий фильтр ускорение видео DirectX (ДКСВА) 2,0 следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8e6c1-112">Next, KsProxy determines whether the downstream filter supports DirectX Video Acceleration (DXVA) 2.0, as follows:</span></span>

1.  <span data-ttu-id="8e6c1-113">Кспрокси запрашивает нисходящий входной ПИН-код для интерфейса **имфжетсервице** .</span><span class="sxs-lookup"><span data-stu-id="8e6c1-113">KsProxy queries the downstream input pin for the **IMFGetService** interface.</span></span>
2.  <span data-ttu-id="8e6c1-114">Если ПИН-код представляет **имфжетсервице**, Кспрокси вызывает **имфжетсервице::-Service** для интерфейса **IDirect3DDeviceManager** .</span><span class="sxs-lookup"><span data-stu-id="8e6c1-114">If the pin exposes **IMFGetService**, KsProxy calls **IMFGetService::GetService** for the **IDirect3DDeviceManager** interface.</span></span> <span data-ttu-id="8e6c1-115">Идентиер службы — это \_ \_ Служба ускорения видео в Mr \_ .</span><span class="sxs-lookup"><span data-stu-id="8e6c1-115">The service identier is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>

<span data-ttu-id="8e6c1-116">Оба этих интерфейса описаны в документации по Media Foundation SDK.</span><span class="sxs-lookup"><span data-stu-id="8e6c1-116">Both of these interfaces are documented in the Media Foundation SDK documentation.</span></span>

<span data-ttu-id="8e6c1-117">Если подчиненный фильтр не поддерживает ДКСВА 2,0, Кспрокси выделяет дополнительный буфер системной памяти.</span><span class="sxs-lookup"><span data-stu-id="8e6c1-117">If the downstream filter does not support DXVA 2.0, KsProxy allocates an additional system memory buffer.</span></span> <span data-ttu-id="8e6c1-118">Он использует этот буфер для копирования видеокадров из видеопамяти в системную память.</span><span class="sxs-lookup"><span data-stu-id="8e6c1-118">It uses this buffer to copy the video frames from VRAM to system memory.</span></span> <span data-ttu-id="8e6c1-119">Метод [**имедиасампле::-Point**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) примера мультимедиа возвращает указатель на этот буфер системной памяти.</span><span class="sxs-lookup"><span data-stu-id="8e6c1-119">The media sample's [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method returns a pointer to this system memory buffer.</span></span>

<span data-ttu-id="8e6c1-120">Однако если нисходящий фильтр поддерживает ДКСВА 2,0, то Кспрокси не выделяет буфер системной памяти.</span><span class="sxs-lookup"><span data-stu-id="8e6c1-120">However, if the downstream filter does support DXVA 2.0, then KsProxy does not allocate a system memory buffer.</span></span> <span data-ttu-id="8e6c1-121">**В этом случае метод метода** Нотимпл возвращает E \_ .</span><span class="sxs-lookup"><span data-stu-id="8e6c1-121">In that case, the **GetPointer** method returns E\_NOTIMPL.</span></span> <span data-ttu-id="8e6c1-122">Вместо этого ожидается, что нисходящий фильтр обращается к поверхности Direct3D образца напрямую.</span><span class="sxs-lookup"><span data-stu-id="8e6c1-122">Instead, the downstream filter is expected to access the sample's Direct3D surface directly.</span></span> <span data-ttu-id="8e6c1-123">Существует два способа, с помощью которых подчиненный фильтр получает указатель на поверхность, оба они эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="8e6c1-123">There are two ways for the downstream filter to get a pointer to the surface, both of them equivalent:</span></span>

-   <span data-ttu-id="8e6c1-124">Запросите пример для интерфейса **имфжетсервице** и вызовите метод **WebService** для интерфейса **IDirect3DSurface9** .</span><span class="sxs-lookup"><span data-stu-id="8e6c1-124">Query the sample for the **IMFGetService** interface and call **GetService** for the **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="8e6c1-125">Идентификатор службы — это \_ Служба буфера MR \_ .</span><span class="sxs-lookup"><span data-stu-id="8e6c1-125">The service identifier is MR\_BUFFER\_SERVICE.</span></span>
-   <span data-ttu-id="8e6c1-126">Выполните запрос к образцу для интерфейса [**IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) и вызовите [**IMediaSample2Config::**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface).</span><span class="sxs-lookup"><span data-stu-id="8e6c1-126">Query the sample for the [**IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) interface and call [**IMediaSample2Config::GetSurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e6c1-127">См. также</span><span class="sxs-lookup"><span data-stu-id="8e6c1-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e6c1-128">Разделы, посвященные расширенному записи</span><span class="sxs-lookup"><span data-stu-id="8e6c1-128">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> </dl>

 

 



