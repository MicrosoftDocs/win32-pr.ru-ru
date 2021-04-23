---
description: В этом разделе описывается функция обработки цветовой палитры оболочки Windows. Программные элементы, описанные в этой документации, экспортируются с помощью Shlwapi.dll и определяются в Shlwapi. h и Shlwapi. lib.
title: Функции обработки цветовой палитры оболочки
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 93848cb3-60c6-4b2f-82d9-abfee97e372a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ba92dcf280b8d54b8778e276bb603d888f5991c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264895"
---
# <a name="shell-color-palette-handling-functions"></a><span data-ttu-id="6d83d-104">Функции обработки цветовой палитры оболочки</span><span class="sxs-lookup"><span data-stu-id="6d83d-104">Shell Color Palette Handling Functions</span></span>

<span data-ttu-id="6d83d-105">В этом разделе описывается функция обработки цветовой палитры оболочки Windows.</span><span class="sxs-lookup"><span data-stu-id="6d83d-105">This section describes the Windows Shell color palette handling functions.</span></span> <span data-ttu-id="6d83d-106">Программные элементы, описанные в этой документации, экспортируются с помощью Shlwapi.dll и определяются в Shlwapi. h и Shlwapi. lib.</span><span class="sxs-lookup"><span data-stu-id="6d83d-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6d83d-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="6d83d-107">In this section</span></span>



| <span data-ttu-id="6d83d-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="6d83d-108">Topic</span></span>                                                           | <span data-ttu-id="6d83d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6d83d-109">Description</span></span>                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d83d-110">**колораджустлума**</span><span class="sxs-lookup"><span data-stu-id="6d83d-110">**ColorAdjustLuma**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-coloradjustluma)<br/>           | <span data-ttu-id="6d83d-111">Изменяет светимость значения RGB.</span><span class="sxs-lookup"><span data-stu-id="6d83d-111">Changes the luminance of a RGB value.</span></span> <span data-ttu-id="6d83d-112">Оттенок и насыщенность не затрагиваются.</span><span class="sxs-lookup"><span data-stu-id="6d83d-112">Hue and saturation are not affected.</span></span><br/> |
| [<span data-ttu-id="6d83d-113">**колорхлсторгб**</span><span class="sxs-lookup"><span data-stu-id="6d83d-113">**ColorHLSToRGB**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-colorhlstorgb)<br/>               | <span data-ttu-id="6d83d-114">Преобразует цвета из оттенка-яркости-насыщенности (HLS) в формат RGB.</span><span class="sxs-lookup"><span data-stu-id="6d83d-114">Converts colors from hue-luminance-saturation (HLS) to RGB format.</span></span><br/>         |
| [<span data-ttu-id="6d83d-115">**колорргбтохлс**</span><span class="sxs-lookup"><span data-stu-id="6d83d-115">**ColorRGBToHLS**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-colorrgbtohls)<br/>               | <span data-ttu-id="6d83d-116">Преобразует цвета из формата RGB в формат "цветовой тон-светимость" (HLS).</span><span class="sxs-lookup"><span data-stu-id="6d83d-116">Converts colors from RGB to hue-luminance-saturation (HLS) format.</span></span><br/>         |
| [<span data-ttu-id="6d83d-117">**шкреатешеллпалетте**</span><span class="sxs-lookup"><span data-stu-id="6d83d-117">**SHCreateShellPalette**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreateshellpalette)<br/> | <span data-ttu-id="6d83d-118">Создает палитру полутонов для указанного контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="6d83d-118">Creates a halftone palette for the specified device context.</span></span><br/>               |



 

 

 




