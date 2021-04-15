---
title: Совместное использование пропускной способности
description: Совместное использование пропускной способности
ms.assetid: 1df61a3a-d34a-447e-a7ee-d5d409e7c4fa
keywords:
- Windows Media Format SDK, совместное использование пропускной способности
- Совместное использование пропускной способности, сведения
- профили, совместное использование пропускной способности
- потоки, совместное использование пропускной способности
- Совместное использование пропускной способности, интерфейс Ивмпрофиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298c690b484a8b4b5990aacd5d525867da8923c0
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104412705"
---
# <a name="using-bandwidth-sharing"></a><span data-ttu-id="32c11-108">Совместное использование пропускной способности</span><span class="sxs-lookup"><span data-stu-id="32c11-108">Using Bandwidth Sharing</span></span>

<span data-ttu-id="32c11-109">Можно использовать объекты совместного использования пропускной способности, чтобы указать, что определенные потоки при объединении не будут использовать больше пропускной способности, чем указано.</span><span class="sxs-lookup"><span data-stu-id="32c11-109">You can use bandwidth sharing objects to specify that certain streams, when combined, will not use more bandwidth than specified.</span></span> <span data-ttu-id="32c11-110">Информация в объекте для совместного использования пропускной способности не создается или не проверяется модулем записи и не используется средством чтения для чего-либо.</span><span class="sxs-lookup"><span data-stu-id="32c11-110">The information in a bandwidth sharing object is not generated or verified by the writer nor used by the reader for anything.</span></span>

<span data-ttu-id="32c11-111">При написании файла, который содержит сведения о совместном использовании пропускной способности в своем профиле, данные хранятся в разделе заголовка.</span><span class="sxs-lookup"><span data-stu-id="32c11-111">When a file is written that has bandwidth sharing information in its profile, the data is stored in its header section.</span></span> <span data-ttu-id="32c11-112">Вы можете использовать интерфейс [**ивмпрофиле**](iwmprofile.md) в модуле чтения, чтобы проверить сведения о совместном использовании пропускной способности при воспроизведении файла.</span><span class="sxs-lookup"><span data-stu-id="32c11-112">You can use the [**IWMProfile**](iwmprofile.md) interface in the reader to check for bandwidth sharing information when the file is played.</span></span>

<span data-ttu-id="32c11-113">Каждый объект совместного использования пропускной способности определяется двумя параметрами.</span><span class="sxs-lookup"><span data-stu-id="32c11-113">Each bandwidth sharing object is defined by two settings.</span></span> <span data-ttu-id="32c11-114">Первый — это пропускная способность, определяемая пропускной способностью и окном буфера.</span><span class="sxs-lookup"><span data-stu-id="32c11-114">First is the bandwidth, as defined by a bandwidth and a buffer window.</span></span> <span data-ttu-id="32c11-115">Второй параметр — тип совместного использования пропускной способности, который может быть либо эксклюзивным, либо частичным.</span><span class="sxs-lookup"><span data-stu-id="32c11-115">The second setting is a bandwidth sharing type, which can be either exclusive or partial.</span></span> <span data-ttu-id="32c11-116">Монопольный доступ к пропускной способности означает, что составные потоки воспроизводятся по одному за раз, а частичные — потоки доставляются параллельно.</span><span class="sxs-lookup"><span data-stu-id="32c11-116">Exclusive bandwidth sharing means that the constituent streams are played back one at a time, while partial means the streams are delivered concurrently.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32c11-117">См. также</span><span class="sxs-lookup"><span data-stu-id="32c11-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32c11-118">**Интерфейс Ивмпрофиле**</span><span class="sxs-lookup"><span data-stu-id="32c11-118">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="32c11-119">**IWMProfile3:: Аддбандвидсшаринг**</span><span class="sxs-lookup"><span data-stu-id="32c11-119">**IWMProfile3::AddBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="32c11-120">**IWMProfile3:: Креатеневбандвидсшаринг**</span><span class="sxs-lookup"><span data-stu-id="32c11-120">**IWMProfile3::CreateNewBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="32c11-121">**IWMProfile3:: Жетбандвидсшаринг**</span><span class="sxs-lookup"><span data-stu-id="32c11-121">**IWMProfile3::GetBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="32c11-122">**IWMProfile3:: Жетбандвидсшарингкаунт**</span><span class="sxs-lookup"><span data-stu-id="32c11-122">**IWMProfile3::GetBandwidthSharingCount**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharingcount)
</dt> <dt>

[<span data-ttu-id="32c11-123">**Работа с профилями**</span><span class="sxs-lookup"><span data-stu-id="32c11-123">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




