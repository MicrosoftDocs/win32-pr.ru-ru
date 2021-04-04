---
description: Сопоставление окружения — это методика, которая имитирует высокоотражающие поверхности без использования трассировки лучей.
ms.assetid: vs|directx_sdk|~\environment_mapping.htm
title: Сопоставление окружения (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686f15b2f097550206f9c02cfc4104e7c9f6c030
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805614"
---
# <a name="environment-mapping-direct3d-9"></a><span data-ttu-id="3f2af-103">Сопоставление окружения (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3f2af-103">Environment Mapping (Direct3D 9)</span></span>

<span data-ttu-id="3f2af-104">Сопоставление окружения — это методика, которая имитирует высокоотражающие поверхности без использования трассировки лучей.</span><span class="sxs-lookup"><span data-stu-id="3f2af-104">Environment mapping is a technique that simulates highly reflective surfaces without using ray tracing.</span></span> <span data-ttu-id="3f2af-105">На практике сопоставление среды применяет специальную текстурную карту, содержащую изображение сцены, окружающей объект с самим объектом.</span><span class="sxs-lookup"><span data-stu-id="3f2af-105">In practice, environment mapping applies a special texture map that contains an image of the scene surrounding an object to the object itself.</span></span> <span data-ttu-id="3f2af-106">Результат приближен к появлению отраженной поверхности, достаточно близко к тому, чтобы обмануть глаза, без каких-либо сложных вычислений, участвующих в трассировке лучей.</span><span class="sxs-lookup"><span data-stu-id="3f2af-106">The result approximates the appearance of a reflective surface, close enough to fool the eye, without incurring any of the complex computations involved in ray tracing.</span></span>

<span data-ttu-id="3f2af-107">На следующем рисунке показан тип сопоставления среды, именуемого сопоставлением сферического окружения.</span><span class="sxs-lookup"><span data-stu-id="3f2af-107">The following illustration demonstrates a type of environment mapping called spherical environment mapping.</span></span> <span data-ttu-id="3f2af-108">Дополнительные сведения см. в статье [сопоставление сферического окружения](spherical-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="3f2af-108">For details, see [Spherical Environment Mapping](spherical-environment-mapping.md).</span></span>

![Иллюстрация чайник с примененной текстурой, отражающей окружающую окружение](images/spheremapped-teapot.png)

<span data-ttu-id="3f2af-110">Чайник на этом изображении отражает свое окружение. на самом деле, к объекту применяется текстура.</span><span class="sxs-lookup"><span data-stu-id="3f2af-110">The teapot in this image appears to reflect its surroundings; this is actually a texture being applied to the object.</span></span> <span data-ttu-id="3f2af-111">Поскольку сопоставление окружения использует текстуру вместе с специально вычисленными координатами текстуры, его можно выполнить в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="3f2af-111">Because environment mapping uses a texture, combined with specially computed texture coordinates, it can be performed in real-time.</span></span>

<span data-ttu-id="3f2af-112">В этом разделе содержатся сведения о выполнении двух распространенных типов сопоставления среды с Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3f2af-112">This section provides information about performing two common types of environment mapping with Direct3D.</span></span> <span data-ttu-id="3f2af-113">Существует множество типов сопоставления среды, используемых в графической отрасли, но в следующих разделах рассматриваются две наиболее распространенные формы: сопоставление кубических сред и сферическое сопоставление среды.</span><span class="sxs-lookup"><span data-stu-id="3f2af-113">There are many types of environment mapping in use throughout the graphics industry, but the following topics target the two most common forms: cubic environment mapping and spherical environment mapping.</span></span>

-   [<span data-ttu-id="3f2af-114">Сопоставление кубических сред</span><span class="sxs-lookup"><span data-stu-id="3f2af-114">Cubic Environment Mapping</span></span>](cubic-environment-mapping.md)
-   [<span data-ttu-id="3f2af-115">Сопоставление сферического окружения</span><span class="sxs-lookup"><span data-stu-id="3f2af-115">Spherical Environment Mapping</span></span>](spherical-environment-mapping.md)

## <a name="related-topics"></a><span data-ttu-id="3f2af-116">См. также</span><span class="sxs-lookup"><span data-stu-id="3f2af-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f2af-117">Конвейер пикселей</span><span class="sxs-lookup"><span data-stu-id="3f2af-117">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 



