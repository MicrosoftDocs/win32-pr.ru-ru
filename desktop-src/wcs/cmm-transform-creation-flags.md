---
title: Флаги создания преобразования CMM
description: Кммс используйте флаги создания преобразования в качестве подсказок для создания преобразования цветов. Для определения оптимального использования этих флагов необходимо использовать модуль CMM.
ms.assetid: f3942929-272c-4f08-98ac-a4d14d2f6ac4
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852ef5c080c361bfffb6915d808787d46e63ba5c
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/02/2021
ms.locfileid: "105719857"
---
# <a name="cmm-transform-creation-flags"></a><span data-ttu-id="7cebc-104">Флаги создания преобразования CMM</span><span class="sxs-lookup"><span data-stu-id="7cebc-104">CMM Transform Creation Flags</span></span>

<span data-ttu-id="7cebc-105">Кммс используйте флаги создания преобразования в качестве подсказок для создания преобразования цветов.</span><span class="sxs-lookup"><span data-stu-id="7cebc-105">CMMs use transform creation flags as hints for how to create a color transform.</span></span> <span data-ttu-id="7cebc-106">Для определения оптимального использования этих флагов необходимо использовать модуль CMM.</span><span class="sxs-lookup"><span data-stu-id="7cebc-106">It is up to the CMM to determine how best to use these flags.</span></span>

<span data-ttu-id="7cebc-107">Все функции, которые используют эти флаги, передают или получают значения флагов, используя параметр с именем *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="7cebc-107">All of the functions that use these flags pass or receive flag values through a parameter called *dwFlags*.</span></span> <span data-ttu-id="7cebc-108">В приведенной ниже таблице должно быть задано значение высокого порядка **слова** *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="7cebc-108">The high-order **WORD** of *dwFlags* should be set to a value from the following table.</span></span>



| <span data-ttu-id="7cebc-109">Константа</span><span class="sxs-lookup"><span data-stu-id="7cebc-109">Constant</span></span>                    | <span data-ttu-id="7cebc-110">Описание</span><span class="sxs-lookup"><span data-stu-id="7cebc-110">Description</span></span>                                                                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cebc-111">ВКЛЮЧИТЬ \_ проверку палитры \_</span><span class="sxs-lookup"><span data-stu-id="7cebc-111">ENABLE\_GAMUT\_CHECKING</span></span>     | <span data-ttu-id="7cebc-112">Используйте это преобразование для проверки цветовой палитры.</span><span class="sxs-lookup"><span data-stu-id="7cebc-112">Use this transform for gamut checking.</span></span>                                                                                                       |
| <span data-ttu-id="7cebc-113">ИСПОЛЬЗОВАТЬ \_ относительную \_ цветопередачу</span><span class="sxs-lookup"><span data-stu-id="7cebc-113">USE\_RELATIVE\_COLORIMETRIC</span></span> | <span data-ttu-id="7cebc-114">Не сохраняйте белую точку.</span><span class="sxs-lookup"><span data-stu-id="7cebc-114">Do not preserve the white point.</span></span> <span data-ttu-id="7cebc-115">Если выходной диапазон не поддерживает данный цвет, используйте ближайший поддерживаемый цвет.</span><span class="sxs-lookup"><span data-stu-id="7cebc-115">If the output gamut does not support a given color, use the nearest supported color.</span></span> <span data-ttu-id="7cebc-116">См. раздел Обработка целей.</span><span class="sxs-lookup"><span data-stu-id="7cebc-116">See Rendering Intents.</span></span> |
| <span data-ttu-id="7cebc-117">Быстрый \_ перевод</span><span class="sxs-lookup"><span data-stu-id="7cebc-117">FAST\_TRANSLATE</span></span>             | <span data-ttu-id="7cebc-118">Поиск только по цвету.</span><span class="sxs-lookup"><span data-stu-id="7cebc-118">Look up color only.</span></span> <span data-ttu-id="7cebc-119">Не Выменяйте интерполяцию цвета.</span><span class="sxs-lookup"><span data-stu-id="7cebc-119">Do not interpolate the color.</span></span>                                                                                            |
| <span data-ttu-id="7cebc-120">пресервеблакк</span><span class="sxs-lookup"><span data-stu-id="7cebc-120">PRESERVEBLACK</span></span>               | <span data-ttu-id="7cebc-121">Вставляет соответствующий ГММП "черного поколения" в качестве последней ГММП в последовательности преобразования.</span><span class="sxs-lookup"><span data-stu-id="7cebc-121">Inserts the appropriate black generation GMMP as the last GMMP in the transform sequence</span></span>                                                     |
| <span data-ttu-id="7cebc-122">WCS \_ всегда</span><span class="sxs-lookup"><span data-stu-id="7cebc-122">WCS\_ALWAYS</span></span>                 | <span data-ttu-id="7cebc-123">Используйте путь к коду WCS даже для преобразований ICC.</span><span class="sxs-lookup"><span data-stu-id="7cebc-123">Use the WCS code path even for ICC transforms.</span></span>                                                                                               |
| <span data-ttu-id="7cebc-124">последовательное \_ Преобразование</span><span class="sxs-lookup"><span data-stu-id="7cebc-124">SEQUENTIAL\_TRANSFORM</span></span>       | <span data-ttu-id="7cebc-125">Флаг создания преобразования для создания последовательного (не оптимизированного) преобразования цвета.</span><span class="sxs-lookup"><span data-stu-id="7cebc-125">Transform creation flag for creating a sequential (non-optimized) color transform.</span></span>                                                           |



 

