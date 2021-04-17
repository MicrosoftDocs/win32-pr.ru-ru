---
description: Отчеты о нехватке памяти позволяют приложению Direct3D определить, когда рабочий набор видеопамяти стал слишком большим.
ms.assetid: 3aa2f81e-81a1-40a3-ad24-72781d36f713
title: Отчеты о нехватке памяти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d380a4c9f88fca3d25eebfcfaf67759226ab040c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673505"
---
# <a name="memory-pressure-reporting"></a><span data-ttu-id="3142c-103">Отчеты о нехватке памяти</span><span class="sxs-lookup"><span data-stu-id="3142c-103">Memory Pressure Reporting</span></span>

<span data-ttu-id="3142c-104">Отчеты о нехватке памяти позволяют приложению Direct3D определить, когда рабочий набор видеопамяти стал слишком большим.</span><span class="sxs-lookup"><span data-stu-id="3142c-104">Memory pressure reporting enables a Direct3D application to determine when its video-memory working set has grown too large.</span></span>

<span data-ttu-id="3142c-105">*Нехватка памяти* — это требование, которое приложение помещает в подсистему памяти.</span><span class="sxs-lookup"><span data-stu-id="3142c-105">*Memory pressure* is the demand placed on the memory subsystem by an application.</span></span> <span data-ttu-id="3142c-106">Хотя любое приложение Direct3D может использовать отчеты о нехватке памяти, эта функция особенно полезна для приложений, которые визуализируют видео с помощью Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3142c-106">While any Direct3D application can use memory pressure reporting, this feature is especially useful for applications that render video by using Direct3D.</span></span> <span data-ttu-id="3142c-107">Воспроизведение видео обычно дает преимущества от больших объемов буферизации, что позволяет заранее декодировать кадры.</span><span class="sxs-lookup"><span data-stu-id="3142c-107">Video playback typically benefits from large amounts of buffering, so that frames can be decoded in advance.</span></span> <span data-ttu-id="3142c-108">В то время как буферизация обычно приводит к более гладкому воспроизведению, это может привести к снижению производительности, если рабочий набор растет слишком большой из-за следующих факторов:</span><span class="sxs-lookup"><span data-stu-id="3142c-108">While buffering generally results in smoother playback, it can actually degrade performance if the working set grows too large, due to the following factors:</span></span>

-   <span data-ttu-id="3142c-109">Память может быть удалена из кэша.</span><span class="sxs-lookup"><span data-stu-id="3142c-109">Memory might be evicted from the cache.</span></span> <span data-ttu-id="3142c-110">В худшем случае это может происходить на каждом кадре видео.</span><span class="sxs-lookup"><span data-stu-id="3142c-110">In the worst case, this can occur on every video frame.</span></span>
-   <span data-ttu-id="3142c-111">Выделения памяти могут размещаться в неоптимальных сегментах памяти.</span><span class="sxs-lookup"><span data-stu-id="3142c-111">Memory allocations might be placed in nonoptimal memory segments.</span></span>

<span data-ttu-id="3142c-112">Начиная с Windows 7, Direct3D может сообщать о некоторых статистических данных о нехватке видеопамяти:</span><span class="sxs-lookup"><span data-stu-id="3142c-112">Starting in Windows 7, Direct3D can report some statistics about the video memory pressure:</span></span>

-   <span data-ttu-id="3142c-113">Число байтов, исключенных процессом за интервал времени.</span><span class="sxs-lookup"><span data-stu-id="3142c-113">The number of bytes evicted by the process over an interval of time.</span></span>
-   <span data-ttu-id="3142c-114">Объем памяти, размещенной в неоптимальных сегментах памяти.</span><span class="sxs-lookup"><span data-stu-id="3142c-114">The amount of memory placed in nonoptimal memory segments.</span></span>
-   <span data-ttu-id="3142c-115">Приблизительная индикация общей эффективности выделения памяти, размещенной в неоптимальной памяти.</span><span class="sxs-lookup"><span data-stu-id="3142c-115">A rough indication of the overall efficiency of the memory allocations placed in nonoptimal memory.</span></span>

<span data-ttu-id="3142c-116">Эти сведения могут помочь приложению поддерживать приемлемый рабочий набор.</span><span class="sxs-lookup"><span data-stu-id="3142c-116">This information can help an application to maintain a reasonable working set.</span></span>

## <a name="using-memory-pressure-reporting"></a><span data-ttu-id="3142c-117">Использование отчетов о нехватке памяти</span><span class="sxs-lookup"><span data-stu-id="3142c-117">Using Memory Pressure Reporting</span></span>

