---
description: 'Отрисовка данных вершин из буфера вершин требует выполнения нескольких шагов. Сначала необходимо задать источник потока, вызвав метод IDirect3DDevice9:: Сетстреамсаурце, как показано в следующем примере.'
ms.assetid: a0435a3d-e1dd-4365-904d-8e5713e379ce
title: Подготовка к просмотру из буфера вершин (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cebb68c5395a827a9aee4ea1f8465257c436bb7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139271"
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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Буферы вершин](vertex-buffers.md)
</dt> <dt>

[Отрисовка из буферов вершин и индексов (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> </dl>

 

 
