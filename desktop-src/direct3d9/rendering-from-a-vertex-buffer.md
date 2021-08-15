---
description: 'Отрисовка данных вершин из буфера вершин требует выполнения нескольких шагов. Сначала необходимо задать источник потока, вызвав метод IDirect3DDevice9:: Сетстреамсаурце, как показано в следующем примере.'
ms.assetid: a0435a3d-e1dd-4365-904d-8e5713e379ce
title: Подготовка к просмотру из буфера вершин (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ee3d477fc812d2dabed765e28bb14452a6badf746a331a13283108ef46b47c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520075"
---
# <a name="rendering-from-a-vertex-buffer-direct3d-9"></a>Подготовка к просмотру из буфера вершин (Direct3D 9)

Отрисовка данных вершин из буфера вершин требует выполнения нескольких шагов. Сначала необходимо задать источник потока, вызвав метод [**IDirect3DDevice9:: сетстреамсаурце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) , как показано в следующем примере.


```
d3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
```



Первый параметр [**IDirect3DDevice9:: сетстреамсаурце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) указывает Direct3D на источник потока данных устройства. Вторым параметром является буфер вершин для привязки к потоку данных. Третий параметр — смещение от начала потока до начала данных вершин в байтах. Четвертый параметр — это шаг компонента в байтах. В приведенном выше образце кода размер КУСТОМВЕРТЕКС используется для шага компонента.

Следующим шагом является информирование Direct3D о том, какой шейдер вершин использовать, вызвав метод [**IDirect3DDevice9:: сетвертексшадер**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) . В следующем примере кода задается код ФВФ для шейдера вершин. Это информирует Direct3D о типах вершин, с которыми он работает.


```
d3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
```



После установки источника потока и шейдера вершин все методы рисования будут использовать буфер вершин. В приведенном ниже примере кода показано, как визуализировать вершины из буфера вершин с помощью метода [**IDirect3DDevice9::D равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .


```
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 1 );
```



Второй параметр, [**IDirect3DDevice9::D равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) , принимает индекс первого вектора в буфере вершин для загрузки.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Буферы вершин](vertex-buffers.md)
</dt> <dt>

[Отрисовка из буферов вершин и индексов (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> </dl>

 

 
