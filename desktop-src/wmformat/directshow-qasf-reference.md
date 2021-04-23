---
title: Справочник по КАСФ DirectShow
description: Справочник по КАСФ DirectShow
ms.assetid: 66f483b5-3886-48b4-bc43-7c3517abd20d
keywords:
- Windows Media Format SDK, КАСФ
- Пакет SDK для Windows Media Format, DirectShow
- DirectShow, Справочник по КАСФ
- Фильтры КАСФ, справочные материалы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c509030f676b83a84f67590a242aea623656a514
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413281"
---
# <a name="directshow-qasf-reference"></a><span data-ttu-id="d4d1e-107">Справочник по КАСФ DirectShow</span><span class="sxs-lookup"><span data-stu-id="d4d1e-107">DirectShow QASF Reference</span></span>

<span data-ttu-id="d4d1e-108">В этом разделе содержатся справочники по программированию для следующих фильтров, интерфейсов и перечислений DirectShow КАСФ.</span><span class="sxs-lookup"><span data-stu-id="d4d1e-108">This section contains programming references for the following DirectShow QASF filters, interfaces and enumerations.</span></span> <span data-ttu-id="d4d1e-109">Документация по пакету SDK для DirectShow содержит справочные материалы и руководства по программированию для дополнительных универсальных интерфейсов, предоставляемых такими фильтрами, как **ибасефилтер** и **Ипин**, а также для более ранних версий компонентов касф.</span><span class="sxs-lookup"><span data-stu-id="d4d1e-109">The DirectShow SDK documentation contains reference and programming guide materials for additional generic interfaces exposed by these filters, such as **IBaseFilter** and **IPin**, and for earlier versions of the QASF components.</span></span>

<span data-ttu-id="d4d1e-110">Описание имени КАСФ см. в разделе [About DirectShow](about-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="d4d1e-110">For an explanation of the QASF name, see [About DirectShow](about-directshow.md).</span></span>

<span data-ttu-id="d4d1e-111">В состав компонентов DirectShow КАСФ входят следующие фильтры.</span><span class="sxs-lookup"><span data-stu-id="d4d1e-111">The following filters are included with the DirectShow QASF components.</span></span>



| <span data-ttu-id="d4d1e-112">Фильтр</span><span class="sxs-lookup"><span data-stu-id="d4d1e-112">Filter</span></span>                                           | <span data-ttu-id="d4d1e-113">Описание</span><span class="sxs-lookup"><span data-stu-id="d4d1e-113">Description</span></span>                                                      |
|--------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="d4d1e-114">Фильтр чтения WM ASF</span><span class="sxs-lookup"><span data-stu-id="d4d1e-114">WM ASF Reader Filter</span></span>](wm-asf-reader-filter.md) | <span data-ttu-id="d4d1e-115">Считывает и анализирует локальные или удаленные файлы ASF.</span><span class="sxs-lookup"><span data-stu-id="d4d1e-115">Reads and parses local or remote ASF files.</span></span>                      |
| [<span data-ttu-id="d4d1e-116">Фильтр модуля записи WM ASF</span><span class="sxs-lookup"><span data-stu-id="d4d1e-116">WM ASF Writer Filter</span></span>](wm-asf-writer-filter.md) | <span data-ttu-id="d4d1e-117">Создает файлы ASF из сжатых или несжатых входных потоков.</span><span class="sxs-lookup"><span data-stu-id="d4d1e-117">Creates ASF files from compressed or uncompressed input streams.</span></span> |



 

<span data-ttu-id="d4d1e-118">Следующие интерфейсы определяются для использования с компонентами DirectShow КАСФ.</span><span class="sxs-lookup"><span data-stu-id="d4d1e-118">The following interfaces are defined for use with the DirectShow QASF components.</span></span>



