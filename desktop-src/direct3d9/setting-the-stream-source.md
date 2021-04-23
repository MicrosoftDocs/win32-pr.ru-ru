---
description: 'Метод IDirect3DDevice9:: Сетстреамсаурце привязывает буфер вершин к потоку данных устройства, создавая связь между данными вершин и одним из нескольких портов потока данных, которые передаются примитивным функциям обработки.'
ms.assetid: ef317537-3095-435d-b0f2-83cb3b385da2
title: Настройка источника потока (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76d0c296b79d258be6eee2d683979081673d5d04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537586"
---
# <a name="setting-the-stream-source-direct3d-9"></a><span data-ttu-id="78e43-103">Настройка источника потока (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="78e43-103">Setting the Stream Source (Direct3D 9)</span></span>

<span data-ttu-id="78e43-104">Метод [**IDirect3DDevice9:: сетстреамсаурце**](/windows/desktop/api) привязывает буфер вершин к потоку данных устройства, создавая связь между данными вершин и одним из нескольких портов потока данных, которые передаются примитивным функциям обработки.</span><span class="sxs-lookup"><span data-stu-id="78e43-104">The [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api) method binds a vertex buffer to a device data stream, creating an association between the vertex data and one of several data stream ports that feed the primitive processing functions.</span></span> <span data-ttu-id="78e43-105">Фактические ссылки на потоковые данные не выполняются до тех пор, пока не будет вызван метод рисования, например [**IDirect3DDevice9::D равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="78e43-105">The actual references to the stream data do not occur until a drawing method, such as [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), is called.</span></span>

<span data-ttu-id="78e43-106">Поток определяется как универсальный массив данных компонента, где каждый компонент состоит из одного или нескольких элементов, представляющих одну сущность, такую как «расположение», «нормальный», «цвет» и т. д.</span><span class="sxs-lookup"><span data-stu-id="78e43-106">A stream is defined as a uniform array of component data, where each component consists of one or more elements representing a single entity such as position, normal, color, and so on.</span></span> <span data-ttu-id="78e43-107">Параметр STRIDE задает размер компонента в байтах.</span><span class="sxs-lookup"><span data-stu-id="78e43-107">The Stride parameter specifies the size of the component, in bytes.</span></span>

<span data-ttu-id="78e43-108">В следующем примере кода показано задание источника потока и рисование его содержимого.</span><span class="sxs-lookup"><span data-stu-id="78e43-108">The following code demonstrates setting the stream source and drawing its contents.</span></span> <span data-ttu-id="78e43-109">Переменная g \_ ПВБ — это LPDIRECT3DVERTEXBUFFER9, содержащий данные вершин.</span><span class="sxs-lookup"><span data-stu-id="78e43-109">The g\_pVB variable is a LPDIRECT3DVERTEXBUFFER9 that contains vertex data.</span></span>


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



<span data-ttu-id="78e43-110">Дополнительные сведения об этом коде см. в следующем учебнике: [учебник 3. использование матриц](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="78e43-110">For more information about this code see the following tutorial: [Tutorial 3: Using Matrices](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)</span></span>

## <a name="related-topics"></a><span data-ttu-id="78e43-111">См. также</span><span class="sxs-lookup"><span data-stu-id="78e43-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78e43-112">Отрисовка примитивов</span><span class="sxs-lookup"><span data-stu-id="78e43-112">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
