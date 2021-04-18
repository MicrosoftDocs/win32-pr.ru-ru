---
description: Термин Блит является сокращением для &\# 0034; передача битового блока &\# 0034; что представляет собой процесс передачи блоков данных из одного места в памяти в другое.
ms.assetid: 5f2aed2e-66d2-40e6-be35-92c3f92d17bd
title: Копирование поверхностей (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50000e3b620c4d2fd217695551d898e5892430ba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692026"
---
# <a name="copying-surfaces-direct3d-9"></a><span data-ttu-id="8ad81-103">Копирование поверхностей (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8ad81-103">Copying Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="8ad81-104">Термин Блит является сокращением для "передачи битового блока", который представляет собой процесс передачи блоков данных из одного места в памяти в другое.</span><span class="sxs-lookup"><span data-stu-id="8ad81-104">The term blit is shorthand for "bit block transfer," which is the process of transferring blocks of data from one place in memory to another.</span></span> <span data-ttu-id="8ad81-105">Интерфейс драйвера устройства блиттинг (DDI) по-своему используется в Direct3D 9 в качестве основного механизма перемещения больших прямоугольников пикселей в зависимости от каждого кадра, механизма копирования, ориентированного на метод повторного выполнения [**IDirect3DDevice9::P**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="8ad81-105">The blitting device driver interface (DDI) continues to be used in Direct3D 9 as the primary mechanism for moving large rectangles of pixels on a per-frame basis, the mechanism behind the copy-oriented [**IDirect3DDevice9::Present**](/windows/desktop/api) method.</span></span> <span data-ttu-id="8ad81-106">Транспорт иллюстраций в операции Блит выполняется методом [**IDirect3DDevice9:: упдатетекстуре**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="8ad81-106">The transportation of artwork in the blit operation is performed by the [**IDirect3DDevice9::UpdateTexture**](/windows/desktop/api) method.</span></span> <span data-ttu-id="8ad81-107">Кроме того, иллюстрацию можно скопировать в Direct3D 9 с помощью метода [**IDirect3DDevice9:: упдатесурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) , который копирует прямоугольное подмножество пикселей.</span><span class="sxs-lookup"><span data-stu-id="8ad81-107">Artwork can also be copied in Direct3D 9 by using the [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) method, which copies a rectangular subset of pixels.</span></span>

> [!Note]  
> <span data-ttu-id="8ad81-108">Direct3D 9 предоставляет функции D3DX, позволяющие загружать иллюстрации из файлов, применять преобразование цветов и изменять размеры иллюстраций.</span><span class="sxs-lookup"><span data-stu-id="8ad81-108">Direct3D 9 provides D3DX functions that enable you to load artwork from files, apply color conversion, and resize artwork.</span></span> <span data-ttu-id="8ad81-109">Дополнительные сведения о доступных функциях см. [в разделе функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md).</span><span class="sxs-lookup"><span data-stu-id="8ad81-109">For more information about the available functions see [Texture Functions in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8ad81-110">См. также</span><span class="sxs-lookup"><span data-stu-id="8ad81-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ad81-111">Поверхности Direct3D</span><span class="sxs-lookup"><span data-stu-id="8ad81-111">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="8ad81-112">**IDirect3DDevice9:: Стретчрект**</span><span class="sxs-lookup"><span data-stu-id="8ad81-112">**IDirect3DDevice9::StretchRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> <dt>

<span data-ttu-id="8ad81-113">**IDirect3DDevice9:: Стретчрект**</span><span class="sxs-lookup"><span data-stu-id="8ad81-113">**IDirect3DDevice9::StretchRect**</span></span>
</dt> </dl>

 

 
