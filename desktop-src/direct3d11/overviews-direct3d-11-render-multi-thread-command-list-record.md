---
title: Запись списка команд
description: В этом разделе показано, как создать и записать список команд.
ms.assetid: f5b90dfb-0b07-432e-813b-1541efbe3de5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712f48386e0625c58a1f11c122d105064477ca8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777081"
---
# <a name="how-to-record-a-command-list"></a>Как записать список команд

[Список](overviews-direct3d-11-render-multi-thread-command-list.md) команд — это записанный список команд подготовки к просмотру. В этом разделе показано, как создать и записать [список команд](overviews-direct3d-11-render-multi-thread-command-list.md). Используйте список команд для записи команд подготовки к просмотру и их последующего воспроизведения. Список команд удобно использовать для разделения задач визуализации между потоками.

**Запись списка команд**

1.  Список команд должен быть создан из отложенного контекста, который содержит состояние устройства и действия визуализации. При наличии устройства создайте отложенный контекст, вызвав [**ID3D11Device:: креатедеферредконтекст**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

    ```
    HRESULT hr;
    ID3D11DeviceContext* pDeferredContext = NULL;

    hr = g_pd3dDevice->CreateDeferredContext(0, &pDeferredContext);
    ```

    

2.  Используйте отложенный контекст для подготовки к просмотру.

    ```
    float ClearColor[4] = { 0.0f, 0.125f, 0.3f, 1.0f };
    pDeferredContext->ClearRenderTargetView( g_pRenderTargetView, ClearColor );
        
    // Add additional rendering commands
    ...
    ```

    

    В этом простом примере очищается целевой объект прорисовки, но можно добавить дополнительные команды рендеринга.

3.  Создайте или запишите список команд путем вызова [**ссылку ID3D11DeviceContext:: финишкоммандлист**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) и передачи указателя на неинициализированный интерфейс [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) .

    ```
    ID3D11CommandList* pd3dCommandList = NULL;
    HRESULT hr;
    hr = pDeferredContext->FinishCommandList(FALSE, &pd3dCommandList);
    ```

    

    При возврате из метода создается список команд, содержащий все команды рендеринга, а интерфейс возвращается приложению.

    Логический параметр указывает среде выполнения, что нужно сделать с состоянием конвейера в отложенном контексте. **Значение true** означает, что при завершении записи состояние контекста устройства будет восстановлено до состояния "до команды". **значение false** означает, что состояние не изменится после записи. Это означает, что контекст устройства будет отражать изменения состояния, содержащиеся в списке команд.

Пример воспроизведения списка команд см. в разделе [как воспроизвести список команд](overviews-direct3d-11-render-multi-thread-command-list-play.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Список команд](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[Использование Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




