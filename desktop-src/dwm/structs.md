---
title: Структуры DWM
description: В этом разделе содержатся сведения о структурах диспетчер окон рабочего стола (DWM).
ms.assetid: 26b36617-54c2-405a-9a7d-bd86fefa94b6
keywords:
- Диспетчер окон рабочего стола (DWM), справочные материалы
- DWM (диспетчер окон рабочего стола), Справочник
- Диспетчер окон рабочего стола (DWM), структуры
- DWM (диспетчер окон рабочего стола), структуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f212d248c0f70cfd51e6e47b2d37c89d24f630b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068006"
---
# <a name="dwm-structures"></a><span data-ttu-id="4a331-107">Структуры DWM</span><span class="sxs-lookup"><span data-stu-id="4a331-107">DWM Structures</span></span>

<span data-ttu-id="4a331-108">В этом разделе содержатся сведения о структурах диспетчер окон рабочего стола (DWM).</span><span class="sxs-lookup"><span data-stu-id="4a331-108">This section contains information about the Desktop Window Manager (DWM) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4a331-109">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="4a331-109">In this section</span></span>



| <span data-ttu-id="4a331-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="4a331-110">Topic</span></span>                                                                     | <span data-ttu-id="4a331-111">Описание</span><span class="sxs-lookup"><span data-stu-id="4a331-111">Description</span></span>                                                                                                                                               |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a331-112">**DWM \_ блурбехинд**</span><span class="sxs-lookup"><span data-stu-id="4a331-112">**DWM\_BLURBEHIND**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind)<br/>                      | <span data-ttu-id="4a331-113">Указывает свойства DWM размытия позади.</span><span class="sxs-lookup"><span data-stu-id="4a331-113">Specifies DWM blur-behind properties.</span></span> <span data-ttu-id="4a331-114">Используется функцией [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) .</span><span class="sxs-lookup"><span data-stu-id="4a331-114">Used by the [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) function.</span></span><br/>                     |
| [<span data-ttu-id="4a331-115">**\_параметры DWM Present \_**</span><span class="sxs-lookup"><span data-stu-id="4a331-115">**DWM\_PRESENT\_PARAMETERS**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_present_parameters)<br/>     | <span data-ttu-id="4a331-116">Указывает параметры кадра видео DWM для компоновки кадров.</span><span class="sxs-lookup"><span data-stu-id="4a331-116">Specifies DWM video frame parameters for frame composition.</span></span> <span data-ttu-id="4a331-117">Используется функцией [**двмсетпресентпараметерс**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) .</span><span class="sxs-lookup"><span data-stu-id="4a331-117">Used by the [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) function.</span></span><br/>   |
| [<span data-ttu-id="4a331-118">**\_Свойства ЭСКИЗА \_ DWM**</span><span class="sxs-lookup"><span data-stu-id="4a331-118">**DWM\_THUMBNAIL\_PROPERTIES**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties)<br/> | <span data-ttu-id="4a331-119">Задает свойства эскиза DWM.</span><span class="sxs-lookup"><span data-stu-id="4a331-119">Specifies DWM thumbnail properties.</span></span> <span data-ttu-id="4a331-120">Используется функцией [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) .</span><span class="sxs-lookup"><span data-stu-id="4a331-120">Used by the [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) function.</span></span><br/>                 |
| [<span data-ttu-id="4a331-121">**\_ \_ сведения о времени DWM**</span><span class="sxs-lookup"><span data-stu-id="4a331-121">**DWM\_TIMING\_INFO**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_timing_info)<br/>                   | <span data-ttu-id="4a331-122">Указывает сведения о времени композиции DWM.</span><span class="sxs-lookup"><span data-stu-id="4a331-122">Specifies DWM composition timing information.</span></span> <span data-ttu-id="4a331-123">Используется функцией [**двмжеткомпоситионтимингинфо**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo) .</span><span class="sxs-lookup"><span data-stu-id="4a331-123">Used by the [**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo) function.</span></span><br/>         |
| [<span data-ttu-id="4a331-124">**MilMatrix3x2D**</span><span class="sxs-lookup"><span data-stu-id="4a331-124">**MilMatrix3x2D**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-milmatrix3x2d)<br/>                         | <span data-ttu-id="4a331-125">Указывает матрицу 3x2, описывающую преобразование.</span><span class="sxs-lookup"><span data-stu-id="4a331-125">Specifies a 3x2 matrix that describes a transform.</span></span> <br/>                                                                                            |
| [<span data-ttu-id="4a331-126">**отношение неподписанных \_**</span><span class="sxs-lookup"><span data-stu-id="4a331-126">**UNSIGNED\_RATIO**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-unsigned_ratio)<br/>                      | <span data-ttu-id="4a331-127">Определяет тип данных, используемый API DWM.</span><span class="sxs-lookup"><span data-stu-id="4a331-127">Defines a data type used by the DWM APIs.</span></span> <span data-ttu-id="4a331-128">Он представляет обобщенное соотношение и используется для различных целей и единиц даже внутри одного API.</span><span class="sxs-lookup"><span data-stu-id="4a331-128">It represents a generic ratio and is used for different purposes and units even within a single API.</span></span><br/> |



 

 

 





