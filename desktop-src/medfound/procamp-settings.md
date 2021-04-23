---
description: Эти флаги определяют параметры видеопроцессора (cAmp).
ms.assetid: 60d97b9e-d77c-4e53-94ea-ebd59c2601df
title: Параметры параметра cAmp (Dxva2api. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0181d7491d948a4ec4219ada4241397b8a721b0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673461"
---
# <a name="procamp-settings"></a><span data-ttu-id="91c4f-103">Параметры параметра cAmp</span><span class="sxs-lookup"><span data-stu-id="91c4f-103">ProcAmp Settings</span></span>

<span data-ttu-id="91c4f-104">Эти флаги определяют параметры видеопроцессора (cAmp).</span><span class="sxs-lookup"><span data-stu-id="91c4f-104">These flags define video processor (ProcAmp) settings.</span></span>



| <span data-ttu-id="91c4f-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="91c4f-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                         | <span data-ttu-id="91c4f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="91c4f-106">Description</span></span>           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------|
| <span id="DXVA2_ProcAmp_None"></span><span id="dxva2_procamp_none"></span><span id="DXVA2_PROCAMP_NONE"></span><dl> <span data-ttu-id="91c4f-107"><dt>**DXVA2 \_ \_**</dt> <dt>Символ 0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="91c4f-107"><dt>**DXVA2\_ProcAmp\_None**</dt> <dt>0x0000</dt></span></span> </dl>                         | <span data-ttu-id="91c4f-108">Нет</span><span class="sxs-lookup"><span data-stu-id="91c4f-108">None</span></span><br/>       |
| <span id="DXVA2_ProcAmp_Brightness"></span><span id="dxva2_procamp_brightness"></span><span id="DXVA2_PROCAMP_BRIGHTNESS"></span><dl> <span data-ttu-id="91c4f-109"><dt>**DXVA2 \_ 0x0001 \_ яркость**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="91c4f-109"><dt>**DXVA2\_ProcAmp\_Brightness**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="91c4f-110">Brightness</span><span class="sxs-lookup"><span data-stu-id="91c4f-110">Brightness</span></span><br/> |
| <span id="DXVA2_ProcAmp_Contrast"></span><span id="dxva2_procamp_contrast"></span><span id="DXVA2_PROCAMP_CONTRAST"></span><dl> <span data-ttu-id="91c4f-111"><dt>**DXVA2 \_ 0x0002 с \_ контрастностью**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="91c4f-111"><dt>**DXVA2\_ProcAmp\_Contrast**</dt> <dt>0x0002</dt></span></span> </dl>         | <span data-ttu-id="91c4f-112">Контраст</span><span class="sxs-lookup"><span data-stu-id="91c4f-112">Contrast</span></span><br/>   |
| <span id="DXVA2_ProcAmp_Hue"></span><span id="dxva2_procamp_hue"></span><span id="DXVA2_PROCAMP_HUE"></span><dl> <span data-ttu-id="91c4f-113"><dt>**DXVA2 \_ 0x0004 \_ оттенок**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="91c4f-113"><dt>**DXVA2\_ProcAmp\_Hue**</dt> <dt>0x0004</dt></span></span> </dl>                             | <span data-ttu-id="91c4f-114">Оттенок</span><span class="sxs-lookup"><span data-stu-id="91c4f-114">Hue</span></span><br/>        |
| <span id="DXVA2_ProcAmp_Saturation"></span><span id="dxva2_procamp_saturation"></span><span id="DXVA2_PROCAMP_SATURATION"></span><dl> <span data-ttu-id="91c4f-115"><dt>**DXVA2 \_ 0x0008ая \_ насыщенность Camp**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="91c4f-115"><dt>**DXVA2\_ProcAmp\_Saturation**</dt> <dt>0x0008</dt></span></span> </dl> | <span data-ttu-id="91c4f-116">Насыщенность</span><span class="sxs-lookup"><span data-stu-id="91c4f-116">Saturation</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="91c4f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="91c4f-117">Requirements</span></span>



| <span data-ttu-id="91c4f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="91c4f-118">Requirement</span></span> | <span data-ttu-id="91c4f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="91c4f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91c4f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91c4f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="91c4f-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="91c4f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91c4f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91c4f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="91c4f-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="91c4f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91c4f-124">Header</span><span class="sxs-lookup"><span data-stu-id="91c4f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="91c4f-125"><dt>Dxva2api. h</dt></span><span class="sxs-lookup"><span data-stu-id="91c4f-125"><dt>Dxva2api.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91c4f-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91c4f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91c4f-127">Константы Media Foundation</span><span class="sxs-lookup"><span data-stu-id="91c4f-127">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




