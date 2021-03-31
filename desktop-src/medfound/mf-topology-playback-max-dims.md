---
description: Задает размер окна назначения для воспроизведения видео.
ms.assetid: 46af4c11-042c-4580-ba9d-3aee6172de56
title: Атрибут MF_TOPOLOGY_PLAYBACK_MAX_DIMS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1fc6a57c5e031bc6f35f36e688bd44986f541b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263615"
---
# <a name="mf_topology_playback_max_dims-attribute"></a><span data-ttu-id="45605-103">\_ \_ Максимальный размер для воспроизведения топологии \_ MF \_</span><span class="sxs-lookup"><span data-stu-id="45605-103">MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS attribute</span></span>

<span data-ttu-id="45605-104">Задает размер окна назначения для воспроизведения видео.</span><span class="sxs-lookup"><span data-stu-id="45605-104">Specifies the size of the destination window for video playback.</span></span>

## <a name="data-type"></a><span data-ttu-id="45605-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="45605-105">Data type</span></span>

<span data-ttu-id="45605-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="45605-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="45605-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="45605-107">Get/set</span></span>

<span data-ttu-id="45605-108">Чтобы получить этот атрибут, вызовите [**мфжетаттрибутесизе**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize).</span><span class="sxs-lookup"><span data-stu-id="45605-108">To get this attribute, call [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize).</span></span>

<span data-ttu-id="45605-109">Чтобы задать этот атрибут, вызовите [**мфсетаттрибутесизе**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize).</span><span class="sxs-lookup"><span data-stu-id="45605-109">To set this attribute, call [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize).</span></span>

## <a name="applies-to"></a><span data-ttu-id="45605-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="45605-110">Applies to</span></span>

[<span data-ttu-id="45605-111">**имфтопологи**</span><span class="sxs-lookup"><span data-stu-id="45605-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="45605-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45605-112">Remarks</span></span>

<span data-ttu-id="45605-113">Загрузчик топологии использует этот атрибут для оптимизации конвейера перед началом воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="45605-113">The topology loader uses this attribute to optimize the pipeline before playback starts.</span></span> <span data-ttu-id="45605-114">Если этот атрибут задан, также установите для атрибута [" \_ \_ \_ \_ Оптимизация воспроизведения статических топологий MF](mf-topology-static-playback-optimizations.md) " **значение true**.</span><span class="sxs-lookup"><span data-stu-id="45605-114">If you set this attribute, also set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="45605-115">Верхние 32 бит значения атрибута содержат ширину, а младшие 32 бита содержат высоту в пикселях.</span><span class="sxs-lookup"><span data-stu-id="45605-115">The upper 32 bits of the attribute value contain the width and the lower 32 bits contain the height, both in pixels.</span></span>

<span data-ttu-id="45605-116">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="45605-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="45605-117">Требования</span><span class="sxs-lookup"><span data-stu-id="45605-117">Requirements</span></span>



| <span data-ttu-id="45605-118">Требование</span><span class="sxs-lookup"><span data-stu-id="45605-118">Requirement</span></span> | <span data-ttu-id="45605-119">Значение</span><span class="sxs-lookup"><span data-stu-id="45605-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="45605-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45605-120">Minimum supported client</span></span><br/> | <span data-ttu-id="45605-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="45605-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="45605-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45605-122">Minimum supported server</span></span><br/> | <span data-ttu-id="45605-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="45605-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="45605-124">Header</span><span class="sxs-lookup"><span data-stu-id="45605-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="45605-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="45605-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45605-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45605-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45605-127">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="45605-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="45605-128">Атрибуты топологии</span><span class="sxs-lookup"><span data-stu-id="45605-128">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="45605-129">Управление качеством видео</span><span class="sxs-lookup"><span data-stu-id="45605-129">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




