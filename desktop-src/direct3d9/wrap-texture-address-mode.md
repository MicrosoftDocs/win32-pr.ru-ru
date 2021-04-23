---
description: Режим адресации текстуры, определяемый элементом D3DTADDRESS, \_ перечисленным в перечислимом ТИПЕ D3DTEXTUREADDRESS, делает Direct3D повторять текстуру для каждого целочисленного соединения.
ms.assetid: fe33c484-346d-4888-ba88-b8ab00feefbb
title: Включить режим адресации текстуры (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721ace45599236022f32e6b0ec3723e346befbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262317"
---
# <a name="wrap-texture-address-mode-direct3d-9"></a><span data-ttu-id="79bc1-103">Включить режим адресации текстуры (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="79bc1-103">Wrap Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="79bc1-104">Режим адресации текстуры, определяемый элементом D3DTADDRESS, \_ перечисленным в перечислимом типе [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , делает Direct3D повторять текстуру для каждого целочисленного соединения.</span><span class="sxs-lookup"><span data-stu-id="79bc1-104">The wrap texture address mode, identified by the D3DTADDRESS\_WRAP member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, makes Direct3D repeat the texture on every integer junction.</span></span> <span data-ttu-id="79bc1-105">Предположим, например, что приложение создает квадратный примитив и задает координаты текстуры (0.0,0.0), (0.0,3.0), (3.0,3.0) и (3.0,0.0).</span><span class="sxs-lookup"><span data-stu-id="79bc1-105">Suppose, for example, your application creates a square primitive and specifies texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0).</span></span> <span data-ttu-id="79bc1-106">Если установить режим адресации текстуры в D3DTADDRESS \_ , то текстура будет применена три раза в обоих направлениях, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="79bc1-106">Setting the texture addressing mode to D3DTADDRESS\_WRAP results in the texture being applied three times in both the u-and v-directions, as shown in the following illustration.</span></span>

![иллюстрация текстуры с изображением лица с обертыванием в U- и V-направлениях](images/wrap.png)

<span data-ttu-id="79bc1-108">Эффекты этого режима адресации текстуры аналогичны, но отличаются от них в режиме зеркального отображения.</span><span class="sxs-lookup"><span data-stu-id="79bc1-108">The effects of this texture address mode are similar to, but distinct from, those of the mirror mode.</span></span> <span data-ttu-id="79bc1-109">Дополнительные сведения см. в разделе [режим адресации зеркальной текстуры (Direct3D 9)](mirror-texture-address-mode.md).</span><span class="sxs-lookup"><span data-stu-id="79bc1-109">For more information, see [Mirror Texture Address Mode (Direct3D 9)](mirror-texture-address-mode.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="79bc1-110">См. также</span><span class="sxs-lookup"><span data-stu-id="79bc1-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79bc1-111">Режимы адресации текстур</span><span class="sxs-lookup"><span data-stu-id="79bc1-111">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
