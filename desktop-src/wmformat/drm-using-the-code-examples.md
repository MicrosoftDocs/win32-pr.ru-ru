---
title: Примеры кода клиента DRM для Microsoft Windows Media
description: Примеры кода клиента DRM для Microsoft Windows Media
ms.assetid: 75db2663-9eb8-406d-b1a9-8f6092c95f9d
keywords:
- Windows Media Format SDK, примеры кода
- Windows Media Format SDK, пример кода
- Windows Media Format SDK, примеры кода DRM
- Управление цифровыми правами (DRM), примеры кода
- DRM (Управление цифровыми правами), примеры кода
- Управление цифровыми правами (DRM), пример кода
- DRM (Управление цифровыми правами), пример кода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 054d1ed804873c8aca104203ee1f235ecb3856f5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414420"
---
# <a name="using-the-microsoft-windows-media-drm-client-code-examples"></a><span data-ttu-id="7de6f-110">Примеры кода клиента DRM для Microsoft Windows Media</span><span class="sxs-lookup"><span data-stu-id="7de6f-110">Using the Microsoft Windows Media DRM Client Code Examples</span></span>

<span data-ttu-id="7de6f-111">Примеры кода включены в эту документацию, чтобы продемонстрировать использование компонентов.</span><span class="sxs-lookup"><span data-stu-id="7de6f-111">Code examples are included in this documentation to illustrate the use of components.</span></span> <span data-ttu-id="7de6f-112">Примеры записываются как можно более четкие и лаконичные.</span><span class="sxs-lookup"><span data-stu-id="7de6f-112">The examples are written to be as clear and concise as possible.</span></span> <span data-ttu-id="7de6f-113">При чтении примеров следует учитывать следующие соглашения.</span><span class="sxs-lookup"><span data-stu-id="7de6f-113">When reading the examples, you should be aware of the following conventions.</span></span>

-   <span data-ttu-id="7de6f-114">Предполагается, что все примеры включают в себя Windows. h и вмдрмсдк. h.</span><span class="sxs-lookup"><span data-stu-id="7de6f-114">All examples are assumed to include windows.h and wmdrmsdk.h.</span></span> <span data-ttu-id="7de6f-115">В примере будет содержаться Примечание, если для компиляции требуются другие заголовки.</span><span class="sxs-lookup"><span data-stu-id="7de6f-115">The example will include a note if it requires other headers in order to compile.</span></span>
-   <span data-ttu-id="7de6f-116">В случае возникновения ошибки проверка ошибок была ограничена до выхода из функции.</span><span class="sxs-lookup"><span data-stu-id="7de6f-116">Error checking has been restricted to breaking out of the function if an error occurs.</span></span> <span data-ttu-id="7de6f-117">В приложении следует проверить определенные коды ошибок и предоставить некоторый тип отчетов об ошибках.</span><span class="sxs-lookup"><span data-stu-id="7de6f-117">In an application, you should check for specific error codes and provide some kind of error reporting.</span></span>
-   <span data-ttu-id="7de6f-118">Интерфейсы и память освобождаются в примерах кода с помощью макросов с именем безопасного \_ выпуска и безопасного \_ массива \_ Delete.</span><span class="sxs-lookup"><span data-stu-id="7de6f-118">Interfaces and memory are released in the code examples using macros named SAFE\_RELEASE and SAFE\_ARRAY\_DELETE.</span></span> <span data-ttu-id="7de6f-119">Эти макросы определяются в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="7de6f-119">These macros are defined in the following code:</span></span>
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

    

## <a name="related-topics"></a><span data-ttu-id="7de6f-120">См. также</span><span class="sxs-lookup"><span data-stu-id="7de6f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7de6f-121">**начало работы**</span><span class="sxs-lookup"><span data-stu-id="7de6f-121">**Getting Started**</span></span>](drm-getting-started.md)
</dt> </dl>

 

 




