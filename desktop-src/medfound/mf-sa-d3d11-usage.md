---
description: Указывает, как выделить поверхности Microsoft Direct3D 11 для образцов мультимедиа.
ms.assetid: E9A415FA-74BF-4822-BB0E-D8AAA7D73664
title: Атрибут MF_SA_D3D11_USAGE (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0609435cf42134f28e8464fd3173412836c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263364"
---
# <a name="mf_sa_d3d11_usage-attribute"></a><span data-ttu-id="d56b7-103">\_ \_ Атрибут использования D3D11 SA для MF \_</span><span class="sxs-lookup"><span data-stu-id="d56b7-103">MF\_SA\_D3D11\_USAGE attribute</span></span>

<span data-ttu-id="d56b7-104">Указывает, как выделить поверхности Microsoft Direct3D 11 для образцов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d56b7-104">Specifies how to allocate Microsoft Direct3D 11 surfaces for media samples.</span></span> <span data-ttu-id="d56b7-105">Использование показывает, доступен ли образец для ЦП или GPU.</span><span class="sxs-lookup"><span data-stu-id="d56b7-105">The usage directly reflects whether a sample is accessible by the CPU or GPU.</span></span>

## <a name="data-type"></a><span data-ttu-id="d56b7-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d56b7-106">Data type</span></span>

<span data-ttu-id="d56b7-107">**D3D11 \_ Использование** хранится как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="d56b7-107">**D3D11\_USAGE** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d56b7-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d56b7-108">Remarks</span></span>

<span data-ttu-id="d56b7-109">Значение этого атрибута является значением [**\_ использования D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) .</span><span class="sxs-lookup"><span data-stu-id="d56b7-109">The value of this attribute is a [**D3D11\_USAGE**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) value.</span></span>

### <a name="microsoft-media-foundation-transforms"></a><span data-ttu-id="d56b7-110">Преобразования Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d56b7-110">Microsoft Media Foundation Transforms</span></span>

<span data-ttu-id="d56b7-111">В этом контексте атрибут применяется только в том случае, если преобразование Microsoft Media Foundation (MFT) возвращает **true** для атрибута [MF \_ SA D3D11 с \_ \_ поддержкой](mf-sa-d3d11-aware.md) .</span><span class="sxs-lookup"><span data-stu-id="d56b7-111">In this context, the attribute applies only when the Microsoft Media Foundation transform (MFT) returns **TRUE** for the [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) attribute.</span></span>

<span data-ttu-id="d56b7-112">Если файл MFT поддерживает Direct3D 11, этот атрибут предоставляет указание для MFT при выделении поверхностей Microsoft Direct3D для вывода.</span><span class="sxs-lookup"><span data-stu-id="d56b7-112">If an MFT supports Direct3D 11, this attribute provides a hint to the MFT when allocating Microsoft Direct3D surfaces for output.</span></span> <span data-ttu-id="d56b7-113">Задайте атрибут следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d56b7-113">Set the attribute as follows:</span></span>

1.  <span data-ttu-id="d56b7-114">Вызовите [**имфтрансформ:: жетаутпутстреаматтрибутес**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) , чтобы получить хранилище атрибутов MFT.</span><span class="sxs-lookup"><span data-stu-id="d56b7-114">Call [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) to get the MFT attribute store.</span></span>
2.  <span data-ttu-id="d56b7-115">Вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="d56b7-115">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="d56b7-116">Конвейер Media Foundation задает атрибут перед запуском потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="d56b7-116">The Media Foundation pipeline sets the attribute before streaming starts.</span></span> <span data-ttu-id="d56b7-117">MFT должна попытаться учитывать параметр при выделении поверхностей.</span><span class="sxs-lookup"><span data-stu-id="d56b7-117">The MFT should attempt to honor the setting when it allocates surfaces.</span></span> <span data-ttu-id="d56b7-118">Если это невозможно, MFT может игнорировать атрибут вместо сбоя выделения.</span><span class="sxs-lookup"><span data-stu-id="d56b7-118">If that is not possible, the MFT can ignore the attribute, rather than failing the allocation.</span></span>

<span data-ttu-id="d56b7-119">Кроме того, если в MFT требуются поверхности Direct3D для входных данных, он может предоставить этот атрибут как подсказку для выделения поверхностей ввода.</span><span class="sxs-lookup"><span data-stu-id="d56b7-119">In addition, if the MFT requires Direct3D surfaces for input, it can expose this attribute as a hint for how the input surfaces should be allocated.</span></span> <span data-ttu-id="d56b7-120">Запросите атрибут следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d56b7-120">Query the attribute as follows:</span></span>

1.  <span data-ttu-id="d56b7-121">Вызовите метод [**имфтрансформ:: жетинпутстреаматтрибутес**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) , чтобы получить атрибуты входного потока.</span><span class="sxs-lookup"><span data-stu-id="d56b7-121">Call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) to get the input stream attributes.</span></span>
2.  <span data-ttu-id="d56b7-122">Вызовите [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="d56b7-122">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="d56b7-123">Выборка распределителя</span><span class="sxs-lookup"><span data-stu-id="d56b7-123">Sample Allocator</span></span>

<span data-ttu-id="d56b7-124">Этот атрибут можно задать в примере распределителя видео в методе [**имфвидеосамплеаллокаторекс:: инитиализесамплеаллокаторекс**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="d56b7-124">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d56b7-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d56b7-125">Requirements</span></span>



| <span data-ttu-id="d56b7-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d56b7-126">Requirement</span></span> | <span data-ttu-id="d56b7-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d56b7-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d56b7-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d56b7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d56b7-129">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="d56b7-129">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="d56b7-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d56b7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d56b7-131">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="d56b7-131">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="d56b7-132">Header</span><span class="sxs-lookup"><span data-stu-id="d56b7-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d56b7-133"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="d56b7-133"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d56b7-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d56b7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d56b7-135">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d56b7-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
