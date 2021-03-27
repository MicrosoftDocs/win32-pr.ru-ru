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
# <a name="how-to-enumerate-adapters"></a>Руководство. Перечисление адаптеров

В этом разделе показано, как использовать графическую инфраструктуру Microsoft DirectX (DXGI) для перечисления доступных графических адаптеров на компьютере. Direct3D 10 и 11 могут использовать DXGI для перечисления адаптеров.

Обычно необходимо перечислить адаптеры по следующим причинам:

-   Для определения того, сколько графических адаптеров установлено на компьютере.
-   Чтобы помочь выбрать адаптер, который будет использоваться для создания устройства Direct3D.
-   Для получения объекта [**идксгиадаптер**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) , который можно использовать для получения возможностей устройства.

**Перечисление адаптеров**

1.  Создайте объект [**идксгифактори**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) , вызвав функцию [**креатедксгифактори**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory) . В следующем примере кода показано, как инициализировать объект **идксгифактори** .
    ```
    IDXGIFactory * pFactory = NULL;

    CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)
    ```

    

2.  Перечислите каждый адаптер, вызвав метод [**идксгифактори:: енумадаптерс**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) . Параметр *Adapter* позволяет указать номер индекса адаптера (с отсчетом от нуля) для перечисления. Если адаптер по указанному индексу недоступен, метод возвращает [**ошибку DXGI, \_ \_ не \_ найденный**](/windows/desktop/direct3ddxgi/dxgi-error).

    В следующем примере кода показано, как перечислить адаптеры на компьютере.

    ```
    for (UINT i = 0; 
         pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND; 
         ++i) 
    { ... }
    ```

    

В следующем примере кода показано, как перечислить все адаптеры на компьютере.

> [!Note]  
> Для Direct3D 11,0 и более поздних версий рекомендуется, чтобы приложения всегда использовали [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) и [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) .

 


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 