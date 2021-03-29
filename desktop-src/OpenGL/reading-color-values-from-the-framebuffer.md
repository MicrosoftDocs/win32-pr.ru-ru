---
title: Считывание значений цвета из буфера кадров
description: При использовании функций, считывающих значения цвета из буфера кадров, следует учитывать различия между чтением значений RGBA и значений цветовых индексов на true-цветных устройствах и на устройствах на основе палитры.
ms.assetid: 70a96f09-37e9-4dfe-a6e0-0223e0a04bac
keywords:
- OpenGL в Windows, считывание значений цвета из фрамебуфферс
- считывание значений цвета из фрамебуфферс OpenGL
- фрамебуфферс, считывание цветовых значений OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4df14690b68f7e93949d26ee50ac562ebd667be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774894"
---
# <a name="reading-color-values-from-the-framebuffer"></a><span data-ttu-id="d732b-106">Считывание значений цвета из буфера кадров</span><span class="sxs-lookup"><span data-stu-id="d732b-106">Reading Color Values from the Framebuffer</span></span>

<span data-ttu-id="d732b-107">При использовании функций, считывающих значения цвета из буфера кадров, следует учитывать различия между чтением значений RGBA и значений цветовых индексов на true-цветных устройствах и на устройствах на основе палитры.</span><span class="sxs-lookup"><span data-stu-id="d732b-107">When using functions that read back color values from the framebuffer, be aware of the differences between reading RGBA values and color-index values on true-color devices and on palette-based devices.</span></span>

<span data-ttu-id="d732b-108">На true-цветном устройстве:</span><span class="sxs-lookup"><span data-stu-id="d732b-108">On a true-color device:</span></span>

-   <span data-ttu-id="d732b-109">Значения RGBA ограничиваются каналом на устройстве.</span><span class="sxs-lookup"><span data-stu-id="d732b-109">RGBA values are limited to the channel in the device.</span></span>
-   <span data-ttu-id="d732b-110">Значения в цветовых индексах хранятся в буфера кадров в виде значений RGBA.</span><span class="sxs-lookup"><span data-stu-id="d732b-110">Color-index values are stored as RGBA values in the framebuffer.</span></span> <span data-ttu-id="d732b-111">При использовании этих значений необходимо выполнить обратное преобразование из RGBA в логический индекс палитры.</span><span class="sxs-lookup"><span data-stu-id="d732b-111">When using these values, you must perform an inverse translation from RGBA to the logical palette index.</span></span> <span data-ttu-id="d732b-112">Если два логических индекса имеют одинаковые значения RGBA, может возвращаться неверный индекс.</span><span class="sxs-lookup"><span data-stu-id="d732b-112">If two logical indexes have the same RGBA values, the wrong index can be returned.</span></span>

<span data-ttu-id="d732b-113">На устройстве на основе палитры:</span><span class="sxs-lookup"><span data-stu-id="d732b-113">On a palette-based device:</span></span>

-   <span data-ttu-id="d732b-114">Значения RGBA считываются из индекса в системной палитре.</span><span class="sxs-lookup"><span data-stu-id="d732b-114">RGBA values are read from an index in the system palette.</span></span> <span data-ttu-id="d732b-115">Логический индекс получается из обратной таблицы, а компоненты RGBA извлекаются.</span><span class="sxs-lookup"><span data-stu-id="d732b-115">The logical index is obtained from an inverse table, and the RGBA components are extracted.</span></span>
-   <span data-ttu-id="d732b-116">Значения цветовых индексов считываются из индекса в системную палитру, а обратная таблица используется для получения индекса логической палитры.</span><span class="sxs-lookup"><span data-stu-id="d732b-116">Color-index values are read from an index into the system palette and an inverse table is used to get the logical palette index.</span></span>

 

 




