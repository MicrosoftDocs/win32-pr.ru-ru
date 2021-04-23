---
description: Указывает, сколько буферов распределительного примера видеороликов создается для каждого примера видео.
ms.assetid: A782BF8A-822A-407D-A30A-F2045BBB0BC0
title: Атрибут MF_SA_BUFFERS_PER_SAMPLE (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d658ae72c53d986b364b2b6a3f405ae0052ea3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811032"
---
# <a name="mf_sa_buffers_per_sample-attribute"></a><span data-ttu-id="2c8ec-103">\_ \_ Буферов SA MF \_ на \_ Пример атрибута</span><span class="sxs-lookup"><span data-stu-id="2c8ec-103">MF\_SA\_BUFFERS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="2c8ec-104">Указывает, сколько буферов распределительного примера видеороликов создается для каждого примера видео.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-104">Specifies how many buffers the video-sample allocator creates for each video sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="2c8ec-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2c8ec-105">Data type</span></span>

<span data-ttu-id="2c8ec-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2c8ec-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c8ec-107">Remarks</span></span>

<span data-ttu-id="2c8ec-108">Если для выделения видеороликов используется интерфейс [**имфвидеосамплеаллокаторекс**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) , этот атрибут можно использовать для создания видеороликов, содержащих несколько буферов.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-108">If you use the [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) interface to allocate video samples, you can use this attribute to create video samples that contain multiple buffers.</span></span> <span data-ttu-id="2c8ec-109">Например, если значение атрибута равно 2, распределитель создает два буфера видео для каждого примера видео.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-109">For example, if the attribute value is 2, the allocator creates two video buffers for each video sample.</span></span> <span data-ttu-id="2c8ec-110">Задайте атрибут в параметре *паттрибутес* метода [**Имфвидеосамплеаллокаторекс:: инитиализесамплеаллокаторекс**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="2c8ec-110">Set the attribute in the *pAttributes* parameter of the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

<span data-ttu-id="2c8ec-111">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-111">The default value is 1.</span></span> <span data-ttu-id="2c8ec-112">Если атрибут не задан, распределитель создает образцы видео, содержащие один буфер на выборку.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-112">If the attribute is not set, the allocator creates video samples that contain a single buffer per sample.</span></span>

<span data-ttu-id="2c8ec-113">Этот атрибут в основном предназначен для Media Foundation преобразований (МФТС), поддерживающих вывод стерео трехмерного вывода, в следующей ситуации:</span><span class="sxs-lookup"><span data-stu-id="2c8ec-113">This attribute is primarily intended for Media Foundation transforms (MFTs) that support stereo 3D output, in the following situation:</span></span>

-   <span data-ttu-id="2c8ec-114">MFT поддерживает графическую инфраструктуру Microsoft DirectX (DXGI).</span><span class="sxs-lookup"><span data-stu-id="2c8ec-114">The MFT supports Microsoft DirectX Graphics Infrastructure (DXGI).</span></span>
-   <span data-ttu-id="2c8ec-115">MFT выделяет свои собственные выходные примеры.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-115">The MFT allocates its own output samples.</span></span>
-   <span data-ttu-id="2c8ec-116">В MFT для выделения выходных образцов используется интерфейс [**имфвидеосамплеаллокаторекс**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="2c8ec-116">The MFT uses the [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) interface to allocate the output samples.</span></span>
-   <span data-ttu-id="2c8ec-117">В трехмерном видеоформате для каждого представления используется отдельный буфер.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-117">The 3D video format uses a separate buffer for each view.</span></span>

<span data-ttu-id="2c8ec-118">Если все эти условия имеют значение true, MFT должно установить для атрибута значение 2 (один буфер для представления).</span><span class="sxs-lookup"><span data-stu-id="2c8ec-118">If all of these criteria are true, the MFT should set the attribute value to 2 (one buffer per view).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c8ec-119">Требования</span><span class="sxs-lookup"><span data-stu-id="2c8ec-119">Requirements</span></span>



| <span data-ttu-id="2c8ec-120">Требование</span><span class="sxs-lookup"><span data-stu-id="2c8ec-120">Requirement</span></span> | <span data-ttu-id="2c8ec-121">Значение</span><span class="sxs-lookup"><span data-stu-id="2c8ec-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c8ec-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c8ec-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2c8ec-123">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="2c8ec-123">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="2c8ec-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c8ec-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2c8ec-125">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="2c8ec-125">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="2c8ec-126">Header</span><span class="sxs-lookup"><span data-stu-id="2c8ec-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c8ec-127"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c8ec-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c8ec-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c8ec-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c8ec-129">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2c8ec-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




