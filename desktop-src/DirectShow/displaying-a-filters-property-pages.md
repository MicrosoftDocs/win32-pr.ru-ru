---
description: Отображение страниц свойств фильтра
ms.assetid: 4a5f6938-7b33-4350-b8fa-cf78c5c44bcd
title: Отображение страниц свойств фильтра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0845a12b73363dc6ed93654439fd31826bf9cfc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416448"
---
# <a name="displaying-a-filters-property-pages"></a><span data-ttu-id="99020-103">Отображение страниц свойств фильтра</span><span class="sxs-lookup"><span data-stu-id="99020-103">Displaying a Filter's Property Pages</span></span>

<span data-ttu-id="99020-104">Страница свойств является одним из способов, с помощью которых фильтр поддерживает свойства, которые пользователь может задать.</span><span class="sxs-lookup"><span data-stu-id="99020-104">A property page is one way for a filter to support properties that the user can set.</span></span> <span data-ttu-id="99020-105">В этой статье описывается, как отобразить страницы свойств фильтра в приложении.</span><span class="sxs-lookup"><span data-stu-id="99020-105">This article describes how to display a filter's property pages in an application.</span></span> <span data-ttu-id="99020-106">Дополнительные сведения о страницах свойств см. в документации по пакету SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="99020-106">For more information about property pages, see the Platform SDK documentation.</span></span>

> [!Note]  
> <span data-ttu-id="99020-107">Хотя многие из фильтров, предоставляемых с помощью служб DirectShow, поддерживают страницы свойств, они предназначены для отладки и не рекомендуются для использования приложением.</span><span class="sxs-lookup"><span data-stu-id="99020-107">Although many of the filters provided with DirectShow support property pages, they are intended for debugging purposes, and are not recommended for application use.</span></span> <span data-ttu-id="99020-108">В большинстве случаев Аналогичная функциональность предоставляется через пользовательский интерфейс фильтра.</span><span class="sxs-lookup"><span data-stu-id="99020-108">In most cases the equivalent functionality is provided through a custom interface on the filter.</span></span> <span data-ttu-id="99020-109">Приложение должно управлять этими фильтрами программным способом, а не предоставлять пользователям страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="99020-109">An application should control these filters programmatically, rather than expose their property pages to users.</span></span>

 

<span data-ttu-id="99020-110">Фильтры со страницами свойств предоставляют интерфейс **испеЦифипропертипажес** .</span><span class="sxs-lookup"><span data-stu-id="99020-110">Filters with property pages expose the **ISpecifyPropertyPages** interface.</span></span> <span data-ttu-id="99020-111">Чтобы определить, определяет ли фильтр страницу свойств, запросите фильтр для этого интерфейса с помощью **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="99020-111">To determine whether a filter defines a property page, query the filter for this interface using **QueryInterface**.</span></span>

<span data-ttu-id="99020-112">Если вы непосредственно создали экземпляр фильтра (путем вызова **CoCreateInstance**), у вас уже есть указатель на фильтр.</span><span class="sxs-lookup"><span data-stu-id="99020-112">If you directly created an instance of a filter (by calling **CoCreateInstance**), you already have a pointer to the filter.</span></span> <span data-ttu-id="99020-113">В противном случае можно перечислить фильтры в графе с помощью метода [**ифилтерграф:: енумфилтерс**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) .</span><span class="sxs-lookup"><span data-stu-id="99020-113">If not, you can enumerate the filters in the graph, using the [**IFilterGraph::EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) method.</span></span> <span data-ttu-id="99020-114">Дополнительные сведения см. [в разделе Перечисление объектов в графе фильтра](enumerating-objects-in-a-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="99020-114">For details, see [Enumerating Objects in a Filter Graph](enumerating-objects-in-a-filter-graph.md).</span></span>

<span data-ttu-id="99020-115">Получив указатель интерфейса **испеЦифипропертипажес** , извлеките страницы свойств фильтра, вызвав метод **испеЦифипропертипажес::** .</span><span class="sxs-lookup"><span data-stu-id="99020-115">Once you have the **ISpecifyPropertyPages** interface pointer, retrieve the filter's property pages by calling the **ISpecifyPropertyPages::GetPages** method.</span></span> <span data-ttu-id="99020-116">Этот метод заполняет считанный массив глобально уникальных идентификаторов (GUID) с помощью идентификатора класса (CLSID) каждой страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="99020-116">This method fills a counted array of globally unique identifiers (GUIDs) with the class identifier (CLSID) of each property page.</span></span> <span data-ttu-id="99020-117">Подсчет массива определяется структурой **каууид** , которую необходимо выделить, но не нужно инициализировать.</span><span class="sxs-lookup"><span data-stu-id="99020-117">A counted array is defined by a **CAUUID** structure, which you must allocate but do not have to initialize.</span></span> <span data-ttu-id="99020-118">Метод **IsArray** выделяет массив, который содержится в элементе **пелемс** структуры **каууид** .</span><span class="sxs-lookup"><span data-stu-id="99020-118">The **GetPages** method allocates the array, which is contained in the **pElems** member of the **CAUUID** structure.</span></span> <span data-ttu-id="99020-119">По завершении Освободите массив, вызвав функцию **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="99020-119">When you are done, free the array by calling the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="99020-120">Функция **олекреатепропертифраме** предоставляет простой способ отобразить страницы свойств в модальном диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="99020-120">The **OleCreatePropertyFrame** function provides a simple way to display the property pages inside a modal dialog box.</span></span>


```C++
IBaseFilter *pFilter;
/* Obtain the filter's IBaseFilter interface. (Not shown) */
ISpecifyPropertyPages *pProp;
HRESULT hr = pFilter->QueryInterface(IID_ISpecifyPropertyPages, (void **)&pProp);
if (SUCCEEDED(hr)) 
{
    // Get the filter's name and IUnknown pointer.
    FILTER_INFO FilterInfo;
    hr = pFilter->QueryFilterInfo(&FilterInfo); 
    IUnknown *pFilterUnk;
    pFilter->QueryInterface(IID_IUnknown, (void **)&pFilterUnk);

    // Show the page. 
    CAUUID caGUID;
    pProp->GetPages(&caGUID);
    pProp->Release();
    OleCreatePropertyFrame(
        hWnd,                   // Parent window
        0, 0,                   // Reserved
        FilterInfo.achName,     // Caption for the dialog box
        1,                      // Number of objects (just the filter)
        &pFilterUnk,            // Array of object pointers. 
        caGUID.cElems,          // Number of property pages
        caGUID.pElems,          // Array of property page CLSIDs
        0,                      // Locale identifier
        0, NULL                 // Reserved
    );

    // Clean up.
    pFilterUnk->Release();
    FilterInfo.pGraph->Release(); 
    CoTaskMemFree(caGUID.pElems);
}
```



## <a name="related-topics"></a><span data-ttu-id="99020-121">См. также</span><span class="sxs-lookup"><span data-stu-id="99020-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99020-122">Основные задачи DirectShow</span><span class="sxs-lookup"><span data-stu-id="99020-122">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



