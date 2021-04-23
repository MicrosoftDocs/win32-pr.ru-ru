---
title: Примеры кода пакета SDK для формата Windows Media
description: Примеры кода пакета SDK для формата Windows Media
ms.assetid: 1459a438-d42c-4d84-baa8-fc672f5d5d27
keywords:
- Windows Media Format SDK, примеры кода
- Windows Media Format SDK, пример кода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db438a8cb42bbb45768421cc34c129f19948f1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414660"
---
# <a name="using-the-windows-media-format-sdk-code-examples"></a><span data-ttu-id="968b8-105">Примеры кода пакета SDK для формата Windows Media</span><span class="sxs-lookup"><span data-stu-id="968b8-105">Using the Windows Media Format SDK Code Examples</span></span>

<span data-ttu-id="968b8-106">Многие из объясненных разделов этого пакета SDK включают примеры кода.</span><span class="sxs-lookup"><span data-stu-id="968b8-106">Many of the explanatory sections of this SDK include code examples.</span></span> <span data-ttu-id="968b8-107">Примеры записываются как можно более четкие и лаконичные.</span><span class="sxs-lookup"><span data-stu-id="968b8-107">The examples are written to be as clear and concise as possible.</span></span> <span data-ttu-id="968b8-108">При чтении примеров следует учитывать следующие соглашения.</span><span class="sxs-lookup"><span data-stu-id="968b8-108">When reading the examples, you should be aware of the following conventions.</span></span>

-   <span data-ttu-id="968b8-109">Предполагается, что все примеры включают в себя Windows. h и вмсдк. h.</span><span class="sxs-lookup"><span data-stu-id="968b8-109">All examples are assumed to include windows.h and wmsdk.h.</span></span> <span data-ttu-id="968b8-110">Все необходимые файлы заголовков упоминаются в пояснительном тексте.</span><span class="sxs-lookup"><span data-stu-id="968b8-110">Any other required header files are mentioned in the explanatory text.</span></span>
-   <span data-ttu-id="968b8-111">В случае возникновения ошибки проверка ошибок была ограничена до выхода из функции.</span><span class="sxs-lookup"><span data-stu-id="968b8-111">Error checking has been restricted to breaking out of the function if an error occurs.</span></span> <span data-ttu-id="968b8-112">В приложении следует проверить определенные коды ошибок и предоставить некоторый тип отчетов об ошибках.</span><span class="sxs-lookup"><span data-stu-id="968b8-112">In an application, you should check for specific error codes and provide some kind of error reporting.</span></span>

    <span data-ttu-id="968b8-113">При проверке возвращаемых значений методов или функций, возвращающих значение **HRESULT** , следует использовать макрос **Failed** , чтобы определить, указывает ли возвращаемое значение на ошибку.</span><span class="sxs-lookup"><span data-stu-id="968b8-113">When checking return values from methods or functions that return an **HRESULT** value, you should use the **FAILED** macro to discover whether the return value indicates failure.</span></span>

    ```C++
    HRESULT hr;
    hr = SomeFunction();
    if (FAILED(hr))
    {
       // Check for specific error values.
    }
    ```

    

    <span data-ttu-id="968b8-114">Во многих примерах в этой документации используется макрос с именем GOTO \_ exit \_ \_ , если сбой, который определен в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="968b8-114">Many of the examples in this documentation use a macro named GOTO\_EXIT\_IF\_FAILED, which is defined in the following code.</span></span>

    ```C++
    #ifndef GOTO_EXIT_IF_FAILED
    #define GOTO_EXIT_IF_FAILED(hr) if(FAILED(hr)) goto Exit;
    #endif
    ```

    

    <span data-ttu-id="968b8-115">Эти примеры функций имеют тег «Exit:», после чего возвращаются все интерфейсы и память, выделенные в функции, и код ошибки, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="968b8-115">These example functions each have a tag named "Exit:", after which all interfaces and memory allocated in the function are released and the error code, if any, is returned.</span></span>

-   <span data-ttu-id="968b8-116">Интерфейсы и память освобождаются в примерах кода с помощью макросов с именем безопасного \_ выпуска и безопасного \_ массива \_ Delete.</span><span class="sxs-lookup"><span data-stu-id="968b8-116">Interfaces and memory are released in the code examples using macros named SAFE\_RELEASE and SAFE\_ARRAY\_DELETE.</span></span> <span data-ttu-id="968b8-117">Эти макросы определяются в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="968b8-117">These macros are defined in the following code:</span></span>
    ```C++
    #ifndef SAFE_RELEASE
    #define SAFE_RELEASE(x) \
       if(x != NULL)        \
       {                    \
          x->Release();     \
          x = NULL;         \
       }
    #endif

    #ifndef SAFE_ARRAY_DELETE
    #define SAFE_ARRAY_DELETE(x) \
       if(x != NULL)             \
       {                         \
          delete[] x;            \
          x = NULL;              \
       }
    #endif
    ```

    

-   <span data-ttu-id="968b8-118">Часто необходимо включить логику одного примера в другой пример, чтобы пример был осмысленным.</span><span class="sxs-lookup"><span data-stu-id="968b8-118">Often, you will need to include the logic of one example in another example for the example to be meaningful.</span></span> <span data-ttu-id="968b8-119">В этих случаях включается комментарий TODO со ссылкой на соответствующий пример кода.</span><span class="sxs-lookup"><span data-stu-id="968b8-119">In those instances, a TODO comment is included, with a reference to the appropriate code example.</span></span>
-   <span data-ttu-id="968b8-120">Чтобы сделать код более удобочитаемым, ни один из примеров функций в этой документации не проверит их входные параметры.</span><span class="sxs-lookup"><span data-stu-id="968b8-120">To make the code easier to read, none of the example functions in this documentation validate their input parameters.</span></span> <span data-ttu-id="968b8-121">При копировании любой из этих функций в код следует проверить все входные параметры.</span><span class="sxs-lookup"><span data-stu-id="968b8-121">If you copy any of these functions into your code, you should validate any input parameters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="968b8-122">См. также</span><span class="sxs-lookup"><span data-stu-id="968b8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="968b8-123">**начало работы**</span><span class="sxs-lookup"><span data-stu-id="968b8-123">**Getting Started**</span></span>](getting-started.md)
</dt> </dl>

 

 




