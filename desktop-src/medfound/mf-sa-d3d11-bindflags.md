---
description: Задает флаги привязки, используемые при выделении поверхностей Microsoft Direct3D 11 для образцов мультимедиа.
ms.assetid: C3B475B1-9A44-47EA-BCE7-D3D0FB56DDAC
title: Атрибут MF_SA_D3D11_BINDFLAGS (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb5ae4161a6782a3ea7a69b471044e43c5ee7a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345835"
---
# <a name="mf_sa_d3d11_bindflags-attribute"></a><span data-ttu-id="62881-103">\_Атрибут MF SA \_ D3D11 \_ биндфлагс</span><span class="sxs-lookup"><span data-stu-id="62881-103">MF\_SA\_D3D11\_BINDFLAGS attribute</span></span>

<span data-ttu-id="62881-104">Задает флаги привязки, используемые при выделении поверхностей Microsoft Direct3D 11 для образцов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="62881-104">Specifies the binding flags to use when allocating Microsoft Direct3D 11 surfaces for media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="62881-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="62881-105">Data type</span></span>

<span data-ttu-id="62881-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="62881-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="62881-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62881-107">Remarks</span></span>

<span data-ttu-id="62881-108">Значение этого атрибута является побитовым **или** для флагов [**\_ \_ флага привязки D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) .</span><span class="sxs-lookup"><span data-stu-id="62881-108">The value of this attribute is a bitwise **OR** of [**D3D11\_BIND\_FLAG**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) flags.</span></span>

### <a name="microsoft-media-foundation-transforms"></a><span data-ttu-id="62881-109">Преобразования Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="62881-109">Microsoft Media Foundation Transforms</span></span>

<span data-ttu-id="62881-110">В этом контексте атрибут применяется только в том случае, если преобразование Microsoft Media Foundation (MFT) возвращает **true** для атрибута [MF \_ SA D3D11 с \_ \_ поддержкой](mf-sa-d3d11-aware.md) .</span><span class="sxs-lookup"><span data-stu-id="62881-110">In this context, the attribute applies only when the Microsoft Media Foundation transform (MFT) returns **TRUE** for the [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) attribute.</span></span>

<span data-ttu-id="62881-111">Если файл MFT поддерживает Direct3D 11, этот атрибут предоставляет указание для MFT при выделении поверхностей Microsoft Direct3D для вывода.</span><span class="sxs-lookup"><span data-stu-id="62881-111">If an MFT supports Direct3D 11, this attribute provides a hint to the MFT when allocating Microsoft Direct3D surfaces for output.</span></span> <span data-ttu-id="62881-112">Задайте атрибут следующим образом:</span><span class="sxs-lookup"><span data-stu-id="62881-112">Set the attribute as follows:</span></span>

1.  <span data-ttu-id="62881-113">Вызовите [**имфтрансформ:: жетаутпутстреаматтрибутес**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) , чтобы получить хранилище атрибутов MFT.</span><span class="sxs-lookup"><span data-stu-id="62881-113">Call [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) to get the MFT attribute store.</span></span>
2.  <span data-ttu-id="62881-114">Вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="62881-114">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="62881-115">Конвейер Media Foundation задает атрибут перед запуском потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="62881-115">The Media Foundation pipeline sets the attribute before streaming starts.</span></span> <span data-ttu-id="62881-116">MFT должна попытаться учитывать параметр при выделении поверхностей.</span><span class="sxs-lookup"><span data-stu-id="62881-116">The MFT should attempt to honor the setting when it allocates surfaces.</span></span> <span data-ttu-id="62881-117">Если это невозможно, MFT может игнорировать атрибут вместо сбоя выделения.</span><span class="sxs-lookup"><span data-stu-id="62881-117">If that is not possible, the MFT can ignore the attribute, rather than failing the allocation.</span></span>

<span data-ttu-id="62881-118">Кроме того, если в MFT требуются поверхности Direct3D для входных данных, он может предоставить этот атрибут как подсказку для выделения поверхностей ввода.</span><span class="sxs-lookup"><span data-stu-id="62881-118">In addition, if the MFT requires Direct3D surfaces for input, it can expose this attribute as a hint for how the input surfaces should be allocated.</span></span> <span data-ttu-id="62881-119">Запросите атрибут следующим образом:</span><span class="sxs-lookup"><span data-stu-id="62881-119">Query the attribute as follows:</span></span>

1.  <span data-ttu-id="62881-120">Вызовите метод [**имфтрансформ:: жетинпутстреаматтрибутес**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) , чтобы получить атрибуты входного потока.</span><span class="sxs-lookup"><span data-stu-id="62881-120">Call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) to get the input stream attributes.</span></span>
2.  <span data-ttu-id="62881-121">Вызовите [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="62881-121">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="62881-122">Выборка распределителя</span><span class="sxs-lookup"><span data-stu-id="62881-122">Sample Allocator</span></span>

<span data-ttu-id="62881-123">Этот атрибут можно задать в примере распределителя видео в методе [**имфвидеосамплеаллокаторекс:: инитиализесамплеаллокаторекс**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="62881-123">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="62881-124">Требования</span><span class="sxs-lookup"><span data-stu-id="62881-124">Requirements</span></span>



| <span data-ttu-id="62881-125">Требование</span><span class="sxs-lookup"><span data-stu-id="62881-125">Requirement</span></span> | <span data-ttu-id="62881-126">Значение</span><span class="sxs-lookup"><span data-stu-id="62881-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="62881-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62881-127">Minimum supported client</span></span><br/> | <span data-ttu-id="62881-128">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="62881-128">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="62881-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62881-129">Minimum supported server</span></span><br/> | <span data-ttu-id="62881-130">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="62881-130">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="62881-131">Header</span><span class="sxs-lookup"><span data-stu-id="62881-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="62881-132"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="62881-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62881-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62881-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62881-134">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="62881-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
