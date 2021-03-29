---
description: Видеодекодер Media Foundation DV — это Media Foundation преобразование, которое декодирует видео в форматах DV.
ms.assetid: 97e5ba52-92fc-49e4-9c22-6f61bfda2003
title: Видеодекодер DV
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed277c3e4dd1aaa031d4dcf4694c7c3051fe37ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808093"
---
# <a name="dv-video-decoder"></a><span data-ttu-id="84431-103">Видеодекодер DV</span><span class="sxs-lookup"><span data-stu-id="84431-103">DV Video Decoder</span></span>

<span data-ttu-id="84431-104">Видеодекодер Media Foundation DV — это [Media Foundation преобразование](media-foundation-transforms.md) , которое декодирует видео в форматах DV.</span><span class="sxs-lookup"><span data-stu-id="84431-104">The Media Foundation DV video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that decodes DV video.</span></span>

<span data-ttu-id="84431-105">Декодер DV Video поддерживает следующие типы входных данных:</span><span class="sxs-lookup"><span data-stu-id="84431-105">The DV video decoder supports the following input types:</span></span>



| <span data-ttu-id="84431-106">Subtype</span><span class="sxs-lookup"><span data-stu-id="84431-106">Subtype</span></span>                 | <span data-ttu-id="84431-107">Описание</span><span class="sxs-lookup"><span data-stu-id="84431-107">Description</span></span>                  |
|-------------------------|------------------------------|
| <span data-ttu-id="84431-108">**Мфвидеоформат \_ DVC**</span><span class="sxs-lookup"><span data-stu-id="84431-108">**MFVideoFormat\_DVC**</span></span>  | <span data-ttu-id="84431-109">Видео DVC/DV</span><span class="sxs-lookup"><span data-stu-id="84431-109">DVC/DV Video</span></span>                 |
| <span data-ttu-id="84431-110">**Мфвидеоформат \_ двхд**</span><span class="sxs-lookup"><span data-stu-id="84431-110">**MFVideoFormat\_DVHD**</span></span> | <span data-ttu-id="84431-111">HD-ДВКР (1125-60 или 1250-50)</span><span class="sxs-lookup"><span data-stu-id="84431-111">HD-DVCR (1125-60 or 1250-50)</span></span> |
| <span data-ttu-id="84431-112">**Мфвидеоформат \_ двсд**</span><span class="sxs-lookup"><span data-stu-id="84431-112">**MFVideoFormat\_DVSD**</span></span> | <span data-ttu-id="84431-113">SDL-ДВКР (525-60 или 625-50)</span><span class="sxs-lookup"><span data-stu-id="84431-113">SDL-DVCR (525-60 or 625-50)</span></span>  |
| <span data-ttu-id="84431-114">**Мфвидеоформат \_ двсл**</span><span class="sxs-lookup"><span data-stu-id="84431-114">**MFVideoFormat\_DVSL**</span></span> | <span data-ttu-id="84431-115">SD-ДВКР (525-60 или 625-50)</span><span class="sxs-lookup"><span data-stu-id="84431-115">SD-DVCR (525-60 or 625-50)</span></span>   |



 

<span data-ttu-id="84431-116">Он поддерживает один тип выходных данных:</span><span class="sxs-lookup"><span data-stu-id="84431-116">It supports a single output type:</span></span>



| <span data-ttu-id="84431-117">Subtype</span><span class="sxs-lookup"><span data-stu-id="84431-117">Subtype</span></span>             | <span data-ttu-id="84431-118">Описание</span><span class="sxs-lookup"><span data-stu-id="84431-118">Description</span></span> |
|---------------------|-------------|
| <span data-ttu-id="84431-119">Мфвидеоформат \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="84431-119">MFVideoFormat\_YUY2</span></span> | <span data-ttu-id="84431-120">Видео YUY2</span><span class="sxs-lookup"><span data-stu-id="84431-120">YUY2 video</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="84431-121">Требования</span><span class="sxs-lookup"><span data-stu-id="84431-121">Requirements</span></span>



| <span data-ttu-id="84431-122">Требование</span><span class="sxs-lookup"><span data-stu-id="84431-122">Requirement</span></span> | <span data-ttu-id="84431-123">Значение</span><span class="sxs-lookup"><span data-stu-id="84431-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="84431-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84431-124">Minimum supported client</span></span><br/> | <span data-ttu-id="84431-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="84431-125">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="84431-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84431-126">Minimum supported server</span></span><br/> | <span data-ttu-id="84431-127">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="84431-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="84431-128">DLL</span><span class="sxs-lookup"><span data-stu-id="84431-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84431-129"><dt>Mfdvdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84431-129"><dt>Mfdvdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84431-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84431-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84431-131">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="84431-131">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="84431-132">Поддерживаемые форматы мультимедиа в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="84431-132">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="84431-133">Типы видеоклипов</span><span class="sxs-lookup"><span data-stu-id="84431-133">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 




