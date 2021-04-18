---
title: Идентификаторы типов цветового пространства
description: Эти константы определяют тип массива цветового пространства PostScript 2. Следующие значения являются допустимыми типами массивов цветового пространства.
ms.assetid: dc312db2-3bc5-461f-819c-37ff14cff896
topic_type:
- apiref
api_name:
- CSA_A
- CSA_GRAY
- CSA_ABC
- CSA_DEF
- CSA_RGB
- CSA_Lab
- CSA_DEFG
- CSA_CMYK
api_type:
- NA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 973db6c56dda5bde8614dffa13f461761934fcde
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/02/2021
ms.locfileid: "105719855"
---
# <a name="color-space-type-identifiers"></a><span data-ttu-id="0520f-104">Идентификаторы типов цветового пространства</span><span class="sxs-lookup"><span data-stu-id="0520f-104">Color Space Type Identifiers</span></span>

<span data-ttu-id="0520f-105">Эти константы определяют тип массива цветового пространства PostScript 2.</span><span class="sxs-lookup"><span data-stu-id="0520f-105">These constants specify the type of a Postscript 2 color space array.</span></span> <span data-ttu-id="0520f-106">Следующие значения являются допустимыми типами массивов цветового пространства.</span><span class="sxs-lookup"><span data-stu-id="0520f-106">The following values are valid color space array types.</span></span>

<dl> <dt>

<span data-ttu-id="0520f-107"><span id="CSA_A"></span><span id="csa_a"></span>**CSA \_ A**</span><span class="sxs-lookup"><span data-stu-id="0520f-107"><span id="CSA_A"></span><span id="csa_a"></span>**CSA\_A**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0520f-108">Получите массив цветового пространства Циебаседа из монохромного профиля.</span><span class="sxs-lookup"><span data-stu-id="0520f-108">Get a CIEBasedA color space array from the monochrome profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0520f-109"><span id="CSA_GRAY"></span><span id="csa_gray"></span>**\_СЕРАЯ CSA**</span><span class="sxs-lookup"><span data-stu-id="0520f-109"><span id="CSA_GRAY"></span><span id="csa_gray"></span>**CSA\_GRAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0520f-110">Получите массив цветового пространства Циебаседа из монохромного профиля.</span><span class="sxs-lookup"><span data-stu-id="0520f-110">Get a CIEBasedA color space array from the monochrome profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0520f-111"><span id="CSA_ABC"></span><span id="csa_abc"></span>**CSA \_ ABC**</span><span class="sxs-lookup"><span data-stu-id="0520f-111"><span id="CSA_ABC"></span><span id="csa_abc"></span>**CSA\_ABC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0520f-112">Получите массив цветовых пространств Циебаседабк из профиля RGB или L <sup>\*</sup> a <sup>\*</sup> b.</span><span class="sxs-lookup"><span data-stu-id="0520f-112">Get a CIEBasedABC color space array from the RGB or L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0520f-113"><span id="CSA_DEF"></span><span id="csa_def"></span>**CSA \_ DEF**</span><span class="sxs-lookup"><span data-stu-id="0520f-113"><span id="CSA_DEF"></span><span id="csa_def"></span>**CSA\_DEF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0520f-114">Получите массив цветовых пространств Циебаседдеф из профиля RGB или L <sup>\*</sup> a <sup>\*</sup> b.</span><span class="sxs-lookup"><span data-stu-id="0520f-114">Get a CIEBasedDEF color space array from the RGB or L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0520f-115"><span id="CSA_RGB"></span><span id="csa_rgb"></span>**CSA \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="0520f-115"><span id="CSA_RGB"></span><span id="csa_rgb"></span>**CSA\_RGB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0520f-116">Получите массив цветового пространства Циебаседдеф, за которым следует массив цветового пространства Циебаседабк из профиля RGB.</span><span class="sxs-lookup"><span data-stu-id="0520f-116">Get a CIEBasedDEF color space array followed by a CIEBasedABC color space array from the RGB profile.</span></span> <span data-ttu-id="0520f-117">При выполнении, если принтер не поддерживает Циебаседдеф цветовые пространства, функция использует определение Циебаседабк.</span><span class="sxs-lookup"><span data-stu-id="0520f-117">On execution, if the printer doesn't support CIEBasedDEF color spaces, the function uses the CIEBasedABC definition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0520f-118"><span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**CSA \_ Labs**</span><span class="sxs-lookup"><span data-stu-id="0520f-118"><span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**CSA\_Lab**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0520f-119">Возвращает массив цветового пространства Циебаседабк из профиля L <sup>\*</sup> a <sup>\*</sup> b.</span><span class="sxs-lookup"><span data-stu-id="0520f-119">Gets a CIEBasedABC color space array from the L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0520f-120"><span id="CSA_DEFG"></span><span id="csa_defg"></span>**CSA \_ дефг**</span><span class="sxs-lookup"><span data-stu-id="0520f-120"><span id="CSA_DEFG"></span><span id="csa_defg"></span>**CSA\_DEFG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0520f-121">Получите массив цветовых пространств Циебаседдефг из профиля CMYK.</span><span class="sxs-lookup"><span data-stu-id="0520f-121">Get a CIEBasedDEFG color space array from the CMYK profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0520f-122"><span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**CSA \_ CMYK**</span><span class="sxs-lookup"><span data-stu-id="0520f-122"><span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**CSA\_CMYK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0520f-123">Получите массив цветовых пространств Циебаседкмик из профиля CMYK.</span><span class="sxs-lookup"><span data-stu-id="0520f-123">Get a CIEBasedCMYK color space array from the CMYK profile.</span></span>


</dt> </dl> </dd> </dl>

## <a name="see-also"></a><span data-ttu-id="0520f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0520f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0520f-125">Основные понятия управления цветом</span><span class="sxs-lookup"><span data-stu-id="0520f-125">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="0520f-126">Константы ICM</span><span class="sxs-lookup"><span data-stu-id="0520f-126">ICM Constants</span></span>](wcs-constants.md)
</dt> </dl>

 

 




