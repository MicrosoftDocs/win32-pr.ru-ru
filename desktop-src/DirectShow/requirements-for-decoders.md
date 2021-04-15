---
description: Требования к декодерам
ms.assetid: 149aea20-0d37-4b1c-a098-8446c4088ce1
title: Требования к декодерам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461120bec88636e4c015c2e319d855571e8ac1b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494841"
---
# <a name="requirements-for-decoders"></a><span data-ttu-id="68603-103">Требования к декодерам</span><span class="sxs-lookup"><span data-stu-id="68603-103">Requirements for Decoders</span></span>

<span data-ttu-id="68603-104">Декодеры, которые доставляют образцы в VMR, должны соблюдать следующие правила.</span><span class="sxs-lookup"><span data-stu-id="68603-104">Decoders that deliver samples to the VMR must observe the following rules:</span></span>

-   <span data-ttu-id="68603-105">В VMR для каждого видеокадра должен быть доставлен один кадр подизображения.</span><span class="sxs-lookup"><span data-stu-id="68603-105">There should be one subpicture frame delivered to the VMR for each video frame.</span></span> <span data-ttu-id="68603-106">Оба кадра должны иметь одинаковые метки времени.</span><span class="sxs-lookup"><span data-stu-id="68603-106">The two frames should have the same time stamps.</span></span>
-   <span data-ttu-id="68603-107">Если подизображение не изменилось, используйте \_ флаг AM гбф \_ нотасинкпоинт в методе [**имемаллокатор::-buffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) , чтобы заставить распределитель вернуть буфер, содержащий последний кадр, доставленный в VMR.</span><span class="sxs-lookup"><span data-stu-id="68603-107">If the subpicture has not changed, use the AM\_GBF\_NOTASYNCPOINT flag in the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method to force the allocator to return a buffer containing the last frame delivered to the VMR.</span></span> <span data-ttu-id="68603-108">Просто поставьте новый штамп времени для примера и снова доставьте его в VMR.</span><span class="sxs-lookup"><span data-stu-id="68603-108">Just put a new time stamp on the sample and deliver it to the VMR again.</span></span> <span data-ttu-id="68603-109">Если картинка славы пуста, ее все еще следует доставлять.</span><span class="sxs-lookup"><span data-stu-id="68603-109">If the subpicture fame is blank, you should still deliver it.</span></span> <span data-ttu-id="68603-110">VMR определит пустой фрейм и не смешивает его с видео.</span><span class="sxs-lookup"><span data-stu-id="68603-110">The VMR will detect the empty frame and not blend it with the video.</span></span> <span data-ttu-id="68603-111">Эта проверка выполняется микросхемой VGA и не влияет на производительность воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="68603-111">This test is performed by the VGA chip and does not affect the playback performance.</span></span>
-   <span data-ttu-id="68603-112">Все примеры, за исключением динамических потоков, должны иметь действительные метки времени начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="68603-112">All samples, except for live streams, must have valid start and stop time stamps attached.</span></span> <span data-ttu-id="68603-113">(DVD не является активным потоком.)</span><span class="sxs-lookup"><span data-stu-id="68603-113">(DVD is not a live stream.)</span></span>
-   <span data-ttu-id="68603-114">Метки времени образца носителя должны быть непрерывными</span><span class="sxs-lookup"><span data-stu-id="68603-114">The media sample time stamps must be contiguous</span></span>
-   <span data-ttu-id="68603-115">Декодер должен идентифицировать себя как VMR-совместимый для использования построителями Graph.</span><span class="sxs-lookup"><span data-stu-id="68603-115">The decoder must identify itself as VMR-capable for use by graph builders.</span></span>
-   <span data-ttu-id="68603-116">Поток субтитров теперь должен содержать внедренные альфа-значения для каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="68603-116">The subpicture stream should now contain embedded per-pixel alpha values.</span></span> <span data-ttu-id="68603-117">Тип поверхности ARGB4444 идеально подходит для подизображений.</span><span class="sxs-lookup"><span data-stu-id="68603-117">The ARGB4444 surface type is ideal for subpictures.</span></span>
-   <span data-ttu-id="68603-118">Не следует рассчитывать на то, что шаг подизображения совпадает с шириной поверхности.</span><span class="sxs-lookup"><span data-stu-id="68603-118">Do not assume that the stride of the subpicture is the same as the surface width.</span></span> <span data-ttu-id="68603-119">Это не всегда имеет место при использовании VMR.</span><span class="sxs-lookup"><span data-stu-id="68603-119">This is not always the case with the VMR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68603-120">См. также</span><span class="sxs-lookup"><span data-stu-id="68603-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68603-121">Об ускорении видео DirectX</span><span class="sxs-lookup"><span data-stu-id="68603-121">About DirectX Video Acceleration</span></span>](about-directx-video-acceleration.md)
</dt> </dl>

 

 