<span data-ttu-id="7cebc-126">**Слово** низкого порядка может иметь одно из следующих значений констант.</span><span class="sxs-lookup"><span data-stu-id="7cebc-126">The low-order **WORD** can have one of the following constant values.</span></span>



| <span data-ttu-id="7cebc-127">Константа</span><span class="sxs-lookup"><span data-stu-id="7cebc-127">Constant</span></span>     | <span data-ttu-id="7cebc-128">Описание</span><span class="sxs-lookup"><span data-stu-id="7cebc-128">Description</span></span>                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cebc-129">\_режим цветопробы</span><span class="sxs-lookup"><span data-stu-id="7cebc-129">PROOF\_MODE</span></span>  | <span data-ttu-id="7cebc-130">Для предварительного просмотра изображения будет использоваться преобразование.</span><span class="sxs-lookup"><span data-stu-id="7cebc-130">Transform will be used to preview the image.</span></span> <span data-ttu-id="7cebc-131">Низкое качество изображения.</span><span class="sxs-lookup"><span data-stu-id="7cebc-131">Low image quality.</span></span>                                    |
| <span data-ttu-id="7cebc-132">НОРМАЛЬНЫЙ \_ режим</span><span class="sxs-lookup"><span data-stu-id="7cebc-132">NORMAL\_MODE</span></span> | <span data-ttu-id="7cebc-133">Преобразование будет использоваться для обычного вывода изображения.</span><span class="sxs-lookup"><span data-stu-id="7cebc-133">Transform will be used for normal image display.</span></span> <span data-ttu-id="7cebc-134">Среднее качество изображения.</span><span class="sxs-lookup"><span data-stu-id="7cebc-134">Average image quality.</span></span>                            |
| <span data-ttu-id="7cebc-135">Лучший \_ режим</span><span class="sxs-lookup"><span data-stu-id="7cebc-135">BEST\_MODE</span></span>   | <span data-ttu-id="7cebc-136">Преобразование будет использоваться для отображения изображения самого высокого качества на целевом устройстве.</span><span class="sxs-lookup"><span data-stu-id="7cebc-136">Transform will be used for the display of the highest-quality image possible on the target device.</span></span> |



 

<span data-ttu-id="7cebc-137">При переходе из \_ режима цветопробы в наилучший \_ режим качество вывода обычно повышается, а скорость преобразования отклоняется.</span><span class="sxs-lookup"><span data-stu-id="7cebc-137">Moving from PROOF\_MODE to BEST\_MODE, output quality generally improves and transform speed declines.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cebc-138">См. также</span><span class="sxs-lookup"><span data-stu-id="7cebc-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cebc-139">Основные понятия управления цветом</span><span class="sxs-lookup"><span data-stu-id="7cebc-139">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="7cebc-140">Константы ICM</span><span class="sxs-lookup"><span data-stu-id="7cebc-140">ICM Constants</span></span>](wcs-constants.md)
</dt> </dl>

 

 




