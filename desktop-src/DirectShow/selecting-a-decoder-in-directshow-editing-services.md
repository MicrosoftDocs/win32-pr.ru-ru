---
description: Выбор декодера в службах редактирования DirectShow
ms.assetid: dc6b0445-7fc1-4331-9000-a652b44a8364
title: Выбор декодера в службах редактирования DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956ad0284722eb394590b1b0065f167c55b3cf51
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494886"
---
# <a name="selecting-a-decoder-in-directshow-editing-services"></a><span data-ttu-id="5245d-103">Выбор декодера в службах редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="5245d-103">Selecting a Decoder in DirectShow Editing Services</span></span>

<span data-ttu-id="5245d-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="5245d-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="5245d-105">Когда [службы редактирования данных DirectShow](directshow-editing-services.md) (DES) визуализируют проект редактирования видео, механизм визуализации автоматически выбирает необходимые декодеры.</span><span class="sxs-lookup"><span data-stu-id="5245d-105">When [DirectShow Editing Services](directshow-editing-services.md) (DES) renders a video editing project, the Rendering Engine automatically selects the necessary decoders.</span></span> <span data-ttu-id="5245d-106">Это может произойти внутри метода [**ирендеренгине:: коннектфронтенд**](irenderengine-connectfrontend.md) или динамически во время подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="5245d-106">This may happen inside the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method, or else dynamically during rendering.</span></span>

<span data-ttu-id="5245d-107">Пользователь может установить несколько декодеров, способных декодировать определенный файл.</span><span class="sxs-lookup"><span data-stu-id="5245d-107">A user might install several decoders that are capable of decoding a particular file.</span></span> <span data-ttu-id="5245d-108">Если доступно несколько декодеров, DES использует алгоритм [интеллектуального соединения](intelligent-connect.md) для выбора декодера.</span><span class="sxs-lookup"><span data-stu-id="5245d-108">When multiple decoders are available, DES uses the [Intelligent Connect](intelligent-connect.md) algorithm to select the decoder.</span></span>

<span data-ttu-id="5245d-109">В приложении нет способа указать, какой декодер следует использовать.</span><span class="sxs-lookup"><span data-stu-id="5245d-109">There is no way for the application to specify directly which decoder to use.</span></span> <span data-ttu-id="5245d-110">Однако декодер можно выбрать опосредованно через интерфейс обратного вызова [**иамграфбуилдеркаллбакк**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) .</span><span class="sxs-lookup"><span data-stu-id="5245d-110">However, you can choose the decoder indirectly through the [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) callback interface.</span></span> <span data-ttu-id="5245d-111">Реализуя этот интерфейс в приложении, вы можете получать уведомления во время процесса построения графа и отклонять определенные фильтры из графа.</span><span class="sxs-lookup"><span data-stu-id="5245d-111">By implementing this interface in your application, you can receive notifications during the graph-building process and reject certain filters from the graph.</span></span>

<span data-ttu-id="5245d-112">Начните с реализации класса, предоставляющего интерфейс [**иамграфбуилдеркаллбакк**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) :</span><span class="sxs-lookup"><span data-stu-id="5245d-112">Start by implementing a class that exposes the [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) interface:</span></span>


```C++
class GraphBuilderCB : public IAMGraphBuilderCallback
{
public:
     // Method declarations (not shown).
};
```



<span data-ttu-id="5245d-113">Затем создайте экземпляр диспетчера графа фильтров и зарегистрируйте свой класс для получения уведомлений обратного вызова:</span><span class="sxs-lookup"><span data-stu-id="5245d-113">Then create an instance of the Filter Graph Manager and register your class to receive callback notifications:</span></span>


```C++
// Declare an instance of the callback object.
GraphBuilderCB GraphCB; 

// Create the Filter Graph Manager.
CComPtr<IGraphBuilder> pGraph;
hr = pGraph.CoCreateInstance(CLSID_FilterGraph);
if (FAILED(hr))
{
    // Handle error (not shown).
}
// Register to receive the callbacks.
CComQIPtr<IObjectWithSite> pSite(pGraph);
if (pSite)
{
    hr = pSite->SetSite((IUnknown*)&GraphCB);
}
```



<span data-ttu-id="5245d-114">Затем создайте подсистему отрисовки и вызовите метод [**ирендеренгине:: сетфилтерграф**](irenderengine-setfiltergraph.md) с указателем на диспетчер графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="5245d-114">Next, create the Render Engine and call the [**IRenderEngine::SetFilterGraph**](irenderengine-setfiltergraph.md) method with a pointer to the Filter Graph Manager.</span></span> <span data-ttu-id="5245d-115">Это гарантирует, что модуль визуализации не создаст собственный диспетчер графов фильтров, а использует экземпляр, настроенный для обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="5245d-115">This ensures that the Render Engine does not create its own Filter Graph Manager, but instead uses the instance that you have configured for callbacks.</span></span>


```C++
CComPtr<IRenderEngine> pRender;
hr = pRender.CoCreateInstance(CLSID_RenderEngine);
if (FAILED(hr))
{
    // Handle error (not shown).
}

hr = pRender->SetFilterGraph(pGraph);
```



