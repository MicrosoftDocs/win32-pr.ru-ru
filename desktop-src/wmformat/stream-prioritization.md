---
title: Определение приоритетов потоков
description: Определение приоритетов потоков
ms.assetid: 6b3e9b03-62ef-422b-97ab-197d1cd15beb
keywords:
- Windows Media Format SDK, определение приоритетов потоков
- Расширенный системный формат (ASF), определение приоритетов потоков
- ASF (Расширенный системный формат), определение приоритетов потоков
- Пакет SDK Windows Media Format, порядок приоритетов для потоков
- Расширенный системный формат (ASF), порядок приоритета для потоков
- ASF (Расширенный системный формат), порядок приоритета для потоков
- потоки, определение приоритетов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1628ef050d393cd2d98e73708d5a9ad6c3be4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069584"
---
# <a name="stream-prioritization"></a><span data-ttu-id="27f2e-110">Определение приоритетов потоков</span><span class="sxs-lookup"><span data-stu-id="27f2e-110">Stream Prioritization</span></span>

<span data-ttu-id="27f2e-111">При создании файла ASF можно указать порядок приоритета для его составных потоков.</span><span class="sxs-lookup"><span data-stu-id="27f2e-111">When you create an ASF file, you can specify a priority order for its constituent streams.</span></span> <span data-ttu-id="27f2e-112">Если вы выполняете потоковую передачу по приоритетному файлу и доступная пропускная способность не достаточна для доставки всех потоков, модуль чтения удалит потоки в порядке, соответствующем обратным приоритетам.</span><span class="sxs-lookup"><span data-stu-id="27f2e-112">If you stream a prioritized file and the available bandwidth is not enough to deliver all of the streams, the reader will drop streams in reverse priority order.</span></span> <span data-ttu-id="27f2e-113">Таким образом можно гарантировать, что наиболее важные потоки в файле не будут удалены из-за сетевых проблем.</span><span class="sxs-lookup"><span data-stu-id="27f2e-113">In this way you can guarantee that the most important streams in your file will not be dropped due to network difficulties.</span></span>

<span data-ttu-id="27f2e-114">Определение приоритетов потоков настраивается с помощью объекта определения приоритетов потоков и добавляется в профиль.</span><span class="sxs-lookup"><span data-stu-id="27f2e-114">Stream prioritization is configured with a stream prioritization object and added to the profile.</span></span> <span data-ttu-id="27f2e-115">Профиль может содержать только один объект определения приоритетов потоков.</span><span class="sxs-lookup"><span data-stu-id="27f2e-115">A profile can contain only one stream prioritization object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27f2e-116">См. также</span><span class="sxs-lookup"><span data-stu-id="27f2e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27f2e-117">**Функции файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="27f2e-117">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="27f2e-118">**IWMProfile3:: Креатеневстреамприоритизатион**</span><span class="sxs-lookup"><span data-stu-id="27f2e-118">**IWMProfile3::CreateNewStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)
</dt> <dt>

[<span data-ttu-id="27f2e-119">**IWMProfile3:: Жетстреамприоритизатион**</span><span class="sxs-lookup"><span data-stu-id="27f2e-119">**IWMProfile3::GetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)
</dt> <dt>

[<span data-ttu-id="27f2e-120">**IWMProfile3:: Ремовестреамприоритизатион**</span><span class="sxs-lookup"><span data-stu-id="27f2e-120">**IWMProfile3::RemoveStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-removestreamprioritization)
</dt> <dt>

[<span data-ttu-id="27f2e-121">**IWMProfile3:: Сетстреамприоритизатион**</span><span class="sxs-lookup"><span data-stu-id="27f2e-121">**IWMProfile3::SetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)
</dt> <dt>

[<span data-ttu-id="27f2e-122">**Интерфейс Ивмстреамприоритизатион**</span><span class="sxs-lookup"><span data-stu-id="27f2e-122">**IWMStreamPrioritization Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization)
</dt> <dt>

[<span data-ttu-id="27f2e-123">**Использование определения приоритетов потоков**</span><span class="sxs-lookup"><span data-stu-id="27f2e-123">**Using Stream Prioritization**</span></span>](using-stream-prioritization.md)
</dt> </dl>

 

 




