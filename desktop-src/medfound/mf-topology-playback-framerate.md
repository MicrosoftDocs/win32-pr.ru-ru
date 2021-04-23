---
description: Указывает частоту обновления монитора.
ms.assetid: deeb780c-2dc2-4a9a-926a-23b9ae3bedd5
title: Атрибут MF_TOPOLOGY_PLAYBACK_FRAMERATE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620d7ff7dbc893065ebb378557f0731cd8826582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263616"
---
# <a name="mf_topology_playback_framerate-attribute"></a><span data-ttu-id="0e893-103">\_ \_ Атрибут частоты воспроизведения для топологии MF \_</span><span class="sxs-lookup"><span data-stu-id="0e893-103">MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE attribute</span></span>

<span data-ttu-id="0e893-104">Указывает частоту обновления монитора.</span><span class="sxs-lookup"><span data-stu-id="0e893-104">Specifies the monitor refresh rate.</span></span>

## <a name="data-type"></a><span data-ttu-id="0e893-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0e893-105">Data type</span></span>

<span data-ttu-id="0e893-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="0e893-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="0e893-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="0e893-107">Get/set</span></span>

<span data-ttu-id="0e893-108">Чтобы получить этот атрибут, вызовите [**мфжетаттрибутератио**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="0e893-108">To get this attribute, call [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span></span>

<span data-ttu-id="0e893-109">Чтобы задать этот атрибут, вызовите [**мфсетаттрибутератио**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="0e893-109">To set this attribute, call [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span></span>

## <a name="applies-to"></a><span data-ttu-id="0e893-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="0e893-110">Applies to</span></span>

[<span data-ttu-id="0e893-111">**имфтопологи**</span><span class="sxs-lookup"><span data-stu-id="0e893-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="0e893-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e893-112">Remarks</span></span>

<span data-ttu-id="0e893-113">Загрузчик топологии использует этот атрибут для оптимизации конвейера перед началом воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0e893-113">The topology loader uses this attribute to optimize the pipeline before playback starts.</span></span> <span data-ttu-id="0e893-114">Если этот атрибут задан, также установите для атрибута [" \_ \_ \_ \_ Оптимизация воспроизведения статических топологий MF](mf-topology-static-playback-optimizations.md) " **значение true**.</span><span class="sxs-lookup"><span data-stu-id="0e893-114">If you set this attribute, also set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="0e893-115">Частота кадров выражается в виде коэффициента.</span><span class="sxs-lookup"><span data-stu-id="0e893-115">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="0e893-116">Верхние 32 бит значения атрибута содержат числитель, а младшие 32 биты содержат знаменатель.</span><span class="sxs-lookup"><span data-stu-id="0e893-116">The upper 32 bits of the attribute value contain the numerator, and the lower 32 bits contain the denominator.</span></span>

<span data-ttu-id="0e893-117">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="0e893-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e893-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0e893-118">Requirements</span></span>



| <span data-ttu-id="0e893-119">Требование</span><span class="sxs-lookup"><span data-stu-id="0e893-119">Requirement</span></span> | <span data-ttu-id="0e893-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0e893-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0e893-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e893-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0e893-122">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0e893-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0e893-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e893-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0e893-124">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0e893-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0e893-125">Header</span><span class="sxs-lookup"><span data-stu-id="0e893-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e893-126"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e893-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e893-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e893-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e893-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0e893-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0e893-129">Атрибуты топологии</span><span class="sxs-lookup"><span data-stu-id="0e893-129">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="0e893-130">Управление качеством видео</span><span class="sxs-lookup"><span data-stu-id="0e893-130">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