<span data-ttu-id="5245d-116">При подготовке к просмотру проекта метод [**иамграфбуилдеркаллбакк:: селектедфилтер**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) приложения вызывается непосредственно перед тем, как диспетчер графов фильтров создаст новый фильтр.</span><span class="sxs-lookup"><span data-stu-id="5245d-116">When the project is rendered, the application's [**IAMGraphBuilderCallback::SelectedFilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) method is called immediately before the Filter Graph Manager creates a new filter.</span></span> <span data-ttu-id="5245d-117">Метод **селектедфилтер** получает указатель на интерфейс **IMoniker** , представляющий моникер для фильтра.</span><span class="sxs-lookup"><span data-stu-id="5245d-117">The **SelectedFilter** method receives a pointer to an **IMoniker** interface that represents a moniker for the filter.</span></span> <span data-ttu-id="5245d-118">Проверьте моникер и, если вы решили отклонить фильтр, возвратите код ошибки из метода **селектедфилтер** .</span><span class="sxs-lookup"><span data-stu-id="5245d-118">Examine the moniker, and if you decide to reject the filter, return a failure code from the **SelectedFilter** method.</span></span>

<span data-ttu-id="5245d-119">Сложная часть состоит в том, чтобы определить, какие моникеры представляют декодеры — и в частности, какие моникеры представляют декодеры, которые нужно отклонить.</span><span class="sxs-lookup"><span data-stu-id="5245d-119">The difficult part is to identify which monikers represent decoders — and in particular, which monikers represent decoders that you want to reject.</span></span> <span data-ttu-id="5245d-120">Одним из решений является следующее:</span><span class="sxs-lookup"><span data-stu-id="5245d-120">One solution is the following:</span></span>

-   <span data-ttu-id="5245d-121">Перед визуализацией проекта используйте метод [**IFilterMapper2:: енумматчингфилтерс**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) , чтобы создать список фильтров, зарегистрированных как принимающий нужный тип входных данных.</span><span class="sxs-lookup"><span data-stu-id="5245d-121">Before rendering the project, use the [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method to create a list of filters that are registered as accepting the desired input type.</span></span> <span data-ttu-id="5245d-122">Для типов сжатия видео или аудио этот список должен сопоставляться с набором декодеров.</span><span class="sxs-lookup"><span data-stu-id="5245d-122">For video or audio compression types, this list should map to a set of decoders.</span></span>
-   <span data-ttu-id="5245d-123">Метод **енумматчингфилтерс** Возвращает коллекцию моникеров.</span><span class="sxs-lookup"><span data-stu-id="5245d-123">The **EnumMatchingFilters** method returns a collection of monikers.</span></span> <span data-ttu-id="5245d-124">Для каждого моникера в коллекции следует получить свойство **DisplayName** , как описано в разделе [Использование модуля сопоставления фильтров](using-the-filter-mapper.md).</span><span class="sxs-lookup"><span data-stu-id="5245d-124">For each moniker in the collection, get the **DisplayName** property, as described in [Using the Filter Mapper](using-the-filter-mapper.md).</span></span>
-   <span data-ttu-id="5245d-125">Сохраните список отображаемых имен, но не указывайте отображаемое имя, соответствующее фильтру, который вы хотите использовать для декодирования.</span><span class="sxs-lookup"><span data-stu-id="5245d-125">Store a list of the display names, but omit the display name that matches the filter you want to use for decoding.</span></span> <span data-ttu-id="5245d-126">Отображаемые имена для фильтров программного обеспечения имеют следующую форму:</span><span class="sxs-lookup"><span data-stu-id="5245d-126">Display names for software filters have the following form:</span></span>

    ```C++
    OLESTR("@device:sw:{CategoryGUID}\{FilterCLSID}");
    ```

    

    <span data-ttu-id="5245d-127">where</span><span class="sxs-lookup"><span data-stu-id="5245d-127">where</span></span>

    ```C++
    CategoryGUID
    ```

    

    <span data-ttu-id="5245d-128">Идентификатор GUID категории фильтра.</span><span class="sxs-lookup"><span data-stu-id="5245d-128">is the GUID of the filter category, and</span></span>

    ```C++
    FilterCLSID
    ```

    

    <span data-ttu-id="5245d-129">Идентификатор CLSID фильтра.</span><span class="sxs-lookup"><span data-stu-id="5245d-129">is the filter's CLSID.</span></span> <span data-ttu-id="5245d-130">Для дмос формат совпадает, но измените `sw` на `dmo` .</span><span class="sxs-lookup"><span data-stu-id="5245d-130">For DMOs, the format is the same, but change `sw` to `dmo`.</span></span>

    <span data-ttu-id="5245d-131">Теперь список содержит отображаемые имена для каждого фильтра, который выводит нужный тип мультимедиа, но не является предпочтительным фильтром.</span><span class="sxs-lookup"><span data-stu-id="5245d-131">The list now contains display names for every filter that outputs the desired media type but is not your preferred filter.</span></span>

-   <span data-ttu-id="5245d-132">В методе **селектедфилтер** получите свойство **DisplayName** в предложенном моникере и проверьте его на соответствие сохраненному списку.</span><span class="sxs-lookup"><span data-stu-id="5245d-132">In the **SelectedFilter** method, get the **DisplayName** property on the proposed moniker and check it against the stored list.</span></span> <span data-ttu-id="5245d-133">Если отображаемое имя совпадает с записью в списке, отклоните этот фильтр.</span><span class="sxs-lookup"><span data-stu-id="5245d-133">If the display name matches an entry in the list, reject that filter.</span></span> <span data-ttu-id="5245d-134">В противном случае примите его, вернувшись в значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="5245d-134">Otherwise, accept it by returning S\_OK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5245d-135">См. также</span><span class="sxs-lookup"><span data-stu-id="5245d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5245d-136">Подготовка проекта</span><span class="sxs-lookup"><span data-stu-id="5245d-136">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



