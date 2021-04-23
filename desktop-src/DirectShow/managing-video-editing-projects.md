---
description: Управление проектами редактирования видео
ms.assetid: f8d74807-562f-429b-93a1-e65d0f15163b
title: Управление проектами редактирования видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491cfcb9a6e94874d2cae43567b61666bbd43cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105662017"
---
# <a name="managing-video-editing-projects"></a><span data-ttu-id="ccc80-103">Управление проектами редактирования видео</span><span class="sxs-lookup"><span data-stu-id="ccc80-103">Managing Video Editing Projects</span></span>

<span data-ttu-id="ccc80-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="ccc80-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="ccc80-105">Следующие советы помогут вам управлять проектами в [службах редактирования DirectShow](directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="ccc80-105">The following tips will help you to manage projects in [DirectShow Editing Services](directshow-editing-services.md).</span></span>

<span data-ttu-id="ccc80-106">Изменения в временной шкале</span><span class="sxs-lookup"><span data-stu-id="ccc80-106">Changes to the Timeline</span></span>

-   <span data-ttu-id="ccc80-107">При изменении временной шкалы после построения графа фильтра вызовите [**ирендеренгине:: коннектфронтенд**](irenderengine-connectfrontend.md) еще раз, чтобы перестроить внешний интерфейс.</span><span class="sxs-lookup"><span data-stu-id="ccc80-107">If you change the timeline after you build the filter graph, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) again to rebuild the front end.</span></span> <span data-ttu-id="ccc80-108">Как правило, это не влияет на оставшуюся часть графа.</span><span class="sxs-lookup"><span data-stu-id="ccc80-108">Usually, this does not affect the rest of the graph.</span></span> <span data-ttu-id="ccc80-109">Однако иногда перед перестроением внешнего интерфейса модулю подготовки отчетов необходимо удалить всю диаграмму.</span><span class="sxs-lookup"><span data-stu-id="ccc80-109">Occasionally, however, the render engine needs to delete the entire graph before it rebuilds the front end.</span></span> <span data-ttu-id="ccc80-110">(Например, это происходит при добавлении или удалении группы.) Метод **коннектфронтенд** возвращает параметр S \_ warn \_ аутпутресет, чтобы сообщить, что он удалил граф.</span><span class="sxs-lookup"><span data-stu-id="ccc80-110">(For example, this happens if you add or remove a group.) The **ConnectFrontEnd** method returns S\_WARN\_OUTPUTRESET to signal that it deleted the graph.</span></span> <span data-ttu-id="ccc80-111">В этом случае приложение должно перестроить раздел отрисовки графа.</span><span class="sxs-lookup"><span data-stu-id="ccc80-111">If this happens, your application must rebuild the rendering section of the graph.</span></span>
-   <span data-ttu-id="ccc80-112">Чтобы полностью удалить все объекты из временной шкалы, вызовите метод [**иамтимелине:: клеараллграупс**](iamtimeline-clearallgroups.md) .</span><span class="sxs-lookup"><span data-stu-id="ccc80-112">To remove all objects completely from the timeline, call the [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md) method.</span></span>

<span data-ttu-id="ccc80-113">**Очистка**</span><span class="sxs-lookup"><span data-stu-id="ccc80-113">**Cleanup**</span></span>

-   <span data-ttu-id="ccc80-114">По завершении использования подсистемы визуализации вызовите метод [**ирендеренгине:: скрапит**](irenderengine-scrapit.md) .</span><span class="sxs-lookup"><span data-stu-id="ccc80-114">When you are finished using a render engine, call the [**IRenderEngine::ScrapIt**](irenderengine-scrapit.md) method.</span></span> <span data-ttu-id="ccc80-115">Как и в случае с любым COM-объектом, не забудьте освободить каждый указатель интерфейса по окончании его использования.</span><span class="sxs-lookup"><span data-stu-id="ccc80-115">As with any COM object, be sure to release every interface pointer when you are finished using it.</span></span>
-   <span data-ttu-id="ccc80-116">Механизм визуализации не сохраняет счетчик ссылок на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="ccc80-116">The render engine does not keep a reference count on the timeline.</span></span> <span data-ttu-id="ccc80-117">Не освобождайте временную шкалу до завершения ее использования и всегда вызывайте **скрапит** в подсистеме рендеринга первыми.</span><span class="sxs-lookup"><span data-stu-id="ccc80-117">Do not release the timeline before you are done using it, and always call **ScrapIt** on the render engine first.</span></span>
-   <span data-ttu-id="ccc80-118">При освобождении всех ссылок на временную шкалу не используйте объекты в этой временной шкале, даже если на них хранятся счетчики ссылок.</span><span class="sxs-lookup"><span data-stu-id="ccc80-118">If you release all references to a timeline, do not use any of the objects in that timeline, even if you are holding reference counts on them.</span></span>