<span data-ttu-id="3142c-118">Отчеты о нехватке памяти используют существующий интерфейс **IDirect3DQuery9** для запроса устройства.</span><span class="sxs-lookup"><span data-stu-id="3142c-118">Memory pressure reporting uses the existing **IDirect3DQuery9** interface to query the device.</span></span> <span data-ttu-id="3142c-119">В перечисление **D3DQUERYTYPE** добавлен новый тип запроса.</span><span class="sxs-lookup"><span data-stu-id="3142c-119">A new query type has been added to the **D3DQUERYTYPE** enumeration.</span></span>


```C++
D3DQUERYTYPE_MEMORYPRESSURE        = 19,
```



<span data-ttu-id="3142c-120">Чтобы использовать этот запрос, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3142c-120">To use this query, perform the following steps:</span></span>

1.  <span data-ttu-id="3142c-121">Вызовите **IDirect3DDevice9Ex:: CreateQuery** с флагом **D3DQUERYTYPE \_ меморипрессуре** .</span><span class="sxs-lookup"><span data-stu-id="3142c-121">Call **IDirect3DDevice9Ex::CreateQuery** with the **D3DQUERYTYPE\_MEMORYPRESSURE** flag.</span></span> <span data-ttu-id="3142c-122">Этот метод возвращает указатель на интерфейс **IDirect3DQuery9** .</span><span class="sxs-lookup"><span data-stu-id="3142c-122">This method returns a pointer to the **IDirect3DQuery9** interface.</span></span>
2.  <span data-ttu-id="3142c-123">Вызовите **IDirect3DQuery9:: Issue** с флагом **\_ Begin D3DISSUE** , чтобы начать интервал измерения.</span><span class="sxs-lookup"><span data-stu-id="3142c-123">Call **IDirect3DQuery9::Issue** with the **D3DISSUE\_BEGIN** flag to begin the measurement interval.</span></span>
3.  <span data-ttu-id="3142c-124">Вызовите **IDirect3DQuery9:: Issue** с флагом **\_ End D3DISSUE** .</span><span class="sxs-lookup"><span data-stu-id="3142c-124">Call **IDirect3DQuery9::Issue** with the **D3DISSUE\_END** flag.</span></span>
4.  <span data-ttu-id="3142c-125">Вызовите метод **IDirect3DQuery9:: GetData** , чтобы получить результат запроса.</span><span class="sxs-lookup"><span data-stu-id="3142c-125">Call **IDirect3DQuery9::GetData** to get the query result.</span></span> <span data-ttu-id="3142c-126">Запрос возвращает структуру [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) .</span><span class="sxs-lookup"><span data-stu-id="3142c-126">The query returns a [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) structure.</span></span>

## <a name="example-code"></a><span data-ttu-id="3142c-127">Пример кода</span><span class="sxs-lookup"><span data-stu-id="3142c-127">Example Code</span></span>

<span data-ttu-id="3142c-128">В следующем примере показаны две функции, измеряющие нехватку памяти.</span><span class="sxs-lookup"><span data-stu-id="3142c-128">The following example shows two functions that measure memory pressure.</span></span> <span data-ttu-id="3142c-129">Первый начинает интервал измерения, а второй извлекает результаты измерения.</span><span class="sxs-lookup"><span data-stu-id="3142c-129">The first begins the measurement interval, and the second retrieves the results of the measurement.</span></span>


```C++
HRESULT BeginMemoryPressureQuery(
    IDirect3DDevice9Ex *pDevice, 
    IDirect3DQuery9 **ppQuery
    )
{
    HRESULT hr = pDevice->CreateQuery(D3DQUERYTYPE_MEMORYPRESSURE, ppQuery);

    if (SUCCEEDED(hr))
    {
        hr = (*ppQuery)->Issue(D3DISSUE_BEGIN);
        if (FAILED(hr))
        {
            (*ppQuery)->Release();
            *ppQuery = NULL;
        }
    }
    return hr;
}

HRESULT EndMemoryPressureQuery(
    IDirect3DQuery9 *pQuery, 
    D3DMEMORYPRESSURE *pResult
    )
{
    HRESULT hr = pQuery->Issue(D3DISSUE_END);
    if (SUCCEEDED(hr))
    {
        hr = pQuery->GetData(pResult, sizeof(*pResult), D3DGETDATA_FLUSH);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="3142c-130">См. также</span><span class="sxs-lookup"><span data-stu-id="3142c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3142c-131">API-интерфейсы видео Direct3D</span><span class="sxs-lookup"><span data-stu-id="3142c-131">Direct3D Video APIs</span></span>](direct3d-video-apis.md)
</dt> </dl>

 

 



