---
description: 'Метод IDirect3DDevice9:: Сетстреамсаурце привязывает буфер вершин к потоку данных устройства, создавая связь между данными вершин и одним из нескольких портов потока данных, которые передаются примитивным функциям обработки.'
ms.assetid: ef317537-3095-435d-b0f2-83cb3b385da2
title: Настройка источника потока (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91bd760b23204de2c6ccd313b164ac7536c7db2d3e2da26d7e40b7d98daa60a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044242"
---
# <a name="setting-the-stream-source-direct3d-9"></a>Настройка источника потока (Direct3D 9)

Метод [**IDirect3DDevice9:: сетстреамсаурце**](/windows/desktop/api) привязывает буфер вершин к потоку данных устройства, создавая связь между данными вершин и одним из нескольких портов потока данных, которые передаются примитивным функциям обработки. Фактические ссылки на потоковые данные не выполняются до тех пор, пока не будет вызван метод рисования, например [**IDirect3DDevice9::D равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).

Поток определяется как универсальный массив данных компонента, где каждый компонент состоит из одного или нескольких элементов, представляющих одну сущность, такую как «расположение», «нормальный», «цвет» и т. д. Параметр STRIDE задает размер компонента в байтах.

В следующем примере кода показано задание источника потока и рисование его содержимого. Переменная g \_ ПВБ — это LPDIRECT3DVERTEXBUFFER9, содержащий данные вершин.


```
if( SUCCEEDED( g_pd3dDevice->BeginScene() ) )
{
    // Setup the world, view, and projection matrices
    SetupMatrices();

    // Render the vertex buffer contents
    g_pd3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
    g_pd3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
    g_pd3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 1 );

    // End the scene
    g_pd3dDevice->EndScene();
}
```



Дополнительные сведения об этом коде см. в следующем учебнике: [учебник 3. использование матриц](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Отрисовка примитивов](rendering-primitives.md)
</dt> </dl>

 

 
