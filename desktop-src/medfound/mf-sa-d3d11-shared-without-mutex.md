---
description: Указывает распределительу образцов видео для создания текстур с общим доступом с помощью устаревшего механизма.
ms.assetid: A9F4D4AF-BB47-48E2-B40A-D0245FD61FAF
title: Атрибут MF_SA_D3D11_SHARED_WITHOUT_MUTEX (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9139328c9d272007be6e5cd9434614cb1de8c9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701703"
---
# <a name="mf_sa_d3d11_shared_without_mutex-attribute"></a><span data-ttu-id="453d3-103">MF \_ SA \_ D3D11 \_ Shared \_ без \_ атрибута мьютекса</span><span class="sxs-lookup"><span data-stu-id="453d3-103">MF\_SA\_D3D11\_SHARED\_WITHOUT\_MUTEX attribute</span></span>

<span data-ttu-id="453d3-104">Указывает распределительу образцов видео для создания текстур с общим доступом с помощью устаревшего механизма.</span><span class="sxs-lookup"><span data-stu-id="453d3-104">Indicates to the video sample allocator to create textures as shareable using the legacy mechanism.</span></span>

## <a name="data-type"></a><span data-ttu-id="453d3-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="453d3-105">Data type</span></span>

<span data-ttu-id="453d3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="453d3-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="453d3-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="453d3-107">Remarks</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="453d3-108">Выборка распределителя</span><span class="sxs-lookup"><span data-stu-id="453d3-108">Sample Allocator</span></span>

<span data-ttu-id="453d3-109">Этот атрибут можно задать в примере распределителя видео в методе [**имфвидеосамплеаллокаторекс:: инитиализесамплеаллокаторекс**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="453d3-109">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="453d3-110">Требования</span><span class="sxs-lookup"><span data-stu-id="453d3-110">Requirements</span></span>



| <span data-ttu-id="453d3-111">Требование</span><span class="sxs-lookup"><span data-stu-id="453d3-111">Requirement</span></span> | <span data-ttu-id="453d3-112">Значение</span><span class="sxs-lookup"><span data-stu-id="453d3-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="453d3-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="453d3-113">Minimum supported client</span></span><br/> | <span data-ttu-id="453d3-114">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="453d3-114">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="453d3-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="453d3-115">Minimum supported server</span></span><br/> | <span data-ttu-id="453d3-116">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="453d3-116">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="453d3-117">Header</span><span class="sxs-lookup"><span data-stu-id="453d3-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="453d3-118"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="453d3-118"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="453d3-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="453d3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="453d3-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="453d3-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="453d3-121">**Имфвидеосамплеаллокаторекс:: Инитиализесамплеаллокаторекс**</span><span class="sxs-lookup"><span data-stu-id="453d3-121">**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)
</dt> <dt>

[<span data-ttu-id="453d3-122">MF \_ SA \_ D3D11 \_ Shared</span><span class="sxs-lookup"><span data-stu-id="453d3-122">MF\_SA\_D3D11\_SHARED</span></span>](mf-sa-d3d11-shared.md)
</dt> </dl>

 

 




