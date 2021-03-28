---
title: Операции, доступные для мозаичных ресурсов
description: В этом разделе перечислены операции, которые можно выполнять с мозаичными ресурсами.
ms.assetid: 1CF42A18-B6EA-4BA9-BEDE-9A8CC083CBAF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45d051943816502fd0bafb77e67241026f31498
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068398"
---
# <a name="operations-available-on-tiled-resources"></a>Операции, доступные для мозаичных ресурсов

В этом разделе перечислены операции, которые можно выполнять с мозаичными ресурсами.

-   void [**ID3D11DeviceContext2:: упдатетилемаппингс**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) and [**ID3D11DeviceContext2:: копитилемаппингс**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) Operations — эти расположения плиток точек в мозаичном ресурсе для размещения в пулах плиток, а также для значений NULL или для обоих. Эти операции могут обновлять раздельные подмножества указателей плиток.
-   \*Операции копирования () и Update \* () — все API-интерфейсы, которые могут копировать данные в рабочую область пула по умолчанию (например, [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) и [**ID3D11DeviceContext1:: UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)), работают для мозаичных ресурсов. Чтение из несопоставленных плиток дает 0, а операции записи в несопоставленные плитки не выполняются.
-   Операции [**ID3D11DeviceContext2:: копитилес**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) и [**ID3D11DeviceContext2:: упдатетилес**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) . Эти операции существуют для копирования плиток по степени гранулярности 64 КБ на детализацию и из любого ресурса-буфера в каноническом макете памяти. Видеодрайвер и оборудование выполняют любую память "группирующие", необходимую для мозаичного ресурса.
-   Привязки конвейера Direct3D и представления и привязки представлений, которые будут работать с ресурсами, не являющимися мозаичными, работают и для мозаичных ресурсов.

Элементы управления плиткой доступны в немедленных и отложенных контекстах (так же, как и обновления типичных ресурсов) и после выполнения влияют на последующие обращения к плиткам (но не ранее отправленные операции).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание мозаичных ресурсов](creating-tiled-resources.md)
</dt> </dl>

 

 




