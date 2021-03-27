---
title: Перечисление адаптеров
description: В этом разделе показано, как использовать графическую инфраструктуру Microsoft DirectX (DXGI) для перечисления доступных графических адаптеров на компьютере.
ms.assetid: f8ef981c-363e-4ac8-8734-69c68f346950
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af16aba0131d93a5f72732931a68f132126b5d48
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997107"
---
# <a name="how-to-enumerate-adapters"></a><span data-ttu-id="dc7b2-103">Руководство. Перечисление адаптеров</span><span class="sxs-lookup"><span data-stu-id="dc7b2-103">How To: Enumerate Adapters</span></span>

<span data-ttu-id="dc7b2-104">В этом разделе показано, как использовать графическую инфраструктуру Microsoft DirectX (DXGI) для перечисления доступных графических адаптеров на компьютере.</span><span class="sxs-lookup"><span data-stu-id="dc7b2-104">This topic shows how to use Microsoft DirectX Graphics Infrastructure (DXGI) to enumerate the available graphics adapters on a computer.</span></span> <span data-ttu-id="dc7b2-105">Direct3D 10 и 11 могут использовать DXGI для перечисления адаптеров.</span><span class="sxs-lookup"><span data-stu-id="dc7b2-105">Direct3D 10 and 11 can use DXGI to enumerate adapters.</span></span>

<span data-ttu-id="dc7b2-106">Обычно необходимо перечислить адаптеры по следующим причинам:</span><span class="sxs-lookup"><span data-stu-id="dc7b2-106">You generally need to enumerate adapters for these reasons:</span></span>

-   <span data-ttu-id="dc7b2-107">Для определения того, сколько графических адаптеров установлено на компьютере.</span><span class="sxs-lookup"><span data-stu-id="dc7b2-107">To determine how many graphics adapters are installed on a computer.</span></span>
-   <span data-ttu-id="dc7b2-108">Чтобы помочь выбрать адаптер, который будет использоваться для создания устройства Direct3D.</span><span class="sxs-lookup"><span data-stu-id="dc7b2-108">To help you choose which adapter to use to create a Direct3D device.</span></span>
-   <span data-ttu-id="dc7b2-109">Для получения объекта [**идксгиадаптер**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) , который можно использовать для получения возможностей устройства.</span><span class="sxs-lookup"><span data-stu-id="dc7b2-109">To retrieve an [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) object that you can use to retrieve device capabilities.</span></span>

<span data-ttu-id="dc7b2-110">**Перечисление адаптеров**</span><span class="sxs-lookup"><span data-stu-id="dc7b2-110">**To enumerate adapters**</span></span>

1.  <span data-ttu-id="dc7b2-111">Создайте объект [**идксгифактори**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) , вызвав функцию [**креатедксгифактори**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory) .</span><span class="sxs-lookup"><span data-stu-id="dc7b2-111">Create an [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) object by calling the [**CreateDXGIFactory**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory) function.</span></span> <span data-ttu-id="dc7b2-112">В следующем примере кода показано, как инициализировать объект **идксгифактори** .</span><span class="sxs-lookup"><span data-stu-id="dc7b2-112">The following code example demonstrates how to initialize an **IDXGIFactory** object.</span></span>
    ```
    IDXGIFactory * pFactory = NULL;

    CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)
    ```

    

2.  <span data-ttu-id="dc7b2-113">Перечислите каждый адаптер, вызвав метод [**идксгифактори:: енумадаптерс**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) .</span><span class="sxs-lookup"><span data-stu-id="dc7b2-113">Enumerate through each adapter by calling the [**IDXGIFactory::EnumAdapters**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) method.</span></span> <span data-ttu-id="dc7b2-114">Параметр *Adapter* позволяет указать номер индекса адаптера (с отсчетом от нуля) для перечисления.</span><span class="sxs-lookup"><span data-stu-id="dc7b2-114">The *Adapter* parameter allows you to specify a zero-based index number of the adapter to enumerate.</span></span> <span data-ttu-id="dc7b2-115">Если адаптер по указанному индексу недоступен, метод возвращает [**ошибку DXGI, \_ \_ не \_ найденный**](/windows/desktop/direct3ddxgi/dxgi-error).</span><span class="sxs-lookup"><span data-stu-id="dc7b2-115">If no adapter is available at the specified index, the method returns [**DXGI\_ERROR\_NOT\_FOUND**](/windows/desktop/direct3ddxgi/dxgi-error).</span></span>

    <span data-ttu-id="dc7b2-116">В следующем примере кода показано, как перечислить адаптеры на компьютере.</span><span class="sxs-lookup"><span data-stu-id="dc7b2-116">The following code example demonstrates how to enumerate through the adapters on a computer.</span></span>

    ```
    for (UINT i = 0; 
         pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND; 
         ++i) 
    { ... }
    ```

    

<span data-ttu-id="dc7b2-117">В следующем примере кода показано, как перечислить все адаптеры на компьютере.</span><span class="sxs-lookup"><span data-stu-id="dc7b2-117">The following code example demonstrates how to enumerate all adapters on a computer.</span></span>

> [!Note]  
> <span data-ttu-id="dc7b2-118">Для Direct3D 11,0 и более поздних версий рекомендуется, чтобы приложения всегда использовали [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) и [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) .</span><span class="sxs-lookup"><span data-stu-id="dc7b2-118">For Direct3D 11.0 and later, we recommend that apps always use [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) and [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) instead.</span></span>

 


```C++
std::vector <IDXGIAdapter*> EnumerateAdapters(void)
{
    IDXGIAdapter * pAdapter; 
    std::vector <IDXGIAdapter*> vAdapters; 
    IDXGIFactory* pFactory = NULL; 
    

    // Create a DXGIFactory object.
    if(FAILED(CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)))
    {
        return vAdapters;
    }


    for ( UINT i = 0;
          pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND;
          ++i )
    {
        vAdapters.push_back(pAdapter); 
    } 


    if(pFactory)
    {
        pFactory->Release();
    }

    return vAdapters;

}
```



## <a name="related-topics"></a><span data-ttu-id="dc7b2-119">См. также</span><span class="sxs-lookup"><span data-stu-id="dc7b2-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc7b2-120">Использование Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="dc7b2-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 