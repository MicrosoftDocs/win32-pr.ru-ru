---
description: Указывает максимальное число динамических звуковых объектов, которые могут быть отображены в конечной точке аудио симулатанеаусли.
ms.assetid: 6B6D73C1-C2E6-4C23-BBAD-7B51E8441C71
title: Атрибут MF_MT_SPATIAL_AUDIO_MAX_DYNAMIC_OBJECTS (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358045079fb9cf52ad1fd0c8969f54723c7f02d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647396"
---
# <a name="mf_mt_spatial_audio_max_dynamic_objects-attribute"></a><span data-ttu-id="80495-103">\_ \_ \_ Атрибут пространственного звука ( \_ Максимальное \_ число \_ объектов) MF MT</span><span class="sxs-lookup"><span data-stu-id="80495-103">MF\_MT\_SPATIAL\_AUDIO\_MAX\_DYNAMIC\_OBJECTS attribute</span></span>

<span data-ttu-id="80495-104">Указывает максимальное число динамических звуковых объектов, которые могут быть отображены в конечной точке аудио симулатанеаусли.</span><span class="sxs-lookup"><span data-stu-id="80495-104">Specifies the maximum number of dynamic audio objects that can be rendered by the audio endpoint simulataneously.</span></span>

## <a name="data-type"></a><span data-ttu-id="80495-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="80495-105">Data type</span></span>

<span data-ttu-id="80495-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="80495-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="80495-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80495-107">Remarks</span></span>

<span data-ttu-id="80495-108">[**Имфспатиалаудиосампле**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample) может содержать меньше выборок, чем число, указанное этим атрибутом.</span><span class="sxs-lookup"><span data-stu-id="80495-108">An [**IMFSpatialAudioSample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample) may contain fewer samples than the number specified by this attribute.</span></span> <span data-ttu-id="80495-109">Если образец содержит больше звуковых объектов, чем указано этим атрибутом, поведение не определено.</span><span class="sxs-lookup"><span data-stu-id="80495-109">If a sample contains more audio objects than specified by this attribute, the behavior is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="80495-110">Требования</span><span class="sxs-lookup"><span data-stu-id="80495-110">Requirements</span></span>



| <span data-ttu-id="80495-111">Требование</span><span class="sxs-lookup"><span data-stu-id="80495-111">Requirement</span></span> | <span data-ttu-id="80495-112">Значение</span><span class="sxs-lookup"><span data-stu-id="80495-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="80495-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80495-113">Minimum supported client</span></span><br/> | <span data-ttu-id="80495-114">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="80495-114">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="80495-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80495-115">Minimum supported server</span></span><br/> | <span data-ttu-id="80495-116">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="80495-116">None supported</span></span><br/>                                                          |
| <span data-ttu-id="80495-117">Header</span><span class="sxs-lookup"><span data-stu-id="80495-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="80495-118"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="80495-118"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




