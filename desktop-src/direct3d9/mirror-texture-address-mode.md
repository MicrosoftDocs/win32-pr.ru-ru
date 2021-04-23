---
description: Режим адресации зеркальной текстуры, определяемый \_ элементом Mirror D3DTADDRESS перечисляемого типа D3DTEXTUREADDRESS, заставляет Direct3D зеркально отобразить текстуру на каждой границе целых чисел.
ms.assetid: 816efd4d-94b3-4b6c-9fc9-218cc2207b97
title: Режим адресации зеркальной текстуры (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 471ad8b715d9375947162c66474687b9d6376bec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416620"
---
# <a name="mirror-texture-address-mode-direct3d-9"></a><span data-ttu-id="c1bda-103">Режим адресации зеркальной текстуры (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c1bda-103">Mirror Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="c1bda-104">Режим адресации зеркальной текстуры, определяемый \_ элементом Mirror D3DTADDRESS перечисляемого типа [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , заставляет Direct3D зеркально отобразить текстуру на каждой границе целых чисел.</span><span class="sxs-lookup"><span data-stu-id="c1bda-104">The mirror texture address mode, identified by the D3DTADDRESS\_MIRROR member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to mirror the texture at every integer boundary.</span></span> <span data-ttu-id="c1bda-105">Предположим, например, что приложение создает квадратный примитив и задает координаты текстуры (0.0,0.0), (0.0,3.0), (3.0,3.0) и (3.0,0.0).</span><span class="sxs-lookup"><span data-stu-id="c1bda-105">Suppose, for example, your application creates a square primitive and specifies texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0).</span></span> <span data-ttu-id="c1bda-106">Установка режима адресации текстуры для D3DTADDRESS \_ зеркального отображения результатов в текстуре, применяемую три раза в обоих направлениях: u и v.</span><span class="sxs-lookup"><span data-stu-id="c1bda-106">Setting the texture addressing mode to D3DTADDRESS\_MIRROR results in the texture being applied three times in both the u- and v-directions.</span></span> <span data-ttu-id="c1bda-107">Каждая вторая строка и каждый столбец, к которым применяется текстура, является зеркальным отражением предыдущей строки или столбца, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="c1bda-107">Every other row and column that it is applied to is a mirror image of the preceding row or column, as shown in the following illustration.</span></span>

![иллюстрация зеркальных изображений в сетке 3x3](images/mirror.png)

<span data-ttu-id="c1bda-109">Эффекты этого режима адреса текстуры аналогичны, но отличаются от них в режиме переноса.</span><span class="sxs-lookup"><span data-stu-id="c1bda-109">The effects of this texture address mode are similar to, but distinct from, those of the wrap mode.</span></span> <span data-ttu-id="c1bda-110">Дополнительные сведения см. в разделе [режим переноса адреса текстуры (Direct3D 9)](wrap-texture-address-mode.md).</span><span class="sxs-lookup"><span data-stu-id="c1bda-110">For more information, see [Wrap Texture Address Mode (Direct3D 9)](wrap-texture-address-mode.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1bda-111">См. также</span><span class="sxs-lookup"><span data-stu-id="c1bda-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1bda-112">Режимы адресации текстур</span><span class="sxs-lookup"><span data-stu-id="c1bda-112">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
