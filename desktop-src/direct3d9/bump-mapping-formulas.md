---
description: Direct3D применяет следующие формулы к компонентам DU и DV в каждом пикселе схемы выпуклости.
ms.assetid: ae1de432-d1cc-45a5-b25f-b669cd30af3b
title: Формулы сопоставления выпуклости (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436aee9689d78b8b706bb98d908f2e3fbc05ca6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142946"
---
# <a name="bump-mapping-formulas-direct3d-9"></a><span data-ttu-id="a2783-103">Формулы сопоставления выпуклости (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a2783-103">Bump Mapping Formulas (Direct3D 9)</span></span>

<span data-ttu-id="a2783-104">Direct3D применяет следующие формулы к компонентам<sub>d и d</sub> <sub>V</sub> в каждом пикселе схемы выпуклости.</span><span class="sxs-lookup"><span data-stu-id="a2783-104">Direct3D applies the following formulas to the D<sub>U</sub> and D<sub>V</sub> components in each bump map pixel.</span></span>

![формулы в преобразованиях матрицы отображения рельефов](images/dudv-transform.png)

<span data-ttu-id="a2783-106">В этих формулах переменные D<sub>и d</sub> <sub>V</sub> берутся непосредственно из пикселя на карте выпуклости и преобразуются матрицей 2x2 для получения выходных значений разности<sub>d и d</sub><sub>V</sub>.</span><span class="sxs-lookup"><span data-stu-id="a2783-106">In these formulas, the D<sub>U</sub> and D<sub>V</sub> variables are taken directly from a bump map pixel and transformed by a 2x2 matrix to produce the output delta values D<sub>U</sub>' and D<sub>V</sub>'.</span></span> <span data-ttu-id="a2783-107">Система использует выходные значения для изменения координат текстуры, которые соответствуют карте среды на следующей стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="a2783-107">The system uses the output values to modify the texture coordinates that address the environment map in the next texture stage.</span></span> <span data-ttu-id="a2783-108">Коэффициенты матрицы преобразований задаются при D3DTSS \_ BUMPENVMAT00, D3DTSS \_ BUMPENVMAT10, D3DTSS \_ BUMPENVMAT01 и D3DTSS \_ BUMPENVMAT11 стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="a2783-108">The coefficients of the transformation matrix are set though the D3DTSS\_BUMPENVMAT00, D3DTSS\_BUMPENVMAT10, D3DTSS\_BUMPENVMAT01, and D3DTSS\_BUMPENVMAT11 texture stage states.</span></span>

<span data-ttu-id="a2783-109">В дополнение к разностным значениям и версии v система может вычислить значение светимости, используемое для модуляции цвета схемы среды на следующем этапе смешения, как показано в следующей формуле.</span><span class="sxs-lookup"><span data-stu-id="a2783-109">In addition to the u and v delta values, the system can compute a luminance value that it uses to modulate the color of the environment map in the next blending stage, as shown in the following formula.</span></span>

![Формула для яркости выходных данных, вычисленная по коэффициенту масштабирования и смещению](images/l-transform.png)

<span data-ttu-id="a2783-111">В этой формуле L — вычисляемая насыщенность выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a2783-111">In this formula, L' is the output luminance being computed.</span></span> <span data-ttu-id="a2783-112">Переменная L — это значение светимости, взятое из пиксела на карте выпуклости, умноженное на коэффициент масштабирования, S и смещение на значение переменной O. На \_ этапе текстуры D3DTSS бумпенвлскале и D3DTSS \_ бумпенвлоффсет определяются значения для переменных S и O в формуле.</span><span class="sxs-lookup"><span data-stu-id="a2783-112">The L variable is the luminance value taken from a bump map pixel, which is multiplied by the scaling factor, S, and offset by the value in the variable O. The D3DTSS\_BUMPENVLSCALE and D3DTSS\_BUMPENVLOFFSET texture stage states control the values for the S and O variables in the formula.</span></span> <span data-ttu-id="a2783-113">Эта формула применяется, только если операции смешения текстур для этапа, содержащего карту выпуклости, задано значение D3DTOP \_ бумпенвмаплуминанце.</span><span class="sxs-lookup"><span data-stu-id="a2783-113">This formula is only applied when the texture blending operation for the stage that contains the bump map is set to D3DTOP\_BUMPENVMAPLUMINANCE.</span></span> <span data-ttu-id="a2783-114">При использовании D3DTOP \_ бумпенвмап система использует значение 1,0 для L.</span><span class="sxs-lookup"><span data-stu-id="a2783-114">When using D3DTOP\_BUMPENVMAP, the system uses a value of 1.0 for L'.</span></span>

<span data-ttu-id="a2783-115">После вычисления Дельта выходных значений D<sub>U</sub>и d<sub>V</sub>система добавляет их в координаты текстуры на следующей стадии текстуры и производит модуляцию выбранного цвета с помощью светимости, чтобы получить цвет, применяемый к многоугольнику.</span><span class="sxs-lookup"><span data-stu-id="a2783-115">After computing the output delta values D<sub>U</sub>' and D<sub>V</sub>', the system adds them to the texture coordinates in the next texture stage, and modulates the chosen color by the luminance to produce the color applied to the polygon.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2783-116">См. также</span><span class="sxs-lookup"><span data-stu-id="a2783-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2783-117">Сопоставление рельефов</span><span class="sxs-lookup"><span data-stu-id="a2783-117">Bump Mapping</span></span>](bump-mapping.md)
</dt> </dl>

 

 



