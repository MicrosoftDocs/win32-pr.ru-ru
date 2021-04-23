---
description: Указывает количество несжатых буферов, которые требуются для работы приемника мультимедиа расширенного модуля подготовки видео (Евр).
ms.assetid: b62bff64-153f-4028-a546-250419dc4152
title: Атрибут MF_SA_REQUIRED_SAMPLE_COUNT (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe7d47370cd4877a0f9722d443bc6bb3f7bdeb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712253"
---
# <a name="mf_sa_required_sample_count-attribute"></a><span data-ttu-id="f6d22-103">\_ \_ \_ Атрибут количества выборок для сопоставления MF \_</span><span class="sxs-lookup"><span data-stu-id="f6d22-103">MF\_SA\_REQUIRED\_SAMPLE\_COUNT attribute</span></span>

<span data-ttu-id="f6d22-104">Указывает количество несжатых буферов, которые требуются для работы приемника мультимедиа расширенного модуля подготовки видео (Евр).</span><span class="sxs-lookup"><span data-stu-id="f6d22-104">Indicates the number of uncompressed buffers that the enhanced video renderer (EVR) media sink requires for deinterlacing.</span></span>

## <a name="data-type"></a><span data-ttu-id="f6d22-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f6d22-105">Data type</span></span>

<span data-ttu-id="f6d22-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f6d22-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f6d22-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6d22-107">Remarks</span></span>

<span data-ttu-id="f6d22-108">Это атрибут уровня потока.</span><span class="sxs-lookup"><span data-stu-id="f6d22-108">This is a stream-level attribute.</span></span> <span data-ttu-id="f6d22-109">Чтобы получить атрибут из евр, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f6d22-109">To get the attribute from the EVR, do the following:</span></span>

1.  <span data-ttu-id="f6d22-110">Вызовите [**имфмедиасинк:: жетстреамсинкбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) , чтобы получить приемник потока.</span><span class="sxs-lookup"><span data-stu-id="f6d22-110">Call [**IMFMediaSink::GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) to get the stream sink.</span></span>
2.  <span data-ttu-id="f6d22-111">Запросите приемник потока для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="f6d22-111">Query the stream sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>
3.  <span data-ttu-id="f6d22-112">Вызовите [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f6d22-112">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="f6d22-113">На внутреннем уровне микшер предоставляет этот атрибут для Евр.</span><span class="sxs-lookup"><span data-stu-id="f6d22-113">Internally, the mixer provides this attribute to the EVR.</span></span> <span data-ttu-id="f6d22-114">Чтобы получить атрибут из микшера, вызовите метод [**имфтрансформ:: жетинпутстреаматтрибутес**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes).</span><span class="sxs-lookup"><span data-stu-id="f6d22-114">To get the attribute from the mixer, call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes).</span></span>

<span data-ttu-id="f6d22-115">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="f6d22-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6d22-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f6d22-116">Requirements</span></span>



| <span data-ttu-id="f6d22-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f6d22-117">Requirement</span></span> | <span data-ttu-id="f6d22-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f6d22-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6d22-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6d22-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f6d22-120">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="f6d22-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="f6d22-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6d22-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f6d22-122">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="f6d22-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f6d22-123">Header</span><span class="sxs-lookup"><span data-stu-id="f6d22-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6d22-124"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6d22-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6d22-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6d22-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6d22-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f6d22-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f6d22-127">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="f6d22-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f6d22-128">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f6d22-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f6d22-129">Атрибуты Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f6d22-129">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




