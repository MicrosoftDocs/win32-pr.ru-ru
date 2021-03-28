---
title: Воспроизведение списка команд
description: В этом разделе показано, как воспроизвести список команд.
ms.assetid: 4e6c0a98-85ff-45ca-963b-7d5c55f47195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d04df73b481adea17e1f985e2c1851039fd016a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996767"
---
# <a name="how-to-play-back-a-command-list"></a>Как воспроизвести список команд

[Список](overviews-direct3d-11-render-multi-thread-command-list.md) команд — это записанный список команд подготовки к просмотру. Используйте список команд для предварительной записи команд рисования и воспроизведения их позже. В этом разделе показано, как воспроизвести [список команд](overviews-direct3d-11-render-multi-thread-command-list.md). Список команд можно использовать для разделения задач визуализации между потоками.

В этом разделе описывается воспроизведение списка команд. Сведения о записи списка команд см. [в разделе как записать список команд](overviews-direct3d-11-render-multi-thread-command-list-record.md).

**Воспроизведение списка команд**

-   Вызовите [**ссылку ID3D11DeviceContext:: вызова элемента executecommandlist**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) и передайте допустимый объект [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) .
    ```
    if(g_pd3dCommandList)
    {
        g_pImmediateContext->ExecuteCommandList(g_pd3dCommandList, TRUE);
    }
    ```

    

[**Вызова элемента executecommandlist**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) должен выполняться в [непосредственных контекстах](overviews-direct3d-11-devices-intro.md) для записанных команд, которые должны выполняться в графическом процессоре. Используйте непосредственный контекст для передачи команд в GPU для выполнения, используйте отложенный контекст для записи команд для воспроизведения в другой список команд. При вызове **вызова элемента executecommandlist** в другом отложенном контексте создается список отложенных команд. Чтобы выполнить команды в объединенном списке отложенных команд, необходимо выполнить их в непосредственных контекстах.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Список команд](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[Использование Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