| <span data-ttu-id="d4d1e-119">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="d4d1e-119">Interface</span></span>                                                  | <span data-ttu-id="d4d1e-120">Описание</span><span class="sxs-lookup"><span data-stu-id="d4d1e-120">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4d1e-121">**иамвмбуфферпасс**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-121">**IAMWMBufferPass**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)                 | <span data-ttu-id="d4d1e-122">Предоставляет метод, позволяющий приложениям регистрировать обратные вызовы из входных контактов [модуля записи WM ASF](wm-asf-writer-filter.md) или выходных закрепления фильтра [чтения WM ASF](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="d4d1e-122">Provides a method that enables applications to register for callbacks from the input pins of the [WM ASF Writer](wm-asf-writer-filter.md) or the output pins of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="d4d1e-123">Используется при индексировании и при добавлении расширений модулей данных.</span><span class="sxs-lookup"><span data-stu-id="d4d1e-123">Used in indexing and when adding data unit extensions.</span></span> |
| [<span data-ttu-id="d4d1e-124">**иамвмбуфферпасскаллбакк**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-124">**IAMWMBufferPassCallback**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) | <span data-ttu-id="d4d1e-125">Реализуются приложениями и вызываемыми фильтрами.</span><span class="sxs-lookup"><span data-stu-id="d4d1e-125">Implemented by applications and called by the filters.</span></span> <span data-ttu-id="d4d1e-126">Приложения используют для этого интерфейса один метод для получения сведений об отдельных примерах в потоке.</span><span class="sxs-lookup"><span data-stu-id="d4d1e-126">Applications use the one method on this interface to obtain information about individual samples in the stream.</span></span> <span data-ttu-id="d4d1e-127">Используется при индексировании и при добавлении расширений модулей данных.</span><span class="sxs-lookup"><span data-stu-id="d4d1e-127">Used in indexing and when adding data unit extensions.</span></span>                                                 |
| <span data-ttu-id="d4d1e-128">[**иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d4d1e-128">[**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>               | <span data-ttu-id="d4d1e-129">Реализовано в модуле записи WM ASF.</span><span class="sxs-lookup"><span data-stu-id="d4d1e-129">Implemented on the WM ASF Writer.</span></span> <span data-ttu-id="d4d1e-130">Используется приложениями для указания профилей и параметров индексирования для файла.</span><span class="sxs-lookup"><span data-stu-id="d4d1e-130">Used by applications to specify profiles and indexing parameters for the file.</span></span>                                                                                                                                                              |
| <span data-ttu-id="d4d1e-131">[**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d4d1e-131">[**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>             | <span data-ttu-id="d4d1e-132">Предоставляет дополнительные функции настройки модуля записи WM ASF.</span><span class="sxs-lookup"><span data-stu-id="d4d1e-132">Provides additional configuration functions on the WM ASF Writer.</span></span>                                                                                                                                                                                                             |



 

<span data-ttu-id="d4d1e-133">Следующее перечисление, структура и события определяются для использования с компонентами DirectShow КАСФ.</span><span class="sxs-lookup"><span data-stu-id="d4d1e-133">The following enumeration, structure, and events are defined for use with the DirectShow QASF components.</span></span>



| <span data-ttu-id="d4d1e-134">Перечисление</span><span class="sxs-lookup"><span data-stu-id="d4d1e-134">Enumeration</span></span>                                                               | <span data-ttu-id="d4d1e-135">Описание</span><span class="sxs-lookup"><span data-stu-id="d4d1e-135">Description</span></span>                                                                                                                                                                       |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d1e-136">[\_\_параметр асфвритерконфиг \_](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d4d1e-136">[\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))</span></span> | <span data-ttu-id="d4d1e-137">Определяет параметры конфигурации фильтра, используемые в методах [**IConfigAsfWriter2:: param**](iconfigasfwriter2-getparam.md) и [**сетпарам**](iconfigasfwriter2-setparam.md) .</span><span class="sxs-lookup"><span data-stu-id="d4d1e-137">Defines filter configuration parameters used in the [**IConfigAsfWriter2::GetParam**](iconfigasfwriter2-getparam.md) and [**SetParam**](iconfigasfwriter2-setparam.md) methods.</span></span> |



 



| <span data-ttu-id="d4d1e-138">Структура</span><span class="sxs-lookup"><span data-stu-id="d4d1e-138">Structure</span></span>                                         | <span data-ttu-id="d4d1e-139">Описание</span><span class="sxs-lookup"><span data-stu-id="d4d1e-139">Description</span></span>                                                                                                                                           |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4d1e-140">**\_данные о \_ событии ВМТ \_**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-140">**AM\_WMT\_EVENT\_DATA**</span></span>](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) | <span data-ttu-id="d4d1e-141">Содержит сведения о событии [**\_ состояния ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) и связанном с ним коде состояния, возвращенном пакетом SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="d4d1e-141">Contains information pertaining to a [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) event and the associated status code returned by the Windows Media Format SDK.</span></span> |



 



| <span data-ttu-id="d4d1e-142">Событие</span><span class="sxs-lookup"><span data-stu-id="d4d1e-142">Event</span></span>                                           | <span data-ttu-id="d4d1e-143">Описание</span><span class="sxs-lookup"><span data-stu-id="d4d1e-143">Description</span></span>                                                                                                     |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4d1e-144">\_событие EC ВМТ \_</span><span class="sxs-lookup"><span data-stu-id="d4d1e-144">EC\_WMT\_EVENT</span></span>](ec-wmt-event.md)              | <span data-ttu-id="d4d1e-145">Событие, переадресованное из пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="d4d1e-145">Event forwarded from the Windows Media Format SDK.</span></span>                                                              |
| [<span data-ttu-id="d4d1e-146">\_ \_ событие индекса EC \_ ВМТ</span><span class="sxs-lookup"><span data-stu-id="d4d1e-146">EC\_WMT\_INDEX\_EVENT</span></span>](ec-wmt-index-event.md) | <span data-ttu-id="d4d1e-147">Отправляется, когда приложение использует [модуль записи WM ASF](wm-asf-writer-filter.md) для индексации видеофайлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d4d1e-147">Sent when an application uses the [WM ASF Writer](wm-asf-writer-filter.md) to index Windows Media Video files.</span></span> |



 

 

 