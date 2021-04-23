---
description: Объявление вершины определяет макет буфера вершин и программирует подсистему тесселяции.
ms.assetid: 09dae498-3b33-4c33-bc7e-47f2bf784e4c
title: Объявление вершины (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c769aa6fb80de1fd83067ebb9f32b591baa8e883
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710593"
---
# <a name="vertex-declaration-direct3d-9"></a><span data-ttu-id="ba4a4-103">Объявление вершины (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ba4a4-103">Vertex Declaration (Direct3D 9)</span></span>

<span data-ttu-id="ba4a4-104">Объявление вершины определяет макет буфера вершин и программирует подсистему тесселяции.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-104">A vertex declaration defines the vertex buffer layout and programs the tessellation engine.</span></span> <span data-ttu-id="ba4a4-105">Начиная с Direct3D 9, потоки вершин выражаются в виде массива структур [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) (вместо использования кодов гибкого формата ВЕРШИН (фвф)).</span><span class="sxs-lookup"><span data-stu-id="ba4a4-105">Starting with Direct3D 9, vertex streams are expressed as an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures (instead of using flexible vertex format (FVF) codes).</span></span> <span data-ttu-id="ba4a4-106">Каждый элемент массива описывает каждый тип данных каждой вершины.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-106">Each array element describes each per-vertex data type.</span></span> <span data-ttu-id="ba4a4-107">Преобразование кодов> ФВФ в новый формат рассматривается в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="ba4a4-107">Converting FVF> codes into the new format is covered in the following topics:</span></span>

-   [<span data-ttu-id="ba4a4-108">Сопоставление кодов ФВФ с объявлением Direct3D 9 (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ba4a4-108">Mapping FVF Codes to a Direct3D 9 Declaration (Direct3D 9)</span></span>](mapping-fvf-codes-to-a-directx-9-declaration.md)
-   [<span data-ttu-id="ba4a4-109">Фиксированные коды ФВФ функций (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ba4a4-109">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)
-   [<span data-ttu-id="ba4a4-110">Сопоставление между объявлением Direct3D и кодами ФВФ (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ba4a4-110">Mapping between a Direct3D Declaration and FVF Codes (Direct3D 9)</span></span>](mapping-between-a-directx-9-declaration-and-fvf-codes.md)
-   [<span data-ttu-id="ba4a4-111">Сопоставление между объявлением Direct3D 9 и объявлением Direct3D 8 (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ba4a4-111">Mapping between a Direct3D 9 Declaration and a Direct3D 8 Declaration (Direct3D 9)</span></span>](mapping-between-a-directx-9-declaration-and-directx-8.md)
-   [<span data-ttu-id="ba4a4-112">Программирование одного или нескольких потоков (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ba4a4-112">Programming One or More Streams (Direct3D 9)</span></span>](programming-one-or-more-streams.md)

## <a name="related-topics"></a><span data-ttu-id="ba4a4-113">См. также</span><span class="sxs-lookup"><span data-stu-id="ba4a4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba4a4-114">Буферы вершин</span><span class="sxs-lookup"><span data-stu-id="ba4a4-114">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 



