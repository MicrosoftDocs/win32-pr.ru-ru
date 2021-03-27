---
description: Приложение может получать метрики шрифта для физического шрифта только после выбора шрифта в контексте устройства.
ms.assetid: 3eaabc8b-e244-4b65-918b-a20043afa535
title: Устройства и единицы проектирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb52a671727a2fa84d5514b469be5bd320f3318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898429"
---
# <a name="device-vs-design-units"></a><span data-ttu-id="98b46-103">Устройства и единицы проектирования</span><span class="sxs-lookup"><span data-stu-id="98b46-103">Device vs. Design Units</span></span>

<span data-ttu-id="98b46-104">Приложение может получать метрики шрифта для физического шрифта только после выбора шрифта в контексте устройства.</span><span class="sxs-lookup"><span data-stu-id="98b46-104">An application can retrieve font metrics for a physical font only after the font has been selected into a device context.</span></span> <span data-ttu-id="98b46-105">При выборе шрифта в контексте устройства он масштабируется для устройства.</span><span class="sxs-lookup"><span data-stu-id="98b46-105">When a font is selected into a device context, it is scaled for the device.</span></span> <span data-ttu-id="98b46-106">Метрики шрифта, характерные для устройства, называются единицами устройства.</span><span class="sxs-lookup"><span data-stu-id="98b46-106">The font metrics specific to the device are known as device units.</span></span>

<span data-ttu-id="98b46-107">Переносимые метрики в шрифтах называются единицами проектирования.</span><span class="sxs-lookup"><span data-stu-id="98b46-107">Portable metrics in fonts are known as design units.</span></span> <span data-ttu-id="98b46-108">Для применения к указанному устройству единицы проектирования необходимо преобразовать в единицы устройства.</span><span class="sxs-lookup"><span data-stu-id="98b46-108">To apply to a specified device, design units must be converted to device units.</span></span> <span data-ttu-id="98b46-109">Используйте следующую формулу для преобразования единиц проектирования в единицы устройства.</span><span class="sxs-lookup"><span data-stu-id="98b46-109">Use the following formula to convert design units to device units.</span></span>

<span data-ttu-id="98b46-110">*Девицеунитс* = (*десигнунитс* / *унитсперем*) \* (*PointSize*/72) \* *девицересолутион*</span><span class="sxs-lookup"><span data-stu-id="98b46-110">*DeviceUnits* = (*DesignUnits*/*unitsPerEm*) \* (*PointSize*/72) \* *DeviceResolution*</span></span>

<span data-ttu-id="98b46-111">Переменные в этой формуле имеют следующие значения.</span><span class="sxs-lookup"><span data-stu-id="98b46-111">The variables in this formula have the following meanings.</span></span>



| <span data-ttu-id="98b46-112">Переменная</span><span class="sxs-lookup"><span data-stu-id="98b46-112">Variable</span></span>           | <span data-ttu-id="98b46-113">Описание</span><span class="sxs-lookup"><span data-stu-id="98b46-113">Description</span></span>                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98b46-114">*девицеунитс*</span><span class="sxs-lookup"><span data-stu-id="98b46-114">*DeviceUnits*</span></span>      | <span data-ttu-id="98b46-115">Указывает метрику шрифта *десигнунитс* , преобразованную в единицы устройства.</span><span class="sxs-lookup"><span data-stu-id="98b46-115">Specifies the *DesignUnits* font metric converted to device units.</span></span> <span data-ttu-id="98b46-116">Это значение указывается в тех же единицах, что и значение, указанное для *девицересолутион*.</span><span class="sxs-lookup"><span data-stu-id="98b46-116">This value is in the same units as the value specified for *DeviceResolution*.</span></span>                          |
| <span data-ttu-id="98b46-117">*десигнунитс*</span><span class="sxs-lookup"><span data-stu-id="98b46-117">*DesignUnits*</span></span>      | <span data-ttu-id="98b46-118">Указывает метрику шрифта для преобразования в единицы устройства.</span><span class="sxs-lookup"><span data-stu-id="98b46-118">Specifies the font metric to be converted to device units.</span></span> <span data-ttu-id="98b46-119">Это значение может быть любой метрикой шрифта, включая ширину символа или значение Ascend для всего шрифта.</span><span class="sxs-lookup"><span data-stu-id="98b46-119">This value can be any font metric, including the width of a character or the ascender value for an entire font.</span></span> |
| <span data-ttu-id="98b46-120">*унитсперем*</span><span class="sxs-lookup"><span data-stu-id="98b46-120">*unitsPerEm*</span></span>       | <span data-ttu-id="98b46-121">Задает размер квадрата EM для шрифта.</span><span class="sxs-lookup"><span data-stu-id="98b46-121">Specifies the em square size for the font.</span></span>                                                                                                                                 |
| <span data-ttu-id="98b46-122">*PointSize*</span><span class="sxs-lookup"><span data-stu-id="98b46-122">*PointSize*</span></span>        | <span data-ttu-id="98b46-123">Задает размер шрифта в пунктах.</span><span class="sxs-lookup"><span data-stu-id="98b46-123">Specifies size of the font, in points.</span></span> <span data-ttu-id="98b46-124">(Одна точка равна 1/72 дюйма.)</span><span class="sxs-lookup"><span data-stu-id="98b46-124">(One point equals 1/72 of an inch.)</span></span>                                                                                                 |
| <span data-ttu-id="98b46-125">*девицересолутион*</span><span class="sxs-lookup"><span data-stu-id="98b46-125">*DeviceResolution*</span></span> | <span data-ttu-id="98b46-126">Указывает число единиц устройства (в пикселях) на дюйм.</span><span class="sxs-lookup"><span data-stu-id="98b46-126">Specifies number of device units (pixels) per inch.</span></span> <span data-ttu-id="98b46-127">Типичные значения могут быть 300 для лазерного принтера или 96 для экрана VGA.</span><span class="sxs-lookup"><span data-stu-id="98b46-127">Typical values might be 300 for a laser printer or 96 for a VGA screen.</span></span>                                                |



 

<span data-ttu-id="98b46-128">Эта формула не должна использоваться для преобразования единиц устройства обратно в единицы проектирования.</span><span class="sxs-lookup"><span data-stu-id="98b46-128">This formula should not be used to convert device units back to design units.</span></span> <span data-ttu-id="98b46-129">Единицы устройства всегда округляются до ближайшего пикселя.</span><span class="sxs-lookup"><span data-stu-id="98b46-129">Device units are always rounded to the nearest pixel.</span></span> <span data-ttu-id="98b46-130">Распространенная ошибка округления может стать очень большой, особенно если приложение работает с размерами экрана.</span><span class="sxs-lookup"><span data-stu-id="98b46-130">The propagated round-off error can become very large, especially when an application is working with screen sizes.</span></span>

<span data-ttu-id="98b46-131">Чтобы запросить единицы проектирования, создайте логический шрифт, высота которого указана как *унитсперем*.</span><span class="sxs-lookup"><span data-stu-id="98b46-131">To request design units, create a logical font whose height is specified as *unitsPerEm*.</span></span> <span data-ttu-id="98b46-132">Приложения могут извлекать значение для *унитсперем* путем вызова функции [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) и проверки элемента **нтмсизим** структуры [**невтекстметрик**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .</span><span class="sxs-lookup"><span data-stu-id="98b46-132">Applications can retrieve the value for *unitsPerEm* by calling the [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) function and checking the **ntmSizeEM** member of the [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure.</span></span>

 

 