<span data-ttu-id="ccc80-119">**Несколько экземпляров временной шкалы**</span><span class="sxs-lookup"><span data-stu-id="ccc80-119">**Multiple Timeline Instances**</span></span>

-   <span data-ttu-id="ccc80-120">Не переносите объекты временной шкалы между временными шкалами.</span><span class="sxs-lookup"><span data-stu-id="ccc80-120">Do not move timeline objects between timelines.</span></span> <span data-ttu-id="ccc80-121">Каждый объект на временной шкале должен быть создан этой временной шкалой.</span><span class="sxs-lookup"><span data-stu-id="ccc80-121">Every object in a timeline must be created by that timeline.</span></span> <span data-ttu-id="ccc80-122">Временная шкала содержит внутренний кэш со сведениями о создаваемых им объектах. Перемещение объектов временной шкалы может привести к нарушению работы кэша.</span><span class="sxs-lookup"><span data-stu-id="ccc80-122">The timeline holds an internal cache with information about the objects that it creates; moving timeline objects can disrupt the cache.</span></span>
-   <span data-ttu-id="ccc80-123">Никогда не используйте один и тот же экземпляр механизма визуализации с несколькими временными шкалами.</span><span class="sxs-lookup"><span data-stu-id="ccc80-123">Never use the same instance of a render engine with more than one timeline.</span></span> <span data-ttu-id="ccc80-124">Модуль подготовки отчетов содержит кэш со сведениями о временной шкале.</span><span class="sxs-lookup"><span data-stu-id="ccc80-124">The render engine holds a cache with information about the timeline.</span></span> <span data-ttu-id="ccc80-125">Несколько временных шкал нарушит кэш и приведут к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="ccc80-125">Multiple timelines will disrupt the cache and cause unpredictable results.</span></span> <span data-ttu-id="ccc80-126">Если требуются две активные временные шкалы, создайте отдельные экземпляры модулей подготовки отчетов для каждой временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="ccc80-126">If you need two active timelines, make separate instances of render engines for each timeline.</span></span>
-   <span data-ttu-id="ccc80-127">Временная шкала может использовать более одного механизма рендеринга, но не одновременно.</span><span class="sxs-lookup"><span data-stu-id="ccc80-127">A timeline can use more than one render engine, but not at the same time.</span></span> <span data-ttu-id="ccc80-128">Удалите старый обработчик прорисовки перед использованием другого механизма рендеринга.</span><span class="sxs-lookup"><span data-stu-id="ccc80-128">Delete the old render engine before using another render engine.</span></span> <span data-ttu-id="ccc80-129">(Обычно это делается при переключении с использования базового механизма рендеринга для предварительного просмотра в модуль интеллектуального преобразования для записи файлов.)</span><span class="sxs-lookup"><span data-stu-id="ccc80-129">(You would typically do this when you switch from using the basic render engine for preview to the smart render engine for file writing.)</span></span>

<span data-ttu-id="ccc80-130">**Сохраняемость**</span><span class="sxs-lookup"><span data-stu-id="ccc80-130">**Persistence**</span></span>

-   <span data-ttu-id="ccc80-131">Граф фильтра не является постоянным при сохранении проекта в XML-файл.</span><span class="sxs-lookup"><span data-stu-id="ccc80-131">The filter graph is not persistent when you save the project to an XML file.</span></span> <span data-ttu-id="ccc80-132">Таким образом, теряются все сведения, относящиеся к смарт-сжатию, формату сжатия или параметрам сжатия.</span><span class="sxs-lookup"><span data-stu-id="ccc80-132">Therefore, you lose any information relating to smart recompression, compression format, or compression parameters.</span></span> <span data-ttu-id="ccc80-133">Приложение может восстановить эти параметры после загрузки проекта.</span><span class="sxs-lookup"><span data-stu-id="ccc80-133">It is up to the application to restore these parameters after it loads a project.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ccc80-134">См. также</span><span class="sxs-lookup"><span data-stu-id="ccc80-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccc80-135">Использование служб редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="ccc80-135">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



