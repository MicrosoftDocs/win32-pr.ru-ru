---
description: 'Существует два способа добавления тумана в сцену: с пиксельным туманом и (или) вершиной тумана.'
ms.assetid: 96531830-2df1-40d4-af46-09b1ca153834
title: Типы тумана (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b5dd845373ac4a42a32ab7a9965501df4894568
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139563"
---
# <a name="fog-types-direct3d-9"></a><span data-ttu-id="39bf1-103">Типы тумана (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="39bf1-103">Fog Types (Direct3D 9)</span></span>

<span data-ttu-id="39bf1-104">Существует два способа добавления тумана в сцену: с пиксельным туманом и (или) вершиной тумана.</span><span class="sxs-lookup"><span data-stu-id="39bf1-104">There are two ways to add fog to a scene: with pixel fog and/or vertex fog.</span></span> <span data-ttu-id="39bf1-105">В следующих разделах показаны формулы, используемые в уравнениях тумана, а также реализация вершин и пиксельных туманов.</span><span class="sxs-lookup"><span data-stu-id="39bf1-105">The following topics illustrate the formulas used in fog equations, as well as implementing vertex and pixel fog.</span></span> <span data-ttu-id="39bf1-106">Приложение может реализовать туман с шейдером вершин и одновременно при необходимости пиксельный туман.</span><span class="sxs-lookup"><span data-stu-id="39bf1-106">An application can implement fog with a vertex shader, and pixel fog simultaneously if desired.</span></span>

-   [<span data-ttu-id="39bf1-107">Формулы тумана</span><span class="sxs-lookup"><span data-stu-id="39bf1-107">Fog Formulas</span></span>](fog-formulas.md)
-   [<span data-ttu-id="39bf1-108">Параметры тумана</span><span class="sxs-lookup"><span data-stu-id="39bf1-108">Fog Parameters</span></span>](fog-parameters.md)
-   [<span data-ttu-id="39bf1-109">Смешение тумана</span><span class="sxs-lookup"><span data-stu-id="39bf1-109">Fog Blending</span></span>](fog-blending.md)
-   [<span data-ttu-id="39bf1-110">Цвет тумана</span><span class="sxs-lookup"><span data-stu-id="39bf1-110">Fog Color</span></span>](fog-color.md)
-   [<span data-ttu-id="39bf1-111">Вершинный туман</span><span class="sxs-lookup"><span data-stu-id="39bf1-111">Vertex Fog</span></span>](vertex-fog.md)
-   [<span data-ttu-id="39bf1-112">Пиксельный туман</span><span class="sxs-lookup"><span data-stu-id="39bf1-112">Pixel Fog</span></span>](pixel-fog.md)

<span data-ttu-id="39bf1-113">Смешение тумана управляется состояниями отрисовки; Он не является частью программируемого конвейера пикселей.</span><span class="sxs-lookup"><span data-stu-id="39bf1-113">Fog blending is controlled by render states; it is not part of the programmable pixel pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39bf1-114">См. также</span><span class="sxs-lookup"><span data-stu-id="39bf1-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39bf1-115">Буфер кадров</span><span class="sxs-lookup"><span data-stu-id="39bf1-115">Frame Buffer</span></span>](frame-buffer.md)
</dt> </dl>

 

 



